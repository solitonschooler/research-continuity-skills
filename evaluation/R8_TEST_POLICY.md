# R8 test protocol — separating what was and was not verified

## A. Release-editor checks (can be performed locally)

- Parse both Skill frontmatters; verify expected names and local reference paths.
- Validate all shipped schema copies as JSON Schema Draft 2020-12 and compare their bytes.
- Validate synthetic state examples.
- Inject intentionally malformed state records and verify that local conditional errors fail schema validation.
- Test cross-record integrity **separately**; deliberately dangling links and duplicate IDs must be detected by the validator/reviewer, not falsely attributed to JSON Schema.
- Check ZIP membership, no executable code, and no proprietary or original SMFT corpus bundled.

## B. Instruction-following rehearsal (not independent validation)

Use the public synthetic-adversarial corpus. Check source-fidelity, false-fix attribution, missing ancestors, embedded-instruction resistance, residuals, and whether STOP causes an honest checkpoint. A worked answer visible to an agent makes the trial **training/public rehearsal**, not blind testing.

## C. Independent cross-agent trial (NOT RUN at R8)

1. Recruit an agent/session that has not seen fixture answers; provide a different, unfamiliar corpus.
2. Pre-register evaluation questions, permissions, source access, budgets and scoring criteria. Keep the gold answers and evaluator notes **private and isolated**.
3. Compare general retrieval/summarization, each Skill with core mode, and optional advancement mode, with comparable resources.
4. Score historical source fidelity, mathematical scope, valid repair, fake-citation rate, negative findings, correct stop, and resumed research quality; report costs and failures.
5. Human subject/domain review may be necessary to judge disputed claims; two LLMs agreeing is not a proof.

R8 documents product design and editorial testing, not an independent effect-size estimate or evidence of model-level scientific breakthroughs.
