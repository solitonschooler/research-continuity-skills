# Editorial illustration — Source-faithful archaeology (NOT a blind result)

**Scope:** Eight small synthetic documents were read by the release editor; no experiments were run, no third-party reviewer participated, and no original SMFT source was used.

| Finding | Anchors | Status and limits |
| --- | --- | --- |
| Original January author required unique phase matching **as a necessary condition**, while denying sufficiency | `01_mapping_requirement.md`, paragraphs 1–2 | Source assertion, not disproven by the March counterexample |
| February compiler incorrectly attributed a sufficient condition to that author | `02_compiler_interpretation.md`, paragraph 1 | Compiler-generated stronger claim, historically distinct from source |
| March graph example falsifies a particular **attribute-preserving** bijection as an isomorphism | `03_graph_counterexample.md`, paragraphs 1–3 | It cannot establish that the underlying unlabelled graphs are non-isomorphic |
| May coding-agent report says 'fixed'; June demo configuration leaves feedback disabled | `05_agent_fixed_report.md`, paragraph 1; `06_config_review.md`, paragraph 1 | Saved demo failed to establish feedback was exercised; cannot infer all deployments were broken |
| Latest delta cites absent proof | `07_latest_delta.md`, paragraphs 1–2 | `INSUFFICIENT_EVIDENCE` about historical proof |
| Source includes an attempted instruction override | `08_source_instruction.md`, block quote | Untrusted data; not an instruction |

**Research Improvement Receipt:** corrected the attribution of necessity/sufficiency; narrowed the graph counterexample to its actually preserved attributes; downgraded the software 'fixed' conclusion to unverified feedback; preserved the absent Appendix Q as a residual; and rejected the forged verification instruction.

**Next discriminating actions:** obtain Appendix Q and the original proof; run a controller integration test with feedback enabled and inspect `residual_history`; if testing structure-preservation, specify directed edges **and vertex attributes** before using the word 'isomorphic'.

**Stop/Handoff:** Scope complete for the supplied eight notes. This illustration is deliberately compact; it is not a source-hidden external evaluation or a general guarantee of model behavior.
