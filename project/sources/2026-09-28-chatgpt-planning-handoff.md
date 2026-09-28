# AI Handoff: High Fees Not For Me

## Purpose of this document

This handoff gives another AI collaborator the full working context for the **High Fees Not For Me** project. It should be treated as a product-planning brief, not as authorization to build, deploy, configure domains, create accounts, or publish content.

The project owner plans to divide future work between Codex and Claude. Before doing work, identify the specific assignment and avoid duplicating or overwriting work completed by the other AI.

## Current project status

- Status: **Planning and product discovery only**
- No website has been built.
- No GitHub repository has been created.
- No domains have been configured.
- No research agents have been deployed.
- No fee records have been published.
- No newsletter, advertising, registration, or mobile app system exists.
- The owner wants to discuss and approve the architecture and workflows before implementation.

## Project identity

- Working name: **High Fees Not For Me**
- Primary domain: **highfeesnotforme.com**
- Secondary domain: **highfeesnotforme.info**
- Domains were purchased June 10, 2026 through Whois.com.
- Current recommendation: use the `.com` domain as the canonical public address and redirect `.info` to `.com` when the project reaches deployment.

## Product vision

Create an evidence-based consumer platform where people can discover, report, and understand high, unexpected, mandatory, hidden, or poorly disclosed fees added to bills, invoices, receipts, reservations, or purchases.

Examples include:

- Resort and destination fees
- Automatic or forced gratuities
- Service and operations charges
- Facility fees
- Credit-card or payment surcharges
- Delivery, processing, convenience, administrative, or similar added charges

The platform should begin with Florida and may expand to other states later.

The strongest proposed positioning is:

> See the real fees consumers encountered, supported by evidence and reviewed before publication.

The platform should be a moderated, evidence-based registry rather than an unverified complaint board.

## Core principles

1. Nothing submitted or discovered is published automatically.
2. Every public fee entry must be assigned a business category and fee type.
3. Claims should be factual, neutral, and traceable to evidence.
4. The project owner has final approval authority.
5. Uploaded receipts and invoices must be treated as sensitive private evidence.
6. The platform should distinguish a high or objectionable fee from an illegally charged fee.
7. The system should preserve company, location, date, amount, and evidence context.
8. Businesses need a correction or response process.

## Intended product surfaces

### Public responsive website

The first product should be a responsive browser application that works well on desktop and mobile. It may be installable as a Progressive Web App. A separate native iOS/Android application should be considered later, after the reporting workflow is validated.

The public site should include:

- Home page led by the newest verified fee findings
- Browse and search by category, fee type, company, and location
- Company and fee detail pages
- Data Gathering Form for public reports
- Florida and federal law information
- About / founder-story page
- Registration and newsletter subscription in a later phase
- Clearly separated advertising or sponsor areas in a later phase

### Private review center

The owner needs a private workspace to:

- Review researcher discoveries and consumer submissions
- Inspect uploaded evidence
- Review automated receipt extraction
- Request missing information
- Detect duplicates
- Approve, reject, or archive records
- Redact evidence before publication
- Publish approved records
- Handle disputes and corrections
- Approve newsletters before sending
- Review audit history

### Eventual mobile application

The owner wants a mobile experience where people can photograph or upload receipts and describe hidden or additional charges. The recommended sequence is to perfect this workflow in the responsive web application first, then decide whether a native app is justified.

## Data Gathering Form (DGF)

**DGF means Data Gathering Form.** It is the structured form through which a user reports a high or unexpected fee noticed on an invoice, bill, or receipt.

Proposed required fields:

- Business name
- Business location or website
- One of the approved business categories
- Fee name exactly as shown
- Fee amount or percentage
- Transaction date
- When and how the fee was first disclosed
- Whether the fee appeared mandatory
- Expected total
- Final total
- Factual description of the experience
- Receipt, bill, or invoice upload
- Submitter contact email for verification
- Confirmation that the submitter has the right to share the evidence
- Consent to private review, redaction, and permitted publication

The form should not accept an incomplete submission. Evidence upload is mandatory.

The system may compare the stated business, date, fee label, fee amount, and transaction total with extracted receipt data. Mismatches should be flagged for human review rather than automatically rejected or published. Facts such as when a fee was disclosed may not appear on a receipt.

## Recommended taxonomy

Business categories and fee types must be separate.

