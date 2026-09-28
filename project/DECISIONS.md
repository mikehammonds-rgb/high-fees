# Decisions

_Append-only. Newest at the bottom. To reverse a decision, add a new one that supersedes it._

### D1 — 2026-09-28 — The repo is the single source of truth

Every AI working here (Claude, ChatGPT/Codex, others) reads and writes project state in the repo,
not in its own chat memory. Rules in `AGENTS.md`; `CLAUDE.md` just points to it.
**Why:** so any agent can pick up where another left off.

### D2 — 2026-09-28 — Branch + PR per session; Mike merges

Agents never commit to `main`. Branch name `<agent>/<topic>`.
**Why:** prevents two agents overwriting each other and gives Mike a review point.

### D3 — 2026-09-28 — Host on GitHub Pages, publish `site/`

A GitHub Actions workflow deploys `site/` on every push to `main`.
**Why:** free, no extra accounts, cloud-only. **Revisit if** the brief needs server-side features
(accounts, form storage, a database) — then consider Vercel or Netlify.

### D4 — 2026-09-28 — Plain HTML/CSS/JS, no build step

**Why:** any agent can edit it without installing anything or knowing a framework's conventions.
**Revisit if** the site grows past a handful of pages or needs shared components.

### D5 — 2026-09-28 — Drive holds binaries and raw research only

Google Drive folder "High Fees website" is for large files and source material. Anything an agent
needs to act on gets copied into the repo.
**Why:** not every AI tool can read Drive; all of them can read the repo.
