# Public GitHub Publication Checklist

This public-source mirror includes the 325 original SMFT PDF/DOCX/TXT files, but still omits the original TAR duplicates, the v8.6 FULL master, private chats not in the authored source collection, and sealed benchmark material. Review rights and privacy before public commit.

## Rights and privacy

- [ ] Select and add an explicit license for the Skills, schemas, text and authored examples. Review whether separate licenses are needed for optional sample corpora.
- [ ] Confirm rights to any SMFT v4.4/v6.0/v8.6 release specimen; do not assume rights to third-party papers/images just because they were included in research archives.
- [ ] Search for secrets, personal data, private evaluation rubrics, benchmark keys, URLs with tokens and unpublished source excerpts.
- [ ] Check source attribution and copyrighted quotations; synthetic examples are safest for default distribution.

## Installation and behavior

- [ ] Confirm `SKILL.md` frontmatter and matching directory names.
- [ ] Install each Skill **by itself** in at least one actual Agent Skills host; then test both together.
- [ ] Confirm local references and schema load without requiring a repository-level shared folder.
- [ ] Test `SCAN`, `VERIFY_REPAIR`, `DEVELOP`, `STOP`, `INSUFFICIENT_EVIDENCE` and handoff.
- [ ] Test an inaccessible source, malformed citation, adversarial document instructions and unexecuted experiment declaration.

## Evidence and research results

- [ ] Independently review a non-SMFT case; compare against a generic research agent and retrieval baseline with matched budget.
- [ ] Ensure source coverage is never falsely stated as full depth review.
- [ ] Keep public worked examples separate from sealed tests. Publish limitations and negative results.
- [ ] Choose version tag and add a changelog after actual external user feedback.

## Optional future specimen

A curated SMFT v6.0 example may be released *separately* only after rights, size, PII and benchmark-leakage review. Consider a compact sample and optional archive links instead of automatically loading large data. This mirror **does** contain original SMFT source papers; it does **not** contain private evaluation files or a cleared v8.6 Kernel.

## R8 additional acceptance gates

- [ ] If published publicly, select an explicit appropriate LICENSE from the rights holder; no license is chosen in this draft.
- [ ] Try both Skills in each platform claimed supported (installation and resource discovery).
- [ ] Compare the result against a new corpus without the example answer visible, under matched source/time/budget conditions.
- [ ] Review `shared/ACCEPTANCE_GATES.md` and do not claim G2/G3/G4 are satisfied merely because JSON Schema passes.
- [ ] Keep future SMFT real-source example packages opt-in and individually rights/privacy reviewed.

## Source mirror checks

- [x] Extracted 325 authored original files and verified each against the v8.6 source manifest hash and byte size.
- [ ] Confirm research-corpus rights/license and inspect third-party embedded materials before publishing.
- [ ] Add original TARs under local `RCS/release-assets/original-source-tars/` if desired.
- [ ] Produce and review `kernelization_v8.6_PUBLIC.tar` separately; do not upload the private FULL master.
- [ ] Regenerate manifests if any files are changed by Codex.
