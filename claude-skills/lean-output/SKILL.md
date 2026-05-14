---
name: lean-output
description: Reduce output tokens by enforcing terse, direct responses with no filler and optional response budgets.
---

# lean-output

Use this skill to keep responses compact, direct, and cheap.

## Use when
- Working on straightforward coding tasks.
- Iterating quickly on fixes or edits.
- Reducing response verbosity across a session.
- Setting a concise default style in Claude workflows.

## Covers
- Startup audit
- Caveman mode
- No preamble rule
- Output budget

## Core rules
- Respond in minimal words.
- Skip preamble, explanation, and summary unless needed.
- Start with the answer.
- No “here is”, no “I will”, no “Great question”, no “Of course”, no “Certainly”, no “Let me”, no “Sure”.
- No closings.
- For code tasks, prefer code-first output.
- Comments only when critical.
- Keep technical substance; remove filler.
- If a response budget is given, treat it as a hard cap.

## Startup audit preset
Use this at the start of a session:

```text
Respond in minimal words.
Skip preamble, explanation, summary.
Start with the answer.
Code only when appropriate. Comments only when critical.
No “here is”, no “I will”, no closings.
```

## CLAUDE.md preset
Use this as a persistent default:

```text
Respond in minimal words.
Skip preamble, explanation, summary.
Start with the answer.
Code only when appropriate. Comments only when critical.
No “here is”, no “I will”, no “Great question”, no “Of course”, no “Certainly”, no “Let me”, no “Sure”, no closings.
```

## Output budget preset
Use this for simple tasks:

```text
Your response budget for this task is 300 tokens.
Prioritize what matters. Cut everything else.
```

## Style guidance
- Prefer short sentences or fragments when clarity is preserved.
- Keep exact code, function names, API names, and error strings unchanged.
- Do not remove important warnings, assumptions, or safety-critical details.
- If the user explicitly asks for explanation, provide it briefly.

## Notes
This skill is aligned with common Claude Code advice to keep persistent instructions short and specific, and it is also compatible with public “caveman”-style compression approaches that focus on preserving substance while stripping filler.