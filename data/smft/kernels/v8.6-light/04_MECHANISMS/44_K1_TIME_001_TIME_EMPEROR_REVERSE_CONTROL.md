---
artifact_id: SMFT-KERN-K1-TIME-001
kernel_id: K1-TIME-001
version: 0.3.0
snapshot_date: 2026-10-14
status: source-anchored-conditional-construction
logical_path: 04_MECHANISMS/44_K1_TIME_001_TIME_EMPEROR_REVERSE_CONTROL.md
language: zh-Hant+en
origin_sources: [SRC-0323]
translation_sources: [SRC-0309]
formal_context: [SRC-0106, SRC-0299, SRC-0279]
generative_moves: [GM-005, GM-013, GM-014]
---

# K1-TIME-001 — 時皇 × 逆數 × Expectation-Driven World Formation / Backward Control

> **MICRO-KERNEL:** 《皇極經濟》的「時皇」不是物理時間倒流定理，而是一個更微妙的 **anticipated future as present organizing information**：可信（或被信以為真）的未來預期在當下改變參與者的互動與資源配置，可能自我促成、亦可能自我挫敗。§4.6「逆數」至少有兩種不同而相關的運作：**由既有生成規律推知未來（forecast/inference）**，以及**由目標未來逆求現在應施行的制度、傳播與維持機制（backward planning/control）**。兩者都沿正常物理時間向前實行；不可把 planning-arrow 當作 causal-arrow。

## 1. Anchored source genealogy and original uncertainty

**Genesis `SRC-0323`:** §4.5a ¶1061–1080 uses 泰 as access/new matching of heaven/earth rather than mere topological swap. §4.5b ¶1081–1097 gives succession example: a signal of future heir apparent reorganizes *current* allegiance, resources and coordination even before accession; present actions may then help actualize the anticipated regime. §4.5c ¶1100–1123 explicitly draws analogies to relativity / spatial-temporal curvature, yet calls for caution, asks whether 時皇 differs from 人皇 and whether false announcements are 皇 or 霸, and acknowledges incompleteness. Treat **claimed physical equivalence as analogy/conjecture, not a result**.

**`SRC-0323` §4.6a/b ¶1127–1156:** draws on 「數往者順，知來者逆」. Proposed *developmental explanatory sequence* is Qian–Kun opportunity → Gen–Dui nurturing/continued flow → Zhen–Xun reproduction/propagation → Kan–Li mutually regulated ecosystem. **Reverse control** starts by altering a leverageable Kan–Li institution/strategy, aims to generate propagation, supports sustainability by incubation, and can yield a new opportunity/recognizable world. §4.6b ¶1154 cautions transitions are **not necessary**; §4.6c ¶1159–1166 demands that analysts identify the actual difference/flow and layer instead of abstract metaphor.

**2024 translation `SRC-0309`:** Chapter 1 ¶20–26, 37–65 distinguishes externally indexed **Adaptation Trigrams** (clock-like macroeconomic phase) from internally relational **Incubation Trigrams**. This is a *separate phase variable*, **not identical with 時皇**, and does not prove cyclical prediction.

**Later grammar:** `SRC-0106` §3 protocol and §5 Kan–Li (`(5.3),(5.10)`), §11 incubation/recovery, §12 effective theory. `SRC-0299` pp. 4–12 defines Declaration `D:Σ→W_D`, the difference state/policy/purpose/declaration revision, Gate, Trace, Residual, Latching and Purpose; `SRC-0279` pp. 3–6, 18–25 proposes **multi-regime control and hysteresis** rather than compulsory calendar phases. These are bridges for formalization, **not documentary evidence that HJ already contained these operators in 2024**.

## 2. Three arrows must remain distinct

1. **Physical/event causal arrow `→_c`:** past physical signal and current decisions affect later state. `s_t → b_t → u_t → x_{t+1}`. There is no empirical proof in these sources of future events physically sending signals to the past.
2. **Inference/forecast arrow `→_i`:** given past/current trace, forecast the distribution of later outcomes: `H_{≤t} → \widehat{P}(x_{t+h}|H_{≤t})`. This is an information calculation at `t`.
3. **Design/backward-planning arrow `←_d`:** given terminal objective `G`, compute what earlier admissible controls could reach it: `G_h ← Pre_L(G_h) ← ... ← Pre_L^h(G_h)`. This is reverse *computation*, not physical reverse chronology.

Also distinguish **reported forecast** from **truthful forecast** and **purpose** from mere instantaneous goal. An announced future may work by changing beliefs despite being false; classification as 皇 / 霸 is precisely an unresolved normative/causal distinction in HJ §4.5c.

## 3. Minimal typed expectation-dependent model — COMPILER PROPOSAL (`M2`)

