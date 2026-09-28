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
9. What did "Harness" mean in the original notes?
10. Who besides Mike may eventually approve publication?

New:

- **This repo is public.** Anything committed, including the founder story, plans, and notes, is
  visible to anyone and stays in git history. OK to keep it public? (Free GitHub Pages needs a public
  repo. Keeping the repo private needs a paid GitHub plan or a different host.)
- Did the Whois.com purchase include a hosting plan? If so, it may not be needed (see D6).

## Known issues

- GitHub Pages must be enabled (Settings → Pages → Source: GitHub Actions) before the deploy
  workflow can succeed.
- Domain renewal: both domains were bought 2026-06-10. Check the renewal date and auto-renew in
  Whois.com so they don't lapse.
- The legal facts in the source doc (FTC fee rule, Florida restaurant operations-charge law, Florida
  card-surcharge statute) have **not been re-verified** in this repo. Don't publish them until they're
  checked against official sources.