### Proposed business categories

1. Hotels & Travel
2. Restaurants & Food Delivery
3. Entertainment & Ticketing
4. Retail & Consumer Services
5. Utilities, Telecom & Subscriptions
6. Other

These categories are provisional and require owner approval.

### Example fee types

- Resort or destination fee
- Automatic gratuity
- Service or operations charge
- Facility fee
- Credit-card or payment surcharge
- Delivery fee
- Convenience or processing fee
- Administrative fee
- Regulatory-recovery fee
- Cancellation or termination fee
- Other added charge

Every published observation should have one business category and at least one fee type.

## Company and location model

The owner's initial thought was that only one instance per company should be needed; for example, one Marriott resort-fee entry even if fees vary by location.

Recommended refinement: provide one consolidated public company page while preserving individual, location-specific observations and evidence.

Example:

```text
Marriott
└── Resort/destination fee
    ├── Property A — $35 — observed June 2026
    ├── Property B — $45 — observed July 2026
    └── Property C — $30 — observed August 2026
```

This avoids repetitive results without treating one receipt as proof of a policy at every location.

## Proposed core data entities

- Company
- Location
- Business category
- Fee type
- Fee observation
- Consumer submission
- Evidence asset
- Research source
- Review decision
- Law or regulation
- Company response or dispute
- Registered user
- Subscription
- Newsletter issue
- Audit-history event

An observation should preserve the company, specific location or online channel, fee label, amount or percentage, transaction date, disclosure timing, source, evidence, review status, and last verification date.

## Submission and publishing workflow

```text
Research-agent discovery or consumer submission
                    ↓
             Private intake queue
                    ↓
       Security scan and privacy screening
                    ↓
     Receipt extraction and duplicate matching
                    ↓
       Evidence and source-quality review
                    ↓
           Legal/editorial risk review
                    ↓
              Owner final approval
                    ↓
       Published company/location observation
                    ↓
        Corrections, disputes, and rechecks
```

Suggested statuses:

- New
- Needs information
- Under review
- Verified
- Approved for publication
- Published
- Disputed
- Outdated
- Rejected
- Archived

Only the owner, or a moderator explicitly authorized by the owner, should move a record into approved or published status.

## Receipt and evidence safeguards

Receipts, invoices, and bills may reveal names, addresses, card digits, loyalty numbers, reservation numbers, account numbers, QR codes, barcodes, and location metadata.

Recommended safeguards:

- Restrict accepted file types and sizes.
- Scan uploads for unsafe content.
- Encrypt original evidence.
- Remove image metadata where appropriate.
- Detect and redact personal, payment, and account information.
- Keep originals private by default.
- Publish only a redacted excerpt or image when appropriate.
- Maintain a review and access audit trail.
- Define retention and deletion policies.
- Obtain clear submitter consent.
- Provide correction, removal, and dispute procedures.

The owner must decide whether the public sees redacted receipt evidence or only a notice that evidence was privately verified.

## Research-agent concept

The owner wants an AI agent that searches for hidden or additional fees, starting in Florida.

The research agent should create review candidates, never publish autonomously. Potential source types include:

- Official company booking and checkout pages
- Official menus and ordering pages
- Published terms, rate disclosures, and fee schedules
- Government rules and enforcement actions
- Consumer-submitted receipts
- Reputable reporting used as a lead rather than final proof

Each discovery should preserve:

- Source URL or evidence identifier
- Capture date
- Exact fee language
- Amount or percentage
- Business category
- Fee type
- Company
- Location or geographic scope
- Disclosure context
- Confidence score
- Missing information
- Recheck date

## Controlled agent-review loop

The owner requested a loop through which the agent can review and improve its work. The safe interpretation is a controlled quality loop, not self-modifying production software.

Recommended loop:

1. Search
2. Extract
3. Classify
4. Match companies and detect duplicates
5. Critique the sufficiency of evidence
6. Identify missing or contradictory information
7. Revisit weak or outdated records
8. Place the candidate in the private review queue

Prompt, classification, workflow, or code changes should be proposed, tested against a fixed evaluation set, and human-approved before release.

## Agent memory

Agent memory should be implemented as structured, auditable records rather than unbounded conversational memory. Every remembered claim should link to its source, evidence, review history, and current status. The system should be able to revisit stale records without treating past conclusions as permanent truth.