Fix protocol `P` (who/what is the developing subject, boundaries, observations, timescale, admissible interventions). Define:

- `x_t∈X_P`: physical/social/economic state; `r_t`: operating regime; `L_t`: Li admissibility relation.
- `s_t∈S`: a current signal, announcement, reputation cue or observed commitment concerning a proposed future; `b_t∈B`: current belief distribution about future outcomes (agent-indexed if needed).
- `u_t∈U`: feasible control/response chosen by agents; `H_t`: committed evidence trace; `G⊂X` terminal goal (not necessarily Purpose).
- `T_r` and `\mathcal B` are specified forward dynamics and belief-update rules, with randomness `\xi_t`.

$$
 b_{t+1}=\mathcal B_P(b_t,s_t,H_t),\qquad
 u_t=\pi_P(x_t,b_t,G,L_t),\qquad
 x_{t+1}=T_{r_t}(x_t,u_t,\xi_t),\quad (x_t,u_t,x_{t+1})\in L_t.
$$

Read this in normal temporal order. **A future event is not an argument causally entering the previous state; a *present representation of a future event* is.** An additional update can condition future declarations on admitted traces and residuals: `D_{n+1}=U_D(D_n,L_n^+,L_n^-)` only after its own guard and evidence conditions; refer `SRC-0299`, not HJ as source of this exact equation.

**Two feedback signs:** A credible succession signal may make joining new coalition increasingly attractive (positive social complementarity); a warning of future shortages may instead cause present conservation that **prevents** the shortage (negative anticipatory feedback). The sign must be established, not assumed.

## 4. The non-obvious generative move: a new future can be *organized before it exists*

`GM-013`:

- `OLD FRAME`: a trend is only extrapolation of current physical/economic flows; present behavior responds only to realized current resources.
- `IMPASSE`: actors reorganize before the publicly anticipated event exists; a belief can *create* the very coordination that subsequently validates it.
- `MOVE`: promote **present future-expectation / announcement / shared belief** into a first-class, causally active present state, while allowing feedback between belief and realized outcome.
- `ENABLED`: equilibrium selection, credibility / signaling games, announced standards, recruitment into new organizations, self-fulfilling vs self-defeating policy, world-formation via expectation and commitment.
- `LIMIT`: present belief is real and causal; a physically nonexistent future event has no backward causal link shown here. HJ's spacetime language is a metaphor, not a proof of relativistic equivalence.
- `RESIDUAL`: how a true new 道 differs from manipulation/propaganda/霸; institutional vs temporal innovation; endogenous trust; genuine new world vs relabeling old world.

**Tiny coordination construction (COMPILER EXAMPLE, `M3` for fixed-point arithmetic only):** suppose a population joins a proposed successor regime if it expects at least a fraction `q∈(0,1)` of participants to join. With homogeneous, fully informed strategic expectations, `p=0` and `p=1` are both self-consistent stationary participation equilibria: if `p=0`, no one joins; if `p=1`, everyone joins. A credible announcement can help select one equilibrium **in an appropriate specified learning/selection model**, but the existence of two fixed points **does not prove** that a signal will move the population between them. Add heterogeneous thresholds, enforcement, imperfect information and finite funds before claiming predictions.

## 5. Inverse calculation as **reachable-set** control (`GM-014`)

Assume for this subsection a deterministic discrete finite-horizon controlled system with **declared** time-dependent allowed transitions:

$$
 x_{t+1}=F_t(x_t,a_t),\qquad (x_t,a_t,F_t(x_t,a_t))\in L_t.
$$

For any target state set `A⊆X`, define the admissible backward predecessor:

$$
 \operatorname{Pre}_{L,t}(A)
 =\{x\in X:\exists a\in U_t(x),\; (x,a,F_t(x,a))\in L_t,\; F_t(x,a)\in A\}.
$$

Start from terminal target `G_h=G` and compute:

$$
G_t=\operatorname{Pre}_{L,t}(G_{t+1}),\qquad t=h-1,\ldots,0.
$$

**Elementary conditional theorem:** `x_0∈G_0` iff there exists an admissible `h`-step control path ending in `G`, under the stated deterministic Markov/time-indexed assumptions. Proof by backward induction on remaining steps. This is a **standard control construction introduced by the compiler** (`M3`), **not** HJ's formula or a proof that all phenomena must follow P8D order.

**Guard 1:** A target can be unreachable. If `L` prohibits the desired institutional transition, no amount of encouraging propaganda changes `Pre_L` unless the rule/admissible action set *itself* can be legitimately revised.

**Guard 2:** For disturbances `w∈W`, a robust predecessor might require `∃a∀w: F(x,a,w)∈A`, whereas `∀w∃a` assumes the controller observes disturbance before choosing control. Changing quantifiers changes the theorem and feasible set. Dynamic replanning with feedback policy is yet another formulation.

