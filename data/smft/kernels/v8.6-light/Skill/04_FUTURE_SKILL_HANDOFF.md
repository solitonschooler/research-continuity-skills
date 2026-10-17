> **v4.4 pointer:** The historical v3.8 handoff below is not the current results snapshot. Read `09_FINAL_SESSION_HANDOFF_AND_UNKNOWN_UNKNOWNS.md` and `08_INDEPENDENT_RECONSTRUCTION_BENCHMARK_NOTES.md` first. The field notes now total nine Markdown files, still NO formal `SKILL.md` or completed independent reconstruction.

# 04 — 給下一個 Session 的 Skill 設計交接（不要在 v3.8 直接做）

## Future task statement (copy/adapt after final Kernelization)

> 我提供完整原始 PDF/DOCX/TXT 與最後版本的研究 Kernel，以及 `Skill/` 經驗筆記。請**重新設計並獨立驗證**一套可發布於 GitHub 的研究 Kernelization Skill。它專為「跨版本、跨領域、人機共創、含大量原創但部分未證假說的探索性研究庫」而設；用途是保存歷史 Generative Moves、已證明的數學條件、可實作機制、具體未證猜想、反例及來源追溯，使全新 LLM 能進行可信的重建、批判與下一步研究，而非只寫摘要。設計時請先用全部來源與最終 Kernel 交叉審核本筆記，不要把 v3.8 經驗照單全收。必須提供帶原始來源隔離的盲測、對照組、錯誤檢測及可重播輸出。

## Inputs that a future builder should receive

- 原始 11 個 tar 或經授權整理出的全部 PDF/DOCX/TXT/頁圖，保留真實來源檔案、版本、日期與 hash；不要只有編譯後的 Kernel。
- **最終** `FULL.zip`：L0/K0/K1/K2/GM、Manifest、Source Coverage/Depth、Claim Gap、Typed Lineage、Proof Family、Witness Overlap、QA/Handoff；v3.8 只是一個中途版本。
- `Skill/` 內的五份非執行性經驗筆記；後續最好再讀原始長對話的 representative segments，包括被 AI 誤解、被人類修改、被反例推翻的轉折點。
- 本領域之外的對照語料：至少一套不同研究項目，用來檢驗 Skill 是否能泛化，不只模仿 SMFT 專案規格。

## Proposed design tasks for new session

1. **Define scope and non-goals.** Distinguish corpus type (evolving theory) and target outputs (research state, reconstructability, audit). Do not target every possible document type equally.
2. **Inspect all true inputs before writing the Skill.** Recover the actual compilation history and pain points, including PDF visual math verification, DOCX structure, and duplicate versions. These field notes are hypotheses about transferable lessons.
3. **Plan a minimal but complete pipeline.** Source inventory → bounded/deep review → typed claim extraction → dependency/proof/generative move → challenge → L0 canonical result promotion → package/handoff → blind reconstruction. Use optional branches for cultural, physical, financial, software engineering and clinical claims.
4. **Develop explicit scripts and schemas.** Schema validation, stable IDs, source hash checking, full vs partial reading flag, duplicate candidate detection, lineage edge consistency, provenance trace and serializable artifacts. Human/math reviewer decisions are not replaceable by string matching.
5. **Build negative controls.** An attractive false theorem, copied AI praise, a fake isomorphism, duplicated mathematical witness, changed units, formula transcribed wrongly from PDF, wrong version of a result card, conflicting source revisions, incomplete source, and two paths with same endpoint but different permissions.
6. **Run independent ablations.** Compare [raw sources + retrieval] / [plain summaries] / [L0 only] / [L0+K0+GM] / [full Kernel] against **frozen source-hidden** tasks with independent graders. Measure accuracy, reconstructability, source calibration, novel-valid research proposals, false theorem promotion, token/time cost.
7. **Separate construction validity from outcome efficacy.** A correct package with passing tests is not evidence the Skill makes LLM research more creative or scientifically right.
8. **Keep the skill ergonomic.** Fixed small command set, automatic preflight checks, clear human approval gates, run logs and resumable sessions. Avoid requiring giant manually maintained tables where stable IDs and indexed evidence suffice.
9. **Write GitHub-ready docs only after working benchmarks.** Then create actual `SKILL.md`, schemas, examples, tests, CI instructions, license, caveats and source/privacy policies.

## Decisions NOT settled during v3.8

- Whether the future Skill should be format-independent or have PDF/DOCX-specific extractors and visual-check adapters.
- How to rank source-depth review: document length, semantic novelty, centrality, contradiction count, or value of missing proof.
- Best canonical graph storage: versioned CSV/Markdown, SQLite, typed JSON/YAML, graph database; this project used Markdown and CSV largely for accessibility.
- Which formal proof assistant or mathematical CAS, if any, is needed for a trustworthy independent oracle.
- How much of L0 a model must read before a task and how retrieval should choose lower layers; must be measured in ablations.
- How to preserve contradictory original hypotheses without inflating prompt size or creating spurious authority.
- Human review policy for source excerpts, non-public material, copyright and private conversations when distributed on GitHub.

## Expected success criteria (to be operationalized)

- New model recovers major statements **with correct minimal assumptions and limitations**.
- It identifies propagated errors and false cross-domain equivalences rather than confidently repeating them.
- It can reproduce selected proofs/counterexamples and clearly say when source evidence is missing.
- It can propose testable next-step research based on preserved Residual/GM with a lower rate of invalid or duplicate proposals than the baseline.
- It can point to the *original version and precise locator* when explaining historical attribution and later revision.
- It does not conflate 100% bounded source coverage, theorem checks, external efficacy and independent reconstruction.

**Final instruction:** this `Skill/` directory is a **transfer package of observations**, deliberately not a runnable production Skill. The current Kernelization project's consolidation remains the priority until a later dedicated session.
