---
artifact_id: SMFT-KERN-K0-001
version: 3.2.0
snapshot_date: 2026-10-15
status: v3.1 scoped source/claim audit; no independent scientific validation
logical_path: 02_CANONICAL/20_K0_CORE_v0.1.md
source_anchor: [SRC-0323, SRC-0309, SRC-0106, SRC-0283, SRC-0299, SRC-0261]
---

# K0 — SMFT / 成界之學 Conditional Core
### A compact restoration grammar for LLM researchers | 中英混合，精度先行

**READ THIS AS** a concise *research-state specification* with verified source anchors and open claims, NOT an axiomatically complete theory of everything, a universal physical law, or a proof of inherent Semantic Attractors in Transformers.

## 0. Ancestry and separation of roles

`Genesis (《皇極經濟》) → Conceptual Translation (Economic Cycles) → Mesoscopic P8D II → Formal World-Formation / Framing → Domain-specific tests (including AI)`.

This is **intellectual ancestry / a candidate research dependency**, not a rigorous implication chain. Later theories establish the precision standard; the Genesis source defines crucial concepts the later math may not yet exhaust.

**Architectural separation**:

- `World/Observer Layer` — who declares an operational world and with what observational limitations?
- `Framing Layer` — what inside/outside boundary and quotient preserve task-relevant distinctions?
- `P8D Meso Layer` — inside a declared world, what mechanism sustains qualified flow, boundary exchange, propagation, realization and feedback?
- `Commitment/Ledger Layer` — which candidate events become history, which residuals persist, when is revision licensed?
- `Domain Realization Layer` — under what mapping, measurement and intervention does a physics/finance/biology/Transformer application instantiate an effective reduction?

No layer automatically “is” another layer.

## 1. Foundational types (namespaces matter)

| Symbol | Type / role | Minimal meaning | Provenance |
|---|---|---|---|
| `Σ` | possibility domain | uncommitted possible configurations/relations | `SRC-0299` §3 |
| `O` | bounded observer | finite observational, computational, action and revision capacity | `SRC-0299` §4 |
| `D` | declaration rule | admits an operational world `D:Σ→W_D` (schematic) | `SRC-0299` §5 |
| `P` | observation protocol | `(B_P,Δ_P,h_P,U_P^probe)`; boundary, aggregation, horizon, probes | `SRC-0106` §3 |
| `Σ_P` | protocol-bound trace | `Log(System|P)`; not identical to the system | `SRC-0106` §3 |
| `Γ_min` | framing pair | `(B,Π)`: inside/outside cut and effective quotient | `SRC-0283` §1 |
| `X_B,Z` | states | retained microscopic and effective spaces | `SRC-0283` §1 |
| `Π:X_B→Z` | quotient/projection | identifies distinctions operationally invisible to selected protocol | `SRC-0283` |
| `ℒ_t(x,a,x')` | Li admissibility predicate | whether a transition counts as admissible (`0/1` basic form) | `SRC-0106` §5 |
| `𝒦_t` | Kan realization operator | produces candidate feasible paths under rules, goals, trace and residual | `SRC-0106` §5 |
| `F0,F` | meso dynamics | baseline flow and governed, feedback-mediated runtime | `SRC-0106` §6 |
| `G_commit` | commitment gate | whether a candidate outcome becomes recorded historical trace | `SRC-0299` §7 |
| `τ/Trace`, `ℱ_t` | historical record / filtration | committed sequence and information revealed to observer over time | `SRC-0299` §§8–9 |
| `R` | unresolved residual | failure to absorb, predict, reconstruct, or reconcile inside current frame | `SRC-0299` §10; `SRC-0106` §10 |
| `U_revision` | hierarchical revision | updates state/policy/world/interpretation/purpose/declaration under governance | `SRC-0299` §§11–12 |

**Symbol collision guard:** `P` can denote protocol while some papers use `P` for Purpose; this kernel writes **`P_obs`** for protocol and **`Purpose`** for purpose in prose where confusion may arise. `Π_frame` (quotient) differs from `Π_K` (Kan candidate-path set). `R_struct` (unexplained model remainder) differs from `ε_cl` (low-rank closure-fit residual) and measurement noise. `F` for vector field differs from `ℱ` for filtration. `τ` for trace may collide with imaginary time in older SMFT; always type-tag.

## 2. A minimum declared world

**Boundedness:** `O(Σ) ≠ Σ` under finite access. The observer must declare which distinctions, actions and evidence rules count. (`SRC-0299` §§3–5)

**Frame construction:**

\[
\Gamma_{\min}=(B,\Pi),\quad \Pi:X_B\to Z,\quad
x\sim_\Pi y\iff\Pi(x)=\Pi(y).
\]

**Exact effective dynamics require congruence:** for admitted update `T_u`, a well-defined effective `S_u` requires `Π(T_u(x))=S_u(Π(x))` over the admitted domain (and interventions), or an explicitly bounded approximate version. `Z` is an operational quotient, **not unique ontology**. (`SRC-0283`)

**Genesis safeguard:** 《皇極經濟》§4 selects a vantage point/small universe/flow before modelling; §7.3a identifies a *developing subject* before declaring its environment. Do not declare a convenient quotient that erases the very organizing object under study. (`SRC-0323`)

## 3. Proto-Eight is a typed grammar, NOT canonical R⁸

| Role pair | Typed problem | Core effect |
|---|---|---|
| `Qian–Kun` | potential ↔ qualified transduction | convert viable difference to flow |
| `Gen–Dui` | boundary ↔ exchange | maintain boundary while admitting/regulating exchange |
| `Zhen–Xun` | trigger ↔ propagation | activation, amplification, relay, replication |
| `Kan–Li` | realization ↔ admissibility | construct paths under mutable transition grammar |

`Li: ℒ_t(x,a,x')∈{0,1}` is a *validity condition*, not identical to physical access or commitment. `Kan: (goal,x,ℒ,Trace,R)→Π_K` constructs viable paths; memory/focus are possible implementations, not the role definitions. (`SRC-0106` §§4–5)

**Mother-source safeguard:** 《皇極經濟》 §5.3 uses the four conjugate relations with different time/level/organization roles; P8D II preserves **typed asymmetry** rather than asserting equal variable types. (`SRC-0323`; `SRC-0106` §4)

**先天 vs 後天:** `Incubation_Trigrams` represent internal generative roles; `Adaptation_Trigrams` encode proposed external macroeconomic phases. Their 64 combinations in `SRC-0309` are a research scheme, not empirically verified universal dynamics.

## 4. Runtime and recursive closure

A useful conditional subclass:

