---
name: safe-agents
description: Add approval gates before broad, agentic, or multi-file work so Claude plans first and expands scope only with permission.
---

# safe-agents

Use this skill to add a checkpoint before Claude starts broad autonomous work.

## Use when
- A task likely requires more than 3 file edits.
- The implementation path is unclear.
- Commands may trigger broad repo exploration.
- The task is high-impact, expensive, or risky.
- You want approval before Claude expands scope.

## Covers
- Plan before agent

## Core rules
- Before any task requiring more than 3 file edits, stop and present a plan.
- List which files will be touched.
- Explain why each file needs changes.
- Wait for approval before running any commands.
- If scope expands mid-task, pause and ask again.
- Prefer explicit checkpoints over silent autonomy.

## Default instruction
```text
Before any task requiring more than 3 file edits:
Describe your plan in text.
List which files you’ll touch and why.
Wait for my approval before running any commands.
```

## Planning format
Use this structure:

```text
Plan:
1. [step]
2. [step]
3. [step]

Files:
- path/to/fileA — reason
- path/to/fileB — reason
- path/to/fileC — reason

Waiting for approval before running commands.
```

## Decision rules
### Require approval when
- More than 3 files may change.
- The change crosses modules or layers.
- The task includes repo-wide search or refactoring.
- Migrations, renames, or generated updates are involved.
- There is risk of deleting, overwriting, or broad restructuring.

### Proceed without approval when
- The fix is obviously local.
- The user explicitly asked for autonomous execution.
- Only 1 to 3 files need clear, low-risk edits.
- The path is already known and narrow.

## Guardrails
- Do not silently widen scope.
- Do not run broad commands before presenting the plan.
- Do not confuse “simple request” with “small change set”.
- If uncertainty is high, ask before acting.
- If the user approves the plan, execute only that plan unless re-approved.

## Notes
This skill works well for multi-file or agentic workflows because Claude Code can coordinate broad edits across a codebase, which makes planning and approval a useful cost and scope control layer.