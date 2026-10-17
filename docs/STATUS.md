# v0.2.0 Draft Status / Known Limits

## Built

- Two English-first, independently installable Agent Skills with optional research-advancement behaviors.
- Shared evidence contract; duplicate packaged contract/schema per Skill for standalone installation.
- Typed JSON Schema for source identity, claims, relations, residuals, verification receipts, iteration deltas and resumption state.
- Purely synthetic teaching cases and public evaluation methodology.

## Validation distinctions

- **Structural checks:** can be performed by the release editor; see `RELEASE_VALIDATION.md` for the actual recorded checks after packaging.
- **Historical/semantic review:** design was informed by selected SMFT v8.6 field notes; this is not an exhaustive re-audit of 86 turn transcripts or 325 source documents.
- **Mathematical review:** synthetic quadratic worked example is elementary and can be checked explicitly; no external mathematician approval has been obtained.
- **Independent end-user effectiveness:** NOT RUN.
- **Cross-model blind reconstruction:** NOT RUN.
- **Public SMFT source mirror:** 325 original research documents are now included by the author's request, with SHA-256/byte verification. A separate rights/privacy content review and an explicit license remain pending; the public v8.6 Kernel and sealed evaluations are not bundled.

## Known limitations

- Not a complete research compiler or truth-validation algorithm; relies on agent capabilities, access, and user oversight.
- Correct JSON does not imply correct references or valid results; plain JSON Schema cannot generally enforce cross-record ID existence/uniqueness without extra checks.
- No executable code or package manager; installation conventions differ across platforms.
- Reports cannot guarantee recoverability after abrupt failure without an actually saved checkpoint.
- Agent creativity and the optional SMFT mathematical lens have not been shown to improve scientific validity in controlled studies.
- The schema's canonical `$id` uses an explicit non-resolving `example.invalid` placeholder. Replace only when a stable official project domain is chosen.

This is a **GitHub uploadable experimental draft**, not a certified production research instrument.

## R8 validation delta

The public adversarial mini-corpus and tighter schema are teaching and editorial quality-control assets, not an independent benchmark. See `R8_VALIDATION.md`; independent agent usage, cross-model evaluation, blind source reconstruction and host installation are not yet performed.

## Local mirror integration

The 325-file authored SMFT corpus is a publication supplement to v0.2.0 and does not constitute independent validation of the Skills or theory. The public v8.6 Kernel is pending.
