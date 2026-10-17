# Evaluation: engineering acceptance versus research effectiveness

**Not an independent empirical validation.** This folder explains how to evaluate the Skills. No secret answer key, hidden items, copyrighted test sources, or external evaluation results are included.

## Layer 1 — engineering / contract acceptance

- The two `SKILL.md` files have valid frontmatter with names matching directories and useful trigger descriptions.
- Each Skill is standalone-installable with local references and the same schema version.
- Schema files are syntactically valid JSON Schema Draft 2020-12.
- Worked fixture JSON validates structurally; source reference IDs, receipt target IDs and lifecycle changes are checked separately.
- User can request a bounded scan, advanced mathematical repair, a stop, and a resumable handoff.
- A missing source, unexecuted test, unsupported citation and unverifiable cause are **not reported as verified**.

Note: this GitHub ZIP has no validation executable; these checks may be performed by a release editor or an equipped agent using its own tools. Document what actually ran.

## Layer 2 — source-level and mathematical evaluation

Provide unfamiliar corpora with hidden, independently adjudicated source-grounded questions. Measure citation fidelity, source attribution, preserved assumptions, correct proof/counterexample targets, classification of unsupported claims, historical vs rational reconstruction, and false accusation rate. Record human adjudicator disagreement.

## Layer 3 — utility and generalization

Compare under matched model, source availability, budget, and token/tool constraints:

A. General-purpose agent with source access and ordinary retrieval.  
B. Same agent with `CONSOLIDATE` only.  
C. Same agent with optional `VERIFY_REPAIR` + `DEVELOP`.  
D. Where useful, existing user-maintained research index or RAG pipeline.

Use **non-SMFT corpora** as well as SMFT-inspired data. Evaluate new-session handoff, ability to discover valid repair opportunities, cost, latency, and sensitivity to context. Cross-model trials are valuable but not a substitute for sealed evaluation.

## Benchmark contamination policy

- Public examples teach behavior; they must not be passed off as independent/held-out results.
- Private gold answers and hidden rubric belong outside the public repository and away from tested agents.
- Agents asked to evaluate must not receive answer keys in linked docs, tools or previous-context memory.
- Track which model, version, prompts, files, tools, budget and public examples were visible.
- Reuse of known benchmark examples requires disclosure; an independent unfamiliar corpus is required to claim generalization.

## Claims permitted at v0.2.0

Permitted: two Skills and JSON contract exist; public worked examples illustrate intended behavior; chosen static tests passed *if the actual release validation record confirms this*.  
Not permitted: "proven superior to RAG", "automatically invents correct science", "verified on 86 independent experiments", "universally portable", or "independently validated".

See [R8 public adversarial cases](R8_ADVERSARIAL_CASES.md) and [R8 test policy](R8_TEST_POLICY.md). These are **public examples**, not sealed evaluation items.
