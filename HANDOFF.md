# HANDOFF — current state

_Snapshot, not history. Rewrite it at the end of every session. History goes in `project/LOG.md`._

**Last updated:** 2026-09-28 · **By:** Claude (Code) · **Branch:** claude/epic-gates-w8c84y

## Where things stand

- **Phase 0: planning only.** Nothing has been designed or built. The only published content is a
  "Coming soon" placeholder page.
- Mike's earlier ChatGPT planning is in the repo at
  `project/sources/2026-09-28-chatgpt-planning-handoff.md` and summarized in `project/BRIEF.md`.
  The concept: a moderated, evidence-based registry of high or hidden consumer fees, starting in
  Florida. Most of that doc is **recommendations Mike hasn't approved yet**. Don't treat them as decisions.
- That doc was written before this repo existed. Where it says "no GitHub repository", it is out of date.
- Mike owns `highfeesnotforme.com` and `highfeesnotforme.info` (Whois.com, bought 2026-06-10).
  Not connected yet; the plan is in D6.

## In progress

- Nothing.

## Next steps (in order)

1. **Product-definition session with Mike:** answer the open questions below and the founder
   interview (section "Founder-story page" in the source doc). Record answers in `BRIEF.md` / `DECISIONS.md`.
2. **Architecture decision.** D3/D4 (static GitHub Pages, no build step) can't support the DGF,
   evidence uploads, the private review center, accounts, or the newsletter. Those need a backend,
   a database, private file storage, and login. Decide whether:
   - (a) the static site is only for the Phase 2 prototype (public pages with synthetic sample data),
     and the backend is chosen later, or
   - (b) the backend is chosen now.
   Record the choice as a new decision that supersedes D3/D4 where needed.
3. From those answers: v1 requirements, data model, page map, moderation and evidence policy,
   phased implementation plan. All go to Mike for approval.
4. Prototype public pages in `site/` with **synthetic** data only.
5. After the prototype: connect `www.highfeesnotforme.com` per D6.

## Questions for Mike

From the ChatGPT planning (still unanswered):

1. Does the site cover fees disclosed too late, fees that are unreasonably high, or both?
2. Should a properly disclosed but objectionably high fee be published?
3. Are submitters always anonymous to the public?
4. Do companies get to respond before publication, after, or only after a dispute?
5. Does the public see redacted evidence, or only a "privately verified" statement?
6. Are the six proposed business categories approved?
7. Must someone create an account before submitting a DGF?
8. What minimum evidence qualifies a research-agent discovery for human review?
9. ~~What did "Harness" mean?~~ **Answered by Mike's notes:** "Harness" is the heading over
   "loop to review and fix", "tools it can connect to", and "memory". So it means the setup the
   research agent runs inside (its loop, tools, and memory), not a specific product. Mike to confirm.
10. Who besides Mike may eventually approve publication?

## Where the ChatGPT plan differs from Mike's notes (Mike decides)

Mike's notes are in `project/sources/mike-original-idea-notes.md`. ChatGPT changed these items;
Claude's view is in brackets.

- **Receipt must match the description.** Notes: "must match". ChatGPT: flag mismatches for human
  review instead of auto-rejecting, because some facts (e.g. when the fee was disclosed) aren't on a
  receipt. [Agree with ChatGPT.]
- **One instance per company.** Notes: one entry per company, "fees may vary". ChatGPT: one company
  page with each location's fee listed underneath. [Agree; it keeps your idea and doesn't imply every
  location charges the same.]
- **Agent loop "fix anything itself".** ChatGPT: the agent can improve its own findings in the
  private queue, but changes to its own instructions or code need testing and your approval.
  [Agree. A self-changing agent making claims about real businesses is a legal risk.]
- **Categories.** Notes name 4 (Hotels, Restaurants, Stores, Utilities) + "Other". ChatGPT added
  Entertainment & Ticketing as the 5th. [Reasonable: the FTC fee rule covers tickets and lodging.
  But it's your call.]
- **Browser and mobile versions.** Notes: both. ChatGPT: one mobile-friendly website first, native
  app later. [Agree; one codebase until the reporting flow is proven.]
- **Ads.** Notes: create ad/sponsor space. ChatGPT: design the space now, sell it later.
  [Agree; ads next to unproven claims about companies hurt credibility.]
- **Agents list.** Notes list 8 roles. ChatGPT: the 5-member council reviews content; architect,
  developer, tester, PM, and designer are building roles. [Agree. In practice, Claude and Codex fill
  the building roles.]
- **Research agent built "using Codex".** Recorded as a preference, not yet a decision. It needs a place
  to run and pays per use for AI and search (see Known issues).

## Other questions

- **This repo is public.** Anything committed, including the founder story, plans, and notes, is
  visible to anyone and stays in git history. OK to keep it public? (Free GitHub Pages needs a public
  repo. Keeping the repo private needs a paid GitHub plan or a different host.)
- Did the Whois.com purchase include a hosting plan? If so, it may not be needed (see D6).

## Known issues

- GitHub Pages must be enabled (Settings → Pages → Source: GitHub Actions) before the deploy
  workflow can succeed.
- Domain renewal: both domains were bought 2026-06-10. Check the renewal date and auto-renew in
  Whois.com so they don't lapse.
- **Running cost.** The research agent and council use paid AI/search services every time they
  run. No budget is set yet. Needed before building them.
- The legal facts in the source doc (FTC fee rule, Florida restaurant operations-charge law, Florida
  card-surcharge statute) have **not been re-verified** in this repo. Don't publish them until they're
  checked against official sources.
