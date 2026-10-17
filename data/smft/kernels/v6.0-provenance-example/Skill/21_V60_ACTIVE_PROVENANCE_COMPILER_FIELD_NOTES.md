# v6.0 Field Notes — Active Provenance materialization (NOT runnable GitHub Skill)

## Real problems encountered

1. **The newest file in one family is often only a delta.** GL59 contained no GL50–GL58 proofs, so treating it as the cumulative register silently loses earlier mathematical dependencies. Compile the list of authoritative episodes, track a per-file SHA, and explicitly mark missing family versions (there is no GL53 source register).
2. **Real CSV schemas drift.** `CROSS_FAMILY_DEPENDENCY_v5.4..v5.9.csv` use SIX distinct schema shapes: `from`/`to`, `from_node`/`to_node`, `dependency_node`/`atlas_result`, `parent_node`/`target_node`, and two different typed-condition representations. The first attempt to index assuming `from_node` failed on v5.4. Recover using a schema map; preserve original row, edge type, source and forbidden inference. Never construct a 'DERIVES' relation merely by transitivity.
3. **A current maturity row marked INHERITED is not a downgrade.** v5.9 labels v5.8 theorem components as `INHERITED_NO_V59_PRIMARY_READ`. A naive current view would discard v5.8's four scoped certifications. Merge previous version and new explicit scope, and label what is inherited versus actually reread.
4. **Source-depth signals are heterogeneous.** Hash/pass/read scope fields changed repeatedly between v4.5 and v5.9 (`hash_match`, `sha256_match`, `hash_verified`, various read scope fields); simple one-schema collection accidentally counts just 9 later reread sources. Schema-aware collection finds more records, but these remain bounded *reported* reviews; all original 325 raw files were NOT rehashed or reread in v6.0.
5. **Archival CSVs are stale by design, not inaccurate simply because of age.** The latest 619-edge Theory Lineage and 216-entry Claim Gap are from v3.7. Materialize as inherited scope, not falsely 'v6.0 reviewed'. Historical W/PF navigation is not proof equivalence.
6. **Two deployment layers are not interchangeable.** The runtime 14-file Knowledge pack omits complete GL proof texts. The current evidence overlay helps independent rederivation but is NOT proof of minimal semantic sufficiency; old archive includes private benchmark answers and must not be supplied to blind participants.
7. **Raw package accumulates empty/legacy artifacts.** Keep original full archive byte paths for history/overlay accuracy; omit noisy zero-byte and test-cache files from *participant-facing* runtime/active views. Archive CRC does not validate the semantics of those artifacts.

## Reusable validation pattern

Check 60 exact RA IDs, 98 unique GL/L audit headings and matching full text, 325 source identities and first-pass status, 400 historical W IDs/W024 unresolved, 83 source-typed late edges, unchanged 14 official slots and 40–44 protection, previous Skill hashes, and successful v5.9+INCREMENTAL byte overlay. Add negative controls for missing proof material, mismatched current grade, wrong edge schema, leaked grader files, or stale active-version pointers. Independent LLM answer count remains zero.

The above are **observed repository/compilation facts**, not a completed reusable Skill or scientific claim.
