# Independent acceptance protocol (public method, no hidden answer key)

## Controlled conditions

Freeze: task statement, input collection, permissions, tools, source retrieval opportunity, maximum time/token budget, number of rounds, model versions, and grading independence. Different agents may choose methods freely but must share the same evidence/acceptance standard. A tool-free agent cannot be required to provide hash checks, code execution, source PDF OCR or experiments it cannot run.

## Metrics (score only on genuinely reviewed cases)

| Dimension | What to check | Typical failure |
| --- | --- | --- |
| Citation fidelity | Supported claim anchored to actually read source span | Invented page, source or quote |
| Fidelity to assertion | Necessity, sufficiency, quantifier, variable meaning preserved | Compiler invents stronger theorem and then refutes it |
| Mathematical / causal scope | Correct countermodel and conditions | Local trial presented as universal theorem |
| Dependency and history | Correct revisions and independence | Duplicate error counted as independent confirmation |
| Residual usefulness | Next test could discriminate alternatives | Vague suggestion without observable criterion |
| Independent reconstruction | New agent can recover decisive reasoning and limits | Recites conclusion but loses assumptions |
| Non-SMFT transfer | Works on engineering/project history as well | SMFT vocabulary overfitted to unrelated documents |
| Efficiency | Meaningful correct output per budget | Large markdown output with little verifiable value |
| Negative findings | Correct refusal, uncertainty, stop | Fabricated success for inaccessible evidence |

## Trial setup

1. Evaluation designer obtains an *unseen* corpus and produces a private ground truth with source coordinates and expert checks where needed.
2. Keep public Skills and teaching cases visible as intended; isolate private gold and grading rubric from evaluated agents.
3. Run identical tasks in randomized order for at least two baseline conditions, matched budget and source access.
4. An independent evaluator reviews artifacts against source, separating `schema valid`, `source faithful`, `mathematically valid`, `scientifically supported`.
5. Report both improvement and regressions with uncertainty, resource usage, failure cases and evaluator limitations.
6. Do not treat a one-off positive example as evidence of cross-model improvement or general scientific discovery.

## Current state

No such independent source-hidden controlled trial has been completed for v0.2.0. A future public report should provide methodology, aggregate results and reproducibility materials without leaking future hidden benchmark items.
