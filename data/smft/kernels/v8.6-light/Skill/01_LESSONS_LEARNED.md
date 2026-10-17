# 01 — Kernelization 的實際經驗教訓

## A. 先凍結原始來源身份，再讀內容

1. 不因檔名相似就當是相同來源。使用 `(archive, member_path, SHA-256, bytes, mtime)` 形成不可變 source identity；一個原文有 PDF/TXT 不同版本，須分別記錄，另加「可能派生／重複」邊。
2. Source ID 在整個專案中穩定（如 `SRC-0323`）。CSV 應保存原始欄位，新增對照檢視表，而非為了填滿新版而重寫舊 Provenance。
3. 長 PDF／DOCX 的全文可索引 ≠ 全文已讀。記「實際讀到的章節、頁碼或段落」；遇到關鍵公式、圖、流程狀態，要看原始排版或圖像，不能只信文字抽取結果。
4. 部分文件非常長；對數百頁合輯應有兩層 Coverage：first bounded reading 和 later systematic deep review。不要將 first-pass 325/325 包裝成 full audit。

## B. Kernel 不是一般摘要或壓縮

5. 傳統文章摘要回答「作者說甚麼」；這個項目需要保存「**在甚麼型別/前提/觀測/干預下，哪個轉移或定理才成立**」。只有摘要的模型會忘記最重要的判斷條件。
6. 分離 L0（成果）、K0（最小語法與型別）、K1（運作機制）、K2（證明/反例/測試）以及 GM（創造性轉換）。未證想法可在 H／Residual 保存，不因尚未證明便丟掉，也不能偷升 K0 定理。
7. L0 應按**重要成果**組織而不是按文件出版順序；保留固定 ID；只有真正新增重要成果才新增卡片。60 卡可長期維持，而原文及 Witness 不斷增加。
8. 概念重名不等於等價。要證明 `A ≅ B` 必須給出映射、保持的運算/關係、定義域、逆或充分性、哪些觀測可驗證。
9. 交叉領域常有「翻譯很漂亮，但推導箭頭不成立」。例如哲學/術數/物理的角色對應，可留下工程假說，但不讓統一用語偷渡「物理定理」。

## C. 用「會破壞論證的反例」檢查文本

10. 找反例之前先核對作者原來的量詞（所有系統、某個局部模型、特定干預類別）及數學型別。單純找到極端例子不能直接否定有額外假設的弱版本。
11. 逐步建立 Witness：**source quote locator → formal signature → conditions → calculation/countermodel → exact scope → surviving weak interpretation → residual**。以固定 ID 鎖定，未來新版本補充而不是覆寫。
12. 有時來源的「已證明」只是使用數學術語。例如 Hessian 實對稱卻聲稱純虛特徵值；或用非負 path penalty 推出耗散。建立最小反例很有用，但不要借局部反例宣稱整個研究無價值。
13. 後期文章也會複製早期失誤。找到同一錯誤在兩個 SRC 重複，不算兩項獨立數學發現；應記成 propagated claim/error chain。

## D. 多文件全局一致性不能靠 LLM 記憶

14. 文件只有幾 MB，也不能假設模型已在同一工作上下文看到每項公式。可重建性來自穩定 ID、可檢索 L0、Proof Family Index 和明確的 source retrieval，而不是靠模型保證「我全記得」。
15. 不要因為 400 個 Witness 就認為有 400 條獨立定理。抽取**通用引理**和來源特定的適用條件，保留原 Witness ID 並用 overlap decision 記錄。未人工審核的對照不能自動去重。
16. 人工分類和自動發現有不同意義。PF 索引可能完整列出 W001–W400，但仍有未分類、缺標題定位的早期條目；索引「有一行」不是證明重建完成。
17. 要區分源檔存在、原文範圍審核、資料欄位可驗證、數學引理可重演、真實世界假說有外部證據、全新 LLM 可正確復原六個不同階段。
18. 增量封裝須保持 canonical nested 文件與 flat upload 副本逐位元一致，並以 hash 驗證不可更動的部分。回歸測試不能硬編碼「永遠嵌入 v3.3 Atlas」；應測歷史保留與現行版本正確指向。

## E. 保存創造力而不附和

