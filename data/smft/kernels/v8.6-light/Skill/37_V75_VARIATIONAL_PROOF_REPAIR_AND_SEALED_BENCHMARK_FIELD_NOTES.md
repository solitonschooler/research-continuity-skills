# Skill/37 — v7.5 Variational proof repair and sealed-benchmark governance (FIELD NOTES)

**Status:** actual SHA-matched original-PDF bounded review and 20/20 math + 16/16 sealed-gate local tests; no independent participant LLM, no independent scientific validation. Not a finished `SKILL.md`.

## Case V75-RAYLEIGH-ACTION
- Trigger: `SRC-0048` pp4–5 asserts variation of integrated velocity-square `Γ` produces drag `c qdot`; reused by `SRC-0057` p5/9.
- Actual procedure: retrieve original TAR member, verify bytes and SHA, read physical PDF pages, visually inspect equations, execute symbolic Euler derivative and exact path counterexample.
- Observed: `δ∫(c/2)qdot²/δq=−c qddot` not `c qdot`; complex action coefficient omitted and damping sign printed inconsistently. Source claim fails under its own fixed-endpoint action assumptions.
- Repair rule: distinguish **functional derivative** `δΓ/δq` from **instantaneous velocity partial derivative** `∂R/∂qdot`; allow Lagrange–d'Alembert/contact/doubled-state alternatives as separately stated theories. Never rewrite old source as if it already had this repair.
- Generative residual: test corrected models with controlled energy budget and state-space domain; compare to ordinary mechanics and causal controls.

## Case V75-PENALTY-NOT-DAMPING
- Trigger: `SRC-0057` infers asymptotic attracting trajectories from a nonnegative convex constraint penalty.
- Actual procedure: model quadratic action, prove undamped oscillator exact solution with conserved total energy; check rank 7/2D affine LoShu families and boundary soft hinge.
- Negative result: quadratic position penalty ≠ dissipation, constraint minimum ≠ unique configuration, finite hinge ≠ hard barrier. `max(0,x)²` is C¹, so claiming it is only subdifferentiable at 0 is too weak.
- Conditional repair: gradient flow or damped ODE + Lyapunov decrease plus extra existence, boundedness and convergence assumptions; independent falsification still required.
- Failure to avoid: symbolic resemblance to `entropy`, `attractor`, `energy` as a substitute for correct derivatives; treating a symmetrically equivalent family as isolated minimum without explicitly quotienting.

## Case V75-SEALED-EVALUATOR
- Trigger: C2 historical Kernel pack has ~15.449× C1 whitespace-word volume; old private rubric already inside compiler FULL.
- Actual procedure: implemented `sealed_trial_gate_v75.py`; 16 local synthetic anti-leak / budget / metadata cases PASS; inspected an inherited participant pack: filename/CRC lexical gate is not semantic separation.
- Negative result: No external hidden tasks, frozen actual tokenizer logs, independent subject or grader available. **LLM Benchmark NOT_RUN**; no score, no evidence of Kernel uplift.
- Repair rule: require outside source curator, sealed private grades and task commitment made without compiler access, identical real tokenizer budgets and model/tool constraints, independent trial receipts, blind grading, and nested-task statistical treatment. Fail closed otherwise.
- Future optional Skill capability: `Hypothesis-Driven Experimental Research` and `Evidence Reconstruction Integrity` should include a cross-source **mathematical dependency breaker** and an **externalized blinded-judge gate**. Both should preserve failed claims and countermodels as generated research assets.

## Evidence limitations
Selected PDF pages only; no complete primary-source line-by-line certification. 20 tests reproduce basic mathematics, not dissipation empirics. 16 gates validate artificial fixtures only, not LLM quality. Pre-existing science and ordinary math baselines remain valid; do not claim unique SMFT value. Historical original hashes and all earlier Skill notes preserved.
