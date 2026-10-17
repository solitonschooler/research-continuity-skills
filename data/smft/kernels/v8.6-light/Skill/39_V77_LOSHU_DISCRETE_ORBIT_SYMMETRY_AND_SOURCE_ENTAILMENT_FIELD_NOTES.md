# Skill/39 — v7.7 exact LuoShu classification, source audit, and selection impossibility (FIELD NOTES)

**Case:** V77-LOSHU-D4-SELECTOR. SHA-verified source `SRC-0104` PDF physical pp15–17 and `SRC-0107` pp8–10,13; original pages 8–9 visually checked. Related GL75-03/GL76-03 → GL77-01/02/03 → RA-H04. This note is a field note **not** a runnable `SKILL.md`.

## Trigger and actual process
A previous softened claim 'affine LuoShu constraints produce a unique stable square' failed. Re-read the original source and distinguish (i) exact digit permutation, (ii) continuous affine constraints, (iii) D4-orientation and (iv) semantic performance; do not confuse one with another. Derive explicit 2D affine solution family, prove 8 exact D4-orbit points, check all 9! permutations, prove symmetry stabilizer no-go, create a hand-engineered polynomial D4-invariant objective and execute 128 random/5 symmetric initializations with a standard nearest-orbit baseline. Save protocol/hash before run and 133 row-level results.

## Observed and negative findings
- Source p8 statement every repeated assignment has sum below 45 is refuted by all fives. Source p9 Shannon entropy cannot distinguish any permutation of a fixed 1..9 multiset; relaxing repeats makes all-five strictly higher entropy, so entropy cannot be used as proof of LuoShu semantic maximal stability. Preserve source-authored claims and compiler counterarguments separately.
- Formula for every real LuoShu magic grid is L(a,b), and exactly 8 integer digit permutations occur at (±1,±3)/(±3,±1). Up to D4 there is one orbit; not one oriented grid.
- A deterministic *total* D4-equivariant selector from all continuous states to free D4-orbit is impossible from stabilizer mismatch at origin; external orientation/noise/random output can evade assumptions. Never mislabel that necessity as proof of SMFT Observer.
- An engineered D4-invariant polynomial with exact target zero set solves all 128 generic starts but fails all five symmetric states. Standard nearest-of-eight handles 133/133. It is **not evidence** for naturally emergent attractors or a better algorithm. Report evaluation counts and unequal costs explicitly.
- Initial unit test applied CCW rotation (a,b)→(−b,a); verification failed. Correct induced action is (a,b)→(b,−a) for `np.rot90`, and the corrected 31 tests pass. **Repair rule:** group-action operators must be checked numerically against concrete objects before invoking high-level group proofs.

## Reusable Skill operation and future interface
`Original claim → explicit state-domain/premises → algebraic classification → standard symmetry group → no-go conditions → benchmark against trivial exact solver → negative controls → evidence-limited residual`. Require test fixtures at fixed points and symmetry axes; forbid hand-designed energies from being promoted as observed mechanisms. Note `source_review=bounded`, `independent_reconstruction=NOT_RUN`, `natural_semantic_attractor=NOT_RUN`. Maintain historical file hashes; add new versioned notes, never silently replace old notes.

## Generative residual
Test whether additional orientation is an observable protocol variable in a real engineering setting, and whether symmetry quotient improves useful tasks compared with simple exact discrete assignment. Benchmark independent LLM research reconstruction with sealed fresh cases, not self-grading.
