# Installing the draft Skills

These are ordinary folders using the open Agent Skills `SKILL.md` convention. The repository is not a universal installer and does not assume a specific host runtime.

- **Install only Builder:** copy the entire `skills/research-kernel-builder/` directory into a location scanned for skills by your agent; keep `references` and `assets` inside it.
- **Install only Archaeologist:** copy the entire `skills/research-archaeologist/` directory similarly. It does not require Builder.
- **Install both:** copy both directories without renaming either; they share semantics but have independent resource copies, and neither requires the repository's `shared/` root to work.

For Claude Code, `.claude/skills/` or `~/.claude/skills/` are documented skill roots. Other platforms, including Codex and Gemini, may provide different installation and trust settings; verify current product documentation instead of assuming directory equivalence. If your hosted assistant accepts a ZIP skill upload, packaging may require a ZIP containing a **single** skill directory rather than this two-skill repository ZIP. The GitHub repo is designed to be unpacked first.

The user supplies authorized source materials in their normal workspace. This package does not ship PDF extraction tools, scripts, a Python CLI, fixed storage backends, or model-specific API configuration. A capable agent may choose permitted tools but must report their actual use and limits.

For basic smoke tests, use `examples/synthetic-research` or `examples/synthetic-software`. For harder attribution, implementation and missing-evidence cases, use `examples/synthetic-adversarial` and `evaluation/R8_ADVERSARIAL_CASES.md`. Do not represent results on these visible teaching cases as independent evaluations.

See also: https://agentskills.io/specification and your host's official documentation.
