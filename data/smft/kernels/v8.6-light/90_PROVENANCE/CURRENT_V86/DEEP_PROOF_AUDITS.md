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


---

# Imported v6.1 source-scoped audit (new compiler nodes)

# v6.1 — Five-Source Semantic-Time and Observer-Measure Proof Audit

**Scope.** All primary SHA-256 references match the immutable 325-entry Manifest. PDF physical page numbers start at 1. This is targeted source mathematical audit and historical-development qualification, **not entire document reading** and not empirical confirmation of SMFT or an independent LLM blind test.

## GL61-01 — Incorrect complex-time differential operator in SMFT Rev1

**Original source.** `SRC-0270`, PDF physical p.4, §1.3, eq. (1.2), explicitly defines `ζ=τ+iT` then sets `∂Ψ/∂ζ = ∂Ψ/∂τ+i∂Ψ/∂T`.

**Finite falsifier.** With `f(τ,T)=τ+iT=ζ`, the correct complex derivative is `df/dζ=1`, while the source RHS yields `1+i(i)=0`. Thus the displayed operator cannot be `∂/∂ζ` with the standard complex structure.

**Conditional repair.** For `C^1` functions of independent real coordinates `(τ,T)` use Wirtinger operators `∂_ζ=(∂_τ−i∂_T)/2` and `∂_{bar ζ}=(∂_τ+i∂_T)/2`. For holomorphic functions the second equals 0. If semantic `T` is merely an auxiliary coordinate or no analytic continuation exists, the model must define a different directional operator by name and provide its own meaning; the original equation is not a standard chain rule.

**Preserved.** A complex *coordinate* can be introduced as a modeling convention. The SSLE on real `τ` in §1.4 is a separate phenomenological model and does not depend on the erroneous formal identity for its symbolic definition.

**Atlas:** RA-H01, RA-R06, RA-O01. **Evidence:** source-reopened local mathematical counterexample, not a physical time law.

## GL61-02 — POVM completeness requires normalized input state

**Original.** `SRC-0270` PDF physical p.6, §2.2, Theorem 2.5, and p.57 Appendix B. Given `E_φ=O_φ†O_φ` and `Σ E_φ=I`, source states `Σ Pr(φ|ψ)=1`. It implicitly uses `⟨ψ,Iψ⟩=1` in the proof.

**Theorem with full premises.** For any Hilbert-space vector `ψ`, `Σ_φ ||O_φ ψ||²=||ψ||²`. Thus the probabilities sum to 1 **if** `||ψ||²=1`. For a density operator `ρ` with `Trρ=1`, `Σ Tr(E_φ ρ)=1` if effects sum to `I` and are positive. For any outcome with strictly positive probability the normalized Kraus update `O_φψ/||O_φψ||` is well-defined.

**Counterexample.** On one-dimensional `ℂ`, take `E_1=I` and `ψ=2`. The resulting weight is 4, not a probability; source condition `Σ E=I` alone is insufficient. Also mere nonnegative semantic intensity need not be a measurement outcome law without a normalized measurement instrument.

**Preserved.** The intended normalized quantum-inspired measurement theorem is correct when the omitted state normalization is specified. It does not prove biological/neural semantic collapse.

**Atlas:** RA-H01, RA-M12, RA-O01. **Depends on:** `GL52-04`, `GL52-05` only by scope/normalization relation; different underlying dynamics.

## GL61-03 — Model lineage: recursion order is not a universal source of time

**Original source sequence within the documents** (historical conceptual relation, no unverified first-publication claim):

- `SRC-0263` PDF pp.1–3,11–13 proposes primitive recursive-generation dependency as *proto-causality*. It explicitly calls the idea a thesis, **not a theorem**.
- `SRC-0266` pp.2–3 critiques recursion as potentially a presentation or construction order, not ontological genesis; p.23 and p.46 proposes viewpoint-selected filtration with ledgered trace as a more general model.
- `SRC-0265` pp.1–2,15,45,51–53 adds Declaration, admissibility Gate, trace and residuals; p.52 explicitly differentiates **event order from causal dependency**. `SRC-0264` pp.1–4 continues the self-revising declaration program, without retroactively validating the earlier proto-time ontology.

**Mathematical separation.** An operation-expression DAG induces a partial dependency order on its nodes, not a unique scalar duration, globally canonical total order, physical metric or interventional causal relationship. Independent subexpressions need no ordering. E.g., two independent leaves `a` and `b` can be evaluated in either order without changing `f(a,b)`; no unique historical clock follows from the mathematical tree alone.

**Conditional result.** A declared policy can select a linear extension/timestamped ledger and produce an *operational* order. But it is external protocol information, not intrinsic inevitability. For causal claims, an intervention or a domain-specific dependency mechanism is needed; observational precedence is insufficient (as `SRC-0265` itself recognizes).

**Atlas:** RA-H01, RA-H05, RA-R06, RA-O01; epistemic relation `REVISED_BY` versus `DERIVES`.

## GL61-04 — Trace update recurrence alone does not prove irreversible history

**Original.** `SRC-0265` PDF p.45 gives `L_{k+1}=UpdateTrace_P(L_k,τ_k,R_k,GateMeta_k)`; p.52 uses an unqualified `TraceUpdate ⇒ irreversibility` (8.30) and the thesis of an ordered irreversible ledger (8.42).

**Falsifier.** Take a valid update `U(L,e)=L+[e]` and a later allowed reset `Reset([e])=[]`. The system can return to the same materialized state. More directly, `U(L,e)=e` overwrites its previous state. A recurrence `L_{k+1}=U(L_k,e_k)` does not prevent either. Thus a timestamp, a ledger label or an update equation alone cannot make history irreversible.

**Qualified engineering theorem.** If event records are persistently append-only, cannot be erased by authorized actions, timestamps/identity are authenticated and replay semantics preserve order, the stored *event history* is monotone with respect to its prefix partial order. Even then the application state can be logically reverted by appending a compensating event; append-only persistence is not identical to a thermodynamic arrow of time or a formal theorem of physical irreversibility.

**Atlas:** RA-E05, RA-H05, RA-R07, RA-O08. **Related:** `GL57-05`, `GL57-06` on ordered event replay and external truth; do not infer all traces are tamper-proof.

## Cross-source boundary

`SRC-0270` and `SRC-0263` are genuine source statements; `GL61-*` are new *compiler mathematical/audit nodes*, not new original Witnesses W401+. The late-source filtration/declaration program deliberately revises the earlier recursive-pre-time analogy. Retain the early creative hypothesis as historical generative content, but mark its claimed universality and physical implication open. Prior four conditional model theorem components RA-M01..RA-M04 remain unchanged; no new scientific component is promoted.


---

# Imported v6.2 source-scoped audit (compiler GL62 nodes)

# v6.2 — Source-Specific SMFT Foundations Mathematical Audits

Scope: `SRC-0270` selected PDF physical pp.4–8,12–16,57–59, crosschecked with
`SRC-0271` selected pp.15,21–22,27–28 and `SRC-0268` pp.2–3,10 as
historical/related formulations. Original member SHA-256 values exactly match
`90_SOURCE_MANIFEST.csv` (see `SOURCE_IDENTITY_AND_DEPTH_v6.2.json`).
No whole-original review, physical experiment, neural observation, or independent LLM trial.
The four `GL62-*` labels are **new compiler audit nodes**, not W401+.

## GL62-01 — Pinsker does not yield a KL attention-cost lower bound

**Source assertion:** `SRC-0270` p.15 Theorem 5.3 (5.2), p.58 B.3 (B.4–B.5):
`W_c >= κ1 TV(Q,P)^2 >= κ2 KL(Q||P)` for fixed positive κ1,κ2, claimed from
Pinsker/log-sum; normalization, θ-Lipschitz actuation.

**Countermodel:** `Q=(1/2,1/2)` and `P=(ε,1−ε)`, ε→0+. Total variation
`δ=|1/2−ε|<=1/2`, whereas
`KL(Q||P)=1/2 log(1/(4 ε(1−ε)))→∞`.
No positive *global* κ2 can satisfy `κ1 δ²>=κ2 KL` on all such pairs.
The actual Pinsker direction is `δ²<=KL(Q||P)/2` (for natural logarithms).
This cannot be reversed without restricting probabilities away from zero and
proving an *upper* KL/TV relation under the additional restrictions.

**Preserved conditional result:** If a task-specific action model *independently*
establishes quadratic work `W_c>=c δ²`, retain that as a candidate restricted
lower bound. Instrument POVM normalization and θ-Lipschitz alone do not
specify its actuator-work coefficient or prove an entropy-sharpening bound.
`W_c>=κ3 ΔH` (source Corollary 5.4) remains an unproved, separately calibrated
claim; do not infer it from the invalid displayed chain.

**Atlas:** RA-H01, RA-O01. **PF:** PF07, PF10. **Class:** SOURCE-FALSIFIED INEQUALITY
plus retained conditional control-cost design.

## GL62-02 — Compatible / commuting POVMs need not agree in marginals

**Source assertion:** `SRC-0270` pp.7–8 Theorem 2.14, p.13 Theorem 4.5 (4.3),
pp.57–58 B.2 imply equality of observers' marginals from commuting/joint POVM
and normalized instruments (with an admissible frame map).

**Finite countermodel:** Hilbert space ℂ², state `ρ=|0><0|`.
`E^A_0=|0><0|`, `E^A_1=|1><1|`,
`E^B_0=|1><1|`, `E^B_1=|0><0|`; all effects commute, POVMs are
complete and positive, and the joint PVM exists. Yet
`Pr_A(0|ρ)=1` and `Pr_B(0|ρ)=0`.
This case also satisfies the source's unitary frame conjugation using Pauli
X, which swaps labels, but the state ρ was **not** co-transformed and no
explicit outcome relabeling reconciled propositions.

**Repaired statement:** Compatibility permits joint measurement, not equal
marginals. To assert equal probabilities for all density matrices ρ, require
`E^B_{mapped φ}=E^A_φ` after declaring a *same proposition* and mapping,
or compare `Tr(U E^A_φ U† · UρU†)=Tr(E^A_φ ρ)` with both the effect
and state jointly transformed by a unitary U.
For a given state, direct trace equality suffices. Independently, commuting
observables do **not** imply statistical independence of the joint law.

**Atlas:** RA-H01, RA-M12, RA-O01. **PF:** PF01, PF02.

## GL62-03 — Anti-Hermitian H is not the conservative generator in i∂ψ=Hψ

**Source assertion:** `SRC-0270` p.7 Proposition 2.12: if observer coupling
is norm-preserving on average and `H_s` is **anti-Hermitian**, the wavefunction
norm is conserved between collapse ticks. This contrasts with the standard
Schrödinger sign convention of its p.4 equation (1.3).

**One-dimensional countermodel:** take ℏ=1, H=iI (so H†=−H), observer term=0.
`i ψ_dot = i ψ` implies `ψ(t)=e^t ψ(0)`, so
`||ψ(t)||²=e^{2t}||ψ(0)||²` is not conserved.

**Repaired condition:** For a densely defined self-adjoint H in the
well-posed Hamiltonian regime, `U(t)=exp(−itH/ℏ)` is unitary and norm preserving.
For differentiable solutions with extra term N, the exact balance is
`d||ψ||²/dt = (i/ℏ)<ψ,(H†−H)ψ> + (2/ℏ) Im<ψ,N(ψ)>`.
With self-adjoint H and an N whose imaginary expectation is zero (pathwise),
norm is constant. A claim merely of mean-zero leakage supports at best an
**expectation-level** norm balance if precisely defined, not conservation of
every trajectory.

**Preserved:** The p.5 linear limit with a self-adjoint Laplacian and real V
can have genuine unitary evolution under declared boundary conditions.
`SRC-0268` §SSLE loss/drive is a separate non-conservative phenomenological
model; no contradiction with explicitly designed dissipative dynamics.
**Atlas:** RA-H01, RA-M12, RA-O01. **PF:** PF02, PF10.

## GL62-04 — Frame covariance and joint distributions have distinct prerequisites

**Source:** `SRC-0270` p.12 eq. (4.1), p.13 eq. (4.3), pp.57–58 B.2.
The unitary coordinate transformation identity is
`Tr(U E U† · UρU†)=Tr(Eρ)`; if only E is transformed while ρ stays fixed,
there is **no** general equality. Normalization under `E' = U E U†` also needs
`ΣE'=UU†=I`; an arbitrary nonunitary U does not satisfy this in the usual
finite-dimensional square representation.

**Separate countermodel to “joint law factorizes for commuting effects”:**
let `ρ=(|00><00|+|11><11|)/2` on two bits, and measure each bit in the
computational basis. All effects commute. Marginals are Bernoulli(1/2),
but the joint has `P(00)=P(11)=1/2`, `P(01)=P(10)=0` rather than `1/4`
independent cells. Joint measurability is strictly weaker than independence.

**Repair:** Distinguish three typed properties: `JOINT_MEASURABLE`,
`COVARIANT_WITH_JOINT_STATE_MAP`, and `EQUAL_MARGINALS_FOR_MATCHED_PROPOSITIONS`;
add `INDEPENDENT_JOINT` only under an actual product-state or decorrelation
premise. The strong observer-consensus claim remains hypothesis without
matched, calibrated outputs and independent domain-specific tests.

**Atlas:** RA-M12, RA-H01, RA-O01. **PF:** PF01, PF02, PF05.

## Cross-source proof and hypothesis boundary

These local audits challenge equations and theorem prerequisites of a specific
formalization. They do not falsify the overarching SMFT research programme,
confirm physical observer collapse, or measure actual neural semantic fields.
`SRC-0271` supplies earlier SSLE and observer-history language; `SRC-0268`
contains subsequent domain-directed loss/drive; the selected passages do not
establish which source is a first chronological discovery. Existing
RA-M01..M04 model-only certification is unchanged. W024 remains reserved.


# v6.3 — source-scoped observation and creative research design

## GL63-01 — A recorded event does not ensure its next experimental repetition

**Source assertion** `SRC-0245` Theorem 4.3 physical pp.11–12: a frame mapping, commuting effects and accessible trace of observed event imply that B's mapped outcome is delta-certain. This conflates certainty about A's recorded historical fact with certainty of a **new** B measurement.

**Exact CP-instrument countermodel**: Hilbert space ℂ²; let `P0=|0><0|`, `P1=|1><1|` and `|+>=(|0>+|1>)/√2`. Let A's instrument be `M_i(ρ)=Tr(P_iρ)|+><+|`, a legitimate positive, trace-nonincreasing measure-and-reprepare instrument whose sum is trace preserving. Start with `ρ=|0><0|`, so A's outcome i=0 has probability one, is durably recorded and readable by B; the measured effects are `{P0,P1}`. Let B **re-measure the identical PVM** `{P0,P1}` after A's re-preparation. Same proposition, identity frame mapping, commuting (indeed identical) effects, shared trace all hold, but `Pr(B=0 | recorded A=0)=<+|P0|+>=1/2`, not 1.

**Precise repair**: `Pr(record_A=0|F_B)=1` if B's sigma algebra includes that historical record; do not replace the random variable `record_A` by a new `outcome_B`. For repeat measurement require nondemolition/repeatable instruments (`P_i ρ_i P_i=ρ_i` for post-state conditional on i), correct outcome matching and measurement ordering, or explicit conditional joint law `Pr(B=m(A)|A)=1`. Compatibility alone supplies neither. In certain genuinely shared classical-record protocols the history claim is valid and useful. **Atlas** RA-M12, RA-H01, RA-O01. **PF** PF01/PF02.

## GL63-02 — A past-algebra fixed point need not have state probability one

**Source assertion** `SRC-0245` §6.1.4 physical pp.17–18: for any event `E∈F_j` at time k≥j, conditional expectation `E_k(E)=E` **and** `ρ_k(E)=1`. First equation is standard algebraic measurability identity; second is false for an arbitrary event in the past algebra.

**Minimal counterexample**: let `X∼Bernoulli(1/2)`, `F=σ(X)`, and the event `E={X=1}∈F`. Then `E[1_E|F]=1_E` almost surely, while `P(E)=1/2`, not 1. To achieve certainty, condition on the *actually realised event*, e.g. on `{X=1}` (where well-defined with positive probability), and distinguish conditioning on a realised record from the unconditional state `ρ_k`. Also, a conditional expectation into a von Neumann subalgebra requires suitable existence/state-preservation assumptions in general, not just notation.

**Preserve** trace-measurability and filtration retention, not the unconditional probability-one claim. **Atlas** RA-M12, RA-O01. **PF** PF01.

## GL63-03 — Noncommuting unsharp quantum effects can be jointly measurable

**Source assertion** `SRC-0245` §7.2 physical p.20 says noncommuting effects imply no joint POVM; its displayed *sharp rank-one projection example* is indeed incompatible. The general statement about **all effects** is too strong.

**Constructive countermodel**: take `η=1/2` (more generally `0<η≤1/√2`) and Pauli σx, σz. Define `E^X_a=(I+aησx)/2`, `E^Z_b=(I+bησz)/2`, `a,b∈{−1,+1}`. Effects across X/Z do not commute: `[E^X_+,E^Z_+]=η²[σx,σz]/4 ≠0`. Yet `G_{ab}=(I+aησx+bησz)/4` is positive since eigenvalues `(1±η√2)/4≥0`; `Σ_b G_{ab}=E^X_a`, `Σ_a G_{ab}=E^Z_b` and `Σ_abG_ab=I`. Thus both POVMs are jointly measurable despite noncommuting effects.

**Repaired claim**: commuting POVMs imply joint measurability (in the standard effects setting); noncommutation does not by itself exclude it for unsharp measurements. Noncommuting sharp PVMs generally are not jointly measurable. Neither property guarantees *matching outcomes*. **Atlas** RA-M12, RA-O01; **PF** PF02.

## GL63-04 — SBS gives conditional redundancy, not arbitrary exponential consensus

**Source assertion** `SRC-0245` Theorem 4.4 physical p.13 promises `Pr(φ_i=k)→1` and exponentially decaying pairwise disagreement as number m of environment fragments grows under exact/approximately distinguishable SBS, without specifying decoder or how individual observer signal-to-noise improves with m.

**Quantifier guard**: if latent pointer `K∈{0,1}` is random and each ideal fragment copies it perfectly, then `Pr(Y_i=K|K)=1` but unconditional `Pr(Y_i=0)=Pr(K=0)` need not approach 1 for any fixed 0. Moreover, for approximately distinguishable fragments with independent per-observer binary readout errors `e∈(0,1/2)` held fixed, `Pr(Y_i ≠ Y_j | K)=2e(1−e)` for each *fixed pair* i,j, independent of number m of other fragments. This can be realised with nonorthogonal pointer-conditional fragment states or their classical commuting analog. Mere addition of noisy fragments does not improve a single observer's local decoder.

**Repaired positive statement**: for exact orthogonally encoded pointer fragments and faithful pointer decoding, agreement between separate observers is already exact for every m (conditional on the shared K). For noisy copies, a *new assumption* that each observer obtains r independent fragments of accuracy >1/2 permits majority-vote concentration `Pr(error)≤exp(−2r(1/2−e)²)` by Hoeffding; r is an observer's *aggregated sample size*, not the global number m automatically. A quantum Chernoff argument likewise requires explicit discrimination tasks/sample scaling. **Atlas** RA-M12, RA-H01; **PF** PF02/PF05.

