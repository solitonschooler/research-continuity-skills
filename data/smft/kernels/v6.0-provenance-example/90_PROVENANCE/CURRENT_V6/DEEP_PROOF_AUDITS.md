# CURRENT V6 — Consolidated Local Proof Registers (GL/L audit history)

**Important:** This is a full-text concatenation of v4.5–v4.9 source-scoped proof audits and GL50–GL59 authored episodes. All formulas retain their original version-qualified scope. It is *not* a proof of SMFT ontology, no new GL numbers minted, and no independent LLM benchmark run. GL53 does not exist because v5.3 worked on benchmark architecture.



---

# Imported original audit: `PROOF_DEPENDENCY_RECONSTRUCTION_v4.5.md`

**Source audit SHA256:** `725f971c5f00cf46e441423532c713935933428bac5f0d0e700caaf5e26b8c47`. Original record, no silent proof strengthening.

# v4.5 Source-anchored Proof Dependencies — first Global Depth / Atlas challenge

Date: 2026-10-15. This is a **source-page-scoped audit**, not whole-document validation,
independent LLM reconstruction, or real-world physics/AI/health evidence.
Primary source identities and SHA-256 matches: `SOURCE_IDENTITY_CHECK_v4.5.json`.
No new W, PF, GM or RA identifiers are minted; these local `L45-*` nodes are *dependency audit IDs*.

## L45-01 — Exact convex duality; false budget identity

**Premises.** Proper closed convex `psi`, `Phi=psi*`, and a differentiable paired path
`lambda(t)=grad Phi(s(t))`, `s(t)=grad psi(lambda(t))`.
The Fenchel–Young relation is `Phi(s)+psi(lambda)-lambda·s=0` on this path.

**Proof.** Differentiate either convex potential:
`dPhi=lambda·ds`; `dpsi=s·d(lambda)`;
`d(Phi+psi)=d(lambda·s)=lambda·ds+s·d(lambda)`.
Consequently `DeltaPhi = integral lambda·ds`; it is generally **not**
`W_s - Delta psi` when `W_s=integral lambda·ds`.

**Concrete falsifier.** `psi(lambda)=lambda²/2`, `Phi(s)=s²/2`,
`s=lambda=t` from 0 to 1: `DeltaPhi=1/2`, `W_s=1/2`,
`Delta psi=1/2`; purported identity `1/2=0` is false.

**Actual primary locations.**
- `SRC-0119` PDF physical p.2, §3.5, on-manifold time identity states
  `dPhi/dt=lambda·dot(s)-dpsi/dt`: false under stated dual pairing.
  The same PDF p.5 §6.18 / p.6 §7.16 repeats the budget rule.
- `SRC-0118` PDF p.6, §4.13 repeats `DeltaPhi=W_s-Delta psi-Gamma_loss`
  without defining independently measured quantities and a calibrated balance law
  sufficient to make it true; not a convex-duality identity.
- `SRC-0229` PDF p.54, equations (15.17)–(15.18) reproduce
  `DeltaPhi=W_s-Delta psi` as a runtime reconciliation gate.

**Retained.** Fenchel–Young gap `>=0` is true, convex duality remains useful
as an operational consistency test. `Gamma_loss` can be a separately calibrated
dissipation observable, never inferred merely by rearranging a false identity.

**Linked Atlas / older Witness:** RA-M06, RA-R05, RA-E15; W198, W257–259, W350;
PF07. Relationship: shared lemma and traced propagation, not four independent theorems.

## L45-02 — Discrete structural work is not an exact endpoint potential increment

**Premises.** Differentiable convex `Phi`, at each tick `lambda_k=grad Phi(s_k)`.
Let `Delta s_k=s_{k+1}-s_k`, `W_left=sum lambda_k·Delta s_k`.

**Exact derivation.**
`Phi(s_{k+1})-Phi(s_k) = lambda_k·Delta s_k +
D_Phi(s_{k+1}||s_k)`.
Hence `Delta Phi_total - W_left = sum D_Phi(s_{k+1}||s_k) >= 0`.
For `Phi(s)=s²/2`, one tick 0→1, the left-endpoint work is 0
and the endpoint potential increase is 1/2.

**Consequence.** `SRC-0229` pp.53–54 computes `Delta W_s(k)=lambda_k·Delta s_k`;
even a repaired budget using `DeltaPhi=W_s` requires a quadrature correction
or an integral definition. A positive difference here is not automatically physical
"dissipation", dishonesty or a faulty agent trace.

**Linked:** RA-E15, RA-M06, PF07; W350.

## L45-03 — Supremum over baselines breaks robust conjugacy

**Actual original:** `SRC-0119` PDF p.5, §7.2–7.4:
`Phi_rob(s)=sup_{q in Q} Phi_q(s)` and
`psi_rob(lambda)=sup_{q in Q} psi_q(lambda)`; uses their sum in a robust gap
and in subsequent budget/metric gates (p.6).

**Countermodel:** `Q={Bernoulli(0.2), Bernoulli(0.8)}`,
`phi(x)=x`, `s=0.2`, `lambda=0`.
`psi_rob(0)=0`;
`Phi_rob(0.2)=max{0,KL(Bern(0.2)||Bern(0.8))}`
`=0.6 ln 4 = 0.8317766167`.
Yet `s=0.2` is in the subgradient of `psi_rob` at 0; indeed,
`psi_rob*(0.2)=0`, not `Phi_rob(0.2)`.
Thus **sup Φ and sup ψ are not generally Fenchel conjugates**,
and `G_rob=0` is not equivalent to alignment to some admissible baseline.

**Boundary:** if each `Phi_q=psi_q*`, then
`Phi_rob+psi_rob-lambda·s >=0` is still true: choose any same `q`,
apply Fenchel–Young and take suprema. The robust positive gap can be
used as a conservative *mismatch score* if that is the declared purpose.
It cannot silently inherit gradient reciprocity, inverse Fisher Hessian,
or the exact dual ledger. A proper alternative is to declare a single
effective `psi_rob` and use `psi_rob*`, or retain q-labelled paired ledgers;
these are different model choices with different semantics.

**Linked:** RA-M06/RA-R05; add a NEW dependency limit, not a new scientific finding.

## L45-04 — Δ5 projector normalization

**Actual original:** `SRC-0108` PDF physical p.3 §2.2 declares
the standard 10-component norm `||a||²=sum_{n=1}^{10}|a_n|²`;
p.8 §5.1 states `E_pair=sum_{n=1}^5 |a_n+a_{n+5}|²` and
`E_pair=||P_+a||²`, with `P_+=(I+T5)/2`.

**Correct identity:**
`||P_+ a||² = (1/2) sum_{n=1}^5 |a_n+a_{n+5}|²`;
therefore `E_pair=2||P_+a||²`, not `||P_+a||²`.
Sample `a=(1,0,...,0)` gives `1` versus `1/2`.

**Retained:** minimizers of the unconstrained/nonzero-normalized problem
remain `ker P_+` because the incorrect factor is strictly positive.

**Linked:** RA-R09, RA-H04; PF10, W17–20. A numerical coefficient correction
is not a proof that HeTu dynamics emerge in a natural system.

## L45-05 — Δ5 phase-lock quantifier is conditional

**Actual original:** `SRC-0108` pp.8–9 §5.2–5.3 treats both fixed
magnitudes and freely adjustable magnitudes, but Theorem 5.1 asserts that
every minimizing phase difference is π **equivalently** `a_{n+5}=-a_n`.

**Distinguish cases.**
- Fixed `r_n,r_{n+5} > 0`: phase minimum is π; when unequal,
  `a_{n+5}=-a_n` does not follow. For magnitudes 1 and 2,
  `(a_n,a_{n+5})=(1,-2)` minimizes phase cost but not vector equality.
- If either radius is zero: phase difference is undefined/irrelevant.
- Free amplitudes with fixed positive total norm `||a||²=C`: zero energy
  is attainable in `ker P_+`, where `a_{n+5}=-a_n`; zeros may still
  occur in individual pairs, for which phase is undefined.

**Repaired theorem:** state phase minimization given positive fixed magnitudes
separately from nullspace characterization of global vector minimizers.

## L45-06 — Signed link density is not automatically an energy penalty

**Actual original:** `SRC-0274` PDF p.2 §2.1 allows `L_{ij,f} in Z
(or a real density)` and §2.2 uses `E_link=beta sum L_{ij,f}`, `beta>0`,
calling this a "linking / twist cost".

**Counterexample:** with one unconstrained signed link `L=-N`,
`E_link=-beta N→-infinity`. The term is not nonnegative or bounded below
as a stand-alone penalty; no norm, admissible lower bound or stabilizing term
is supplied by that displayed expression.

**Repair options:** `beta sum |L|`, `beta sum L²`, restrict `L>=0`,
or document topology-constrained signed `L` plus a dominating coercive
regularizer. Each option changes chirality/sign predictions and must
be restated before simulations.

The same source's `1-cos(theta_i-theta_j)` (or face-matched
difference) is invariant to a *common* phase shift, but is not a
locally `U(1)`-gauge-invariant link by itself. A local version needs
a connection `A_ij` and a declared rule
`theta_i→theta_i+alpha_i, A_ij→A_ij+alpha_i-alpha_j`.
Spin/Pauli/4π claims additionally require representation, exchange
operator and actual empirical tests; the link repair does not supply those.

**Linked:** RA-M08, RA-H07, RA-M10, RA-R02; PF06, W236–238 / W224–228.

## Scope of this audit

All six local reconstructions are bounded **mathematical checks** on
identified formulae, with a directly executable finite counterexample where
applicable. They are **not** six validated SMFT hypotheses.
The audits do not imply entire PDFs were read: page numbers are physical PDF pages
counted from 1, and `fitz` text extraction was supplemented with page-image
inspection for `SRC-0108` p.8 and `SRC-0274` p.2.
Holdout reconstruction not executed. W024 remains unresolved.


---

# Imported original audit: `PROOF_DEPENDENCY_RECONSTRUCTION_v4.6.md`

**Source audit SHA256:** `681e6dbd46548ffaaa0f7ff48b2677f2d30facd3348dd87d26b88b6a20495159`. Original record, no silent proof strengthening.

# v4.6 Source-Anchored Mathematical Dependency Reconstruction — Port versus Robust Ledger

Date: 2026-10-15. Every `L46-*` is a **local conditional lemma / audit node**, not a newly claimed historical Witness, a scientific discovery, or an additional Proof Family. Four original PDF members are SHA-matched to the immutable 325-entry Source Manifest. Physical page numbers count from one.

## L46-01 — Robust maximum of log-partitions need not be differentiable

**Source statement:** `SRC-0119` p.5 §7.2–7.4 and §7.10 prescribe `ψ_rob(λ)=sup_{q'∈U} ψ_{q'}(λ)` followed by `I_rob=∇²ψ_rob` and `M_rob=∇²Φ_rob=I_rob⁻¹`. `L45-03` already showed independent supremum envelopes need not be a conjugate pair.

**Countermodel:** For binary `X∈{0,1}`, with `φ(X)=X`, choose the **actual KL-divergence ball** around `q_ref=Bernoulli(0.5)` with radius `ρ=KL(Bernoulli(0.2)||Bernoulli(0.5))≈0.1927447570`. In this binary case the admitted baselines are exactly `q(X=1)∈[0.2,0.8]`. In particular the two endpoints have `q₁(X=1)=0.2` and `q₂(X=1)=0.8`. Write

`ψ_q(λ)=log(1−q+q exp λ)`, `ψ_rob(λ)=max{ψ_0.2(λ),ψ_0.8(λ)}`.

At `λ=0`, the two branches meet, both having value zero; their slopes are respectively `0.2` and `0.8`. For `λ<0`, the lower-q branch dominates, and for `λ>0` the higher-q branch dominates. Thus the **left and right derivatives at zero differ**, `∂_-ψ_rob(0)=0.2`, `∂_+ψ_rob(0)=0.8`; the classical Hessian is not defined there. A scalar `I_rob(0)` and its inverse cannot simply be evaluated as written. The subdifferential `[0.2,0.8]` is meaningful but not a Fisher covariance of one selected baseline.

**Quantifier guard:** this countermodel uses a *specific* positive-radius KL ball; for `ρ=0` there is only the fixed baseline and the partition function can be smooth. At `λ=0` the entire ball ties in value, while the extremal baselines have different derivatives, proving nonsmoothness here. Thus it refutes the **unconditional smooth-Hessian inference** from the source definitions, not every possible smooth regularized robust construction.

**Repair:** fixed baseline; or explicit differentiable selection/unique active `q'(λ)` with regularity; or generalized subgradient and nonsmooth control gates. No natural-life health or AI validation follows. `PF07` shared convex-analytic premise; RA-M06, RA-R05.

## L46-02 — Exact importance sampling cannot be silently combined with weight clipping

**Source:** `SRC-0119` p.5 §7.8–7.9 first asserts `E_q'[g]=E_q[wg]` for `w=q'/q`, then instructs `E_q[w]=1` and clipping `w∈[0,w_max]` while using the same exact reweighting interpretation.

**Premises:** `q'≪q`; unclipped Radon–Nikodym ratio provides the exact identity. Let `q=Bernoulli(0.2)`, `q'=Bernoulli(0.8)`. Raw weights are `w(1)=4`, `w(0)=1/4`, with `E_q[w]=1`. Clip to `w_max=2`: `w_c(1)=2`, `w_c(0)=1/4`, hence `E_q[w_c]=0.6≠1`, and for `g(X)=X`, `E_q[w_cX]=0.4` whereas `E_q'[X]=0.8`.

**Consequence:** clipping changes the target and the exact identity fails. Renormalization can restore total mass but generally changes the target again; in this example the renormalized indicator expectation is `2/3`, not `0.8`, and the rescaled weight at `X=1` exceeds the stated cap. Any clipped/reweighted drift gate needs a stated bias/tail correction; do not advertise exact equality under capped weights. `PF07` / measurement contract.

## L46-03 — A moving reference baseline contributes its own potential drift

**Source:** `SRC-0119` p.6 §7.13–7.16 changes `q_ref` through EMA yet retains a work ledger without a baseline-change term. v4.5 already showed `ΔΦ=W_s−Δψ` is not a conjugacy identity even at fixed `q`.

For binary distributions, `Φ_q(s)=KL(Bern(s)||Bern(q))` and its differential is

`dΦ_q(s)=λ_q(s) ds + [(q−s)/(q(1−q))]dq`, with `λ_q(s)=log[s/(1−s)]−log[q/(1−q)]`, for interior `s,q∈(0,1)`.

Fix `s=0.5` and move `q:0.2→0.3`: `ds=0`, so `∫λ ds=0`, yet `Φ_0.2(0.5)≈0.2231435513` and `Φ_0.3(0.5)≈0.0871766936`. Thus a baseline-move correction is required even after the v4.5 fixed-baseline derivative repair. For robust active sets, extra branch-switching or nonsmooth terms may arise. No claim is made that this is a measured physical entropy flow.

## L46-04 — Exact joint functional port closure is conditional factorization

**Primary:** `SRC-0259` p.218 Theorem 5.1/eqs (5.1)–(5.10); corroborating summary `SRC-0261` pp.5–6 eqs (4.3)–(4.9). Legacy compiler W41/W154/W272 and `PF01/PF03` share but are not identical observer scopes.

Let finite internal space `S`, external state `B`, admissible input `U`, `F:S×B×U→S`, `G:S×B×U→B`, `H:S×B×U→Y`, and `π:S→P=π(S)`. Assume the full product of arguments is admissible, or **declare** the admissible triple set with a common `(p,b,u)` support and valid successor closure.

There are reduced functions `F̄:P×B×U→P`, `Ḡ:P×B×U→B`, `H̄:P×B×U→Y` agreeing with the full system **iff** all three original maps `π∘F`, `G`, `H` are constant over each `π` fiber for fixed `(b,u)`. Necessity follows because a function of one reduced tuple cannot yield two values; sufficiency follows by defining each reduced map from any valid representative `s` in a fiber, whose value is independent of that choice.

**What it proves:** conditional, deterministic, task/protocol-relative *state factorization*. **What it does not prove:** correctness against external task truth, natural modularity, emergent attractors, neural mechanism, general stochastic lumpability, or scientific originality of the elementary factorization theorem.

## L46-05 — Protocol extension can destroy a previously valid port

**Primary:** `SRC-0261` p.10 §5 S3; `SRC-0260` pp.7–9 §6–7 and `SRC-0259` p.263 finite-audit boundary.

