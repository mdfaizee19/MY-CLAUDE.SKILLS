# Shared — used by both personas

## Installed plugins (manifests copied in `installed-plugins/`)

These are already active in this Claude Code profile — nothing to install.

| Plugin | What it does |
|---|---|
| [`superpowers`](installed-plugins/superpowers/README.md) | Core skills library: TDD, systematic debugging, brainstorming, planning, git worktrees, code review workflow — the source of most `cse-student/` and half of `ai-intern/` skills |
| [`vercel`](installed-plugins/vercel/README.md) | Build and deploy web apps and agents on Vercel — source of all `ai-intern/` Vercel skills |
| [`frontend-design`](installed-plugins/frontend-design/README.md) | UI/UX implementation guidance |
| [`code-review`](installed-plugins/code-review/README.md) | Automated PR review with multiple specialized agents and confidence-based scoring |
| [`security-guidance`](installed-plugins/security-guidance/README.md) | Pattern-based security warnings on edits, generated code |
| [`github`](installed-plugins/github/plugin.json) | Official GitHub MCP server — issues, PRs, code review, repo search from Claude directly |

## Built into Claude Code itself (always available, no plugin needed)

| Skill | What it does | Who reaches for it |
|---|---|---|
| `code-review` | Reviews the current diff for bugs and cleanup opportunities | Both |
| `simplify` | Applies reuse/simplification/efficiency cleanups | Both |
| `verify` | Exercises a change end-to-end to confirm it actually works | Both |
| `run` | Launches the app and drives it in a browser | Both |
| `init` | Bootstraps a CLAUDE.md for a new repo | Both |
| `review` | Reviews a GitHub PR | Both |
| `security-review` | Full security review of pending changes | Both, more critical for the intern |
| `dataviz` | Chart/graph/dashboard design guidance | Both |
| `artifact-design` | Design guidance for Claude Artifacts | Both |
| `claude-api` | Reference for Claude API/SDK usage, pricing, model IDs | Mostly the intern |
| `loop` | Runs a prompt/command on a recurring interval | Mostly the intern (polling deploys, evals) |
| `schedule` | Cron-style scheduled cloud agents | Mostly the intern |
| `update-config` | Configures the Claude Code harness (hooks, permissions, env vars) | Whoever owns the repo's `.claude/settings.json` |
| `keybindings-help` | Customize Claude Code keyboard shortcuts | Either, personal preference |
| `fewer-permission-prompts` | Reduces repeat permission prompts by allowlisting safe commands | Either, quality-of-life |

## Why some things aren't files in this folder

Anything in the table above lives inside the Claude Code application itself, not as a `SKILL.md` on disk in this profile — there's no file to meaningfully copy. They're always available regardless of this toolkit folder; it's here purely as a reference for what to reach for.