## GL63-05 — Research-critique, residual generation and optional Attractor lens need factorial falsification

**Source anchors** `SRC-0298` pp.3–7,14–16,23–27 explicitly demands baselines, one-functional-component interventions where possible, ablations, effect thresholds, failure gates and research-world benchmarks. `SRC-0299` pp.3–8,13–18 separates hypotheses/no-gos/superseded interpretations. `SRC-0258` pp.1–7 distinguishes protocol-compiled proxies from direct empirical LLM mechanism claims; `SRC-0252` pp.4–5,7–8,11 provides engineering candidates, not a matched validated improvement for an Attractor-augmented kernel.

**Compiler design, NOT an observed gain**: Every proposed conflict repair must output `{claim ID, quantifier domain, source locator, minimal countermodel, repaired conditional version, residual, discriminating test}`. Each analogy-guided proposal must supply a type mapping and an explicit failed analogy/negative control. For creativity assessment hold model, token and retrieval budgets fixed; cross external fields and unseen corpora; preregister evidence/rubric, sample alternatives without Attractor mathematics, and compare four conditions: A generic literature-review baseline, B + versioned Kernelization, C + independently labelled Attractor module, D + randomized/balanced human-analogy prompting. An optional 2×2 factorial `Attractor(on/off) × Analogy(on/off)` within constant compiler B can isolate interaction effects rather than conflating C vs D. Evaluate valid contradiction detection, repair soundness, reproducible downstream hypotheses, novelty with independent prior-art checking, false positives and calibration; source-matched blinded graders needed.

**Residual admission gate**: a generic paper-review criticism is NOT an open mathematical conjecture until an exact residual predicate/test is specified. A compelling analogy is NOT proof of mechanism, and a literature co-occurrence is NOT causal dependence. Negative results may yield a positive repaired theorem as in GL63-01..04, but no real LLM creativity improvement is inferred from these toy constructions. **Atlas** RA-H10, RA-O05, RA-O08, RA-R10; **PF** PF04/PF05/PF11.


---

# Added original scoped audit: `GENERAL_LEMMA_REGISTER_v6.4.md`

# v6.4 — Positive Joint Port / Attractor / Observer / Residual Bridge, plus Finite-Step Gate Repair

**Evidence scope:** Original TAR members `SRC-0130` physical pp.20,23–24; `SRC-0261` pp.6,10,12,14,22,28; `SRC-0298` pp.7–9,14–15,19; `SRC-0299` pp.4,6–7,11,13,16,18,20,25; `SRC-0129` pp.16,23; `SRC-0252` pp.5,8,13,17. The six original PDF bytes were checked against immutable SHA-256 manifest entries. Rendered and visually checked source PDF `SRC-0130` physical p.23. This is targeted reading, not full-document certification. All GL64 formulas below are **new compiler-authored conditional results/countermodels**, inspired by source-defined functional roles; no claim that source authors established these exact theorems, no empirical AGI verification or independent LLM reconstruction.

## GL64-01 — Approximate controlled Port closure plus contraction gives finite-horizon error certificate

**Source anchors:** `SRC-0261` p.6 (exact fiber-factorization / joint output), pp.10,14 (synthetic attractor residual and open protocol limits); `SRC-0299` p.7 (residual magnitude vs direction), pp.13,25 (typed core and causal arrows). Prior exact math: GL50-01/02, GL59-01. **This is not the same as proving the natural existence of a Functional Port.**

Let `q:X→(Z,d)` be the declared Port and let the actual controlled state evolve `x_{t+1}=F_{u_t}(x_t)`. The candidate effective system evolves `z_{t+1}=G_{u_t}(z_t)`. Assume **the identical declared open-loop control sequence** `u_t` is supplied to both; each `G_u` is `λ`-Lipschitz on the reachable domain for a common `0≤λ<1`; and the one-step abstraction defect satisfies `d(q(F_u(x)),G_u(q(x)))≤ε_t` for the actual reachable pair at that time (uniform `ε` is a special case). Set `E_0=d(q(x_0),z_0)` and `E_{t+1}=λE_t+ε_t`.

**Proof:** by triangle inequality and Lipschitz property,
`d(q(x_{t+1}),z_{t+1}) ≤ d(q(F_{u_t}(x_t)),G_{u_t}(q(x_t))) + d(G_{u_t}(q(x_t)),G_{u_t}(z_t)) ≤ ε_t + λ d(q(x_t),z_t)`; induction gives `d(q(x_t),z_t)≤E_t=λ^t E_0 + Σ_{j=0}^{t-1}λ^{t-1-j}ε_j`. If `ε_j≤ε`, then `E_t≤λ^t E_0+ε(1−λ^t)/(1−λ)`. At `λ=1`, the valid weaker bound is `E_0+Σ ε_j`. The theorem needs true defects along the actual rollout or a proved uniform envelope; a finite training-set estimate alone is not a uniform bound.

**Non-entailment:** Attractor-like contractivity of the *abstract* dynamics does not make q a naturally selected causal individual, ensure unbiased observer data, or validate a real neural representation. A hidden autonomous feedback policy can invalidate the common-control premise (GL64-04). Domain/regime switches require re-certification.

## GL64-02 — Observer *decision* agreement can follow from a sufficient score margin, not mere shared records

**Source anchors:** `SRC-0261` p.6 output congruence; `SRC-0299` pp.4,6–7 (declared observations, trace and residual); `SRC-0298` p.7–8 (false commitment metrics); source-bound correction GL63-01 (historical records do not force a new measurement).

Let an observer's *deterministic declared scoring protocol* `s:Z→ℝ^m` be `K`-Lipschitz in sup norm: `||s(a)−s(b)||∞≤K d(a,b)`. Let `j=argmax_i s_i(z_t)` be unique, with top-two score gap `m_t=s_j(z_t)−max_{k≠j}s_k(z_t)>0`. If `m_t>2K E_t` and GL64-01 applies, then `argmax_i s_i(q(x_t))=j`, since every score moves by at most `KE_t`, reducing the gap by at most `2KE_t`. If two observers use a shared aligned score protocol with certificates `E_t^A,E_t^B`, each needs its own margin gate (or joint bound). This is **deterministic action/readout agreement** conditional on measurement alignment and separation; it does not assert same random quantum outcome, subjective agreement, or independence of their observations.

**Negative control:** near a score tie, arbitrarily tiny state error can flip argmax. No positive uniform decision guarantee without a margin or explicit stochastic coupling. Different frame mappings or different policies invalidate the conclusion.

## GL64-03 — Finite-step Ξ Gate: exact Lyapunov change has a quadratic term

**Source anchor:** `SRC-0130` p.23 equations (8.14)–(8.18) define the first-order improvement `−eᵀ W Δe` and Gate G4 as sign agreement + minimum magnitude; the prior v5.7 audit showed that a negative signed improvement could pass G4. Here we identify a **distinct finite-step obstruction even when first-order improvement is positive**. `SRC-0129` p.16 explicitly presents discrete-time controls and regime-local linearisations; p.23 excludes jump instants.

For symmetric positive-semidefinite `W`, `V(e)=½eᵀWe`, and a finite state change `h=e_{t+1}−e_t`, the **exact** improvement is
`I_actual=V(e_t)−V(e_{t+1})=−e_tᵀWh−½hᵀWh`.
The paper's directional `−eᵀWh` agrees only to first order. **Counterexample:** `W=1`, `e_t=1`, `h=−3`: directional proxy `+3>0`, exact `I_actual=½−2=−3/2`; a matched positive predicted and measured directional change could pass G4 while increasing the actual loss. Proposed finite-step improvement Gate must use observed `I_actual>0`, independently compare predicted and observed exact finite-step improvement (with tolerances) and control for baseline/no-action trend to attribute benefits causally. At infinitesimal time steps, the source formula remains a useful local directional derivative, not a guarantee for arbitrary finite control amplitude. On a singular W, improvement says nothing about its null directions.

## GL64-04 — Open-loop port certificates do not transfer to mismatched feedback policies

**Source anchors:** `SRC-0261` pp.6,14,28: admissibility, interventions and task-specific Port validity; `SRC-0298` pp.7–8 insists on budget-matched experimental arms and declared interventions.

**Exact countermodel:** `X=Z={0,1}`, `q=id`, `F_0(x)=G_0(x)=0`, `F_1(x)=G_1(x)=1`. Each fixed-control map is zero-Lipschitz (`λ=0`) and has one-step abstraction defect `ε=0`. Start `x_0=z_0=0`. But if the real policy chooses `u_t=1` and the simulated policy chooses `u'_t=0`, then `q(x_1)=1` and `z_1=0`, so discrepancy is 1 despite the apparent zero-error open-loop certificate.

**Repair:** declare and validate a *joint closed-loop map*, e.g. `H(x)=F_{π_X(x)}(x)`, `\bar H(z)=G_{π_Z(z)}(z)`, with `d(qH(x),\bar H q(x))≤ε` and `\bar H` Lipschitz, or require identical action traces and replay them in both systems. Unverified policy alignment, changing intervention sets or out-of-regime actions are explicit stop gates. A controller can be useful in practice without meeting this strong theorem.

## GL64-05 — Residual ledger yields conditional ex-post bounds, not automatic advance prediction

**Source anchors:** `SRC-0299` pp.6–7: trace, filtration and directional-vs-magnitude residual; p.18 revision accountability; `SRC-0298` pp.8–9: commitments, false positives, null-vs-alternative residual ablation; `SRC-0130` p.23: direction vs predictive gate.

If each realized transition logs `r_t=d(qF_{u_t}(x_t),G_{u_t}(qx_t))` with genuine state/trace access, an append-only ledger can compute `E_{t+1}=λE_t+r_t`, which **after observing transition t** certificates the realized discrepancy. This is a valid algebraic online replay object, but a pre-decision guarantee for `t+1` requires a *precommitted* bound `r_t≤\bar r_t`, a calibrated high-probability bound, or a validated monitor with no intervening unobserved action. A retrospective residual ledger cannot by itself predict the next unseen residual.

Countermodel: training log has `r_t=0` for every observed tick, while a later adversarial mode adds a one-time `r=1`; the prior empirical maximum zero is no valid universal bound. Revision Gate should record its confidence source, coverage/regime, permissions, rejected alternatives and explicit stop criteria. Residual magnitude `Σ w_t r_t²` and coherent signed directional residual are distinct statistics; neither independently identifies the true causal source of a mismatch.

## GL64-06 — Research Skill constructive bridge with null-generative controls (prospective)

**Source anchors:** `SRC-0298` pp.8–9,14–15: module ablations, residual-direction comparison and representation-change experiments; `SRC-0299` pp.13,18,25: dependency graph, accountable revision and a functional-geometry entrance test; `SRC-0261` pp.22,28: decoy false positives and mapping contract. This is a **design prescription**, not a completed Skill or a proof of creativity enhancement.

**Required repair card:** `source / exact proposition / assumptions / minimal countermodel or supporting derivation / what survives / missing bridge / paired hypothesis and rival / falsification test / status / historical lineage`. Example grounded here: GL64-03 first-order gate accepted overshoot → add exact discrete Lyapunov difference → compare under same action and baseline against a no-action control → retain `Δe→0` directional interpretation. User-provided analogy should be translated into typed state, operator, metric, invariant and observation maps *before* using an Attractor lens; ask whether a simpler non-attractor model fits equally well. A useful residual must lead to a measurable discriminant, not merely a suggestive new metaphor.

**Prospective factorial benchmark:** generic Review/Repair only vs Kernelization provenance plus optional Attractor lens on/off and human analogy on/off, with hidden out-of-corpus tasks, paired model/token budgets, blinded verification of repairs, false-positive rate, novelty with prior-art audit, measurable test specificity and ability to reject seductive but false analogies. The v6.4 theorem/countermodels are new local mathematical audits; **independent LLM N=0**, no claimed Skill transfer, no empirical Attractor/analogy gain.


---

# v6.5 — Compiler-audited synthetic conditional mathematics

# v6.5 — Deterministic Synthetic Port / Gate Assay and Baseline Equivalence

**Evidence status:** Four original-source PDF bytes verified against their immutable Manifest entries (`SRC-0130` pp.22–24; `SRC-0261` pp.6,10,14; `SRC-0298` pp.8–9,14; `SRC-0299` pp.6–7,18). PDF `SRC-0298` physical p.9 rendered and visually inspected. The source members were previously extracted from their archived original PDFs and rechecked by SHA-256; these are targeted readings, **NOT new full-document deep-read certifications**. All math and code experiments below are **compiler-authored**, not a verbatim source experiment and not a test on actual LLM representations. Four-source assertions should not be conflated with the 325 source identity roster.

## GL65-01 — Exact grid enumeration of an approximate Port error certificate and the ordinary control equivalence

**Source anchors:** `SRC-0261` p.6 equation (4.12) and p.14 protocol/identifiability limits; GL64-01. `SRC-0298` pp.8–9 asks for matched-budget arms and null vs alternative rather than assuming gains.

Explicit synthetic controlled system: `x_t=(z_t,h_t)`, `q(x_t)=z_t`; actual `z_{t+1}=λz_t+u_t+a tanh(h_t)`, `h_{t+1}=ρh_t`; effective `z^m_{t+1}=λz^m_t+u_t`. For **identical** exogenous action sequences, `r_t=|a tanh(h_t)|≤|a|` and `|q(x_t)-z^m_t|≤E_t` where `E_{t+1}=|λ|E_t+|a|`, `E_0=0.15`. This is exactly the standard scalar Lipschitz/state-abstraction certificate, and does not require an independently discovered SMFT Attractor. We enumerate λ∈{0.2,0.6,0.9,1.0,1.1}, a∈{0.02,0.12}, ρ∈{0.3,0.8}, h₀∈{−2,−.2,0,.2,2}, z₀∈{−.8,0,.8}; 300 rollouts × 12 declared shared actions = **3,600 actual transitions**. The bounds had **0 violations**, by construction under model assumptions. For `|λ|<1`, asymptotic certified width tends to `|a|/(1−|λ|)`; for `|λ|≥1`, no bounded asymptotic width follows. A regime-blind valid baseline substitutes `L=max(1,|λ|)` and gives generally looser width. A baseline ordinary controller supplied the *same known* |λ| yields exactly the same predictions and bounds as the alleged Attractor variant (**zero incremental predictive gain by vocabulary**). No empirical effect-size or statistical confidence can be inferred; these are deterministic examples designed to reproduce a theorem.

## GL65-02 — Decision-margin certificate gives selective accuracy, not unconditional agreement

**Source anchors:** `SRC-0261` p.6 aligned declared Port/output; GL64-02 and GL63-01. For aligned `s(z)=(z,-z)`, each score is K=1 Lipschitz, margin at model state equals `m_t=2|z^m_t|`. When `m_t>2 E_t`, model and actual decisions cannot disagree (simple 2KE bound). In 3,600 synthetic transition readouts there were **1,870 certified** cases, **0 disagreements among certified**, and **308 disagreements among all cases**. Cases without certification can still be correct. Certification coverage 51.94% is neither the population success rate nor an independent physical Observer Agreement test. If decisions differ under altered outcome frames or stochastic quantum instruments, this certificate does not transfer. A zero false-disagreement count on an exhaustive *declared grid* does not establish robustness outside the grid.

## GL65-03 — Finite-step beneficial Gate vs first-order direction Gate: explicit false-accept matrix

**Source anchor:** `SRC-0130` physical p.23 equation (8.16)–(8.18) uses first-order direction and a sign-matching gate; GL57 and GL64-03 provide prior counterexamples. For `V(e)=½e²`, candidate finite update `h`, `D=−eh` is first-order improvement, but exact improvement is `I=−eh−½h²`. Enumerating 7 declared error states `e∈{−2,−1,−.5,0,.5,1,2}` and 9 candidate changes `h∈{−3,−2,−1,−.5,0,.5,1,2,3}` gives **63** possibilities. Positive-only first-order Gate accepted 24, **6 were actually harmful** (`I<0`). Positive exact-improvement Gate accepted 14 and **0 harmful**; remaining cases include neutral (must distinguish strict acceptance). This is a head-to-head *algebraic control gate* comparison in one fixed grid; not external evidence of deployable physical control. It does not test the source G4's full noisy prediction/calibration behavior; it tests its missing finite-step beneficialness condition.

## GL65-04 — Even exact before/after improvement does not identify causal control benefit

**Source anchors:** `SRC-0130` p.23 makes effectiveness claims, `SRC-0298` p.8 calls for matched ablations. Consider unobserved no-action trend `e_no=e+d` and action outcome `e_act=e+d+c`. An action can satisfy `V(e_act)<V(e)` while `V(e_act)>V(e_no)`, meaning it improved the prior state but made a better natural trajectory worse. Example `e=1, d=−0.4,c=+0.2`: `e_act=0.8`, `e_no=0.6`, before `V=0.5`, after `V=0.32`, no-action `V=0.18`; before/after improvement +0.18 but relative causal value `V(e_no)−V(e_act)=−0.14`. Full grid of 3×5×5=75 specified cases gives **8** such instances. Remedy: matched no-action control or identified counterfactual with stated assumptions; cannot infer causal gain from before/after alone. Counterfactual comparison itself is not randomized or empirically identified in this synthetic benchmark; it is known by construction.

## GL65-05 — Each fixed-control map can contract while switched forcing has no common fixed point

**Source anchors:** `SRC-0261` pp.6,10 and GL64-01/04. `G_+(z)=λz+1`, `G_-(z)=λz−1`, `λ=0.6`. Both maps are strict contractions. Under alternating input `+1,−1,+1,...`, the attracting driven trajectory is a period-two orbit `(+1/(1+λ),−1/(1+λ))=(+0.625,−0.625)` and **not one autonomous fixed point**. The explicit 180-step iteration reaches the two-cycle to machine precision. Contraction-based error/forgetting certificates can remain valid under the same input stream, but do not license an unqualified single global Semantic Attractor. Must distinguish common fixed point, nonautonomous pullback/response and switched-system attractors.

## GL65-06 — Closed-loop mismatch survives zero per-action abstraction defect

**Source anchors:** `SRC-0261` pp.6,14; GL64-04. `F_u(x)=G_u(x)=u` for `u∈{0,1}`: each fixed-action map has `λ=0`, and Port defect is exactly zero. But with actual feedback action `u=1` and surrogate feedback `u=0` at the same starting value, first-step discrepancy is 1. Experiment reproduces exact countermodel. Joint policy-state Port or identical replayed actions are prerequisites for closed-loop certification. Adding residual ledger after divergence cannot retroactively justify a previously authorized action.

## GL65-07 — Skill-method provenance and prospective factorial ablation, with negative baseline result

**Source anchors:** `SRC-0298` p.8 matched intervention/budget arms and p.9 explicit null hypothesis comparing `(magnitude only)` against `(magnitude,direction)`; `SRC-0299` p.7 directional/magnitude ledger distinction and p.18 accountable revisions. Future GitHub Skill should support source-internal and cross-paper conflict, conditional theorem repair, productive Residual and original historical Generative Moves, optional Attractor math and human analogies. A concrete audit example is **GL65-04**: an alleged controlled improvement creates a nontrivial `no-action counterfactual` Residual which can guide next experiment. An analogy must map `entities→operators→observables→countermodel→falsifier`, with a linguistically plausible decoy failing the typed mapping test. Pre-register 2×2 factorial arms `(Attractor on/off)×(human analogy on/off)` with matched tokens/model/resources plus unrelated paper corpora. Real blinded Skill inference **NOT_RUN**; these 3,600 synthetic transitions, 63 Gate cases and 75 counterfactual rows cannot measure LLM creativity, superior knowledge compilation, or natural semantic basin existence. The mathematically equivalent ordinary Lipschitz baseline is a **reported null** for additional effect of Attractor vocabulary under fixed premises. Explicitly preserve negative effects and avoid marketing language.



