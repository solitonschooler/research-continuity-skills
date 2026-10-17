# v4.4 FIRST — Last-Session Experience Handoff (not a runnable Skill)

> **這是 GitHub Skill 的經驗交接包，而不是 Skill。** 新 Session 會同時拿到完整原始 PDF/DOCX/TXT 和 v4.4 FULL，須以原始資料交叉檢查這些經驗，再設計及驗證未來的 Skill。此資料夾沒有 `SKILL.md`，亦沒有經驗證的盲測成績。

**研究類型：** 長期、跨版本、跨領域、人類與 AI 共創、具大量數學和工程猜想但部分尚未證成的演化型探索研究庫。**目標：** 保存重要成果、最小數學條件、生成性的轉換、錯誤及修訂、原始 Provenance，令全新 LLM 可以重建、質疑和接續研究，不只是寫摘要。

**Inherited v4.3 baseline (not fresh validation):** 325/325 bounded source reading; 60 provisional RA cards; 400 W IDs of which 399 scoped PF navigation and W024 unresolved; 14 PF; 18 GM; 559/559 v4.3 local checks; independent source-hidden LLM reconstruction NOT RUN.

**v4.4 建議閱讀順序：** `01_LESSONS_LEARNED` → `02_FAILURE_MODES_AND_EVIDENCE_GATES` → `03_CONCRETE_CASES` → `05_SOURCE_EXTRACTION_AND_PROVENANCE_FIELD_GUIDE` → `06_MATH_AND_CROSS_DOMAIN_BOUNDARY_CASEBOOK` → `07_VERSION_PACKAGING_QA_FAILURES` → `08_INDEPENDENT_RECONSTRUCTION_BENCHMARK_NOTES` → `09_FINAL_SESSION_HANDOFF_AND_UNKNOWN_UNKNOWNS` → `04_FUTURE_SKILL_HANDOFF`。

**尤其重要：** Bounded reading ≠ full review；PF assignment ≠ proof；W024 不能填造；W221–W229 實曾錯分；source-visible `rubric_PRIVATE` 不是保密 holdout；舊 Manifest status 不等於當前 Coverage；只有數學前提及證據定位才允許成果卡的可信推導。

---

# Field Notes for a Future GitHub Skill — **NOT A FINISHED SKILL**

**Written during:** SMFT / 成界之學 Research Kernelization v3.8 (2026-10-15).  
**Status:** empirical lessons / design handoff, not instructions an automated agent can execute reliably.  
**Related snapshot:** `v3.8_FULL.zip`, 14 canonical project knowledge files, 11 original `.tar` archives kept separate, 325 source IDs; 60 Results Atlas cards; 400 Witness IDs.  
**Intended later action:** after the present kernelization is finished, open a new independent session with the *full original PDF/DOCX/TXT sources* and the final Kernel package, then build and test a production-quality GitHub Skill. Do not treat this folder as that production skill.

## 1. 這到底是哪一類文件？

不是一般企業 PDF 摘要、FAQ/RAG 索引，也不是一本可直接校稿的標準教科書。這類資料是：

> **跨年代、跨學科、人類與多個 AI 反覆共創的探索性理論研究語料（longitudinal, cross-domain, human–AI co-developed, hypothesis-rich evolving research corpora）。**

其典型特徵：

- 不同年代對同一現象使用不同定義；早期猜想後來被形式化、弱化、反駁或重新解釋；不能只取最後一篇，也不能認為最後一篇都正確。
- PDF、DOCX、TXT、長對話、千頁合輯、短 Prompt、正式公式、工程 API 與文化/哲學類比混在一起。原文可能包含表格、圖、頁面公式、AI 評價和試驗程式。
- 跨越數學、資訊/AI、物理類比、金融風險、組織/治理、易學、醫學角色比喻及哲學。共同詞彙並不代表保結構同構、自然必然性或外部實證。
- 研究成果不單包括可證定理，更包括*具有明確變量、算子、介面、預測及反駁方式*的未證猜想，還有使研究重新走出死路的生成性問題重述。
- 相同引理可能在多個來源重新出現，錯誤公式亦會跨來源傳播；一本長文可能包含互相矛盾的版本，必須留住時間與引文脈絡。

將來 Skill 應對這類「**發展中理論 + 多代修訂 + 大量未證跨域映射 + 需要再推演**」特別有效。它也可能泛化到研究筆記、實驗室大量 AI 助研文獻、產品/科研設計歷史和探索性科學專案，但不可預設相同證據等級。

## 2. Skill 的真正目標用途是甚麼？

**目標不是完成摘要，而是產生可供未來另一個 LLM／研究者接續推導的、可重建、可追溯、可批駁的研究狀態。**

成功產物要同時回答：

