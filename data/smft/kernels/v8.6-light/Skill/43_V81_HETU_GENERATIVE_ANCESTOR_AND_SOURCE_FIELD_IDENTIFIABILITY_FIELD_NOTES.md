# Field Note 43 — v8.1: Missing generative ancestor and source-field identifiability

**Case:** V81-HETU-ANCESTOR-01; GL81-01..04; RA-H04; supplemental 15-page user-uploaded source SHA `51c5ebb98fff2fc36e46c2a9948dd64a955a4fa4c56c10fe65aaabe0d4a4358f` (not silently added to 325 historic IDs).

**Trigger:** user identified a model-misspecification risk: v7.8–v8.0 directly tested LuoShu from general local energies, omitting the hypothesized training-built Hetu source field. They provided additional primary text that has a richer notion of Hetu than a static list of five pairs.

**Actual review:** read pp1–5, 8–10, 13–14 of the source, visually inspect pp3,5,9. Extract source's field-body/bifrequency/trace/center/phase-lock structure and its explicit admission of the unsolved quantization problem. Compare to previously executed direct grid energies. Identify the appendix's peripheral 8-cycle and distinct central 5. DO NOT conflate these with a nine-state cycle. Construct the conditional wreath-product stabilizer proof; run a source-conditioned, *synthetic*, standard correlation/matching learner under matched nulls; impose independent Laplacian diffusion only as a controlled illustrative extension.

**Observed:** learned association retrieves supplied latent pair partitions reliably when shared factor signal and sample size are sufficient; fails at low signal/low N, and rho=0 null. Learned-pair graph diffusion suppresses paired perturbations, ordinary baseline does likewise when supplied correct graph. The source structure itself was planted, so no observation of genuine Hetu emergence. No downstream LuoShu from learned memory was measured. Precisely **19/19 new scoped tests passed**, NOT the historical all-suite.

**Failed reduction / source repair:** Hetu ≠ five memorized pairs; its hypothesis includes source field, temporal accumulated trace, orientation, center, pre-collapse frequencies and constraint on projections. Testing `generic nearest-neighbor grid energy→LuoShu` does not test `training→Hetu→LuoShu`. But adding an unobservable ancestor AFTER every null result is equally unacceptable: freeze independent source-field observables *before* testing subsequent trace outcomes.

**Formal residual:** five unordered pairs of 10 abstract channels admit 3840 relabeling automorphisms; pair recovery alone cannot yield a distinguished LuoShu board/trace without further labeled/oriented/numeric information. Literal `1→6→7→2→9→4→3→8→1` is 8-cycle with separate fixed 5, not 9-cycle. These are bounded theorems, not universal SMFT refutations.

**Practical QA failure caught:** early test import accidentally executed and overwrote simulated data because run script had top-level side effects. Fixed by moving experiment to guarded `run_experiment()` before final QA. This is a general reproducibility skill: tests must not overwrite artifacts they claim merely to verify.

**Reusable Future Skill rule:** `GenerativeAncestorAudit`: list candidate ancestry chain, independently observable state for each arrow, temporal order, which training inputs encode it, baseline learning method, ablation and nulls; `SourceVsCompiler` ledger; `TemporalObjectType` gate (8-cycle-plus-center is not 9-cycle); `TestIsolation` import side-effect guard; `PairOnlyIdentifiability` symmetry check. Keep competing outputs and failures; no forced success.

**Evidence grade:** bounded source interpretation + conditional mathematical theorem + actual synthetic code and 320 runs/40 diffusion metrics. No real Transformer, independent LLM Reconstruction, external ecological physics or Feng Shui claims validated. No new formal runnable GitHub SKILL.md created.
