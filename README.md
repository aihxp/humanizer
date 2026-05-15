# humanizer

![version](https://img.shields.io/badge/version-1.0.0-blue)
![license](https://img.shields.io/badge/license-MIT-green)
![type](https://img.shields.io/badge/type-pure--prompt%20skill-purple)
![dependencies](https://img.shields.io/badge/dependencies-none-brightgreen)
![patterns](https://img.shields.io/badge/tell%20catalog-32%20patterns-orange)
![tools](https://img.shields.io/badge/works%20with-8%20AI%20coding%20tools-teal)

A standalone, pure-prompt skill that rewrites AI-sounding prose so it reads as
genuinely human, and rewrites in a specific writer's voice when a sample or
style profile is available. It is just instructions: `SKILL.md` plus a few
reference files. No scripts, no dependencies, no network access.

## Why this one is different

- **Faithfulness over liveliness.** A three-layer guard plus a mandatory
  meaning check stop the most common humanizer failure: inventing plausible
  facts, causes, or quotes to make a rewrite "sound concrete."
- **Restraint by design.** A density pre-check scales effort to evidence, and
  an explicit do-not-flag reference protects already-human writing instead of
  laundering it into smooth, average prose.
- **Variance, not synonym-swapping.** It targets the real signature of
  machine text (uniform rhythm) rather than relocating it with a thesaurus.
- **Voice-first.** When a writing sample or a `VOICE.md` / `STYLE-GUIDE.md`
  is present, it rewrites in that author's cadence and stance, not generic
  neutral prose.
- **Opt-in edge.** A stance mode adds opinion and punch on explicit request,
  hard-blocked from inventing content.

## What it removes

A 32-pattern catalog in six families, each with detect / why / before-after /
restraint notes: inflated significance, promotional and evasive language,
formulaic structure, lexical tics, syntactic tics, and formatting artifacts,
including chat-UI contamination, debunking-pose headings, and diff-anchored
writing.

## Supported tools

| Tool | File it reads | Install |
|---|---|---|
| Claude Code | `SKILL.md` | `cp -r` this repo to `~/.claude/skills/humanizer/`, or use the repo in-project |
| Cursor | `.cursor/rules/humanizer.mdc` | Open this repo in Cursor, or copy `.cursor/rules/humanizer.mdc` + `SKILL.md` + `references/` into your project |
| Codex | `AGENTS.md` | Clone this repo into (or beside) your project; Codex reads `AGENTS.md` |
| Antigravity | `AGENTS.md` | Same as Codex: keep `AGENTS.md` + `SKILL.md` + `references/` in the workspace |
| Gemini CLI | `GEMINI.md` | Keep `GEMINI.md` + `SKILL.md` + `references/` in the project Gemini runs in |
| Pi Coder | `AGENTS.md` | Point Pi Coder at this repo / its `AGENTS.md` |
| OpenCode | `AGENTS.md` or `SKILL.md` | Copy the skill into OpenCode's skills directory, or keep `AGENTS.md` in the project |
| GitHub Copilot | `.github/copilot-instructions.md` | Copy `.github/copilot-instructions.md` + `SKILL.md` + `references/` into the target repository |

Every adapter points the agent at the same `SKILL.md` and `references/`, so
the workflow is identical across tools. The simplest universal install is to
clone this repository into (or alongside) the project you are writing in.

## Usage

Ask, in plain language, to humanize, de-slop, or fix prose that "reads like
AI," "sounds corporate," or is "too generic," or to make a draft sound like
you or a named author. You do not need to say the word "humanize."

For voice-matched output, do one of:

- paste a sample of the target writing,
- name a well-known author, or
- keep a `VOICE.md` (schema in `references/voice-matching.md`) or a
  `STYLE-GUIDE.md` in the project; it is discovered automatically.

Every run returns the rewritten text plus a short report: what changed, what
was deliberately left alone, a meaning check, and a next step.

## Scope

This skill improves prose quality and authentic voice. It is not designed or
tuned to defeat plagiarism checkers or AI-detection systems, and it names no
detector. Requests framed as passing AI work off as a person's own for a
graded or contractual assessment are reframed toward the quality-and-voice
use the skill actually serves.

## Layout

```
SKILL.md                        orchestrator: workflow, guardrails, output contract
AGENTS.md                       cross-tool entry point (Codex, Antigravity, OpenCode, Pi Coder)
GEMINI.md                       Gemini CLI context
.cursor/rules/humanizer.mdc     Cursor project rule
.github/copilot-instructions.md GitHub Copilot instructions
references/tell-patterns.md     the 32-pattern catalog (read in Pass 2)
references/do-not-flag.md       false positives, human markers, stop conditions
references/voice-matching.md    voice discovery and application
references/examples.md          four worked end-to-end runs
evals/evals.json                verification cases (not part of the runtime skill)
```

## License

MIT. See [LICENSE](LICENSE).
