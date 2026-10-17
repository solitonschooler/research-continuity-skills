# External assets for GitHub Releases

This mirror intentionally leaves two folders outside the tracked repository for future *GitHub Release* uploads:

- `RCS/release-assets/original-source-tars/`: add the 11 original, unchanged `.tar` archives. Compare their SHA-256 values with `SOURCE_ARCHIVE_INDEX.csv`.
- `RCS/release-assets/kernel/`: add a separately reviewed `kernelization_v8.6_PUBLIC.tar` if and when produced. **Do not simply rename the original v8.6 FULL**; the master may contain private scoring materials and holdout answers.

The Git repository itself already contains the 325 extracted sources. GitHub Releases need not duplicate them, but the original TAR archives are useful for exact archival provenance.

Any `v8.6-light` compiled learning package also needs its own provenance, publication review, and truthful version labelling.
