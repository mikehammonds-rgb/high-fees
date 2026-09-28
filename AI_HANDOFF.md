# AI HANDOFF — High Fees Not For Me

**Every AI (Claude, Codex, ChatGPT, any other) reads this file first and updates it last.**
It is the one shared handoff doc. It's a snapshot of *now*, not a history (history goes in
`project/LOG.md`). Full rules are in `AGENTS.md`.

- **Start of a session:** read this whole file before doing anything. Then tell Mike in 2–3 lines
  what you understand the state to be and what you plan to do.
- **End of a session:** rewrite this file so it's true right now: update the date/agent line,
  "Where things stand", "Decisions so far", next steps, and questions. Then add a
  `project/LOG.md` entry. **A session that doesn't update this file isn't finished.**
- **AI that can't edit the repo** (e.g. ChatGPT chat): at the end, output the full updated
  `AI_HANDOFF.md` (and a LOG entry) for Mike to hand to Claude or Codex to commit.

**Last updated:** 2026-09-28 · **By:** Claude (Code) · **Branch:** claude/epic-gates-w8c84y (PR #1 merged; this end-of-day update is PR #2)

## Reminders for Mike (AIs: mention any open ones at the start of each session)

- [ ] **Privacy Protection** on both domains in the Whois.com Control Panel (manage.whois.com, then the
      domain, then Privacy Protection). It's about $2 pro-rata to 2027-06-10. At checkout, make sure it's
      privacy protection and not a pricier "Domain Protect+" bundle.
- [ ] **Merge the open PR** from the last session before starting with another AI.
- [x] Domain renewal reminder: yearly Google Calendar reminder on June 1 (domains expire June 10).

## What this is (one paragraph)

A moderated, evidence-based registry of add-on fees consumers run into (resort fees, forced
gratuities, service/operations charges, card surcharges, and the like), starting in Florida.
Fees come from research (official sources) and from user reports with a receipt. Nothing goes public
until Mike approves it. Details: `project/BRIEF.md`.

## Where things stand

- **Phase 0: planning only.** Nothing has been designed or built. The only published content is a
  "Coming soon" placeholder page.
- Background material, read-only: Mike's original notes (`project/sources/mike-original-idea-notes.md`)
  and the earlier ChatGPT planning doc (`project/sources/2026-09-28-chatgpt-planning-handoff.md`).
  That ChatGPT doc was the first handoff. **This file replaces it**; don't update the old one.
- Mike owns `highfeesnotforme.com` and `highfeesnotforme.info` (Whois.com, bought 2026-06-10, renew 2027-06-10).
  Domain only, with no hosting plan, which is what D6 needs (GitHub Pages hosts for free).
  Not connected yet.

## Decisions so far (full text in `project/DECISIONS.md`)

- D1 The repo is the single source of truth. D2 Branch + PR per session; Mike merges.
- D3/D4 Static site on GitHub Pages, plain HTML/CSS/JS, no build step (being revisited, see next steps).
- D5 Google Drive only for large files and raw material.
- D6 After the prototype, `www.highfeesnotforme.com` is the main address; `.info` forwards to it.
- D7 The ChatGPT planning doc is reference material; Mike's notes win any conflict.
- D8 No paid, automated AI for now: no research agent, council, or AI receipt reading. Research
  happens in Claude/Codex sessions, and the council is a checklist.
- D9 Product answers:
  - Scope: add-on fees beyond the listed price, including buried "disclosed" ones.
  - Submitters choose anonymous (default) or shown.
  - Companies respond only by dispute; every entry has a dispute link.
  - Public proof is a cropped fee line plus the review date.
  - Categories: Hotels · Restaurants · Food Delivery & Apps · Stores · Utilities ·
    Travel & Transportation · Home & Personal Services · Other.
  - An account is required to submit.
  - Research needs an official source, date, and screenshot.
  - Only Mike approves publication.
- D10 `AI_HANDOFF.md` is the one handoff doc; every AI reads it first and updates it last.
- D11 How the 6 notes-vs-ChatGPT differences were settled:
  - Receipt mismatches are flagged for Mike, not auto-rejected.
  - One company page with each location's fee listed underneath.
  - A mobile-friendly site first; an app-store app later.
  - Ad spots are designed now but stay empty for now.
  - An AI may fix only its own unpublished findings.
  - Council checklist for content; Claude and Codex do the building; customer service is Mike's inbox.
- D12 About page: first name + Tampa only; text approved in `project/content/about.md`.

## In progress

- Nothing. Session ended 2026-09-28 at Mike's request. **Start next session with next step 1.**

## Next steps (in order)

1. **Architecture decision** (Claude's recommendation for Mike to confirm: prototype the public
   pages as a free static site with synthetic data first, then pick a free-tier service for
   accounts, the database, and uploads before building the DGF). D3/D4 (static GitHub Pages, no build step) can't support the DGF,
   evidence uploads, the private review center, required accounts (D9), or the newsletter. Those need a backend,
   a database, private file storage, and login. Decide whether:
   - (a) the static site is only for the Phase 2 prototype (public pages with synthetic sample data),
     and the backend is chosen later, or
   - (b) the backend is chosen now.
   Record the choice as a new decision that supersedes D3/D4 where needed.
2. From those answers: v1 requirements, data model, page map, moderation and evidence policy,
   phased implementation plan. All go to Mike for approval.
3. Prototype public pages in `site/` with **synthetic** data only.
4. After the prototype: connect `www.highfeesnotforme.com` per D6.

## Questions for Mike

The 10 product questions (D9), the 6 notes-vs-ChatGPT differences (D11), and the founder interview
(D12) are done. Still open:

- The architecture decision (next steps, item 1).

## Other questions

- **This repo is public.** Anything committed, including the founder story, plans, and notes, is
  visible to anyone and stays in git history. OK to keep it public? (Free GitHub Pages needs a public
  repo. Keeping the repo private needs a paid GitHub plan or a different host.)

## Known issues

- GitHub Pages must be enabled (Settings → Pages → Source: GitHub Actions) before the deploy
  workflow can succeed.
- **Domain renewal: both domains renew 2027-06-10** (confirmed by Mike). Auto-renew isn't in the obvious places in
  the Whois.com panel. Mike has a yearly calendar reminder to renew on June 1. Privacy Protection was off on the .com. Mike is reviewing the ~$2 pro-rata option; check
  it's on for both domains.
- `project/content/about.md` has one `[VERIFY]` sentence (FTC fee rule). Check it before the page goes live.
- The legal facts in the source doc (FTC fee rule, Florida restaurant operations-charge law, Florida
  card-surcharge statute) have **not been re-verified** in this repo. Don't publish them until they're
  checked against official sources.
