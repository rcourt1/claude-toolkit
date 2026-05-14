---
name: context-control
description: Reduce context usage by limiting file reads, compressing project state, and creating short session handoffs.
---

# context-control

Use this skill to keep context small, relevant, and reusable across long coding sessions.

## Use when
- Working in a large repo.
- Focusing on one folder or subsystem.
- Continuing a long session.
- Preparing to pause and resume later.
- Trying to reduce unnecessary context loading.

## Covers
- File scope lock
- Context compression
- Session handoff

## Core rules
- Read only the files needed for the current task.
- Prefer narrow scope before broad repo exploration.
- Compress project state into a short working summary when context grows.
- Preserve decisions, constraints, and next steps.
- Before ending a session, leave a short handoff for the next one.

## Mode 1: File scope lock
Use this when the task is limited to one area.

### Rules
- Only read files inside the specified directory.
- Do not load anything outside that directory unless explicitly asked.
- If more context is needed, ask before expanding scope.
- Prefer targeted file inspection over repo-wide search.

### Preset
```text
For this task, only read files inside /src/[specific folder].
Do not load anything outside that directory unless I explicitly ask.
```

## Mode 2: Context compression
Use this when the session is getting long or drifting.

### Rules
- Summarize the project state in under 500 tokens.
- Focus on stack, architecture, current task, and top 3 constraints.
- Keep only information needed for correct continuation.
- Drop repetitive history and low-value chatter.
- Use the compressed summary as working memory going forward.

### Preset
```text
Summarize everything you know about this project in under 500 tokens.
Focus on: stack, architecture, current task, top 3 constraints.
Use this as your working memory going forward.
```

## Mode 3: Session handoff
Use this before ending or pausing work.

### Rules
- Write a handoff in about 200 tokens.
- State what was built or changed.
- State what remains unfinished.
- State what to do first next session.
- Include blockers or open decisions if they matter.

### Preset
```text
Before we end: write a 200-token summary of what we built,
what’s unfinished, and what to do first next session.
```

## Compression checklist
Keep these if relevant:
- Active task
- Files changed
- Key decisions
- Constraints
- Known bugs
- Next action

Drop these if not needed:
- Repeated explanations
- Dead-end ideas
- Old alternatives already rejected
- Full command history
- Unchanged repo background

## Guardrails
- Compression must preserve actionable truth, not just shorten text.
- Do not remove important constraints, assumptions, or unresolved blockers.
- Do not expand file scope silently.
- If the task becomes cross-cutting, say so before widening context.

## Notes
This skill matches Claude’s broader compaction pattern: retain the important facts, decisions, and next steps while shedding low-value history, which is especially useful in long agentic coding sessions.