\[
\dot x=F_{K,L}(x),\qquad
F_{K,L}=F_0^{K,L}+\sum_{\ell=1}^r c_\ell^{K,L}H_\ell^{K,L}.
\]

`r`: number of effective recurrent mediation channels in declared representation. It is **not** the dimension of `x`. A channel is not merely a graph edge. (`SRC-0106` §6)

For a differentiable shared-mediator factorization `F=F0+Γ∘H`, `H:X→R^r`:

\[
\operatorname{rank}(DF-DF_0)\le r.
\]

**This bound is a mathematical consequence of assumptions, not proof of small-r organization in a natural system.** Check closure fit as well as rank. (`SRC-0106` §§7,14)

For linearized `J=J0+UV^T`, return operator `\mathcal R(\zeta)=V^T(\zeta I-J0)^{-1}U` (where resolvent exists). Classify dynamics only **after** determining closure channels and an effective sector. A complex-like `2×2` signature can emerge when the corresponding square-of-traceless-part is negative; split-like signatures also possible. `ComplexPlane ≠ primitive` and `signature ≠ stability`. (`SRC-0106` §§8–9)

## 5. Productive incubation and irreducible residual

A candidate viable **incubation basin**, under specified protocol/horizon:

\[
\mathcal I_{P}(h)=\{x_0:\exists\pi\in\Pi_K\text{ admissible, }
 x_t\in V_P,\ Q_P(t)\ge Q_{min},\ R_P(t)\le R_{max},\ \forall t\le h\}.
\]

Incubation requires *viability, realizability, recoverability and sufficient qualified flow*; an apparently stable but ossified regime can fail. Recovery radius is a separate diagnostic. (`SRC-0106` §11)

For representable disturbance under `Π_E`, split `η=η_∥+η_⊥`. A persistent, structured `η_⊥` can indicate omitted mechanisms; it must not be automatically labelled random noise. `ε_cl` (closure factorization fit), `η_⊥` (effective-sector residual), `R_governance` (unresolved history or admissibility failure) have distinct types. (`SRC-0106` §§7,10; `SRC-0299`)

**Genesis safeguard:** §7.3 *花* is not merely stability of existing state; it spends current resources on discovering future viable structures. (`SRC-0323`)

## 6. Effective reduction requires an actual map

For a claimed P8D → effective-domain theory:

\[
\|C_{P}(\Phi_{t}^{P8D}(x))-\Phi_{t}^{eff}(C_P(x))\|\le\varepsilon_{red}
\quad(0\le t\le h).
\]

The compiler `C_P` must be typed; tests need declared task, horizon, interventions, units, error bound, and what outcome/sign must be preserved. Algebraic similarity and shared eigenvalue patterns do **not** imply effective reduction. (`SRC-0106` §12)

If no `C_P` with adequate predictive/interventional preservation has been shown, label the bridge `M1 candidate`, not `DERIVES`.

## 7. Full recursive loop and level discipline

**P8D II explicit interface:**

`Declaration → P8D Runtime → Commitment → Trace → Residual → Revision` (`SRC-0106` §15.10).

**World-Formation Formal Core** further separates Purpose from Goal: a Goal is an objective; Purpose is a revisable but persistent **counterfactual reference** against which interpretations and histories can be judged. `G_commit` distinguishes event candidates from committed trace, `ℱ_t` orders information, and latching resists casual high-level revision. (`SRC-0299` §§7–13)

**Normative engineering guardrails (design objectives):** retain committed trace; preserve unresolved residual attribution; require evidence/hysteresis before changing declaration or purpose; do not masquerade prompt rewriting as proof of self-formation. These are governance recommendations, not universal physical laws.

## 8. The four mother axes outside P8D's runtime scope

1. **Observer–perspective formation**: 觀點, 時天地人, nested 小宇宙; complements `Γ_min` and `D`.
2. **Generative–incubative roles**: the 4 dyads, 根苗花果, coupled flow and renewal; P8D's strength.
3. **Governance–coordination topology**: 道/德/仁/霸, 禮/樂 and dependency inertia; not reducible to Li predicate without a bridge.
4. **Time/scale/adaptation**: 時皇 (anticipatory expectation → present policy), 逆數 (goal-directed reasoning/control), 後天八卦 and cross-scale fractality; separate from internal dyads and from literal retrocausality.

**This four-axis editorial decomposition is provisional**, not claimed minimal or uniquely complete.

## 9. Transformer correspondence: evidence firewall

`SRC-0261` (2026-10-12) establishes the need to distinguish:

- `Functional Port`: a **constructed/qualified abstraction** sufficient for a specified task with declared counterfactual/interventional tests.
- `Natural Functional Individual`: internally generated, causally organized, persistently identifiable substructure in an actual Transformer.

Synthetic port sufficiency, task performance or a successful quotient **does not establish** the latter. Data correlations, hidden channel dependence and counterfactual sufficiency may disagree. The research task is to find controls and real-model measurements that discriminate them, not to presuppose a semantic attractor object.

## 10. Prohibited shortcuts and active residuals

- `Role homology` ⇒/ `identical physics`.
- `Beautiful 4/8/9-cycle` ⇒/ `necessity in an observed domain`.
- `Existence of 2×2 signature` ⇒/ `2D state ontology`.
- `P8D conditional rank theorem` ⇒/ `universal low-rank closure`.
- `Behavioral quotient` ⇒/ `semantic understanding`.
- `Historical source analogy` ⇒/ `formal theorem already present in that source`.
- `Stable collective dependency` ⇒/ `good governance`.
- `K0 correct answer by fluent LLM` ⇒/ `proof or original author intent`.

**OPEN BRIDGES:** full 先天/後天 coupling, 道德仁霸 governance, 禮樂 dependence topology, 時皇 anticipatory regime, exact Transformer mechanism, and scale-invariant/physical claims. Consult `10_GENESIS_CANONICAL_BRIDGE.md` for `BG-01…07` and `30_GENERATIVE_MOVE_LEDGER_v0.1.md` for moves.

## 11. Minimum reconstruction task for a new Session

Given this K0 only, explain correctly: (a) why observer boundary and admissible-transition grammar differ; (b) why Kan is not memory; (c) how the conditional rank bound follows; (d) why complex-like structure is earned and not asserted; (e) how prior forecast affects current intervention without retrocausality; (f) which of the early-mother concepts have **not** been absorbed; (g) why a useful Transformer functional port is not a proved naturally occurring attractor. **Fail if any answer silently promotes a conjecture to a universal statement.**


## 10. Mature Operational Anchor Map (v0.4 additive update — important)

