# Recommended strategy

Decision date: 2026-09-29. All demand, effort and acquisition estimates are hypotheses to test. This is a product-discovery plan, not a claim of product-market fit.

## Decision

Build one coherent product after a two-week validation sprint. The leading hypothesis is **GuildBrief: event decisions and executive handoffs for small Discord-based clubs and esports teams**. The backup is an **upload-first learning-page QA engine**. Keep the creator experiment ledger as a third option, rather than starting three projects in parallel.

The best reason to choose Discord is access to real workflows and potential testers. A missing directory search result is a weak reason by itself. Broad connectors, cited recaps and decision extraction already have competitors. The proposed advantage is a complete, recurring workflow that handles changing event plans, ambiguous commitments, role-based access and handoff review together. That advantage is unproven until organizers use it repeatedly.

## What the new platform changes

The current platform is an installable package system shared across ChatGPT and Codex. Skills guide recurring workflows; MCP exposes controlled capabilities; UI is optional. Public directory publication, private testing and repository distribution are different routes. See [platform facts](../research/platform-facts.md) for official references.

Public listing is not automatic. Treat third-party integration authorization and store eligibility as dependencies, with a documented go/no-go decision. Do not assume that renaming a connector as an app makes it eligible. Do not confuse availability of a development connection with permission to distribute publicly.

## The three best bets

| Bet | User and repeated job | Original functionality to test | Founder advantage | Major gate | First experiment |
|---|---|---|---|---|---|
| GuildBrief | Club/event organizers preparing the next event or incoming executive | Reviewable timeline of decisions, superseded plans, responsibility evidence and unresolved questions | Club operations and gaming-community experience | Discord permissions/content access and OpenAI eligibility | Reconstruct one recent event with an organizer; compare against their real handoff |
| Learning-page QA | Course authors checking pages before publication | HTML lint rules, accessibility/template findings, suggested diffs and a reviewed change report | Existing LMS page-audit experience | Data ownership, institution OAuth for live integration; do not reuse employer assets | Evaluate synthetic and independently authorized page exports with three authors |
| Creator experiment ledger | Small creators reviewing what actually improved an upload | Link creative hypotheses and revision decisions to measured outcomes and generation cost | Video editing and channel workflow knowledge | Analytics OAuth and incumbents; manual/upload-first prototype | Three creators record one hypothesis before upload, then review the result next week |

Read [the landscape](opportunity-landscape.md) before choosing a backup: lower institutional friction does not automatically mean higher demand.

## Why focus beats a connector collection

A long tool list makes implementation look busy but gives users little reason to return. A memorable task produces a clearer demo, search page, onboarding flow and retention metric. The project should answer one question exceptionally well before adding another provider.

For GuildBrief, the first question is: **“What did we actually agree for our next event, what changed, and who still owes an answer?”** A second useful workflow is generating an outgoing executive's reviewable handoff. Avoid broad moderation, automated posting, all-account DMs, recordings and permanent message indexing in the first release.

## Four growth mechanisms worth testing

1. **Task repetition:** event planning and handoffs cause users to return without reminders from the founder.
2. **Team introduction:** an organizer invites a teammate after a useful result, through an approved product flow.
3. **Useful public examples:** synthetic event templates, permission engineering writeups and short demos attract people with the same problem.
4. **Platform discovery:** precise metadata and example prompts help the right user recognize the product, if it is approved. Placement is a possibility, not a strategy to depend on.

Avoid growth through mass unsolicited DMs, auto-inviting members, publicly indexing private conversations or calling every server member a user. A bot's reach may count toward Discord access-review thresholds while remaining entirely different from actual product adoption.

## Validation sprint: September 29–October 12

Assume 8–10 hours per week alongside studies and other commitments. Rescale the schedule if actual availability differs.

**Days 1–3:** obtain the relevant integration/eligibility guidance; recruit organizers for interviews; prepare a synthetic sample event with a proposal, a confirmed change, a conflicting statement and an unassigned task. Check working-name availability before buying any domain.

**Days 4–7:** conduct six interviews. Ask about the most recent real missed decision, not whether they like AI. Record their current workaround, consequences, frequency, installation authority and acceptable data flow. No private messages should be stored in this public repository.

**Days 8–10:** reach twelve interviews total and compare three task concepts. Ask organizers to verify a sample brief. Test whether they prefer using ChatGPT, a Discord command or a simple web page; assistant-interface preference is part of discovery, not a given.

**Days 11–14:** obtain three concrete pilot commitments; choose one recurring job; freeze initial scope; record whether the public-store route is eligible, unresolved or unavailable. If neither recurring demand nor a permitted delivery path exists, test learning-page QA instead.

## Demand gates

| Gate | Proposed evidence | Decision |
|---|---|---|
| Problem | At least three organizers describe recent, recurring failures and agree to pilot | Continue discovery for this workflow |
| Access | A documented authorized way to retrieve only permitted data; policy questions resolved enough for the intended pilot | Proceed to implementation of that delivery route |
| Activation | Organizer completes a useful brief with correct evidence and understands data access | Expand beyond founder-operated demos |
| Repeat use | Three of five teams return voluntarily by November 23, then three initial teams use it in three of four weekly cycles by December 7 | Continue improving this workflow |
| Independence | Another tester installs and completes the workflow from documentation | Publish a usable release on an eligible route |
| Growth | Returning teams, referrals and manageable support cost | Repeat the strongest acquisition channel |

These small samples guide decisions; they cannot establish broad market size, causality or product-market fit.

## Resource plan

Allocate roughly 100–120 hours over twelve weeks if proceeding. Weeks 1–2 cover discovery (about 16–20 hours); weeks 3–6 cover a tightly scoped synthetic auth/retrieval/brief implementation (32–40 hours); weeks 7–10 cover consenting pilots, evaluation and documentation (32–40 hours); weeks 11–12 cover the release and distribution decision (16–20 hours). First live onboarding is targeted for November 10 after full access and quality gates. Re-estimate after the API spike and extend dates if engineering or approvals take longer; never compress the security gates to preserve the schedule.

Use existing recording equipment and editing skills. Cap the initial spending hypothesis at CAD 300 for twelve weeks; approve actual purchases separately. Start with on-demand retrieval and client-side synthesis where appropriate. That reduces storage and operator inference spending, but still uses the assistant's allowance and does not make data processing free or local.

## What makes this credible on a resume

The worthwhile achievements are authenticated multi-tenant tooling, exact access checks, protocol integration, difficult negative tests, source-backed output, independently reproducible setup and measured adoption. Store presence and a popular provider name are weaker evidence on their own.

Maintain a public technical narrative: why a decision was made, the failure case that motivated it, the test that verifies it, and the measured user result. Publish only authorized, anonymized or synthetic evidence. See [portfolio evidence](portfolio-evidence.md).

## Immediate next action

Start the first backlog milestone, **Validate demand and delivery eligibility**. The current repository should remain explicitly marked research/planning until functioning code and a reproducible demo exist.
