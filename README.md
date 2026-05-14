# claude-toolkit

A public toolkit of reusable Claude skills, prompts, patterns, and workflow helpers.

This repo started as a place to store Claude skills I want available in every session. Over time, it will grow into a broader toolkit of practical Claude AI resources that make day-to-day use more efficient, more consistent, and easier to scale.


## Why this repo exists

If you use Claude often enough, you start repeating the same patterns:
- asking for shorter responses,
- narrowing file scope,
- stopping unnecessary full-file rewrites,
- compressing context at the end of long sessions,
- or adding guardrails before agentic work expands too far.

Those patterns are useful, but retyping them every session is noisy and easy to forget.

This repo exists to collect those patterns in one place and turn them into reusable assets.

The first focus is Claude skills, because they are one of the cleanest ways to package repeated behavior into something structured and reusable. Anthropic’s docs describe skills as reusable instruction packages that extend Claude’s capabilities, while Claude Code also supports creating and sharing skills for repeated workflows.

## What is in this repo

Right now, this repo is mainly for Claude skills.

Over time, it may also include:
- `SKILL.md` files for reusable behaviors,
- `CLAUDE.md` patterns and templates,
- prompt snippets,
- workflow notes,
- session management patterns,
- repo structures for Claude Code,
- and other small utilities that make Claude easier to use well.

The aim is practical reuse, not collecting random AI files.

## Current focus

The current skill set is focused on token efficiency and workflow discipline:
- lean output,
- diff-only editing,
- reasoning control,
- context control,
- safe agent behavior.

These are meant to make Claude more predictable in real work, especially during coding or long technical sessions.

## Who this is for

This repo is most useful for people who:
- use Claude regularly,
- work across coding, research, writing, or planning,
- want more control over output style and token usage,
- and prefer reusable systems over rewriting the same instructions repeatedly.

It is especially relevant for people using Claude Code or custom Claude skills, where reusable instruction files and workflow conventions have a direct effect on how Claude behaves.

## Repo philosophy

A few principles guide what goes into this repo:

- Public only: no secrets, no personal credentials, no sensitive work context.
- Reusable first: anything here should be useful beyond one narrow session.
- Small and modular: simple tools are easier to combine and maintain.
- Practical over clever: the goal is better workflows, not novelty.
- Expandable: the repo should be able to grow from “skills collection” into a wider Claude toolkit without needing a redesign.

## What a “toolkit” means here

In this repo, a toolkit means a collection of small, reusable building blocks for working with Claude more effectively.

That can include:
- behavior-level tools, like skills,
- instruction-layer tools, like `CLAUDE.md` templates,
- process tools, like handoff or compression patterns,
- and usage guides for installing or combining them.

Skills improve behavior. Templates improve consistency. Workflow notes improve repeatability.

Together, they make Claude easier to use intentionally.

## Structure

The structure will likely evolve, but a typical layout may look like this:

```text
claude-toolkit/
├── claude-skills/
│   ├── lean-output/
│   │   └── SKILL.md
│   ├── diff-editing/
│   │   └── SKILL.md
│   ├── reasoning-control/
│   │   └── SKILL.md
│   ├── context-control/
│   │   └── SKILL.md
│   └── safe-agents/
│       └── SKILL.md
├── claude-md/
├── prompts/
├── templates/
└── docs/
```

## How to use this repo

You do not need to use everything.

The best way to use this repo is to pick the parts that solve a real problem in your workflow:
- install a skill,
- copy a template,
- adapt a pattern,
- or use a prompt as a starting point.

For Claude Skills, Claude supports custom skills created from `SKILL.md` files, and Claude Code also supports creating, managing, and sharing reusable skills.

## What this repo is not

This repo is not:
- a dump of random prompts,
- a place for private instructions,
- a replacement for judgment,
- or a claim that Claude should always behave the same way in every context.

Some tasks need more reasoning. Some need full-file output. Some need broader context. The goal here is not rigidity. It is better defaults.

## Future direction

The long-term goal is simple: build a clean public repo of Claude resources that are actually useful in daily work.

That may include:
- better skill packs,
- install notes,
- example workflows,
- layered `CLAUDE.md` setups,
- task-specific instruction templates,
- and general patterns for using Claude more effectively over time.

If the repo becomes a reliable personal toolkit first, it has a good chance of being useful to other people too.

## Notes

This repo only contains public-safe material. Anything personal, sensitive, or tied to private work stays out.

That keeps the repo shareable, easier to maintain, and safer to expand.