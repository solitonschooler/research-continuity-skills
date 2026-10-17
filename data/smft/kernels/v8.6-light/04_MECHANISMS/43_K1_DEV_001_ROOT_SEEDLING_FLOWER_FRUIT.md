---
artifact_id: SMFT-KERN-K1-DEV-001
kernel_id: K1-DEV-001
version: 0.3.0
snapshot_date: 2026-10-14
status: source-anchored-conditional-construction
logical_path: 04_MECHANISMS/43_K1_DEV_001_ROOT_SEEDLING_FLOWER_FRUIT.md
language: zh-Hant+en
origin_sources: [SRC-0323]
translation_sources: [SRC-0309]
formal_context: [SRC-0106, SRC-0279, SRC-0299]
generative_moves: [GM-007, GM-012]
---

# K1-DEV-001 — 根苗花果 × Incubation / Recovery / Evolutionary Investment

> **MICRO-KERNEL:** 《皇極經濟》的「根苗花果」不是生命週期的四個時間標籤，也不是四個字與 P8D 四對 dyads 的任意對照。它是**固定一個發育主體及觀點後**，將當前的自強機制（**根：定位可取得的機會；苗：持續統攝要素的本業模式**）與兩種犧牲當下資源的未來導向行為（**花：改進本業的高風險探索；果：在新空間複製／傳播本業**）分開。P8D II 的 incubation basin 為整個系統的 viability / qualified flow / admissibility / residual 提供更嚴格的條件，但 **花 ≠ Incubation Basin**；花的非平凡內容在於 *option creation, experiment cost, mediation/exchange, failure burden, and delayed improvement*。

## 1. Source proof of ancestry, not retrospective attribution

**Genesis source `SRC-0323`:** §7.3a paragraphs 1929–1939: **identify the developing object and its observed result before inventing its environment**. §7.3b ¶1943–1951: four functions; **「根苗」自強 / 「花果」發展投資**. §7.3c ¶1954–1975: definitions and **three distinct costs of 花**: (i) internal research investment, (ii) expenditure to access/couple external partners/experience/resources (花蜜付給媒人), (iii) failure cost displacing viable alternatives. §7.3d ¶1979–1987: partner filters / compatibility as a way of containing exploration failure. §7.3e ¶2000–2005: same carrier under play-vs-profit protocol changes what counts as 花/果. §4.3b ¶970–989 provides another embryo: challenge + nurturing/buffer + generalized exchange medium enabling evolution.

**Translation `SRC-0309` Chapter 1 ¶20–26, 53–69:** Incubation Trigrams (internal relational roles) and Adaptation Trigrams (external-cycle phases) are **two classifications**, not synonyms. `8×8` proposed combinations are not empirical periodic necessity.

**Mature mathematical reference `SRC-0106`:** §11 physical PDF pages 49–55, especially `(11.1)–(11.15)` and `(11.20)–(11.26)`, and §12 pages 55–59 on effective reduction. Sources state that incubation is not mere equilibrium. A later *five-regime* candidate (`SRC-0279`, pp. 5–11, 23–25) distinguishes Generation, Activation, Closure, Selection, Retention; this is a **possible compiler bridge**, not proof that 根苗花果 = G/A/C/S/R. `SRC-0299` pp. 4–9 distinguishes Declaration, Gate, Trace, Residual and Revision.

**Important chronology:** stable source IDs/hash do not prove these are the *earliest invention dates*. All mathematics introduced as **COMPILER PROPOSAL** below is post hoc operationalization, not a mathematical formula authored in 2024.

## 2. Role types: no false one-to-one correspondence

| HJ development function | Question and type | P8D / later possible realization | Non-equivalence guard |
|---|---|---|---|
| 根 / `Root` | What **opportunity-to-resource differential** is available to this *particular* developing object? | Qian–Kun potential/transduction, conditioned on declared perspective | Root ≠ physical ground, exogenous demand, or an automatically profitable gradient |
| 苗 / `Sprout` | How does the incumbent **recurrently reproduce viable operation**? | Kan–Li admissible operating routes; qualified Q; other dyads coupled | 苗 ≠ the full 8-role grammar and not merely monetary profit |
| 花 / `Flower` | What **resources, compatibility checks and failed trials** are risked to improve the *incumbent generative mode*? | Gen–Dui buffer/exchange; exploration experiments; recovery; information-bearing residual | 花 ≠ generic propagation; ≠ all of incubation; ≠ automatic increase of fitness |
| 果 / `Fruit` | What resources are committed to **replication into other contexts** with transfer/adaptation costs? | Zhen–Xun transmission/activation; repeated feasible instantiation | 果 ≠ guaranteed faithful transfer, ≠ experimental novelty, ≠ universal fitness |

**Source-specific inversion:** HJ §7.3c introduces 果 before 花. Do not manufacture a required time ordering `Root→Sprout→Flower→Fruit`. A system may make fruit-like expansion using the old mode, flower-like research in parallel, or fail before either.

## 3. Formal interface with P8D II: incubation is a property of the *whole runtime*

