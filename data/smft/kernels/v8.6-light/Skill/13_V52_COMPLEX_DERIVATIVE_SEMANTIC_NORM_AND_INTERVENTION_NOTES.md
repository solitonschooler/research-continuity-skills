# v5.2 observed source-audit field notes — NOT a runnable GitHub Skill

This note documents **actual** errors/limits seen while re-opening SHA-matched original PDFs. It supplements `12_...` and older field notes, not a replacement for them.

## 1. Differentiating then simplifying can silently drop the driving derivative

`SRC-0043` p.27 (3.27) has a valid differential term `dr_CAPM/dt`; (3.29) and (3.31) lose it when the base rate is frozen. This creates spurious nonzero angular velocity at a **constant** CAPM rate. Audit every algebraic **step in a derivation chain**, not only the boxed or first formula. Use a `constant-input → zero-output` negative-control test and dimensional sanity checking.

## 2. Source domain constraints can determine whether a model exists

`SRC-0023` p.6 claims `A=|Z|` and `Q=sqrt(A²−R²)`. The same paper's p.11 CAPM construction can yield `R/A>1` when the CAPM rate is below the declared base. Signed future cashflows can make its "amplitude" formula negative. A **well-definedness test** should precede any theorem/forecast test. Repair may restrict admissible data, not necessarily refute the conceptual analogy.

## 3. A Schrödinger-like syntax need not imply norm or measurement validity

`SRC-0268` pp.2–3 explicitly adds `-iΓ Ψ`, external drive `J`, and observer coupling to an SSLE. A complex-valued field then need not preserve `||Ψ||²`. For every probability word, separately inspect (i) Hilbert or state-space choice; (ii) norm balance; (iii) positivity; (iv) completeness of channel effects; (v) time/rate calibration; (vi) boundary flux. Example: real exterior Robin `∂nΨ=κΨ` yields zero normal probability current despite a plausible “gate-throughput” analogy; interior interface jumps are different.

## 4. A domain analogy requires independent causal intervention contracts

`SRC-0261` p.6 exact Port closure under declared interventions cannot be inferred from `SRC-0247/0268` proposed semantic field/collapse operators. Demand an actual neural state map, clock, admissible actions, hidden-channel negative controls and natural formation experiment. Use edge `TRANSLATES_ONLY` when no actual representation-preserving map is supplied.

## 5. Confirm known corrections without laundering them into new discoveries

`SRC-0043` pp.8–9 itself distinguishes identities versus empirical hypotheses, and historic RA-M09 already recognizes a polar-identity residual is zero. Reopening this source strengthens provenance; it does **not** justify claiming an original v5.2 theorem. Stable W IDs and revision dates remain separate from compiler findings.

## 6. Blind model evaluation remains blocked, not “complete”

C0/C1/C2 participant-stage ZIPs exclude private rubrics but no separate independent LLM endpoint or fair RAG control is available within the current runtime. Leakage lint and math unit tests do not substitute for an independent reconstruction score. Never expose FULL with answer/rubric materials as participant input.
