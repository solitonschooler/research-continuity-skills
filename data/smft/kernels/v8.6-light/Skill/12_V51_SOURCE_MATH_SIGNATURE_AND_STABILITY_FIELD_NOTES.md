# 12 — v5.1 Source-verified cross-family proof and test-oracle pitfalls

This is **field experience for future Research Kernelization Skill design**, NOT the final GitHub `SKILL.md`. Real working examples and exact source math are in `90_PROVENANCE/GENERAL_LEMMA_REGISTER_v5.1.md` and local tests `test_v51_family_skeletons.py`. Scope: five original SHA-verified PDFs at specified physical pages; no whole-PDF reading claim.

## 1. A Lyapunov function can decrease for the wrong reason

`SRC-0108` pp.13–14, Theorem 8.1 used a nonnegative energy of the Δ5 symmetric projection and uniform damping. Its proof inferred convergence of *phase differences* to π. A permissible linear initial condition with pair `x=y` preserves relative phase 0 forever while x,y→0 and the projected energy→0. Even strong asymptotic convergence **in norm** to a target set containing 0 need not select a nonzero pattern or relative mode.

**Reusable gate:** identify the observable being claimed (absolute norm vs normalized phase vs finite-time response), whether its denominator can tend to zero, and whether transverse decay is genuinely faster than tangent decay. Test the simplest admitted symmetric eigenmode before applying LaSalle. Mark any invalid strong consequence as refuted while preserving the valid lower-level energy inequality and static optimizer.

## 2. An impressive empirical signature may be true by definition

`SRC-0108` p.14 §8.5 defines partner fluxes by the imaginary part of opposite complex products. They necessarily satisfy `Pi_partner=-Pi` for all states, not just phase lock. At exact antisymmetry, both become identically zero and correlation is undefined. An experiment reporting partner correlation -1 would not distinguish the theory from its null model.

**Reusable gate:** compute candidate measurement on (a) target model, (b) explicit non-target positive/negative control, (c) degenerate zero-signal cases. Report discriminative power rather than algebraic truth. This applies to gauge holonomy, attractor readout, ledger residual and periodic/cycle statistics.

## 3. Cross Proof Family algebra is not a cross-domain entailment

The equation `dot V≤0` occurs in convex duality, damped mechanics and phase amplitudes; PF07, PF10 still use different states, energy definitions, and invariant sets. Gauge PF06 uses transformation/cochain invariance, not an automatically dissipative state law. Require a precise typed mapping before relabeling analogous proofs as `DERIVES`.

## 4. Sign/measure mismatches must be challenged in the original symbol conventions

`SRC-0287` §3.3 and §3.6 mistakenly assign restoring sign to a negative subgradient under an additional minus in the evolution. Treat `dot Delta=-mu, mu=-grad V` as an anti-gradient unless the source actually changes one sign. Bounded **nonzero** stochastic forcing can leave nonzero stationary variance even when deterministic drift is restorative: control-theoretic boundedness is not convergence in probability to the exact point.

## 5. Successful proofs can be compiler-derived, not source-authored

The new `dot G<=0` follows only after **we declare** a negative-residual joint flow; the original convex paper provided `G` and gradients but did not thereby establish this flow or its efficacy. Preserve distinct fields for `SOURCE_CLAIM`, `COMPILER_REPAIR`, `INTERNAL_MATH_CHECK` and `EXTERNAL_EMPIRICAL_VALIDATION`. Never credit a mathematically valid new controller to the upstream author without evidence they asserted that controller.

## 6. Benchmark leak fence is not a result

The local FULL includes pre-existing private tasks/rubrics; the three C0/C1/C2 participant input packs are staged, not tested. Do not send FULL, this audit, or rubrics to trial participants if testing source-hidden reconstruction of these exact claims. Source material in earlier model context or training may also contaminate claimed independent holdout. Use a genuinely separate model, fresh private problem generation, matched budgets, and a RAG baseline before making performance claims.

**Preservation:** v5.0 `Skill` 12-note historical hash matrix remains unchanged. This new numbered field note is an added experience artifact; no protected 40–44 Kernel file edited, no executable Skill created.