## Proposed five-agent review council

The owner requested multiple agents and a five-member council that monitors its own work, including one agent knowledgeable about state and federal fee laws.

Recommended council:

1. **Researcher** — discovers candidates and gathers sources.
2. **Evidence Critic** — challenges whether evidence actually supports each claim.
3. **Legal Monitor** — tracks relevant federal and state requirements and flags unsupported legal conclusions.
4. **Editor and Taxonomist** — normalizes company names, categories, fee types, and public wording.
5. **Quality and Operations Reviewer** — checks privacy, duplicates, stale sources, broken links, and workflow health.

The council may record disagreements but cannot publish by vote. The owner retains final approval.

The requested customer-service, lead-architect, developer, tester, project-manager, and web-design roles should be treated separately:

- Architect, developer, tester, designer, and project manager are product-development roles.
- Customer service becomes an operational workflow when public submissions and company disputes begin.
- These roles do not need to be persistent content-review agents during the first version.

## Legal-information approach

The owner wants federal and state laws concerning hidden, forced, or additional fees mentioned on the home page.

Recommended approach:

- Put a concise “Know the rules” summary on the home page.
- Link it to a dedicated, dated legal-information library.
- Store jurisdiction, industries covered, effective date, current status, plain-language summary, official source, last-review date, and reviewer for each entry.
- Clearly state that the material is informational and is not legal advice.
- Do not call a fee illegal, fraudulent, or a scam without an authoritative ruling or qualified legal review.

Important research already identified during planning:

- The FTC Rule on Unfair or Deceptive Fees became effective May 12, 2025 and covers live-event tickets and short-term lodging. It generally requires upfront display of a total price that includes mandatory fees; it does not broadly prohibit fees.
- Florida expanded restaurant operations-charge disclosure requirements effective July 1, 2026. Covered charges include service charges, automatic gratuities, credit-card surcharges, and delivery fees, with prescribed disclosure and receipt requirements.
- Florida's credit-card surcharge statute and its enforcement history are legally nuanced and should not be simplified into a claim that all credit-card surcharges are illegal.

All legal information must be reverified against current official sources before publication. A qualified attorney should review the site's legal summaries, moderation rules, terms, privacy practices, and defamation risk before public launch.

## Public language and editorial standards

Prefer neutral formulations such as:

- “A consumer submitted evidence showing…”
- “The receipt listed a 20% operations charge…”
- “The fee was reported as mandatory…”
- “Evidence reviewed on [date].”

Avoid unsupported conclusions such as:

- “This company scams customers.”
- “This fee is illegal.”
- “Every location charges this fee.”

Public records should distinguish:

- Observed fee
- Disclosure timing
- Whether the charge appeared mandatory
- Evidence status
- Applicable legal information
- Whether the company responded

## Home page direction

The main page should focus on the newest verified findings. Proposed sections:

1. Mission and search
2. Latest verified findings
3. Browse by business category
4. Common fee types
5. Report a fee through the DGF
6. Concise legal-information cards
7. Newsletter invitation
8. Clearly labeled future sponsor placement

The legal library and founder biography should be separate pages rather than crowding the main feed.

## Founder-story page

The owner wants a separate page explaining:

- Who they are
- Why they oppose high or hidden fees
- What they first noticed
- When they noticed it
- How the practice spread
- How one company or category adopts a fee and competitors follow
- The hotel resort-fee example
- How the problem might be resolved
- What consumers, businesses, and lawmakers can do

The biography should not be drafted as fact until the owner answers:

1. What first hidden or unexpected fee made the issue personal?
2. Where and approximately when did it happen?
3. What was the fee and when was it disclosed?
4. What did the business say when questioned?
5. When did the owner realize the issue was broader than one experience?
6. What outcome does the owner most want the project to create?
7. What personal or professional background may be shared publicly?
8. Should the page use the owner's real name and photograph, or emphasize the mission with limited personal information?

## Registration and subscriptions

The owner wants users to register and subscribe. Recommended separation:

- A site account is used for submission history, saved items, and future participation.
- Newsletter subscription is a separate, explicit consent.
- Email ownership should be verified.
- Users must be able to unsubscribe.
- The first public reporting experience should not necessarily require a full account if that would prevent useful reports; this remains an owner decision.

## Monthly newsletter workflow

