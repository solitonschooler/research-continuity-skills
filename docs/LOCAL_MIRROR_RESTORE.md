# Reconstructing the full public-source mirror from multiple ZIP files

**The complete single ZIP compressed to ~292 MB and could not be attached reliably.** The distributed archive set restores the **same full on-disk mirror**.

## Instructions (Windows)

1. Download `RCS-BASE-GITHUB-MIRROR.zip` and **all 8** `RCS-SMFT-SOURCES-NN-of-08.zip` overlays.
2. Extract `RCS-BASE-GITHUB-MIRROR.zip` to the same parent folder you want to use for `RCS/`. To get `D:\RCS\`, extract to `D:\`.
3. Extract **each** sources ZIP to **that same parent folder** (`D:\` in this example). Keep paths and overwrite only if the unzip tool asks about identical empty directories. Do NOT extract into `D:\RCS\`; that would create `D:\RCS\RCS\...`.
4. The resulting Git repository is `D:\RCS\research-continuity-skills\`. Its `data\smft\src\` folder should contain **325** PDF/DOCX/TXT files.
5. Compare files against `data\smft\SOURCES_MANIFEST.csv` (contains original v8.6 stable source IDs and SHA-256). `data\smft\SOURCE_PARTS_INDEX.csv` maps each file to the overlay containing it. The repository `MANIFEST_SHA256.md` includes all complete-mirror files, so it won't match a base-only extraction until overlays are added.
6. Add the original 11 TARs later to `D:\RCS\release-assets\original-source-tars\` if desired. Add private v8.6 master only to `D:\RCS\private-evaluation\`. A **reviewed** public v8.6 TAR can later go in `D:\RCS\release-assets\kernel\`.

Only `RCS/research-continuity-skills/` should become the Git repository. The `RCS/release-assets/` and `RCS/private-evaluation/` sibling folders are not the Git repo.

All files were compared to v8.6 source manifest SHA-256 and byte length during mirror assembly. Matching source bytes do not certify their scientific content. No private benchmark or full Kernel master was included in these packages.