---

# v6.6 — Held-out Port Calibration, OOD Collapse, Statistical-vs-Deterministic Gate

**Evidence:** Four source PDF identities (`SRC-0261` pp.6,14; `SRC-0298` pp.8–9; `SRC-0299` p.7; `SRC-0130` p.23) independently SHA-verified against immutable 325-row Manifest. `SRC-0298` physical p.9 rendered and visually checked. All dataset generation, regressions and statistical calculations are NEW COMPILER-DEVISED SYNTHETIC EXPERIMENTS, not experiments in those source papers. Raw per-sample CSV, exact RNG seed, generator and runnable code provided in `EXPERIMENTS_V66`. No scientific or LLM-world validation; no source fully reread.

## GL66-01 — Fit conditional effective Port on unseen data, do not leak true λ into estimation

Declare hidden-state generator `z'=0.65 z + u + 0.22 tanh(h) + 0.07 u²` where `h` is hidden and `q(x)=z`. Train 1,800 simulated i.i.d. observations under `h~N(0,0.22²)` and `u∈{-0.2,0.2}`, estimating `\hat z'=\hat b_0+\hat λ z+\hat b_u u` by OLS without access to actual coefficients, hidden `h`, or nonlinear action term. Learned `\hat λ=0.6528892748`, generator λ is 0.65. Numerical closeness on this run is **not** proof of functional sufficiency: the same `z,u` may have different successors when `h` differs. `SRC-0261` p.6 requires a fiber-respecting transition, p.14 highlights natural individual identification as outstanding. Under observational fitting, absence of residual on sampled states alone cannot prove fiber-factorization for all possible hidden states or policies.

## GL66-02 — Split-conformal calibration under exchangeability yields marginal coverage, not a uniform dynamical error bound

Use 400 independent exchangeable calibration observations. Compute absolute residuals `r_i=|z'_i-\hat G(z_i,u_i)|` and `q=r_(k)`, `k=ceil((n+1)(1−α))=381`, `α=.05`, so `q=0.0963616074`. Under exchangeability of calibration and a *single new* test score with a fixed fitted model, split-conformal threshold has marginal future-score coverage ≥`1−α` (up to tie details and finite sample discreteness), **not for each state and not jointly over 12 steps**. Held-out i.i.d. 1,159/1,200 = **96.5833%** covered, 41 outside. Therefore `\hat ε=q` must never be substituted as a *uniform deterministic* `ε` in GL64-01's all-state port bound. It is an empirical statistical tolerance interval. No conditional safety or OOD coverage theorem is claimed.

## GL66-03 — Same threshold loses meaning under hidden-state covariate shift

Shift unobserved `h` to `N(2.8,0.2²)`, with matched input regime. OOD hidden-shift test has **0/1,200** covered. Changing action from ±.2 to ±1 with same hidden distribution gives **862/1,200 = 71.8333%** covered, and combining both shifts yields 0/1,200. These regimes were explicitly programmed and are not estimates of natural LLM drift. Formal countermodel: for identical `(z,u)`, choosing `h=0` vs `h=3` changes projected successor by `0.22 tanh(3)≈0.2189`. Thus no exact deterministic `z`-only quotient exists without restrictions; train fit or apparent contraction cannot repair lost hidden information. Cf `SRC-0261` p.6 action-relative Port, p.14 identifiability.

## GL66-04 — A statistical radius cannot be used as a deterministic decision-margin certificate

For scores `(z,−z)`, `|\hat z'|>q` is a **probabilistic screening heuristic**, not GL64-02's theorem using guaranteed `E_t`. In held-out i.i.d. regime 1,033 are margin-screened, **1 has wrong sign**; hidden shift 1,013 screened, **119 wrong**. Action-shift 1,200 screened with 0 wrong even though 338 residuals lie outside the radius: decision correctness and calibrated state-error validity measure different properties. (Combined shift: 1,200 screened/0 sign mismatches despite 0% error coverage, because forced action magnitudes dominate the sign.) Do not call these observations safety-certified decisions. The margin theorem remains valid only when its uniform error bound really holds. Compare `SRC-0130` p.23 risky gate eligibility and GL65-02.

## GL66-05 — Estimated local contraction is not identified functional closure or a global Lipschitz certificate

The OLS slope 0.652889 is the fitted derivative of `\hat G`, not the worst-case derivative/transition variation of the true hidden-state dynamics under unknown `h` or feedback. Even if `|\hat λ|<1`, errors may be biased, action-dependent and nonstationary, as GL66-03 demonstrates. An ordinary linear OLS/state-abstraction baseline supplied identical data and fit produces numerically identical predictions, error estimates and decisions to the Attractor-labelled version. No additional benefit due to terminology is measured. Correct tests: held-out identified action support; in-support vs OOD calibrated uncertainty; counterexample at same q-fiber; partial-identification bounds on hidden variable effects; exchangeability monitoring and stop-control gate on detected drift.

## GL66-06 — Residual magnitude, direction, and constructive Skill work under matched null hypotheses

`SRC-0298` physical p.9 explicitly prescribes comparing residual magnitude against magnitude-plus-direction; `SRC-0299` p.7 distinguishes an accumulated squared residual and directional coherence. In this toy generator the hidden-state shift produces a coherent positive signed error even when the calibrated radius collapses. The proposed *next* experiment is matched calibration/evaluation of two drift detectors (absolute magnitude only vs magnitude and residual sign), measuring false alarms at fixed false-positive budget and out-of-distribution detection delay. This is **NOT_RUN**, so no magnitude+direction uplift is reported. For the future Skill, the warranted local workflow is `CLAIM → ASSUMPTIONS → COUNTERMODEL → CONDITIONAL REPAIR → RESIDUAL → FALSIFIER`, with optional Attractor analogies separately ablated. Human analogy effect, real creative research value, and independent source-hidden LLM benchmark are **NOT_RUN**. Maintain source-page-hash, typed edge, and equal-information rival baseline; avoid conflating routine OLS with new research invention.


---

# Newly compiled GL67 source-qualified local audit

# v6.7 — Residual Magnitude/Direction, Sequential Change Detection, and Gate Opportunity Costs

**Source boundary:** `SRC-0298` physical p.9 explicitly proposes a magnitude-only versus magnitude-plus-direction experiment; `SRC-0299` p.7 motivates dual residual ledger; `SRC-0261` pp.6,14 establishes protocol-sensitive Port sufficiency; `SRC-0130` p.23 specifies Gate G4. All four SHA-256 match the immutable Source Manifest. Physical pages only; no full-depth certification. **All generators, scan statistics, simulations and gate policies below are newly compiled synthetic methods, NOT experiments actually reported by these source papers.** Script `v67_residual_change_assay.py`, results and 8,000 per-stream alert records are provided. `20261016` seed, 4,000 training normal traces, 5,000 separate normal calibration traces, and five regimes ×1,600 test traces of 64 time steps each. Direction/sign-only shifts begin at zero-based t=20. Normal calibration sets a separate 95th percentile *whole-horizon maximum-scan* cutoff for each detector; the unequal numeric cutoffs are necessary for matched familywise false alarms. No independent LLM or neural Attractor trial.

## GL67-01 — Pure sign shift is information-theoretically invisible to absolute-only detector

Let `r_t=s_t m_t` with `m_t≥0`, and construct two controlled sequences using exactly the same magnitude path `m_1,…,m_T`. In the null `Pr(s_t=+1)=1/2`; after a specified change point under the sign alternative `Pr(s_t=+1)=.9` (or `.1`), with independent signs conditional on the magnitude paths. For **every** measurable detector `φ(|r_1|,…,|r_T|)` the test output is pathwise identical under the paired null and sign alternative. Consequently its true alarm probability under that alternative equals its null alarm probability, over the same coupling. This is a property of the specially constructed sign-only alternative, not a general assertion that magnitude can never detect bias. A signed statistic can have power because its observation sigma-algebra is strictly richer; a fair rival is a standard two-sided signed sequential statistic, not an Attractor-branded score.

## GL67-02 — Matched full-horizon false-alarm calibration is necessary for two-channel comparison

For two moving-window widths 8,16 compute normalized magnitude mean shifts and (for dual) normalized signed mean shifts. Scan timewise maxima up to the full 64-step horizon, calibrating each model's 95th percentile separately on 5,000 independent null streams. Cutoffs `T_mag=3.437451863492663`, `T_dual=3.583724281650433`; on a distinct 1,600-stream stationary test, full-horizon alarm counts **74/1600 (4.625%)** and **75/1600 (4.6875%)** respectively. False alarms before t=20 were 17 and 15. Empirical calibration does not prove 5% future control under unknown distributions or indefinitely repeated monitoring; multiple scanning windows require maximum-statistic rather than naive pointwise control.

## GL67-03 — Direction-only changes: evidence for standard signed-residual detection, not new physics

At the same full-horizon-calibrated false-alarm budget, positive sign-only change has first alarm after t=20 in **57/1600** (magnitude-only) versus **757/1600** (dual); negative sign-only **57/1600** versus **751/1600**. The 57 baseline alerts are identical on paired magnitude paths, verifying GL67-01 exactly. Among dual detections, median *detected-only* delay was 22 steps for both signed regimes. Never treat the median among detections as the unconditional detection delay or imply near-universal 100% power. This local change detector is a standard time-series method whose benefit is from supplied signed data and justified distributional contrast; nothing establishes an SMFT/Attractor-specific advantage.

## GL67-04 — Added directional channel can hurt on amplitude-only changes

Magnitude scale ×1.7 after t=20 gives **1553/1600** post-change alerts for magnitude-only versus **1549/1600** for the two-channel detector (97.0625% vs 96.8125%), with 9 and 10 steps detected-only median delay. Adding another scanned channel increases the null critical value; direction is not universally an improvement. Joint sign+scale shift gives 1553/1600 versus 1585/1600 and median detected delays 9 vs 7 steps. This is model-conditional calibration/power tradeoff, not a universal optimality theorem.

## GL67-05 — A drift alarm is not a Gate safety proof, and abstention consumes beneficial actions

Define a separate **synthetic one-step opportunity rule**: accepting an action yields putative benefit `0.08-r_t`; actions with `r_t>0.08` are harmful. Before the first detector alert, accept; afterwards abstain. Under the positive sign alternative, magnitude-only accepts **31,081 harmful** and **37,271 beneficial** post-change opportunities, while the dual policy accepts **24,390 harmful** and **29,884 beneficial**. So dual avoids 6,691 more harmful actions relative to magnitude-only but also abstains from 7,387 additional beneficial opportunities. Treat these as counterfactual fixed-trajectory counts, not a proof of better net utility, truly causal improvement, runtime safe action, or valid feedback-world interventions. Alerts can also occur before the programmed change. Evaluation must jointly report false alarms, missed detection, beneficial opportunity loss, utility weights and protocol shift. `SRC-0130` G4 cannot acquire a safety guarantee by attaching this monitor.

## GL67-06 — Residual-direction research programme and Skill controls

The source question `SRC-0298` p.9 compares `Performance(R)` vs `Performance(R,direction)` and presents directional coherence as **testable hypothesis**, not universal theorem. A magnitude-preserving sign change is an intentionally favorable falsifier of the null, while an amplitude-only alternative is a deliberately unfavorable countercontrol. A real Port experiment should estimate residuals on unseen traces without access to hidden regime or true error sign during action selection, specify change-point alarm budget, apply a closed-loop replan policy, and then compare to an equal-information standard signed drift detector. This run has not executed closed-loop interventions, neural observations, independent source-hidden LLM reconstruction or Attractor/analogy creativity factorial experiments. The future Skill should emit `claim → contradictory case → scope repair → constructive residual → competing null mechanism → measurable test`, while keeping optional mathematical Attractor and human analogy as separate ablations. **No unique Attractor benefit claimed.**


---

# v6.9 — Neural proxy disconfirmation, coordinate invariance, and future falsification

**Provenance.** Original source `SRC-0258` physical PDF pp.3–8 discusses `P=(B, Δ, h, u)`, protocol-dependent generalization transitions, role-defined Ξ=(ρ,γ,τ), and proxy identifiability; `SRC-0221` PDF pp.1–5 is a shorter author/NotebookLM account. Both original TAR members verified by the v6.9 compiler against stable SHA256 and size. Only bounded pages were read; **no full-depth audit**. Mathematical counterexamples and neural experiments below are *compiler new*, not discoveries reported by the sources. Experiment: `v69_real_transformer_falsification.py`, `EXPERIMENTS_V69/`. This is a newly trained small Transformer, **not pretrained natural LLM cognition or evidence of the existence/nonexistence of SMFT semantic attractors**. The exact protocol was committed in local executable code before the initial local experiment; there is **no external timestamped preregistration**; a reporting bug in control loss was repaired and the full run repeated. Held-out examples are not in optimization, but this experiment is not an independent laboratory replication.

## GL69-01 — Finite checkpoint trajectory cannot certify an asymptotic attractor

**Typed objects:** observed finite sequence of state vectors and an unknown deterministic update, with no globally identified transition law. A formal 1D counterexample is sufficient.

Fix finite T and `x_j=2^{-j}`, `j=0,...,T`. Define `f(x)=x/2` and `g(x)=x/2+c ∏_{j=0}^{T-1}(x-2^{-j})`, with nonzero `c`. Both continuous maps satisfy `f(x_j)=g(x_j)=x_{j+1}` at all **observed** `j<T`. Yet `f(0)=0` and `g(0)=c∏_{j=0}^{T-1}(-2^{-j})≠0`; zero is a fixed-point attractor for f but not even a fixed point for g. Thus a finite orbit alone cannot prove the hypothesized asymptotic attractor even under an assumed autonomous 1D model. A nonautonomous optimizer trajectory across model checkpoints identifies still less about **inference-time** state dynamics, which is a distinct index. This does not falsify a specified attractor under additional structural restrictions, recurrent state observation, perturbation-response and out-of-sample predictions.

**Links:** `SRC-0258` pp.3–8; `SRC-0221` pp.1–5 as motivating claims about protocol-bound crossings, not the source of this proof. `RA-O01`, `RA-O02`, `RA-E14`. **Evidence grade:** exact compiler model counterexample; not real Transformer attractor falsification.

## GL69-02 — Class-geometry coherence without a declared metric is representation dependent

Let two labeled classes in R² be `A={(0,0),(2,0)}`, `B={(0,1),(2,1)}`. Euclidean within-class distance is 2 and the nearest inter-class distance is 1, hence raw distance cohesion is poor. Under invertible rescaling `S_k(x,y)=(x,ky)` for k>2, within-class distance stays 2 but vertical inter-class distance becomes k, reversing that nearest-neighbor relation. A downstream function can compensate with `S_k^{-1}` and retain identical input/output behavior. This is a function-factorization counterexample; **not** a claim that every invertible matrix is a symmetry of every fixed LayerNorm Transformer architecture. Any representation metric is legitimate only after its coordinate convention, permissible equivalence transformations and measurement test are declared.

**Links:** `SRC-0258` pp.4,7 (protocol and proxy stability); `RA-O01`, `RA-M01`. **Evidence:** exact finite mathematical counterexample. It constrains interpretations; it does not imply learned representation geometry is useless.

## GL69-03 — Zero-step representation decoding is a positive learning-proxy falsifier

**Question posed before measurement:** Does class geometry itself appear only when the small Transformer acquires task behavior? CPU PyTorch experiment trained two real `TransformerEncoderLayer` blocks on majority of five binary inputs. Fixed balanced split: 24 train, 8 held out, three model seeds 17/23/41; checkpoints `0,20,60,120,240`; three additional training-label permutation controls (shuffled only training labels). A separate ordinary sklearn RidgeClassifier is trained on labeled train-split CLS features at each checkpoint; this probe **is supervised** and its result must never be called untrained zero-shot neural understanding.

**Observation:** At initialization, the original network itself scores 4/8 heldout (chance-level here) on all three seeds, but the ordinary supervised Ridge probe reaches **8/8** heldout from all three *untrained Transformer features*. Thus the stronger proposed proxy "class decodability first emerges with task competence" is falsified **in this selected small model and split**; there is an obvious standard baseline requiring no learned semantic attractor. After 20 steps, actual model gets 8/8 in each seed; fixed checkpoint spacing is too coarse to identify sharpness, delayed grokking or a critical surface. The final three shuffled-training-label controls achieve 3/8, 5/8, 4/8 on true heldout labels. Random-label controls are not entirely powerless (part of the task structure can persist in random input features) and three seeds/8 examples are underpowered for broad transfer claims.

**Surviving weak claim:** cross-checkpoint representational diagnostics can be *tested* as prospective predictors under harder tasks, preregistered thresholds, multiple splits, matched linear probes and independent replicates. **Not inferred:** proof of semantic attractor, causality of geometric clustering, sudden understanding, originality relative to prior grokking work.

## GL69-04 — Internal single-token patch fails when true counterfactual output must change

At checkpoints 0,120,240, for every heldout receiver and each of five input bits, create donor differing at exactly that bit; replace the **post-layer-1 representation of only that bit token** with donor's value; finish layer 2. The full counterfactual forward pass is the ordinary matched control (replace whole input and recompute all activations). Store all 720 cases, including shuffled-label runs. At final step in trained true-label runs, there are 120 patch cases (3 seeds × 8 receivers × 5 bits), of which 45 have a changed correct label. Targeted single-token patch yields correct label on **0/45 changed-label** cases, and does not flip original output in any of those 120 cases; complete input counterfactual is correct on all 120. The patch is correct for 75/75 unchanged-label cases, so its overall 62.5% is misleading if unstratified.

**Inference boundary:** this precisely falsifies *the chosen single-site transplant sufficiency* in this trained model; it does not refute distributed computation, other token/layer choices, multi-site activation patching, formal Port existence, or semantic attractor ontology. The right next experiment is registered multi-site patching with matched sham and off-manifold controls, with a causal correction score conditioned on label-changing samples, plus exact fiber congruence on declared interventions (cf. `GL50-01`, `GL59-01`).

**Explicit allowed statuses:** proxy disconfirmation in a trained synthetic-domain Transformer `M4_LOCAL_NEURAL`; whole semantic-attractor hypothesis `OPEN/NOT_TESTED`; independent source-hidden LLM `NOT_RUN`; Attractor/Human analogy creativity benefit `NOT_RUN`.


---

# v7.0 — Causal-site, gauge, and source ODE dependency audit

**Evidence boundary:** `SRC-0258` original TAR SHA-256 matched immutable manifest; newly checked physical PDF pp.9–14, source-specific equations pp.13–14, page rendering checked p.10 and p.13–14; only bounded selected-page review. v6.9 checkpoint artifacts were executed by this compiler, not reported in the original source. Three normal and three shuffled-label trained Transformer seeds, frozen checkpoint training data (24/8), 5-bit majority, 4 checkpoint observations in new experiment. There is no independently replicated natural-language semantic attractor experiment.

## GL70-01 — Compensated invertible readout-gauge preserves logits but not cosine geometry

