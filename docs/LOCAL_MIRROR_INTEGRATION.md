# Local mirror integration notes

This is an **additive packaging of the v0.2.0 experimental Skill draft**, not a newly proven release.

The two Skills' logic, schema, and worked teaching examples remain unchanged from v0.2.0. The mirror supplements them with 325 extracted research documents, a corpus identity manifest, and a source-archive index. No Python scripts are bundled in the repository.

After extraction, publish **only** `RCS/research-continuity-skills/` to GitHub. The sibling `RCS/release-assets/` holds user-added release asset TARs; `RCS/private-evaluation/` is strictly local.

What is missing:
- explicit LICENSE for the Skills and rights decision for source corpus;
- `kernelization_v8.6_PUBLIC.tar` (not produced in this package);
- original 11 TARs (you will add the originals locally);
- private master v8.6 (user will keep locally);
- independently executed installation and efficacy tests.

Source IDs were taken unchanged from `kernelization/90_PROVENANCE/90_SOURCE_MANIFEST.csv` in the supplied v8.6 master. All original source files matched SHA-256 and bytes at assembly time.

The original historical validation results in docs describe the Skill draft, not the full publication audit of the public source corpus.
