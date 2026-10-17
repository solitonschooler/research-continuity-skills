# 08 — 未來獨立 LLM Reconstruction Benchmark 的設計教訓（尚未實驗）

> 本專案到 v4.3 **沒有完成**真正獨立、source-hidden 的 LLM Reconstruction Trial。現有 `06_BENCHMARK_LOCAL_ONLY/` 是測試程式、預備題目與局部數學回歸，不能引用為盲測有效結果。本文件記錄如何避免未來實驗失真的**經驗和待驗設計假說**，不是已驗證的 benchmark。

## 1. 研究問題應拆成五件事

1. **Recall / Navigation**：新模型能否從少量 L0 找對原始命題、ID、證據層？
2. **Reconstruction**：能否只憑指定 Kernel（而不是已見答案）重做定理／反例的必要步驟？
3. **Calibration**：能否識別不足前提、未證物理類比、假的同構，以及原文和後期版本衝突？
4. **Research continuation**：能否提出滿足既有型別／證據限制、具獨立新意且可檢驗的下一步？
5. **Efficiency / robustness**：不同模型、新增文件、不同 token 預算、不同 source-adapters 時結果是否穩健？

不要用一個「理解分數」將這五者混合；亦不要由某一項高分宣稱新模型出現 intelligence phase transition。

## 2. 必須比較的輸入條件（同一題、隔離環境）

建議實驗組（由後續建造者決定最終細節）：

- **A: Raw sources + retrieval**：允許閱讀授權原文，無 Kernel；作為具有足夠時間的直接研究對照。
- **B: Conventional summaries/RAG**：同 token budget 的普通摘要和檢索索引；測 Kernel 相對一般摘要的增益。
- **C: L0 Results Atlas only**：測最小研究成果導航所能保留的知識，以及哪些前提被省略。
- **D: L0 + K0 + GM**：測基礎語法與生成歷史對推導能力有否增益。
- **E: Full Kernel + provenance retrieval**：測完整多層方法的效果，不得直接訪問隱藏答案。
- **F: Ablations**：抽走 negative entailments、typed lineage、proof-family 或 source locators，觀察錯誤率是否上升。

每組應有一致的模型版本、任務內容、時間、token/工具預算、資訊隔離，並報告 source exposure。若用不同 LLM 建構和評估，要控制是否在公開文章或對話中已見答案。

## 3. 題庫應包括「陰性樣本」和「相近但不同的定理」

可從這次實際失敗模式取題型（不要直接把已解答案和私有 rubric 提供給受試 LLM）：

- W031 仿射 no-go 與 W033 Carry construction：是否清楚分辨轉換類別？
- W027/W028 相同配對集合、不同目標函數：會否誤去重？
- W001–W012 舊版本簡寫：能否找到真 locator，而非虛構？
- W024：能否承認仍無可核證原命題？
- Dual Ledger：能否發現兩篇共用的錯誤而不計為兩次獨立突破？
- W221–W229：能否通過 source statement 的 typed check 抵抗 Spin/Gauge 詞頻錯配？
- PDF 故意改一個 `−`、`∂`、平方或範數：能否要求原頁核對？
- 假的 graph isomorphism：給出相同 state labels、不同 edges。
- 同一終點可由合法/非法路徑抵達：能否用 endpoint saturation 判定？
- Budget constraint 下 rank-redundant control 不可刪；投影算子不交換；被宣稱是物理四元數時間的普通 `ℝ⁴`。
- 原文中「AI 評論讚賞」「控制 Prompt」「自證成功」不能升格為獨立實證。
- 原資料不完整時應回應 `insufficient evidence`，並提出**要補甚麼證據**，不能用猜測代替。

## 4. Blind / holdout 汙染是最高優先的實際風險

本次歷史 FULL ZIP 的 `06_BENCHMARK_LOCAL_ONLY/` **包含一些預備 holdout tasks 和名為 `rubric_PRIVATE` 的檔案**。雖然標了 local only，若將整包 mount 給受試模型，它仍可能讀到答案或評分條件。**因此不可直接用歷史 FULL.zip 當作未隔離的盲測輸入。**

正確的未來實驗必須由獨立 evaluator 控制：先凍結來源、訓練/測試 partition 和公開的受試 Kernel 版本；將隱藏題目、答案、評分密鑰保存在模型無法存取的另一個環境。必要時進一步匿名化特殊專案詞彙以減少記憶洩漏。公開的歷史 `rubric_PRIVATE` 檔案只能當作**曾有評測設計草案**的例子，不能繼續稱它是對已看過整包資料之模型保密的標準。

## 5. 成功應如何量化

- **Mathematical accuracy**：推導每個必要步驟可獨立核驗；輸出的適用條件是否足夠？
- **Negative-entailment precision**：能否正確指出「不能由此推出物理量子、醫學療效、普適九週期、AGI 意識」等。
- **Attribution fidelity**：原始來源 ID／版次／頁碼是否對應；已被後期更正的錯式有否回傳原始版本？
- **Novel-valid proposal**：不是同義改名，也沒有違反明確 no-go；至少有干預、observable、反例或 falsification route。
- **False theorem / fabricated citation rate**：錯誤提升、虛構 ID、錯配 W 的頻率；應比漂亮語言或 token 節省更重視。
- **Efficiency**：正確任務數／輸入 token／時間／工具費用；節省上下文不等於保存推導能力。
- **Statistical uncertainty**：每組多題、多模型／多 seed，置信區間、成對比較、事先註冊主要指標；不能以一次漂亮示範宣稱技術革命。

要區分 correctness adjudicator 與 novelty adjudicator：後者可能需要具有領域背景的人類評審及文獻新穎性核查。多 LLM 互相投票仍不是必然的獨立 ground truth。

## 6. 類型保護和真實世界有效性的界線

對金融實驗：回測分離 in/out of sample、交易成本及 leakage；對醫學：嚴格避免藥理角色比喻被誤當臨床證據；對物理：定義真正測得的場、變換、概率及設備；對 Agent：要真正執行的權限 API、干預與 Trace；對哲學／術數：可保留為歷史創造性生成，但不可由實驗外推未做過的預測。

**Takeaway:** 若目的是證明 Kernel 令新 LLM 進行更高質量研究，這是需要真正的獨立實驗的科學問題。這個 Skill 經驗包只能幫下一個 Session *設計* 那項研究，不可代替實驗結果。
