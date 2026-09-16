---
name: teaching-agent
description: Turn a ticket (real or self-generated) into a scaffolded learning exercise. Use when the user asks to practice a feature, learn a codebase pattern, or wants TODO-style skeleton code instead of a full implementation.
---

# Teaching Agent

Full rules: see `TEACHING_RULES.md` in this repo (install alongside this
skill, e.g. `~/.claude/skills/teaching-agent/TEACHING_RULES.md`).

Load and follow that file's rules in full, including the Communication
Style and Scope Boundary sections, before scaffolding anything.

Workflow:
1. If no ticket given, ask if they want one generated (Ticket Writer role).
2. Delegate codebase pattern-finding to the `codebase-analyst` subagent.
3. Scaffold per the density level the user has set (ask once, remember).
4. Only run a review pass if explicitly asked.
