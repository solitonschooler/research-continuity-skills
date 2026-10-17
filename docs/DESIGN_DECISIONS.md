# Architecture Decisions — R1 to R7 synthesis

1. **Two task-based entrances, not source-based entrances.** Documents and dialogues often contain both formal results and historical episodes; Builder maintains a reconstructable state, Archaeologist reconstructs contested history.
2. **Shared declarative evidence contract.** Rules for trustworthy attribution are portable; methods of extraction, mathematics and code execution are the host agent's responsibility. No official Python/CLI is bundled.
3. **Optional research advancement, not only summaries.** SMFT v4.4–v8.6 field notes report consolidation, verification, counterexamples, conditional repair, version-history correction, synthetic experiments, negative controls, meta-research improvement and stop rules. Provide these as opt-in activities; do not promise novelty or truth.
4. **Autonomous, bounded iterations.** The user may stop at any time. A round must preserve its status, change receipt and next entry; do not make continuous improvement mandatory.
5. **Historical and rational reconstruction are different.** A better proof invented later should never be reported as what earlier researchers actually thought.
6. **Public use must be testable.** Form/schema validation, source fidelity, logical correctness, cross-session reconstruction and external scientific support are separate gates. No public worked case may be presented as sealed evidence.
7. **Design full first, distill later.** A future extremely short Skill variant should only follow comparisons showing which constraints can safely be omitted for newer LLMs.
8. **SMFT is optional specimen and possible conceptual lens, not the universal ontology.** Future SMFT v6.0/v8.6 case releases need rights/privacy review; may be valuable for advanced teaching but risk overfitting and evaluation contamination.
9. **No license imposed on user's IP.** The author/rights holder must decide before public release. The draft is distributed for review without assuming MIT/CC-BY or authorization for external source archives.
10. **Competitive modesty.** Provenance and longitudinal compilation overlap with existing research/agent tools; public claims should focus on demonstrable value under contested and evolving evidence.

## Key design risks to revisit

- A complete formal schema may be too demanding for 10-file tasks. Use the same logical distinctions in a short narrative when appropriate; reserve JSON for durable handoffs.
- Standalone packaging duplicates the shared contract and schema; check all copies on each release.
- Untrusted instructions in retrieved sources should never override the Skill's provenance/security boundaries.
- Repaired research outputs may be *new inventions* by the agent; label them and test independently rather than attributing them to historical source authors.
- A failed origin/emergence test can still yield valuable conditional mathematics, but cannot establish the sought natural mechanism.

## R8 — editorial acceptance hardening

A v0.1.0 JSON Schema-only pass missed five deliberately invalid records; three are now blocked by local schema conditionals and the remainder require explicitly documented cross-record acceptance checks. Public synthetic challenge cases illustrate attribution and historical-mechanism errors, but the results are **not** a sealed independent benchmark. This improves quality controls without imposing a fixed algorithm on the host LLM.
