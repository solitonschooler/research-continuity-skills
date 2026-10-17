# Field note 14 — v5.3 真實經驗：Blind Reconstruction、RAG Stage 和污染防線

**類型：** 研究工程的現場經驗記錄，不是正式 GitHub Skill，也不是可以自動驗證 LLM 數學正確性的工具。

## 本輪確實發生甚麼

1. **先核對 benchmark 的來源版本。** v5.0 時產生的 C1/C2 測試輸入在 v5.2 仍被引用。新輸入必須標明資料快照並重新產生 Hash；否則實驗正在測試一個不確定版本，而非聲稱的 Kernel。
2. **語義洩漏不等於文件洩漏。** 即使 private rubric、題目檔不在受試 ZIP，既有 Kernel 可以直接包含該題的答案。這合法地檢驗忠實重建能力，卻不應宣稱測試 *unseen discovery*。
3. **只有可真的執行的部分，才列作已執行。** 本輪重開三份原始 TAR PDF，hash 全部匹配，抽取 186 個頁面，使用 BM25 實跑 4 題，參考背景頁命中 3/4；這完全不是 3/4 答題正確，更不是模型表現。`R0_SOURCE_BM25` 是 retrieval-stage diagnostic，不能叫完整 RAG baseline。
4. **不等輸入長度不可直接比較。** C0/C1/C2 空白分詞估算分別 78 / 5,852 / 90,406，且英文空白分詞非中文 token 成本。長 Context 即使資訊更多，也可能使有限模型表現變差。
5. **實際缺乏獨立模型入口，就如實保持 0。** 32 個 task×condition×repeat 是 **計劃**，並非 32 次獨立受試；每個 trial 都必須有原始回答、模型識別、隔離宣告與盲評記錄，才能計算分數。
6. **回歸測試應包含攻擊性陰性樣本。** 故意把 `rubric_PRIVATE.md` 或 `frozen_tasks` 混進模擬 participant ZIP，驗證檢查器必定拒絕。正常包檢查全綠只說明認得的泄漏種類被排除，不能保證沒有語義、預訓練或先前對話污染。

## 通用審核形式

`Corpus snapshot -> Versioned exposure -> Task isolation -> Model execution receipt -> Raw answer -> Blind grade -> Statistical contrast`。

目前真正走通至 `Versioned exposure`，另單獨完成了 `Corpus retrieval stage`。**絕不可由前兩段推出最後一段已成功。** 後期其他語料亦可沿用這種分階段證據守則。

## 上游 LLM 數學研究如何保留

- 保留 `SRC-0268`、`SRC-0269`、`SRC-0247` 的真實來源身份和哈希，區分 PDF「文字已抽取」與「已經審讀和驗證」；本輪沒有 186 頁的深度研究認證。
- 保留原來 SSLE F1–F4 題目作為 **historical known-target fidelity benchmark**，另開 fresh hidden tasks 測新穎推演，不刪除或秘密修改原題。
- Task-conditioned retrieval 可能命中與數學答案不同的背景頁；原文出處、數學可推出性和成功實驗是三個不同的評估物件。

**檔案：** `90_PROVENANCE/BENCHMARK_METHODOLOGY_v5.3.md`；`BENCHMARK_RETRIEVAL_DIAGNOSTIC_v5.3.json`；`06_BENCHMARK_LOCAL_ONLY/benchmark_v53/{benchmark_build.py,trial_protocol.py}`。

## 真正踩過的 QA 假陽性

v5.3 初次回歸有一個 Stage Gate 錯報：C2 正文裡提及 `rubric_PRIVATE.md`（只是「不可洩漏」的警告），掃描器卻視為真正泄漏。改用 ZIP member name、實際 private rubric 的長字串內容及模擬洩漏對照後，可以正確區分兩者。這是直接的工程事故，未來通用 Skill 必須把**文字描述某個證據物件**與**該物件實際存在／被暴露**分開；保留原測試失敗記錄，不要假裝從未發生。
