---
name: reasoning-control
description: Keep reasoning effort proportional to task complexity so straightforward work does not trigger unnecessary deep analysis.
---

# reasoning-control

Use this skill to prevent overthinking on simple, well-scoped tasks.

## Use when
- Fixing a small bug.
- Making a narrow refactor.
- Updating one isolated feature.
- Answering a direct technical question with a clear path.
- Working on a task where deep exploration is unlikely to add value.

## Covers
- Thinking cap

## Core rules
- Use minimal reasoning for straightforward tasks.
- Treat simple bug fixes, refactors, and scoped edits as low-complexity by default.
- Do not overthink the task.
- Prefer the simplest correct solution.
- Keep analysis proportional to risk, ambiguity, and scope.
- Increase reasoning only if a real blocker, hidden dependency, or ambiguity appears.

## Default instruction
```text
Use minimal reasoning for this task.
It is a straightforward bug fix, refactor, or scoped change.
Do not overthink it.
```

## Decision rules
### Use low reasoning when
- The file scope is small.
- The requested change is explicit.
- The existing pattern is already clear.
- The task can be completed with a direct implementation.

### Increase reasoning only when
- Requirements conflict.
- The bug cause is unclear.
- Multiple systems are affected.
- Security, data loss, or production risk is involved.
- The simplest fix may create hidden regressions.

## Response style
- Move quickly to the solution.
- Avoid long option lists unless trade-offs matter.
- Do not narrate internal thinking at length.
- If complexity appears, state it briefly and then adapt.

## Guardrails
- Minimal reasoning does not mean careless reasoning.
- Do not skip validation of important assumptions.
- Do not force a simple answer onto a genuinely complex problem.
- If more context is required, ask for it early instead of guessing.

## Notes
This skill follows the general custom-skill pattern of one focused workflow per `SKILL.md`, and it pairs well with concise `CLAUDE.md` defaults plus other narrow skills such as diff-based editing or plan-before-agent guardrails.