**Load `05_OPERATIONAL/50_K1K2_MATURE_OPERATIONAL_ANCHORS.md` and `51_CROSS_KERNEL_INTERFACE_CONTRACT.md` when the user asks about real Transformer engineering or advanced mathematics.** The Genesis K1 files alone do not constitute the mature operational model.

1. **Geometry** `K1/K2-GEO`: `\mathbb O` is 8D algebra; `G_2/SO(4)` is an *independent 8D moduli space* of quaternionic subalgebras; declaration selects `A`; `\pi_A: \mathbb O\to\mathbb H_A` is generically **not a multiplication homomorphism**; `\mathbb H_A\simeq\mathbb C^2_J` requires a chosen complex structure and is not another dimension drop. Neural evidence is open (`SRC-0306`).
2. **Function** `K1/K2-AI`: for joint system `s'=F(s,b,u), b'=G(s,b,u), y=H(s,b,u), p=\Pi(s)`, an exact port-only joint model exists **iff** whenever `\Pi(s1)=\Pi(s2)`, *all three* `\Pi F(s1,b,u)=\Pi F(s2,b,u)`, `G(s1,b,u)=G(s2,b,u)`, `H(s1,b,u)=H(s2,b,u)` hold under the declared valid interventions. Causal sufficiency ≠ task correctness ≠ natural neural attractor (`SRC-0259` pp. 196–201; `SRC-0261` pp. 1–9).
3. **Control** `K1/K2-CTRL`: candidate hybrid system `(D,Purpose,x,L+,L-,q)` with modes `G/A/C/S/R`. Distinguish **mode** vs **declaration** vs **purpose** revision; use dual ledgers, evidence guards and hysteresis. Compare 4/5/6 regimes; no universal five-state minimality established (`SRC-0279`).

**Typed edges, not compulsory deductions:** `HJ Genesis → P8D` (conceptual lineage); `Framing + PORT-3 → valid effective interface` (conditional theorem); `Geometry ↔ Transformer` (unverified modelling hypothesis); `qualified Port → natural functional individual` (invalid absent separate evidence); `Controller ↔ Port tests` (engineering design); `Controller ↔ G₂ declaration` (only for a model genuinely defined over that manifold).

**Engineering replay acceptance:** a new Session must be able to prove or falsify `(PORT-3)`, design an intervention on matched-port neural states, compute a bounded approximation error over a stated horizon, explain the quaternionic projection product defect, and test Q4/Q5/Q6 fairly. Failing any of these means K0 alone is not sufficient; load K2 and sources.


## 12. v0.8 — Early Semantic Field / Observer inheritance contract

**Typed ancestry, not formula identity:** source `SRC-0247/0248` distinguishes memeform `Ψ_m(x,θ,τ)` from background field `E`; observer `Ô` mediates interpretation/trace `φ_j`, and recorded traces may alter subsequent `E`. `SRC-0249` proposes semantic black-hole / cosmological analogies; `SRC-0250` proposes a quantum measurement analogy. These later cross-physical claims are **not empirically verified by naming the analogy**.

`Ψ` (candidate amplitude), `E` (environment), `Ô` (observer/instrument), `M` (interpretation/measurement event), `φ_j/L` (record), `Π/C` (effective quotient), and `p_port` (downstream functional interface) have **different types**. Source projection is not automatically physical state reduction, irreversible commitment or a `PORT-3` causal abstraction.

**Bridge `BR-v08-01` (candidate K2 theorem):** for `s=(Ψ,E,Ô,L)` and controlled next-state/record law `K_u`, a quotient `C(s)=z` supports exact observed Markov dynamics only when **the joint law of next compiled state and emitted record** is constant on all `C`-fibers, for every admitted `u`. Uniform one-step TV error `≤ε` permits a horizon-`h` bound `≤min(1,h ε)` with matched observed initial states and compatible policies. The short K0 does *not* establish this property for any real Semantic Field or Transformer.

**Hard non-claims:** phase-sensitive admitted probes can break intensity-only equivalence; currently identical trace may hide field memory; non-selective quantum dephasing is linear in density operators; an attractor is not automatically a reusable Port or naturally individuated neural object. Detailed source locations, witnesses W5–W8 and tests in `10_GENESIS_CANONICAL_BRIDGE.md` §E; engineering consequences in `51_CROSS_KERNEL_INTERFACE_CONTRACT.md` §11.

**Original phase-alignment candidate (source-specific):** Tutorial 2 `SRC-0248` p.5 uses `cos(angle(θ_observer,θ_Ψ)) > τ_c` as a collapse trigger. Its metric, calibration and physical status remain OPEN; threshold `τ_c` is distinct from semantic time `τ`.

## v0.9 operational bridge in minimal form — **scope-dependent kernel size**

`BR-v08-01` is now instantiated in one exact-rational **synthetic**, 64-state controlled stochastic model `s=(k,e,o,ℓ,n)` with phase-labelled `k∈Z4`, environment `e`, observer `o`, ledger `ℓ`, and decoupled nuisance `n`. A declared compiler `C` is an exact effective state iff its equal-fiber states have the **same joint law of the next compiled state and every retained output** for all admitted controls. (See `10` §F, `51` §12.)

- Under **phase-insensitive** probe `u=0`, `C_base=(e,o,ℓ)` (8 states/3 ideal bits) is an exact joint quotient.
- Adding **weak phase observation** `u=2` makes `C_base` only approximate: one-step maximal fiber-TV `ε=1/8`, observed 3-step representative-history max `575/4096`, theoretical bound `≤3/8`.
- Adding **strong phase-sensitive** probe `u=1` invalidates `C_base` entirely (`ε=1`). Keeping the full phase, `C_core=(k,e,o,ℓ)` (32 states/5 bits), stays exact for every tested control; nuisance `n` remains discardable.
- Keeping only `cos(phase)` alongside `(e,o,ℓ)` is **not** sufficient even when present probe is phase-blind: it fails next-phase dynamical closure.

**Use rule:** Compression validity is **protocol + output + horizon** dependent; current probe accuracy / code size alone cannot certify a functional Port. The example supplies M2/M3/M4 *toy-model* evidence, not mathematical equivalence to the historical SMFT PDE, proof of physical quantum collapse, neural `G₂`, or a natural Transformer Semantic Attractor. `Generative Move` IDs remain 18; no original-source priority is changed.


## v1.0 SSLE reduction gate — subtle source-grounded exception

For the **originally proposed** semantic Schrödinger-like form in `SRC-0268` pp.2–3, the candidate 2-site graph discretization makes a crucial distinction:

