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

### D6 — 2026-09-28 — Custom domain after the prototype: `www.highfeesnotforme.com`

Mike owns `highfeesnotforme.com` and `highfeesnotforme.info` (registrar: Whois.com, bought 2026-06-10).
Until the prototype is ready, the site stays on the default GitHub Pages URL. Then:

- **Primary:** `www.highfeesnotforme.com`, set as the Pages custom domain; the bare `highfeesnotforme.com`
  redirects to it. DNS is changed at Whois.com.
- **`.info`:** forwards to the `.com` at the registrar. It is not a second copy of the site
  (Pages serves one custom domain per repo).
- Don't connect the domain before Mike says the prototype is ready: once DNS points at Pages,
  every push to `main` is live on the real domain.

**Why:** keeps free, automatic Pages deploys (D3) while using Mike's domain. **Revisit if** D3 is
revisited (the brief needs a server) — then the domain points at the new host instead.

### D7 — 2026-09-28 — ChatGPT planning is reference material, not decisions

Mike's ChatGPT planning is kept verbatim in `project/sources/2026-09-28-chatgpt-planning-handoff.md`
and summarized in `BRIEF.md`. Mike's own notes (`project/sources/mike-original-idea-notes.md`) outrank
it where they differ. Its "recommended" items stay proposals until Mike approves them and
they are recorded here. Its coordination rules are folded into `AGENTS.md` §2a.
**Why:** one set of rules and one state file for every AI; avoid treating suggestions as settled.

### D8 — 2026-09-28 — No paid, automated AI for now

Mike: "scratch the paid AI part". Nothing is built that calls pay-per-use AI or search services:
no scheduled research agent, no automated 5-member council, no AI receipt reading.
Instead, for now:

- **Research** happens in normal working sessions with Claude or Codex, using Mike's existing
  subscriptions. Findings go to the private review folder as candidates; Mike approves as before.
- **The council** becomes a written review checklist (researcher, evidence critic, legal monitor,
  editor/taxonomist, quality/privacy), applied in those sessions and by Mike.
- **Receipts** are checked by Mike by eye (or later by free, non-AI tools).

**Why:** no running costs until the idea is proven. **Revisit if** manual research can't keep up
or submission volume grows. Any paid service needs Mike's OK and a budget first.
