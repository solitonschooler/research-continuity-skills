---
artifact_id: SMFT-KERN-K1-GOV-001
kernel_id: K1-GOV-001
version: 0.2.0
snapshot_date: 2026-10-14
status: source-anchored-model-hypothesis
logical_path: 04_MECHANISMS/42_K1_GOV_001_RITUAL_DEPENDENCY_INERTIA.md
language: zh-Hant+en
origin_sources: [SRC-0323]
translation_sources: []
formal_context: [SRC-0106, SRC-0299]
generative_moves: [GM-008]
---

# K1-GOV-001 — 禮樂：從協同表象到 Dependency Inertia / Self-maintaining Institutions

> **Micro-kernel:** 《皇極經濟》把「樂」從可觀察的同步、和諧、共鳴，逆推到 **「依賴的慣性」**：重複互動及共享記憶使群組在撤去一部分明文指令後，仍能維持特定節奏、互動與行為傾向。`禮` 設定可識別的規範/交易接口；`樂` 可由互動中形成，也可能反過來固化、改變或侵蝕 `禮`。這個結構 **可以有益，也可以壓迫、上癮或退化**；persistent coordination ≠ truth / welfare / moral goodness / causal proof of a semantic attractor.

## 1. Why this matters to the entire Kernel graph

One of the 2024 mother-work's key moves is to refuse a purely external-control explanation of organization. Rules can launch a repeated interaction, but its persistence may subsequently depend on a different state carrier: repeated trust, mutual expectation, shared symbolic cues, switching costs, learned co-dependence and tacit expectations. **Appearances of harmony alone do not identify the carrier.**

This is a research **mechanism question**, not a theorem already proved in the early text. `SRC-0323` makes this distinction explicitly:

| Source locator | What the author actually develops | What must not be retroactively imposed |
|---|---|---|
| §5.3e, DOCX paragraphs `1501–1510` | 制度範圍 ↔ 曲成手段 mutually define effective activity; rules may reduce transaction frictions | Source did not specify modern effective-Li operator |
| §5.3f, `1512–1533` | 禮 can produce 協同 and forms of broadly construed 樂; quality requires avoiding addictive entrainment | “Music” is not a universal endorsement of social conformity |
| §5.4, `1538–1549` | 以禮制樂: use rules to induce durable rhythms and self-maintenance; warns of an *autonomous self-continuation monster* | Persistence does not entail morally legitimate governance |
| §5.5a, `1551–1565` | 意念→制度化→協同鞏固 appears as a plausible organization-development sequence | Stages are interpretive/business patterns, not universal law |
| §999c, `2227–2239` | Crucial correction: 協同 is a **surface feature**, while 樂 is proposed to be 「依賴的慣性」 | No original quantitative inertia measure supplied |
| §999d, `2241–2256` | Shared values, recognizable symbols, emotional/behavioral cues, and reciprocal enforcement of ritual | These are mechanisms proposed by the book, not verified neuron-level attractors |

**Origin:** `SRC-0323` §§5.3–5.5, 999. **Mature interface candidate:** `SRC-0106` §5.7–5.12 and §15; `SRC-0299` Trace / Filtration / Revision. No assertion that those late works already prove HJ's dependency-inertia claim.

## 2. Separate four often-confused layers

1. **禮 / explicit institution** `L^F`: formal rule, recognized membership/permission, written schema, declared sanction, process.
2. **Effective admissibility** `L^E`: which transactions/actions are actually recognized and sustained; arises jointly from rules, enforcement, realized adaptive behavior and history (P8D II Kan–Li).
3. **樂 / dependency inertia** `D_t`: hypothesized persistent internal relational state such that past repeated interactions affect future action *even after conditioning on current formal instructions*.
4. **Observable coordination** `C_t`: synchrony, conformity, repeated transaction rhythm, shared choices, compliance. `C_t` is an **effect/measurement candidate**, not definition of `D_t`.

This distinction creates the key causal alternatives:

```text
(1) 禮 L^F → mediated routines → D_t → coordination C_t
(2) D_t → enacted precedent → effective Li L^E → new institutions
(3) external sanctions / monopoly / coercion → C_t (without strong intrinsic D_t)
(4) common external shock → C_t (correlation without mutual dependency)
```

The Kernel must preserve **all four hypotheses** until interventions discriminate them.

## 3. Minimal typed candidate model — COMPILER PROPOSAL, NOT SOURCE EQUATION