For a declared protocol `P`, state space `X_P`, viable region `V_P`, admissibility relation `L_t`, Kan realization policies `Π_K`, horizon `h`, qualified flow `Q_P` and specified residual magnitude `R_P`, P8D II `(11.7)` defines (a time-discrete rendering, with terminal viability checked separately):

$$
\mathcal I_P(h)=\left\{x_0:\exists\pi\in\Pi_K,\;x_t\in V_P\;(0\le t\le h),\; (x_t,a_t,x_{t+1})\in L_t,\;Q_P(t)\ge Q_{\min},\;R_P(t)\le R_{\max}\;(0\le t<h)\right\}.
$$

This is a **definition for a declared model** (`M2`), not empirical evidence that any particular ecosystem/business/LLM qualifies. P8D II `(11.14–11.15)` also offers a *probabilistic* version with joint success probability at least `1−δ`. When temporary recovery windows are admissible, specify **exceptions to `Q_min`**, rather than simultaneously insisting every timestep has full throughput and experimenting with a shutdown.

**Crucial proof boundary:** In source `(11.8)`, recoverability is described as *implicit* and `(11.9)` defines a recovery-radius diagnostic. Mere membership `x_0∈I_P(h)` under an `∃π` path **does not logically guarantee any positive robust recovery radius** `ρ_rec>0` against nonzero perturbations. A singleton viability set is a trivial counterexample. The stronger property must specify perturbation set, action timing, recovery horizon, and quantifier order:

$$
\forall\delta\in D_P(x,\rho)\;\exists\pi_\delta\in\Pi_K:\;\Phi^{\pi_\delta}_{\le T_{rec}}(x+\delta)\in\mathcal I_P(h),
$$

with constraints also respected along the recovery path. `∀δ∃π` permits observing disturbance then adapting; `∃π∀δ` requires a *single* policy robust to all tested disturbances. Do not confuse them. Basin volume `|I_P|` and recovery radius are independent diagnostics, as P8D II explicitly notes in `(11.10)`.

## 4. A minimal budgeted evolutionary-investment model — COMPILER PROPOSAL (`M2`)

Declare the carrier `X` (firm, organism, project, AI runtime), environment and horizon. Example state and choices:

- `s_t≥0`: deployable resources; `m_t∈M_t`: incumbent recurrent operating mode (苗); `e_t`: experimental candidate/knowledge state; `y_t`: replicated installations (果); `r_t≥0`: unresolved residual/failure burden; `H_t`: committed observations (trace).
- `b_t`: required sustaining expenditure; `i_t`: flower-like experimental investment; `p_t`: fruit-like replication investment; **no implication** that all currencies share the same units without explicit conversion.
- `q_t(m_t,x_t)`: qualified operation; `V_P`: viability; `L_t`: admitted transitions; `κ_P`: identity/recovery constraint.

A possible budget relation with units declared:

$$
 b_t+i_t+p_t\le s_t+\mathrm{inflow}_t,\quad i_t,p_t\ge0.
$$

The resource update and experimental results depend on domain-specific `F_{P}` and random variables `\xi_t`; **do not fabricate a universal transition law**. A useful schematic transition is:

$$
(s_{t+1},m_{t+1},e_{t+1},y_{t+1},r_{t+1})
=F_P(s_t,m_t,e_t,y_t,r_t,b_t,i_t,p_t,a_t,\xi_t),
\qquad (x_t,a_t,x_{t+1})\in L_t.
$$

**Three flower costs** (HJ §7.3c) can be registered as `c_internal`, `c_interface`, `c_failure_opportunity`. `c_interface` has a separate actor/partner and compatibility gate. `c_failure_opportunity` includes foregone deployment or displacement of proven modes; it is **not** just the direct monetary loss of a failed trial.

A candidate *typed* path:

`Incumbent viability (根+苗) → costed experiment (花) → measured outcome / failure trace → admissibility and model evaluation → optional mode revision m→m' → optional transfer / dissemination (果)`.

This is an **engineering workflow proposal**, not a mandatory natural life-cycle.

## 5. Information-value lemma: why 花 can be useful without being always good

Let `a∈A` be a finite action set, future unknown state `ω`, integrable reward `u(a,ω)`, and observation `Y` obtained by an experiment. If the experiment **only adds information** and has no cost, does not change the available action set, and the decision maker may ignore `Y`, then:

$$
\underbrace{\mathbb E_Y\left[\max_{a\in A}\mathbb E[u(a,\omega)\mid Y]\right]}_{V_{\mathrm{with\ info}}}
\ge \underbrace{\max_{a\in A}\mathbb E[u(a,\omega)]}_{V_{\mathrm{without\ info}}}.
$$

**Short proof:** for each fixed `a`, `max_{a'}E[u(a',ω)|Y]≥E[u(a,ω)|Y]`; take expectation and maximize the fixed `a`. This **generic value-of-information theorem** is a compiler-provided conditional result (`M3`), **not** a scientific proof of the universality of 花 or a theorem in HJ/P8D II.

