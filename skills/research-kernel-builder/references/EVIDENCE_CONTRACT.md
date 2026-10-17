# Research Evidence Contract — 0.2.0 (canonical)

This contract is required regardless of effort profile. It specifies obligations and semantics, **not** the method, programming language or model used to fulfill them. The JSON Schema (`research-state.schema.json`) is an optional full-form machine-readable encoding for larger/iterative jobs; a small job may maintain the same distinctions in a readable report.

## Core objects

1. **Source** — stable ID, title, revision/identity, actual access and reading depth; hash only if *computed or reliably supplied and distinguished as such*. Inventory ≠ extracted ≠ read ≠ audited.
2. **Assertion** — precise claim, actual source role, source fidelity, assumptions, epistemic status, lifecycle status, evidence anchors. Preserve author statements separately from agent formalizations, stronger test propositions and new deductions. A counterexample to an agent-strengthened claim must not automatically be attributed as an error in the source.
3. **Relation** — typed link and justification. `DERIVES_FROM` demands a sound derivation; `HISTORICALLY_INFLUENCED_BY` indicates documented history; `ANALOGOUS_TO` indicates resemblance without entailment; `SUGGESTS` is a research lead, not a theorem.
4. **Residual** — missing evidence, outstanding proof, contradiction, unexplained mechanism, experiment gap, attribution uncertainty or failed test, with a discriminating next step when one exists.
5. **Verification receipt** — what was *actually* checked, by whom/what, using which evidence, whether it passed, failed, was inconclusive or never ran, and its limits. Self-review is not independent review.
6. **Round + Handoff** — bounded objective, read scope, typed changes, receipts, unresolved issues, stop reason and next entry. A round can be `PAUSED` with useful output; old state remains recoverable.

## Evidence and validity are multiple axes

Do not compress the following into `verified: true`:

- **Origin:** source author; human researcher's new interpretation; agent reconstruction; new agent-generated claim; unknown.
- **Source fidelity:** verbatim/paraphrase/formalization/stronger claim/narrower claim/alternative/unverified. Re-open original scope if changing quantifiers (`all` vs `some`), sufficient vs necessary conditions, units, signs or parameter domains.
- **Epistemic type:** conjecture, conditional proposition, within-model proof, counterexample, observation or unresolved. A mathematically proven *conditional* theorem does not establish the conditions occur naturally.
- **Lifecycle:** active/revised/superseded/rejected. Superseded work remains historically visible.
- **Verification method:** source compare, formal derivation, manual mathematical audit, computational check, synthetic or empirical experiment, independent review or not performed.

## Fidelity and mathematical promotion gate

For each high-consequence formal statement ask:

1. What exact source spans support the attribution, and were those spans actually inspected?
2. What assumptions, quantifiers, variable meanings, observers and relevant operators are required?
3. Is this a source-authored claim, an agent-created formalization, a stronger test, or a new result?
4. Does a claimed isomorphism preserve the specified operations, transitions, observables and admissible interventions, or merely map labels one-to-one?
5. Can a small counterexample refute the claim? Does it refute precisely the source claim or only a stronger formulation?
6. Has the claim survived a mathematical review, or merely a matching citation, local numeric test or synthetic demonstration?

If unresolved, use `INSUFFICIENT_EVIDENCE` and preserve the question. Do not invent missing pages, dates, proof lemmas, test executions or citations.

## Version and lineage gate

An older result is not invalidated by omission from a newer delta. Track explicit `REVISES`, `SUPERSEDES` (via lifecycle), `CONTRADICTS` and `HISTORICALLY_INFLUENCED_BY` separately. Before combining near-duplicate claims compare their assumptions and quantifiers; choose separate IDs for non-equivalent results. Changes should be append/revise with history rather than destructive replacement.

## Experimental gate

Before reporting experimental support, identify test intervention, measurement, dataset origin, negative control, ordinary comparator, leakage/contamination risks and applicability limit. "Source structure recovered from implanted data" does **not** demonstrate "structure self-emerges in real systems." No unexecuted protocol may be labelled `EXPERIMENT_EXECUTED`.

## Limits of this schema

Structural validation may detect malformed JSON, missing fields and invalid status values. It **cannot** establish citation truth, historical causality, mathematics, source hashes, referential uniqueness, nondisclosure or scientific validity. An agent with suitable tools may verify these and record receipts; otherwise mark the relevant check `NOT_RUN`. An independent challenger still needs the cited source and must not be shown private benchmark answers.

## Minimal output for a 10-document job

A concise narrative + table can satisfy the contract if it contains: actual coverage; significant source-anchored claims; typed disagreement/revision; new-agent contributions labeled; unverified matters; work performed; why it stopped; and how to resume. Avoid turning the protocol into an obligatory large graph.

**R8 clarification:** The schema rejects a source-authored claim with no anchor, a `NOT_PERFORMED`/`PASSED` receipt, and a saved checkpoint with no location. It still cannot verify unique IDs, actual source existence, cross-record references, or scientifically true claims. Apply [Acceptance Gates](ACCEPTANCE_GATES.md) independently.