For `n` bounded participating units, let:

- `G_t=(V,E_t)`: time-dependent group interaction network.
- `L_t^F ∈ Rule`: declared institutional rules; `L_t^E∈AdmissionGrammar`: effective validity predicate, potentially dynamic.
- `a_i(t)∈A_i`: agent action; `q_ij(t)≥0`: observed *qualified* repeated dependence-producing interaction between units `i,j`, e.g. task flow, credible cue, mutually useful exchange.
- `d_ij(t)≥0`: latent dependency strength; `D_t=[d_ij(t)]`. It is an **operational latent variable hypothesis**, not an intrinsic social/semantic substance.
- `τ_t`: historical trace under declared observational protocol `P`.
- `C_t = Obs_P(a(t),G_t)`: measured surface coordination; `W_t`: possible welfare/health/dissipation outcomes (a separate evaluation, not coordination itself).

A first, deliberately simple **test model** (`M2` proposal):

$$
d_{ij}(t+1)=(1-\lambda_{ij})d_{ij}(t)+\beta_{ij}q_{ij}(t),
\quad 0<\lambda_{ij}\le 1,\quad \beta_{ij}\ge0.
$$

Actions may then depend on memory and effective rules:

$$
\Pr(a_i(t+1)\mid x_t,L_t^E,D_t,\tau_t)
\ne\Pr(a_i(t+1)\mid x_t,L_t^E,\tau_t)
$$

for some properly controlled contexts. **This conditional-dependence statement is an operational diagnostic hypothesis**. It is not by itself a causal identification result; latent confounding, imperfect `τ` and model misspecification can produce it.

A causal version requires selective perturbation of q or interaction/cue structure while holding major alternative channels constant. If repeated interaction is **endogenously generated by dependence**, e.g. `q_{ij}(t)=f_{ij}(D_t,L_t^E,x_t)`, feedback may support multiple persistent regimes or hysteresis. If it is removed and no compensating feedback exists, the simple update above predicts **decay**. Do not say any dependency necessarily survives indefinitely without reinforcement.

**Notation caveat:** `D_t` here is **dependency matrix**; **do not confuse** with Declaration `D` of World-Formation Formal Core, or with observer protocol `Δ_P`. Keep the full symbol name `Dep_t` where crossing namespaces.

## 4. Key Generative Move (GM-008)

`Old frame`: institution is imposed; observed synchrony = coordination = essence of 樂.

`Impasse`: observed synchrony doesn't explain how group organization persists, or how a group can maintain an undesirable rule after formal inducements change.

`Move`: treat persistence-generating **dependency inertia** as a distinct latent structure; recognize formal rules and realized relationships as mutually modifying.

`New possible objects`: interdependence graph, history-dependent action kernel, learned cue→response mapping, institutional hysteresis, cost of reconfiguration, endogenous effective admissibility, and welfare-separated sustainability criteria.

`Enables`: organizations, firms, communities, agent collectives and possibly Transformer memory/attention architectures can be compared using **intervention-resolved persistence**, not a superficial synchrony metric. The Transformer parallel is only a *candidate engineering analogy* and needs circuit evidence.

`Residual`: HJ's moral cultivation and `樂盈而反` (satiation/moderation) remain partly normative; formal `Dep_t` cannot by itself represent beneficial restraint or social justice. The `禮↔樂` analogy does not imply all communities share identical institutional dynamics.

## 5. Testable separation: 「樂」 vs mere coordination

**Protocol setup:** compare several groups under matched tasks, baseline incentives, resource access and external shocks; declare observation horizon and permitted rule/cue interventions. Use a factorized design where possible:

| Manipulation | Expected discriminating observation | Competing explanation |
|---|---|---|
| Suppress shared cue/ritual while keeping incentive and legal rules | Persistent latent `Dep` may sustain choices despite missing immediate signal; cue-driven coordination may vanish | Unseen continuing social sanction |
| Alter formal policy while preserving trained interaction network | Effective practices may lag/oppose policy change; locate hysteresis and adjustment costs | Delayed enforcement only |
| Rewire interaction ties while holding announcements/payoffs | If dependency network matters, coordinated behavior changes in tie-specific way | Network simply transmits information |
| Introduce alternative providers/partners and exit option | High dependence may retain incumbent participation beyond immediate measured utility | Contract lock-in, monopolistic constraint |
| Compare welfare/innovation under equally high synchrony | High `C_t` may correspond either to productive coordination or coercive ossification | Need independent welfare measures, not popularity proxy |