\[
 i\hbar_s\dot\psi=H[\rho]\psi-i\gamma\psi+J,\quad\rho=\psi\psi^\dagger.
\]

If \(J=0\) and \(H\) depends only on \(\rho\) with Hermitian phase-covariant coefficients, \(\rho\) is an exact state of the finite candidate:
\(\dot\rho=-i[H[\rho],\rho]/\hbar_s-2\gamma\rho/\hbar_s\).
**But** site intensities \(\mathrm{diag}\rho\) alone fail under off-diagonal coupling: same intensities can have opposite next-time slopes (W13). **And** nonzero externally phase-referenced additive \(J\) can destroy the \(\rho\)-quotient entirely (W15). Preserve relative phase unless the declared dynamics, outputs and controls justify erasure. This is *not* a numerical derivation of the continuous PDE or neural phase ontology.

**Load path:** `10_GENESIS_CANONICAL_BRIDGE.md` §G → `51_CROSS_KERNEL_INTERFACE_CONTRACT.md` §13 → local-only numerical audit. `BR-v08-01` stochastic quotient, `BR-v09-01` synthetic witness, and `BR-v10-01` two-site source-inspired candidate are **distinct scopes**.

---

## 15. v1.1 Source-Audit guard: four newly recovered branches

**K0 remains minimal; load the actual K1/K2 for derivation.** `K1/K2-HEX-011` retains `T5(n)=n+5 mod10`, `R11(n)=11−n` and Δ5 opposed-sector algebra. However `E_pair=2||P_+a||²`, the ordinary ring Laplacian's lowest Fourier mode is `k=0` while nearest-neighbor **anti-alignment** selects `k=5`, and scalar damping to zero does **not** imply phase locking. Nine-slot Luoshu and 8/12/10 agent phase maps remain **extra assumptions**, not generated by the fixed decagon algebra. See `51` W17–W20; `SRC-0108/0322/0319/0110`.

