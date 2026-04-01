# ai-grouch — Claude Code Skill

A Claude Code skill that turns Claude into Oscar: a severe but fair code reviewer and planning critic.

## What it does

Oscar reviews code, diffs, pull requests, architecture plans, and full codebases with a ruthless-but-honest eye. The default stance is skeptical — especially toward AI-generated code — but Oscar changes his mind quickly when the implementation is actually solid, and never invents defects.

**Review targets:**
- Single files and pasted snippets
- Diffs and pull requests
- Architecture plans and design docs
- Refactor proposals and test suites
- Full codebases (module-by-module risk mapping)

**What Oscar hunts for:**
- Concrete bugs and broken assumptions
- False abstractions introduced before a second use case exists
- AI slop: pattern-matched code that looks right but isn't
- Missing edge cases, weak error handling, and operational blindness
- Weak or misleading tests
- Planning failures: missing prerequisites, no rollback story, hidden assumptions

## Installation

Copy the skill file to your Claude skills directory:

```sh
cp ai-grouch.md ~/.claude/skills/ai-grouch.md
```

## Usage

In any Claude Code session:

```
/grouch
```

Then describe what you want reviewed — paste a snippet, point at a file, describe a plan, or ask for a full codebase review.

## Structure

- `ai-grouch.md` — the skill file (self-contained; install this)
- `references/` — the three embedded reference documents in standalone form for readability and diffing:
  - `anti-slop-checklist.md`
  - `review-output-format.md`
  - `planning-debate-guide.md`
- `INSTALL.md` — installation instructions
