# 05 — 來源抽取、閱讀深度及 Provenance：實際現場經驗

> **Field evidence, not an executable procedure.** 本文件是由 v1–v4.3 實際整理原文與索引時發現的檢查要點。未來 GitHub Skill 應先以真實 PDF/DOCX/TXT 驗證，再設計解析器；不能直接視此清單為已測試完成的 Skill。

## 1. 語料的正確分析單位

- **Physical source**：11 個原始 TAR 中精確的 member bytes；本項目 325 個來源識別。`.tar` 只是一種交付容器，不等於論文或理論版本。
- **Document version**：同一研究的舊版、修正版、長篇合集、同名 TXT/PDF、改寫評論可能互相重疊；一個版本的式子不應自動代表其他版本。
- **Claim**：局部可指認的命題，具有量詞、前提、結論、相應觀察方式；不等於整篇文章。
- **Mathematical result / witness**：公式證明、反例或有限檢查及其適用範圍；不等於物理、醫學或 AGI 事實。
- **Generative move**：讓作者由舊困局轉換至新問題的創造性步驟，即使原始推論未成立，仍可能有重要保存價值。
- **Research result**：經全局審核後有資格進入精簡 L0 Atlas 的重要結果／工程架構／可檢驗猜想／修訂／開放橋樑；不按文章數目機械生成。

## 2. 不可變來源身分，和可變審核狀態必須拆開

本專案以 `(source_id, tar_archive, member_path, SHA-256, byte_count, original mtime)` 識別來源。實際可取用 TAR 成員的 bytes，重新計算 SHA-256，再與 `90_SOURCE_MANIFEST.csv` 比對。**雜湊驗證只證明你讀的是指定 bytes**，不證明公式正確。

- `SRC-XXXX` 永久不隨文件改名、移動、合輯重新排序而改寫。SHA 相同才是相同 bytes；相同 filename 不足以判定重複。
- 比對 **manifest snapshot timestamp** 與 **coverage update timestamp**。v3.8 發現舊 Manifest 151 個 `reading_status` 保留歷史「當時未審核」，即使 v3.7 Coverage 已有 325/325 定點閱讀；不能任意改寫歷史欄位以製造一致。
- 版本差異宜以新增 `SUPERSEDES`、`REFINES`、`PROPAGATED_ERROR` 等有型別的關聯追蹤，**不要**默默覆蓋原版敘述。
- 不要因文件引號、數學空格、Unicode 渲染差異或 W ID 左側補零，就誤判來源身分不符或丟失定理。

## 3. 從 PDF／DOCX／TXT 所學到的閱讀風險

### PDF

- 文字抽取適合發現關鍵詞與可重建候選，但 **不構成對公式、圖及版面資訊的核對**。該專案多次核對關鍵 PDF 實際頁圖，發現型別與公式差異。
- 保存 **physical page index（0-based）、印刷頁號、章節標題、原文附近定位短語、原始 URL／tar member**。不同頁碼系統要清楚區分。
- 公式中的 `∂`、`∇`、`†`、上下標、`−`、`i`、群商空間與小數點非常易在抽取中出錯；應有 page-render 對照。
- 有圖形/表格/嵌入 LaTeX 截圖時，純文字完全不夠；OCR 如無法可靠確認公式，不應偷偷當作確定值。
- 數百頁合集可先定點選讀關鍵段落，但是要顯示**未讀頁範圍**，不能用「pdf 已成功被系統搜尋」代替已檢驗整篇。

### DOCX

- `python-docx` 的 `paragraphs` 可能略去表格、文字方塊、圖片、註腳、修訂追蹤和內嵌物件；需要按格式檢查 `tables`／關係部件。
- `SRC-0321`《意識原本》為 1455 段落長文；指定段落可追溯，不等於已檢查整本書每個證明。原文內某處稱 AI 尚未實現，另一處說「必要充分」，必須保留版本內部的張力。
- 對 DOCX，除了段落索引，也要保存章節標題和附近文本 hash／snippet，避免人為加段落使 offset 漂移。

### TXT／Markdown／長對話

- 需要處理編碼（UTF-8、BOM 等）、長行、前後引用、AI 與人類不同 speaker、原文和後來評論分層。
- 某個 GPT 的評語是**一次 AI 生成的研究意見**，不是外部獨立證明。研究者糾正 AI 錯誤的「轉折點」有時比最後答案更有編譯價值。
- 文章總結不一定能保留形成概念所需的所有 Generative Moves；完整原始人機對話若未提供，應明確記錄遺失的生成過程，不補造歷史對話。

## 4. 來源深度應是明確多維狀態，而不是單一完成率

v3.7 建立了 Source Depth Gap Audit：325/325 只代表每份有至少一個指定範圍的選讀紀錄。當時 303 筆主要是定點／未確證深度、18 筆帶需重新審核的全文標記、4 筆標記含糊（**歷史快照，非對所有 325 份原文的新判決**）。

未來可分開記錄：`bytes verified`、`locator read`、`pages reviewed`、`tables/figures checked`、`document-wide review`、`claim formalized`、`independent oracle executed`、`external replication`。每個狀態應有證據及時間戳，而不是一欄 true/false。

## 5. Source → Claim → Result 的回溯條件

每一張重大成果卡最終應能形成可重播的證據鏈：

`RA-ID → precise claim_id → W/Proof obligation → SRC-ID + edition → archive/member SHA → page/paragraph → literal equation/check → reviewer note`。

反方向也需要：新增來源可能 `REFINES` 一張現有 RA 卡、補充反例、傳播同一錯誤、或只留下 Residual；**不能自動新增 RA 結果**。若遇到所引用頁面不存在、引文來源版本不符、或公式與頁圖不同，應明示 BLOCKED 而不是從類似文章「補完」。

## 6. 常見錯誤及對應檢驗

| 假象 | 實際問題 | 現場教訓 |
|---|---|---|
| 同名兩文件 | 不同 SHA/版本 | 源 ID 與版次都要保留 |
| 325/325 coverage | 可能只是每件讀一段 | 用 Source Depth 報告，不宣稱 complete reading |
| CSV status 矛盾 | 舊 snapshot 和新 update 並存 | 日期對照，保護凍結 Manifest |
| 檢索找到 W001–W012 沒標題 | 舊版本用 W1–W12 且放在 Genesis/bench report | 搜尋所有歷史伴隨文件；ID canonicalization |
| W024 找不到 | 無可核證原命題 | 保留 `UNRESOLVED_RESERVED_ID`，不可臆造 |
| PDF 公式文字完整 | 可能少負號、星號或上標 | 必要時人工核對原頁 |
| 完整原文可讀 | 還未證明數學正確 | Claim/Witness/Oracle 分開 |

## 7. 實際封裝限制

本項目 14 個正式 Project Knowledge 槽位與完整離線 archive 不是同一層。Source TAR 和大型 QA／測試集合保持分離，可降低 Boot 噪音；`Project_Upload_Flat/` 只是 canonical 14 文件的位元組相同副本。未來 Skill 必須依目標環境重新評估限制，**不要硬編碼成「所有使用者都只能 14 份、固定要有 11 個 tar」**。