19. 對作者思路做**生成性保存**：早期大膽假說即使被反例限制，仍要保留「哪些觀察啟動新問題」；區分歷史貢獻與現代推導證據。
20. 對 AI 給的正面評價，記為觀點/外部意見，而非獨立科學驗證。代數、控制/可辨識性、真實 A/B、學術領域的証據級別不同。
21. 對「自然形成」「必要」「唯一」「普遍」「等價」「最優」「保守」這些強字眼主動加 Proof Obligation；它們常是連接猜想與定理的破口。
22. 專案真正想保存的是「*能產生下一個可測問題*」的最小生成結構，不只是事後看似漂亮的總結。

## F. 觀察到的專案方法限制

- 多輪人工產生的 Manifest 有歷史狀態欄：即使 Coverage 後來達到 325/325，也可能保留 `not_reviewed_in_kernelization_batch` 等舊值；必須以**時間/版本**辨別，不應隨意視為資料自相矛盾或任意覆寫。
- Test count 高，只能證明 local math/software invariants；不能評價語義理論、金融投資、物理本體、臨床或 AGI 智能提升。
- 目前 source-hidden clean-room independent LLM reconstruction 仍未正式執行，這正是未來 Skill 要先設計的 benchmark，而不是後補漂亮的宣傳材料。


## v4.0 lesson — proof-family assignment is a typed judgment, not clustering

An apparently easy mass reclassification of 400 Witnesses must still read each original compiled proposition and preserve its assumptions. The concrete W027/W028 pairing objectives illustrate why similar inputs are not duplicate proofs. W031/W033 illustrate why affine no-go and nonlinear constructive proofs coexist. Save dependency nodes, guardrails and original ID with every assignment; do not claim mathematical proof from a family label. Source-bound math audit is not rereading full original documents or independent reconstruction. See `90_PROVENANCE/PROOF_DEPENDENCY_AUDIT_v4.0.csv`.


## v4.1 lesson — shared family, distinct quantifiers and observers

Proof-family routing must not let keyword similarity erase mathematical distinctions: W099 unrestricted graph Laplacian ground and constrained antiphase sector are different claims; W102 deterministic replay and W103 third-party authentication have different trust assumptions; W085 Schmidt-rank analysis and W086 postselected weak-value algebra are not empirical gravity. For each historical W, save exact source *compiled* paragraph, typed constraints, negative entailment and provenance. Family assignment itself is not a new theorem.


### v4.2 field lesson — classify proof by type, not metaphor or topic name

A 60-Witness batch showed how repeated phrases (phase, Fold, attractor, Gate, transfer, truth) can denote different mathematical operations: W131 finite-frequency Hopf is not W214 Hessian spectrum; W151 broadcast fan-out differs from W162 duplicated delivery; W169 typed-distance residual differs from W316 endogenous zero-residual. Retain both original locators and explicit negative entailments; never auto-merge based on a shared Proof Family. No new executable Skill; keep this as future-skill evidence.


### v4.3 field lesson — taxonomy completion is not evidence closure

After classifying 74 additional old compiled propositions, 399 of 400 IDs have scoped PF tags, but W024 has no authenticated statement. Resist the tempting but invalid report "400 mathematical proofs verified". We only audited their compiled formulations, not every original source or independent external validity. Keep a reserved-ID hole visibly unresolved; state explicit negative entailments and cross-family comparisons; do not turn ontology tags into theorems or delete historical source trajectories.


## v4.4 closing lesson — handoff reliability is research correctness

Historic statistics in this document reflect different versions, not current status. At inherited v4.3: 399/400 W scoped PF family routing; W024 remains without an authenticated original proposition. A few MB of text does not guarantee the LLM attended to all mathematical assumptions. Preserve separate dashboards for source/depth, theorem validity, typed dependency, L0 maturity and independent reconstruction. The v4.3 W221–W229 wrong-family episode is evidence that automated semantic grouping can corrupt the graph; use exact compiled statement and negative-entailment checks.

**Important blind-test leak:** Some historical FULL packages contain preparatory holdout tasks or private rubric inside `06_BENCHMARK_LOCAL_ONLY`. Passing a fresh model the whole FULL invalidates any claim the model lacked access to grader guidance. See `08_INDEPENDENT_RECONSTRUCTION_BENCHMARK_NOTES.md`.
