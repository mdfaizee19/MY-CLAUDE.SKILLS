# AI Intern — Skills & Plugins

For building and shipping LLM-powered features: chatbots, agents, RAG, tool-calling, deployed on Vercel.

## Skills included here (copied, ready to use)

All from the already-installed `vercel` plugin, plus overlapping `superpowers` skills and `use-railway`.

| Skill | Use it for |
|---|---|
| [`ai-sdk`](skills/ai-sdk/SKILL.md) | Building with the Vercel AI SDK — chat UIs, streaming, tool calling, structured output, embeddings |
| [`ai-gateway`](skills/ai-gateway/SKILL.md) | Routing across model providers, fallbacks, cost tracking through one API |
| [`vercel-agent`](skills/vercel-agent/SKILL.md) | AI-powered code review and production incident investigation |
| [`vercel-functions`](skills/vercel-functions/SKILL.md) | Serverless/Fluid Compute functions backing your AI features |
| [`vercel-sandbox`](skills/vercel-sandbox/SKILL.md) | Running untrusted or AI-generated code safely in an isolated microVM |
| [`workflow`](skills/workflow/SKILL.md) | Durable, resumable multi-step agent workflows (retries, pause/resume) |
| [`vercel-connect`](skills/vercel-connect/SKILL.md) | Scoped OAuth to third-party APIs/MCP servers from your agent |
| [`vercel-storage`](skills/vercel-storage/SKILL.md) | Blob storage, Edge Config, Postgres/Redis via the Marketplace |
| [`deployments-cicd`](skills/deployments-cicd/SKILL.md) | Deploy, promote, roll back; CI workflow setup |
| [`env-vars`](skills/env-vars/SKILL.md) | Managing secrets/config across environments |
| [`vercel-cli`](skills/vercel-cli/SKILL.md) | Everything from the terminal — logs, env, deploys, domains |
| [`nextjs`](skills/nextjs/SKILL.md) | App Router architecture for the app hosting your AI features |
| [`react-best-practices`](skills/react-best-practices/SKILL.md) | Quality pass after editing chat/agent UI components |
| [`shadcn`](skills/shadcn/SKILL.md) | Fast, consistent UI components for chat interfaces and dashboards |
| [`verification`](skills/verification/SKILL.md) | End-to-end check: browser → API → data → response, before calling a feature done |
| [`marketplace`](skills/marketplace/SKILL.md) | Installing databases/auth/other integrations without hand-rolled infra |
| [`writing-skills`](skills/writing-skills/SKILL.md) | Packaging internal know-how as a reusable Claude skill for the team |
| [`dispatching-parallel-agents`](skills/dispatching-parallel-agents/SKILL.md) / [`subagent-driven-development`](skills/subagent-driven-development/SKILL.md) | Splitting independent eval/build tasks across subagents |
| [`systematic-debugging`](skills/systematic-debugging/SKILL.md) | Debugging flaky model output or tool-call failures methodically |
| [`test-driven-development`](skills/test-driven-development/SKILL.md) | Writing evals/tests before wiring up a new tool or agent behavior |
| [`use-railway`](skills/use-railway/SKILL.md) | Alternative deploy target for backend services outside Vercel |

## Built into Claude Code already (no file to copy, just use them)

- **`security-review`** — run before shipping anything that takes untrusted input into a prompt (prompt injection surface)
- **`code-review`** / **`simplify`** / **`verify`** — PR-quality passes
- **`claude-api`** — canonical reference for Anthropic API/SDK details (model IDs, pricing, tool use, MCP, caching)
- **`dataviz`** — eval dashboards, latency/cost charts
- **`loop`** / **`schedule`** — recurring checks (e.g. poll a deploy, rerun an eval suite on a cadence)

## Marketplace plugins worth installing (not yet on this machine)

See [`../marketplace-plugins/README.md`](../marketplace-plugins/README.md) for the full catalog. Most relevant to an AI intern:

- `mcp-server-dev` — designing/building MCP servers that work well with Claude
- `agent-sdk-dev` — Claude Agent SDK scaffolding and verification agents (Python/TS)
- `plugin-dev` — building custom Claude Code plugins for the team
- `pr-review-toolkit` — deeper PR review agents beyond the base `code-review` plugin
- `mcp-tunnels` — expose a private MCP server to Claude through a secure tunnel
- `playground` — spin up an interactive HTML playground to demo a feature
- `session-report` — write up what an agent session actually did, for standup/handoff
- `claude-md-management` — keep the repo's CLAUDE.md current as the codebase grows fast

## Connected services relevant to you

- **Jira / Confluence** — ticket tracking and internal docs during the internship
- **Gmail** — drafting/searching work email from Claude
- **Railway** — quick backend/service deploys outside the primary Vercel pipeline
- **Figma** — pulling design context into code for the UI you're shipping
