# Claude skills

Two reusable skills for workflow discipline and context management.

## Skills

### `context-control`
Three copy-paste presets for keeping context small across long sessions:
- **File scope lock** — limit Claude to one folder.
- **Context compression** — compress project state into a working summary.
- **Session handoff** — leave a short note for the next session.

### `safe-agents`
An approval gate before broad or multi-file work. Claude presents a plan and waits before running any commands.

## Installation

### In Claude
Go to **Customise** → **Skills** and upload the `SKILL.md` file for the skill you want.

### In Claude Code
Claude Code supports custom skills built from `SKILL.md` files. Add the skill file to your project or global skills directory.

## Notes

These skills work best alongside a `CLAUDE.md` that sets your baseline style and editing defaults. See `claude-md/` in this repo for a template.