After `c_internal+c_interface+c_failure_opportunity`, viability threats, selection bias or irreversible experiments, net value can be **negative**. A cheaper control, no experiment, or direct 果 replication can dominate. If `Y` has zero decision-relevant information, gross option value is zero.

**Counterexample to naïve universality:** A self-sustaining business has `s=1`, next-cycle survival requires all `1` in sustaining expenditure. A trial costing `0.2` leaves only `0.8`, which cannot keep the current operation admissible. Positive predicted learning value does not make that trial a viable 花 action. Restore viability only by obtaining funds, buffering, partitioning the experiment, or changing the protocol/admissibility—none is free.

## 6. Generative Move GM-012 — invest in *future modes*, not just more of the present mode

- `OLD_FRAME`: development = spend on current throughput or extend existing mode.
- `IMPASSE`: such a system can scale while becoming brittle or locally optimal; cannot explain expenditure on uncertain recombinations, compatibility search and failed experimentation.
- `MOVE`: split **maintenance of incumbent organization** from **costly exploration** and **replication**, under a perspective-relative viability constraint.
- `NEW TYPES`: `Mode`, `Experiment`, `OpportunityCost`, `PartnerCompatibility`, `Recovery`, `TransferContext`.
- `ENABLES`: testable option-value engineering, staged admission of novel modes, comparison of experiment/recovery policies, differentiation of innovation failure vs dissemination failure.
- `RESIDUAL`: evolutionary inevitability (not proved); universal biological comparative advantage; genuine purpose or semantic meaning of novel modes; real-world calibration of risk/benefit.
- `NON-ENTAILMENT`: `花` can cause death, fail to improve mode, or add noisy complexity; `果` can spread an unfit template. Stability or attractive branding ≠ self-sustaining viability.

## 7. Canonical graph edges / backward and forward compatibility

- `REFINES`: `SRC-0323` root–sprout–flower–fruit → `SRC-0106` §11 viability/recovery conditions for **the whole runtime**; not identical types.
- `TRANSLATES (M1)`: 花 ↔ `Gen–Dui` incubation conditions; 果 ↔ `Zhen–Xun` propagation; context-dependent, not mapping each role to one trigram uniquely.
- `DEPENDS_ON`: `K1-GEN-001` perspective/subject; `K1-P8D-001` Kan–Li admission; `K1-GOV-001` may contribute learned partner-dependency costs; `K1-TIME-001` can influence risk allocation by future anticipations.
- `REFINES / BRIDGE OPEN`: `SRC-0279` Generation+Activation distinguishes possible candidate from executed trial; Closure+Selection distinguishes trial from accepted new mode; do **not** identify these five regimes with 根苗花果.
- `UNRESOLVED`: What mathematical/evidential conditions authorize **mode change** `m→m'` rather than mere parameter tuning within `m`? Requires a declared reduction / intervention experiment.

## 8. Minimal experiment / reconstruction tests

1. **Dual-budget test:** Holding capital, current profit and environment fixed, compare an explore-heavy and replicate-heavy policy. Does the Kernel identify why high short-term output could accompany declining long-run adaptability? State assumptions, not a universal ranking.
2. **Perturbation-recovery trap:** Two models have equally large viable sets; one offers `ρ_rec>0` after bounded shocks, the other `ρ_rec=0`. Can the LLM explain why stability/viability membership alone does not settle resilience?
3. **Source fidelity:** Locate exactly where HJ assigns three **distinct** costs to 花 and why 花 is not just a marketing/sales funnel.
4. **Evidence boundary:** Derive the information-value inequality and produce a counterexample in which *net* flower investment is harmful despite its positive gross information value.
5. **Cross-domain operationalization:** Replace firm with an LLM engineering harness. What are observable `s`, `m`, `i`, `p`, trace, qualified flow, violation of Li? What real experiment rather than analogy would support the bridge?

## 9. Proof and provenance ledger

| Claim | Status | Locator |
|---|---|---|
| Root/sprout self-support, flower/fruit future-directed cost | Historical source `M0`, text verified | `SRC-0323` §7.3b/c, ¶1943–1975 |
| Multiple flower costs and compatibility mediation | Historical source `M0`, text verified | `SRC-0323` §7.3c/d ¶1968–1987 |
| Incubation basin and recovery radius | Declared mathematical definitions `M2` | `SRC-0106` `(11.1–11.15)`, PDF pp. 50–53; pages 51–52 visually checked |
| `I_P(h)` alone need not imply robust `ρ_rec>0` | Compiler mathematical caution `M3` via counterexample | Based on `SRC-0106` definitions, **not source theorem** |
| Budgeted investment and decision-value inequality | Compiler model `M2` / conditional lemma `M3` | §4–5 of this Kernel, **not HJ equation** |
| Real ecosystems and Transformer runtime conform to this grammar | **Open `M1` cross-domain hypothesis** | Experimental data / interventions needed |

**Hard stop:** do not turn “花 is important to adaptive evolution” into “all successful species/firms/AGI must spend a fixed percent on experimentation.” Do not turn protocol-relative `Q_min` into a universal numerical threshold.
