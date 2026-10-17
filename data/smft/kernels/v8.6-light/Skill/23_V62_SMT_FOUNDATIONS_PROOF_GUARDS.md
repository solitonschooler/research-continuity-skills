# v6.2 — SMFT Foundations Original Theorem Proof Guards (Skill field experience)

**Observed, not hypothetical.** Source `SRC-0270` actual p.15/p.58 uses
Pinsker in the **wrong direction**, effectively asserting a universal
TV² lower bound on KL. The apparently mathematical deduction looked credible
until checked on two-point distributions near singular reference mass.
Compiler rule: for a claimed inequality chain, state each inequality's
actual direction and quantify constants *before* composing claims; test near
boundary distributions, not just symmetric examples.

**Observed measurement conflation.** `SRC-0270` pp.8,13,57–58 treats joint
POVM compatibility as observer-agreement. Two commuting binary PVMs can give
different marginals in the same state; joint measurability does not mean
dependent outcomes. Compiler rule: separately label `COMMUTES`,
`JOINT_MEASURABLE`, `EQUAL_DISTRIBUTIONS`, `INDEPENDENT` and
`FRAME_COVARIANT`. Require the specific co-transformation or mapped
proposition predicate for the last two claims.

**Observed sign/convention trap.** `SRC-0270` p.7 describes `H_s` as
anti-Hermitian inside an equation written `i ℏ ψdot = Hψ`. Here norm
conservation normally uses **self-adjoint** H; the *time-evolution generator*
`−iH/ℏ` is anti-Hermitian. Distinguish the operator being tested, not only
its adjective. A one-complex-dimensional exponent is an effective
negative control.

**Evidence hygiene.** Raw SHA-256 match and physical-page rendering do not
make an entire source fully read, nor make mathematical local models true in
neural/physics domains. Preserve a source text assertion, a concrete
countermodel, and separately the repaired conditional theorem. New GL audits
must be appended cumulatively to CURRENT_Vxx; old Current snapshots and
original Skill file hashes stay immutable. Beware old unittest assertions
that hardcode the prior active Atlas label. Do not erase test obligations to
make a new release green.

**Benchmark:** Re-running same-model mathematical checks is not an
independent, source-hidden LLM reconstruction study. N remains 0 until an
isolated model answers and a genuinely private rubric scores it.

Source anchors and equations: `GENERAL_LEMMA_REGISTER_v6.2.md`,
`SOURCE_IDENTITY_AND_DEPTH_v6.2.json`.
