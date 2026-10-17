# v5.7 Field Experience — Gate polarity, replay order and maturity source depths

This is a *real project field note*, NOT `SKILL.md` and not a hypothetical GitHub product.

1. **Opposite-sign magnitude acceptance**: `SRC-0130` p.23 `sign(I_obs)=sign(I_pred)` plus `abs` bound accepts predicted harmful controller. Always test both favorable and adverse signs as negative controls, not just model-fit correspondence. `GL57-01`.
2. **State variance vs sensor instability**: `SRC-0130` p.21 interprets raw state variance gate as proxy stability; exact changing plant falsely fails, uninformative fixed sensor falsely passes. Require observability and same-state sensor repeat error; `GL57-02`.
3. **Correlated controls vs intervention**: `SRC-0130` pp.15–18 includes both correlation shortcut and one-channel MEP. Preserve author intent: covariance signs descriptive, intervention designs causal. Rank-deficient co-varying channels can hide nonzero opposite effects (`GL57-03`).
4. **Typed event replay**: `SRC-0237` p.76 `Σ A_k` is convenient notation, but real event application is order-sensitive. Distinguish an event log inventory from deterministic ordered replay; store explicit preconditions, sequence and conflict resolution (`GL57-05`).
5. **Processed source != true claim**: coverage ledgers and typed closure preserve provenance, not outside mathematical validity. When truth oracle missing keep contradictory or speculative material visible; never promote because all segments processed (`GL57-06`).
6. **Corpus coherence != Kernel competence**: `SRC-0212` pp.24–31 proposes adaptive compression by domain coherence but does not demonstrate independent efficacy; echoed false source claims can create high coherence. Route residuals without erasing ideas; reserve promotion for an independent task (`GL57-08`).

QA requirements: record exact original TAR member SHA, physical page scope, countermodel, surviving weaker theorem, no hidden-rubric leakage. Do not turn this field note into an executable Skill yet. Prior notes are byte-immutable.
