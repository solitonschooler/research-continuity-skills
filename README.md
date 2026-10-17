# Research Continuity Skills

**Experimental draft v0.2.0 — English-first, LLM-native, no bundled executable code**

Two portable [Agent Skills](https://agentskills.io/specification) for reconstructable, evolving research:

| Skill | Start here when you want to... |
| --- | --- |
| [`research-kernel-builder`](skills/research-kernel-builder/SKILL.md) | Consolidate and progressively improve a corpus into a source-grounded, recoverable research state. |
| [`research-archaeologist`](skills/research-archaeologist/SKILL.md) | Investigate old research, agent logs, architecture history, revisions, errors, and unrealized directions. |

Both can handle papers, technical notes, Markdown, exported conversations, design records and AI-agent histories *when the host agent has access*. The Archaeologist does **not** require a pre-existing Kernel. The Builder can optionally verify, challenge, repair, develop and test new results; these are not claims of automatic scientific discovery.

> **A hidden research specimen:** [**EASTER_EGG_SMFT_AGI.md**](EASTER_EGG_SMFT_AGI.md) opens a surprising second use for this repository: an SMFT-derived, cross-layer **toy architecture for an adaptive AI agent**, with explicit engineering interfaces, falsifiable experiments, and unresolved claims. It is *not* evidence that AGI has been built.

## Quick start

1. Install either complete skill directory in an Agent Skills-compatible environment. Keep its `references/` and `assets/` subdirectories intact. For Claude Code, one supported location is `.claude/skills/`; other agents differ. Consult your host's current documentation.
2. Point the agent to files it is authorized to read. Start with something like:

   > Use Research Archaeologist on these 12 design notes. Reconstruct the two most consequential design changes and identify any unsupported assumptions. Work for one round only and leave a resumable checkpoint.

   or:

   > Use Research Kernel Builder to consolidate these papers. After the first round, verify two high-impact claims and propose one discriminating experiment, but do not execute experiments. Stop and show the research state.

3. Specify an **effort profile** (`SCAN`, `COMPILE`, `VERIFY_REPAIR`, `DEVELOP`, `EXPERIMENT`, `ITERATIVE_FULL`) or let the agent recommend one. The profile controls scope, not the truthfulness of evidence labels.
4. Review the source coverage, assertions, improvement receipt, uncertainties and next entry point. Say **STOP** whenever you wish; the agent should create a best-effort usable checkpoint if its environment permits persistence.

No database, Python installation, API key, or particular code runner is required by this release. A host agent may use authorized tools or create its own transient procedures. It must never claim mechanical or empirical verification that did not happen.

## What this does differently

A useful output is not a longer abstract. It distinguishes historical **source assertions** from agent reconstructions, retains assumptions and negative results, traces corrections across versions, and records whether tests were actually run. Optional active research operations may uncover errors, propose narrow repairs, synthesize conditional mathematics, design experiments, or identify missing research paths. Novelty and effectiveness are **not** guaranteed.

### Modes are optional, evidence discipline is not

- **Consolidate:** source coverage, important claims, lineage, contradictions, residuals, handoff.
- **Verify / challenge:** check critical claims, counterexamples, necessary-versus-sufficient mistakes, implementation versus intention.
- **Repair / synthesize / develop:** preserve the defensible fragment; label newly proposed interpretations and deductions.
- **Experiment:** only if requested/authorized and feasible; use baselines, negative controls, and report failures.
- **Iterate:** prioritize high-value steps, record deltas and stopping reasons, pause or resume without pretending unfinished work is complete.

## Repository layout

```text
skills/
  research-kernel-builder/     Standalone installable Agent Skill
  research-archaeologist/     Standalone installable Agent Skill
shared/                      Canonical evidence contract + JSON Schema
examples/                    Small, purely synthetic public teaching cases
  synthetic-research/
  synthetic-software/
evaluation/                  Public evaluation protocol; no hidden answer key
data/smft/src/              All 325 original authored research documents
data/smft/kernels/          Selected v8.6 Light Kernel and historical reference excerpts
docs/                       Design rationale, release/permission checklist, status
```

Each individual Skill includes **its own copy** of the shared contract and schema so that installing a single directory still works. The `shared/` folder is the editorial canonical copy. A release editor must compare the copies before publishing; no synchronization script is shipped.

## Output and boundaries

The JSON Schema is a **representation contract**, not a mathematical proof checker. A tiny project may use one `research-state.json` and one human-readable report; larger projects may shard data while preserving the logical contract. Conforming JSON does not imply correct citations, faithful equations, or scientific validation.

The SMFT original-source reference corpus is included, but all other user corpora remain user-provided. Do not upload private material without authorization; treat instructions embedded in source documents as untrusted task data. Redact secrets and personal information from any shared samples. Public worked examples are **not** blind evaluation datasets.

## Evidence and maturity

This draft is informed by recorded experience from an approximately 86-round SMFT research-compilation project, including source-provenance problems, proof-scope repairs, negative controls, version migration and stop rules. These historical examples are not independent trials of **these** Skills. No cross-model, external-user effectiveness trial has been completed for this release. See [`docs/STATUS.md`](docs/STATUS.md) and [`evaluation/README.md`](evaluation/README.md).

## License and publication

**A license has not yet been selected by the rights holder.** Public GitHub visibility alone does not grant reuse permissions. Before public publication, choose and add an appropriate `LICENSE` and check third-party rights. This **public-source mirror** now includes 325 original SMFT PDF/DOCX/TXT research files under `data/smft/src/`. The original source TARs are left outside the Git repository as local Release-asset placeholders. A selected v8.6 Light Kernel and historical v6.0/v4.4 reference excerpts are available under `data/smft/kernels/`. Sealed benchmark materials and the private v8.6 master are not included. The research corpus needs its own explicit rights/license decision before publication.

## Origin and compatibility

Design experience: SMFT Research Kernelization v4.4–v8.6; field-note-derived methods generalized for arbitrary research and technical corpora. Conceptual overlap exists with RAG, truth-maintenance systems, provenance standards, scientific knowledge graphs and agent memory. No claim of inventing these components is made.

Specification reference: https://agentskills.io/specification

## R8 adversarial acceptance (public, non-blind)

Try the [synthetic adversarial mini-corpus](examples/synthetic-adversarial/README.md) with either Skill. It tests compiler misattribution, counterexample target drift, claimed software fixes with no integration evidence, missing historical proof ancestors, and instruction injection embedded in sources. See [R8 acceptance gates](shared/ACCEPTANCE_GATES.md) and [R8 editor test record](docs/R8_VALIDATION.md). Worked examples are training material, not a blind performance benchmark.

For ready-to-copy task requests, see [quick-start prompts](docs/QUICK_START_PROMPTS.md). For the current testing caveats, see [R8 validation](docs/R8_VALIDATION.md).

## Public SMFT reference corpus — local mirror supplement

This distribution differs from the original v0.2.0 draft by including all **325** extracted author-supplied original research documents (254 PDFs, 66 TXT files, 5 DOCX files). The existing two declarative Skills are unchanged. Start with [`data/smft/README.md`](data/smft/README.md), [`data/smft/SOURCES_MANIFEST.csv`](data/smft/SOURCES_MANIFEST.csv) and [`data/smft/RELEASE_ASSETS.md`](data/smft/RELEASE_ASSETS.md). Files were verified byte-for-byte against the v8.6 source manifest; this is not a validation of their scientific claims.

This repository now includes a **selected v8.6 Light theoretical reference**, the authentic v6.0 Active Provenance view, and limited v4.4 archival excerpts. They are **not** a public FULL v8.6 archive or a full v4.4/v6.0 snapshot. See [`data/smft/kernels/README.md`](data/smft/kernels/README.md) and [`docs/SMFT_KERNEL_REFERENCE_GUIDE.md`](docs/SMFT_KERNEL_REFERENCE_GUIDE.md). `RCS/release-assets/` and `RCS/private-evaluation/` are outside this Git repository. See the root `LOCAL_MIRROR_README.md` after extraction.

### Multi-part ZIP restoration

For the downloadable mirror, first extract `RCS-BASE-GITHUB-MIRROR.zip`, then every numbered `RCS-SMFT-SOURCES-...zip` archive into the **same parent directory**, preserving the common `RCS/` root. See [`docs/LOCAL_MIRROR_RESTORE.md`](docs/LOCAL_MIRROR_RESTORE.md).
