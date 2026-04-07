# Claude Code Skills

Reusable [Claude Code](https://docs.anthropic.com/en/docs/claude-code) skills for software engineering workflows.

## Available Skills

| Skill | Description |
|-------|-------------|
| [`investigate-bug`](./investigate-bug/) | Systematically investigate production bugs — traces error logs to root cause, gathers evidence from code/DB/traces, and produces a comprehensive bug report |

## Installation

Copy any skill folder into your project's `.claude/skills/` directory:

```bash
# Copy a single skill
cp -r investigate-bug /path/to/your/project/.claude/skills/

# Or clone and copy
git clone https://github.com/<your-username>/claude-code-skills.git
cp -r claude-code-skills/investigate-bug /path/to/your/project/.claude/skills/
```

Then invoke it in Claude Code:

```
/investigate-bug FFmpeg failed with exit code 234, trace ID abc123
```

## How Skills Work

Skills are custom slash commands for Claude Code. They live in `.claude/skills/<name>/SKILL.md` and are automatically discovered when you open a project.

- **Project-scoped**: Place in your repo's `.claude/skills/` to share with your team
- **Personal**: Place in `~/.claude/skills/` to use across all your projects

Learn more: [Claude Code Skills Documentation](https://docs.anthropic.com/en/docs/claude-code/skills)

## Contributing

1. Create a new folder with your skill name
2. Add a `SKILL.md` with YAML frontmatter and instructions
3. Open a PR with a description of what the skill does and when to use it
