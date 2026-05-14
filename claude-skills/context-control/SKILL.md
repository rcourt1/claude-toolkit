---
name: context-control
description: Reduce context usage by limiting file reads, compressing project state, and creating short session handoffs.
---

# context-control

Use this skill to keep context small and reusable across long sessions.

## File scope lock

```text
For this task, only read files inside /src/[specific folder].
Do not load anything outside that directory unless I explicitly ask.
```

## Context compression

```text
Summarize everything you know about this project in under 500 tokens.
Focus on: stack, architecture, current task, top 3 constraints.
Use this as your working memory going forward.
```

## Session handoff

```text
Before we end: write a 200-token summary of what we built,
what's unfinished, and what to do first next session.
```
