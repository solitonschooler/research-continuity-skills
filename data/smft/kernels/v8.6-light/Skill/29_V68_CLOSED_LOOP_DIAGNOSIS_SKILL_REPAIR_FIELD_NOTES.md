# v6.8 Field Notes — Closed-loop Experimental Repair and Candidate Research Skill

**Not a runnable Skill.** Source-bounded v6.8 work reuses SHA-verified original `SRC-0298` p9, `SRC-0299` p7, `SRC-0261` pp6/14 and `SRC-0130` p23. New Python assay is compiler authored and synthetic. Continue the four user-requested future functions: (1) paper conflict detection and conditional repair, (2) residual→testable future research, (3) optional Attractor mathematics contrasted with ordinary techniques, (4) user analogies→formal rival predictions. None of the latter two creative gains were measured.

## 1. Critical experience from code and paper auditing

- **Do not infer an active causal pipeline from an event ledger.** First assay run raised many alarms yet all controller results exactly matched the fixed-feedback baseline: although `r_t` was measured, the historical residual update buffer was not written. Fix: write `prev_r[:,t]=r` before the next action, and add end-to-end regression requiring the alarmed-control trajectory to differ under sustained bias. Never treat unit-tested detector alerts as successful policy execution.
- **Domain-specific success must include a designed failure regime.** When the shift is persistent bias, dual residual monitoring plus bias correction lowers quadratic proxy cost, but when only volatility doubles, the same policy worsens cost. If an old research article asserts directional residuals always help, repair its quantifier: *help when direction indicates an identifiable persistent fault and action remedy is appropriate*.
- **Information-matched rival first.** Conventional signed CUSUM reads the same signed residuals; its drift costs are close to dual's. Retain this negative novelty control even if Attractor language inspired the test. Do not use magnitude-only as the sole weaker comparator.
- **Causal identification before action:** observed `r=b+gu+noise`; with no variation in `u`, gain and bias cannot be separately identified. Issue a `REQUIRES_INTERVENTION` edge and propose safe persistent-excitation test; do not infer agent ontology from residual coherence.
- **Keep all policy comparisons honest:** separately report true (post-action) state cost, effort, surrogate failures, null false alarms, no-action vs fixed-feedback baseline, and privileged oracle bound. Same exogenous noise across policies is a paired experimental design; in gain shift policy actions alter residuals, so old fixed-path replay is insufficient.

## 2. Research-generating residuals and creativity module

- Conflict: a Gate triggers but may worsen total cost. Conditional repair: require fault-type diagnosis (persistent bias versus volatility versus action gain). Generative move: `detector → intervention choice → prospective expected regret` rather than `detector → automatic success`.
- Attractor optional mathematical lens: compare convergence/long-memory claims to plain Lipschitz/CUSUM under the *same features, compute, and data*. Under no uplift, record result as equivalence or ordinary baseline success, not new SMFT law.
- Human analogy: convert a user-proposed metaphor (e.g. a basin shifts) into two or more contradictory observable predictions and a disconfirmation experiment; preserve analogy as `SUGGESTS`, never `DERIVES`.
- For a future GitHub Skill: output a typed proof/evidence DAG, negative controls, diagnosis-vs-detection audit, specific executable test plan and versioned residual/provenance ledger; report hallucination and invalid repair costs. Never self-certify scientific creativity or source-hidden reconstruction using local simulation.

## 3. Reusable check

`Immutable source claim → typed quantifier → explicit counterexample → conditional positive mechanism → end-to-end intervention wiring → matched-information standard baseline → adverse regime → generative residual → fresh nonprivileged test → Skill ledger.`

Previous 29 notes remain byte-identical; original sources and protected 40–44 unchanged. **No independent LLM, neural Attractor, or creativity uplift experiment conducted.**
