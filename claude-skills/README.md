# Claude token optimization skills

A small collection of reusable Claude skills focused on one thing: using Claude more efficiently.

These skills are for people who use Claude heavily and want tighter control over token usage, output length, context loading, and agent behavior. They are not meant to make Claude sound cleverer. They are meant to make it cheaper, faster, and more predictable.

## Why this exists

When Claude is part of your daily workflow, token waste compounds quickly. A little extra preamble, a full-file rewrite when only 5 lines changed, broad repo exploration for a narrow fix, or overly deep reasoning on a simple task can add unnecessary cost and friction.

This repo exists to reduce that overhead.

The skills here turn common “good habits” into reusable instructions:
- keep output lean,
- show diffs instead of full files,
- avoid overthinking simple tasks,
- limit context to only what matters,
- and add approval checkpoints before broad agentic work.

They are intentionally small, practical, and composable.

## What these skills are for

These skills help Claude:
- respond with less filler,
- avoid loading unnecessary context,
- keep code edits compact,
- scale reasoning to task complexity,
- and pause before broad multi-file work.

They are especially useful for:
- coding sessions with lots of iteration,
- large repos where context can balloon,
- long-running sessions that need compression,
- and agent-style workflows where uncontrolled scope can get expensive fast.

## What is a Claude skill?

A Claude skill is a custom instruction package built around a `SKILL.md` file. Skills teach Claude how to behave in a specific situation, and Claude can choose to use them automatically when the prompt matches the skill’s purpose.

Think of them as reusable behavior modules, for example:
- one skill for concise output
- one for safer agent workflows

Good skills are:
- narrow in scope,
- easy to trigger through normal language,
- opinionated enough to be useful,
- and able to work alongside other skills.

## Installation

### In Claude
Custom skills can be created or uploaded through Claude’s Skills interface in Settings/Capabilities, where Anthropic documents support for custom `SKILL.md`-based skills.

General flow:
1. Open Claude.
2. Go to **Customise**.
3. Go to **Skills**.
4. Create or upload a skill using its `SKILL.md` file.

### In Claude Code
Claude Code also supports creating, managing, and sharing skills, including custom skills built from `SKILL.md` files.


## Design principles

These skills follow a few simple rules:
- one clear purpose per skill,
- short instructions,
- practical defaults,
- minimal overlap,
- easy to combine.

The goal is not to create a giant instruction system. The goal is to create small reusable tools that make Claude more efficient in real work.

## Who this is for

This repo is most useful for people who:
- use Claude frequently for coding or technical work,
- care about token efficiency,
- work in large or messy codebases,
- want tighter control over agent behavior,
- and prefer reusable system-level habits over retyping the same prompt patterns.

## Notes

These are workflow tools, not magic fixes. They work best when the task itself is clear and scoped well.

If a task is genuinely complex, Claude still needs room to reason properly. If a full file is needed, a diff-only style should be relaxed. If a repo-wide change is intentional, approval gates should be used to guide it, not block it.

The aim is disciplined usage, not rigid usage.