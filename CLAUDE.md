# Claude Agents Repository

This is a collection of Claude Code subagent `.md` files, not a runnable application. There is no build step, no tests, and no dependencies.

## What This Repo Contains

43+ agent definition files organized into 8 department folders (`engineering/`, `design/`, `marketing/`, `product/`, `project-management/`, `studio-operations/`, `testing/`, `bonus/`).

## Agent File Format

Each `.md` file follows this structure:
- **YAML frontmatter** between `---` delimiters: `name`, `description`, `model`, `color`, `tools`, `permissionMode`, `memory`, and optional fields like `skills`, `maxTurns`, `background`, `isolation`, `mcpServers`, `hooks`
- **Markdown body**: the agent's system prompt (500+ words covering role, responsibilities, expertise, and constraints)

## Conventions

- File names use **kebab-case** (e.g., `database-migration-agent.md`)
- Files live in the appropriate **department folder**
- The `name` field in frontmatter must match the file name (without `.md`)
- The `description` field must include 3-4 `<example>` blocks showing when to use the agent
- Every agent file must have exactly 2 `---` delimiters (opening and closing frontmatter)

## How to Test Agents

1. Copy agent files to `~/.claude/agents/` (user-level) or `.claude/agents/` (project-level)
2. Restart Claude Code to load the new agents
3. Describe a task matching the agent's description to verify it gets selected
4. Test with real tasks to validate the system prompt produces useful results