**Exact conditional statement.** Let the row-vector representation `z∈R^d` be read by `f(z)=zW^T+b`, and let `A∈GL(d,R)`. Define `z'=zA` and `W'=W A^{-T}`. Then `f'(z')=z A (W A^{-T})^T+b=zW^T+b=f(z)` for every z. It is wrong to read a *specific* Euclidean/cosine separation score as model-function invariant under such non-isometric changes of representation. This is a change of representation **with a compensated downstream readout**, not a claim that one can arbitrarily change hidden state in a fixed frozen network.

**Executed evidence:** 6 final checkpoints × 4 prespecified coordinate transformations (identity, orthogonal, fixed diagonal, and readout-axis stretch) =24 measurements. Max output-logit numerical discrepancy ≤1.1e-14; orthogonal transform preserves cosine score to ≤1e-8. With three genuinely trained models, readout-axis transform changes training-oracle cosine class-separation from `(0.9294,0.9442,0.9381)` to `(0.9963,0.9971,0.9967)` while preserving model decisions. The readout-aligned transformation depends on trained output weights **but not on class labels selected to maximize separation**. All numeric values come from compiler assay, not `SRC-0258`.

**Repair:** declare observational equivalence/gauge group, fixed geometry or an invariant derived from input-output causal effects before giving a class cluster an attractor interpretation. Does not deny dynamics if there is independent temporal restoration evidence. Source anchor `SRC-0258` pp.9–12 discussion of DFT as symmetry-selected observation basis, not a demonstration that arbitrary gauges are scientifically equally justified.

## GL70-02 — Multi-site causal transplant reveals bounded, distributed functional dependence

**Executed evidence and exact scope:** Frozen step240, three correctly trained majority Transformers. Forty one-bit counterfactual pairs per seed, fifteen change the oracle target. Use post-layer1 donor activations at six prespecified sites; report **only primary 45 label-changing pairs**: sham 0/45; changed bit 0/45; CLS-only 30/45; CLS+changed bit 30/45; off-target bit 0/45; all tokens 45/45. Here all initial and whole-input donor predictions are correct (not assumed true for permuted controls). The 45 events are correlated within 8 heldout inputs and three trained seeds: no independent N=45 estimate of a population accuracy. Results from ordinary activation patching do not establish a semantic attractor or unique `Functional Port`.

**Conditional repair:** an interventionally useful state component may be CLS+other contextual vectors even when donor changed-bit vector is insufficient. Better question: can a proposed reduced-state quotient predict **unseen** donor effects and retain intervention closure across a controlled family of state/action pairs better than baselines? Attention readout/circuit explanations are conventional equal-information rivals. Keep unsuccessful, successful and sham patches together. Source `SRC-0258` p.9's observation map is a candidate generator, not an external validation of this intervention outcome.

## GL70-03 — Full intermediate-state substitution is a compositional identity, not emergence evidence

**Formal theorem:** For a deterministic two-stage computation `f=f_2∘f_1`, substituting the complete intermediate state `f_1(y)` when processing `x` produces `f_2(f_1(y))=f(y)`, provided that no other independent state or side channel survives the intervention. This is true whether the net is trained, random, or label-permuted. At every checked checkpoint the 960 all-token patch cases match donor logits to numerical tolerance (three seeds, two training controls, four checkpoints, 40 counterfactual pairs), and the matching 960 shams return original logits. A 45/45 post-training success count on label-changing oracle cases therefore verifies implementation consistency, **not** an identified minimal semantic Port or basin. If remaining state bypasses patch location, the hypothesis's assumptions must be revisited.

**Research residual:** interventions on minimal subsets, latent low-rank factor subspaces, patches including/excluding CLS, and distribution-shifted inputs with matchable donor pairs; compare minimum description/measurement cost against full-state transplant.

## GL70-04 — Claimed amplitude→phase positive feedback is absent from the displayed minimal ODE

**Primary original location:** `SRC-0258` PDF physical p.13 §5.2 equations (5.1a)–(5.1b), and p.14 §5.2.2 explicitly describes faster mode growth causing stronger mismatch correction. Original equations are `dA_k/dt=A_k(λ_k cos D_k−β)` and `dD_k/dt=−μ sin D_k` with fixed positive μ; the proposed text calls this a coupled self-reinforcing feedback system. **They are triangular, not dynamically bidirectionally coupled.** For `−π<D_k(0)<π`, phase satisfies exactly `tan(D_k(t)/2)=tan(D_k(0)/2)exp(−μt)`, independent of `A_k(0)`, growth rate λ, decay β, or other modes' amplitudes. Two initial states with identical phase but amplitudes 1 and 100 retain identical phase trajectories, regardless of relative growth rates. Thus the displayed equations do NOT support the asserted implication "higher A speeds phase alignment". Yet the true conditional one-way relation is preserved: when `λ_k>0`, greater phase alignment increases that mode's logarithmic amplitude-growth rate; under additional persistent advantage conditions a relative amplitude ratio can diverge.

**Minimal repair choices:** (i) revise prose and call this *alignment→growth one-way selection*, allowing changing *relative importance* but not faster phase correction; or (ii) write an explicitly coupled law `dD_k/dt=−μ(A_1,...,A_K)sin D_k` with justified smoothness, signs, empirical mechanism, and resource allocation, and verify with independent perturbations. `μ(A)` is a NEW compiler-proposed model candidate, NOT the author's originally proven equation. The source's reference to a prior modular-addition study is an attributed secondary claim, not independently checked here.

**Negative inference:** this logical discrepancy does not refute Fourier mode selection, grokking, all of PORE/SMFT or the original external modular-addition paper; only the specified bidirectional-feedback interpretation of this precise toy ODE lacks mathematical support.

**v7.0 late per-seed transparency addendum to GL70-02 (discovered before release):** CLS/CLS+bit pooled 30/45 = Seed17 15/15, Seed23 0/15, Seed41 15/15 on oracle-changing flips. Report each seed as a cluster; no 2/3 generalization claim. Full-state patch 15/15 on all three. No retraining or selection.



## GL71-01 — Seed-conditional transplant probabilities constrain portability of single-site functional ports

**Compiler post-hoc reanalysis**, source-independent, from v7.0 frozen patch rows. At post-layer1 CLS-only transplant, 15 oracle-changing cases per trained seed: seed 17 donor-label probability mean 0.999904 and 15 successful target flips; seed 23 0.000123 and 0 flips; seed 41 0.999654 and 15 flips. By contrast complete intermediate-state donor replacement succeeds 15/15 per seed and reproduces donor calculation, a composition identity. Substantial probability margins indicate the seed23 failure is not just near threshold. This does not distinguish attention transport, readout, distributed states, off-manifold patching or alignment without further controlled ablation. No independent replication or claim of a universal semantic port.

**Surviving inference:** the chosen CLS replacement is not interventionally sufficient across independently initialized trained models in this local task. **Research residual:** learn a localization/mediation predictor from separate training seeds and test its held-out predictions on new seeds/tasks using whole-state and sham controls, with uncertainty clustered by seed.

## GL71-02 — Genuine amplitude-dependent phase dynamics must be added and separately identified

**Primary source anchor:** `SRC-0258`, physical PDF p13–14, previously hash-checked and bounded-audited in v7.0. Its specified `A'=A(λ cos D−β), D'=−μ sin D` has no A→D influence. **Compiler candidate**, not original claim: replace phase law with `D'=−[μ0+κ A/(K+A)] sin D`, for A,K>0, μ0>0, κ≥0. At κ=0 exact triangular null is recovered. For initial 0<D<π and κ>0, ∂D'/∂A=−κ K sin D/(K+A)^2<0: locally greater A increases alignment speed. Synthetic trajectories test this local comparative prediction and exact κ=0 null. They do not establish source mechanism empirically. Independent interventions on A plus observed D and rigorous model comparisons are required. If A is unobserved, phase-only trajectories cannot uniquely identify amplitude-led coupling.


# v7.1.1 continuation: 2 compiler result nodes

# v7.1.1 — Prospective functional-patch audit and nonlocal differentiability guard

**Evidence type:** new compiler mathematics and new locally trained PyTorch models. No new original-source PDF/DOCX deep read in this continuation. The source context is the earlier source-scoped discussions under `SRC-0258`, `SRC-0261` and the historical GL70/GL71. No statement about natural semantic Attractors is validated.

## GL711-01 — A local derivative does not determine the outcome of a finite state replacement

For any smooth scalar readout margin `m(t)` along a line segment of hidden states `h(t)=h_x+t(h_y-h_x)`, the first-order Taylor prediction at receiver is `m_hat(1)=m(0)+m'(0)`. It cannot generally determine the sign of `m(1)`. **Counterexample:** `m(t)=-1+2(3t²-2t³)` has `m(0)=-1`, `m'(0)=0` and `m(1)=+1`; the first-order prediction remains negative although the actual donor patch margin is positive. Consequently, differentiability of a frozen Transformer downstream map at the receiver and even exact knowledge of its local Jacobian do **not** suffice for global/finitely displaced donor-patch success. This is a generic smooth-function statement; it does not prove that the actual neural failures are caused specifically by saturation, curvature or any named attractor geometry.

A sufficient *bounded-remainder* repair: if along the segment the second derivative exists and `|m''(t)| ≤ M` for `t∈[0,1]`, then `|m(1)-[m(0)+m'(0)]| ≤ M/2`. If the predicted margin has magnitude greater than `M/2`, its sign must be correct. In full vector space, a corresponding Hessian-norm bound gives `M≤L||h_y-h_x||²`. This bound needs a justified path norm/Hessian bound; do not infer it from a trained accuracy alone.

**Link:** `GL70-02`, `GL71-01`, RA-M01. This is a compiler mathematical lemma, not a source-authored result.

## GL711-02 — Eight prospectively specified seeds reveal nonunique CLS sufficiency, and first-order predictor fails at binary benefit

**Protocol written and SHA256-locked before new-seed execution:** `EXPERIMENT_PROTOCOL_V71_CONTINUATION.md` (SHA `6f369c2ac5795a1d120289507afa53c23880111972aef4b610dc214f59f21f5a`). Same architecture, optimizer and fixed 24/8 split as v6.9; independent initialization seeds `101,103,107,109,113,127,131,137`, all trained 240 steps and reached 8/8 heldout oracle accuracy. Four separately trained permuted-label controls were also executed; their oracle correctness is substantially lower, so few counterfactual cases satisfy the conditional both-correct filter.

For 15 label-changing, both-correct receiver/donor cases per normally trained seed, post-layer1 CLS-only donor activation replacement succeeded: `15,15,15,15,9,9,15,0` out of 15, respectively. Total `93/120` patches across **eight models, not 120 independent replications**. Five models show complete success, two partially succeed, one completely fails. At the same point full intermediate-state donor readout is a compositional positive control, not emergence evidence. An off-target single bit token succeeded in 2/120 changing-label cases, illustrating imperfect negative-control isolation.

The **prospective ordinary-gradient prediction** `m_hat=m_x+∇_CLS m_x ·(h_y[CLS]-h_x[CLS])`, with no fitted threshold, outperformed the 'unchanged receiver' binary outcome predictor in **0/8** new seeds (H1 predeclared threshold 6/8 **FAILED**). Continuous donor-margin absolute error was lower in **7/8** new seeds (H2 6/8 directional threshold met); per-seed relative reduction has median ≈0.65%, one seed degrades, and there is no binary decision gain. An 'always donor' optimistic reference correctly predicts 93/120, whereas the first-order and unchanged-receiver predictors each correctly predict 27/120. Accuracy for all eight seeds is identical, but localization is not. This is a weak-fidelity local approximation/conditional causal assay, not a proof of a general mechanistic predictor, semantic Attractor, or model-agnostic functional state quotient.

**Limits:** same fixed dataset split across all new models, oracle-target donor selection, 11/15 donors belong to the training split per model, correlated counterfactual cases and shared architecture. Different seeds are distinct model initializations but not independent task datasets. This does NOT perform a pretrained LM attractor study or source-hidden independent LLM kernel reconstruction. Only 13 new continuation-specific QA checks rerun, plus the historical v7.1 verifier; historical 866/866 project-wide tests remain an unrerun historical result.

**New residual:** measure the entire receiver→donor interpolation trajectory and locate threshold/curvature; prospective score based on separately trained mediation predictors under task/architecture shift; distinguish off-manifold patch artifacts from true mechanism via matched distribution and intervention admissibility. Use equal-information standard gradient/integrated-path/causal mediation baselines; compare experimental cost and statistical uncertainty clustered by model.


# v7.2 continuation: 3 compiler result nodes

# General Lemma / Local Neural Evidence v7.2 — compiler-authored continuation

**Evidence scopes:** Mathematics below is a formal compiler-derived proof; experiment below is a small, synthetic, locally trained PyTorch Transformer experiment, **not** a natural-language semantic attractor test. No new original source PDFs/DOCX were deeply reviewed this version. Prior source-specific boundaries (including `SRC-0258`, `SRC-0261` and `SRC-0283`) remain historical evidence, not newly established results.

## GL72-01 — Exact path-gradient identity and a *conditional* classification certificate

Fix a trained model, one receiver's frozen first-block activation `h`, a donor CLS displacement `δ` and a target class `c`. Let `m:[0,1]→R` be the frozen downstream **logit margin** when only the CLS coordinate of `h` is set to `h_CLS+tδ`. Assume `m` is continuously differentiable. By the fundamental theorem of calculus:

`m(1)=m(0)+∫_0^1 m'(t)dt`, `m'(t)=∇_CLS g_c(h_CLS+tδ)·δ`.

Consequently the `n`-point composite midpoint estimate `mhat_n=m(0)+(1/n)Σ_{k=0}^{n-1}m'((k+1/2)/n)` is just **ordinary numerical quadrature of a pathwise gradient**; it is not a special SMFT operator. If additionally `m` is three-times differentiable on the complete path and `|m'''(t)|≤M`, midpoint quadrature has the deterministic bound

`|mhat_n-m(1)|≤M/(24 n²)`.

*Proof:* Apply composite midpoint rule to `f=m'`, whose second derivative is `f''=m'''`; each subinterval of width `1/n` contributes at most `M/(24 n³)` and there are `n` subintervals. Therefore the patch's target-class sign is **certified** if `|mhat_n|>M/(24 n²)`, with the sign of `mhat_n`. A bound on `m''` instead gives a weaker `|mhat_n-m(1)|≤L/(4n)` if `|m''|≤L`. Smoothness and a quantified bound are **new extra assumptions**, not inferred from finite gradient samples. A comparison of several quadrature estimates does not by itself bound `M`. Full-state patch identity and protocol-limited causal Port sufficiency are separate questions.

## GL72-02 — Finite path-gradient samples cannot guarantee finite-patch classification without regularity bounds

Let any predetermined finite set of derivative query points `T={t_1,...,t_q}⊂[0,1]` be fixed. Define `p(t)=∏_{j=1}^q(t-t_j)^2` (if `T` empty let `p=1`), and `I=∫_0^1 p(t)dt>0`. Consider the analytic polynomial

`m_a(t)=-1` and `m_b(t)=-1+(2/I)∫_0^t p(s)ds`.

Both have `m_a(0)=m_b(0)=-1` and for every `t_j`, `m'_a(t_j)=m'_b(t_j)=0`, yet `m_a(1)=-1` and `m_b(1)=+1`. Therefore **no fixed finite sample of the path derivative plus initial value** determines the endpoint sign for all smooth/analytic functions without an admitted bound or model-class restriction. Derivative samples at `t=1` still do not suffice: both derivatives vanish there, while endpoint values differ. This is a logical non-entailment result, not an empirical proof that trained Transformers realize the two polynomials. It refines GL711-01 from a one-point gradient to any finite predeclared path-gradient schedule.

## GL72-03 — New task/split shift: conditional repair by ordinary integration, with strong counterexamples

Pre-registered protocol `EXPERIMENT_PROTOCOL_V72.md`, SHA-256 `611187125db1c5c6b0d30455809d402fe598ed627f28f75161ee231e72c3d091`, defined *before* any v7.2 training. Two task families at a new split, 4 seeds each, AdamW 360 steps: majority seeds 149/151/157/163; 2-bit XOR seeds 167/173/179/181. Each receives 40 heldout receiver→single-bit donor counterfactual attempts. All 8 checkpoints saved; 320 case records, 122 **eligible** oracle-changing/both-correct cases (receiver and donor correctness filtered), of which 106 had a donor originally IN TRAINING. CLS Patch success 68/122 dependent cases: majority [9,15,6,3] of 15; XOR [5/14,16/16,6/16,8/16]. MAJ 4/4 models scored 8/8; XOR 3/4 scored 8/8, seed167 7/8. All model-specific decisions preserved; **not** 122 independent replications.

Ordinary gradient baselines were BASE unchanged, LOCAL initial Jacobian, midpoint PATH-1, PATH-4, PATH-8. A-priori H1 `PATH-8` binary accuracy strictly exceeds LOCAL in ≥5 of ≥6 qualifying models: **PASS 7/8**. H2 `PATH-8` endpoint margin MAE beats LOCAL in ≥6/8 models: **PASS 7/8**. Descriptive H3 majority heterogeneity across 4 fully correct models: **PASS**. These PASS outcomes show **standard quadrature improves an approximation in this local experiment**, not a unique Attractor gain or certified causal quotient. Not monotonic in n, e.g. majority Seed149 PATH-4 MAE 48.98 > PATH-8 8.70 and LOCAL 12.73; XOR Seed173 PATH-8 binary only 4/16, MAE 47.40 > LOCAL 20.03. 8-point finite quadrature can fail markedly.

**Generative residual:** Learn or certify path derivative variation and choose quadrature adaptively under a fixed computation budget, while comparing direct two-endpoint evaluation; require donor-and-receiver both genuinely withheld from training and replicate across new task/splits. Without curvature/regularity bound, GL72-02 forbids universal finite-gradient decision certification. No natural semantic attractor, large pretrained Transformer, independent source-hidden LLM or human analogy creative uplift is demonstrated.


# Incremental v7.3 source-scoped audit nodes (not previously in v7.2 deep aggregate)

# GENERAL_LEMMA_REGISTER_v7.3 — incremental compiler-only research

## GL73-01 — Fully unseen pairs do not imply uniform CLS causal transfer

**Type:** local experimental observation, not theorem about attractors. Protocol locked before model training (SHA-256 in `EXPERIMENTS_V73/design.json`). For seven-bit majority, stratified 96/32 split with 24 changed-label directed heldout-to-heldout pairs, three seeds (191,193,197) reach 32/32 heldout correct. CLS-only patch causal target success is 12/24, 0/24, 7/24; full hidden state patch 24/24 all three. Under same input/output competence and heldout-to-heldout pair design, intermediate CLS intervention varies across learned realizations. This is evidence of implementation heterogeneity under this exact intervention, not proof of a unique functional Port or an SMFT attractor. Patch inputs can be off the naturally reachable activation manifold.

## GL73-02 — Offsite patch is not generally a null control

**Type:** negative empirical control audit. Changing an alternate bit-token hidden state sometimes changes target classification (0/24, 5/24, 5/24 across seeds). Calling this intervention an always-inert negative control is invalid. Appropriate null control requires control matching that is demonstrated to preserve the relevant causal quantity, or predeclared random/sham with measured false-change frequency. The positive full-state replay is tautological under deterministic continuation and does not establish a novel mechanism.

