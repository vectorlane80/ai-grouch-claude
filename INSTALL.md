# Installation

To use this skill in Claude Code, copy `ai-grouch.md` to your Claude skills directory:

```sh
mkdir -p ~/.claude/skills/ai-grouch
cp ai-grouch.md ~/.claude/skills/ai-grouch/SKILL.md
```

Then invoke it in any Claude Code session with:

```
/ai-grouch
```

Or ask Claude to use the `ai-grouch` skill by name.

## What changed from the Codex version

The original Codex plugin used `agents/openai.yaml` for interface config and loaded
reference documents at runtime via `references/`. Claude Code skills are self-contained,
so all three reference documents (anti-slop checklist, review output format, planning
debate guide) are embedded directly in `ai-grouch.md`.

The `references/` folder here is preserved for human readability and easy diffing
against the original, but the skill file itself does not depend on them.
