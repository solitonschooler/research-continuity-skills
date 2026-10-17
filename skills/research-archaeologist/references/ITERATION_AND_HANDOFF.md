# Bounded Iterations, Improvement Receipts, and Handoff

## A research round is a proposed state transaction

An iteration may add, confirm, weaken, reject, revise or relate an existing claim. Preserve earlier states or changes where resources permit. The intention is *auditable change*, not database transaction guarantees or mathematically monotone quality.

**Before:** current best state, scope, known gaps, read-depth record, pending permissions.  
**During:** prioritize high-impact feasible uncertainties; record what evidence was actually inspected and what actions were executed.  
**After:** publish the change set, receipts, unresolved residuals, next entry and stop rationale. Do not label a partial round complete.

## Research Improvement Receipt (human readable)

A single round should identify, when applicable:

- **Consolidated:** claim IDs/material merged or indexed, without conflating distinct propositions.
- **Confirmed:** exactly what survived which source/math/tool check.
- **Corrected / refuted:** the specific target claim, minimal counterexample, valid fragment and affected descendants.
- **New agent contribution:** conditional lemma, alternative explanation, hypothesis, missing development, test design, with origin separated from original authors.
- **Experiment:** test actually run versus protocol only; baselines, negative controls, results, limits.
- **Unresolved:** missing source/conditions, ambiguity, resource limits or external-validation requirement.
- **Continuity:** files actually saved, state/version ID, next best action and blocked actions.

For a very small corpus, this may be one short table, not a large JSON ledger.

## Profiles and stopping policy

- `SCAN`: inventory and rapid issue map; do not imply full reading.
- `COMPILE`: bounded source-constrained current research state.
- `VERIFY_REPAIR`: selected critical verification, non-entailments, mathematical or implementation repairs.
- `DEVELOP`: new conditional deductions, missing ancestors, falsifiable hypotheses; no guarantee of novelty.
- `EXPERIMENT`: only authorized/feasible checks; distinguish plans from executed trials.
- `ITERATIVE_FULL`: repeated priority-driven rounds with explicit user budget and checkpoints.

The user can start at any profile, switch profiles and stop after any round. A user instruction to stop immediately overrides a plan for more work; if persistence is unavailable, provide a copyable checkpoint text and say persistence was not verified.

**Stop when:** requested scope complete; user requests stop; additional rounds have no plausible discriminating value under current resources; evidence is insufficient to proceed; a validation or authorization gate fails; or the budget is exhausted. Do not infer a target's real-world emergence from the ease of deriving consequences under assumed conditions.

## Minimal continuity test

An unfamiliar new agent, seeing only the saved state and cited available evidence, should be able to answer: What was examined? What was concluded and with what scope? What failed? Which claims are historical vs new? Which checks were actually performed? What should be checked next? Which resources are still missing?

A later independent test should measure these against generic-agent and retrieval baselines at comparable budgets. A same-session self-recap does not count as independent evaluation.

**R8 clarification:** For full JSON states, follow the [Acceptance Gates](ACCEPTANCE_GATES.md) to check that a cited checkpoint actually exists. A location string alone does not prove successful persistence.
