# R8 — Editor validation and limitations (2026-10-17)

**Status:** Editorial schema/fixture tests executed; not independent LLM effectiveness testing. No Python or executable validator is included in the release. A transient editor-side test tool was used, then excluded from distribution.

## Findings carried forward from R7

The v0.1.0 schema mistakenly accepted five defective records: dangling source reference, duplicate source ID, `NOT_PERFORMED`+`PASSED` verification, claim marked checkpoint saved without location, and source-authored claim with no anchor. The issue is not proof of a bad source; it is an inadequate structural gate.

## v0.2.0 validation results actually executed

| Check | Result | Scope / limitation |
| --- | --- | --- |
| JSON Schema Draft 2020-12 validity | PASS | Schema syntax only |
| Existing synthetic research state | PASS | Updated `contract_version` to 0.2.0 |
| New eight-source adversarial state | PASS | Editorially authored, not independently reconstructed |
| `NOT_PERFORMED`+`PASSED` rejected by schema | PASS | Conditional schema check |
| Source-authored assertion without source anchor rejected | PASS | Conditional schema check |
| Claimed saved checkpoint lacking location rejected | PASS | Presence of location, not existence of file |
| Dangling source, duplicate ID, dangling relation, dangling round receipt, nonexistent checkpoint file | DETECTED IN EDITOR AUDIT | **Not** caught by JSON Schema; requires supplemental cross-record checks and actual file access |
| Both Skill frontmatters and local resources | PASS | YAML syntax and file presence, not platform installation |
| Three schema copies identical | PASS | Editorial byte comparison |
| Eight fictional source SHA-256 hashes | PASS | Identity only; no external source validation |
| Directed labelled-graph counterexample | PASS | The stated attribute-preserving bijection does not preserve an edge; no assertion that unlabelled graphs are non-isomorphic |
| Original v8.6 source audit across all papers | NOT RUN | R8 is a GitHub Skill engineering round |
| Independent fresh agent run | NOT RUN | The editorial worked response is publicly visible and not a blind trial |
| Installation on Claude Code / Codex / Gemini etc. | NOT RUN | Must be tried in real host environments |
| Independent human mathematical review | NOT RUN | Limited to editor checks of fictional example |
| Rights-holder selection of public license | PENDING | Do not imply unrestricted reuse |

Machine-readable editor-side check outcomes are saved in [`R8_EDITOR_TEST_RESULTS.json`](R8_EDITOR_TEST_RESULTS.json). It is a release record, **not** benchmark evidence.

## Important limitations of a declarative, no-code distribution

- JSON Schema cannot normally check global ID uniqueness across arrays, document existence, assertion truth, or causal claims.
- An unequipped agent can report a good-faith review but must not manufacture a mechanical PASS.
- `SOURCE_AUTHOR` with a cited locator does not guarantee a faithful quote: G3 still requires reading the exact passage.
- A publicly worked synthetic example is useful for instruction and regression, but unsuitable as sealed, independent test data.
- A single self-authored editorial example cannot measure cross-model improvements over standard retrieval, prompting, or RAG.

## Next release gate

At least one genuinely unfamiliar user/agent should run both Skills on a **different** authorized corpus with no access to private gold. Compare to the same agent's generic research workflow under matched source/budget conditions. Record where outcomes improve *and* regress, then decide whether to trim or expand instructions.