**Negative control:** externally synchronised agents obey the same clock but have no reciprocal interactions. Their `C_t` can be high, while little reason exists to infer learned interdependency. **Positive control model:** repeated pair-specific cooperative exchanges yield a history-dependent choice bias under matched immediate rewards. Both need quantitative tests.

## 6. Relation to Kan–Li, Ledger, SMFT and Framing

- `K1-P8D-001`: 礼 may instantiate part of `Li^F`; actual transactions co-shape `Li^E` through adaptive realization. **Do not identify 樂 with Li, Kan or a distinct fifth dyad.** `Dep` may be one latent mediator input to Kan, an input to effective Li, or a source of persistent emergent constraints; require a domain-specific implementation.
- `K1-GEN-001`: Dependence appears only under a declared boundary/interaction observation. Cross-scale comparisons require explicit map and invariants.
- `SRC-0299`: Trace can record commitments; repeated records can become relevant to future decisions. But **a database trace is not automatically shared dependence**, and dependence need not have a single digital ledger.
- Later Semantic Attractor / SMFT: it is attractive to call a stable dependency graph an “attractor”. This is only justified in the **dynamical systems sense** if invariant/inward-stable basins or other attractor criteria are specified for a stated model. Real Transformer *semantic object* identification is a separate empirical burden (`SRC-0261` evidence guard in K0).
- 道德仁霸: forms of creating/maintaining order can coexist with or manipulate dependency inertia. Do not equate `王仁=Li` or `帝德=Dep` globally; these labels represent a broader governance typology.

## 7. Failure modes / proof obligations

- `BF-GOV-01` **Synchrony fallacy:** `C_t` high but pair-dependence negligible after matching common signal and incentives.
- `BF-GOV-02` **Lock-in fallacy:** persistence is contractual switching cost, threat or monopoly, not internal learned relational dependence; both may coexist but must be distinguished.
- `BF-GOV-03` **Welfare fallacy:** high persistence or efficiency of coordination is treated as morally desirable. HJ explicitly warns of cult-like and self-perpetuating harmful institutions.
- `BF-GOV-04` **Math overclaim:** simple persistence equation is presented as a discovered empirical law or as 2024 equation. It is a **compiler-generated model for falsification**.
- `BF-GOV-05` **False permanence:** inferred no decay merely from a temporary plateau; test several time constants and remove reinforcement channels.

**Empirical acceptance criterion (proposed):** adding a history-dependent `Dep` mechanism must improve **held-out intervention prediction** beyond rival current-incentive/sanction/common-shock models, not just fit a descriptive story. Check repeated trials, uncertainty and unit-/domain-specific validity.

## 8. Reconstruction tests

1. Explain HJ's §999 distinction between `協同` (appearance) and `依賴的慣性` (proposed generative carrier). Construct a case with synchrony but no relational inertia.
2. A formal platform rule changes but users persist in a shared habit. Distinguish trace, effective Li, dependency inertia, switching costs and coercion. Propose **one intervention** that discriminates two of these causes.
3. Why can `以禮制樂` and `以樂制禮` both occur? What prevents this from being equivalent to a scalar feedback loop with guaranteed positive welfare?
4. What would refute `Dep` as an independently useful state variable after matching history, current incentives and rules?

## 9. Evidence ledger and provenance

- **Historical source** `SRC-0323`, cited paragraph locators under §1; strongest explicit source basis = §999c/§999d; 2024 DOCX internal creation metadata available via manifest. No claim of source equations.
- **Late formal context** `SRC-0106` §§5,15 and `SRC-0299` §§5–10: distinct gate, valid-transition, commitment, trace semantics. Correspondence `M1/M2`, not formal equivalence.
- **Compiler additions** `Dep_t` update rule, causal diagrams, controls and hypotheses (model `M2`, unvalidated). Interventions would supply `M4/M5` only **after** execution with results, which this release does not claim.
- **Unabsorbed**: cultivation / moderation / normative value of 樂; specifically HJ distinguishes beneficial coordination from harmful addiction/coercive lock-in.

**Interfaces:** `K1-GEN-001` declaration, `K1-P8D-001` Li / Kan, `GM-008`, downstream social/AI test frameworks. Do not fold this Kernel into a “generic rhythm” or “music signal” simplification.
