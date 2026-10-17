# Research Archaeology — Investigative Guide

## Ask a discriminating historical question

Examples: When did assumption A first appear? Did B refute it or merely change scope? Did an AI coding agent actually exercise the patched branch? Did several reports repeat one original source? Was a proposed solution abandoned because it failed or because evaluation stopped?

## Evidence map

For each material episode keep (a) records and exact locations; (b) what the actor explicitly said/did; (c) tests or observable outcomes; (d) later interpretation; (e) independent assessment and missing evidence. Distinguish source timestamps from inference about chronological order. A missing log is not evidence of a nonexistent experiment.

## Three reconstructions, never one blended story

- **Documented history:** traceable claims, decisions, commits, calculations, negative results and their actual temporal order.
- **Causal hypothesis:** possible explanation for a change, with explicit alternatives and needed discriminating evidence. Temporal sequence ≠ causal proof.
- **Rational reconstruction:** a better derivation or development path invented now. Useful for improvement, but not a historical attribution.

## Common traps

1. A later paper can correct a result but still inherit a hidden earlier error. Track propagation rather than counting repeated citations as independent support.
2. A source may assert only necessity, while a later compiler accidentally claims sufficiency. Test attribution before issuing a mathematical rebuttal.
3. A commit note saying "bug fixed" does not prove the change was loaded, tested or causally responsible. Separate source assertion from runtime evidence.
4. A supposedly independent multi-agent conclusion may share one prompt, dataset, dependency or ancestor document. Audit actual independence.
5. The *absence* of a result in a newer summary is not its refutation. Inspect previous artifact and explicit migration links.
6. The apparently wrong historical path may contain a generative insight. Preserve original failure, valid fragment and testable alternative separately.

## Scope control

A local audit of 5–12 documents is often enough to test the method. Do not require a giant long-lived Kernel for every investigation. If the user wants active improvement, select only high-value, feasible candidates and apply the optional advancement guidance. Publish a readable chronology, annotated disagreements, narrow repair suggestions, verification limits and a continuation checkpoint.

## Specialized domains

Software: identity may include commit/PR/build, and confidence requires observing tests or implementation. Research mathematics: retain axioms, quantifiers, exact formula semantics and countermodels. Product history: distinguish documented decision rationale from plausible post hoc motivation. All can use generic `Source`, `Assertion`, `Relation`, `Round`, `Residual` and `Receipt` with optional `extensions` fields.
