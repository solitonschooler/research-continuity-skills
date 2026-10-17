# Skill/38 — v7.6 Falsifiable dissipative LuoShu dynamics versus conventional optimization (FIELD NOTES)

**Case ID:** `V76-LOSHU-REAL-RELAXATION`; related `SRC-0057` inherited v7.5 bounded source reading, GL75-02/03 → GL76-01/02/03 → RA-H04. Evidence is **compiler-owned synthetic numeric** plus standard mathematical proof. No fresh PDF deep audit or independent physical validation; this is NOT a runnable GitHub Skill.

## Trigger
The previous round repaired an invalid assertion: a quadratic *position penalty* does not automatically create friction. New question: even with correctly specified dissipation, does the claimed LuoShu attractor offer an engineering advantage or actually select LuoShu configurations?

## Actual procedure
Construct the eight row/column/diagonal 3×3 line constraints, check rank and nullspace, compare (i) direct least-squares projection, (ii) standard GD, (iii) GD merely relabelled as LuoShu flow (algorithm-identity negative control), (iv) explicitly damped mechanics, (v) undamped mechanics. Use the same 96 saved real-valued initializations, 400 iterative gradients, 401 steps per case, explicit source code, 192480 per-step records, all 9! distinct-digit assignments enumeration, and 17 executable data/math integrity checks.

## Observed positive and negative evidence
- Damped mechanical ODE does have an exact **total energy** decay identity under its stated assumptions. This is ordinary classical mechanics, not a special cultural or semantic mechanism.
- At the chosen finite iteration budget, ordinary GD gets constraint residual <1e-6 on 96/96, damped Euler only 3/96. A rebranded identical GD step has *identical* output. A one-shot pseudoinverse also solves the affine feasibility system but has a different computational cost model.
- Zero line-sum residual need not be a valid digit permutation: all fives is a counterexample even under entry bounds 1..9. There are eight actual discrete digit-permutation solutions (D4 copies), but a continuum of real feasible states. A minimizer *set* is not a unique attractor point.
- No trained Transformer, independent LLM Reconstruction, natural Semantic Attractor, creativity uplift, or real dissipative measurement in this version.

## Failure modes and repair rules
1. **Observable mismatch**: measure residual to the declared affine constraint and also valid digit assignment; never merge them.
2. **Control mismatch**: 'damped', 'penalized' and 'gradient' are different operators; check actual differential equations, not labels.
3. **False uniqueness**: identify null directions, equality of states vs symmetry quotient, and initial-condition dependence.
4. **Baseline concealment**: include exact linear-algebra solve and ordinary iterative methods; never call algorithmic relabelling novel.
5. **Budget concealment**: direct projection is not matched to 400 gradient evaluations; compare setup cost as well as numerical error.
6. **False preregistration**: a 32-run pilot occurred before 96-run final; record the experiment as exploratory, not preregistered.
7. **QA inflation**: 17/17 synthetic consistency checks do not mean scientific maturity or a successful external model trial.

## Generative residual and future Skill implication
Require an automatic `Claim → mathematical state domain → measured observable → ordinary baseline → disconfirming control → failure scope → next experiment` gate. For many culturally named systems, preserving their additional combinatorial/orientation priors (if genuinely declared) may be more valuable than claiming a new dissipation law. A generic Research Kernelization Skill should know when a universal dynamical term is simply standard optimization and should preserve both the surviving representation and the counterexample. Capability 5, hypothesis-driven experiments, remains optional and falsification-first.
