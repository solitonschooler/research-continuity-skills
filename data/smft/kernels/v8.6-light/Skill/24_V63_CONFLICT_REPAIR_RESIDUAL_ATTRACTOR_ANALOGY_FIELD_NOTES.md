# v6.3 Field Notes — From Research Compilation to Auditable Discovery Assistance

**Status: non-executable experience log, NOT a completed GitHub Skill.** This note deliberately preserves (i) an actual source-tested contradiction repair, (ii) prospective design requirements motivated by the user, and (iii) still-unverified Attractor/analogy capability-gain hypotheses. Do not rewrite prior field notes in place.

## 1. Observed casebook: within-document and cross-document contradiction repair

- `SRC-0270` v6.2 treated joint/commuting measurement as agreement. `SRC-0245` p.12 supplies an elaborated record-based theorem, but its proof still moves from the historical outcome A to a **new** outcome B. Construct the smallest quantum CP negative control: `M_i(ρ)=Tr(P_iρ)|+><+|`, same PVM for A and B, A=0 recorded and accessible, B=0 next with probability 1/2. This falsifies overstrong delta-certainty while preserving the value of shared historical records (`GL63-01`).
- `SRC-0245` p.18 writes conditional expectation `E_k(E)=E` and then arbitrary past-event probability `ρ_k(E)=1`. Use a Bernoulli event to check the hidden quantifier; measurability does not imply the event occurred (`GL63-02`).
- `SRC-0245` p.20's concrete noncommuting **sharp** example lacks a joint POVM, but its general claim wrongly generalises from PVM to all POVM. Explicit Pauli-unsharp `G_ab` demonstrates noncommuting **jointly measurable** effects (`GL63-03`). Always seek generality counterexample distinct from refuting source's *specific* example.
- `SRC-0245` p.13 SBS consensus proof elides whether the extra fragments are observed by the same decoder. Fixed local noisy observations keep the pairwise error constant even as global fragment count grows. Require a `K`-conditioned decoder and independent sample-count premise to invoke concentration (`GL63-04`).

**Reusable compiler schema**: `source_id / exact page / proposition / type / quantified premises / minimal failing model / surviving conditional theorem / consequences / independent test / confidence / version revision link`. Preserve source original text and exact offending implication separately; never erase an author's correct narrower result.

## 2. Residual discovery must be constructive, not merely negative

For each verified conflict: (a) extract which *one* premise was missing; (b) preserve what remains correct; (c) write a necessary/sufficient candidate, separating them; (d) propose a concrete experiment or independent proof; (e) register alternate interpretations/negative controls; (f) identify old downstream claims that must be downgraded. An unmeasured idea is `PROPOSED_RESIDUAL`, not an observed mechanism. This procedure operated in v6.3 `GL63-01..04`, but its transfer to unrelated corpora is not yet externally tested.

## 3. Adding mathematical Attractor Kernel — a separate optional lens

Do NOT bake the SMFT/Attractor mathematics into the neutral evidence scanner. Pass only a **typed optional hypothesis-generator module** when an independent operator enables it. Proposed prompts to operationalize: identify state space, observation protocol, semigroup/Markov closure, attractor basin under an explicit metric, perturbations, transition/bifurcation, time scale, and negative models where stability does NOT convey function. Explicitly retain external alternatives (standard dynamical systems, information theory, causal inference, no attractor). False analogy/no-go outcomes must be emitted alongside positive suggestions.

No current independent data show Attractor mathematics increases valid mathematical discoveries, contradiction recall/precision, true theorem repairs, or creativity. Treat anticipated gain as `HYPOTHESIS_WITH_TEST`, not a marketing fact.

## 4. Human analogy as a controlled creative input

Record user analogy verbatim and map source→target typed structures. Require explicit `mapped variables / invariant / proposed morphism / where the map fails / formal lemma-or-test / baseline alternative / prior-art search requirement`. Example: soap-bubbles→representational clustering is only a suggestion until measured trajectories, distance, aggregation operator and falsifying intervention are fixed. Without this, analogies can increase compelling but untestable stories.

## 5. Fair independent skill evaluation protocol (proposed, NOT_RUN)

- Use **unseen non-SMFT research corpora**, mixed disciplines, contaminated vs source-hidden question sets, and blind human/external expert grading. No judge access to reference answer while generating; no private rubric in participant FULL.
- Comparator 1: an existing open peer-review/literature-agent pipeline; comparator 2: generic full/RAG retrieval under matched token, wall-clock and model conditions; comparator 3: Research Kernelization compiler alone.
- Factorial study *inside matched compiler*: `Attractor off/on × Analogy off/on`. Randomly assign analogy prompts, balance positive and deliberately misleading analogies, and pre-register scoring. Inspect main effects and interactions; do not conclude an effect by comparing two confounded packages.
- Grade contradiction precision/recall, valid mathematical repairs, unresolved residual **testability**, originality checked against external prior art, successful downstream validation, and rate of false enticing conjectures; report cost and failure cases.
- Required release status until an actual isolated model, private grading, and clean-rubric study occurs: independent source-hidden LLM **NOT_RUN**, observed Attractor increment **UNKNOWN**, creativity increment **UNKNOWN**.

## 6. Packaging and historical evidence gates

Current `CURRENT_V63` should keep all 106 earlier GL/L nodes and 99 edges untouched, append 5 scoped new nodes and 12 typed edges, and preserve previous Current snapshots; Source Manifest stays at 325 unchanged. Do not mistake local math unittest count, theorem proof in toy spaces, or SHA-matched source extraction for an independent skill evaluation. Skill folder remains field notes; no runnable instructions or API skill manifest created in this round.