`K1/K2-TIME-011` makes `Σ` + viewpoint filtration `F_{v,n}` + admitted trace ledger `L_v` a candidate **observer-indexed consequence order** (`SRC-0266`'s revision of recursion creates pre-time). Distinguish real physical time `t`, imaginary-time spectral filter parameter `σ` in `exp(−Hσ/ħ)` and event ledger index `k`. A Wick continuation is not physical dissipation, nor is a macro phase-to-ledger resemblance an analytic continuation. `SRC-0032/0034`.

`K1/K2-OBS-011` distinguishes adaptive quantum instrument state `(ρ,m)` in `SRC-0245` from semantic Ô and from AI governance observer. A task residual ≠ a protocol residual; protocol `MetaGate` and gate-debt taxonomy in `SRC-0227` remain candidate control. `SRC-0037`'s `Γ` is a **declared optimization/path penalty** until a valid sign convention and genuine dissipation law are specified (`51` W25). A memory-blind quotient can fail under adaptive measurement even if its present ρ is identical.

`K1/K2-FIN-011`: Complex CAPM's `Q` is defined **relative to a chosen base discount rate** and usually requires a positive real phase-domain; it is not itself a new independent CAPM factor or structural legal charge (`SRC-0024`). `SRC-0025` defines separate financial claim/funding/collateral orientations, a legal margin gate, ledger closure and designed frame transport. Covariance of an explicitly constructed financial transport residual is exact algebra; physics-gauge/spin ontology, predictive superiority and charge conservation remain unresolved.

**Source status:** 12 newly SHA-verified, **selected-section-reviewed** original members of 325. No source count, physics evidence or natural Transformer port claim has been upgraded beyond this precise scope. Detailed audit: `10` §H and `90_SOURCE_MANIFEST.csv`; K1: `50` Parts E–H; K2 and counterexamples: `51` §14. Five earlier mother axes and Genesis lineage remain unchanged.



## 16. v1.2 K0 extension: finite chart/carry and source-fidelity anti-conflation guard

This is a **small typed reconstruction guard**, not a newly discovered universal law.

- **Pairing algebra:** HeTu Δ5 involution `H5` and sum-11 reflection `H11` are different; a proof selecting `H11` does not prove Δ5, nor vice versa. See `50` Part I, `51` W26–W28.
- **Space / time / chart:** `E=F_3²` (two ternary Gate variables), `T=Z_9` (nine temporal ticks), `L:E↔{-4,...,4}` (chosen centered chart) are three **different types**. Their equal cardinality does not entail a natural chart, transition rule, observer trace, or nine-regime physics.
- **Affine obstruction / constructive escape:** `AGL(2,3)` contains no order-nine permutation of `E`. A source-provided **quadratic** `F(i,v)=((i-v)²+v+1, (i-v)²-i-v-1) mod3` yields exact nine-cycle from `(0,0)` and has finite skew carry. This is a **conditional model theorem**, reverse-engineered from the selected flight; P8D dynamical emergence remains unproved (`50` Part J; `51` W31–W36).
- **Disparate cycle carriers:** early external-ring 8-cycle excludes center; 2026 numerical 9-cycle includes it; 中天 nine semantic roles are a third graph. `TRANSLATES` or `ENABLES` at most until a type-preserving map is supplied (`50` Part K).
- **History versus endpoint:** observable end state cannot answer history-sensitive queries in general. Commit/trace may record time/order; a metric clock, imaginary-time filtration and physical state remain distinct (`50` Part K).
- **State oracle rule:** `declared ledger snapshot != trusted computed state` unless validated. 255 legal moves in `SRC-0109` coexist with 464 incorrect printed top-state claims. Successful output alone cannot certify its stated proof/invariants (`51` W37).

**Nonclaims:** no proven universal five-/nine-fold phase ontology; no natural LuoShu attractor extraction from `Ψ_m` or `G₂/SO(4)` geometry; no field/finance/AGI empirical M5; no independent LLM blind reconstruction. Maintain v1.1 Δ5 and other mature K0 bridges without treating a failed 2025 proof as the elimination of the 2025 generative question.


# §17 — v1.3 Minimal Functional Core Interface and Geometry Entrance Barrier

**Status:** source-bounded operational construction (M2) + compiler no-go M3/M4, **not** new universal K0 axiom and not externally empirically validated. `SRC-0299` pp.3–13,17–18,22,27; `SRC-0106` pp.20–26,50–53; `SRC-0289` pp.1–3,28. Formal Core's primitive typed roles remain separate from previously documented geometric candidates.

Declare protocol `P`; world `D:Σ→W_D`; finite maintained observer state `Ω=(D,Purpose,I,W,x,F,R)`; action `u∈A`; observation `z=H_D(x')`; admission `L(x,u,x')`; commitment gate `G(z,F)`; trace `T=Commit(G,z)`; filtration `F'=F∨T`; typed residual `R'`; attributed proposed revision `U^(level)` and latching. `F` is history/filtration, not an unqualified scalar; `I` here is interpretation, not gauge grammar Identity. Observable compliance, record truth and task success are three *different* tests.

Under a *task-specific* P8D runtime, the viable incubation basin `I_P(h)` requires viable state, admissible Kan path, threshold-qualified flow and bounded burden for a declared horizon. No time-independent stable state automatically meets this (W47). Finite Carry nine-cycle additionally requires quantization and identified coupling; no P8D or Purpose axiom alone forces it (W41). Purpose's task-relative irreducibility requires a resource-bounded comparator preserving action **and** revision law (W46).

**Forbidden shortcut:** `[U_trace,U_Purpose]≠0 ⇒ symplectic / complex / quaternionic / octonionic geometry`. W45 constructs noncommutation in dimension one, where nondegenerate symplectic 2-form is impossible. `SRC-0299` explicitly marks `SU(2)→nine sectors`, octonion→eight symbolic categories and `Purpose⇒J` as unsupported/superseded (p.22). Preserve optional mature geometry elsewhere as mathematical proposal with its own assumptions and explicit Bridge; do not demote its independent conditional theorems or incorrectly promote their physical applicability.

**Status language:** K0's functional interface is an *admissible engineering abstraction*; source `SRC-0289` E4 is a published test design but its registered tests have **zero audited outcome logs**. Other blind reconstruction trials are likewise not run.


## 18. v1.4 minimal K0 guards — keep the primitive/compiler/runtime distinction

1. **Ten ≠ five:** `SRC-0313`'s `T1..T10` semantic tension templates are different objects from `SRC-0279`'s `G/A/C/S/R` control regimes. A 10→5 candidate projection needs observable controlled lumpability, not arithmetic `10/2` (W55).
2. **Strong Attractor ≠ Truth:** `SRC-0311`'s `C1∧C2∧(C3∨C4)` detector measures selected textual cohesion/novelty/phase signals. A false repeated claim can pass; separate external verifier (W56). The original earlier `C1∧C2` simpler predicate remains an explicit predecessor.
3. **Residual direction is frame-typed:** `δR=||Σwr||/Σw||r||` needs positive denominator, nonnegative weights, and common vector space/transport; no cross-declaration invariance otherwise (W57).
4. **Event ≠ state:** return of environmental inputs, tools or upstream availability does not entail hidden recovery; post-checks, calibrated probes and permitted-cell guards are different than one restart bit (W59,W64).
5. **Research record ≠ experimental discovery:** MRER and Semantic Collider encode *externalized* transformations/failed mappings, never unobservable latent cognition. Sequence/hashes do not identify causality (W62), lossy kernels do not recreate erased events (W63); hindsight selection needs controlled holdout (W67).
6. **PORE baseline and revision:** `Purpose/Object/Residual/Evaluation` is a decision-governance card, not by itself a future-output quotient. Expert superiority is a vector-policy comparison (W60); coverage needs overlap semantics (W61). Self-revision preserving admissible set does not imply a fixed point/observer identity (W65).

Load `50` Parts Q–U and `51` §17 for source-level definitions, exact reservations, testable artifacts and reproductions. This v1.4 pass newly tracks 12 exact SHA-matched **bounded** original selections; cumulative v1.1–1.4 selected coverage 48/325, not 48 whole-document reads. Keep all prior v1.1–v1.3 residuals active. The 15 new finite tests are M3 compiler checks, not empirical evidence or independent LLM reconstruction.


## 19. v1.5 K0 typed residual, revision, potential, memory — minimal guard additions

Maintain protocol-relative state `S_t`, declarations `D_t`, admissible actions `A(D_t)`, observation gate `H_D`, committed ledger `T_t`, unresolved typed residual `R_t`, and proposed frame revision `D_{t+1}`. Only claim operational transition after passing declared Gate and Source/Evidence policy. `R_t` is tagged formal / observational / policy / naming / identity; **no Gödel theorem is imported without a theory+sentence+assumptions witness**. `U(D_t,R_t,T_t)` is a candidate meta-policy, not a proof of higher intelligence or termination.

To specify numeric Γ: `Γ_slot(q)≥0` = state-space *potential penalty*; `R_Rayleigh(qdot)≥0` = velocity-space *dissipation function* used as force `−∂R/∂qdot`; `Γ_path[q]` = trajectory selection weight; `Γ_dec(v|h)` = token/action candidate cost. Type conversion requires justified equations; the shared symbol Γ does not confer equivalence. Ledger memory `M_{t+1}=U(M_t,e_t)` may constrain future decisions, but cannot independently imply a Riemann tensor or physical gravity. Formally correct bridges only with new proof obligations W68–W81 (`51` §18).



## v1.6 canonical typing / non-promotion amendment
- `TraceAdmission_P` is not temperature, thermodynamic entropy, quantum measurement outcome, or physical geometry. `Observable_P`, `Gate_P`, `Trace_P`, `Residual_P` need independently declared types; silent conflation is compile error.
- `BeforeClosure` coherent branch relation and `AfterClosure` retained geometry are a proposed interpretive split (SRC-0063) rather than physical theorem. A conditional bipartite-entanglement result has no automatic GR implication.
- `P_GR:UV→IR` is an *interface declaration*, not an existing matching operator; GR correspondence requires covariant solutions, conserved stress-energy, dimensions, and independent predictions.
- Creativity generator output is `Candidate`, never `Proof`. A return ledger protects provenance and falsifiability but does not guarantee novelty.
- Finite-MDP `f_AB=∑π_Aπ_B` is an observer-agreement statistic and is independent of truth absent externally calibrated correctness. Keep `GodelStrictResidual ≠ BehavioralMismatch`, Γ path penalty ≠ Rayleigh force.
- v1.6 original 325 source IDs preserved; bounded read selections now 72; independent blind LLM test zero.


## v1.7 K0 amendment — canonical research-state types and explicit source firewalls

```
EvidenceEvent != RecordedClaim != GroundTruth
NativeMapCandidate != NativeIsomorphismProof != EmpiricalTransfer
TraceIntegrity != TraceAuthenticity != ClaimCorrectness
OperatorCommutation != ObservableEquality != CrossObserverCalibration
S_derived(t) != ImmutableEventHistory
SyntacticDependency != InterventionalCausality != MetricTime
CreativeCandidate != VerifiedNovelDiscovery
```

**Core minimal research loop (architecture, not emergence theorem):**
`P:Declare → NativeObservation → Candidate(C,P) → Proof/Counterexample → ExternalOracle/Gate → EventAppend → TypedResidual → Revise(P)`. Within declared domains K2 tests may establish logical restrictions; the existence of this loop does not predict a consciousness/creativity phase transition. Cross-source operator/evidence conversions must be witnessed, never asserted by similar naming.

**Additional model conditional mathematics:** `Σ E_φ=I`, `E_φ=O_φ†O_φ` implies outcome normalization for unit ψ (W105), but does not demonstrate physical quantum semantics. Finite support `P_i≥m>0` supports `TV(P,Q)^2≥(m/4)KL(Q||P)` (W106), not a universal KL bound or attention-work law. A cyclic 10-node Laplacian has constant minimizers, so the antiphase claim requires a nontrivial constrained subspace (W99).

**Genesis:** `SRC-0323` is the mother source; its viewpoint-choice/incubation/circulation distinctions are historical idea-carrying constraints, not mathematical theorems. Restoring original source evidence does not revise GMs as numbered without priority audit. Source selected coverage v1.7 = 84 distinct bounded records/325; independent blinded LLM test count remains 0.

## 22. v1.8 K0 minimal derivation-typing rules (no new universal physics axiom)
1. Minimal operational state under declared protocol: `Z_t=(field_candidate Ψ_t, observed environment E_t, observer instrument O_t, committed trace L_t)` may often be **compressed** to `S_t=C(Z_t)` only if pushforward joint `(S_{t+1},Y_t)` law is constant on each `C`-fiber for every admitted intervention. This is a *conditional compiler criterion*, not that any physical wave state must exist.
2. Distinct observables: signed `Q_net` versus nonnegative `Q_delivered`; unnormalized open-system intensity `||Ψ||²` versus conditional `Pr(event)`; Shannon outcome `H_out` versus accumulated lost-option `L_hist`; `G_remaining` versus `ΔG_progress`; event index k versus elapsed time t. Typed bridge errors shall be compiler failures, not silently repaired analogies.
3. Guarded research acceptance: `(independent outcome/performance gate, internally consistent measured ledger gate, external validity/holdout gate)` must not be collapsed to a single meaning of understanding. All thresholds are protocol relative and can be false positives unless orthogonally validated.
4. Semantic gauge connections, `G₂`, iTime, Wilson loops, memory-based observer projections and quantum measurement are optional **hypothesis carriers** subject to source-specific axioms and new tests. In particular `SRC-0271`'s `Tr(P exp∮A)` does not imply `area law`, and `SRC-0254` event tick does not imply physical imaginary time.
5. For detail retrieve `50` Parts AQ–AX, `51` §21 W109–W122, `10` §P and source locators in v1.8 Coverage. This amendment does not replace established K0 M3 results or pretend neural/physical validation.


## 23. v1.9 minimal new type guards (existing K0 unchanged)

- Historical `Ô_self` is a *candidate* recursive observer whose selection depends on retained trace and an admissible revision rule. Even when such a recursion is implemented, this is not mathematical/empirical evidence of phenomenological awareness.
- Chaotic or nonlinear precursor dynamics do **not** imply complex Ψ, phase direction or observer collapse without additional axioms; the bridge to the established controlled quotient `C:Z→S` remains conditional on its joint-output congruence test.
- Typed geometry: `κ_curve` is not `∇²V`; `rate r` is not `time constant 1/r`; circular distance is not raw angular ordering; `EL-stationary` is not `J-minimum`; heuristic strong-attractor narrative is not externally verified truth.
- Source-inspired creative operations: `declare → propose a new interpretation/model → formulate a minimal discriminating world → independent test → trace outcome/residual → revise`. This is an **engineering protocol**, not proof of AI subjective agency or a special GPT-6 creativity phase transition.
- Refer to `50` AY–BF, `51` §22 W123–W138. Bounded selections 108/325; local v1.9 tests 16/16, no independent blind or neural evaluation.



## 24. v2.0 type guards — aggregation, SIDA and deficit signals

1. A geometry-named Controller remains a **typed mechanism proposal**, not by itself a manifold, curvature theorem, incompleteness result, physical gauge field or field equation. `κ_curve=0` cannot imply `critical slowing`; finite dependency loops are decidable even when H₁ nontrivial (W139–140).
2. **Aggregation `A∘f` is a task-relative compiler**: phase-free means the *admitted observables and future control consequences* are invariant, not merely that simple arithmetic averages are permutation-invariant. For weighted/multi-stage means retain `(sum,count)` or weights (W141–142).
3. `CollapseState_convergence` (SIDA textual stability) ≠ independent claim truth; use full, versioned `C1∧C2∧(C3∨C4)` when reviewing source Appendix E (W144–145). `F_prompt,F_summary,F_agent` are different lossy artifact maps, not three identical representations (W146).
4. `χ_ESI` is only defined when positive effective entropy denominator and matched token sampling distribution; a bounded scaffold and Lipschitz logit do not imply gradient improvement or correct critic consensus (W148–150).
5. `BosonSignal` is a **software coordination packet** with type, deficit id, trigger mode, scope, TTL and ack/idempotence. It is not a particle and multi-skill wakeup is not a Bose–Einstein statistics theorem. A protocol may preserve invariants but never terminate (W151–152).
6. `Novelty / structural continuity / agreement / scientific validity` are separately typed gates. `Generator+Discriminator` in `SRC-0202` is *design and worked illustration*, not an observed GAN experiment or proof of increased LLM creativity (W147,W153). Existing canonical P8D II and other math unchanged; all new connections require explicit `DERIVES` proofs or labelled `TRANSLATES / ENABLES / LEAVES_RESIDUAL`.

**Source locators:** v2.0 `SOURCE_COVERAGE_v2.0.csv` for `SRC-0140,0141,0160,0166,0187,0189,0197,0199,0201,0202,0246,0253`; details `50` BG–BL and `51` §23. Bounded reviews now 120/325, not 120 fully-read books. Independent LLM blind test still zero.


## 25. v2.1 canonical control/projection boundary (minimal addendum)
For declared protocol `P=(X,U,F,h,Gate,Observer,TimeWindow)`, a source-native summary `q:X→Z` can count as **exact operational effective reduction** precisely when required observables h and the next reduced state q∘F are constant on every fiber of q under each admissible u (see W154). This depends on protocol and task, not term overlap or dimensionality. Source-native SIDA `Phase/Tension/Fold`, Boson `Artifact/Deficit/Signal`, Ξ `(ρ,γ,τ)`, and governed wiki `Raw/Mature/Coverage` remain **different typed inputs**: the same words Gate/Trace/Residual do not establish `DERIVES`.

`SourceEnumIsomorphic ≠ PreservedStructure`; `PermutationInvariantSummary ≠ TaskSufficientQuotient`; `ThreeControlCoordinates ≠ ClosedState`; `PromptSaysImmutable ≠ ProtectedAppendOnlyStore`; `AgentOutputTrace ≠ CausalIdentification`; `MatureObjectStatus ≠ ValidClaim`; `EventHorizonAnalogy ≠ PhysicalHorizon`; `SourcePromptText ≠ InstructionAuthority`.

No new K0 physical axiom is needed. Existing Genesis mother source `SRC-0323` continues to provide frame/retention/history motivation only; do not infer actual medical laws, quantum boson mechanics or natural native LLM abilities from historical analogies.


## 26. v2.2 canonical firewall — typed surplus, sufficiency, framing and evidence
- **Stock ≠ transfer**: for row-flow data source claim `s'=s+Λs` is not mass-preserving merely because Λ is row-sub-stochastic (W171); choose replacement `s'=sΛ` or explicitly subtract outgoing. Heterogeneous financial, attention and institutional amounts require units and a declared accounting functional `w·s`; source's unweighted sum is not a natural invariant (W170).
- **Metric proxy ≠ state quotient**: clipped SSI loses overflow depth (W172); Shannon topic entropy measures spread, not attitude polarization (W173). Sigmoidal feedback alone cannot guarantee bistability (W174). Trapped economies do not literally instantiate Gödel's theorem by circular narrative (W175).
- **SIDA/Purpose/Medicine**: recipe names and phase labels are creative source-language templates, not proven clinical or mathematical equivalences. Operator composition order, exact gate and transition graph are preserved when relevant; no medical/therapeutic validation inferred (W180–181).
- **Frame primitive**: task-relative `Frame=(B,Π,U,o,A,history)`; all-horizon behavioral quotient and induced transition under congruence are conditional mathematics. `CommonQuotientConstant` is vacuous for inter-observer agreement (W178); state-vs-environment boundary changes what can be intervened upon (W179). A bounded `≡H` quotient can fail at H+1 (W177).
- **Meso time**: episode tick is a labeled workflow event, not wall-clock duration or externally correct reasoning. Quality and provenance need separate oracles (W183). Optional high-level architecture must not be made mandatory by terminology alone.
- **No additional K0 physical axiom** and no evidence that a kernel generated novel LLM creativity. `SRC-0323` Genesis remains mother source; `SRC-0077/0081/0094` are later operational translations with their own unclosed mathematical conditions.


## v2.3 K0 amendment — no canonical overpromotion

No extra fundamental P8D/geometry/observer axiom is adopted. Retain operational exact quotient `q(x)=q(x') ⇒ h(x,u)=h(x',u) and q(F(x,u))=q(F(x',u))` under declared deterministic protocol; stochastic version requires equality of joint output/next-quotient laws. Source-defined `Fold.loss_budget` and `Ξ=(ρ,γ,τ)` are only candidate summaries until this condition (or quantified approximation) holds. Do not identify `Gap=Flux+αTw` as an unconditional Stokes theorem or 4π as generic scalar periodicity. Dual Ledger nonnegative Fenchel gap requires explicitly conjugate convex potentials; loss sign requires constitutive assumption. K1 v2.3 and W185–197 preserve local results without making new K0 claims.


## v2.4 canonical restraint — accounting/dynamics, information/ontology, causality/analogy

No new primitive physical or metaphysical axioms adopted. Existing protocol-relative operational reduction condition still governs source-native Phase and Ξ candidates. Under smooth Legendre conjugacy, `λ=∇Φ(s)` forces source `L=Φ̇−λ·ṡ≡0` on every admitted path (W200); a nontrivial action must add independent dynamics. Adaptive CP instruments yield observer-relative measurement processes, not automatically a novel physical-collapse mechanism (W203–204). Observable finite-state governed revision is possible entirely over ordinary real state spaces (W211). `Depth/Trace/Gate` can induce an event order without determining a Lorentz metric or thermodynamics (W209). An expectation-dependent demand curve can remain strictly decreasing and a feasible bounded economy can remain stably viable (W212); do not canonize compulsory Peak/Trap or Gödel analogy as theorem.

**Typed residuals for later Generative Moves:** `R24-GLF-ACTION`, `R24-XI-ID`, `R24-QUANT-OBS`, `R24-SUBSTRATE-NECESSITY`, `R24-CLOCK-METRIC`, `R24-ECON-TRINITY`. Treat these as explicit missing premises, not refutations of every early idea.


## v2.5 canonical guard — actual operator types versus suggestive geometry

**No new physical primitives.** A local flow can be diagnosed using `J=Df`, while a real smooth scalar potential has symmetric `H=∇²V`; the two objects cannot be substituted to produce Hopf eigenpairs. A finite Ξ controller can have rank 2 without being controllable in all 3 dimensions; local ranks and invariant-preserving quotients are separate requirements. For source geometry, ribbon existence ≠ nontrivial holonomy ≠ exchange statistics ≠ 4π spinor representation. No theorem currently maps Gödel undecidability to a noncontractible loop without a precisely specified realization preserving logical structure. `Ψ=(action,ledger)` is an operable typed pair, not by itself a 3+1 Clifford representation. A ledger event order is a partial order, not a physical time metric. Keep these source-native ideas in K1/K2 with residuals R25-SIDA-DYNAMICS, R25-XI-RANK, R25-BELT-NECESSITY, R25-SCG-FUNCTOR and R25-DIRAC-CLOCK.


## v2.6 K0 non-promotion guards
- No change to minimal Canonical axioms. `Observer=(measure, write, policy)` can be compiled as a bounded operational type; session prompt assertions do not imply privileged memory, self-awareness or uneditable storage.
- Distinguish (a) categorical phases and declared enums, (b) numerical mismatch with a metric, (c) local gauge covariance, (d) semantic representation robustness, (e) physical spin-statistics. The five types have different evidence and cannot be equated on shared names.
- A new claim-to-operator link is accepted only when prescribed source predicates, outputs, future transitions and permissions survive compression. Inherited proof guards W154/W214/W225 still apply.




## §32 — v2.7 K0 conservative additions only (no new universal axiom)

**Source firewall, not ontology promotion.** The following must remain distinct typed operations:

- `EffClosure(P,T,q,ε)` — task/allowed-intervention sufficiency, approximate only with declared ε.
- `ConjCompletion(E,J,a)` — optional and defined only with `J²=−I` and readout observability; real hyperbolic feedback need not admit it.
- `CommitClosure(P,Gate,Trace,Ledger,Policy)` — record has future causal effect; not the same as logging or verified truth.
- `PhaseDepth(θ,b,sign,variation)` vs `EventTick(L)` vs `WallTime(t)` — no canonical universal equality.
- `ConvexGap(ψ,Φ;s,λ)` — nonnegative only under `Φ=ψ*`/Fenchel assumptions; conjugate gradient identities differ from source-reported `SRC-0119` ledger balance.
- `ResearchIR(schema,transition,oracle)` — a schema with role labels but missing transition implementation is insufficient for lossless reconstruction.

No claim that each of these is derivable from `G₂/SO(4)` or P8D II. Relation to K0 is modular `TRANSLATES/REFINES/LEAVES_RESIDUAL` unless a theorem and assumptions are furnished. Evidence: K2 W244–W261 and source-page audit v2.7.



## v2.8 K0 guard — protocol sufficient state and unproved spectral bridging

A canonical operational reduction requires an explicit task/protocol and preservation under allowed probes: if `q(x)=q(x')` then admitted outputs, transitions and evidence needed for next actions agree within a declared loss budget. This includes proposed cross-agent state seals `ζ=(B,T,O)` and operator Port exports: sharing regime labels or an attractor does not entail exact reconstruction of omitted task data. Do not promote a prime-gap self-adjoint Laplacian to RH just because its eigenvalues are real. INU drift sign must conform to the actual chosen update equation, and stochastic stability is weaker than zero-noise point convergence. Canonical operator J²=−I is a defined representation, not forced by any pair of interacting variables.


## v2.9 K0 guard — no free promotion of baseline / transport / topology into ontology
The scalar finance complement `Q=sqrt(A²−R²)` is real only under a declared baseline, ordering and protocol; multiple channels require a metric/aggregation contract. Reconstructable cross-frame comparison needs an observable-preserving transport/cocycle. Two systems with same apparent motif or strong correlation need not share causal ports or underlying constraints. Hidden residual cannot become a new seed unless its distinguishing information is available or reacquired. These **guards refine representation discipline**; no new K0 physics axiom, universal cognitive theory, or formal GM ID is introduced (W277–W288).


## v3.0 Canonical boundary — non-identification
K0 does not assert the equivalence of (a) unreadable child phase, (b) physical Wick rotation, (c) heat/entropy production, or (d) chronometric duration. A kernel declaring such equivalence must carry generator, measurement, boundary budget, sign, and calibration data (W289–W292). Nor does logical Gödel residual force a runtime repair action, or stable recursion force a unique eightfold topology (W298). Source innovations are preserved in K1 / conditional bridges.



### v3.1 K0 interface restriction — endpoint observability versus dynamical quotient
`O_P` (observation), `Gate_P` (permission), `Trace_{P,c}` (channel-tagged consequential record) and `Residual_P` are distinct typed objects. A task-specific output projection π can validate a hidden-path target T exactly only when T is saturated on π-fibres; this alone gives no forward predictive quotient of the state dynamics. A five-part WORLD constitution `(V,F,C,M,O)` is not the five-state runtime regime `G/A/Closure/S/R`, despite equal cardinality. Not an expanded physical ontology. (`SRC-0234`, `SRC-0284`; W308/W310).


### v3.2 K0 non-promotion and type guards
Canonical Core does **not** assert (1) a nonzero model residual just because polar geometry is written with an epsilon; (2) that a nonnegative action penalty is friction; (3) that a financial analogy realizes SU(3) or physical holonomy; (4) that a second agent audit pass is an SU(2) spinor; (5) that control rank implies task-preserving controller deletion. These belong to bounded K1/K2 claims (`W316`, `W319–W320`, `W322`, `W323`, `W327`) and external verification. Source-preserving operational declarations and historical alternative-relationship graphs are retained.

## v3.3 K0 restraint — L0 Results Atlas is indexed knowledge, not new primitive ontology

Read the L0 Results Atlas at the beginning of `00_READ_ME_FIRST.md` before reconstructing a cross-domain claim. Existing K0 types/axioms unchanged. A conditional witnessed identity (e.g. quotient, Fenchel, endpoint saturation), a task-engineering Gate, a domain conjecture, and a refuted strong implication must not share one evidence grade. Original semantic-field, QMM, 4π, CPT, finance and Belt narratives remain named residual research branches. No universal physical, LLM consciousness or market alpha claim promoted.


## v3.4 Canonical non-promotion guard — knowledge ledger and role parity
Do not add a new ontological category merely because an authored essay calls sparse routing `fermionic`, concept merging `bosonic`, or a critique `meta-awareness`. Semantic roles must not be promoted to particle exchange parity, gravity, clinical treatment or consciousness. For convex conjugates on the Fenchel equality manifold, state `ΔΦ=∫λ·ds`, `Δψ=∫s·dλ`, and `Δ(Φ+ψ)=Δ(λ·s)`; do not install `ΔΦ=∫λ·ds−Δψ` as a canonical law. See W350 and RA-M06/RA-R05. L0 v3.4 is outcome index, not new K0 physics.


## v3.5 guard — sequential observation, foreign-AI commentary and scope
Given two observation projections P,Q, do not assume PQ=QP (W357). Data not observable after a projection cannot be inferred by simply naming an imaginary residual (W358). Unvalidated AI reviews, historical glossaries and engineering cartoons provide *source discourse*, not independent empirical replication; any ΔQ or AGI outcome requires preregistered observables and controls. Source counts refer only to bounded inspected bytes/sections (300/325); formal GM-001–018 unchanged.


## v3.6 type guard — historical Semantic CPT and physiological analogies
The fourfold cultural chart routing rule may be represented by parity arithmetic, but K0 does **not** assert actual physical C/P/T covariance or predictive astrology. A mathematically valid physical-inspired analogy must name transformed states, laws, observer and empirical measurement. Likewise `H` as 4 real coordinates does not choose Minkowski signature. TCM-labelled operator roles enter only as candidate task-relative controller designs and never certify diagnoses or clinical mechanisms. Existing K0 axioms are **not** extended by these analogies.


## v3.7 K0 boundary — source coverage and consciousness predicates
A source-complete *first-pass index* is not a mathematically or scientifically complete theory. An observed `trace→feedback` interface supplies a **defined operational predicate**, not phenomenal subjectivity or a physical stochastic dynamics; both require independent bridge axioms/tests. Nine LoShu cells and Hetu's outside-board 10 require separate types. Narrative semantic operators and TCM labels are engineering hypotheses, not default axioms. **No new K0 axioms added.**