**Evidence scope:** all 240 rows, checkpoint weights, exact 7-bit protocol and rerun script in EXPERIMENTS_V73. Three trained models are experimental replication units; multiple directed pairs are dependent. No broader source claims audited here. Pretrained language semantic attractor, independent LLM reconstruction, creativity gain NOT_RUN.


# Incremental v7.4 source-scoped audit nodes

# GENERAL_LEMMA_REGISTER_v7.4 — source-scoped audit and compiler mathematical guards

**Scope:** Reopened SHA-checked original `SRC-0006` PDF physical pp.95–108 (visual p98,p106); `SRC-0007` physical pp.96–103 (visual p100). Not whole-document deep review. The following formal lemmas are **compiler reconstructions**, not equations copied verbatim from the sources and not general scientific confirmation of SMFT.

## GL74-01 — Projection fidelity is claim-wise entailment, not an untyped scalar ranking

**Source claim:** `SRC-0006` physical p98 §17.5–17.7 states `ProjectionStrength ≤ ReconstructionStrength` (17.16), discusses suppression of negative evidence, and distinguishes recorded, reconstructed, and unresolved claims. Pages 95–102 introduce view invariants and audit-backtracing. The original formula is a **methodological constraint**, not a formally defined real-valued inequality.

**Typed assumptions:** Let nonempty Ω(E) be worlds compatible with the recorded evidence E and reconstruction assumptions; let public projection P assert propositions φ₁,…,φₖ in classical two-valued logic. Then a sufficient fidelity criterion is `∀i ∀ω∈Ω(E), φᵢ(ω)=true` (i.e. `E ⊨ φᵢ`). If the task requires retaining specified contrary evidence, additionally require a declared evidence projection contract; entailment alone does not preserve provenance.

**Countermodel:** Ω(E) has two worlds with exactly the same timestamped external event sequence A then B. B is causally derived from A in only one world. `A precedes B` is entailed; `B was caused by A` is not. No numeric 'confidence' threshold can make a causal claim logically entailed simply because chronological order is well evidenced.

**Conditional repair:** Publish separately `RECORDS`, `SUPPORTS`, `RECONSTRUCTS`, `UNKNOWN`; audit output's explicit entailment obligations under a specified model class and record what counterevidence a lossy projection omits. Probabilistic belief calibration is an additional declared contract, not a substitute for logical implication. **No universal automatic semantic theorem prover is claimed.**

**Reconstructable checks:** `06_BENCHMARK_LOCAL_ONLY/benchmark_v74/research_claims.py`, `test_v74.py`; the finite-world guard is a concrete mathematical countermodel only, not accuracy evidence for an LLM.

## GL74-02 — Agreement of reconstructors cannot identify an observationally hidden genealogy

**Source claim:** `SRC-0006` physical p106 §18.4–18.6 differentiates reconstruction stability from domain truth and grades reconstruction independence. Source p6 acknowledges non-unique reconstruction. **The theorem below is compiler-authored.**

**Typed assumptions:** Two equiprobable worlds ω₀,ω₁ share all admissible observed external traces O, but their target binary genealogical relation G differs. A reconstructor's answer uses only O and independent randomness uncorrelated with hidden G.

**Proof:** Conditional on O, the two labels have equal probability. Any binary predictor outputs a label 0 or 1; expected correct probability is exactly 1/2, including randomized outputs. With unequal prior p the optimum is `max(p,1−p)`. Multiple reconstructors seeing the same O cannot overcome this identification limit by agreement alone. **It can be removed only by new discriminating evidence / additional assumptions**, not by resampling paraphrases.

**Research implication:** Separate reproducibility (inter-annotator or model agreement), source-lineage fidelity and claim truth. For causal genealogy, record explicit prompts, timestamps, revisions, human statements or intervention traces capable of distinguishing worlds; absent these, label the causal edge `UNKNOWN`, not `DERIVES`.

## GL74-03 — Shared-structure recovery needs causal nulls and abstention-aware denominators

**Source claim:** `SRC-0007` physical pp.96–103 §9 defines hidden-invariant synthetic-world assays. p100 gives `FalseInvariantRate = N_false/N_claimed` (9.12) and four types of controls (positive, negative, partial homology, null); p102 discusses removing persistent trace as an intervention. This is **a research proposal**, not an executed independent LLM result.

**Formal guard:** Two finite worlds can show an identical unperturbed event trace despite having opposite structural truth about `Trace -> FutureConstraint`: in world U the mark is passive; in world V it alters future transition. One controlled intervention on the mark distinguishes them. Observational surface similarity alone cannot certify the proposed causal invariant.

**Metric guard:** If `N_claimed=0`, the quoted false-invariant ratio is undefined (0/0). Treat `ABSTAIN_ALL` separately, with coverage and true-invariant recall; do not reward zero claims as zero false-invariant rate. If any claim is unadjudicated, report adjudication coverage rather than silently assigning true/false. Under shared training ancestry, repeated reconstructor agreement does not establish independent replication.

**Negative result:** The current archive contains no executed independent source-hidden LLM assay comparing four collider controls. The local finite examples confirm a risk mechanism only. Synthetic world's simulator truth ≠ new real-world scientific discovery.


# v7.4 Deep Proof Index Repair — restoring historical entrypoint lookup

This appendix restores headings absent in previous cumulative Deep View. Historical registers remain unchanged; original title variants are copied under the exact index-heading alias. Not new proofs.


## GL61-01 — Complex semantic time Wirtinger correction

**Historical primary reference:** `PROOF_DEPENDENCY_RECONSTRUCTION_v6.1.md`. **Inherited audit node**, no new research maturity claim.

```text
## GL61-01 — Incorrect complex-time differential operator in SMFT Rev1

**Original source.** `SRC-0270`, PDF physical p.4, §1.3, eq. (1.2), explicitly defines `ζ=τ+iT` then sets `∂Ψ/∂ζ = ∂Ψ/∂τ+i∂Ψ/∂T`.

**Finite falsifier.** With `f(τ,T)=τ+iT=ζ`, the correct complex derivative is `df/dζ=1`, while the source RHS yields `1+i(i)=0`. Thus the displayed operator cannot be `∂/∂ζ` with the standard complex structure.

**Conditional repair.** For `C^1` functions of independent real coordinates `(τ,T)` use Wirtinger operators `∂_ζ=(∂_τ−i∂_T)/2` and `∂_{bar ζ}=(∂_τ+i∂_T)/2`. For holomorphic functions the second equals 0. If semantic `T` is merely an auxiliary coordinate or no analytic continuation exists, the model must define a different directional operator by name and provide its own meaning; the original equation is not a standard chain rule.

**Preserved.** A complex *coordinate* can be introduced as a modeling convention. The SSLE on real `τ` in §1.4 is a separate phenomenological model and does not depend on the erroneous formal identity for its symbolic definition.

**Atlas:** RA-H01, RA-R06, RA-O01. **Evidence:** source-reopened local mathematical counterexample, not a physical time law.
```

## GL61-02 — POVM completeness with normalized state

**Historical primary reference:** `PROOF_DEPENDENCY_RECONSTRUCTION_v6.1.md`. **Inherited audit node**, no new research maturity claim.

```text
## GL61-02 — POVM completeness requires normalized input state

**Original.** `SRC-0270` PDF physical p.6, §2.2, Theorem 2.5, and p.57 Appendix B. Given `E_φ=O_φ†O_φ` and `Σ E_φ=I`, source states `Σ Pr(φ|ψ)=1`. It implicitly uses `⟨ψ,Iψ⟩=1` in the proof.

**Theorem with full premises.** For any Hilbert-space vector `ψ`, `Σ_φ ||O_φ ψ||²=||ψ||²`. Thus the probabilities sum to 1 **if** `||ψ||²=1`. For a density operator `ρ` with `Trρ=1`, `Σ Tr(E_φ ρ)=1` if effects sum to `I` and are positive. For any outcome with strictly positive probability the normalized Kraus update `O_φψ/||O_φψ||` is well-defined.

**Counterexample.** On one-dimensional `ℂ`, take `E_1=I` and `ψ=2`. The resulting weight is 4, not a probability; source condition `Σ E=I` alone is insufficient. Also mere nonnegative semantic intensity need not be a measurement outcome law without a normalized measurement instrument.

**Preserved.** The intended normalized quantum-inspired measurement theorem is correct when the omitted state normalization is specified. It does not prove biological/neural semantic collapse.

**Atlas:** RA-H01, RA-M12, RA-O01. **Depends on:** `GL52-04`, `GL52-05` only by scope/normalization relation; different underlying dynamics.
```

## GL61-03 — Recursive to declared filtration revision chain

**Historical primary reference:** `PROOF_DEPENDENCY_RECONSTRUCTION_v6.1.md`. **Inherited audit node**, no new research maturity claim.

```text
## GL61-03 — Model lineage: recursion order is not a universal source of time

**Original source sequence within the documents** (historical conceptual relation, no unverified first-publication claim):

- `SRC-0263` PDF pp.1–3,11–13 proposes primitive recursive-generation dependency as *proto-causality*. It explicitly calls the idea a thesis, **not a theorem**.
- `SRC-0266` pp.2–3 critiques recursion as potentially a presentation or construction order, not ontological genesis; p.23 and p.46 proposes viewpoint-selected filtration with ledgered trace as a more general model.
- `SRC-0265` pp.1–2,15,45,51–53 adds Declaration, admissibility Gate, trace and residuals; p.52 explicitly differentiates **event order from causal dependency**. `SRC-0264` pp.1–4 continues the self-revising declaration program, without retroactively validating the earlier proto-time ontology.

**Mathematical separation.** An operation-expression DAG induces a partial dependency order on its nodes, not a unique scalar duration, globally canonical total order, physical metric or interventional causal relationship. Independent subexpressions need no ordering. E.g., two independent leaves `a` and `b` can be evaluated in either order without changing `f(a,b)`; no unique historical clock follows from the mathematical tree alone.

**Conditional result.** A declared policy can select a linear extension/timestamped ledger and produce an *operational* order. But it is external protocol information, not intrinsic inevitability. For causal claims, an intervention or a domain-specific dependency mechanism is needed; observational precedence is insufficient (as `SRC-0265` itself recognizes).

**Atlas:** RA-H01, RA-H05, RA-R06, RA-O01; epistemic relation `REVISED_BY` versus `DERIVES`.
```

## GL61-04 — Trace recurrence versus append-only irreversibility

**Historical primary reference:** `PROOF_DEPENDENCY_RECONSTRUCTION_v6.1.md`. **Inherited audit node**, no new research maturity claim.

```text
## GL61-04 — Trace update recurrence alone does not prove irreversible history

**Original.** `SRC-0265` PDF p.45 gives `L_{k+1}=UpdateTrace_P(L_k,τ_k,R_k,GateMeta_k)`; p.52 uses an unqualified `TraceUpdate ⇒ irreversibility` (8.30) and the thesis of an ordered irreversible ledger (8.42).

**Falsifier.** Take a valid update `U(L,e)=L+[e]` and a later allowed reset `Reset([e])=[]`. The system can return to the same materialized state. More directly, `U(L,e)=e` overwrites its previous state. A recurrence `L_{k+1}=U(L_k,e_k)` does not prevent either. Thus a timestamp, a ledger label or an update equation alone cannot make history irreversible.

**Qualified engineering theorem.** If event records are persistently append-only, cannot be erased by authorized actions, timestamps/identity are authenticated and replay semantics preserve order, the stored *event history* is monotone with respect to its prefix partial order. Even then the application state can be logically reverted by appending a compensating event; append-only persistence is not identical to a thermodynamic arrow of time or a formal theorem of physical irreversibility.

**Atlas:** RA-E05, RA-H05, RA-R07, RA-O08. **Related:** `GL57-05`, `GL57-06` on ordered event replay and external truth; do not infer all traces are tamper-proof.

## Cross-source boundary

`SRC-0270` and `SRC-0263` are genuine source statements; `GL61-*` are new *compiler mathematical/audit nodes*, not new original Witnesses W401+. The late-source filtration/declaration program deliberately revises the earlier recursive-pre-time analogy. Retain the early creative hypothesis as historical generative content, but mark its claimed universality and physical implication open. Prior four conditional model theorem components RA-M01..RA-M04 remain unchanged; no new scientific component is promoted.
```

## GL68-01 — Closed-loop intervention needs end-to-end observable wiring

**Historical primary reference:** `GENERAL_LEMMA_REGISTER_v6.8.md`. **Inherited audit node**, no new research maturity claim.

```text
## GL68-01 — Closed-loop intervention needs end-to-end observable wiring

Define nominal controlled model `x_{t+1}=a*x_t+u_t` and actual simulator `x_{t+1}=a*x_t+(1+g_t)u_t+b_t+epsilon_t`. The controller only sees its measured history `(x,r,u)`, with innovation `r_t=x_{t+1}-(a*x_t+u_t)`. A detector can signal `alarm_t=1` yet have **no causal effect** if the estimator is not fed the recorded residuals. Initial local implementation accidentally failed to write `prev_r[:,t]=r`; measured every policy's performance exactly equalled fixed-feedback despite nonzero alarms. The end-to-end wiring was corrected and a regression guard added: learned-action performance must differ from fixed-feedback in bias conditions. This is an implementation discovery, not a theorem about natural AI semantics. Open-loop alert counts cannot establish controller response.
```

## GL68-02 — Closed-loop cost gain is model-conditional, not universal

**Historical primary reference:** `GENERAL_LEMMA_REGISTER_v6.8.md`. **Inherited audit node**, no new research maturity claim.

```text
## GL68-02 — Closed-loop cost gain is model-conditional, not universal

Experiment: six regimes × 680 unseen episodes × 80 time steps, same exogenous noise sequences for six policies, disjoint 2,800-episode normal training and 5,000-episode normal detector calibration. Nominal `a=.74`, feedback `u=clip(-.82*x,-1,1)`, after alarm additive adaptation `-clip(mean(previous 10 observed innovations),-.5,.5)`. Hidden bias `b=±.22` after time index 30. Across positive bias, cumulative cost `sum_t(x_{t+1}²+.045u_t²)` means fixed=3.988999, magnitude=2.495080, dual=2.379092, standard signed CUSUM=2.389382; negative bias fixed=4.007648, magnitude=2.498147, dual=2.382505, CUSUM=2.390292. No hidden bias/time used for the deployed detectors. **Measured under this synthetic controlled family only.** Cost comparison is paired, not an independent replication.
```

## GL68-03 — Noise-only change is a deliberately adverse negative control

**Historical primary reference:** `GENERAL_LEMMA_REGISTER_v6.8.md`. **Inherited audit node**, no new research maturity claim.

```text
## GL68-03 — Noise-only change is a deliberately adverse negative control

When innovation variance (not hidden mean bias) doubles, the same alarm+recent-mean correction mistakenly takes temporary noise as persistent bias; cumulative mean cost fixed=5.367903 vs magnitude=5.778363, dual=5.749312, standard signed CUSUM=5.704055. Thus a structurally reasonable directional residual alarm does not by itself justify *which* model revision/action to take. An active diagnosis step (persistent mean vs variance vs action gain) is a constructive proof/test residual. This restricts blind transition from detector significance to causal diagnosis.
```

## GL68-04 — Equal-information standard statistical baseline is indispensable

**Historical primary reference:** `GENERAL_LEMMA_REGISTER_v6.8.md`. **Inherited audit node**, no new research maturity claim.

```text
## GL68-04 — Equal-information standard statistical baseline is indispensable

Dual detector scans both signed and magnitude moving windows (8,16); signed CUSUM uses **the same observed signed residual sequence**, not an Attractor-specific statistic. Each detector separately calibrates the 95th percentile of its whole 80-step maximum on 5,000 independent null streams. On a separate stationary batch of 1,000 full null traces, conventional magnitude, dual and CUSUM alarms were respectively 47,49,40, illustrating finite-sample rather than universal false-alarm guarantees. In hidden bias conditions dual cost 2.379/2.383 versus CUSUM 2.389/2.390: marginal differences; no attributable exclusive Attractor benefit. Thresholds are not mathematically valid indefinitely or under distribution shift.
```

## GL68-05 — Closed-loop residuals confound hidden bias with actuator gain

**Historical primary reference:** `GENERAL_LEMMA_REGISTER_v6.8.md`. **Inherited audit node**, no new research maturity claim.

```text
## GL68-05 — Closed-loop residuals confound hidden bias with actuator gain

For the controlled plant, the observable innovation is `r_t=b_t+g_t u_t+epsilon_t`. For a fixed intervention value `u0`, pairs `(b,g)` and `(b+c*u0,g-c)` produce identical conditional innovation means, so even infinitely many exact observations at fixed `u0` cannot separately identify bias and gain. Identification needs sufficiently varied declared interventions (persistent excitation) or independent structure/prior bounds. An alarm or even exact residual sign cannot tell the mechanism in isolation; adaptive control changes the innovation process when `g≠0`, invalidating naive exogenous replay comparisons. This is a simple model-level identifiability lemma, NOT evidence that the semantic attractor exists.
```

## GL68-06 — Policy-specific causality and oracle separation

**Historical primary reference:** `GENERAL_LEMMA_REGISTER_v6.8.md`. **Inherited audit node**, no new research maturity claim.

```text
## GL68-06 — Policy-specific causality and oracle separation

All six tested policies change `u_t` within the simulator and therefore causally affect later `x`, unlike v6.7 open-loop counterfactual abstention. In gain-shift conditions `g=.35` after time 30, controller actions also affect subsequent residuals. Distinct policies use **identical sampled exogenous shocks and hidden regime paths** for paired evaluation, but generate different closed-loop states/innovations. A privileged `oracle_bias` controller reads hidden `b_t`; it is an illustrative unattainable comparator and must not be included in matched-information ranking. The no-control (`u=0`) baseline is also reported, and is a different opportunity-cost comparator from fixed feedback. A quadratic proxy cost and arbitrary |x|>.45 surrogate do not imply real safety.
```

## GL68-07 — Research-Kernel Skill: repair → residual → discriminating experimental designs

**Historical primary reference:** `GENERAL_LEMMA_REGISTER_v6.8.md`. **Inherited audit node**, no new research maturity claim.

```text
## GL68-07 — Research-Kernel Skill: repair → residual → discriminating experimental designs

`SRC-0298`'s two-channel idea becomes a falsifiable synthetic test only once source boundary, observables, rival standard methods, negative controls, and action effects are declared. Three reusable conceptual safeguards: (i) instrument that a detected signal actually enters the action pathway, (ii) separate mean drift, variance and gain-change diagnoses, and (iii) evaluate both technical accuracy and total intervention utility under held-out regimes. Optional SMFT/Attractor analysis must be a separately toggled explanatory model compared to equal-information standard CUSUM/control, not an automatic promotion. User analogies must be translated into falsifiable *predictions*, boundary checks and rival mechanisms. This run did NOT test whether supplying Attractor mathematics or user analogy improves LLM scientific creativity.
```

## GL69-02 — Class geometry is coordinate dependent

**Historical primary reference:** `GENERAL_LEMMA_REGISTER_v6.9.md`. **Inherited audit node**, no new research maturity claim.

