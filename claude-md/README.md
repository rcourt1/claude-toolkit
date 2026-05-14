# claude-md

CLAUDE.md templates for setting persistent defaults in Claude Code projects.

## What is CLAUDE.md?

A `CLAUDE.md` file is read by Claude Code at the start of every session. It sets standing instructions that apply throughout the project without needing to be repeated in each prompt.

## What is in here

| File | Purpose |
|---|---|
| `CLAUDE.md` | Baseline style and editing defaults — lean output, diff-only edits, minimal reasoning |

## How to use

Copy the template into the root of your project:

```bash
cp CLAUDE.md /your/project/CLAUDE.md
```

Edit it to fit your project. Remove anything that does not apply. Add project-specific context if needed.

## Notes

Keep CLAUDE.md short. Long instruction files dilute the signal. If a behavior is conditional or task-specific, a skill is a better fit than a standing instruction.
