# Public SMFT Kernel learning examples — integration guide

This add-on remedies the missing `90_PROVENANCE` and versioned Kernel examples in the initial RCS 325-source mirror. It is a **reference package**, not another Skill and not a new scientific certification.

## Contents and provenance

All historical data files are copied **byte-for-byte** from the author-supplied `kernelization_v8.6.tar` and are listed in `data/smft/kernels/KERNEL_EXCERPT_MANIFEST_SHA256.csv` with their original TAR member paths and hashes.

- `data/smft/kernels/v8.6-light/` — core theoretical documents, active v8.6 provenance, original source identity table, field notes, selected inherited Atlas/index records.
- `data/smft/kernels/v6.0-provenance-example/` — authentic v6.0 `CURRENT_V6` folder and historical v6.0 evidence records.
- `data/smft/kernels/v4.4-history-excerpt/` — six authentic v4.4-labelled historical audit documents (not the original v4.4 FULL).

## Use with Skills

Use `skills/research-kernel-builder/SKILL.md` to examine the v6-to-v8.6 evidence change, compile selected original papers, or extend an existing research state. Use `skills/research-archaeologist/SKILL.md` to investigate the v4.4/v6.0/v8.6 history, contradictions, and repair paths. Always distinguish source-written claims, compiler-added results, speculative assumptions and scientific observations. Use original `data/smft/src/` for source-attributed checks.

### A practical starter task for any agent

> Read `data/smft/kernels/README.md`. Learn the difference between current theory, source history, and provenance. Compare the preserved v6.0 `CURRENT_V6` README with the v8.6 `CURRENT_V86` README. Select three historical corrections or failure cases and trace them to the original source documents when available. Cite exact paths. Mark any missing ancestor `INSUFFICIENT_EVIDENCE`. Do not use the supplied historical references as a sealed test answer key.

## Repository maintenance

- The original 325 source documents remain under `data/smft/src/` and are already present in the existing mirror. No need to copy them again.
- Existing `RCS/release-assets/original-source-tars/` remains empty until the user adds archives for GitHub Releases.
- Existing `RCS/private-evaluation/` remains local. Do not move PRIVATE rubrics, holdouts, or unreviewed master v8.6 into the Git repo.
- The addon refreshes `MANIFEST_SHA256.md`, the main README, and the SMFT README. If you have edited these three files locally since the original mirror, inspect differences before overwrite.
- This release has **no bundled Python scripts**. All processing scripts used to prepare the zip were internal and not included.

## Scope of checks

This package checks archive extraction, SHA-256 file identity, JSON/CSV readable formats where applicable, expected reference paths, package integrity and manifest consistency. It does **not** conduct a full source-to-Kernel mathematical review or independent source-hidden LLM benchmark.
