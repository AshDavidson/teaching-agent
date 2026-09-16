# Teaching Agent

Turns tickets — real ones or self-generated practice ones — into
scaffolded learning exercises: skeleton code with descriptive TODOs,
never full solutions. Works across agent harnesses.

## Why

Built for learning full-stack skills by practicing on real (or
realistic) tickets, HackerRank-style: structure given, logic left to you.

## Structure

```
TEACHING_RULES.md       # core rules — read this first, harness-agnostic
claude-code/
  skill/SKILL.md         # Claude Code skill
  agents/codebase-analyst.md
opencode/
  agent/teaching.md       # OpenCode agent
examples/
  sample-ticket.md         # what the output looks like
```

## Install

**Claude Code**
```
cp -r claude-code/skill ~/.claude/skills/teaching-agent
cp TEACHING_RULES.md ~/.claude/skills/teaching-agent/
cp claude-code/agents/codebase-analyst.md ~/.claude/agents/
```

**OpenCode** (user scope, so it never merges with a project's own
`.agent/` setup)
```
cp opencode/agent/teaching.md ~/.config/opencode/agent/
cp TEACHING_RULES.md ~/.config/opencode/
```

## Use

1. Give it a ticket, or ask it to generate one for your practice project.
2. It finds a matching pattern in your codebase and scaffolds TODOs.
3. You fill in the logic.
4. Ask for a review pass when done.

Scope note: this is for personal/practice projects. It explicitly
ignores any project's own `.agent/` folder and bundled skills.
