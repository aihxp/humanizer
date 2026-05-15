# Changelog

All notable changes to this skill are documented here. This project adheres
to semantic versioning.

## [1.0.0] - 2026-05-15

First stable release.

### Added

- Pure-prompt `humanizer` skill: `SKILL.md` plus four on-demand reference
  files. No scripts, no dependencies, no network access.
- 32-pattern tell catalog in six families, each with detect / why /
  before-after / restraint guidance (`references/tell-patterns.md`),
  including chat-UI contamination, debunking-pose headings, and diff-anchored
  writing.
- Restraint reference (`references/do-not-flag.md`): false positives, human
  markers to preserve, model idiolects, and hard stop conditions.
- Voice-first workflow with filesystem voice discovery and an optional
  `VOICE.md` schema (`references/voice-matching.md`).
- Density pre-check (Step 0c) that scales effort to evidence so human-first
  text is not over-edited.
- Opt-in stance mode (Step 0b) for livelier output on explicit request,
  hard-blocked from inventing content.
- Three-layer anti-fabrication guard and a mandatory meaning check covering
  both invented specifics and soft causal or temporal inference.
- Four worked end-to-end examples (`references/examples.md`).
- Multi-tool support: Claude Code, Cursor, Codex, Antigravity, Gemini CLI,
  Pi Coder, OpenCode, GitHub Copilot, Windsurf, Cline, Continue, Zed, and
  Aider, via `SKILL.md`, `AGENTS.md`, `.cursor/rules/humanizer.mdc`,
  `GEMINI.md`, `.github/copilot-instructions.md`, `.windsurfrules`,
  `.clinerules`, `.continue/rules/humanizer.md`, and `CONVENTIONS.md`.
- Verification eval set (`evals/evals.json`), MIT license.
