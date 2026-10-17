# Field Notes 33 — v7.1.1 / prospective small-Transformer falsification and stale-Handoff repair

**Nature:** FIELD NOTES for future GitHub Research Kernelization Skill, NOT a working Skill. Compiler-generated v7.1 continuation. Scientific conclusions are restricted to the small local experiment, not to natural-language understanding or SMFT Attractors.

## Case A — Real engineering experiment, not model-assisted storytelling
- **Case/trigger:** Prior v7.1 `GL71-01`, seeds 17/23/41 demonstrated post-hoc heterogeneous post-layer1 CLS sufficiency; risk of fitting a narrative after seeing three outcomes.
- **Procedure actually performed:** A fixed protocol containing model setup, entirely new seeds, prediction function, null baseline, two acceptance criteria and control-model plan was written and SHA256-locked before executing the twelve new PyTorch training runs. The existing 5-bit majority architecture and train/test split were reused deliberately. Saved CPU checkpoints, every receiver/donor counterfactual outcome, continuous margins, per-model summaries, code and environment. Independent verification reran 24 patch spot checks from saved states and 13 data/protocol assertions.
- **Observed:** eight new normally trained models each reached 8/8 heldout task accuracy but CLS-only donor patches succeeded 15/15,15/15,15/15,15/15,9/15,9/15,15/15,0/15; prospective ordinary-gradient predictor did not improve binary decisions in any of eight seeds versus unchanged receiver. Continuous margin MAE improved slightly in seven of eight. Single off-target bit-token negative controls succeeded on 2 of 120 cases. Earlier post-hoc 30/45 does not imply a universal CLS causal port.
- **Failure modes:** conflating independent model initializations with independent data splits; treating 120 dependent donor/receiver cases as 120 independent replications; backprop derivative of a nonlinear map as a reliable large-amplitude intervention forecast; selecting a more favorable criterion after a primary failure; attributing standard-gradient observations to SMFT.
- **Repair rule:** lock prediction/seed/test split before execution, preserve per-model outcomes and target-conditioned eligibility; run standard equal-budget methods; report all predeclared success and failure criteria, data leaks/overlap and matched negative controls. Retain checkable raw models and raw patch rows, not only summaries.
- **Generative residual:** use full donor→receiver path and Hessian bounds, test under new task splits and architectures, predict rather than merely localize functional state positions. Current status: local trained-Transformer experimental observation, NOT scientific validation of semantic attractor mechanism, and independent source-hidden LLM benchmark NOT_RUN.

## Case B — Mathematical repair without changing source authorship
- **Trigger:** A smooth nonlinear function can change sign over a finite donor jump even when its receiver derivative is exactly zero.
- **Actual proof:** `m(t)=-1+2(3t²−2t³)` yields `m(0)=-1,m'(0)=0,m(1)=1`. Added conditional Hessian/Taylor remainder bound as a correctable weak version. Not a claim that this exact polynomial describes observed Transformer dynamics.
- **Future Skill implication:** automatically separate pointwise sensitivity, finite perturbation and exact fiber-congruence certificates, and demand an admissible intervention protocol before labeling a reduced representation functional.

## Case C — Release governance can silently lag scientific progress
- **Trigger:** v7.1 FULL has scientific results and Skill Note 32, but `00_GOVERNANCE/00_READ_ME_FIRST.md` and `99_HANDOFF/99_SESSION_HANDOFF.md` + flattened counterparts begin at v7.0; the latest Skill Matrix is v7.0 and does not list Note 32.
- **Actual audit/repair:** make a version-qualified 7.1.1 patch rather than mutate v7.1 in place; prepend accurate current Boot/Handoff, ensure flat copies are exact matching canonical bytes, append Note 33 and create a full 34-note hash matrix; preserve previous historical files byte-for-byte.
- **Failure mode:** ZIP CRC and artifact counts can pass while the next session is pointed at a stale research state. Automated test must verify newest handoff version, current provenance directory, Skill matrix coverage, and master→flat equality.
- **Future Skill implication:** separate semantic-release invariants from ZIP integrity; record actual test scope. No official SKILL.md has been written.

## Capability coverage
1. Conflict audit & conditional repair: **executed**, Taylor counterexample.
2. Constructive residual discovery: **executed**, failed H1 gives path-integral/curvature experiment.
3. Optional attractor kernel: **NOT VALIDATED**; ordinary-gradient baseline unchanged.
4. Human analogy guided generation: **NOT_RUN**.
5. Hypothesis-driven experimental research: **local executable case only**, not yet a proven general-purpose Skill.