```text
## GL69-02 — Class-geometry coherence without a declared metric is representation dependent

Let two labeled classes in R² be `A={(0,0),(2,0)}`, `B={(0,1),(2,1)}`. Euclidean within-class distance is 2 and the nearest inter-class distance is 1, hence raw distance cohesion is poor. Under invertible rescaling `S_k(x,y)=(x,ky)` for k>2, within-class distance stays 2 but vertical inter-class distance becomes k, reversing that nearest-neighbor relation. A downstream function can compensate with `S_k^{-1}` and retain identical input/output behavior. This is a function-factorization counterexample; **not** a claim that every invertible matrix is a symmetry of every fixed LayerNorm Transformer architecture. Any representation metric is legitimate only after its coordinate convention, permissible equivalence transformations and measurement test are declared.

**Links:** `SRC-0258` pp.4,7 (protocol and proxy stability); `RA-O01`, `RA-M01`. **Evidence:** exact finite mathematical counterexample. It constrains interpretations; it does not imply learned representation geometry is useless.
```

## GL69-03 — Untrained feature linear probe disconfirms emergence-only proxy

**Historical primary reference:** `GENERAL_LEMMA_REGISTER_v6.9.md`. **Inherited audit node**, no new research maturity claim.

```text
## GL69-03 — Zero-step representation decoding is a positive learning-proxy falsifier

**Question posed before measurement:** Does class geometry itself appear only when the small Transformer acquires task behavior? CPU PyTorch experiment trained two real `TransformerEncoderLayer` blocks on majority of five binary inputs. Fixed balanced split: 24 train, 8 held out, three model seeds 17/23/41; checkpoints `0,20,60,120,240`; three additional training-label permutation controls (shuffled only training labels). A separate ordinary sklearn RidgeClassifier is trained on labeled train-split CLS features at each checkpoint; this probe **is supervised** and its result must never be called untrained zero-shot neural understanding.

**Observation:** At initialization, the original network itself scores 4/8 heldout (chance-level here) on all three seeds, but the ordinary supervised Ridge probe reaches **8/8** heldout from all three *untrained Transformer features*. Thus the stronger proposed proxy "class decodability first emerges with task competence" is falsified **in this selected small model and split**; there is an obvious standard baseline requiring no learned semantic attractor. After 20 steps, actual model gets 8/8 in each seed; fixed checkpoint spacing is too coarse to identify sharpness, delayed grokking or a critical surface. The final three shuffled-training-label controls achieve 3/8, 5/8, 4/8 on true heldout labels. Random-label controls are not entirely powerless (part of the task structure can persist in random input features) and three seeds/8 examples are underpowered for broad transfer claims.

**Surviving weak claim:** cross-checkpoint representational diagnostics can be *tested* as prospective predictors under harder tasks, preregistered thresholds, multiple splits, matched linear probes and independent replicates. **Not inferred:** proof of semantic attractor, causality of geometric clustering, sudden understanding, originality relative to prior grokking work.
```

## GL69-04 — Single-site causal transplant fails on label-changing counterfactual

**Historical primary reference:** `GENERAL_LEMMA_REGISTER_v6.9.md`. **Inherited audit node**, no new research maturity claim.

```text
## GL69-04 — Internal single-token patch fails when true counterfactual output must change

At checkpoints 0,120,240, for every heldout receiver and each of five input bits, create donor differing at exactly that bit; replace the **post-layer-1 representation of only that bit token** with donor's value; finish layer 2. The full counterfactual forward pass is the ordinary matched control (replace whole input and recompute all activations). Store all 720 cases, including shuffled-label runs. At final step in trained true-label runs, there are 120 patch cases (3 seeds × 8 receivers × 5 bits), of which 45 have a changed correct label. Targeted single-token patch yields correct label on **0/45 changed-label** cases, and does not flip original output in any of those 120 cases; complete input counterfactual is correct on all 120. The patch is correct for 75/75 unchanged-label cases, so its overall 62.5% is misleading if unstratified.

**Inference boundary:** this precisely falsifies *the chosen single-site transplant sufficiency* in this trained model; it does not refute distributed computation, other token/layer choices, multi-site activation patching, formal Port existence, or semantic attractor ontology. The right next experiment is registered multi-site patching with matched sham and off-manifold controls, with a causal correction score conditioned on label-changing samples, plus exact fiber congruence on declared interventions (cf. `GL50-01`, `GL59-01`).

**Explicit allowed statuses:** proxy disconfirmation in a trained synthetic-domain Transformer `M4_LOCAL_NEURAL`; whole semantic-attractor hypothesis `OPEN/NOT_TESTED`; independent source-hidden LLM `NOT_RUN`; Attractor/Human analogy creativity benefit `NOT_RUN`.
```

## GL711-02 — Prospective cross-seed frozen-architecture patch test

**Historical primary reference:** `GENERAL_LEMMA_REGISTER_v7.1.1.md`. **Inherited audit node**, no new research maturity claim.

```text
## GL711-02 — Eight prospectively specified seeds reveal nonunique CLS sufficiency, and first-order predictor fails at binary benefit

**Protocol written and SHA256-locked before new-seed execution:** `EXPERIMENT_PROTOCOL_V71_CONTINUATION.md` (SHA `6f369c2ac5795a1d120289507afa53c23880111972aef4b610dc214f59f21f5a`). Same architecture, optimizer and fixed 24/8 split as v6.9; independent initialization seeds `101,103,107,109,113,127,131,137`, all trained 240 steps and reached 8/8 heldout oracle accuracy. Four separately trained permuted-label controls were also executed; their oracle correctness is substantially lower, so few counterfactual cases satisfy the conditional both-correct filter.

For 15 label-changing, both-correct receiver/donor cases per normally trained seed, post-layer1 CLS-only donor activation replacement succeeded: `15,15,15,15,9,9,15,0` out of 15, respectively. Total `93/120` patches across **eight models, not 120 independent replications**. Five models show complete success, two partially succeed, one completely fails. At the same point full intermediate-state donor readout is a compositional positive control, not emergence evidence. An off-target single bit token succeeded in 2/120 changing-label cases, illustrating imperfect negative-control isolation.

The **prospective ordinary-gradient prediction** `m_hat=m_x+∇_CLS m_x ·(h_y[CLS]-h_x[CLS])`, with no fitted threshold, outperformed the 'unchanged receiver' binary outcome predictor in **0/8** new seeds (H1 predeclared threshold 6/8 **FAILED**). Continuous donor-margin absolute error was lower in **7/8** new seeds (H2 6/8 directional threshold met); per-seed relative reduction has median ≈0.65%, one seed degrades, and there is no binary decision gain. An 'always donor' optimistic reference correctly predicts 93/120, whereas the first-order and unchanged-receiver predictors each correctly predict 27/120. Accuracy for all eight seeds is identical, but localization is not. This is a weak-fidelity local approximation/conditional causal assay, not a proof of a general mechanistic predictor, semantic Attractor, or model-agnostic functional state quotient.

**Limits:** same fixed dataset split across all new models, oracle-target donor selection, 11/15 donors belong to the training split per model, correlated counterfactual cases and shared architecture. Different seeds are distinct model initializations but not independent task datasets. This does NOT perform a pretrained LM attractor study or source-hidden independent LLM kernel reconstruction. Only 13 new continuation-specific QA checks rerun, plus the historical v7.1 verifier; historical 866/866 project-wide tests remain an unrerun historical result.

**New residual:** measure the entire receiver→donor interpolation trajectory and locate threshold/curvature; prospective score based on separately trained mediation predictors under task/architecture shift; distinguish off-manifold patch artifacts from true mechanism via matched distribution and intervention admissibility. Use equal-information standard gradient/integrated-path/causal mediation baselines; compare experimental cost and statistical uncertainty clustered by model.
```

## GL72-01 — Exact path-gradient identity and a conditional classification certificate

**Historical primary reference:** `GENERAL_LEMMA_REGISTER_v7.2.md`. **Inherited audit node**, no new research maturity claim.

```text
## GL72-01 — Exact path-gradient identity and a *conditional* classification certificate

Fix a trained model, one receiver's frozen first-block activation `h`, a donor CLS displacement `δ` and a target class `c`. Let `m:[0,1]→R` be the frozen downstream **logit margin** when only the CLS coordinate of `h` is set to `h_CLS+tδ`. Assume `m` is continuously differentiable. By the fundamental theorem of calculus:

`m(1)=m(0)+∫_0^1 m'(t)dt`, `m'(t)=∇_CLS g_c(h_CLS+tδ)·δ`.

Consequently the `n`-point composite midpoint estimate `mhat_n=m(0)+(1/n)Σ_{k=0}^{n-1}m'((k+1/2)/n)` is just **ordinary numerical quadrature of a pathwise gradient**; it is not a special SMFT operator. If additionally `m` is three-times differentiable on the complete path and `|m'''(t)|≤M`, midpoint quadrature has the deterministic bound

`|mhat_n-m(1)|≤M/(24 n²)`.

*Proof:* Apply composite midpoint rule to `f=m'`, whose second derivative is `f''=m'''`; each subinterval of width `1/n` contributes at most `M/(24 n³)` and there are `n` subintervals. Therefore the patch's target-class sign is **certified** if `|mhat_n|>M/(24 n²)`, with the sign of `mhat_n`. A bound on `m''` instead gives a weaker `|mhat_n-m(1)|≤L/(4n)` if `|m''|≤L`. Smoothness and a quantified bound are **new extra assumptions**, not inferred from finite gradient samples. A comparison of several quadrature estimates does not by itself bound `M`. Full-state patch identity and protocol-limited causal Port sufficiency are separate questions.
```

## GL73-01 — Fully unseen CLS port transfer heterogeneity

**Historical primary reference:** `GENERAL_LEMMA_REGISTER_v7.3.md`. **Inherited audit node**, no new research maturity claim.

```text
## GL73-01 — Fully unseen pairs do not imply uniform CLS causal transfer

**Type:** local experimental observation, not theorem about attractors. Protocol locked before model training (SHA-256 in `EXPERIMENTS_V73/design.json`). For seven-bit majority, stratified 96/32 split with 24 changed-label directed heldout-to-heldout pairs, three seeds (191,193,197) reach 32/32 heldout correct. CLS-only patch causal target success is 12/24, 0/24, 7/24; full hidden state patch 24/24 all three. Under same input/output competence and heldout-to-heldout pair design, intermediate CLS intervention varies across learned realizations. This is evidence of implementation heterogeneity under this exact intervention, not proof of a unique functional Port or an SMFT attractor. Patch inputs can be off the naturally reachable activation manifold.
```

## GL73-02 — Offsite patch fails strict null validity

**Historical primary reference:** `GENERAL_LEMMA_REGISTER_v7.3.md`. **Inherited audit node**, no new research maturity claim.

```text
## GL73-02 — Offsite patch is not generally a null control

**Type:** negative empirical control audit. Changing an alternate bit-token hidden state sometimes changes target classification (0/24, 5/24, 5/24 across seeds). Calling this intervention an always-inert negative control is invalid. Appropriate null control requires control matching that is demonstrated to preserve the relevant causal quantity, or predeclared random/sham with measured false-change frequency. The positive full-state replay is tautological under deterministic continuation and does not establish a novel mechanism.

**Evidence scope:** all 240 rows, checkpoint weights, exact 7-bit protocol and rerun script in EXPERIMENTS_V73. Three trained models are experimental replication units; multiple directed pairs are dependent. No broader source claims audited here. Pretrained language semantic attractor, independent LLM reconstruction, creativity gain NOT_RUN.
```


## v7.5 current proof append (compiler source-scoped review)
- **GL75-01** GL75-01 — Rayleigh dissipation path-variation / force-derivative non-equivalence; ORIGINAL_SOURCE_CONTRADICTION_COMPILER_ELEMENTARY_PROOF; scoped original SRC-0048; read `90_PROVENANCE/GENERAL_LEMMA_REGISTER_v7.5.md`.
- **GL75-02** GL75-02 — Structural quadratic penalty is a potential, not an automatic dissipation theorem; ORIGINAL_SOURCE_CONTRADICTION_COMPILER_COUNTERMODEL; scoped original SRC-0057; read `90_PROVENANCE/GENERAL_LEMMA_REGISTER_v7.5.md`.
- **GL75-03** GL75-03 — LuoShu line constraints are rank seven; finite hinge is not a hard wall; ORIGINAL_SOURCE_CONTRADICTION_COMPILER_LINEAR_ALGEBRA; scoped original SRC-0057; read `90_PROVENANCE/GENERAL_LEMMA_REGISTER_v7.5.md`.


---

# v7.6 additional scoped compiler lemmas

# GENERAL_LEMMA_REGISTER_v7.6 — executable LuoShu flow comparison and conditional mathematics

**Nature:** new compiler-authored formal mathematics and 96-initialization synthetic numerical experiment inspired by *previously scoped* v7.5 readings `SRC-0048`/`SRC-0057`. **No newly certified source full-text audit.** Ordinary linear algebra and mechanics; not natural-science or unique SMFT mechanism validation. Pilot n=32 preceded final n=96: **exploratory, NOT preregistered**.

## GL76-01 — A rank-deficient quadratic flow converges to a set with initialization-dependent selection

Let `A∈R^{8×9}` be the three row, three column, two diagonal line-sum matrix, `b=15 1_8`, with nonempty feasible affine set `F={q:Aq=b}` and `rank A=7`. Set `V(q)=½||Aq−b||²` and `H=AᵀA` (rank 7). Since `∇V=H(q−q*)` for any `q*∈F`, standard explicit-gradient flow

`q_(n+1)=q_n−η Aᵀ(Aq_n−b)`, with `0<η<2/λ_max(H)`, converges to

`q_inf=q_0−A⁺(Aq_0−b)=argmin_{z∈F}||z−q_0||²`.

**Proof:** decompose `q_0−q*` in orthonormal eigenvectors of symmetric PSD H. Nonzero-eigenvalue modes are multiplied by `(1−ηλ)^n→0`; two kernel modes remain invariant. An affine feasible q* exists (e.g. classic LuoShu), and projection onto `ker A` is conserved by the gradient updates. Thus the limit is the unique Euclidean *projection relative to q0*, not a unique global state selected independently of q0. The exact algebraic projection requires no trajectory limit.

**Negative control:** `q0=qclassic+3.5 v` for nonzero `v∈ker A` is feasible but not a 1–9 digit permutation. Its gradient is zero and it remains fixed. The source-derived claim 'unique attracting configuration' does not follow from these eight relaxed real constraints. Other discrete/symmetry constraints can change the conclusion; declare them.

## GL76-02 — Correct energy dissipation does not imply optimal finite-budget computation or a unique target

For a fixed symmetric PSD `H=AᵀA` and `V=½||Aq−b||²`, declare the *mechanical* dynamics `qdot=v`, `vdot=−c v−∇V(q)` for `c≥0`. Then `E=½||v||²+V(q)` satisfies the **continuous-time identity** `Edot=−c||v||²`. For `c=0` energy is conserved and generic trajectories oscillate in nonzero-eigenvalue modes; for `c>0`, those modes decay. With `v(0)=0`, nullspace components remain the initial ones: long-time point selection still depends on `q0`. The claim follows from declared equations, not the earlier erroneous action variation.

**Local numerical experiment:** 96 deterministic initializations, 400 one-gradient-evaluation iterations, ordinary GD vs exactly renamed LoShu GD vs semi-implicit Euler damped mechanics (`c=2,h=0.04`) vs undamped mechanics. A direct pseudoinverse baseline separately measures exact feasibility, but involves a different setup cost and is **not a matched computational-budget method**. Final fraction with `||Aq−b||<1e−6`: projection 96/96, GD 96/96, renamed GD 96/96, damped 3/96, undamped 1/96. The ordinary and relabelled GD trajectories agree bitwise; no novel LoShu computation is established. Results strongly depend on fixed steps, tolerances and integrator. The discrete numerical scheme is not asserted to obey the exact continuous-time E identity.

**Evidence:** `90_PROVENANCE/EXPERIMENTS_V76/summary.json`, all per-step traces, `06_BENCHMARK_LOCAL_ONLY/benchmark_v76/run_luoshu_v76.py`; no independent outside replication. This tests a synthetic dynamics *defined by compiler*, not actual SMFT/physical attractor.

## GL76-03 — Smooth line-sum relaxation cannot by itself encode distinct 1–9 digits

The vector `q=(5,5,5;5,5,5;5,5,5)` satisfies **all eight** line-sum constraints `Aq=b`, belongs to the box `[1,9]^9`, and has `V(q)=0`, yet repeats the digit 5 nine times. Thus even adding a **box** constraint does not imply 'each digit used exactly once'. Exhaustive enumeration of all `9!=362880` bijective digit assignments returns **eight** satisfying the line sums, representing the classical D4 symmetry orbit; a unique point only follows after an explicitly declared symmetry quotient or symmetry-breaking orientation.

In 96 runs all iterative/end-projection solutions satisfied neither an exact 1–9 permutation nor a preferred classical pattern (0/96 in every method). The zero count is a scoped numerical observation; the all-five construction is the rigorous counterexample. Finite soft penalties, rounding, or simple smooth descent cannot be assumed to implement discrete assignment and symmetry selection: test them against a standard discrete constraint solver. The relaxed 2D real feasible manifold is not the same state space as the eight digit permutations.

### Open research residual
Compare genuine mixed-integer or permutation projection and symmetry-aware quotient controllers on an independently relevant optimization problem, with matched computation/accuracy budget. If ordinary projection/standard discrete solvers dominate, record the negative result and restrict any special attractor claim. To demonstrate physical dissipative dynamics needs real observables and measured state evolution; to demonstrate kernel's reconstruction advantage needs external blind LLM tests. **Independent LLM Reconstruction NOT_RUN.**


# GENERAL_LEMMA_REGISTER_v7.7 — discrete LuoShu classification and symmetry-selection audit

**Provenance:** SHA-verified bounded original reading of `SRC-0107` physical PDF pp.8–10,13 and `SRC-0104` pp.15–17, with source-specific claims recorded in `V77_SOURCE_SCOPE_AND_CLAIM_AUDIT.md`. Mathematics, the polynomial candidate, synthetic optimizer and adversarial experiments here are **new compiler-authored work**, not mathematical proofs supplied by the original authors. No real semantic memory, physics or independent LLM test.

## GL77-01 — Complete affine parametrization and exact discrete LuoShu orbit

For nine real variables in a 3×3 grid satisfying three row sums, three column sums, and two diagonal sums all equal 15, the constraint matrix has rank 7. Its complete solution set is precisely:

```
L(a,b) = [[5+a,   5-a-b, 5+b],
          [5-a+b, 5,     5+a-b],
          [5-b,   5+a+b, 5-a]],   a,b in R.
```

**Proof:** Sum the central row/column and two diagonal equalities to show the center is 5; from the middle-point opposite-pair equations, opposite entries total 10. Set top-left=5+a, top-right=5+b. Substitution of remaining row/column sums forces all other entries as displayed. Conversely all eight sums are directly 15, and `a,b` are independent (rank seven). For the entries to be exactly the distinct digits 1..9, the four opposite-pair offsets must be {1,2,3,4} in absolute value, hence `{|a|, |b|, |a+b|, |a-b|}={1,2,3,4}`. The largest absolute offset equals `|a|+|b|=4` (for any real a,b). Since |a|,|b| are among {1,2,3,4} and distinct, either {1,3} or (hypothetically) {2,2} (ruled out by distinctness), so exactly `{|a|,|b|}={1,3}`. Conversely the eight choices `(±1,±3)` and `(±3,±1)` give every offset ±1..±4 once and form a single orbit under the square's D4 rotations/reflections. Brute-force 9!=362880 permutations also gives exactly 8. Uniqueness holds **modulo D4**, not as an oriented 3×3 grid.

