# AGENTS.md — rules for any AI working in this repo

This project is worked on by more than one AI (Claude, ChatGPT/Codex, possibly others) and by Mike.
Nothing lives in any one tool's memory. **The repo is the memory.** If it isn't written here, the next
agent won't know it.

## 1. Start of every session (read in this order)

1. `HANDOFF.md` — current state, what's in progress, what's next. Always read first.
2. `project/BRIEF.md` — what the site is and who it's for.
3. `project/DECISIONS.md` — decisions already made. Don't reopen them without saying why.
4. The last ~10 entries of `project/LOG.md`.

Then tell Mike, in two or three lines, what you understand the current state to be and what you plan
to do. If `HANDOFF.md` and the code disagree, trust the code and flag the mismatch.

## 2. While working

- **Branch per session.** Never commit to `main` directly. Use `<agent>/<short-topic>`,
  e.g. `claude/pricing-table`, `codex/fee-calculator`. Open a pull request; Mike merges.
- **One agent per branch.** Don't push to another agent's branch. Start a new one from `main`.
- **Small PRs.** One purpose per PR. Title says what changed; body says why and how to check it.
- **No tool-specific magic.** Plain HTML/CSS/JS in `site/` unless `DECISIONS.md` says otherwise.
  No build step until one is decided and recorded.
- **No secrets in the repo.** No API keys, tokens, or personal data. Ever.
- **Ask, don't guess, on product questions.** Put open questions in `HANDOFF.md` under
  "Questions for Mike" instead of inventing an answer.

## 3. End of every session (required — this is the handoff)

Before your final commit on the branch:

1. **Rewrite** `HANDOFF.md` so it reflects reality right now (it's a snapshot, not a history).
2. **Append** one entry to the top of `project/LOG.md` using the template there.
3. If you made a decision that future agents must respect, **add** it to `project/DECISIONS.md`.
4. In the PR body, include: what changed, how to check it, what's next.

A session that doesn't update `HANDOFF.md` isn't finished.

## 4. Repo layout

```
AGENTS.md            ← these rules (canonical; tool files point here)
CLAUDE.md            ← pointer for Claude Code
HANDOFF.md           ← current state + next steps (snapshot)
project/BRIEF.md     ← the idea, audience, goals
project/DECISIONS.md ← decision log (append-only)
project/LOG.md       ← session log (newest first)
site/                ← the website; this folder is what gets published
.github/workflows/   ← GitHub Pages deploy (publishes site/ on push to main)
```

## 5. Where other things live

- **Code, specs, decisions, handoff:** this repo. Always.
- **Large binaries, raw research, image originals:** Google Drive folder "High Fees website".
  If an agent needs something from Drive to do its work, copy the relevant text or the
  final optimized asset into the repo and note where it came from.

## 6. Conventions

- Dates: `YYYY-MM-DD`. Times: US Eastern.
- Markdown for all docs. Keep lines readable; no giant tables of generated text.
- Accessibility and mobile-first are defaults, not extras.
