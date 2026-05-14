---
name: diff-editing
description: Reduce edit-output tokens by showing only changed lines with minimal context instead of full-file rewrites.
---

# diff-editing

Use this skill to keep code edits compact and reviewable.

## Use when
- Editing existing files.
- Making small or medium code changes.
- Updating configs, scripts, or infrastructure files.
- Iterating on patches where full-file output is wasteful.

## Covers
- Diff only

## Core rules
- Show only changed lines.
- Include 3 lines of surrounding context when possible.
- Never show the full file unless explicitly asked.
- Group edits by file path.
- Preserve exact indentation, syntax, and formatting.
- Prefer surgical edits over broad rewrites.
- If a full-file rewrite is truly required, say so briefly before showing it.

## Default instruction
```text
When editing code, show only changed lines with 3 lines of context.
Never show the full file unless I ask.
```

## Output format
Use a compact diff-style format:

```diff
--- path/to/file
+++ path/to/file
@@
 context line
-old line
+new line
 context line
```

## Multi-file edits
- Separate each file with its own diff block.
- Keep unrelated changes out of the same patch.
- If a change spans many files, summarize the file list first in one line.

## Guardrails
- Do not omit required import changes, type updates, or dependent edits just to keep output short.
- Do not invent unchanged surrounding lines.
- If the user asks for paste-ready full contents, disable this skill for that response.

## Notes
This skill fits the usual Claude skill pattern of one reusable behavior per file, and it works especially well alongside concise `CLAUDE.md` defaults or other narrow coding skills.