**Scope:** classification of the chosen *mathematical premises*, not evidence that slot values are natural capacities of semantic trace or that the pattern has unique dynamical stability. Relates to earlier rank/constraint residual GL75-03 and GL76-03.

## GL77-02 — Symmetry-stabilizer obstruction to globally deterministic equivariant orientation

Let `X=R²` carry the D4 action induced by rotating or reflecting L(a,b) and `Y` be its orbit of eight distinct LuoShu solutions. D4 acts freely/transitively on Y. There is **no total D4-equivariant deterministic selector** `f:X→Y`. Indeed x=(0,0) is fixed by all of D4. Equivariance gives `f(x)=f(gx)=g f(x)` for every g, which would require a point in Y fixed by all g; none exists. This argument does not require continuity. Even away from x=0, points on a reflection axis have nontrivial stabilizer and cannot be mapped equivariantly into a free D4 orbit.

A deterministic nearest-of-eight selector can be defined with an explicit **tie-breaking orientation**, but its tie states necessarily break equivariance. A randomized equivariant output distribution, extra orientation/observer variable, asymmetric boundary condition, or a set-valued solution can avoid the deterministic-total-selector assumption. The theorem establishes an information/symmetry requirement, not SMFT Observer ontology or semantic cognition.

## GL77-03 — Conditional invariant polynomial potential, symmetric-trap controls and entropy non-selection

**Compiler candidate:** `F(a,b)=(a²+b²−10)²+(a²b²−9)² ≥ 0` is D4-invariant; zero requires `a²+b²=10` and `a²b²=9`, so its global zero set consists exactly of the eight LuoShu points of GL77-01. Its ordinary gradient descent is a constructive engineered optimization, not spontaneously emergent physical/semantic dynamics. Since ∇F(0,0)=0 and the axes are invariant under its exact gradient flow, origin and axial initial states cannot reach the off-axis targets without symmetry-breaking perturbation. Potential value at origin is 181; origin is not a valid magic-digit permutation.

**Executed synthetic benchmark:** `06_BENCHMARK_LOCAL_ONLY/benchmark_v77/luoshu_v77.py`, protocol SHA recorded in report, 128 seeded normal starts + 5 degenerate starts. All 128 generic starts hit the orbit (within 1e−4) but **none of the five axis/center starts** did; standard exact enumeration of eight choices supplies a simpler always-valid reference without numerical convergence. Median solver evaluation count 596. The eight magic squares result from the already engineered polynomial's exact zero set, not proof of any unique SMFT advantage. 9! exhaustive historical-math checker has verification cost distinct from nearest-eight runtime. Timing is workstation-dependent and not fair matched-resource comparison.

**Source-entailment counterexample:** `SRC-0107` p.8 states repeated values necessarily lower sum below 45, refuted by all-five (sum=45 and every magic line=15). `SRC-0107` p.9 defines Shannon entropy with `p_j=S_j/45`: for the required multiset {1,...,9}, this entropy is invariant under all permutations and therefore cannot choose a LuoShu arrangement. If repeats are allowed, all-five yields entropy ln(9)≈2.1972245773 versus H(1..9)≈2.0498407204, so the specific 1..9 profile is *not* maximum entropy on the larger relaxed nonnegative capacity set. Neither case proves or disproves real semantic stability, which requires separately measured operational definitions.

## Research residuals and tests

1. If a purported LuoShu attractor has genuine functional advantage, define a task requiring direction/orientation, an observation protocol and plain discrete-assignment or standard nonconvex optimization baselines. Distinguish semantic dynamics from a hand-coded orbit potential.
2. Measure whether an extra orientation variable can be inferred or externally supplied. A strict symmetry-requiring system cannot *deterministically* select a unique oriented result from symmetric states without such extra information.
3. Avoid promoting entropy/line-sum constraints to stability or retrieval performance. Evaluate an actual application with matched compute and proper controls.
4. Source original `SRC-0104/0107` bounded review not full-depth; external independence and LLM reconstruction `NOT_RUN`.


---

# V7.8 NEW EXACT FINITE-STATE AUDITS

# General Lemma Register v7.8 — Strong-attractor target leakage and finite-state limits

## GL78-01 — Nine D4 orbits in the 3x3 row-column balance manifold

Let Ω be all permutations of digits 1,...,9 arranged on a labelled 3×3 square; |Ω|=9!=362880. Let each of the three row sums and three column sums be 15, where 15=45/3 is fixed by total mass. A fully enumerative exact finite proof, executable with `luoshu_emergence_v78.py` and `test_v78.py`, establishes exactly 72 such configurations, partitioned into exactly nine disjoint free D4-orbits, each of size 8. Exactly one orbit satisfies both diagonal sums of 15; the other 64 configurations fail at least one diagonal. The nine orbits respectively contain a center entry 1,...,9, constant within each orbit. If only one specified diagonal is additionally balanced, 24 assignments remain, of which 8 satisfy both. With both diagonals balanced, 8 remain, one D4-orbit (GL77-01).

The count 'nine' is a **number of symmetry orbits in a static finite set**, NOT a nine-state periodic dynamical law. Proof level is exhaustive reproducible finite-state enumeration, not a source theorem or independent physical measurement. Premises hard-code a 3×3 grid and digits 1..9, so this is conditional combinatorics, not unprompted LuoShu emergence.

## GL78-02 — Infinite-strength Gibbs no-go for LuoShu selection under insufficient constraints

Define E_RC(p)=∑rows (sum−15)^2+∑cols (sum−15)^2 and E_RC1 adding one diagonal residual; E_FULL additionally adds the other diagonal residual. Let π_β(p)=exp(−β E(p))/Z_β for p∈Ω, β≥0, and M be the eight fully magic permutations.

For each energy, E(p)≥0, E(p)=0 precisely on its listed minimizer set, and E=0 on M. Because Ω is finite, `lim_{β→∞} Z_β = #zeros`, while `∑_{p∈M}exp(−βE(p))=8` at every beta. Hence the exact conditional limits are:

```
model       |Ω|  zero-energy minima   P_beta→infty(M)
NULL        362880   362880            8/362880
RC          362880       72            8/72=1/9
RC+one-diag 362880       24            8/24=1/3
FULL        362880        8            8/8=1
```

Since Z_β≥ #zeros for every β, RC P(M)≤1/9, RC1 ≤1/3. In these models greater β strengthens concentration but cannot distinguish equal-energy ground states. FULL makes the target a priori by encoding **both** diagonal constraints. This no-go holds for this **specific reversible stationary Gibbs family** with an unweighted permutation reference measure; it does NOT prohibit asymmetric priors, non-equilibrium kinetic selection, active control, noise-induced selection, or genuinely different local fields. Large β is not an unconditional measure of physical 'attractor strength'.

## GL78-03 — Kinetic traps, objective leakage and falsifiable continuation

Actually executed ordinary, pair-swap strict steepest descent from 128 fixed pseudorandom permutations for RC and FULL (identical 128 starting states; up to 200 strict-improvement iterations). The RC local solver reached zero penalty 75/128, with only 5/128 final configurations fully magic; 53/128 were trapped at positive penalty. The FULL target-encoded solver reached zero 102/128, and all 102 zero-penalty states were fully magic; 26/128 ended above zero. These observations demonstrate local optimization can differ from infinite-time finite Gibbs equilibrium; no general rate or natural attractor is inferred. FULL's apparent advantage is target-definition leakage by including the diagonal conditions. More general self-organization requires separately measured dynamics and observables without target-specific objective. Do not report FULL as evidence of SMFT unique engineering efficacy.

## Residual: how to discriminate genuine bottom-up emergence

Find priors weaker than 3×3-digit/permutation/line-sum and define local-neighbor dynamics with spatial and temporal observables; test held-out diagonal and orbit structure, negative controls, representation invariances, and performance relative to ordinary solvers. This v7.8 result is compiler-authored mathematics plus scoped local synthetic computation. It cites SRC-0104/0107 **only as inherited bounded theoretical antecedents**; NO new original source deep-read. Transformer LuoShu natural emergence, independent source-hidden LLM reconstruction and creativity gain = NOT_RUN.


---

# V7.9 STRICT LOCAL PAIR POTENTIAL AUDITS

# General Lemma Register v7.9 — Uniform local interactions, engineered selection and kinetic barriers

> Provenance: New compiler-authored mathematical results building on v7.7/v7.8 finite LuoShu antecedents. No new original PDF/DOCX source deep read. `SRC-0104/0107` represent inherited bounded primary-source context, NOT independent confirmation of this v7.9 construction. Local finite synthetic evidence only.

## GL79-01 — Strict local smoothing cannot make LuoShu a global ground state

Let Ω=S9 be all placements of distinct integers 1,...,9 on a **pre-chosen** labelled 3×3 grid. Let G have the twelve horizontal/vertical nearest-neighbour edges. For any strictly increasing real function V on {1,...,8}, define E_V(p)=∑_(i,j)∈G V(|p_i−p_j|). For every LuoShu magic permutation L, the ordered multiset of its twelve edge differences is `[1,1,2,2,4,4,5,5,5,5,7,7]`; for the plain row-major permutation Q=(1,...,9), the ordered differences are `[1,1,1,1,1,1,3,3,3,3,3,3]`. Each order statistic of Q is at most that of L, and some are strictly lower. Therefore **E_V(Q)<E_V(L)** for every strictly increasing V. In particular no such uniform monotone smoothing nearest-neighbour potential can make LuoShu a global energy minimizer. The theorem does not extend to nonmonotone edge potentials, nonlocal or oriented interactions, unbounded grids, or different state priors.

## GL79-02 — Engineered local pair energy with exactly the eight LuoShu ground states

Let V(d) for d=1,...,8 equal `[0,-1,5,-2,-5,5,-5,5]`. This pair potential is homogeneous on all 12 orthogonal edges and D4-invariant; it includes no row/column/diagonal sum predicates. An exhaustive exact 9! integer enumeration gives `min_p E_V(p)=−36`, with exactly eight minimizers, all the standard LuoShu D4 orbit; the least-energy nonmagic permutation has energy −33. The integer energy difference histogram `c(p)=(#edges of difference d)_d=1..8` for any magic board is `[2,2,0,2,4,0,2,0]` and is found for exactly eight boards. This is a **computer-assisted finite-classification existence result**, not a natural self-organization theorem: **V was chosen after examining target LuoShu histogram features through linear programming**. Explicit target information was encoded in local coefficients even though the global diagonal target was not a term in E. For arbitrary perturbation ||δV||∞≤ε, a sufficient certificate that the magic minima remain strictly below all nonmagic competitors is `ε<1/8`: each energy changes by at most 12ε so the 3-unit gap cannot close if 24ε<3. This conservative bound says nothing about local descent reaching those minima.

## GL79-03 — Random local potential selection is distribution-dependent, not natural emergence

For a specified compiler-chosen measure, draw the eight V(d) independently from standard normal N(0,1), using fixed RNG seed 790079 and 4096 draws. For each draw compute exact energies of every distinct 12-edge difference profile arising among all 9! permutations. **2 of 4096** random potentials make the LuoShu orbit the unique global minimizing difference profile; this event therefore selects eight magic boards in this finite domain. This is a synthetic Monte Carlo observation conditional on Gaussian coefficients, lattice, fixed digits and target diagnostic. Do not generalize 2/4096 to nature, physics, language model training, a universal prior, or an information-theoretic frequency law. A separate single Gaussian control (seed 790000) has 16 nonmagic global minima.

## GL79-04 — Ground-state existence does not ensure local kinetic reachability

Use 128 predeclared seeded 1..9 permutations, nearest-neighbour transpositions only, strict steepest-descent with a lexicographic tie break and at most 200 accepted swaps. At the same starts, squared-smoothing `V(d)=d²` reaches a global minimum 13/128 and LuoShu 0; target-engineered local V reaches a global minimum **1/128** and LuoShu 1; one fixed single Gaussian potential reaches a global minimum 2/128 and LuoShu 0. All stopped at adjacent-swap local minima. An exact global optimum is thus insufficient for reliable finite-step local convergence, even when optimum selection is known by exhaustive enumeration. At any finite β>0, by contrast, a correctly constructed adjacent-swap Metropolis chain with positive acceptance probabilities, symmetric proposals and an explicit self-loop is irreducible and aperiodic on S9 and has stationary Gibbs weights proportional to exp(−β E_V). For engineered V its stationary magic mass tends to 1 as β→∞, but **finite mixing, temperature schedule and natural physical realization are entirely untested**. Equilibrium selection, local descent and dynamical self-organization are distinct assertions.

## Residual / next discriminating mechanism

The exact local potential is *not* a free emergence explanation because its coefficients are target-fitted, and the graph/digit/permutation priors remain engineered. To advance, require an **independent** mechanistic selection or learning rule for V with parameters determined without LuoShu-labelled examples, preregistered tasks on unseen grid sizes and digits, and comparison against generic nearest-neighbour tiling, assignment, smoothness, annealing and constraint-solving baselines. Explicitly report nonmagic outcome, failure basins, and time/cost. Do not infer 9-cycle 九宮飛星 from eight-point D4 symmetry; no natural Transformer/LLM LuoShu emergence observed, and independent LLM reconstruction remains NOT_RUN.


---

# v8.0 TARGET-BLIND PRIORS AND LABEL SYMMETRY AUDITS

# General Lemma Register v8.0 — Exchangeability no-go and target-blind prior stress test

> Provenance: COMPILER-AUTHORED mathematical theorem and finite synthetic computation based on a fixed 3×3 distinct-digit permutation universe. Inherited source context `SRC-0104`, `SRC-0107`, bounded historical reading only; neither source is said to contain these new results. No original PDF/DOCX reread in this version. No natural-language Transformer or semantic attractor validation.

## GL80-01 — Full symbol-exchangeability prevents preference for a particular LuoShu pattern

Let Ω be the set of all bijections between nine lattice positions and nine *unstructured* abstract labels. S9 acts on Ω by relabeling the labels, and this action is **transitive**. Let P be the output probability distribution of any algorithm whose entire input, initialization law and transition/selection rules respect arbitrary label permutations: for every σ∈S9 and A⊆Ω, P(σA)=P(A). Then for any two boards p,q, there exists σ with q=σp, so P(p)=P(q)=1/9!. The eight boards identified as LuoShu *after* assigning the ordinary arithmetic meaning to labels 1–9 therefore have probability exactly 8/9!=1/45360.

For any energy E:Ω→R invariant under every relabeling, transitivity implies E is constant. Consequently its Gibbs law is uniform at **every inverse temperature β**, not merely at β→0. A deterministic equivariant map from a truly invariant input to Ω is impossible because no single placement is fixed by S9. This is a formal **conditional no-selection theorem**: if labels carry magnitude, order, distance, parity, asymmetrically trained embeddings, boundary assignments, or externally broken symmetry, the hypothesis fails and the conclusion need not hold. It does not deny target-blind *numerical* dynamics can prefer LuoShu; it identifies a necessary source of arithmetic differentiation or symmetry breaking to investigate.

## GL80-02 — Nine frozen ordinary local numerical priors do not select LuoShu ground states

Before enumeration, the protocol fixed nine V(d) families (linear/squared smoothing, linear/squared repulsion, inverse-gap, odd/even preference or avoidance, three/four periodic cosine) using only orthogonal-neighbor |digit gap|=d. Each has D4-invariant energy E(p)=Σ_edges V(|p_i−p_j|), but DOES NOT have full S9 relabeling invariance (hence GL80-01 alone does not predict their results). Exact exhaustive energies for 362,880 distinct placements find, respectively, **32, 8, 1152, 16, 16, 2880, 34560, 12960, 1920** global minimizers, with **zero LuoShu boards** among global minimizers for every prior. Evidence: `EXPERIMENTS_V80/fixed_prior_exact_groundstates_v80.csv` and source `run_v80.py`; protocol SHA-256 `809e7a166a747413476ba1f7717eea11a1f2ad0861c78b312a7fabc442524b10`.

These are exact outcomes **conditional on the fixed artificial domain and nine manually chosen prior functions**. They do not establish impossibility for all target-blind local mechanisms, all graph sizes, neural nets or physical systems. In contrast, the v7.9 nonmonotone V construction explicitly fitted to LuoShu **did** create eight magic ground states; the distinction is target-selection provenance, not locality alone. The list of ordinary priors was specified prospectively within this session; it is not externally preregistered or validated as natural physical laws.

## GL80-03 — Finite-temperature dynamics retains selection/budget limitations

For five prospectively selected V families, run 64 pseudorandom initial permutations each, with uniform adjacent-edge swap proposals, Metropolis acceptance at β=1 and exactly 500 proposals per trajectory. 320/320 paths were retained with start/end boards, energies, acceptance counts and both end-state and ever-hit-magic indicators. All **0/320** trajectories reached LuoShu at any recorded proposal. The selected controls have no LuoShu global ground state (GL80-02), so this kinetic result is consistent with but does not prove a large-volume dynamic no-go. Since magic occupies just 1/45360 of the uniform permutation state space, zero observed hits is in itself not a powerful surprise under null uniform sampling. The runs do NOT establish equilibrium mixing times or automatic spontaneous pattern formation. Synthetic trajectories are not independent physical realizations.

## Open research discrimination / repair

The hypothesis of natural emergence can only advance if an independent mechanism both **generates or justifies symbol magnitudes / spatial organization** and preferentially selects magic structure without using LuoShu outputs for parameter fitting. Need separately justified data or physical law, unobserved holdout structures, alternative lattices, and baselines for target recognition vs target generation. If an allegedly agnostic mechanism is still S9-exchangeable, GL80-01 is an exact negative prediction. If it breaks S9 by arithmetic differences, GL80-02 shows nine simple breakings are insufficient on this test. Neither result proves full SMFT false or true. Nine static D4-orbit classes ≠ a nine-step flying-star process. Independent LLM reconstruction and natural Transformer LuoShu remain NOT_RUN.


## v8.1 supplemental-source scope and conditional mathematical proof

See `GENERAL_LEMMA_REGISTER_v8.1.md` GL81-01..04 (file-wide SHA logged in current index). Uploaded PDF is source-scoped pp1–5,8–10,13–14 (visually pp3,5,9), SHA in `V81_SUPPLEMENTAL_SOURCE_AUDIT.md`; it is not silently registered as a new stable SID. Original historic cumulative proof and source-depth entries above are preserved. S2 wr S5 symmetry is conditional on unlabelled pairs only; literal appendix peripheral cycle type (8)(1) is separate from a 9-cycle. Synthetic coactivation source is PLANTED, no proof of original field emergence. Independent reconstruction and pretrained neural tests NOT_RUN.

## v8.2 current compiler results — GL82-01..03

See `GENERAL_LEMMA_REGISTER_v8.2.md`: 80 synthetic seeded histories (20 each FULL/PAIR_ONLY/CENTER_ONLY/NONE), 24/24 new scoped QA, 19/19 inherited v8.1; planted phase, no natural Hetu; FULL common-center primary R² 0.441 FAIL; phase lag causal nonidentification proof; ordinary Ridge mask baseline. No new canonical source, source full-depth or independent LLM evaluation.

## v8.3 compiler-added conditional source-field theorems (GL83-01..05)