**Guard 3:** Backward planning computes a set of necessary feasible ancestors of the goal; it does **not** mean the *development* of any organism always follows a single arrow `QianKun→GenDui→ZhenXun→KanLi` or that the planner can always choose Li arbitrarily.

## 6. How this connects to the 2024 「順生 / 逆控」 intuition

Source-grounded non-universal explanatory **forward** story:

`opportunity/transduction (天地) → nurturing/exchange (山澤) → triggering/propagation (雷風) → institutionally regulated interdependence (水火)`.

Source-grounded **reverse managerial** inquiry:

`What Kan–Li rule/realization is controllable now? → what triggers/relays would it activate? → what buffer/exchange makes it repeatable? → what new usable differential / operational world could result?`

The second is a *design requirement graph*, not reversed execution of the first. Reverse inquiry might start elsewhere if direct interventions or model limitations require it. The P8D II typed dyads are interacting functions, not universal historical ages.

**Time phase firewall:** external 後天 adaptation phases `a_ext(t)` may enter `F` or modify constraints, but cannot be conflated with `b_t`, the present belief in a proposed future. Likewise Purpose is a persistent counterfactual criterion (`SRC-0299` pp. 9–10), not every short-term anticipated outcome.

## 7. Bridge to world-revision, with honest limits

`SRC-0279` posits a hybrid regime `q∈{Generation,Activation,Closure,Selection,Retention}` with hysteresis; `SRC-0299` separates state vs policy vs declaration vs purpose revision. Time-Emperor-type anticipation may bias **which candidate future becomes salient**, but **salience is not admission**:

`Future proposal / belief → present attention + action (possibly candidate effects) → qualified evidence → Gate → Trace + Residual → possible Revision / new Declaration`.

Without evidence and an explicit Gate, a collective belief could still dominate agents, but claiming it is **a valid new world** would be a separate normative/empirical assertion. An engineered Transformer or multi-agent realization must specify measurement of `b`, intervention on signals, causal effects on `u`, persistence/recoverability and whether source model or target model is being evaluated. Output narrative fluency alone is not evidence of a natural circuit/attractor.

## 8. Counterfactual tests / reconstruction questions

1. **Self-fulfilling vs self-defeating:** Two announced futures have the same accuracy ex ante; one causes action increasing its chance, another causes prevention. Model feedback signs and explain why mere forecast accuracy cannot identify 時皇.
2. **Backward planning vs retrocausality:** Reconstruct §4.5 heir example as a causal graph with present signal/expectation; identify exactly which edge would be needed for genuine physical retrocausation and why sources do not support it.
3. **Goal unreachable:** Give an admission relation Li under which target cannot be attained regardless of predictive confidence. Show `Pre_L(G)=∅` in a simple two-state example.
4. **Quantifier audit:** Distinguish `∃a∀w` from `∀w∃a` in a one-step recoverability problem; produce a case where they give different answers.
5. **Historical tension:** Explain why HJ asks if false prospect manipulation is 皇 or 霸, and why an instrumental system could show large causal effect without epistemic/moral legitimacy.
6. **Differing time types:** Separate operational time, retrospective inference, planned time, shared expectation, later declaration-revision time, and externally postulated adaptation-cycle phase.

## 9. Evidence / provenance and no-go claims

| Claim | Grade / proof state | Primary locator |
|---|---|---|
| 「時皇」 creates a present trend via future-focused belief | `M0` source statement with author's explicit doubts | `SRC-0323` §4.5, ¶1081–1123 |
| Forward generation vs reverse-control explanation | `M0` conceptual text, **not** fixed universal chronology | `SRC-0323` §4.6b, ¶1140–1156 |
| Internal-vs-external trigram distinctions | `M0/M1` 2024 business interpretation | `SRC-0309` Ch. 1 ¶20–26, 37–65 |
| `Pre_L` recursive reachability iff control path | `M3` conditional mathematical consequence, compiler proof | §5 of this document, standard mathematical construction |
| Multiple coordination fixed points | `M3` only in specified toy threshold assumptions | §4 of this document, not an HJ theorem |
| Declaration, Gate, Trace, Purpose, hysteresis | `M2` definitions/architecture of later work | `SRC-0299` pp. 4–12; `SRC-0279` pp. 18–25 |
| Physical backward causation / quantum-gravity equivalence | **Unproven / not licensed** | Speculative analogy in `SRC-0323` §4.5c |

**Hard stop:** `"anticipatory causation"` here means ordinary *present expectation causing present action*, **not** future causes physically modifying past events. A compelling political or financial narrative has no theorem-level force without identifying actual state, incentives, constraints and interventions.
