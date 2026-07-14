# Marketplace plugins — not yet installed

These are available in the `claude-plugins-official` marketplace (already added on this machine) but not currently installed. Install any of them with:

```
/plugin install <name>@claude-plugins-official
```

## For the CSE student

| Plugin | Description |
|---|---|
| `pyright-lsp` | Python language server (Pyright) — static type checking and code intelligence for `.py`/`.pyi` |
| `clangd-lsp` | C/C++ language server |
| `jdtls-lsp` | Java language server |
| `typescript-lsp` | TypeScript/JavaScript language server |
| `rust-analyzer-lsp` | Rust language server |
| `gopls-lsp` | Go language server |
| `csharp-lsp` | C# language server |
| `kotlin-lsp` | Kotlin language server |
| `ruby-lsp` | Ruby language server |
| `php-lsp` | PHP language server |
| `lua-lsp` | Lua language server |
| `swift-lsp` | Swift language server |
| `math-olympiad` | Solve competition math (IMO-style) problems — useful for discrete math / algorithms coursework |
| `code-modernization` | Modernize legacy codebases (COBOL and similar) — relevant for legacy-systems coursework |
| `commit-commands` | Streamlined git commands for committing, useful for group project workflows |
| `claude-md-management` | Audit and maintain CLAUDE.md quality as a project repo grows |
| `learning-output-style` | Interactive learning mode — Claude requests meaningful code contributions from you at decision points instead of just producing the answer |
| `explanatory-output-style` | Adds educational insights about *why*, not just *what*, for implementation choices |
| `session-report` | Write up what an agent session did — good for a project log or lab writeup |
| `project-artifact` | Generate and publish a polished project status page |
| `code-simplifier` | Agent that simplifies and refines code for clarity |
| `feature-dev` | Full feature-development workflow with codebase-exploration agents, for larger course projects |
| `example-plugin` | Reference example showing every Claude Code plugin extension point — good for learning how plugins work |
| `skill-creator` | Scaffolding for creating your own custom skills |

## For the AI intern

| Plugin | Description |
|---|---|
| `mcp-server-dev` | Skills for designing and building MCP servers that work seamlessly with Claude — deployment models, remote HTTP, etc. |
| `agent-sdk-dev` | Claude Agent SDK development plugin, with verifier agents for Python and TypeScript apps |
| `plugin-dev` | Toolkit for building custom Claude Code plugins (agents, commands, hooks) |
| `pr-review-toolkit` | Comprehensive PR review agents specializing in comments, deeper than the base `code-review` plugin |
| `mcp-tunnels` | Connect Claude to a private MCP server through an Anthropic MCP tunnel (Docker Compose quickstart) |
| `playground` | Creates interactive HTML playgrounds — self-contained explorers with visual controls, good for demoing an AI feature |
| `session-report` | Session write-ups for standup/handoff during the internship |
| `claude-md-management` | Keep CLAUDE.md current in a fast-moving codebase |
| `code-simplifier` | Simplification/clarity pass on generated code |
| `code-modernization` | If the internship involves modernizing an existing legacy system |
| `ralph-loop` | Continuous self-referential AI loops for iterative development — powerful but use with care (autonomous, can run unattended) |
| `hookify` | Create hooks that prevent unwanted agent behaviors by analyzing conversation patterns |

## Shared / either persona

| Plugin | Description |
|---|---|
| `example-plugin` | Learn the full space of plugin capabilities |
| `skill-creator` | Build a custom skill for a recurring task |
| `claude-code-setup` | Analyzes a codebase and recommends tailored Claude Code automations (hooks, etc.) |

## Not from the marketplace — connected MCP services

These are account-based connectors, not installable plugin files, so there's nothing to copy into this folder. Enable them per-service via Claude's connector settings:

- **Figma** — design-to-code and code-to-design, FigJam diagrams
- **Gamma** — AI-generated presentations/documents (project pitches, intern demos)
- **Railway** — infrastructure provisioning and deployment
- **Jira / Confluence (Atlassian)** — issue tracking and internal docs, mainly the intern's daily workflow
- **Gmail** — reading/drafting email from within Claude