See GENERAL_LEMMA_REGISTER_v8.3.md. Local spectral gap, phase holonomy, reversible-vs-driven ring flux and 8+center numeric nonentailment. These are **conditional models**, do not establish large-sample spontaneous source formation, trained Transformer dynamics, or LuoShu numbering. Prior v8.2 primary failed center remains FAILED.


# V8.4 — Conditional center-elimination, source memory and trace closure audit

# General Lemma Register v8.4 — Center Projection, Memory, and Conditional Trace Closure

> All five GL84 nodes are **compiler-authored conditional mathematical deductions**, not transcriptions of canonical SMFT theorems. The 11-node center+five-pairs source is assumed. No spontaneous training emergence, real physical entropy law, natural LuoShu numbering, trained Transformer, or independent LLM benchmark was observed. The 15-page supplemental Hetu paper remains outside the 325-source manifest. This version does not repair or erase prior v8.2 failed center-detection criterion or v8.3 frustrated-cycle results.

## GL84-01 — Pair-center spectral decomposition: pair strength alone cannot build global stability

Let G(c,p) be the weighted undirected 11-node graph with central vertex 0, ten peripheral vertices, five disjoint peripheral pair edges of weight p>0 and ten hub edges of weight c>0. Its symmetric Laplacian L has exact eigenvalues (counting multiplicity): 0 (1), c (4), c+2p (5), 11c (1). Proof: split peripheral coordinates into the 5D pair-antisymmetric subspace, the 4D pair-mean contrasts with total zero, the 1D collective hub/periphery contrast, and 1D global consensus. The spectral gap is lambda2=c and cannot be increased by taking p arbitrarily large when hub weight c stays fixed. If c=0, the five isolated pairs plus center make six connected components, and L has six zero modes. Conditional consequence: strong local pair attraction alone cannot restore global phase/source consistency; hub connectivity can, provided phase offsets are compatible (GL83-02). Linear result also describes local phase linearization around compatible locking; not a global nonlinear stability proof and not a natural Hetu identification.

At c=0.8,p=1.3 the exact spectrum is {0, 0.8×4, 3.4×5, 8.8}, verified numerically. Ordinary graph Laplacian theory entirely explains this result.

## GL84-02 — Center equilibrium elimination induces all-to-all coupling, but is not dynamic elimination

Writing L=[[L_cc,L_cp],[L_pc,L_pp]], the energy of a **static** center/peripheral configuration is E=1/2 x^T L x. Minimizing over center h yields h*=mean(x_1,...,x_10), and an effective peripheral quadratic energy E_eff=1/2 x_p^T [L_pp-L_pc L_cc^{-1}L_cp]x_p. Here L_cc=10c, L_pc=-c 1, so L_eff=L_pp-(c/10)11^T. For distinct peripheral vertices belonging to different pairs, the off-diagonal coefficient is -c/10: a hidden hub, eliminated at equilibrium, induces effective dense pairwise coupling even though the original coupling graph was sparse. This is standard Schur/Kron reduction; it does NOT imply microscopic direct attraction or an AI-specific gravity law.

Important quantifier: h*=mean(x_p) holds for minimizing instantaneous energy or an imposed infinitely fast center, NOT for a center evolving with its own finite relaxation time. Equating static Kron reduction with projected actual dynamics discards memory.

## GL84-03 — Exact deterministic autonomous projection iff hidden kernel is invariant

For a constant linear system xdot=Kx and fixed surjective linear observation y=Pi x, a closed deterministic first-order equation ydot=By valid for **every** x exists iff K(ker Pi) subset ker Pi. Necessity: any hidden offset v in ker Pi leaves y unchanged, so Pi K v must vanish. Sufficiency: define B(Pi x)=Pi K x, which is well-defined exactly under invariance. For the constructed 11-node source K=-L and Pi selecting peripheral nodes 1..9 (nine visible channels), hidden state is [center0, peripheral10]. With identical y, modifying center by +1 changes each visible instantaneous derivative by +c. Therefore the chosen nine-output state does NOT possess an exact time-local closed 9D deterministic evolution for all initial conditions. This is a counterexample to the automatic source→nine-coordinate Markov-law leap, not a no-go for every possible nonlinear/coarse-grained/stochastic/augmented projection. Specific invariant eigenspace quotients do exist, but do not select classic LuoShu labels or a unique nine-output observation.

## GL84-04 — Eliminating a finite-speed hidden center yields an exact causal memory kernel

Consider xdot_i=-c(x_i-h)-p(x_i-x_pair(i)), hdot=c sum_{i=1}^{10}(x_i-h). Solve the second ODE by variation of constants:

h(t)=exp(-10ct)h(0)+c ∫_0^t exp[-10c(t-s)] sum_i x_i(s) ds.

Substitution into the visible equations is an exact generalized Langevin/Volterra memory form: visible future depends on historical peripherals plus hidden initial state. More generally, for block dynamics ydot=Ay+Bh, hdot=Cy+Dh, elimination gives ydot=Ay+B exp(Dt)h(0)+∫_0^t B exp[D(t-s)]C y(s) ds. A memoryless projected equation requires an invariant projection, extra sufficient statistics, restrictive initial-state assumptions, or a justified time-scale approximation. Repeated source-training traces are **not** proven to obey this synthetic kernel.

Numerical audit: dt=0.025 explicit Euler, 500 steps, 48 deterministic seeds, c=.8,p=1.3. In ten-visible/periphery projection: mean trajectory RMSE exact memory ~6.83e-16; static instant-center ~.06221; center clamped zero ~.22519. In *nine*-visible projection with two hidden dimensions, exact retained memory ~3.16e-16; quasistatic hidden equilibrium ~.10841. These exact reconstructions reuse a model-known hidden initial condition; they are algebraic equivalences, not empirical source-discovery or free predictive advantage.

## GL84-05 — Antisymmetric phase transport can rotate dissipative transients without a steady LuoShu trace

Let L_r be an undirected connected ring Laplacian and A be a real skew-symmetric zero-row-sum oriented ring generator. For zdot=(-L_r+omega A)z, omega imposed externally, and z centered (1^T z=0), d/dt[1/2||z||²]=-z^T L_r z <= -lambda2(L_r)||z||². The skew term contributes identically zero instantaneous quadratic energy change, but yields complex eigenvalues/rotating *transients* when omega != 0. All transverse amplitudes decay; no sustained finite-radius orbit or permanent current is implied by the antisymmetric rotation alone. In an independent driven CTMC, permanent stationary probability current requires breaking detailed balance (GL83-03), not merely observing lagged phase coherence. In the v8.4 explicitly imposed eight-ring, 6 eigenvalues become complex and transverse energy decays from .4375 at t0 to about 1.06e-5 at t8. The eight-ring connectivity is supplied by modeler and is neither an observed LuoShu 8-outer trace nor a 9-cycle; numeric labeling still requires an extra law (GL83-04).

**Research type boundary:** Origin of generalized semantic gravity→Hetu source→LuoShu dynamics remains CONJECTURE, scale complexity UNKNOWN. All v8.4 results concern what follows IF specific classical graphs, hidden-state projections and external orientation operators are provided. No source-trace structure was identified in a real pretrained Transformer; independent LLM Reconstruction remains NOT_RUN. Historical 866 regression remains NOT_RERUN. New scoped tests 40/40 and inherited v8.3 scoped 37/37 PASSED.


---

# v8.5 scoped conditional proof view

# General Lemma Register v8.5 — Finite-History Source Observability, Noise and Reversal

> **Compiler-derived conditional mathematics, not a source-authored claim**. Assume the 11-node hub/five-pair classical linear graph of v8.4 (c=.8, p=1.3 unless varied). Nine visible channels select peripheral positions 1...9; hub0 and peripheral10 are hidden. The graph, its parameters, the oriented ring and labels are deliberately SUPPLIED, not learned. Natural semantic gravity → Hetu → LuoShu emergence, integer quantization, trained Transformer behavior and independent source-hidden LLM reconstruction are all NOT_RUN/CONJECTURE.

## GL85-01 — Non-Markov nine-coordinate readout can be exactly finite-history observable

Let xdot=Kx in R^11, with observation y=Cx in R^9, selecting x_1,...,x_9. For a time separation Δ>0 define O_Δ=[C;Ce^{KΔ}]. Two noiseless observations determine every x(0) uniquely iff rank(O_Δ)=11. This is an **observability** criterion, distinct from the autonomous first-order **output closure** criterion K ker C ⊆ ker C (GL84-03). For the v8.4 hub/pair K, hidden directions e_0 and e_10 satisfy CKe_0=c 1_9 and CKe_10=p e_9. As these are independent for c,p>0, rank([C;CK])=11. By analyticity Ce^{KΔ}=C+Δ CK+O(Δ²), O_Δ has full column rank for all sufficiently small Δ>0. Numerical singular-value tests at Δ=.02,.1,.4 also have rank11. This does NOT establish rank for every Δ>0 or robustness under noise and model error.

One concrete continuous-time reconstruction of hidden coordinates from y and its derivatives is h=[dot y_1+(c+p)y_1-p y_2]/c and x_10=[dot y_9+(c+p)y_9-c h]/p. Thus a finite augmented state (y,dot y), constrained to the true 11D reachable manifold, may restore a time-local description although y alone is not Markov. The equations require known parameters, sufficient temporal precision and an appropriate channel arrangement; they do not identify magic LuoShu labels.

## GL85-02 — Exact observability does not guarantee numerically stable source recovery

For a full column rank O_Δ, inversion error with observation noise η satisfies ||xhat−x|| ≤ ||O_Δ^+|| ||η||; the inverse gain is 1/σ_min(O_Δ). In the source graph, the two hidden directions affect observations at order Δ, and the small-Δ inverse is poorly conditioned. Data from 48 fixed seeded initial states × 3 Δ × 2 observational-noise levels (288 rows) confirm this distinction. At Δ=.02,.1,.4 the O_Δ condition numbers are 85.17,19.15,9.08, respectively. With noise standard deviation .001 independently added to both observed nine-vectors, mean hidden-state RMSE is .04559,.01058,.00419. With noiseless observations it is below 5e-14 in those trials. This **particular range** does not prove bigger Δ is always better (at long times all stable transverse signals vanish). Reconstructing an actual neural source also requires discovering the correct observation and transition model.

The simplest comparison is ordinary least squares vs α=.001 ridge vs instantaneous hidden equilibrium, all applied to a fully **specified** linear simulator. Ridge has bias in this setting and need not outperform unregularized least squares. Neither mathematical exact recovery nor a favorable simulation error is an SMFT-exclusive technology.

## GL85-03 — Signed orientation is identifiable under an excitation and model-aware intervention, but not from every scalar trace

Declare A^T=−A with A1=0 on an **externally installed** eight-peripheral oriented ring. Let K_ω=K+ω A. A causal matched-state reversal changes the initial derivative by (K_ω−K_{−ω})x=2ω Ax. Therefore a nonzero Ax and an orientation-sensitive observation are needed to distinguish the signs locally. If K and x are known, the ordinary residual estimator χ=(Ax)^T(\dot x−Kx)/||Ax||² equals ω exactly whenever Ax≠0. Forty-eight matched synthetic starts, ±ω=.65, t=.125 yield a mean nine-output reversal difference norm .25440 and exact oracle χ means ±.65. A uniform start (Ax=0) gives no difference. The graph admits a reflection P with PKP=K and PAP=−A; for a reflection-symmetric initial state the **scalar norm/energy** readout is identical for both signs, notwithstanding potentially different oriented channel traces. Hence an ambiguous scalar response cannot certify direction.

Because A was installed by the analyst, there is no evidence of spontaneous LuoShu orientation, traditional outward eight-step numeric ordering, or a nine-state flying-star cycle. The dissipative skew term does not by itself imply sustained current (GL84-05).

## GL85-04 — Structural labeling and real-model domain firewall

The observability and reversal results are theorems about a model with **specified** 11-dimensional states, known coupling and fixed selected observables. They do not determine: (a) why 5 pairs arise from long training; (b) why one center is privileged; (c) numeric meanings 1...10, Hetu Δ5 pairing, or LuoShu numeric grid assignment; (d) what physical or neural operator makes ω nonzero or switches its sign; (e) a persistent nonequilibrium flux or 9-step temporal recurrence; (f) engineering benefit beyond standard Kalman/observability/state-space identification; (g) learned semantic gravity or original SMFT theory validation. Ordinary control-theoretic reconstruction is the baseline, not an alternative 'new proof' of a semantic field mechanism.

Two negative structural ablations (center coupling c=0 or hidden pair coupling p=0) reduce the **two-snapshot** stacked rank from 11 to 10 at Δ=.1. These are rank outcomes for the stipulated observation protocol, not universal limits for every future sensor or longer observation schedule. The v8.2 common-center R²=.441 primary failure, v7.8–v8.0 scoped finite no-gos, legacy witness W024 and five uncertain historical SHA scopes all remain unresolved. Independent LLM benchmark and natural transformer tests remain NOT_RUN.

**Research continuation:** Find independently justified observables for a purported real Hetu source; estimate an identifiable low-dimensional memory state across genuinely held-out temporal interventions with model mismatch, then compare against classical linear state-space, subspace ID, AR/VAR, and ordinary RNN baselines. Keep spontaneous emergence separate as user-approved conjecture with no known sample-size bound. No full original PDF/DOCX reread in v8.5.


---

# v8.6 scoped compiler mathematical proof view

# General Lemma Register v8.6 — Persistent Flow, Hidden Memory, and Nonequilibrium Firewall

> All following results are **compiler-authored, conditional mathematical deductions** and directly executed synthetic controls. They do **not** appear as theorems in the original SMFT source. An 11-node center + five-pair network and a manually defined eight-peripheral skew operator are *assumed*. The long-training emergence origin is an open conjecture with unknown required data/compute; numeric LuoShu and real Transformer attribution are **NOT_RUN/NOT_DERIVED**.

## GL86-01 — Unforced dissipative source cannot sustain nontrivial transverse circulation solely through skew direction

Let L=L^T⪰0 be the connected 11-node graph Laplacian of the stipulated hub/five-pair graph and A^T=−A, A1=0. For `xdot=(-L+ωA)x`, the mean \\bar x is constant (since 1^TA=0), and z=x−\\bar x1 lies in the mean-zero space. The quadratic discrepancy V=||z||²/2 obeys `Vdot=−z^TLz≤−λ₂(L)||z||²=−2λ₂(L)V`. Grönwall then implies `||z(t)||≤exp(−λ₂(L)t)||z(0)||` for **all** initial conditions. Thus a skew term can turn transient trajectories but cannot sustain a nonzero-amplitude deterministic periodic orbit under these graph assumptions. It does not rule out periodic behavior in a system with negative damping, time-dependent inputs, nonlinear drive or autonomous active feedback.

With c=.8,p=1.3 we numerically obtain λ₂=.8. 48 fixed Gaussian starts×3 manually imposed ω∈{−.65,0,+.65} at time16 have respective mean transverse norms 3.46554e−6,5.32264e−6,3.45344e−6. This synthetic numerical comparison is not a model of real learned Hetu, nor does it establish any LuoShu flying-star order.

## GL86-02 — Sustained *probability* current in continuously driven OU flow differs from an autonomous deterministic limit cycle

For the explicitly *driven* stochastic system `dx=Bx dt+√(2D)dW`, `B=−L−γI+ωA`, γ=.4>0, D=.25>0, all B have negative-definite symmetric part, hence a unique positive stationary covariance Σ satisfying `BΣ+ΣB^T+2DI=0`. With stationary Gaussian density ρ, the Fokker–Planck probability current is `j(x)=(B+DΣ^{−1})xρ(x)=Ωxρ(x)`. The *conventionally defined overdamped* stationary entropy-production rate is `σ=D^{−1}tr(Ω^TΩΣ)≥0`, and the signed orientation-sensitive projection is `tr(A^TΩΣ)`.

For ω=0, B symmetric and Σ=D(L+γI)^{−1}, so Ω=0, no stationary current, detailed balance. For ω≠0, B nonsymmetric; Ω cannot vanish because Ω=0 would imply B=−DΣ^{−1} symmetric. In the fixed tested graph ω=−.65,0,+.65 gives signed flux −.28394484,≈0,+.28394484, with σ=.73825658,≈0,.73825658. Correct covariance equation residuals <5e−15. Directional steady *ensemble* flow demands ongoing external drive/noise; it does not imply any single deterministic system trajectory cycles indefinitely, or that the source labels itself as the traditional LuoShu.

## GL86-03 — Conditional orbit stability requires supplied nonlinear active gain; center memory is not necessary

Let complex z obey `dot z=(µ−|z|²−kh+iω)z`, and real hidden memory h obey `dot h=−ah+b(|z|²−µ)`, with a>0, b≥0, k≥0. If µ>0 and ω≠0, `|z|=sqrt(µ), h=0, θ(t)=θ(0)+ωt` is a periodic orbit with period `2π/|ω|`. In radial-squared coordinate q=|z|² the linearization at (q,h)=(µ,0) is `[[−2µ,−2µk],[b,−a]]`, with trace `−2µ−a<0` and determinant `2µ(a+kb)>0`, establishing local transverse exponential orbital stability. The phase direction is neutral, as expected for an autonomous limit cycle.

A standard Stuart–Landau model with **k=0** retains this cycle: h need not causally sustain it. If ω=0, `q=µ,h=0` describes a *circle of fixed points*, not a rotating cycle. In the tested µ=−.5, a=1.1,b=.6,k=.7 system, the origin in z is linearly stable around hidden equilibrium h=−bµ/a; the 48 trajectories decay to zero amplitude. Angles can keep winding as amplitude vanishes, so raw winding counts are **not** a valid persistence measure. Under µ=1, ω=±.9, k=.7, a=1.1, b=.6, transverse eigenvalues are −1.55±0.79844i. On 48 fixed seeded initial conditions per group, all 48 final radii approach unity for each ±orientation and the no-feedback baseline, while ω=0 produces no net winding; these are ordinary nonlinear-system results, **not natural emergence, learned center memory or a novel SMFT mode**.

## GL86-04 — Nonentailment: orientation, reversible probability flux, memory, and canonical LuoShu are distinct proof obligations

The three model families above prove a boundary, not a universal emergence mechanism: (i) mathematical directionality A or ω; (ii) sustained drive from stochastic forcing or active µ; (iii) hidden memory h; (iv) correct numerical assignment to 1–9 and nine-position topology; (v) eight-exterior numeric sequence versus nine-period flying-star transitions; (vi) a real trained Transformer source and causal effects; (vii) independently improved engineering utility over ordinary control theory are **separate** hypotheses. The model currently **preselects** the graph, ring, parameters and Fourier/radial active gain. Nothing derives the natural source, classical numeric LuoShu map, an eight/nine cycle or a semantic-physics law. The v8.2 center-oracle R²=.441 preregistered fail, v7.8–v8.0 restricted nulls, source citation depth limits, W024 unresolved and five legacy hash-scope ambiguities remain unmodified.

**Continuation:** Test whether a hidden center yields *any separately measurable* heldout causal benefit under model mismatch, external forcing and generic nonlinear oscillator baselines. Distinguish *visible state history*, *steady stochastic probability flux*, and *an active autonomous limit cycle*. Do not infer special Hetu center mechanisms from a cycle that remains after center feedback ablation. Do not repeat tiny emergence benchmarks merely to force a proof beyond available scale. Isolated external blind Reconstruction remains NOT_RUN.
