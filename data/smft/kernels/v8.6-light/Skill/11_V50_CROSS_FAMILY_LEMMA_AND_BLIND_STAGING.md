# v5.0 實際經驗：跨 Proof Family 引理重建與盲測輸入隔離

**性質：** Kernelization 工作筆記（真實審核案例）；不是正式可執行 GitHub Skill，也不能代替外部實驗。

## A. 已實踐的跨家族證明縮併方法

這次並非按「Port、Trace、Projection」等詞聚類，而是把不同來源中真正相同的 proof shape 復原為通用引理：

`f factors through π ⇔ f constant on every π-fiber.`

它可以負責 `SRC-0234` Endpoint 的 validity indicator、`SRC-0261` Port 的聯合 transition/output、以及 `SRC-0237` 中 Truth 是否可由 internal event log 決定。但 **T、f、X、π、可干預集合、合法動作及真偽 oracle 不同**；統一引理後要在每一條 edge 保留量詞、型別、原頁碼、禁推論與歷史 Witness。實際建立 `GL50-01..06` 及 `CROSS_FAMILY_ENTAILMENT_GRAPH_v5.0.csv`，與舊 PF 分類相比，新增的是形式蘊涵關係，不是新 witness 數量。

## B. 本輪新發現的隱性條件：部分控制系統的合法動作域

`SRC-0261` p.6 原文本來就加了「已聲明狀態、操作及封閉性」條件；`SRC-0283` pp.9–10 要求所有 admissible finite words。在部分定義 transition 的系統內，僅檢查兩狀態*共同允許的動作*可能真空通過：兩個同一 Port 纖維狀態在可用動作的集合上仍可能不同。必須額外檢查 `A(s,u)` 是否對 π 的纖維飽和，才能保證 Port-only controller 知道有甚麼動作可做。詳見 `GL50-03` 與測試中的 deliberately non-saturated admissibility。

## C. Proof Family 和跨域比喻不能混成 theorem edges

採用固定 edge 語義：`SAME_LEMMA_INSTANCE`, `CONDITIONAL_DERIVES`, `SHARED_GUARD`, `NON_ENTAILMENT`, `TRANSLATES`；一份 Witness 多家族只代表多個觀測角度，不是兩個 proof object 等價。對於 Wiki promotion 与外部 truth，雖然兩者可用同一 fiber-factorization 引理描述，但內部 Replay 僅證實內部一致性，不提供外部真理的判定 Oracle。這是來源忠誠和數學縮併可兼容的實例。

## D. 首次建立 participant-only input packs（還未實施盲測）

此次分開產生 C0 neutral、C1 Atlas、C2 Atlas+Kernel 三個 **allowlist ZIP**。每個只裝入事先選擇的可見文件與統一 instruction；**不包含** `06_BENCHMARK_LOCAL_ONLY`、hidden task JSONL、rubric、source TAR、old FULL 或當前 Handoff。私有測試在 `06_BENCHMARK_LOCAL_ONLY/reconstruction_v50/`；這些仍會被 FULL 保存以利版本回放，所以 FULL 仍**不可**直接給 blind participant。測試環境應只載入 condition ZIP，題目由另設管理者逐題提供；紀錄模型版本、工具、token 與是否已接觸其他材料。未取得一個真正獨立模型的運行結果前，不得報成功率。

控制組不同長度：C0 為極簡背景、C1 為成果卡、C2 很大。這是資訊量分層比較，不是 token-equal ablation；C2 若使用檢索/分段必須記下實際讀取的 spans 和成本，否則不應得出因果性能增益的強結論。RAG 對照尚未實作。

## E. Release 和歷史證據處理

不覆寫歷史 v4.9 的 `SKILL_FIELD_NOTES_MATRIX_v4.9.csv`；新增本輪 v5.0 matrix，並驗證舊 11 份文件 bytes/Hash 不變。發行 QA 要同時檢查：現行 12 份 Skill 筆記、原 11 份完好、14 份正式 Knowledge、五份受保護文件、325 Source IDs、60 RA、W024、PF/GM、測試數及 INCREMENTAL overlay 逐位元相等。不要為了「今天沒有增加 W/PF」而虛報研究停滯：這輪正是 Proof Dependency 的質量改善。
