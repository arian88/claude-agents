# Claude Code AI Agents

A comprehensive collection of specialized AI agents designed to accelerate and enhance every aspect of rapid development. Each agent is an expert in their domain, ready to be invoked when their expertise is needed.

## Installation

1. **Download this repository:**
   ```bash
   git clone https://github.com/your-org/claude-agents.git
   ```

2. **Copy to your Claude Code agents directory:**
   ```bash
   cp -r claude-agents/* ~/.claude/agents/
   ```

   Or manually copy all the agent files to your `~/.claude/agents/` directory.

3. **Restart Claude Code** to load the new agents.

## Quick Start

Agents are automatically available in Claude Code. Simply describe your task and the appropriate agent will be triggered. You can also explicitly request an agent by mentioning their name.

Learn more: [Claude Code Sub-Agents Documentation](https://docs.anthropic.com/en/docs/claude-code/sub-agents)

### Example Usage
- "Create a new app for tracking meditation habits" → `rapid-prototyper`
- "What's trending on TikTok that we could build?" → `trend-researcher`
- "Our app reviews are dropping, what's wrong?" → `feedback-synthesizer`
- "Make this loading screen more fun" → `whimsy-injector`
- "Review the auth module for security issues" → `security-auditor`
- "Document our REST API endpoints" → `technical-writer`

## Directory Structure

Agents are organized by department for easy discovery:

```
agents/
├── design/
│   ├── accessibility-auditor.md
│   ├── brand-guardian.md
│   ├── ui-designer.md
│   ├── ux-researcher.md
│   ├── visual-storyteller.md
│   └── whimsy-injector.md
├── engineering/
│   ├── ai-engineer.md
│   ├── backend-architect.md
│   ├── code-reviewer.md
│   ├── devops-automator.md
│   ├── frontend-developer.md
│   ├── mobile-app-builder.md
│   ├── rapid-prototyper.md
│   ├── security-auditor.md
│   └── test-writer-fixer.md
├── marketing/
│   ├── app-store-optimizer.md
│   ├── content-creator.md
│   ├── growth-hacker.md
│   ├── instagram-curator.md
│   ├── reddit-community-builder.md
│   ├── seo-specialist.md
│   ├── tiktok-strategist.md
│   └── twitter-engager.md
├── product/
│   ├── feedback-synthesizer.md
│   ├── sprint-prioritizer.md
│   ├── technical-writer.md
│   └── trend-researcher.md
├── project-management/
│   ├── experiment-tracker.md
│   ├── project-shipper.md
│   └── studio-producer.md
├── studio-operations/
│   ├── analytics-reporter.md
│   ├── data-analyst.md
│   ├── finance-tracker.md
│   ├── infrastructure-maintainer.md
│   ├── legal-compliance-checker.md
│   └── support-responder.md
├── testing/
│   ├── api-tester.md
│   ├── performance-benchmarker.md
│   ├── test-results-analyzer.md
│   ├── tool-evaluator.md
│   └── workflow-optimizer.md
└── bonus/
    ├── joker.md
    └── studio-coach.md
```

## Complete Agent List

### Engineering Department (`engineering/`)
- **ai-engineer** - Integrate AI/ML features that actually ship
- **backend-architect** - Design scalable APIs and server systems
- **code-reviewer** - Automated code quality analysis with severity-rated feedback
- **devops-automator** - Deploy continuously without breaking things
- **frontend-developer** - Build blazing-fast user interfaces
- **mobile-app-builder** - Create native iOS/Android experiences
- **rapid-prototyper** - Build MVPs in days, not weeks
- **security-auditor** - Identify vulnerabilities across OWASP Top 10 and dependencies
- **test-writer-fixer** - Write tests that catch real bugs

### Product Department (`product/`)
- **feedback-synthesizer** - Transform complaints into features
- **sprint-prioritizer** - Ship maximum value per sprint
- **technical-writer** - Create API docs, READMEs, ADRs, and tutorials
- **trend-researcher** - Identify viral opportunities

### Marketing Department (`marketing/`)
- **app-store-optimizer** - Dominate app store search results
- **content-creator** - Generate content across all platforms
- **growth-hacker** - Find and exploit viral growth loops
- **instagram-curator** - Master the visual content game
- **reddit-community-builder** - Win Reddit without being banned
- **seo-specialist** - Optimize for search visibility, Core Web Vitals, and structured data
- **tiktok-strategist** - Create shareable marketing moments
- **twitter-engager** - Ride trends to viral engagement

### Design Department (`design/`)
- **accessibility-auditor** - Audit WCAG compliance, ARIA, keyboard nav, and screen readers
- **brand-guardian** - Keep visual identity consistent everywhere
- **ui-designer** - Design interfaces developers can actually build
- **ux-researcher** - Turn user insights into product improvements
- **visual-storyteller** - Create visuals that convert and share
- **whimsy-injector** - Add delight to every interaction

### Project Management (`project-management/`)
- **experiment-tracker** - Data-driven feature validation
- **project-shipper** - Launch products that don't crash
- **studio-producer** - Keep teams shipping, not meeting

### Studio Operations (`studio-operations/`)
- **analytics-reporter** - Turn data into actionable insights
- **data-analyst** - SQL queries, cohort analysis, and business intelligence
- **finance-tracker** - Keep the business profitable
- **infrastructure-maintainer** - Scale without breaking the bank
- **legal-compliance-checker** - Stay legal while moving fast
- **support-responder** - Turn angry users into advocates

### Testing & Benchmarking (`testing/`)
- **api-tester** - Ensure APIs work under pressure
- **performance-benchmarker** - Make everything faster
- **test-results-analyzer** - Find patterns in test failures
- **tool-evaluator** - Choose tools that actually help
- **workflow-optimizer** - Eliminate workflow bottlenecks

### Bonus Agents (`bonus/`)
- **studio-coach** - Rally the AI troops to excellence
- **joker** - Lighten the mood with tech humor

## Proactive Agents

Some agents trigger automatically in specific contexts:
- **studio-coach** - When complex multi-agent tasks begin or agents need guidance
- **test-writer-fixer** - After implementing features, fixing bugs, or modifying code
- **whimsy-injector** - After UI/UX changes
- **experiment-tracker** - When feature flags are added

## Best Practices

1. **Let agents work together** - Many tasks benefit from multiple agents
2. **Be specific** - Clear task descriptions help agents perform better
3. **Trust the expertise** - Agents are designed for their specific domains
4. **Iterate quickly** - Agents support rapid iteration workflows

## Technical Details

### Agent Front Matter Reference

Each agent `.md` file starts with YAML front matter defining its configuration:

| Field | Required | Values | Description |
|-------|----------|--------|-------------|
| `name` | Yes | string | Unique agent identifier (kebab-case) |
| `description` | Yes | string | When to use the agent, with examples |
| `model` | No | `opus`, `sonnet`, `haiku`, `inherit` | AI model selection. Defaults to inherit. |
| `color` | No | `red`, `blue`, `green`, `yellow`, `purple`, `orange`, `pink`, `cyan` | Visual identification in UI |
| `tools` | No | comma-separated list | Tools the agent can access (e.g., `Read, Write, Edit, Bash, Grep, Glob, Agent, WebSearch, WebFetch, TaskCreate, TaskUpdate, TaskList, TaskGet`) |
| `disallowedTools` | No | comma-separated list | Tools explicitly denied (useful when `tools` is omitted and agent inherits all) |
| `permissionMode` | No | `default`, `acceptEdits`, `dontAsk`, `bypassPermissions`, `plan` | How permission prompts are handled |
| `memory` | No | `user`, `project`, `local` | Persistent memory scope for cross-session learning |
| `maxTurns` | No | integer | Maximum agentic turns before stopping |
| `background` | No | `true`, `false` | Whether agent runs in background by default |
| `isolation` | No | `worktree` | Run agent in an isolated git worktree |
| `skills` | No | list | Skills available to the agent |
| `mcpServers` | No | object | MCP servers the agent can access |
| `hooks` | No | object | Lifecycle hooks for agent events |

### Permission Modes

| Mode | Behavior |
|------|----------|
| `default` | Prompts user for each permission request |
| `acceptEdits` | Auto-accepts file edits, prompts for other actions |
| `dontAsk` | Auto-denies all permission prompts (ideal for read-only agents) |
| `bypassPermissions` | Auto-accepts all permission requests |
| `plan` | Agent operates in plan mode, producing plans rather than executing |

### Tool Reference

Common tools available to agents:

| Tool | Purpose |
|------|---------|
| `Read` | Read file contents |
| `Write` | Create or overwrite files |
| `Edit` | Make targeted edits to existing files |
| `Bash` | Execute shell commands |
| `Grep` | Search file contents with regex |
| `Glob` | Find files by pattern |
| `Agent` | Launch sub-agents for complex tasks |
| `WebSearch` | Search the web |
| `WebFetch` | Fetch and process web content |
| `TaskCreate` | Create task list items |
| `TaskUpdate` | Update task status and details |
| `TaskList` | List all tasks |
| `TaskGet` | Get full task details by ID |

### Adding New Agents

1. Create a new `.md` file in the appropriate department folder
2. Follow the front matter format below
3. Include 3-4 detailed usage examples in the description
4. Write a comprehensive system prompt (500+ words)
5. Test the agent with real tasks

#### Agent File Template

```markdown
---
name: your-agent-name
description: "Use this agent when [scenario]. This agent specializes in [expertise]. Examples:\n\n<example>\nContext: [situation]\nuser: \"[user request]\"\nassistant: \"[response approach]\"\n<commentary>\n[why this example matters]\n</commentary>\n</example>\n\n[3 more examples...]"
model: sonnet
color: blue
tools: Write, Read, Edit, Bash, Grep, Glob
permissionMode: default
memory: project
---

You are a [role] who [primary function]. Your expertise spans [domains].

Your primary responsibilities:
1. [Responsibility 1]
2. [Responsibility 2]
...

[Detailed system prompt content — 500+ words covering domain expertise,
methodologies, decision frameworks, and output formats.]

Your goal is to [ultimate objective].
```

## Latest Features

### Persistent Memory

Agents can retain knowledge across sessions using the `memory` field:

- **`project`** — Remembers project-specific patterns, architecture decisions, and conventions. Best for agents that work within a single codebase (engineering, testing, project management).
- **`user`** — Remembers knowledge that transcends projects. Best for agents whose expertise is universal (legal compliance, marketing platforms, tool evaluation).
- **`local`** — Scoped to the local machine.

### Background Agents

Set `background: true` to let an agent run concurrently while you continue working. Ideal for read-only analysis tasks like code review. The `code-reviewer` agent uses this by default.

### `dontAsk` Permission Mode

For read-only agents that should never write files, `permissionMode: dontAsk` auto-denies any write permission prompts. This is safer than trusting the agent not to attempt writes — it enforces the constraint at the permission layer. Used by `code-reviewer`.

### Worktree Isolation

Set `isolation: worktree` to run an agent in a temporary git worktree, giving it an isolated copy of the repository. Useful for agents making risky or experimental changes. Best configured per-invocation via `--worktree` flag rather than hardcoded in agent front matter.

### Agent Teams (Experimental)

Multiple agents can be orchestrated together for complex tasks. The `studio-coach` and `studio-producer` agents are designed to coordinate multi-agent workflows using the `Agent` tool.

### Agent-Scoped Hooks

Agents support lifecycle hooks for automation (e.g., running linters after edits, validating output format). Configure hooks in `.claude/settings.json` at the project level rather than in individual agent files.

### `maxTurns`

Limit the number of agentic turns an agent can take. Useful for agents with bounded tasks — for example, `joker` uses `maxTurns: 5` since humor delivery should be quick.

## Agent Performance

Track agent effectiveness through:
- Task completion time
- User satisfaction
- Error rates
- Feature adoption
- Development velocity

## Customization Checklist

Use this checklist when creating or modifying agents:

### Required Components
- [ ] **YAML Front Matter**
  - [ ] `name`: Unique agent identifier (kebab-case)
  - [ ] `description`: When to use + 3-4 detailed examples with context/commentary
  - [ ] `model`: AI model (opus for complex reasoning, sonnet for balanced, haiku for fast/simple)
  - [ ] `color`: Visual identification
  - [ ] `tools`: Specific tools the agent can access
  - [ ] `permissionMode`: Permission handling
  - [ ] `memory`: Cross-session memory scope (user or project)

### System Prompt Requirements (500+ words)
- [ ] **Agent Identity**: Clear role definition and expertise area
- [ ] **Core Responsibilities**: 5-8 specific primary duties
- [ ] **Domain Expertise**: Technical skills and knowledge areas
- [ ] **Best Practices**: Specific methodologies and approaches
- [ ] **Constraints**: What the agent should/shouldn't do
- [ ] **Success Metrics**: How to measure agent effectiveness

### Testing & Validation
- [ ] Agent activates correctly for intended use cases
- [ ] Agent can use all specified tools properly
- [ ] Responses are helpful and actionable
- [ ] Agent handles unexpected or complex scenarios
- [ ] Works well with other agents in multi-agent workflows
- [ ] Completes tasks within reasonable timeframes

### Department-Specific Guidelines

| Department | Focus |
|------------|-------|
| **Engineering** | Implementation speed, code quality, testing |
| **Design** | User experience, visual consistency, accessibility |
| **Marketing** | Viral potential, platform expertise, growth metrics |
| **Product** | User value, data-driven decisions, documentation |
| **Operations** | Process optimization, data analysis, compliance |
| **Testing** | Quality assurance, performance, workflow efficiency |
| **Project Management** | Team coordination, shipping, scope management |

## Contributing

To improve existing agents or suggest new ones:
1. Use the customization checklist above
2. Test thoroughly with real projects
3. Document performance improvements
4. Share successful patterns with the community