The newsletter should report newly published findings and must be approved by the owner before sending.

```text
Approved findings for the month
→ AI-assisted newsletter draft
→ owner review and edits
→ test email
→ explicit owner approval
→ scheduled send
→ delivery and unsubscribe records
```

No newsletter should be sent autonomously.

## Advertising and sponsorship

The owner wants advertising and sponsor space that may eventually generate revenue.

Recommended safeguards:

- Clearly label every advertisement or sponsorship.
- Sponsors cannot influence verification, publication, corrections, or removal.
- A company should not sponsor its own listing or category page.
- Sponsored content must be visually and editorially distinct from findings.
- Ads must not resemble official fee warnings.
- Publish an editorial-independence policy.
- Design future placements early, but delay active monetization until the site has useful content, traffic, and trust policies.

## Recommended delivery phases

### Phase 0: Product and policy definition

- Approve the mission and scope of “high,” “hidden,” “mandatory,” and “poorly disclosed.”
- Finalize business categories and fee types.
- Define evidence standards and publication rules.
- Define privacy, retention, correction, and dispute policies.
- Obtain appropriate legal review.
- Complete the founder interview.

### Phase 1: Florida research and private review

- Create the core records and private workflow.
- Introduce research candidates in a controlled intake queue.
- Seed a small, high-quality Florida dataset.
- Validate OCR, duplicate detection, categorization, and privacy redaction.
- Keep records private until the process is reliable.

### Phase 2: Public responsive website

- Latest findings home page
- Browse, search, and company pages
- Fee-observation detail pages
- DGF and evidence upload
- Legal-information library
- Founder-story page
- Owner-controlled publication workflow

### Phase 3: Accounts and newsletter

- Registration and authentication
- Submission history
- Saved categories or companies
- Verified newsletter subscriptions
- Owner-approved monthly newsletter
- Company response and correction process

### Phase 4: Expansion and monetization

- Additional states
- Native mobile applications if usage supports them
- Advertising and sponsorship
- Additional human moderators
- Aggregate trend reports and public statistics

## Important unresolved product decisions

The owner has not yet answered these questions:

1. Does the site cover fees that were not disclosed early enough, fees considered unreasonably high, or both?
2. Should a properly disclosed but objectionably high fee be published?
3. Are submitter identities always private from the public?
4. Are companies invited to respond before publication, after publication, or only after a dispute?
5. Does the public see redacted evidence or only a private-verification statement?
6. Are the six proposed categories approved?
7. Must a person create an account before submitting a DGF?
8. What minimum evidence qualifies a research-agent discovery for human review?
9. What was meant by “Harness” in the original notes: a particular product, an agent-control system, or a general orchestration concept?
10. Who besides the owner may eventually approve publication?

## Recommended early product decisions

- Use `highfeesnotforme.com` as the canonical domain.
- Begin with a responsive web application/PWA, not separate web and native implementations.
- Start with Florida.
- Separate business categories from fee types.
- Use consolidated company pages backed by location-specific observations.
- Require evidence for consumer submissions.
- Never publish agent discoveries or consumer reports automatically.
- Keep original receipts private and redact evidence before any public display.
- Let the owner approve all publications and newsletters.
- Use controlled evaluation and human-approved updates instead of agent self-modification.
- Delay advertising and native apps until the core evidence workflow is credible.

## Coordination instructions for AI collaborators

When Codex and Claude share this project:

1. Each AI should receive a specific assignment with clear file or topic ownership.
2. Read this handoff and inspect existing work before proposing changes.
3. Do not silently change agreed terminology, taxonomy, workflows, or policy.
4. Record assumptions and unresolved decisions.
5. Keep legal claims linked to current official sources.
6. Do not add real allegations or company entries without evidence and owner approval.
7. Do not use real uploaded receipts in development fixtures.
8. Use synthetic sample data until the evidence-handling system is approved.
9. Do not create infrastructure, publish, deploy, configure domains, or send email without an explicit assignment.
10. At the end of each assignment, leave a concise handoff describing decisions, files changed, tests performed, risks, and next steps.

## Suggested next assignment

The next useful step is not coding. It is a short product-definition session with the owner to resolve the ten open decisions, complete the founder interview, and approve the evidence and publication policy. From those answers, an AI can prepare a version-one product requirements document, data model, page map, moderation policy, and phased implementation plan for approval.
