# CSE Student & AI Intern Toolkit

A curated bundle of Claude Code **skills** and **plugins**, organized for two personas: a **CSE student** (coursework, DSA, projects, hackathons) and an **AI intern** (LLM apps, agents, deployment). Built from what's actually installed/available on this machine's Claude Code setup on 2026-07-14.

## Folder layout

```
CSE-Student-AI-Intern-Toolkit/
├── cse-student/         Skills + plugin picks for coursework, DSA, projects, hackathons
├── ai-intern/           Skills + plugin picks for LLM/agent development on Vercel
├── shared/              Skills & plugins both personas use, plus installed-plugin manifests
└── marketplace-plugins/ Catalog of NOT-yet-installed plugins worth installing, by persona
```

Each `skills/<name>/SKILL.md` file is a **real copy** of a skill Claude Code already runs — pulled from the `superpowers`, `vercel`, and `frontend-design` plugins, plus two standalone user skills (`hackathon-judge-readiness`, `use-railway`). These aren't documentation *about* the skills — they're the actual instruction files Claude follows when the skill is invoked.

## Two kinds of entries here

1. **Already usable, no install needed** — skills belonging to plugins already installed in this Claude Code profile (`superpowers`, `vercel`, `frontend-design`, `code-review`, `security-guidance`, `github`). Just invoke them in a session, e.g. `/systematic-debugging` or asking Claude to use them.
2. **Not installed yet** — cataloged in `marketplace-plugins/README.md` with the exact install command. These live in the `claude-plugins-official` marketplace but aren't active on this machine.

## Quick install reference

```bash
# Inside an interactive Claude Code session:
/plugin marketplace add claude-plugins-official   # already added on this machine
/plugin install <plugin-name>@claude-plugins-official
```

Standalone skills (not part of a plugin) go in `~/.claude/skills/<name>/SKILL.md` — that's where `hackathon-judge-readiness` and `use-railway` already live.

## Also relevant, but not files you can copy

Some capabilities are built directly into Claude Code itself (not plugin files on disk), so there's nothing to copy here — they're just always available:
`code-review`, `simplify`, `verify`, `run`, `init`, `review`, `security-review`, `dataviz`, `artifact-design`, `claude-api`, `loop`, `schedule`, `update-config`, `keybindings-help`, `fewer-permission-prompts`. See `shared/README.md` for what each does and when each persona would reach for it.

Connected MCP services (Figma, Gamma, Railway, Jira/Confluence, Gmail) are external accounts, not local files — see the persona READMEs for which ones matter to whom.