Explicit finite countermodel: `S={(p,h):p,h∈{0,1}}`, `B={0,1}`, `π(p,h)=p`. Define `F((p,h),b,u)=(p,h)`, `H((p,h),b,u)=p`, `G((p,h),b,u)=p` when `u=0`, and `G((p,h),b,u)=h` when `u=1`. For protocol `U₁={0}`, all three fiber consistency conditions hold, so `(p,b)` is a sufficient reduced state. Extend to `U₂={0,1}`: states `(0,0)` and `(0,1)` have the same port but `G(...,u=1)` differs, so there can be no exact joint reduced model on `p,b`.

If `U₁⊆U₂` and the **state/support domain is held fixed**, exact `U₂` closure implies `U₁` closure, not conversely. Expanding **also** the admissible state set or changing model parameters makes a separate versioned contract; do not claim monotonicity without the fixed-domain guard. `PF01/PF03`, RA-M01, RA-M11, RA-E14, RA-O02.

## L46-06 — Instantaneous output sufficiency is not a Markov state quotient

**Primary:** `SRC-0259` pp.190,217,231 describes output-only versus strong state closure, and `SRC-0261` pp.6,9 differentiates them.

Countermodel: `S={(p,h):p,h∈{0,1}}`, `π(p,h)=p`, output `y=p`, transition `F(p,h)=(h,h)`. Two states `(0,0)` and `(0,1)` yield identical current output zero, but next projected state is respectively zero or one. Thus `y=H̄(π(s))` exists but a deterministic `π∘F=F̄∘π` does not. Do not confuse **current output sufficiency** with **all-horizon behavioral sufficiency**. In fact, for all outputs identically zero, every state is behaviorally equivalent even if a chosen noncanonical port fails state closure (the source's other example in `SRC-0259` p.190).

This gives separate `DERIVES` and `NON_ENTAILMENT` edges; use typed assumptions instead of grouping both under “Port proof”. `PF01/PF13`.

## L46-07 — Observational fit cannot identify the off-support causal path

**Primary:** `SRC-0261` pp.7–8 M6–M9 and `SRC-0259` pp.263–264 / p.303. Fix a training distribution supported only on `p=h` with `p,h∈{−1,+1}` and target `y*=p`.

Two mechanisms `M_A:y=p` and `M_B:y=h` agree on every observed pair and can both achieve zero natural observational error. Under a **declared admissible counterfactual** holding `p=1` and setting `h=−1`, their outputs are `1` and `−1`. Therefore no observational-only procedure can distinguish them from these data. A counterfactual or further structural constraint is necessary to identify which channel is actually used. If such a transplant is off-manifold and not admissible, its result is not evidence of a naturally accessible intervention; record that restriction explicitly.

The source's 2-channel Hessian / `R_obs=v²(1−ρ²)` calculation assumes centered, unit-variance channels and squared-error loss; the worst-case `|v|` requires the declared symmetric admissible `h∈[−1,1]` fiber and absolute loss. These are **necessary quantifier guards**, not universal Transformer equations. `PF03/PF08`, RA-M11/RA-H02.

## L46-08 — Natural individual and attractor advantage remain separate open obligations

**Primary source distinctions:** `SRC-0261` pp.9,14–20,22–26,28–31: M12 says neither arbitrary correct computation nor irrelevant stable attraction implies the other; M1–M6 synthetic model controls; open O1/O3/O5/O9/O11; four retained hypotheses H1–H4. `SRC-0259` pp.373–375,420–423,444 distinguishes functional wrapper, endogenous causal module, natural functional individual, and attractor-mediated individual.

**Explicit null pair:** Let a system have two independent components. Register `a_{t+1}=0` is a genuine globally attracting subsystem; output `y_t=x_t` is computed by a separate feed-forward wire and is independent of `a`. The attractor is real, but intervening on it does not affect the function. Conversely an XOR feed-forward gate performs a function without needing an iterative contracting state. This is not a new proof of general brain architecture: it is a negative control refuting the logical implications.

**Nontrivial hypothesis to preserve (no promotion):** H1 learning-driven port qualification; H2 developmental individuation; H3 endogenous causal organization; H4 attractor-specific advantage. Evidence needed: known-circuit positive/negative controls, invariance to invertible representational mixes, declared admissible interventions, checkpoint histories, matched non-attractor controls, causal removal/restore experiments, and functional reuse tests. These hypotheses remain separate and generatively important even where source math is basic existing theory. No neural/LLM trial executed in this v4.6 Kernelization.

## Typed dependency relation matrix (first executable DAG segment)

| General lemma | Assumptions / type | Result | Witness / source | Residual and forbidden inference |
|---|---|---|---|---|
| L46-01 nonsmooth supremum | multiple active baselines / parameter derivatives | Hessian may fail | SRC-0119 p.5; prior L45-03, PF07 | smooth robust Fisher *needs extra hypotheses* |
| L46-02 exact change-of-measure | absolute continuity, unmodified `q'/q` | exact expectations; clipping breaks | SRC-0119 p.5, PF07 | clipping bias uncalibrated |
| L46-03 moving-potential chain rule | baseline `q(t)` varies | `∂qΦ dq` required | SRC-0119 pp.5–6; RA-R05 | physical heat/entropy not inferred |
| L46-04 quotient factorization | fixed S,B,U / all admissible fibers | joint state/output closure iff 3 congruences | SRC-0259 p.218, SRC-0261 p.6; PF01/PF03 | not a natural individual |
| L46-05 protocol restriction | fixed S and model, `U₁⊆U₂` | expanded protocol may invalidate | SRC-0261 p.10; PF03 | avoid model-version conflation |
| L46-06 output vs Markov | specified map `π` | output congruence alone not future state closure | SRC-0259 pp.190,217; PF01/PF13 | all-horizon behavior differs |
| L46-07 observational aliasing | p=h support; admissible do(h) | observational equivalence ≠ causal identification | SRC-0261 pp.7–8; PF08 | avoid off-manifold interventions without guard |
| L46-08 attraction not functional cause | disconnected attracting variable | attractive ≠ used function | SRC-0261 pp.18–24; PF03 | H1–H4 pending neural mechanism tests |

**Historical provenance and evidence boundary.** `SRC-0259` is a 446-page longitudinal anthology, `SRC-0260` 433 pages, `SRC-0261` 34 pages. Only recorded pages have been read this round; text extraction of all pages is **not** page-by-page verification. None of L46-01..08 is a new physical or AI capability claim. W024 is not located or filled. No clean-room independent LLM reconstruction trial has been run.


---

# Imported original audit: `PROOF_DEPENDENCY_RECONSTRUCTION_v4.7.md`

**Source audit SHA256:** `88681ae23e6b56dd8da0462abe5fd96fc22f856e8b2c97eabd1010b891051ace`. Original record, no silent proof strengthening.

# v4.7 Source-anchored Conditional Dependencies — Training-Time Port Identity and Epistemic Boundaries

**Scope:** New local audit IDs `L47-01..08` (not historical W, GM, PF or scientific proofs). 2026-10-15. Source hashes, exact locators and review depth in `SOURCE_IDENTITY_CHECK_v4.7.json` and `SOURCE_DEPTH_AUDIT_v4.7.csv`. **No independently trained neural models and no independent LLM reconstruction benchmark.**

## L47-01 — Cross-checkpoint Port transport exists iff the change map saturates old fibers

**General lemma.** Let `S0,S1` be sets, `pi0:S0→P0=pi0(S0)` and `pi1:S1→P1=pi1(S1)` surjections onto their images, and `L:S0→S1` a **declared** state correspondence or learning-change map. A deterministic map `R:P0→P1` making `pi1 ∘ L = R ∘ pi0` exists **iff**

`pi0(x)=pi0(y) ⇒ pi1(L(x))=pi1(L(y))` for all admitted `x,y∈S0`.

**Proof:** Necessity follows by applying `R`. Sufficiency: set `R(p)=pi1(L(x))` for any `x` with `pi0(x)=p`; the condition proves well-definedness. Surjectivity of `pi0` onto `P0` gives uniqueness of `R` **for that chosen L and fixed maps**. No `L` is supplied merely by a pair of independent model checkpoints. If L is stochastic, replace deterministic equality with a distributional kernel compatibility condition; if model states are only reachable on selected supports, make the quantifier support explicit.

**Primary motivation, not claim that this lemma was proven there:** `SRC-0261` pp.15–16, O5–O6, asks how identity persists across checkpoint-specific activation coordinates and warns against cluster counts. `SRC-0283` pp.9–11 gives the within-model congruence construction. `SRC-0259` pp.435,437,439 requires fair developmental tracking but does not establish a cross-checkpoint transport theorem.

**Graph:** general quotient-factorization lemma → fixed state correspondence and fibre congruence → valid cross-checkpoint Port map → `SRC-0261` checkpoint proposal → residual `IDENTITY-TRANSPORT-UNMEASURED`. PF01/PF03; RA-M01, RA-H02, RA-O02.

## L47-02 — Two valid Ports and preserved task outputs do not suffice for Port transport

**Countermodel:** `S0=S1={(p,h):p,h∈{0,1}}`; both checkpoint dynamics are identity and **both** output the first bit `y=p`, so all tasks and all future readouts coincide. Choose `pi0(p,h)=p`; choose `pi1(p,h)=(p,h)` and let `L=id`. Each projection supports its own exact reduced dynamics and output. However `pi0(0,0)=pi0(0,1)=0`, while `pi1(L(0,0))=(0,0) ≠ (0,1)=pi1(L(0,1))`. No deterministic `R` can make the diagram commute. This counterexample uses a **nonminimal** later Port; it is *not* a refutation of a separately anchored, minimal-behaviour-quotient transport theorem.

**Conclusion:** `PORT_SUFFICIENT(t0) ∧ PORT_SUFFICIENT(t1)` and even unchanged task output is **insufficient** to assert same identity, canonical birth, or unique maturation trajectory without linking constraints. Stronger positive conditions should include common intervention/observation contract and an identified state relation. PF01/PF03; RA-M01/RA-H02/RA-O02.

## L47-03 — Activation coordinates are not a canonical identity metric

**Positive conjugacy witness:** `S={0,1}`, `F0=F1=id`, `pi0(s)=s`, `pi1(s)=1−s`. Their reduced dynamics are both identity. Outputs are `o0(p)=p` and `o1(q)=1−q`. Define `R(p)=1−p`: then `pi1=R∘pi0`, `R∘Fbar0=Fbar1∘R`, and the full task output is identical under the adapter. Yet the naive Euclidean/raw-bit difference `|pi1(s)−pi0(s)|` is `1` for **every** s. Hence raw activation/cluster change may report an apparent complete identity turnover in a perfectly conjugate system.

**Limitation:** A chosen invertible `R` proves one functional equivalence, not a unique anatomical/causal localization. For real Transformer hidden states an actual cross-model alignment or interventional isomorphism is required; matching neurons, bases or embedding coordinates by index is not enough. See `SRC-0261` pp.15–16,19–21 and `SRC-0259` p.435 (M2 invertibly mixed representation). RA-E14/RA-O02.

## L47-04 — Apparent 'birth' is not established by endpoint discovery or training-fit Port scores

**Exact limitation:** For *every* checkpoint with a well-defined system state, `pi_k=id` is an exact Port if there is an output map and state transition. Existence of a fitted exact Port at `k1` therefore does not by itself distinguish new function formation from trivial identity-preserving bookkeeping. For nested representation classes, the globally best achievable in-sample residual cannot increase, and can decrease purely by overfitting; an observed threshold crossing is not a bifurcation theorem.

**Required experiment:** Freeze discovery/holdout interventions separately; compare pretraining checkpoints and ablate the learned causal routes, with stable task and resource contracts. Test a decodable-but-unused negative control M4, and a changing-coordinate M2, before interpreting lower Port residual as endogenous formation. Training-time causal intervention is needed to claim that the change *caused* formation.

**Original:** `SRC-0261` pp.15–16 O5–O6, pp.20–25 M1–M6/stages/stop rules; `SRC-0259` pp.435–439. PF03/PF08; RA-E14/RA-H02/RA-R08. Open: timestamped developmental causality and genuine mechanistic birth vs retrospective discovery.

## L47-05 — Mind-Seal declared similarity is not a universal operational-sufficiency theorem

**Original claim:** `SRC-0241` p.3 §0.4 calls compact `(ζ,π)` descriptions sufficient for 'manifold-level coherence'; p.17 §5.3 again describes sufficiency for coordination/verification. That same source pp.2–3 explicitly says its 'field/topology/gradient' vocabulary is a *lens*, not differentiable dynamical structure or privileged access to hidden states.

**Simple countermodel:** Two recipient agents receive **identical** seal `z=(ζ,π)` with policy 'release only after external signed approval'. In the same admissible environment with no approval, agent A blocks release; agent B ignores the text and releases. Same seal, different action and trace; no universal `action=H(seal,environment)` exists for the unrestricted recipient class. If authorization is enforced by a protected external runtime and task observation/interventions are fixed, one can instead test a scoped behavioral equivalence / Port qualification, which is an **engineering hypothesis** and not guaranteed by seal serialization.

**Typed repair:** Add recipient/runtime state and a task-specific authorized intervention contract to the input state; require agreement on observed actions, next effective state and trace over admitted tests. Distinguish 'prompt describing an invariant' from 'enforcement ensuring it'. PF03/PF11/PF13; RA-E11, RA-R07 and RA-R10. No statement about model subjective identity or actual physical manifold.

## L47-06 — Genesis chronology is not proof-dependency chronology

**Direct DOCX original:** `SRC-0323` original DOCX ¶851 describes selecting a perspective to determine the '天地' stage; ¶872–878 explicitly says that the same people/events/environment can have different interactions under different chosen perspectives, and recommends fixing one viewpoint before switching. These are **historical/conceptual** origins of perspective-relative modelling. They are not a formal quotient-state theorem: no `S,U,F,o,pi` and no equality under all admissible future interventions is established in those paragraphs.

**Later formalization:** `SRC-0283` pp.3–4 makes a boundary/projection `(B,Π)` explicit; pp.8–11 defines behavioral equivalence and proves quotient/fiber congruence, relative to declared protocol. Record a genealogy edge `GENESIS_ORIGIN` / `ENABLES`, a weaker role correspondence `TRANSLATES`, and an independent mathematical lemma `DERIVES` inside the later declared model **only**. Do not infer original publication date, discovery priority or external novelty from the DOCX creation metadata or tar mtime alone. PF09 / RA-H05, GM-001. Preserves creativity without retroactively attributing precise mathematics.

## L47-07 — Complete the exact behavioral quotient theorem with a right-congruence proof

**Source:** `SRC-0283` pp.8–10, equations (4.1)–(4.13): `x~y` iff every finite admitted intervention word `w`, including empty word, satisfies `o(F_w x)=o(F_w y)`. The source shows that every sufficient quotient refines this relation. To explicitly complete the other direction, if `x~y`, then for each admitted input `u` and word `w`, `o(F_w(F_u x))=o(F_w(F_u y))` by applying equivalence to the concatenated finite word `(u,w)`. Therefore `F_u x ~ F_u y`, yielding induced transitions on the equivalence classes. The empty word also guarantees observation congruence. Together they show the canonical behavioral quotient itself is sufficient under the **fixed global intervention alphabet and total deterministic dynamics** assumptions.

**Boundary:** If admissible inputs depend on state, require matched availability and partial-transition logic. The source later warns (pp.15–16) that approximate `ε`-similarity is not transitive, so one cannot use an arbitrary tolerance relation as an exact quotient. This complete short proof is *mathematical source reconstruction*, not new SMFT discovery. PF01; RA-M01.

## L47-08 — Identify attraction-mediated function by intervening on the causal path

**Source:** `SRC-0261` pp.17–19 O11/O16, pp.20–26 M4–M6 and stop rule E; `SRC-0259` pp.437–440 separates causal path, stable basins, recovery and endogenous organization.

**Negative control:** Hidden system has task bit `p` and auxiliary `a`; `p_{t+1}=p_t`, `a_{t+1}=0`, output `y=p`. The `a` component is a genuine one-step globally attracting fixed point, but interventions `do(a=0/1)` cannot alter output. Claim 'attractor-mediated task' is false. Conversely a fixed task-using structural decoder need not have a state attractor. Positive evidence needs a declared execution clock, an actual attractive invariant set, ablations isolating that path, error/recovery improvement against resource-matched alternatives, and stability under admissible interventions. This is a test contract, **not a reported real neural model experiment**. PF03/PF10; RA-E14/RA-R08/RA-H02.

## Global evidence firewall

Five original sources SHA-matched: `SRC-0323` DOCX and `SRC-0283`, `SRC-0241`, `SRC-0259`, `SRC-0261` PDF. Two sources have long historical bodies and remain *bounded-page read*, not complete. No new W401, PF, GM or RA. Do not equate `L47-01..08` with independent scientific results. W024 still reserved/unverified. No clean-room independent LLM reconstruction or true natural Transformer causality evaluation was performed.


---

# Imported original audit: `PROOF_DEPENDENCY_RECONSTRUCTION_v4.8.md`

**Source audit SHA256:** `15dac4d68983be30449f06b969fd5524dce555fb794d0c320323313f374a70d5`. Original record, no silent proof strengthening.

# v4.8 K0–Genesis / P8D II: Source-anchored Typed Proof Reconstruction

**Date:** 2026-10-15. Nodes `L48-01`–`L48-06` are **new audit dependency IDs**, NOT historic author Witness, PF, GM, or new physical/scientific theorems. Exact primary-source member hashes and reading scopes: `SOURCE_IDENTITY_CHECK_v4.8.json`, `SOURCE_DEPTH_AUDIT_v4.8.csv`. Source PDF page indices are physical, 1-based. Mathematical counterexamples are constructed by the compiler and **not attributed to the historical author**. No independent LLM test or real-world efficacy result is claimed.

## L48-01 — The canonical Kan–Li role is not the older Memory–Focus implementation

**Primary source claim & version change.** `SRC-0106` PDF pp.7–9 (§2.2–2.5), pp.19–26 (§4.8 and §5.1–5.12) explicitly distinguishes the earlier engineering mapping `Kan–Li → Memory–Focus` from the revised canonical `Kan–Li → Realization–Admissibility`. In its equations (5.1)–(5.3), Memory–Focus is a possible implementation projection, whereas Li is a predicate `ℒ_t(x,a,x')∈{0,1}`, and Kan constructs paths from a goal, present state, admissibility rules, trace, and residual (`§5.5`). Memory may *help implement* the path constructor and focus may *help select* active rules. Neither is definitionally equal to the role. `SRC-0268` pp.1–3 is a 2025 semantic-field engineering extension with the older Memory–Focus language, not a superseding definition. `SRC-0323` DOCX ¶1140–1154 names policy/countermeasure interaction as a prior historical conceptual axis.

**Formal non-entailment.** Two systems can have identical stored histories `m`, attention weights `f`, available actions and visible state but different admissibility predicates `ℒ_A(x,a,x')=1` and `ℒ_B(x,a,x')=0`. A memory/focus-only representation cannot distinguish a valid from an invalid proposed act in this pair. Therefore `(memory,focus)` alone is not generally sufficient to recover an independent admissibility grammar.

**Corrected downstream canonical wording.** `RA-E01` previously ends its four-dyad list with `Memory–Focus`, inconsistent with the same package's already-correct K0 §3 and protected `41_K1_P8D_001` definitions. Revise **RA-E01 in L0 only** to say Realization–Admissibility canonical, Memory–Focus historically useful subimplementation. This is a source-verified *compiler repair*, not a new physical result. Do not change protected 41.

**Dependency:** `source revision: SRC-0323 → SRC-0268 → SRC-0106` (conceptual/implementation lineage, not theorem implication); `K0 §3`, `K1 41` → `RA-E01`; `GM-003/004` historically relevant. **Residual:** what minimal measurable variables operationalize ℒ and Kan in real agents/organizations? No evidence here that the four dyads are necessary or unique in nature.

## L48-02 — One throughput mediator does not force rank-one feedback when its reinjection depends on state

**Primary:** `SRC-0106` PDF p.34 (§7.7 eqs.7.42–7.43) already warns about state-dependent reinjection. Do not falsely claim the primary paper forgot this term; challenge compressed restatements that omit it.

**General lemma.** For differentiable `F(x)=F₀(x)+c(x)y(x)`, with scalar `y`, vector `c(x)∈ℝⁿ`, write `q=∇y`. Then

`DF = DF₀ + c qᵀ + y Dc`.

Only when `Dc=0` (or `y Dc` is controlled/rank-bounded and specifically included) can the closure correction be assumed rank≤1. For general `r` channel map `h:X→ℝʳ` with `F=F₀+Γ(h(x))` where Γ does **not** depend separately on `x`, `rank(DF−DF₀)≤r` by the chain rule. The factorization premise is indispensable.

**Counterexample (exact).** `x=(x₁,x₂)`, `y=x₁`, `c(x)=(1,x₂)`, `F₀=0`. Then `F(x)=(x₁,x₁x₂)`, and at `(1,1)`:

`DF = [[1,0],[1,1]]`, determinant `1`, rank `2` although the measured mediator `y` is scalar. The nominal `c qᵀ` alone has rank `1`; the omitted `y Dc` contributes the missing direction.

**Dependency:** `general multivariate chain/product rule → declared c(x),y(x) → conditional low-rank Jacobian claim → SRC-0106 p.34 → residual Δ_J measurement`. **Forbidden:** infer rank-one from the *count of named throughput signals* or from Proto-Eight's eight labels.

## L48-03 — Low-rank correction / small return operator does not imply an exact state quotient

**Primary:** `SRC-0106` PDF pp.35–39 (§§7.8–8.7), especially §8.5, explicitly says closure dimension and modal dimension differ; its return determinant is not a guarantee of low-dimensional dynamics. K0 §6 requires a task/intervention-preserving quotient.

**Countermodel.** Set `x=(x₁,x₂)`, `F₀(x)=(x₂,0)`, `c=(0,1)ᵀ`, `y=x₁`, so `F(x)=(x₂,x₁)` and `DF−DF₀ = [[0,0],[1,0]]` has rank 1. The natural mediator coordinate is `π(x)=y=x₁`. Pick `x=(0,0)` and `x'=(0,1)`: both share the same π but `dπ/dt` is 0 and 1 respectively. No autonomous dynamics on **this proposed π** can exactly reproduce both projected flows. This does not claim *no other* quotient can ever exist.

**Required independent theorem.** For an exact deterministic quotient, `π(s)=π(t)` must imply matching projected outputs and transition dynamics for every admitted control/intervention; equivalently `π∘F_u = \bar F_u∘π` in discrete time (or tangent map condition in continuous time), with all domains and measurement protocols typed.

**Dependency:** `rank correction ≤1` **does not derive** `exact lumpability`; `RA-M01`, `RA-R04`, `RA-E01`. **Residual:** protocol-scoped outputs, interventions and held-out validation for real P8D reductions.

## L48-04 — The closure residual is baseline-relative and may be undefined

**Primary source:** `SRC-0106` PDF pp.34–35 eqs. (7.43)–(7.49) defines `J=J₀+UVᵀ+Δ_J` and `ε_cl=||Δ_J||/||J−J₀||`. The source correctly calls its small residual hypothesis falsifiable. The following is an additional compiler guard on using the formula as evidence.

**Exact boundary failure.** When `J=J₀`, both numerator and denominator can be zero; `ε_cl=0/0` is undefined, not proof of perfect low-rank fit. Introduce a *declared* zero-denominator handling rule and report the raw absolute residual.

**Non-identifiability without a fixed baseline.** For the same observed `J=diag(1,2)`:
- Choose `J₀=diag(0,2)`, `U=V=(1,0)ᵀ`, `Δ_J=0`: rank-1 claimed closure and `ε_cl=0`.
- Choose `J₀=J`, `U=0`, `Δ_J=0`: no closure and `ε_cl=0/0`.
- Choose `J₀=0`, the same `U,V`, `Δ_J=diag(0,2)`: `ε_cl=2/sqrt(5)` in Frobenius norm.

Thus rank and residual depend on the *declared baseline*, fit constraints and norm; they are not unique intrinsic fingerprints of the system. Pre-register `J₀`, admissible factorization, weighting/norm, fit and evaluation data split; include nonlow-rank and shuffled-channel negative controls.

**Dependency:** `observed Jacobian + approved baseline + fitted low-rank pair + holdout residual → evaluable model`, not `J → canonical low-rank natural mode`. **Residual:** calibrate across domains and held-out interventions.

## L48-05 — Return-operator determinant identity is spectral bookkeeping, not a one-mode system

**Primary:** `SRC-0106` PDF pp.36–38 eqs. (8.1)–(8.14) derives the standard matrix determinant lemma under `ζI−J₀` invertibility:

`det(ζI−(J₀+UVᵀ))=det(ζI−J₀) det(I−Vᵀ(ζI−J₀)⁻¹U)`.

**Counterexample to overreading.** Let `J₀=diag(0,2)`, `U=V=e₁`; then `J=diag(1,2)`, return function `R(ζ)=1/ζ`, and `1−R(ζ)=0` captures feedback-shifted eigenvalue `1`, while `2` is still an eigenvalue inherited from the baseline. The return operator being 1×1 does NOT make the full dynamics one-dimensional. At baseline poles the rational factors must be handled by polynomial identity/analytic continuation or direct characteristic determinant; cancelling singular expressions blindly is forbidden.

**Dependency:** matrix determinant lemma + resolvent domain → feedback spectral relation → *optional further* exact reduced-model validation. **Residual:** establish task observables, spectral regime, and actual engineering improvement independent of return-matrix compactness.

## L48-06 — K0/Genesis lineage requires revision-aware edge labels, not a theorem chain

**Reopened originals.** `SRC-0323` DOCX ¶1140–1154 positions the four ancient pairings as one proposed developmental sequence and policy/countermeasure control interpretation; `SRC-0105` PDF pp.1–4 is a concrete two-tank growth-throughput proposal with capacity, demand, fit, retention, enabling friction, buffer, and reinvestment; `SRC-0268` PDF pp.1–3 presents the earlier field/Memory–Focus extension; `SRC-0106` pp.7–9,19–26,34–39 explicitly reframes the earlier engineering mappings; `SRC-0283` PDF pp.3–9 supplies a later separate operational frame/quotient interpretation. The historical DOCX and P8D original do not contain the later full P8D II operator/quotient theorems.

**Typed lineage edges:** `SRC-0323 CONCEPTUAL_ANCESTOR_OF P8D research`, `SRC-0105 REFRAMED_BY SRC-0106`, `SRC-0268 IMPLEMENTATION_REVISED_BY SRC-0106` (specifically Kan–Li), `SRC-0106 TRANSLATES_TO later world-framing questions`, with **no automatic `DERIVES` claim** across documents. Never treat tar member mtime or an LLM-assisted later proof as sufficient evidence of independent priority or mathematical necessity. The exact strongest theorem depends on the assumptions in its formal statement, not on the prestige or chronology of the ancestor document.

**Dependency:** primary-source paragraph/page/editions + typed objects/quantifiers → chronology of ideas; separate `General Lemma → assumptions → result` where actual math exists. **Residual:** full lineage deep review, originality comparison with outside mathematics, and repeated-benchmark test of whether the Kernel supports reconstruction.

## Evidence and release boundary

The six L48 nodes form one coherent source-scoped proof/lineage *batch*, **not six proved SMFT laws**. Source `SRC-0105` has 4 PDF pages; all extractable pages checked and pp.1/4 rendered, but empirical validation, data calibration and originality review are not established. Other long documents were selectively reviewed only. Local finite unit tests are **not** source-hidden independent LLM benchmark results. `W024` is still unresolved and unmodified.


---

# Imported original audit: `PROOF_DEPENDENCY_RECONSTRUCTION_v4.9.md`

**Source audit SHA256:** `308fd79e49a0f2259160c84259fbfe2013698c1c7d27dc40be3f6a34bfd096fa`. Original record, no silent proof strengthening.

# v4.9 — K0 / Genesis / L0 Typed Cross-Source Mathematical Dependencies

**Version:** 2026-10-15, original-member SHA verified against `90_SOURCE_MANIFEST.csv`.
**Evidence:** bounded source-page/paragraph audit; no whole-corpus theorem certification or independent LLM blind trial. `L49-*` are audit nodes, **not** new historical Witness IDs, PFs or Generative Moves.

## L49-01 — Signed interaction graph matrix versus dynamical derivative orientation

**Primary original:** `SRC-0279`, PDF physical p.47 §84 productive direction `G → A → C → S → R → G`; p.57 §104 regulatory direction; p.75 eqs (141.1–141.4); p.88 App.C equations (C.3–C.4), visually inspected.

**Displayed source** places `+` at row `G`, column `A`, and `-` at row `G`, column `C`; by row-as-source convention they mean `G→A`, `G⊣C`. But its differential law is
`dot a_i=a_i [b_i + Σ_j W_{ij} a_j − φ_i(a_i)]`.
For this law the effect of **source j on target i** is `W_ij`. The source matrix's positive `G,A` entry therefore mathematically means `A→G`, not `G→A`. With `a_G=a_A=1`, other intensities zero, `b=φ=0`, the displayed matrix gives `dot a_G=1, dot a_A=0`, the reverse of the intended G→A link.

**Repair:** if rows encode source, columns encode target, write `Σ_j W_{ji} a_j`; alternatively transpose the given source matrix and keep `Σ_j W_{ij} a_j`. Fix sign convention for all links and then rerun controlled perturbation tests; do not simply use a visually correct signed cycle. **Status:** verifiable source equation/interface inconsistency; not rejection of the functional five-regime hypothesis.

**General lemma:** For differentiable positive a_i, the direct influence `∂(dot a_i)/∂a_j = a_i W_ij` for `j != i` when b_i, φ_i do not depend on a_j. Therefore orientation is mathematically observable with interventions if assumptions hold. **Atlas:** RA-E03; RA-H05 (historical relation only); PF10/conditional control.

## L49-02 — Normalized regime occupancy is not an invariant of the proposed law

**Primary:** `SRC-0279` p.52 eq (95.1), calls `Σ_q a_q=1` a crude normalization for regime intensities; pp.75,88 propose multiplicative dynamics.

If the intended a represents fractions on simplex, then `Σ dot a_i = Σ_i a_i [b_i+(Wa)_i−φ_i(a_i)]`, not zero by default. Countermodel: `W=0`, `φ=0`, every `b_i=1`, `Σ a_i(0)=1`, then `dot a_i=a_i` and `Σ a_i(t)=e^t`. A replicator correction `dot a_i=a_i(f_i(a)−Σ_j a_j f_j(a))` keeps `Σ a=1` when normalized initially; using unconstrained absolute intensities is a different admissible interpretation.

**Outcome:** normalization is an independently imposed coordinate convention or conservation condition, not a consequence of (C.4). Prevent interpreting raw unnormalized intensities as probability/occupancy without an enforced policy. **Status:** conditional proof obligation, source does not explicitly assert that (C.4) preserves simplex.

## L49-03 — K5 cycle decomposition is correct but is not a uniqueness theorem for five regimes

**Primary:** `SRC-0279` p.52–53 §96–97, pp.87–89 App.D: `K5=C5 ⊔ C5*` as UNDIRECTED edge-disjoint cycles. The original explicitly warns that this is **not** reverse proof that there must be five regimes.

**General algebra:** On vertex set `Z_7`, define undirected edge classes `E_s={{i,i+s} : i in Z_7}` for `s=1,2,3`, removing duplicate undirected pairs. Each `E_s` is a seven-cycle because gcd(s,7)=1. The classes have no shared edge and together cover all `7*6/2=21` edges of `K7`. Thus `K7=C7(1) ⊔ C7(2) ⊔ C7(3)`. So the property of complete-graph decomposition into edge-disjoint cycles is not exclusive to five, even though the TWO-cycle complement `K5\C5` is special within this comparison.

**Residual:** do controlled K=4,5,6,7 model selection with equal parameter budgets, regime reachability, switch costs and held-out performance. Cycle appearance or matching five Chinese names alone is not predictive evidence. **Atlas:** RA-E03; PF10; no empirical upgrade.

## L49-04 — Three non-equivalent quantities: developmental functions, operating regimes, governance maturity

**Genesis provenance:** `SRC-0323` DOCX ¶1927–1950 describes 根苗花果 as trends, business model, niche, promotion; `SRC-0309` DOCX ¶21–26/¶37–69 AND **four embedded tables** distinguish incubation (lower trigram, organizational roles) from adaptation (upper trigram, external clock). It includes table 2's original `Kan=Final/Overall Responses to Policy`, `Li=Formal & Informal Policy` and therefore preserves historic vocabulary rather than silently retro-writing `Realization–Admissibility` into a 2024 source.

**Later formalization:** `SRC-0279` p.20: `q in {G,A,C,S,R}` is a *mode* with hybrid state update, NOT five mandatory chronological life stages; pp.29–30 explicitly compare other K and characterize five as coarse-graining hypothesis; pp.56–57 compare to Wuxing **as cyclic topology resemblance**, not ancient physical/AI empirical evidence.

**Typed relation:** `SRC-0323 → SRC-0309` is historical/translation/refinement; these earlier four-function developmental roles do not logically DERIVE the five-regime hybrid controller; the eight trigram roles do not imply the five macro-modes; a mapping could be proposed only after declaring observables, state spaces, admissible transition and intervention-preservation tests. Modern synthetic controls do not validate claimed macroeconomic predictive accuracy. **Atlas:** RA-E02, RA-E03, RA-H05; PF09/PF10 separate domains.

## L49-05 — Protocol-relative Ξ monitoring is not automatically an exact quotient

**Primary:** `SRC-0130` pp.2–5 defines `Ξ=(ρ,γ,τ)` with boundary/probe compilation, pp.3–8 drift, four control channels and KL jump; pp.18,22 gate observer perturbation; p.29 explicitly rejects unique internal decomposition and global identifiability.

**Exact conditional lemma:** A deterministic effective next-state operator `F̄_u` on Ξ exists for all permitted u **iff** whenever `C(s)=C(s')`, `C(F_u(s))=C(F_u(s'))` (with aligned protocol and domain). Countermodel `S={(x,h):x,h∈{0,1}}`, `C(x,h)=(x,0,0)`, `F_u(x,h)=(x XOR h,h)`; rich states `(0,0)`, `(0,1)` have same Ξ but different next Ξ. Hence choosing three monitoring coordinates does not prove predictive sufficiency.

**Control nuance:** A 3×4 instantaneous input Jacobian is not injective as a map `u→dot Ξ` (has a nontrivial nullspace); nevertheless its columns *can be estimated* through separately randomized interventions across repetitions, so do **not** infer that four channels can never be identified. Separating an instrumented monitoring interface from a universal exact quotient is the correct boundary. **Atlas:** RA-E04; RA-M01; RA-R04; PF01/PF03.

## L49-06 — Maturation trace, source coverage and truth require different oracles

**Primary:** `SRC-0237` p.57–58 §7 defines segment-level coverage; p.83 §10.9 defines gated promotion; pp.105–106 §13 defines replayability (`recoverable_history/material_updates`) and promotion quality (`justified_promotions/total_promotions`), leaving 'justified' dependent on an adjudication procedure. The source itself explicitly distinguishes maturity governance from truth evidence.

**Countermodel:** Build two knowledge stores with the **same exact** review-event list, hash chain, coverage records, and promotion decisions, but assign different actual truth values to the externally measured proposition (a tampered/stale premise was duplicated in all reviewed excerpts). Any checker seeing only internal events returns identical scores in both worlds; no internal-only replayable metric identifies external scientific truth. Thus an independent observation/source-authentication/replication oracle is a distinct proof obligation, not a further pass through the same copied text.

**Atlas:** RA-E16, RA-E10, RA-O08; PF04/PF05/PF11 navigation does not entail correctness.

## L49-07 — Corpus-domain similarity weights and cutoffs are a prototype, not a calibrated theorem

**Primary:** `SRC-0212` PDF physical pp.27–29 proposes `Compat(D,K)` from weighted ontology/operator/invariant/dependency/citation/vocabulary overlap minus contradiction cost, with illustrative thresholds `>0.8`, `0.5–0.8`, `<0.5`. Page 27 explicitly keeps residual pools and cross-domain attachments rather than forcing every text into one Kernel.

**Mathematical caution:** Unless features, weights, scale/normalization and labeled calibration are frozen, `Compat=0.81` is neither a probability of correct placement nor a universal membership decision. For identical documents with two acceptable operator weights, the same candidate may cross thresholds, so no cutoff is an invariant independent of policy. Also 0.8 written as an illustrative value is not a scientifically validated global optimum.

**Repair:** freeze feature schema, weights, source-truth oracle and negative controls; report false attach / false orphan / contamination on held-out cross-domain articles; allow multi-kernel links with typed edge semantics. **Atlas:** RA-E10, RA-R10, RA-O05/08; PF05. Source is explicitly speculative discussion, not empirical performance evidence.

## L49-08 — Same-sign labels and mathematical edge direction must be typechecked independently

**Synthesis:** `SRC-0279`'s proposed Wood→Fire→Earth→Metal→Water relation, historical pipeline `木發散→火收斂→土構形→金驗證→水反思`, and `SRC-0323` Root–Seedling–Flower–Fruit are different mappings between (a) mode-state sets, (b) task-stage labels, and (c) organizational development stages. Shared cycling and 5/4 count is not an equivalence.

**Source-bounded version distinction:** `SRC-0279` p.56 canonical candidate regime names are `Generation→Activation→Closure→Selection→Retention`; v4.8 RA-E03 begins with older `木發散、火收斂、土構形、金核驗、水反思` and should no longer be presented as an unqualified identity to the later hybrid model. Version, target outputs and transition-graph homomorphism need explicit labeling. A valid interface may TRANSLATE particular roles but cannot DERIVE the five-stage AI pipeline or experimental performance from an untested cycle analogy.

**Atlas correction:** RA-E03 amended in v4.9. No original creative route is erased; old labels remain historical/engineering mappings.

## Reconstructability / evidence audit contract

Each `L49-*` node has source locator, typed mathematical assumption, direct falsifier or discrete witness, forbidden stronger consequence and route to an existing Results Atlas card. These nodes do **not** claim all six original documents were comprehensively reviewed, that any source's cultural mapping has been empirically corroborated, or that 603 inherited green regressions imply a clean-room LLM benchmark.


---

# Imported original audit: `GENERAL_LEMMA_REGISTER_v5.0.md`

**Source audit SHA256:** `db81a52e96dcf109174bdbc42f692ef92a575ea908f29050a37abacec54e7829`. Original record, no silent proof strengthening.

# v5.0 — General Lemma Register: source-preserving cross-family mathematical reconstruction

**Date:** 2026-10-15. **Purpose:** mathematically meaningful consolidation, *not* numerical PF/W growth. Original TAR SHA matched for every source below; exact PDF physical pages provided. Five originals were reopened within the specified scopes; no entire-document proof review or independent LLM blind run is claimed. `GL50-*` are compiler audit IDs, not historical W/GM/RA.

## GL50-01 — Fiber Factorization: the shared exact parent lemma

Let `π:X→P` be a map, `f:X→Y` a function (no topology/measure assumed). Then the following are equivalent:

1. There is a map `f̄:π(X)→Y` with `f=f̄∘π`.
2. For every `x,x' ∈ X`, `π(x)=π(x') ⇒ f(x)=f(x')`.

**Proof:** 1⇒2 immediate. For 2⇒1 define `f̄(p)=f(x)` for any x with π(x)=p; constancy on fibers makes it independent of the representative and uniquely defined on π(X). **Domain subtlety:** outside π(X), an extension to all P is not determined and may be impossible if additional continuity/other structure is demanded.

**Same lemma, distinct objects:**

- **PF13 Endpoint:** `f=1_T:X→{0,1}`. Factorization iff `T=π⁻¹(π(T))`. Source `SRC-0234` App.G physical pp.134–136, RA-M02/RA-E07, W308. The theorem concerns one declared `T`, not automatically any different legality/evidence definition.
- **PF01/PF03 Dynamics/Port:** for a fixed external state b and legal action u, let `f_{b,u}(s)=(π(F(s,b,u)),G(s,b,u),H(s,b,u))`. Exact factorization gives one-step closed Port/external/output operations; source `SRC-0261` p.6, RA-M01/RA-M11/RA-E14, W41/W154/W272/W286. Quantifiers include all admissible b,u and all comparable internal states.
- **PF05/PF11 knowledge truth:** π is *an internal promotion/trace ledger*; f is an independently adjudicated proposition truth label. It factors through ledger only when actual truth is constant on all indistinguishable ledger worlds. The source `SRC-0237` pp.105–106 defines replayability/promotion quality but supplies no proof this truth-saturation property holds. RA-E16/RA-O08, W352.

**Critical boundary:** The shared mathematical lemma permits proof-code reuse, **not** semantic replacement of the predicate, observer, actions, or truth oracle. Same *proof pattern* does not mean the original programs are equivalent or empirically true.

## GL50-02 — Exact controlled joint Port quotient

**Declared types:** S internal state, B external state, U action set; `π:S→P`, `F:S×B×U→S`, `G:S×B×U→B`, `H:S×B×U→Y`, all total on the declared closed product domain. Assume for all `(b,u)` and all `s₁,s₂` with `π(s₁)=π(s₂)`:

`πF(s₁,b,u)=πF(s₂,b,u)` AND `G(s₁,b,u)=G(s₂,b,u)` AND `H(s₁,b,u)=H(s₂,b,u)`.

By GL50-01, unique effective maps on `π(S)×B×U` exist, obtained by choosing any representative s. Induction on legal finite action sequences gives matching effective projected trajectories and outputs, **provided** effective states remain in the declared domain. Source exact guard: `SRC-0261` physical p.6 (eqs 4.7–4.9); see also `SRC-0283` pp.9–10. This is a mathematical reconstruction of conditions already in originals.

**What is not proved:** accurate task result, lower-dimensional state, minimality, discovered real neural Port, naturally learned attractor, or stability after checkpoint transport.

## GL50-03 — The omitted danger in partial systems: admissibility itself must factor

For a partially defined controlled dynamic, add `A:S×B×U→{0,1}` giving legal action eligibility. To make eligibility decidable *from the effective Port alone*, it is necessary and sufficient that `A(·,b,u)` factor through `π` for each `(b,u)`. **Counterexample:** `S={s0,s1}`, π maps both to p; all defined transitions and measured outputs are constant, but `A(s0,u)=1`, `A(s1,u)=0`. Restricting eqs (4.7–4.9) to pairs on which u is simultaneously legal makes them vacuously true while the effective controller cannot know whether u is legal.

This does **not** show `SRC-0261` erroneous: it explicitly qualifies the statement by declared operational and closure conditions; `SRC-0283` requires admissible intervention words, and `SRC-0130` p.18 calls out hard intervention preconditions. This node makes an implicit domain guard explicit so compiler/LLMs do not omit it.

**PF01/PF03/PF04 interface:** controlled quotient, causal Port, runtime authority. **Relation:** SHARED_GUARD, not that every legality gate is a dynamical state transition.

## GL50-04 — Finite-word behavioral equivalence forms the coarsest output quotient

For deterministic total `F_u:X→X` on a fixed, state-independent action alphabet U, observation `o:X→Y`, and all finite words w, define `x≈y` iff `o(F_w(x))=o(F_w(y))` for every w, including empty word ε.

1. This is an equivalence relation (intersection of equality relations).
2. For every u, x≈y implies `F_u(x)≈F_u(y)`, since prepend/append u to each finite test word as composition convention dictates; thus it is a right congruence.
3. `o` is constant on classes by ε. Therefore transition `[x]↦[F_u(x)]` and output `[x]↦o(x)` are well-defined.
4. For any other output-preserving exact quotient π, π(x)=π(y) entails x≈y by induction. Thus its fibers are contained in the ≈ classes; the quotient by ≈ is coarsest up to canonical isomorphism.

This completes an existence direction and specifies needed action closure for the theorem described in `SRC-0283` physical pp.9–10, RA-M01/RA-R04. **Not applicable without modification** if the admissible action words vary with hidden state, observations are probabilistic without probability-law equality, or the model has unbounded-history policies not included in state.

## GL50-05 — Replay evidence and external truth: countermodel across PF13/PF05/PF11

Let X contain (world w, internal event log ℓ). Projection π(w,ℓ)=ℓ. Two worlds may produce identical well-formed, hash-consistent, replayable ℓ while one external proposition is true and the other false; let f(w,ℓ)=truth(w). Since f differs on a π-fiber, GL50-01 proves **no log-only truth function exists** on that domain. `SRC-0237` pp.105–106 supplies internal replay/promotion metrics, not an external truth oracle; `SRC-0234` pp.134–136 separately proves an analogous saturation boundary for endpoint acceptance.

**Non-equivalence:** A log may be perfectly replayable (M2 governance contract) and still record invalid scientific claims; a cryptographic digest ensures byte integrity relative to an external anchor only when such a trust root exists, not scientific truth. This is an epistemic guard, not a theorem that all Wiki Maturation deployments necessarily fail.

## GL50-06 — Cross-family NO-GO implications with explicit finite models

**Endpoint saturation does not imply Markov quotient:** states `S={(a,h):a,h∈{0,1}}`, π(a,h)=a, valid T={(1,0),(1,1)}. T is π-saturated. Set F(a,h)=(a XOR h,h) and observation o(a,h)=a. Same current π for (0,0) and (0,1) but next π differs: 0 vs 1. Thus RA-M02 does not entail RA-M01.

**Port sufficiency does not imply functional correctness:** choose F=id, observation constantly 0, candidate π constant; every fiber is exactly closed but a target task expecting 1 fails. Conversely, computing one target sample correctly says nothing about global interventional sufficiency.

**Stable attractor does not imply useful task Port:** an independently converging hidden register h with output depending only a may be an attractor yet irrelevant to task. A designer-chosen trivial exact Port can exist without naturally emergent attractor. These negative directions are consistent with `SRC-0261` pp.6,13–15, RA-R08/RA-H02.

**Labels:** SAME_LEMMA_INSTANCE for GL50-01 applications, CONDITIONAL_DERIVES for specific realizations, SHARED_GUARD where extra action eligibility is needed, NON_ENTAILMENT for negative examples, and TRANSLATES only for cross-domain motivating analogy.

## Explicit source depth/evidence ceiling

All five SHA checks are recorded in `SOURCE_IDENTITY_CHECK_v5.0.json`; precise review scopes in `SOURCE_DEPTH_AUDIT_v5.0.csv`. PDF p.6 `SRC-0261`, p.9 `SRC-0283`, p.136 `SRC-0234`, p.106 `SRC-0237`, and p.18 `SRC-0130` were rendered as page images and inspected. Algebraic finite countermodels are tested locally; **none is independent scientific validation**. Source-first interpretation may still be challenged by further full reading and independent researchers.


---

# Imported original audit: `GENERAL_LEMMA_REGISTER_v5.1.md`

**Source audit SHA256:** `07c785f5eeed44dd5e74353ec5ab6eef752cec8dd45c90df434dd12f5cb8508b`. Original record, no silent proof strengthening.

# v5.1 — Three distinct Proof-Family Skeletons, with source-scoped counterexamples

Date: 2026-10-15. **Scope:** mathematical audit of five SHA-verified primary PDF members at explicit physical pages (see `SOURCE_IDENTITY_CHECK_v5.1.json`). `GL51-01..07` are *compiler audit IDs*, not new historical Witness, GM, Atlas cards, or physical discoveries.

## GL51-01 — PF07: Fenchel–Young Gap Derivative and a DECLARED descent controller

**Typed conditions:** proper closed convex conjugate pair `Phi=psi*`, smooth where used, fixed baseline `q`, independent state variables `(s,lambda)`. Define `G=Phi(s)+psi(lambda)-lambda·s>=0`.

**Exact general derivative:** `dot G = (grad Phi(s)-lambda)·dot s + (grad psi(lambda)-s)·dot lambda`.
On the conjugate manifold `grad Phi(s)=lambda, grad psi(lambda)=s`, `G=0` and `dot Phi=lambda·dot s`, `dot psi=s·dot lambda` separately; not the source's `dot Phi=lambda·dot s-dot psi`.

**Negative control:** quadratic conjugate `Phi(s)=s²/2`, `psi(lambda)=lambda²/2`, take `s=t`, `lambda=0` for `t>0`. Then `G=t²/2` **increases** despite convex duality. A gap is an alignment *diagnostic*, not a Lyapunov certificate without a stated law.

**Conditional repair / proposed engineering controller (not asserted by source):** impose `dot s=-k(grad Phi(s)-lambda)` and `dot lambda=-h(grad psi(lambda)-s)` with fixed k,h>0. Then `dot G=-k||grad Phi-lambda||²-h||grad psi-s||²<=0`. This guarantees monotonicity while its convergence to a particular global equilibrium still requires additional boundedness, coercivity/invariance, and/or strictness assumptions. Keep the status `COMPILER-DERIVED PROPOSAL`, not historical source theorem.

**Source:** `SRC-0119` physical pp.2–3 §3.3–3.8 and pp.5–8 §§6,8–9; v4.5 `L45-01..03`, v4.6 `L46-01..03`. Linked RA-M06/RA-R05, W198/W257–259, PF07. **Non-entailment:** no medical health prediction, physical thermodynamics or unconditional AI stability follows.

## GL51-02 — PF07: ordinary action penalty and Rayleigh damping are not equivalent

**Source claim:** `SRC-0064` PDF physical p.2 §3 places `Gamma[x]>=0` directly in a variational action `S_eff=integral L dt - lambda Gamma[x]` and says varying it covers Rayleigh friction. `SRC-0119` pp.6–7 §8 separately writes an explicit Rayleigh function R.

**Countermodel:** set `L=(m/2)dot x² - V(x)`, and `Gamma[x]=integral (c/2)dot x² dt` with m,c,lambda>0. Stationarity with fixed endpoints yields `(m-lambda c)ddot x+V'(x)=0`, not `m ddot x+c dot x+V'(x)=0`. For `lambda c<m` this modified action is conservative with a changed inertial coefficient, not friction. The Rayleigh force `-partial R/partial dot x=-c dot x` is an extra generalized-force prescription and requires its own energy bookkeeping.

**Boundary:** Nonlocal dissipative variational principles can exist with special structure and boundary protocols; this finite counterexample only refutes automatic derivation from an arbitrary nonnegative path functional.

**Linked:** RA-M07, W25/W319–320, PF07; `SRC-0064` p.2 and `SRC-0119` §8.

## GL51-03 — PF06: local U(1) connection and holonomy require different objects

**Typed graph:** oriented vertices i,j, phases `theta_i` modulo 2π and antisymmetric oriented link `A_ij=-A_ji`. Define edge mismatch `D_ij=theta_i-theta_j-A_ij` and `E=sum_undirected_edges(1-cos D_ij)`.

**Transformation:** `theta_i→theta_i+alpha_i`, `A_ij→A_ij+alpha_i-alpha_j`. Then every D_ij and E are unchanged under independent local transformations. If instead `A=0` fixed, the bare cosine is only invariant to **common** alpha, not arbitrary sitewise alpha. For a directed cycle C, the Wilson angle `W_C=sum_{(i,j) in C} A_ij mod 2π` is gauge invariant by telescoping. A link energy with local covariance does **not** force `W_C != 0`; pure-gauge `A_ij=theta_i-theta_j` has all D=0 and every loop W=0.

**Source:** `SRC-0274` p.2, energy term and gauge-like/holonomy language; RA-M08/RA-H07, PF06 W236–238. The paper's signed `beta sum L` without sign/coercivity guard remains insufficient as nonnegative energy (v4.5 L45-06). **Non-entailment:** a mathematically correct U(1) link model is not evidence of fermions, 4π spinor response, zero-flux physical effects, or a natural Agent gauge field.

## GL51-04 — PF10: Lyapunov approach to a set is not relative phase selection

**Source:** `SRC-0108` physical pp.13–14 §8.1–8.4 states model `i dot a_n=omega_n a_n + lambda |a_n|² a_n + kappa a_{n+5} - i gamma a_n` and Theorem 8.1 that with uniform damping the Δ5 antisymmetric set becomes globally asymptotically stable, with **all pair phases** `phi_{n+5}-phi_n→π`. p.15 §9.2–9.3 displays identical linear damping for symmetric e and antisymmetric p components.

**Exact allowed counterexample:** choose lambda=0, one mirrored pair `x(0)=y(0)=1`, omega equal, gamma,kappa>0. Then `x(t)=y(t)=exp(-gamma t-i(omega+kappa)t)` for every finite t. `E_pair=|x+y|²=4exp(-2gamma t)→0`; yet the phase difference is **0**, never π. Both e=(x+y)/2 and p=(x-y)/2 have decay rate gamma; their norm ratio is unchanged whenever both components initially nonzero. Every amplitude tends to the **zero** vector, which lies in the antisymmetric set. Thus `distance(a(t),M)→0` can hold trivially without a nonzero antisymmetric pattern being chosen. A globally attracting origin does not establish relative mode selection or normal spectral-gap attraction.

**Additional problem:** even if the static nullspace `ker P_+` minimizes `E_pair`, LaSalle with vanishing total norm cannot give limiting nonzero relative phases; at zero amplitudes the phase is undefined. The theorem's stronger phase-convergence claim is false for its own allowed linear example. Do NOT erase the still-correct static anti-alignment minimizer, or the restricted `dot E_pair=-2gamma E_pair` in the linear symmetric model.

**Needed repair:** normalized/postselected phase observables with a positive-amplitude lower bound and an actual transverse-vs-tangent decay-rate gap, or selective pumping that preserves nonzero antisymmetric amplitude; then reprove under specified dynamics. Do not infer quantum or actual HeTu emergence from a repaired toy model.

**Linked:** RA-R09, RA-H04, PF10, W17–20. Also distinguish v4.5 factor-2 normalization error: `E_pair=2||P_+a||²` under the specified ten-site norm.

## GL51-05 — PF10: a supposed Δ5 flux anti-correlation is tautological

`SRC-0108` p.14 §8.5 defines `Pi_n=kappa Im(conj(a_n)a_{n+5})`, and claims `Pi_{n+5}≈-Pi_n` / correlation <0 as a signature of locked pairs.

With the same real kappa for both directions, **identically for every complex pair** `Pi_{n+5}=kappa Im(conj(a_{n+5})a_n)=-Pi_n`; no phase-locking premise used. Thus for nonconstant observations the Pearson correlation is exactly -1 regardless of locking. At the claimed exact lock `a_{n+5}=-a_n`, both Pi vanish at all times and correlation is undefined (zero variance). This observable by itself is not an independent, discriminative prediction of Δ5 locking; one needs a null-model-sensitive observable and predeclared comparison regime.

**Linked:** PF10 (observable discrimination), PF02 (complex phase readouts), RA-R09/RA-H04, SRC-0108 p.14.

## GL51-06 — PF10: sign of restoring drift and noise floor

`SRC-0287` p.2 sets `dot Delta=-mu` and calls `mu` a restoring field, while §3.3 (eq.3.3) instead sets `mu in -partial V` for convex V with unique minimum at 0. For V=Delta²/2, mu=-Delta gives `dot Delta=+Delta`, unstable. Likewise p.3 eq. (3.6) has `mu=-k sat(Delta/delta0)`; under `dot Delta=-mu` the sign is outward, not restoring. **Repair:** either set `mu in +partial V` when using `dot Delta=-mu`, or define `dot Delta=mu` with the originally negative subgradient. Never silently change source signs.

**Second qualifier:** adding bounded but nonvanishing noise to `dDelta=-kDelta dt+sigma dB_t` produces `E[Delta_t²]=exp(-2kt)Delta_0²+sigma²(1-exp(-2kt))/(2k)`. For sigma!=0 the distribution has a nonzero stationary variance, so Delta does not converge in probability to 0. One may derive mean-square **ultimate boundedness**, not claim exact convergence/whitening or an absorbing equilibrium without a vanishing/noise-controlled diffusion condition. This is a source-scoped countermodel to overly broad engineering wording; no claim concerning the truth of the Riemann Hypothesis follows.

**Linked:** RA-M13, PF10, W273, SRC-0287 pp.2–4, earlier K1 conditional corrections.

## GL51-07 — Type-directed dependency graph: shared Lyapunov algebra, not a common physical mechanism

The same nonnegative scalar derivative template `dot V=grad V·F<=0` can be instantiated as (a) PF07 engineered convex-gap descent (`GL51-01`), (b) PF10 damped mechanics with positive-definite energy and declared forcing (`GL51-02/06`), or (c) energy decay in HeTu toy amplitudes (`GL51-04`). These instances have distinct state types, controlled variables and stable sets. **Shared proof skeleton** is not a claim that semantic entropy is physical energy, that a gauge term provides a Lyapunov function, or that the geometry uniquely picks a phase mode. PF06's local invariance law is a different parent lemma and does not imply a dissipative dynamics without an additional chosen evolution law.

**Graph discipline:** `SHARED_PROOF_SKELETON` for derivative inequalities; `CONDITIONAL_DERIVES` for explicit algebra, `COUNTERMODEL_TO_STRONG_CLAIM` for source overclaims, `NON_ENTAILMENT` for cross-family jumps. Preserve original source provenance/W histories; no PF merged and no RA promotion.

## Evidence boundary

Five original TAR PDF members were independently SHA-matched and limited ranges inspected (seven page images rendered; physical pages cited above). Neither whole-document depth completion nor independent scientific validation/independent LLM reconstruction is claimed. Existing benchmark C0/C1/C2 participant input packages were not run on a separate LLM; no RAG baseline or token-balanced comparison is available.


---

# Imported original audit: `GENERAL_LEMMA_REGISTER_v5.2.md`

**Source audit SHA256:** `dea6893b95ab0daa4dc71fa67894db9be1805c3d541409ff2a26c764fb386c80`. Original record, no silent proof strengthening.

# v5.2 — Cross-domain Source Mathematics / Testability Register

**Scope:** physical-PDF-page-scoped mathematical audit of five SHA-256-confirmed primary members. `GL52-01..07` are *compiler audit nodes*, **not** historical W or author-originated theorems. No entire source is certified fully reviewed. No independent empirical/LLM trial.

## GL52-01 | PF14 / Finance: CAPM angular-rate derivative omission

- **Original:** `SRC-0043` physical p.27, (3.22)–(3.31). The article differentiates `cos θ=[(1+r*)/(1+r(t))]^T` and gives a correct derivative including `dr/dt` in (3.27), but drops this factor in (3.29)/(3.31) after declaring `dr*/dt=0`. Formula page visually checked against PDF.
- **Typed assumptions:** fixed finite `T>0`, rates greater than -1, `r(t)>r*` so `0<cos θ<1`, differentiable `r(t)`, constant `r*`, and `0<θ<π/2`. `θ=arccos` uses principal branch.
- **Proof:** `-tan θ θdot = -T rdot/(1+r)` therefore `θdot=T rdot/[(1+r)tan θ]`. This can be checked via direct chain-rule differentiation.
- **Counterexample to source (3.29):** fixed `r=0.07`, `r*=0.03`, `T=2`, gives `θdot=0`; source (3.29) yields `2/[(1.07)tan θ] >0`, despite no change in rates. This is not an automatic nonzero stress signal.
- **Consequences:** derived `ω_F`, `Λ_F=Qω_F` and any alleged angular-velocity forecast using (3.31) need recalculation. The corrected geometric coordinate and the source's earlier (3.27) survive. If `T(t)` itself changes, an additional maturity-horizon derivative arises and this fixed-T formula cannot be used.
- **Atlas:** RA-E08, RA-M09, RA-O07. **Status:** M3 scoped mathematical correction, M5 financial prediction untested.

## GL52-02 | PF14 / Finance: a real pressure complement requires a declared admissible domain

- **Original:** `SRC-0023` p.6 (2.6)–(2.14), pp.11 and 15 certainty-equivalent/CAPM constructions; `SRC-0043` p.25 CAPM rate ratio.
- **Typed premises:** `A=|Z|≥0`, `R∈ℝ`, `Q∈ℝ`, `A²=R²+Q²`, hence `|R|≤A`. The restricted positive-angle model `0≤θ≤π/2` further requires `0≤R≤A`.
- **Countermodel:** positive discounted CF, `r*=0.05`, `r_CAPM=0.02`, `T=1` implies `R/A=1.05/1.02>1` and `Q=√(A²−R²)` is not real. Lower CAPM hurdle can arise for negative-beta assets/other permitted rate conventions, so strict `r_CAPM≥r*` must be an explicit *applicability gate*, not universal CAPM mathematics.
- **Signed-flow countermodel:** `CF<0` and original `A=CF/(1+r*)^T` gives `A<0`, contradicting `A=|Z|`. One must restrict to positive cashflow, rework sign conventions separately, or use a different embedding; these yield distinct semantic claims.
- **Atlas:** RA-E08 / RA-O07. Does not refute valuation filters outside their admitted real-circle embedding.

## GL52-03 | PF14 / Finance: geometrical residual is identically zero unless inputs are independent

- **Original:** `SRC-0043` pp.3,8–9,55–56 explicitly separates identity, interpretation, empirical hypotheses, and permits the residual to falsify the model. `RA-M09` was already correct on this matter: **do not present as a new source error**.
- **Proof:** With differentiable `A>0`, `Z=Aexp(iθ)`, `g_A=A'/A`, `ω=θ'`, `Z'-(g_A+iω)Z≡0`. Any measured nonzero `ε_dyn` must use rates estimated *independently*, different protocols or time discretization; specify sampling, calibration and null benchmarks.
- **Discriminating test:** compare out-of-sample forecasts or conditional residuals from frozen estimators against conventional market factors, not identity reconstructions from the same `Z` data. Equality of two numbers in a coordinate transform is not empirical risk discovery.
- **Atlas:** RA-M09, RA-E08, RA-O07, PF14; source itself acknowledges this distinction. M3 algebra, M5 NOT_RUN.

## GL52-04 | PF02 / Semantic Field: norm is not automatically conserved by the proposed SSLE

- **Original:** `SRC-0268` physical pp.2–3 master Schrödinger-like SSLE with real saturation `σ|Ψ|²Ψ`, non-Hermitian `-iΓΨ`, observer term and drive `J`. `SRC-0247` p.3 presents `Ψ_m` as interpretation-weight possibility, not measured neural Hilbert amplitude.
- **Assumptions:** for the norm calculation, let `iℏ_s Ψdot=H_self-adjoint Ψ+σ|Ψ|² Ψ -iΓΨ+J`, `ℏ_s>0`, real `σ`, real `Γ≥0`; boundary conditions give no net boundary current. In general the full original observer term requires its own Hermiticity assessment.
- **Derivation:** `d||Ψ||²/dτ = - (2/ℏ_s)∫ Γ|Ψ|² + (2/ℏ_s) Im⟨Ψ,J⟩`. If Γ is positive constant and J=0, `||Ψ(τ)||²=||Ψ(0)||² exp(-2Γτ/ℏ_s)`.
- **Boundary:** A complex equation does not by itself define conserved Born-rule probabilities. An externally normalized conditional state, explicitly nonconserving physical/intensity norm, or a trace-preserving density-matrix dynamics would be different models, requiring documented source/evidence.
- **Atlas:** RA-H01, RA-M12, RA-O01. M3 scoped calculation; no neural-field ontology or empirical collapse implied.

## GL52-05 | PF01/PF02: positive collapse-channel weight does not ensure a probability distribution

- **Original:** `SRC-0268` physical p.2 gives `P_j(τ)=⟨Ψ|O_j†O_j|Ψ⟩` and a tick hazard `λ(τ)=κ⟨Ψ|O†O|Ψ⟩`; p.3 includes loss and drive. `SRC-0247` pp.5–7 uses observer/angle threshold language with no empirical probability calibration.
- **Proof:** each raw channel weight is nonnegative for suitable operators, but `Σ_j P_j=⟨Ψ|Σ_j O_j†O_j|Ψ⟩`. This equals one only when `||Ψ||=1` and the channel effects sum to identity (or other explicitly normalized preparation / postselection). Under loss, even complete effects yield `ΣP_j=||Ψ||²`, not one.
- **Rate versus chance:** `λ` may be a *hazard rate* and may exceed 1 per time unit. Under constant nonnegative λ during interval Δτ, event probability is `1-exp(-λΔτ)`, not automatically `λ`. Without declared click process/calibration, symbolic channel intensities are not empirical observer statistics.
- **Atlas:** RA-H01 / RA-M12 / RA-O01. The conditional normalized fractions `p_j=P_j/ΣP` can be defined if denominator positive, but they are not by themselves evidence of physical Born-rule semantics.

## GL52-06 | PF02: a real Robin boundary cannot be equated to a dissipative sink-flux gate

- **Original:** `SRC-0268` physical p.3 boundary/control: `∂_nΨ|_Σ=κ_g Ψ|_Σ`, and flux `J_x=(ℏ_s/m_x) Im(Ψ*∇Ψ)` at p.2.
- **Proof / qualified obstruction:** At an **exterior** boundary where this is an ordinary Robin derivative and `κ_g∈ℝ`, the normal current is `J_n=(ℏ_s/m_x) Im(κ_g |Ψ|²)=0`. This can tune reflection/standing-state response, but by itself is not a nonzero outflow or absorbing-sink throughput.
- **Critical distinction:** if `Σ` is an *interior interface* and the displayed bracket is a derivative-jump condition, not a single-sided boundary derivative, this zero-flux argument cannot simply be transferred; one must state both sides and continuity/coupling. An imaginary impedance, absorbing potential, non-Hermitian matching or separate sink term can yield flow, but require positivity and balance conditions.
- **Atlas:** RA-H01 / RA-O01. Conditional mathematics, not claim that all source Gate metaphors are false.

## GL52-07 | PF01/PF03: field readout or stable structure is not an identified neural Functional Port

- **Original:** `SRC-0261` physical p.6 exact joint Port closure requires fiberwise equality of `ΠF`, external update `G` and output `H`; pp.15–16 warn against retrospective birth claims; p.25 has stop rules for no predictive increment, false positives, contract drift and attractor without mechanism. `SRC-0247` pp.2–7 describes field/collapse as candidate research language.
- **Dependency:** A proposed `Ψ_m(x,θ,τ)` + event threshold does not identify a real neural readout map `r(h)` or an intervention-closed projection `Π(h)`. To infer a qualified Port, specify `(state, clock, projection, controls, output, legal actions)` and demonstrate `ΠF`, `G`, `H` congruence on every admitted fiber. To infer naturally forming attractors also require measured training trajectories and causal interventions (not just simulations of a deliberately attractive PDE).
- **Countermodel:** two internal states `s=(p,h)` with same observed p; under training interventions `u=0`, define `H=p`; but under `u=1`, define `H=h`. Both are indistinguishable without the hidden intervention, yet a p-only Port fails once u=1 is admitted. This is an explicit *intervention-domain* non-entailment, not a refutation of exact Port factorization with its correct guards.
- **Atlas:** RA-M01, RA-M11, RA-E14, RA-H01/H02, RA-O01/O02, RA-R08. M3 conditional finite countermodel, M5 neural experiment NOT_RUN.

## Conclusions / explicit non-claims

Preserve the semantic field and risk-pressure constructs as hypothesis-rich *generative representations*. Their current algebra does not give automatic norm conservation, Born probabilities, physical sink absorption, new financial alpha, neural attractor formation or an invariant cross-domain isomorphism. Preserve original source hashes and claim lineage; LLM/compiler corrections are not backdated historical author results. No independent model has reconstructed these results under a clean-room hidden rubric in v5.2.


---

# Imported original audit: `GENERAL_LEMMA_REGISTER_v5.4.md`

**Source audit SHA256:** `f5755b61f55c29e92114d6cab81fedc5e8ca0a14970b2d21d1b921c132394607`. Original record, no silent proof strengthening.

# v5.4 Source-Anchored General Lemma Register — Octonionic Declaration and Operational Closure

**Source status:** primary TAR bytes verified against 325-row Manifest. `SRC-0306` is a **1099-page** longitudinal AI dialogue: only physical PDF pp.1–8,75–76,81,86–91,94–104,119–122 were selectively inspected/queried; some formula pages 81,86,90,94,95,102,104 image-rendered. `SRC-0304` selected pp.1–9. `SRC-0283` selected pp.3–10. Neither searchable extraction nor page-range inspection is a whole-document proof audit. Source p.90 rendered and visually verified. All derived statements below are scoped elementary mathematical checks, not external physics/AI validation.

## GL54-01 — G₂-invariant selection cannot uniquely choose an associative declaration

**Source position:** `SRC-0306` physical pp.81,86–87,90,94–95 distinguishes the moduli `M=G₂/SO(4)`, its invariant metric, and a still-needed external declaration functional. The authors propose an observer-/ensemble-conditioned minimizer, not a proven cosmological selector.

**General lemma:** If a group `G` acts transitively on nonempty `M` and `L:M→ℝ` satisfies `L(gm)=L(m)` for every `g,m`, then `L` is constant. For any `m,n`, some `g` has `gm=n`, whence `L(n)=L(m)`. There is no unique minimizer whenever `|M|>1`.

**Application:** `M=G₂/SO(4)` has dimension `14−6=8`; hence its natural invariant metric alone cannot designate a privileged subalgebra. A **covariant data-conditioned** loss `L(gA;gΩ,gP)=L(A;Ω,P)` can be nonconstant for fixed non-invariant `Ω,P`; this does not contradict the lemma. Must declare actual ensemble, task and tie-break, not assert universal symmetry-induced selection.

**Forbidden inference:** an 8-dimensional declaration moduli is not the 8-dimensional underlying octonion vector space, nor a natural law choosing this universe.

## GL54-02 — Projection-loss minimality is not an identification theorem

**Source:** `SRC-0306` physical p.90 equations (27)–(30), `L_res(A)=Σ_i w_i||x_i−D_Ax_i||²`, with optional interaction defect. Source itself acknowledges residual-only selection is constrained PCA.

**Exact counterexample A (nonzero isotropic):** take unit orthonormal imaginary octonion basis `e₁,...,e₇` at equal weight 1. For any associative 3-plane `A⊂Im 𝕆`, `D_A` retains exactly three imaginary dimensions, so `L_res(A)=Σ_i(1−||P_A e_i||²)=7−trace(P_A)=4`. Every possible declaration minimizes. This uses nonzero complete data and does not depend on a zero-ensemble trick.

**Counterexample B (anisotropic yet nonunique):** data `{e₁}` alone give loss 0 for *every* quaternionic subalgebra containing `e₁`; e.g. quaternionic imaginary planes spanned by `(e₁,e₂,e₁e₂)` versus `(e₁,ℓ,e₁ℓ)`.

**Repair obligation:** impose a declared nondegeneracy/separation or external tie-break; demonstrate identifiability under perturbations; evaluate whether `L_int` and `L_obs` actually remove ties. No unconditional unique selection theorem established.

## GL54-03 — Orthogonal projection onto ℍ is not generally a multiplication homomorphism

**Originals:** `SRC-0306` pp.76,87,90 explicitly propose a state projection and an *interaction defect* `||D_A(xy)−D_Ax D_Ay||²`. Thus this is a typed negative control against **overreading the source**, not a claim that source falsely asserted multiplicativity.

**Counterexample:** choose Cayley–Dickson `𝕆=ℍ⊕ℍℓ`, `D(a+bℓ)=a`, `ℓ²=−1`. Then `D(ℓ)=0`, but `D(ℓ²)=−1 ≠ 0=D(ℓ)²`.

**Consequence:** multiplication is closed inside the *admitted* ℍ; octonion multiplication projected from general input is not a morphism. The source's interaction-defect functional therefore carries genuine information, subject to explicit calibration.

## GL54-04 — A closed target algebra is not an exact controlled quotient

**Cross-source:** `SRC-0283` physical pp.7–10 requires future/intervention congruence for an exact behavioral quotient; `SRC-0306` pp.76,87 describe a possible `D_A` without asserting universal dynamics-lumpability.

**Counterexample:** use `D(a+bℓ)=a` and controlled update `F(x)=xℓ`. States `x=ℓ`, `y=−ℓ` share `D(x)=D(y)=0`, but `D(F(x))=−1`, `D(F(y))=+1`. Therefore no well-defined effective map `Fbar` can satisfy `D∘F=Fbar∘D` for both states. This is a precise instance of GL50 fiber factorization failing.

**Repair obligation:** declare admissible state subset, allowed update/observer protocols, and prove the quotient congruence. Algebra closure ≠ operational sufficiency ≠ natural semantic individual.

## GL54-05 — Quaternionic ℂ² is a polarization, not a complementary second 4D port

**Source:** `SRC-0306` physical pp.2,6–8,75–76,81 explicitly revises the initial `8D→two independent 4D branches` picture to `𝕆→ℍ` (loss) followed by `ℍ≅ℂ²` (coordinate choice).

**Formal boundary:** choosing an imaginary unit `i∈Im ℍ` gives a real-linear isomorphism `ℍ→ℂ_i²` of real rank 4, not a second map that independently observes the discarded `ℍℓ`. A stacked pair `x↦(D(x),P(D(x)))` with invertible polarization `P` has real rank ≤4, not 8. Right/left quaternion multiplication involves conjugation in the chosen complex coordinates; this is not an algebra isomorphism `ℍ≅ℂ⊕ℂ`.

**Noncanonical J:** quaternion inner automorphisms rotate imaginary unit axes. For instance, conjugation by `j` sends `i→−i`. A particular `J` must be selected by extra structure; `S²` candidate axes do not choose themselves.

## GL54-06 — Natural declaration metric does not entail a physical metric or global unique geodesic

**Sources:** `SRC-0306` physical pp.94–95,102–104,119–121 gives symmetric-space metric/geodesics and explicitly warns global shortest paths need cut-locus handling; `SRC-0304` physical pp.5–7 distinguishes quaternion Euclidean norm from Lorentzian spacetime and different Hermitian-matrix constructions.

**Scope:** An invariant positive definite metric `g` on `G₂/SO(4)` describes distance between declarations; it is not a Lorentzian metric on 3+1 spacetime. Riemannian `γ_X(t)=g₀ exp(tX)H` expresses geodesics for `X∈𝔪`, but a valid endpoint/geodesic does not prove globally unique shortest path, causal time, transport of `ℂ²` state, physical curvature, or quantum holonomy. A connection on operational associated bundles and empirical measurement correspondence are separate proof obligations.

## Cross-family type table

| Typed relation | Allowed | Disallowed shortcut |
|---|---|---|
| `GL54-01/02 -> RA-H03` | `LIMITS` selection uniqueness | No `DERIVES` cosmos |
| `GL54-03 -> GL54-04 -> RA-M01/RA-R04` | countermodel to exact quotient without guards | No assertion all ℍ models fail |
| `GL54-05 -> RA-H03` | same 4D representation after polarization | No imaginary second independent 4D |
| `GL54-06 -> RA-O04` | geometry/physics boundary | No Lorentz signature from norm alone |

**Scientific maturity:** scoped algebraic results/checkable finite examples; creative candidate selection function preserved as an open model; no independent model reconstruction, physics/neural measurement, or novelty/prior-art certification.


---

# Imported original audit: `GENERAL_LEMMA_REGISTER_v5.5.md`

**Source audit SHA256:** `12a20249c1c186825e02363697376d2a87e091bbed1686fd48888b47642c56e0`. Original record, no silent proof strengthening.

# v5.5 — Source-anchored Declaration, Interaction, Purpose–Observer Proof Register

**Status:** local mathematical reconstruction and primary-source-page challenge. No physics/AGI empirical verification, no full review of the 1,099-page anthology and no independent-model blind reconstruction. `GL55-*` are new audit node IDs, **not** added historical Witnesses or author-priority claims.

**Primary:** `SRC-0306` SHA `1774763df9b38913cfee4047c59c085a44057a0be5dae93f9228d5df893081bb` (original `World Formation.tar` member); exact physical pages listed below. `SRC-0283` and `SRC-0261` are supporting primary sources, hashes in `SOURCE_IDENTITY_AND_DEPTH_v5.5.json`.

## GL55-01 — Two independent imaginary octonions determine a unique associative quaternion subalgebra

**Original context:** SRC-0306 pp.87–90 discusses choosing two independent imaginary directions `u,v` to declare `H_A=span{1,u,v,uv}`. This is a genuine positive identifiability result under stronger data conditions than GL54-02.

**Premises:** `u,v∈Im(O)` are real-linearly independent and nonzero; octonions form an *alternative* normed algebra. Artin's theorem ensures the subalgebra generated by any two elements is associative. After orthogonalization of `u,v`, their product has nonzero imaginary component perpendicular to both; `Q=span_R{1,u,v,uv}` has dimension four and is a quaternion subalgebra.

**Uniqueness:** Any quaternion subalgebra containing both vectors must contain their product and therefore all of `Q`; because both are 4-dimensional, it equals `Q`. **This statement requires the data to be declared EXACTLY contained in the candidate subalgebra.** It does not imply observations from a noisy statistical ensemble specify unique `A` or that an observer/learning process naturally selects it.

**Negative control:** One imaginary sample (`u` only) belongs to many quaternion subalgebras; isotropic data of GL54-02 does not uniquely identify a world. New distinction: *generating-pair exact algebraic identification* vs *observed, perturbed, task-conditioned selection*.

## GL55-02 — Unique fit does not give global positive separation in continuous moduli

**Premises:** On `M=G2/SO(4)` let continuous `L(A)` have a unique minimizer `A*`, e.g. the exact containing-span residual of GL55-01. Since `M` has no isolated points, there are distinct `A_n→A*`. Then `L(A_n)→L(A*)`.

**Consequence:** `inf_{A ≠ A*} (L(A)-L(A*)) = 0`. Hence unique minimizer DOES NOT imply a strictly positive uniform global loss margin against all competing declarations. A finite-net margin, local curvature bound, controlled perturbation model or separated candidate class is needed for quantitative robustness. The source pp.90–100 suggests minimization but does not prove universal stable identification.

## GL55-03 — Covariant selection can break fixed-data symmetry without violating G2-equivariance

**Premises:** Let `L(A;Ω,P)` obey `L(gA;gΩ,gP)=L(A;Ω,P)` for all `g∈G2`. Then minimizer *sets* transform as `Argmin L(·;gΩ,gP)=g Argmin L(·;Ω,P)`. If the optimizer is unique, the selected `A*(gΩ,gP)=gA*(Ω,P)`.

**Limit:** This is equivariance, NOT unconditional invariance `L(gA)=L(A)` for fixed inputs. GL54-01 forbids selection from completely symmetric, fixed no-input criteria; it does not forbid data-conditioned equivariant selectors. Degenerate ensembles may have multiple optimizers. `SRC-0306` pp.89–91,99–101 proposes conditioned losses and gated gradients; this lemma types the missing symmetry assumption.

## GL55-04 — Source equation (17) is not automatically a nondegenerate two-form

**Primary source:** SRC-0306 physical p.610 eqs. (15)–(20), rechecked from rendered PDF image; p.611 explicitly says nondegeneracy/compatibility remain unproved. It proposes `ω_BO(u,v)=δ_uδ_v ℒ−δ_vδ_u ℒ` as an order-sensitive object to induce complex `J`.

**Case 1 — commuting coordinate variations:** If `ℒ` is `C²` and `δ_u,δ_v` are fixed commuting direction derivatives, Schwarz symmetry gives `δ_uδ_v ℒ−δ_vδ_u ℒ=0`, so the proposed two-form is identically zero and degenerate.

**Case 2 — noncommuting vector-field variations:** Write `δ_X f=X(f)`. Then `X(Yℒ)−Y(Xℒ)=[X,Y]ℒ` can be nonzero, but generally is not a tensorial bilinear two-form in the values `X_p,Y_p`. Indeed `[fX,Y]ℒ=f[X,Y]ℒ−Y(f)X(ℒ)`; the last term can survive even if `f(p)=0`. Explicitly on `R²`, `X=∂_x`, `Y=x∂_y`, `ℒ=y`: at origin `Y(0)=0` yet `[X,Y]ℒ=1`. A two-form MUST give zero whenever one argument is zero at the point.

**Repair:** Define a genuine tensorial antisymmetric two-form from explicitly declared causal/observer variations, e.g. use a connection and its curvature or a declared bilinear antisymmetrization on tangent vectors; then independently prove its nondegeneracy. A generic operator commutator, including one of two arbitrary matrices, is also not automatically skew-adjoint relative to an arbitrary metric. **This is a new precise proof obligation, not a claim that the source already proved the route.**

## GL55-05 — Conditional polar complex-structure construction is valid; dimension 4 is not forced

**Primary:** SRC-0306 physical pp.389–401 suggests `Purpose metric + order-sensitive 2-form` and pp.610–613 states `A=g^{-1}ω`, `J=A(-A²)^{-1/2}` under conditions.

**Theorem:** For a finite-dimensional real inner-product space `(V,g)` with a nondegenerate alternating bilinear 2-form `ω`, let `K=g^{-1}ω` so `g(Ku,v)=ω(u,v)`. Then `K` is invertible and `g`-skew-adjoint; `−K²` is symmetric positive definite and commutes with `K`. Define `J=K(−K²)^{-1/2}`. It follows `J²=−I` and `J` is `g`-orthogonal. Thus `(V,J)` is a complex vector space. This is standard linear-algebra polar decomposition, not independent discovery that SMFT necessarily induces ω.

**Boundary:** Nondegenerate alternating forms require EVEN real dimension, but can exist already in real dimension **2**. They do not force dimension 4, two complex channels, a preferred octonionic quaternion `A`, or a natural neural mechanism. For `K=diag(2J₂,3J₂)`, the polar transform has equal-sign unit blocks `diag(J₂,J₂)`; `J₂=[[0,−1],[1,0]]`.

## GL55-06 — No canonical G2-invariant internal imaginary quaternion axis from the declaration alone

**Primary:** SRC-0306 pp.91–93,101–104 defines quaternionic operational fibres and seeks transport; pp.611–616 proposes observer/purpose selection of the internal complex polarization.

**Lemma:** Fix a quaternionic algebra `H_A`. Its stabilizer inside `G2` contains automorphisms rotating the imaginary 3-space of `H_A` (an `SO(3)` action). This action has no nonzero fixed imaginary unit `i∈Im(H_A)`. Consequently, the declaration point `A` alone does not provide a `G2`-equivariant preferred left-multiplication `J=L_i` and `H_A≅C_i²`; choosing one requires additional noninvariant/covariant data (e.g. a declared observer 2-form) or reduced stabilizer.

**Falsifier:** quaternionic conjugation by `j` maps `i→−i` (for orthonormal quaternion `i,j`) while preserving the underlying quaternion subalgebra. A supposedly basis-free invariant selector returning a fixed `i` cannot satisfy both. This is a gauge/choice warning, NOT a prohibition on creating a valid associated bundle with declared connection.

## GL55-07 — Canonical principal connection is mathematical transport, not a path-independent memory oracle

**Source:** SRC-0306 pp.102–111 differentiates base-space geodesics, horizontal lifts, and a desired associated fibre transport; pp.110–111 explicitly lists canonical connection construction as the next programme, not experimentally observed memory.

**General:** In the symmetric pair `g2=h⊕m` with `[h,m]⊂m` and `[m,m]⊂h`, the canonical principal `SO(4)` connection on `G2→G2/SO(4)` has curvature at the base point `F(X,Y)=−[X,Y]_h` (under the conventional sign). This is not identically zero: if `[m,m]=0`, then nonzero proper `m` would be an ideal of simple `g2`, impossible. Thus local connection has nonzero curvature and can have loop-dependent holonomy. Transport needs the actual declared path, connection and representation; returning to the same declaration does not ensure same transported state.

**Not implied:** Nonzero mathematical holonomy ≠ automatically physically measured memory; `Hol(γ)≠I` may still act trivially on particular state components/representations. Nor does the Levi-Civita connection on tangent `TM` specify a *unique observer-level phase or neural-port measurement*.

## GL55-08 — Conditional gradient/Lyapunov and Gate modes are distinct

**Primary:** SRC-0306 pp.99–101 eqs. (22)–(28) declares `dA/dτ=−κ grad L` and proposes residual-gated mobility `κ(R)` to model latching, then pp.108–109 suggests a proximal Gate criterion.

**Math:** For differentiable time-independent `L` and `κ≥0`, `dL/dτ=−κ||grad L||²≤0` along gradient flow. This proves descent under assumptions, not (a) convergence to a unique global selected declaration, (b) sudden re-declaration, (c) hysteresis, or (d) selected internal complex J. For a constant `L` the flow remains fixed for **any** positive large `κ(R)`; raising mobility cannot by itself generate new world selection. A hybrid jump rule, time-dependent/conditioned loss, explicit residual coupling and unique/controlled branch selection are separate mechanism obligations.

## Atlas, lineage and benchmark firewall

- Existing high-risk cards: RA-H03 (genuine later Purpose–Observer J construction but unproved ω genesis), RA-M01 / RA-R04 (operational quotient still requires fibre transition consistency), RA-H07 (connection ≠ empirical holonomy) and RA-O04 (physical interpretation boundary).
- Historical IDs W001–W400 preserved; W024 remains without authenticated proposition. `GL55-*` are compiler-labelled reconstructable claims/countermodels, NOT source-authored discovery priority or extra Proof Families.
- Distinguish source's already-recognized open problems from NEW precise compiler challenges. No Source Manifests or protected K1 40–44 changed; independent isolated model benchmark `NOT_RUN`.


---

# Imported original audit: `GENERAL_LEMMA_REGISTER_v5.6.md`

**Source audit SHA256:** `01622f1dd32e5077b24e0f4babdaba9dd65fe0ca4bf0816d7e6588553860f656`. Original record, no silent proof strengthening.

# v5.6 — Declaration Quotient, Rank Stability & Transport: Typed Proof Register

**Status:** primary-source anchored local mathematical proofs, counterexamples and proposed protocols. `GL56-*` are **compiler audit labels only**; they are not historical Witness IDs or new SMFT empirical discoveries. Source metadata and physical page references: `SOURCE_IDENTITY_AND_DEPTH_v5.6.json`.

## GL56-01 — Fixed linear kernel quotient works, but determines dimension by rank

**Source:** `SRC-0306` PDF physical p.610, eqs. (17)–(20): after obtaining a candidate alternating form `ω_BO`, proposes `V_op=V/ker ω_BO` and then a polar complex `J`. It already states nondegeneracy needs proof; this audit adds explicit dimensional typing.

**Proof (constant vector-space case):** for any alternating bilinear `ω:V×V→R`, let `K={v:ω(v,w)=0 ∀w}`. On `V/K`, define `ω̄([u],[v])=ω(u,v)`. Replacing `u` or `v` by a kernel vector changes nothing, so it is well-defined; `ker ω̄=0` by definition. Its rank is even (`2r`), so `dim(V/K)=2r`, and a positive metric on that quotient permits polar normalization to a complex structure. But the quotient is `C^r`, **not necessarily** `C²`.

**Counterexample:** on `V=R⁴`, `ω=dx₁∧dy₁`. Then `ker ω=span(∂x₂,∂y₂)` and `V/ker ω ≅ R² ≅ C`. The source's fixed linear quotient step is valid; claiming two complex channels without rank four would be invalid. **Links:** GL55-05, RA-H03, RA-O04.

## GL56-02 — State-varying rank need not admit a fixed-dimensional operational bundle

**Scope:** Source p.610 offers a pointwise linear quotient. It does not claim this suffices for a smooth state-dependent field; this is a conditional extension challenge.

**Countermodel:** `ω_t=dx₁∧dy₁+t dx₂∧dy₂` on `R⁴`. At every `t≠0` rank is 4 (`ker=0`, `C²`); at `t=0` rank is 2 (`ker` dimension 2, `C`). It is smooth in `t`, but `V/ker ω_t` changes dimension, so the quotients cannot form a fixed-rank vector bundle across zero.

**Proof obligation:** declare a constant-rank operating stratum or stratified transition/gate and dimension-change protocol. A rank threshold or fitted numeric singular values are not proof of an actual universal four-dimensional world.

## GL56-03 — Constant rank of a variable two-form does not guarantee an integrable kernel

**Premises:** a smooth alternating 2-form on a state manifold, not the single fixed bilinear form of GL56-01. For a smooth quotient manifold whose fibres coincide with the null distribution, the null distribution must be involutive (Frobenius).

**Explicit rank-two countermodel on `R⁴(x,y,z,w)`:**
`α=dz−x dy`, `β=dw−y dx`, `ω=α∧β`.
`ker ω=span(X,Y)` with `X=∂x+y∂w`, `Y=∂y+x∂z`.
Compute `[X,Y]=∂z−∂w`; then `α([X,Y])=+1`, `β([X,Y])=−1`. Thus `[X,Y]` is not in the kernel. This is a **constant-rank** two-form, but its kernel distribution is not involutive; no regular local quotient with these fibres exists.

**Repair:** a **closed** constant-rank two-form has involutive null distribution, since for null `X,Y`, `i_[X,Y]ω=−i_Y(L_Xω)=0` by `dω=0`. The local leaf quotient then inherits a symplectic form. A global smooth Hausdorff quotient is a *further* foliation condition. The source's finite-dimensional algebraic quotient remains correct and should not be retroactively branded as a false theorem.

## GL56-04 — A covariance eigengap gives a concrete *conditional* quaternionic selector

**New compiler proposal, not a claim that SMFT original sources proved this procedure.** `SRC-0306` p.90 proposes a residual/interaction-weighted selection objective but does not specify a global stability theorem.

Let `C∈Sym⁺(Im O)` be a **declared, measurable** 7×7 second-moment matrix with sorted eigenvalues `λ₁≥λ₂>λ₃≥...`; let `P` be the unique top-2 spectral projector, and `E=range(P)`. Any orthonormal `u,v∈E` generate the same quaternion algebra `H_E=span{1,u,v,uv}` (orientation reversal flips `uv` sign, preserving span). Thus a nonzero eigengap `δ=λ₂−λ₃` identifies a unique **data-conditioned algebraic declaration** (not a natural or causal one).

**Perturbation bound:** with `C'=C+E_noise`, let `Q` be any top-2 rank-2 projector for `C'`. By eigenvalue rearrangement, `tr[C(P−Q)]≥(δ/2)||P−Q||_F²`. Optimality of `Q` for `C'` gives `tr[C(P−Q)]≤tr[E_noise(Q−P)]≤||E_noise||_F ||Q−P||_F`. Therefore `||P−Q||_F≤2||E_noise||_F/δ`. This is a quantitative *subspace* robustness criterion for a declared covariance observer, not a claim that two noisy measured vectors automatically identify a physical world.

**Falsifier/guard:** when `λ₂=λ₃`, the top-2 plane is not uniquely identified; isotropic source ensembles of GL54-02 have no preferred quaternion algebra. The model can still fail Port closure, interaction fidelity or time-stable covariance.

## GL56-05 — Polar complex structure is not uniformly stable near rank loss

**Primary:** `SRC-0306` physical pp.389–401 and 610–612, `J=K(−K²)^(−1/2)`, conditional on invertible skew `K` and positive metric.

On Euclidean `R⁴` let `J₂=[[0,−1],[1,0]]`, `K_t=diag(J₂,tJ₂)`. For `t≠0`, `J_t=diag(J₂,sign(t)J₂)`. Yet `||K_t−K_{−t}||₂=2|t|→0`, while `||J_t−J_{−t}||₂=2`. At `t=0`, inverse square root is undefined. Thus **nondegeneracy at each separate state** does not yield a *uniformly robust* complex polarization across a near-degenerate regime. A positive minimum singular-value margin and source-declared branch/transport policy are required.

If dimension four remains fixed and spectral singular values stay bounded below, polar `J` varies continuously under regular perturbations. This is a qualified positive, not a universal no-go for Purpose–Observer `J`.

## GL56-06 — Operational order effect is measurable without automatically becoming a two-form

**Primary:** `SRC-0306` p.610 eqs. (15)–(17), and GL55-04. In a controlled finite-state differentiable model, measure both operator orders with identical initial state, matched perturbation sizes, and identical outcome definition.

For `B_ε(x)=x+εX(x)+O(ε²)` and `O_ε(x)=x+εY(x)+O(ε²)`, the **leading** order-difference of `O_ε∘B_ε` and `B_ε∘O_ε` is `ε²(DY·X−DX·Y)=ε²[X,Y]`, up to sign convention. This is an operational commutator **vector-field effect**, which may be nonzero and experimentally estimable. GL55-04 explains why a scalar `dL([X,Y])` is *not* automatically a pointwise tensorial 2-form.

**Proposed blinded experiment, NOT RUN:** pre-register observable `y`, intervention step `ε`, reset ability, order randomization, held-out states, statistical uncertainty; run B→O, O→B, B→B, O→O and ε/2 controls. Test leading `ε²` scaling, check hidden contextual state and order baseline. Separately construct a candidate local **bilinear tensor** and test pointwise linearity, skewness, rank, closedness and transport; only after these gates may GL55-05's polar `J` apply. Raw noncommutativity is not evidence of complex geometry.

## GL56-07 — Non-Abelian holonomy needs path ordering

**Source:** `SRC-0306` physical pp.327–328, especially (98) `Hol(γ)=exp(−∮_γ ω)` and (99) small-loop curvature heuristic. Those simple exponentials need a commuting/Abelian qualification when `ω` is a matrix-valued non-Abelian connection.

For two intervals with noncommuting constant generators `A` then `B`, transport is `exp(−B)exp(−A)`, generally **not** `exp(−A−B)`. E.g. choose nilpotent `A=[[0,1],[0,0]]`, `B=[[0,0],[1,0]]`; `[A,B]≠0` and the products differ. The precise general form is a path-ordered exponential `P exp(−∫_γ A)`. For an Abelian representation or pairwise commuting connection values, ordinary exponential is valid. This is a source-scoped *mathematical notation/condition repair*, not a physical holonomy observation.

## GL56-08 — Loop defect magnitude has a gauge and logarithm contract

**Source:** `SRC-0306` physical pp.327–328 eqs. (95)–(100) offers `||Log Hol||` as a semantic residual candidate.

Under a frame change at the loop base point, `Hol→S Hol S^(−1)`. The **conjugacy class** is intrinsic. For an orthogonal/unitary representation, Frobenius `||Hol−I||_F` is invariant; for general `GL` frame changes, raw Frobenius norm need not be. Example `Hol=diag(2,1/2)` conjugated by upper-triangular `S` acquires an arbitrary off-diagonal entry, changing `||Hol−I||_F`. In addition, matrix `Log` can be branch ambiguous even when the group element is fixed. A metric/repr, basepoint, branch and gauge-invariant readout must be fixed before calling this a measured residual.

**Boundary:** nonzero holonomy in a declared mathematical bundle proves neither a neural memory event, nor an unavoidable fifth regime, nor physical spin statistics.

## Mandatory cross-family gate and literature status

The general lemma chain is:
`observed order protocol → demonstrated (not assumed) tensor ω → rank/closedness/quotient checks → (g,ω) polar J → declared representation/connection → measured holonomy → interventional Port output test`.
Every arrow has separately listed assumptions. This is a proposed verification architecture, not a theorem that SMFT requires this entire chain. A fixed quaternion subalgebra declaration, observer state and complex polarization are different typed objects; none automatically creates an empirical Semantic Field or natural functional individual.

**Source depth:** SRC-0306 is 1,099 pages and remains *bounded-section reviewed*; supporting `SRC-0283`, `SRC-0261`, `SRC-0304` likewise sampled. No independent LLM reconstruction, real-world neural/physical trial or scientific priority claim added. W024 remains unresolved.


---

# Imported original audit: `GENERAL_LEMMA_REGISTER_v5.7.md`

**Source audit SHA256:** `37ca27a47a038a083342f4df37c53d97e295d0f3cd8e11724ce79725104d14ca`. Original record, no silent proof strengthening.

# v5.7 General Lemma Register — Epistemic Control and Operational Maturation

**Audit class:** bounded original-source mathematical checks; **not** validation of whole documents, deployed controllers or LLM research superiority. `GL57-*` are newly assigned *audit* nodes, **not** historical Witness, PF or Generative Move IDs. All PDF locations mean physical page count beginning at 1.

## GL57-01 — Predicted agreement ≠ beneficial control (PF10/PF04)

**Original:** `SRC-0130` physical p.23 §8.4 eqs (8.14–8.18), with deviation `δΞ=Ξ−Ξ*`, weighted improvement `ΔV=−δΞᵀW δΞ̇` and G4 acceptance `sign(ΔV_obs)=sign(ΔV_pred)`, `|ΔV_obs|≥κ_eff|ΔV_pred|`.

**Finite falsifier:** Scalar `δΞ=1`, `W=1`, `δΞ̇_pred=δΞ̇_obs=+1`, `κ_eff=.8`: both improvements equal `−1`. **G4 passes** even though `d(δΞ²/2)/dt=+1>0`, moving away from the target. This is a directional-safety defect *in the proposed gate*, not in the broader Ξ grammar.

**Repaired conditional gate:** (a) check `I_obs=−δΞᵀW δΞ̇_control_adjusted>0` (or reduction relative to a separately measured baseline), (b) require prediction sign/tolerance agreement, (c) declare positive-semidefinite W and control action admissibility. If the goal is improvement relative to baseline rather than absolute Lyapunov descent, compare counterfactual derivatives under paired baseline and treatment and **do not** call mere baseline improvement absolute stability. Need prospective controls and measurement error budget.

## GL57-02 — Low raw proxy variance is not coordinate validity (PF05/PF10)

**Original:** `SRC-0130` physical p.21 §8.1 eqs (8.2–8.3), p.18 §7.1 eq (7.2): a fixed protocol requires `Var_W(Ξ̂|P)≤ε` before gain estimation.

**Countermodels:** Valid exactly observed deterministic control coordinate `Ξ(t)=t` over a 100-tick window has large sample variance and fails this gate despite zero measurement error; a frozen sensor output `Ξ̂(t)≡0` has zero variance and passes despite being uninformative about a changing plant. Thus raw state variance is neither necessary nor sufficient for a reliable observation channel.

**Repair:** replace or supplement with repeated-measurement conditional variance `Var(Ξ̂|X=s,P)`, state-to-proxy calibration, sensor observability / sensitivity, within-regime drift test, explicit admissible nonstationarity. If a fixed-point operating window is *required*, record that as a narrower scenario assumption, not a universal criterion.

## GL57-03 — Covariance sign graph is not causal gain (PF08/PF10)

**Original:** `SRC-0130` pp.15–18 §6.3–7.2. The paper gives full-rank LS / pseudoinverse gain methods (6.11–6.15) and a fallback `S_ij=sign(cov(δΞ̇_i,δu_j))` (6.16), `I_ij` correlation dominance (6.17), followed by *independent single-channel pulses* (7.4–7.5).

**Adversarial design:** true response `y=u1−u2`; observe only naturally co-varying `u1=u2=z`. Then `y=0` and both covariance signs are zero, while causal partial derivatives are `(+1,−1)`. Its design matrix is rank deficient, so no observational unique gain exists. Distinct one-channel pulses `δu=e1` then `e2` recover both signs in the noiseless model.

**Bound:** retain covariance signs as *descriptive correlations*; causal gain estimation requires specified intervention / exogeneity plus sufficient excitation and protocol stability. Author's own one-channel MEP already motivates this; the correction is to resist promoting the shortcut into causal evidence.

## GL57-04 — Control channel dimensions do not imply controllability (PF10)

**Original:** `SRC-0130` pp.10–11 eqs (4.7–4.10), `Ξ̇_ctrl=B(Ξ,t)u`, `B∈ℝ^{3×4}`, four named intervention channels and three Ξ outputs. The author states channel dominance expectations are testable, not axioms.

**Rank falsifier:** `B=[[1,0,0,0],[0,0,0,0],[0,0,0,0]]`. From zero with drift zero, only first coordinate is movable; 3×4 dimensions alone prove nothing about reaching arbitrary Ξ*. Conversely full row rank of a constant `B` gives instantaneous control directions *if controls are unbounded and all channels admissible*, not automatically full nonlinear constrained reachability.

**Obligation:** record local controllability rank (and where appropriate linearized Kalman / Lie-algebra rank), actuator bounds, regimes, backreaction, and intervention legality before describing the interface as sufficient to control.

## GL57-05 — Event replay is ordered composition, not an unordered sum (PF11/PF05)

**Original:** `SRC-0237` physical pp.71–76 §9, formula `(9.7) maturation_history = Σ_k A_k`, accompanied by excellent typed event records including universe, coverage delta, decisions, residual and closure type.

**Type/ordering challenge:** Suppose event `A` sets `status=provisional` and event `B` sets `status=mature`. `A` then `B` ends mature; `B` then `A` ends provisional. The same unordered event multiset / ordinary algebraic sum cannot reconstruct both. The sum notation is defensible as an informal event-collection metaphor, **not** a replay theorem without event composition semantics.

**Repaired grammar:** declare a total or causally sufficient partial order with conflict semantics; replay `S_n=apply(A_n,…apply(A_1,S_0))`. Source hash and mutable/event authority are separate. Preserve the source's useful typed closure and near-miss retention instead of falsely declaring maturation impossible.

## GL57-06 — Complete coverage is orthogonal to truth (PF05/PF11)

**Original:** `SRC-0237` pp.57–61 gives `(7.5)` per-segment `c(σ)=(M,w,κ,ρ,a,t,conf)`, with coverage and residual separate; pp.72–74 define `robust|provisional|conflict_preserving|escalation_required` closure. pp.105–106 use operational `Promo=justified_promotions/total_promotions` but an external semantic oracle is not supplied.

**Counterexample:** Two text segments `σ1: 2+2=4`, `σ2: 2+2=5` can each be completely processed (κ1=κ2=1, no omitted segments). A closure algorithm blindly promoting both as mathematically true is inconsistent despite perfect coverage. Even preserved provenance or edit history does not imply the claims are correct.

**Repaired promotion contract:** `complete_source_coverage` AND `typed_closure` AND `claim_consistency/proof_or_oracle` AND `decision_authority`. Where the oracle is unknown, retain as hypothesis or conflict, and keep original contradictory data. Existing source's `conflict_preserving` is the right non-destructive branch; the unmet external correctness oracle must remain explicit.

## GL57-07 — Protocol-relative equivalence is not universal semantic identity (PF01/PF09)

**Original:** `SRC-0130` pp.12–14 §5 eqs (5.1–5.11) explicitly fixes P, operation envelope and tolerances ε when comparing Ξ dynamics; `SRC-0237` pp.51–55 §6 declares one active universe per assimilation event.

**Proof obligation:** If `π_P(x1)=π_P(x2)` under a probe family P, an enlarged probe family P' can separate them. Example hidden bit `h∈{0,1}`, old observer returns constant `0`, new probe returns `h`. Under P states are equivalent; under P' not. Thus 'same effective world' remains scope-indexed; cross-universe merged knowledge needs a typed bridge, not just synonym lookup.

**Preserved:** task-relative equivalence is a legitimate engineering concept; it is not proven ontological equality. Link to existing GL50 fiber factorization and RA-M01.

## GL57-08 — Kernelability is a proposed routing heuristic, not a verified score (PF05/PF11)

**Original:** `SRC-0212` pp.24–25,29–31 discusses ontology/operator/invariant reuse, causal consistency, version continuity and cross-reference density to decide whether to compile coherent local Kernels vs leave residuals in graph/RAG/raw. This is an AI conversation/exploratory proposal, **not** an independently measured industry benchmark.

**Countermodel:** A collection of near-identical documents copying the same false arithmetic assertion has high cross-references and operator-vocabulary coherence yet is epistemically unsound. A sparse collection may encode one valid but isolated theorem. Thus compression eligibility must not be identified with scientific truth, provenance or reconstruction quality.

**Operational option:** route by reproducible coherence features plus *separate* reconstruction-loss tests, explicit source-diversity checks, independent correctness challenge and negative controls. Do not certify industry uniqueness, adoption or superior LLM performance from source conversation alone. Preserve residual and uncompressed access.

## Global dependency boundary

`GL57-01,02,03,04` are typed conditions for `RA-E04`, `RA-M11`, and `RA-O08`; `GL57-05,06,08` constrain `RA-E16`, `RA-E10`, `RA-R10`, `RA-O05`, `RA-O08`; `GL57-07` connects interface typing to `RA-M01` without promoting a physics gauge theorem. No independent LLM benchmark, no real agent A/B effectiveness, no source-wide deep certification, and no new historical Witness ID.


---

# Imported original audit: `GENERAL_LEMMA_REGISTER_v5.8.md`

**Source audit SHA256:** `0a70aa9a61f3186a7e29103ee4ee78ca081408cf470bc6a68f15550e2d0bacf5`. Original record, no silent proof strengthening.

# v5.8 Component-Level Canonical Mathematics / Source-Challenge Register

**Scope:** 5 SHA-matched primary PDF members; identified pages only. `GL58-*`
are new local proof-audit identifiers, not historical Witness or newly discovered
scientific principles. Canonical applies only to exact declared model statements.

## GL58-01 — Endpoint iff saturated target (RA-M02, PF13)

Given `π:X→Y` and `T⊆X`, the visible rule `accept(x) iff π(x)∈π(T)`
recognizes exactly `T` iff `T=π⁻¹(π(T))`. Forward: the accepted set is
exactly the preimage. Reverse: equality makes the rule correct.
Countermodel: valid `(answer,authorized)` and invalid `(answer,unauthorized)`
share the answer, hence the endpoint is insufficient.
**Primary original:** `SRC-0234` PDF physical pp.134–136, Appendix G.
**Forbidden implication:** Endpoint sufficiency does not certify intermediate
permission, causal port closure or agent safety without the stated target.

## GL58-02 — Ternary skew-product complete-cycle theorem (RA-M03, PF10)

On `F₃²`, let `T_f(a,b)=(a+1,b+f(a)) mod 3`.
Then `T_f³(a,b)=(a,b+S)` where `S=f(0)+f(1)+f(2)` modulo 3.
If `S=0`, the first coordinate forces every period to be 3, so there
are three disjoint 3-cycles. If `S≠0`, `T_f³` translates b by a nonzero
element of `F₃`, returning only after three such sweeps. Thus every state
has period 9, giving a single 9-cycle on the 9 states.
**Independent brute-force:** all `3³=27` functions checked; 9 with S=0
produce length 3, 18 with S≠0 produce length 9.
**Primary original:** `SRC-0306` physical pp.805–806,839–840.
**Forbidden implication:** finite construction does not derive a specific
LuoShu grid, selected physical cycles or P8D ninefold necessity.

## GL58-03 — Affine order-9 obstruction (RA-M04, PF10)

`AGL(2,3)` has 48 invertible 2×2 matrices and 9 translations.
A hypothetical affine permutation of order 9 has a 3×3 homogeneous
representation `M` over `F₃` of 3-power order. Then `M=I+N` unipotent,
`N³=0` (nilpotent 3×3) and `(I+N)³=I` in characteristic 3, contradicting
order 9. Enumerating all 432 maps verifies possible orders exactly
`{1,2,3,4,6,8}`.
**Primary original:** `SRC-0306` pp.803–804,839.
**Forbidden implication:** This does not exclude nonlinear 9-cycles, and
a nine-state set alone does not specify a dynamics.

## GL58-04 — Magic-square premises and history of reverse construction

`SRC-0107` PDF physical pp.7–9 assumes nine distinct positive labels,
magic sum 15, and equates slot capacities with those labels. Classical
uniqueness under those assumptions concerns arrangements, not semantic
necessity. Translation of each label by +1 preserves magic-square lines
while changing their sum to 18 (hence uniqueness cannot hold without
fixing the label set/sum). Given the fixed multiset {1,…,9},
`H=-Σ(s_i/45)log(s_i/45)` depends only on the multiset, not on placement;
therefore entropy cannot select the LuoShu square from permutations.
`SRC-0306` p.839 **expressly** says its quadratic flight is reverse
engineered from a known trajectory, not derived from P8D.
**Preserve:** the finite carry theorem and the valuable residual/carry
mechanistic conjecture as separate propositions.

## GL58-05 — Research reconstruction and collider evidence ladder

`SRC-0006` PDF physical pp.120–121 distinguishes H_R (research-history
representation), H_X (stable reconstruction) and H_U (practical utility).
H_R alone entails neither H_X nor H_U. `SRC-0007` pp.89–92 explicitly
identifies memorized domain bridges, culturally common attractors, prompt
leakage and shared lineage as null explanations for recurrence.
**Proof obligation:** independent held-out reconstructors versus matched
baselines (same task, exposure budget), then a measured downstream utility
evaluation. Neither a package hash nor self tests count as such trials.

## Global publication rule

Do not change a whole RA card to `fully verified` when only a component is
proved; do not assign compiler proof originality to a historical primary
source; record source pages and whether theorem was reverse-engineered.
No independent model, domain or physics efficacy experiment was executed.


---

# Imported original audit: `GENERAL_LEMMA_REGISTER_v5.9.md`

**Source audit SHA256:** `4cc229ef1067854a0184aea530948dc366d48f9f0e6a179651b8747ef249274f`. Original record, no silent proof strengthening.

# v5.9 Component-Level Theorem Certification: Behavioral Quotient, Port and Mind-Seal

**Audit status:** Four original primary PDF members SHA-256 matched to 325-row Source Manifest. Reopened specified page ranges only; no entire original source was completely deep-reviewed. GL59 IDs are compiler audit nodes, NOT historical Witness IDs, discoveries of the author, or external model observations.

## GL59-01 — Coarsest exact behavioral quotient (reconstructed model theorem)

**Source:** `SRC-0283`, physical PDF pp.8–10, 55–56; `SRC-0261` pp.5–6. Let `X` be a nonempty fixed domain, `U` a shared globally admissible action alphabet, and `F_u:X→X` total deterministic maps, with task output `o:X→Y`. Define `x≈y` iff `o(F_w(x))=o(F_w(y))` for *every finite action word w*, including the empty word. Then ≈ is an equivalence relation and is forward invariant: if x≈y, for any u and w, `o(F_w(F_u(x)))=o(F_{(u,w)}(x))=o(F_{(u,w)}(y))`. Hence output and all transitions descend to `X/≈`. For any exact quotient π preserving both output and each F_u, `π(x)=π(y)` implies x≈y by induction on words. Thus ≈ is the **coarsest exact** (least distinguishing) output-and-transition quotient, unique up to bijection of quotient states. This theorem is conditional on the explicitly fixed protocol; it does not determine natural neural attractors or a canonical factorization independent of `U,o`.

**Qualification:** If eligibility/action availability varies by state, include `A(x,u)` among preserved outputs and handle partial dynamics with a declared legal-word semantics. Do not pretend every sequence is admissible from every state. `SRC-0261` pp.5–6 makes legal-domain closure an explicit condition.

## GL59-02 — Finite-depth agreement does NOT define exact dynamics

**Source:** `SRC-0283` pp.14–15, definition of `≈_H` and its provisional status. **Compiler countermodel:** X={0,1,2,3}, U={a}, F(0)=1,F(1)=2,F(2)=3,F(3)=3; outputs o(0)=o(1)=o(2)=0,o(3)=1. States 0 and 1 share their output and output after one step, so `0≈_1 1`. But F(0)=1 and F(1)=2 lie in different `≈_1` classes because after one further step o(F(1))=0 and o(F(2))=1. Also `o(F²(0))=0≠1=o(F²(1))`. The quotient by `≈_1` has **no well-defined one-step transition**, even though its one-step *observational* comparisons have passed. This is not a contradiction of the original, which explicitly calls finite-depth frames provisional.

## GL59-03 — Full finite-state partition refinement is a canonical algorithmic component

**Sources:** `SRC-0283` pp.9,14–15,45–46; `SRC-0261` pp.6,15. In a fully known deterministic N-state system under total U, start with the output partition `P0`. Iteratively split each block by the signature `(o(x), ([F_u(x)]_{P_k})_{u∈U})`. Then `P_k` coincides with horizon-k behavioral equivalence. Once a round makes no splits, forward congruence holds and no later split is possible. Each strictly refining round increases number of blocks by at least 1; therefore at most `N-|P0|` strict refinements, and the exact quotient is reached after at most N−1 refinements. A stopped finite-horizon computation is a rigorous certificate **only if a full successor-signature stability round has been checked**. The bound is not for unknown/infinite/neural state spaces.

## GL59-04 — Number of distinguishable classes gives a bit lower bound, not a real-coordinate lower bound

**Sources:** `SRC-0241` p.23, original *qualitative* Mind-Seal compression claim; `SRC-0283` p.9 exact behavioral classes; `SRC-0261` p.6 joint port tests. Suppose the finite protocol has M distinct ≈-classes and a deterministic exact sufficient code `ζ:X→C`, preserving all allowed future outputs. Then `ζ(x)=ζ(y)` implies x≈y; otherwise some future action word distinguishes them, contradicting sufficiency. Hence `|ζ(X)|≥M`. Any fixed-length *binary* record needs at least `ceil(log₂ M)` bits; the quotient label attains this cardinality bound (assuming no additional process metadata/constraints). The claim **does not prove** a minimum number of continuous real coordinates: a single exact real coordinate can encode arbitrarily many finite labels. Under finite precision, smoothness, robustness or runtime enforcement, new constraints apply and must be declared.

## GL59-05 — Port sufficiency is independent of task correctness

**Source:** `SRC-0261` PDF physical pp.5–6, mathematical M3 and limitations; `SRC-0241` pp.22–24. An exact singleton code suffices when the system always produces the same (wrong) answer; its output is perfectly predictable but incorrect. Conversely, if a proposed candidate π merges states with distinct task-required later outputs, a full-state controller can still compute correct answers without using π. Thus correctness≠candidate-Port-sufficiency. This justifies separate gates for behavioral preservation, task scoring, permission enforcement and endogenous formation.

## GL59-06 — Observer trace probability is not evidence for physical collapse

**Source:** `SRC-0123` pp.6–9,27–28. If each history-indexed outcome map K_k is a measurable probability kernel, its normalized finite-cylinder laws extend to a unique trace probability law via the standard Ionescu–Tulcea theorem. For realized history filtration `F_k=σ(φ₁,...,φ_k)` the conditional law of an already observed φ_j, j≤k, is almost surely a point mass at its realized value. This is **filtration measurability**, not a new physical quantum reduction or observer-specific causal law. If adaptive context/policy affects future kernels, current outcome alone need not be sufficient: the policy's relevant history/memory must be represented. The finite stochastic model's trace law is mathematically meaningful and stays a different type from semantic/neural observables.

## GL59-07 — State-dependent eligible actions require typed protocol or partial semantics

**Sources:** `SRC-0283` pp.8–10 and Appendix B (admissibility must descend); `SRC-0261` pp.6,10. Let X={x0,x1}, π(x0)=π(x1)=p, current visible output identical; only x0 permits a controlled act u. No port-only controller can determine legality of u from p because any `A_Z(p,u)` would have to equal both `A(x0,u)=1` and `A(x1,u)=0`. Even if transition and output factorization agree for common legal moves, legal-action factorization fails. Include eligibility in o or as a separate required port factorization condition before certifying a runtime-safe effective controller. This is a typed interface condition, not proof that neural natural objecthood exists.

## Component certification decision (v5.9)

- **RA-M01:** `MODEL_THEOREM_COMPONENT_VERIFIED_V59`: exact future-behavior quotient, fixed domain/action semantics and unique coarsest quotient; finite-state refinement with witnessed stability. Not the entire cross-domain card.
- **RA-E11:** `COMPILER_DERIVED_CONDITIONAL_BOUND_V59`: fixed-bit cardinality lower bound derived by the compiler, correcting original qualitative claim. No empirical transfer/compression advantage certified.
- **RA-M12:** `SOURCE_RECONSTRUCTED_STANDARD_MEASURE_THEOREM_V59`: accepted as standard conditional kernel construction only; not independent observer ontology or scientific experimental validation.
- **RA-M11 / RA-E14 / RA-R04 / RA-R08:** strengthened original-source boundary; no newly certified natural AI individual.
- **Old certifications RA-M02/RA-M03/RA-M04 stay unchanged**, on original local conditions.

**Caveats:** no genuine independent model, no fresh Transformer intervention, no whole-source certification, no claim about consciousness or natural semantic dynamics. W024 unresolved. These results are an example of component-level source-grounded formalization and existing-theorem reuse, not credit assignment for newly discovered theorems.
