# R8 — Design checkpoint and next-round handoff

**Current engineering package:** v0.2.0-draft, English, declarative Agent Skills, no bundled Python, no original SMFT corpus.

## Retained decisions

- Two independently installable entrances: `research-kernel-builder` and `research-archaeologist`.
- Shared evidence contract (copied into each Skill for standalone installation).
- Optional verification, repair, development and experimental advancement, not forced into simple scans.
- Stop-anytime, bounded rounds, truthful checkpoint claims, and original-versus-new reasoning distinction.
- Public fictional examples teach; no public private-rubric or held-out answer key.
- SMFT v6.0 curated sample remains a *candidate future optional release* after rights/data audit; **not contained here**.

## Changes this round

- Found five v0.1.0 schema acceptance defects.
- Schema v0.2.0 now rejects three with conditional validation.
- Two classes of failure remain outside schema and are handled by an explicit G2 cross-record gate: duplicated/dangling IDs and real-world evidence existence.
- Added eight-item adversarial corpus and editor-authored findings; preserved the warning that such an example does not count as independent testing.

## Pending (do not imply completed)

1. Cross-platform actual install/use tests by independent agents.
2. Unseen non-SMFT corpus and private evaluator answer key kept *outside public repository*.
3. Matched-budget generic-agent / Skill / optional-advancement comparison.
4. User decision on license and future public SMFT specimen rights.
5. Whether minimal goal-only Skills retain adequate evidence discipline compared with comprehensive versions.

## Next suggested turn

Run R9 **agent usage and cross-session continuation** with an unfamiliar corpus and independently kept evaluator data, or, if independent agents are inaccessible, perform further controlled editorial red-team tests and explicitly state that external evaluation remains pending. Do not spend another round expanding the schema absent a documented failure. Keep user-facing Skills compact and move complex guidance to on-demand references.
