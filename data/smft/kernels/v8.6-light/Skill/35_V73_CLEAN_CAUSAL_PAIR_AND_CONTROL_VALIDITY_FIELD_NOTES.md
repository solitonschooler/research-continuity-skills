# Skill/35_V73_CLEAN_CAUSAL_PAIR_AND_CONTROL_VALIDITY_FIELD_NOTES.md

**Case:** V73-UNSEEN-PAIR; **Capability:** Hypothesis-Driven Experimental Research (candidate), Conflict Audit, Constructive Residual. **Status:** executed local CPU PyTorch proxy experiment; not a general skill validation.

## Trigger
v7.2 had 106/122 eligible donor examples drawn from training. A heldout receiver alone did not warrant fully unseen causal generalisation.

## Actual procedure
Freeze 7-bit majority, stratified 96/32 split, 3 seeds, 300 update steps, pair eligibility and controls in a protocol BEFORE training. Pre-enumerate 24 directed both-heldout opposite-label single-bit pairs; save seeds and checkpoint state, original models and all intervention outcomes; replay. Full-state positive control, alternate bit patch control.

## Observed result
All 3 models reach 32/32 test; CLS patch 12/24,0/24,7/24. Full hidden state patch 24/24 each. Alternate-bit patch changes answer in 0/24,5/24,5/24: do NOT label universally inert. Recorded sample unit = trained seed, not each patch row.

## Failure modes and repair rules
1. **Holdout endpoint asymmetry:** verify both donor and receiver absent from optimization, not only receiver.
2. **Control invalidity:** offsite perturbation is not automatically a null intervention; report its effect rather than conceal it.
3. **Success-count inflation:** directed pair outcomes share weights and training data; avoid binomial independent-trial confidence claims.
4. **Uncontrolled architecture shift:** 5-bit to 7-bit tasks change sequence length and patch mechanism; compare only as conditional differences, not causal architecture-free improvements.
5. **Attractor laundering:** no inference from patch diversity to semantic attractor, cognition or ontological basin.
6. **Compute interruption:** failed initial run after two seeds; save checkpoints immediately, resume with frozen planned seed and replay old seeds, never change design or conceal interruption.

## Generative residual
Identify genuinely inert mechanistically matched negative interventions, characterize CLS information non-uniqueness across models, and test beyond one small task with independent data splits and larger seed counts. Compare with equal-budget standard representation and causal tracing tools. Skill should validate provenance and no-leakage at both ends, explicitly grade controls as VALIDATED/FAILED/UNKNOWN.