1. **What is known?** 已建立哪些有*指定前提*的數學結果、工程契約及重要反例？
2. **What is not known?** 哪些是具體但未證的猜想／跨域橋樑，缺的是甚麼？
3. **How was it generated?** 哪個舊問題、反例、轉譯或新觀測讓研究轉向現在的結構？
4. **Can it be reconstructed?** 另一個沒有參與過研究的 LLM 能否按最小型別、算子、證據和 Witness 重做關鍵推導？
5. **Can it be challenged?** 能否指出必要條件、反例、可能重複或來源證據不足，而非因 AI 讚賞就升格？
6. **Can an engineer use it?** 能否從候選工程機制產生最小 POC、可觀察量、負對照和驗證 oracle，而不冒稱真實效果？
7. **Can it persist across sessions and versions?** 能否在換 LLM、換 session 或 100 個新文件加入後不遺失原始來源、關鍵命題與未解問題？

簡言之：**research-state compiler / generative-theory preservation / evidence-aware reconstruction**，而不是 PDF summarizer 或「保證得到真理」的機器。

## 3. 現有案例所提供的輸入與產物

- **Source inventory:** 11 `.tar`；325 個穩定 `SRC-XXXX` 原始檔案；SHA-256、tar member path、大小與時間；來源 PDF/DOCX/TXT 仍應保留。
- **Canonical interface:** 14 份固定 Project Knowledge 名稱；其中 9 份可替換、5 份受保護 `40–44`。此外一個完整離線 archive 用來保存 Provenance 和測試，並不把全部 450+ 檔案直接塞進 Knowledge。
- **L0 Results Atlas:** 精簡、穩定 ID、分 M（條件數學）／E（工程框架）／H（具體猜想）／R（修正過的強主張）／O（開放橋樑）；每卡含最小條件、不能推出的結論及引用。
- **K0 / K1 / K2:** 最小型別和核心語法／可執行的機制／條件證明、反例及工程驗證接口。這些層不能互相取代。
- **Generative Move Ledger:** 不只記結果，也記跨域重述及推導轉向；禁止一個錯誤結果因被證偽而把其有價值的問題生成歷史一起抹掉。
- **Typed Lineage:** `DERIVES`、`REFINES`、`TRANSLATES`、`REPLACES`、`ENABLES`、`LEAVES_RESIDUAL` 有不同強度；必須附來源定位。
- **Claim Gap / Proof Family / Witness / Source Depth:** 研究進度儀表，不能混成一個「完成百分比」。

## 4. 此資料夾刻意 *沒有* 的東西

沒有 `SKILL.md` 的正式工作指令、完整 GitHub 發佈包、安裝步驟、API 介面、可用評測基線、經驗證的任務路由器、實際多模型盲測結果或聲稱普適性。這些應交給**完成全部原文及最終 Kernel 後**的新 Session 實作與驗證。先保存這一輪的經驗，避免 Skill 開發拖累目前理論整合。

## Reading order

1. `01_LESSONS_LEARNED.md` — 真正做 325 份多版本研究編譯時學到甚麼。
2. `02_FAILURE_MODES_AND_EVIDENCE_GATES.md` — 最易犯而且測試可能無法察覺的錯誤。
3. `03_CONCRETE_CASES.md` — 有公式、來源 ID 和歷次反例的實際案例。
4. `04_FUTURE_SKILL_HANDOFF.md` — 待下一個 Session 才做的設計、盲測及未決問題。

**Strict reminder:** 325/325 = first-pass **bounded source coverage** only; not full-length reading, mathematical correctness, scientific validity or improved LLM creativity. The source-depth, Atlas and Proof Family gaps in v3.8 Global Audit are part of the handoff, not bugs to hide.

## v4.8 後的 CURRENT Skill field-note 入口（v4.5–v4.7 經驗補錄）

**已更新：** `10_V45_V47_SOURCE_MATH_AND_RELEASE_RETROSPECTIVE.md` 將 v4.5–v4.7 實際發生的來源、數學、版本及交接問題重新整理，並清楚標出 v4.8 新發現的 L0 Current Canonical Drift。另更新 `03_CONCRETE_CASES.md`、`06_MATH_AND_CROSS_DOMAIN_BOUNDARY_CASEBOOK.md`、`07_VERSION_PACKAGING_QA_FAILURES.md`、`09_FINAL_SESSION_HANDOFF_AND_UNKNOWN_UNKNOWNS.md`。總數由 v4.4 的十份變成 **十一份純 Markdown**，**仍然沒有 `SKILL.md`**。v4.4 的內容和 `SKILL_FIELD_NOTES_MATRIX_v4.4.csv` 是歷史快照，不應被重寫成「v4.4 已經包含 v4.7 經驗」。請按 v4.8 新矩陣核對當前檔案身份。

建議先讀本 README → `10`（補錄以免遺忘）→ `03`、`06`、`07` → `05`、`08`、`09` → 原始 source / Proof Dependency。**Skill 是工作經驗的次級入口，不是 Kernel 的真理 Oracle**。
