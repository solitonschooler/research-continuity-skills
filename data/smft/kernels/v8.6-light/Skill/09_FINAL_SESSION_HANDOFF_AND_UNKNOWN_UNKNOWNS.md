# 09 — 最後一輪經驗交接：新 Session 先驗證，再製作 GitHub Skill

> **不是正式 `SKILL.md`，也不是完整的 Skill。** 這是留給新 Session 的考證線索與待辦。必須以原始 PDF/DOCX/TXT 及 v4.4 FULL 的真實內容交叉驗證，不可將本 Session 的判斷當不可質疑的權威。

## A. 這類研究語料的型別

**Longitudinal, Cross-Domain, Human–AI Co-developed, Hypothesis-Rich Evolving Research Corpus.** 約 325 份來源橫跨多個時期及版本，混合數學、物理類比、Finance、Organization、AI Agent、SIDA、易學、哲學與對話。研究命題經常從初步類比 → 可操作假說 → 限定條件的數學推導 → 反例／修訂 → 新研究分支；同一個主張可以在不同文章重複出現、甚至重複錯誤。這不是一套已定稿、全部成立的理論論文。

## B. 為甚麼要 Kernelization？

目標是 **Research-State Preservation + Mathematical Reconstructability + Generative-Theory Continuation**，不是摘錄漂亮語句或單純減少 Token。新 LLM 應能回答哪些結果已證、哪些工程機制可測、哪些具體猜想尚未證成、哪項強主張被反例限制、哪些生成性的問題值得再推演；並知道來源 ID／版次／頁碼／推導／反例／權限／量詞等。跨 Session 和跨模型可重建與可挑戰，比讀起來流暢更重要。

## C. 本項目 v4.3 繼承基線（並非完整有效性判決）

- 11 個來源 TAR、325 `SRC`，已完成 **325/325 first-pass bounded source coverage**，不能宣稱全文件逐頁深讀。
- 60 張 provisional Results Atlas，分數學 M／工程 E／猜想 H／修訂 R／開放 O。
- 400 個歷史 Witness 編號；399 個已作 scoped Proof Family **導航分類**，W024 為保留而未找到原命題的編號。這不等於 399 個數學定理已重新獨立驗證，也不等於完整 implication DAG。
- 14 Proof Families、18 Formal Generative Moves；K0/K1/K2/Lineage/Claim Audit/Depth Audit；14 份 Project Knowledge 槽位（本項目特有限制），其中 5 份 `40–44` 保持固定。
- v4.3 559/559 local regression checks；並**沒有** source-hidden independent LLM reconstruction，也沒有以此證明科學／金融／AI 實效。

## D. 下一個 Session 應先做的事情

1. 用原始來源實際 byte/hash/member path 重建身份索引，檢查 14 份現行 Project canonical 文件、所有版本編譯索引和 Source Depth，找出證據缺口。
2. 從 `Skill/README_FIELD_NOTES.md` 開始閱讀全部 01–09 篇 field notes，然後用原始文獻／當時原數學式／編譯報告**反過來挑戰筆記**。這些筆記是研究者觀察，不是完整法典。
3. 針對重要 RA 卡優先驗證 source → claim → witness → proof conditions → RA 的實際完整鏈；保留證據等級，避免錯用 `W5`/`W005` 或漏掉舊版本段落。
4. 用 06 案例庫抽查最容易錯配的數學結構，特別是 v4.3 曾出錯的 W221–W229、Dual Ledger、Gauge/Spinor、SIDA phase、Wick/Complex Finance、RH、Operational Quotient／Endpoint Saturation。
5. 對不同領域各選一組真原文與反例，再選一個**非 SMFT**、同樣長期迭代的研究庫作泛化測試。避免把當下 14 文件／60 RA／PF14 規格硬編碼成所有研究的共同真理。
6. **在設計 GitHub Skill 前先封存獨立盲測**：受試模型不能讀到隱藏題目、答案、私人 rubric。歷史 FULL 中有 `rubric_PRIVATE` 等本地測試草稿，folder 名稱並不會自動保密。
7. 將 raw sources、普通摘要/RAG、L0 only、L0+K0+GM 和完整 Kernel 作公平對照；評估錯誤／重建／校準／新可測研究／成本。通過外部評估後才做完整的 `SKILL.md`、scripts、CI、GitHub 發佈。

## E. 不可以由目前文檔保證的事項

- L0 的全部 60 張卡均經原始文獻全面重驗。
- 399 個 Witness 已有真正經形式證明的 typed entailment graph。
- 原始人機對話的每個生成步驟都在文章裡完整保留。
- 變分／Gauge／Spinor／複數金融／意識的跨域類比有已證的物理或社會因果實證。
- 同一個模型既寫 Kernel 又判自己的正確性便構成 independent grading。
- 在 Github 公開所有原始 PDF／私密對話或測試 rubric 合乎版權、私隱或盲測原則。

## F. 新 Session 可使用的起始工作要求

> 我提供完整原始 PDF/DOCX/TXT 及最新 Kernel FULL package，內有非執行的 `Skill/` 經驗筆記。請先獨立審核資料類型、研究重建的真正目標、數學證據鏈、原始來源閱讀深度、版本治理和已知錯配，檢查哪些方法可泛化到別的長期研究庫。不要立即寫 SKILL.md。先設計有原始證據定位、負對照、holdout 隔離和獨立評審的評測，再實作 GitHub-ready Skill。不能把本地測試、漂亮類比或 AI 正面評價當成科學驗證。

## G. 仍待決定的工程問題

儲存用 SQLite/CSV/typed JSONL/graph？如何實現 PDF/DOCX/TXT 視覺、表格及對話追溯？Proof checker/數學 oracle 用甚麼工具？哪些來源應先全面深讀？如何低成本檢索而不遺忘難題前提？不同任務所需的 L0 token 預算？如何公開資料並保護私隱、版權與 private evaluation？這些應由真 benchmark 決定。

## H. 交接責任邊界

v4.4 **只補齊經驗筆記與版本交接**，沒有新增來源審核、完整 Proof DAG、W024 命題、獨立盲測、GitHub 技術成品。新 Session 對每條經驗均應嘗試尋找原始證據和反例，不要把本 Session 的筆記視為最後裁決。

## v4.8 actual continuation checkpoint（取代「v4.4 是最後版本」的舊閱讀預期）

從 v4.7 FULL 接續，**先填 v4.5–v4.7 漏寫的 Skill 經驗**，由 `10_V45_V47_SOURCE_MATH_AND_RELEASE_RETROSPECTIVE.md` 鏈回 L45/L46/L47 的原始審核。之後才增修 v4.8 K0/Genesis-P8D 原文 cross-validation 和 new L48 nodes。當前 Skill folder 純粹 field notes，不可開發正式 GitHub Skill，仍需等完整 Kernel 的理論、QA 和 source-hidden benchmark 完成。

**額外未知：** 指標正規化／baseline-choice 可讓低秩 closure fit 看似比實際好；v4.8 已有數學反例，尚未有跨場景量測。K0 正確不保證 L0 正確；未來每個版本均須保留 *current semantic consistency gate*。完成 593/593 只表示 v4.7 local test suite，不代表 independent LLM reconstruction。
