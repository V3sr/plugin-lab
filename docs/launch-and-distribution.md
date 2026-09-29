# Launch and distribution plan

Research date: September 29, 2026. Execution window: September 29–December 21, 2026. Status: proposed plan and unsent drafts. No product has been deployed, submitted, advertised or installed on another team's server by this document.

## Launch thesis

Start with a recurring task and a reachable operator: a club administrator, esports organizer or small-team lead preparing an event or handing responsibilities to the next executive. Test whether a brief of confirmed decisions, proposals, unresolved questions and responsibilities saves them from reconstructing a conversation. Source links and permission enforcement support this task; they are not, alone, a novel product category.

Andy can reach suitable organizers through campus and esports experience, and demonstrate the workflow using his editing skills. This is an access advantage, not authorization to use any organization's messages or install software. Recruit consenting pilots independently; do not imply UBC or UBCEA sponsorship.

Working product name: **GuildBrief**. This is a placeholder, with availability and trademarks unchecked. Decide the final name only after the first validation gate.

The goal is recurring useful use, with real deployment and engineering evidence for a resume. Directory placement, downloads, stars, impressions and aggregate server membership are secondary signals.

## Distribution and policy gates

The current public route is a plugin package reviewed for a shared ChatGPT/Codex directory. Verify publishing identity, upload the ZIP, resolve package and server findings, connect/verify the production MCP endpoint, provide a sample reviewer account plus five positive and three negative cases and a walkthrough, then submit; publish after approval. A production public HTTPS endpoint is required. See [OpenAI submission](https://developers.openai.com/plugins/deploy/submission) and [connection/testing](https://developers.openai.com/plugins/deploy/connect-chatgpt).

**Gate before a store-dependent build:** OpenAI's guidelines exclude plugins primarily functioning as unofficial third-party connectors. A richer workflow does not guarantee an exception. Obtain platform clarification before treating a Discord-connected product as eligible. If unresolved, test another source or product rather than assume a listing. [Current guidelines](https://developers.openai.com/plugins/plugin-guidelines).

Development-mode testing, local/repository marketplaces and public listing are different routes. The [official MCP Registry](https://github.com/modelcontextprotocol/registry/blob/main/docs/modelcontextprotocol-io/quickstart.mdx) publishes metadata, with artifacts distributed separately; its documentation still labels it preview. Neither GitHub nor registry publication grants platform eligibility or API authorization. [Packaging reference](https://developers.openai.com/plugins/build/plugins).

Monetization constraint: keep the initial product free or self-hostable within sustainable limits. Do not serve advertisements or run digital-subscription sales/upgrade promotions inside the plugin. Existing paid account entitlements are distinct. Seek a policy review before introducing any commercial model. Advertising **for** a product outside it is different from advertising **inside** it.

See [platform facts](../research/platform-facts.md) and the project's sources for additional eligibility, Discord access and data-handling requirements. Recheck changing policies before submission.

## Segments and channel priority

| Priority | Segment | First useful task | Recruitment approach |
|---|---|---|---|
| 1 | Student club administrators and event executives | Prepare the next event brief or executive handoff | Warm introduction, short discovery interview, optional assisted pilot |
| 2 | Esports/community organizers | Resolve tournament/LAN responsibilities and open decisions | Organizer partnerships and a sample event walkthrough |
| 3 | Small volunteer/project team leads | Recover decisions before a weekly meeting | Referral from a successful pilot; test source and permission needs |
| 4 | Technical MCP users | Run an auditable, self-hosted workflow | GitHub documentation, reproducible example and useful engineering article |
| Later | Broad consumer Discord users | Unvalidated | Do not target until access constraints and recurring value are established |

An administrator often authorizes installation, while another member uses the product. Interview both. A server being accessible to a bot is insufficient evidence that every connected human should receive its content.

Channel order:

1. Personally onboard the first 3–5 consenting teams. Observe setup and a real task, then invite voluntary feedback.
2. Ask a satisfied operator for an introduction to one similar team. Do not add contacts, send automated invitations or mass-DM server members.
3. Publish useful task tutorials and engineering posts with reproducible examples. Search visibility should follow substantive answers.
4. Share short demonstrations with communities whose current rules permit relevant self-promotion. Disclose that Andy built the product.
5. Offer a demo to small relevant creators and organizers; disclose any paid relationship and do not invent testimonials.
6. Use public directories after eligibility and readiness gates pass. Run launch-community experiments when independently usable, without relying on them for ongoing growth.
7. Test paid promotion only after repeat use and an independently usable installation flow.

## Twelve-week schedule

Assume 8–10 hours per week, adjusted around work and school. Each week includes product work, recruiting/learning and a short evidence update in GitHub. Numbers below are proposed targets, not observed performance or promises. November 10 is the earliest planned live-pilot start, conditional on the complete identity/access, current-evidence and synthetic brief-quality gates. Weeks 3–6 provide only 32–40 hours: if the engineering estimate or failed checks require longer, extend the build and shift pilot/cohort/launch dates. Do not compress security or quality work to preserve the calendar.

| Week and dates | Work | Reviewable evidence and decision |
|---|---|---|
| 1 · Sep 29–Oct 5 | Interview 6 organizers across clubs, esports and volunteer teams. Compare three concrete task concepts. Start platform/API eligibility investigation. | Anonymized interview notes: recent incident, frequency, workaround, operator and installation authority. |
| 2 · Oct 6–12 | Reach 12 interviews; recruit 3 prospective pilots. Clarify public-store constraints. Choose one task and distribution route. | Three explicit pilot commitments; a written scope decision and eligibility status. Stop if pain or access is absent. |
| 3 · Oct 13–19 | Implement identity binding and access verification with synthetic/test fixtures. Observe 3 sample-task walkthroughs. | Access boundaries and user identity are explicit; users can distinguish a decision from a proposal. No live team data. |
| 4 · Oct 20–26 | Continue access/revocation/deletion and no-write verification. Begin current-evidence retrieval and brief behavior using fixtures. | Negative permission cases, stale/deleted evidence handling and documented remaining work. No live team data. |
| 5 · Oct 27–Nov 2 | Complete the brief workflow and run the full synthetic quality evaluation; correct failures. Prepare two synthetic demo recordings and installation instructions. | Source support, confirmed-versus-proposed decisions, ownership ambiguity and safe fallback results. No live team data. |
| 6 · Nov 3–9 | Finish the full identity/access/current-evidence and synthetic brief-quality gates. Publish one technical article using sample data; schedule 3 consenting pilots. | A recorded go/no-go decision. Any incomplete gate delays live onboarding; do not skip it. |
| 7 · Nov 10–16 | Earliest live start: assist the first 3 consenting pilot teams only after all gates pass. Run pilot cycle 1; publish the first task tutorial and use-case page. | Actual setup time, first useful task, explicit authorization and per-user activation date. No founder-prompted repeat-use claim. |
| 8 · Nov 17–23 | Run cycle 2 for the first 3 teams. Expand to at most 5 pilots only if current checks and support capacity permit; record a separate cohort clock for new teams. | November 23 second-use checkpoint, with human and team counts reported separately. Prepare independently reproducible installation. |
| 9 · Nov 24–30 | Run cycle 3. Fix the largest observed setup or usefulness problem. Prepare review materials and a versioned permitted distribution package. | Source/permission quality in real tasks; voluntary repeat usage and source-specific eligibility status. No public-launch dependency yet. |
| 10 · Dec 1–7 | Run cycle 4. Have an independent tester install and complete a task. Interview returning teams about whether to keep the product. | Target: 3 teams participate in at least 3 of 4 cycles; at least 2 distinct reasons to keep using it. Installer success; matured individual cohorts only. |
| 11 · Dec 8–14 | Submit for public review or launch through another permitted route only if ready and eligible. Offer up to 5 relevant organizers/creators a walkthrough; a small ad test is optional after the retention/setup gate. | Submission state separated from usage. Cost per activation and retained use; synthetic or consented launch evidence. Approval timing is not promised. |
| 12 · Dec 15–21 | Publish an anonymized case study, release notes and retrospective. If approved, publish the directory listing; repeat the best organic channel. Choose continue, narrow, pivot or archive. | Real cohort metrics, engineering evidence, costs, limitations and next decision. Unready work remains gated. |

Do not wait for public approval to learn from other permitted routes. Do not continue a blocked route merely to keep the schedule looking complete.

## Funnel, metrics and attribution

Funnel: **qualified visit → setup started → authorized connection → first useful brief → voluntary second task → four-week retained use**.

| Metric | Definition | Proposed target |
|---|---|---|
| Discovery interviews | Conversations with target operators about a recent concrete problem | 12 by Oct 12 |
| Pilot commitments | An operator agrees to a specific trial task and has installation authority | 3 by Oct 12 |
| Activated user | Completes an authorized brief with valid evidence and marks it useful, or uses it for the intended task | Measure from first pilot; never infer from install |
| Human second-task rate | Activated people completing another task voluntarily within 14 days, divided by activated people whose 14-day window has elapsed | Nov 23 early count checkpoint; score full windows Nov 24 or later for Nov 10 starts. Directional target ≥50%; report numerator/denominator |
| Team repeat use | Pilot teams with a voluntary useful task in at least 3 of 4 weekly cycles; each team starts its own clock at activation | Target: 3 teams by Dec 7 among teams started Nov 10; later pilots are not prematurely scored |
| Reasons to continue | Specific reasons returning operators give for keeping the product, tied to repeated tasks | At least 2 distinct reasons by Dec 7 |
| Independent installation | A tester outside founder-assisted onboarding completes setup and one useful task | By Dec 7, after all live-data gates |
| Weekly active team | At least one human initiates a useful task that week | Planning base: 5 teams by Dec 21; stretch: 10 |
| Four-week retained user | A person completes a useful task in days 21–27 after activation; score once that measurement window closes | Planning base: 10 people by Dec 21; stretch: 30 |
| Four-week cohort retention | Retained people divided by people whose day-21–27 measurement window has closed | Directional expansion target: ≥40%; earliest Nov 10 cohort matures Dec 8. Report counts and uncertainty |
| North-star metric | Teams completing a useful event/handoff brief each week | Trend upward with repeat use |
| Quality | Citation validity, unsupported statements, task usefulness, permission failures | Permission leakage blocks expansion; quality thresholds set before pilot |
| Operations | Setup success/time, p95 latency, per-task cost, support minutes/team | Sustainable within budget; publish measured values |

The late retention targets need early cohorts. New week-12 installs cannot count as week-12 four-week retained users. Teams added in week 8 and people connecting later within a team start their own clocks. The earlier 10-team/30-retained-human ambition is now the stretch target under this slower ramp; the planning base is 5 active teams and 10 retained people. Neither is a forecast. Count automated scheduled runs separately from human activity. Count a server's members as potential reach only, never as users.

Illustration, **not a forecast**: 500 qualified visitors × 10% connections × 60% activation × 40% four-week retention = 12 retained people. Replace every assumed rate with observed cohorts. This shows why large view counts can yield little repeat use.

Record minimal, disclosed product events and the acquisition source. Exclude message text, secrets and unnecessary identity from analytics. Use consented anonymous task feedback; do not copy private conversations into public GitHub issues. Disclose telemetry accurately and provide meaningful controls. Avoid a “no tracking” promise if usage events are collected.

## Landing page and listing drafts

These describe the proposed outcome. Edit to match implemented capabilities before publication. No live landing page is created by this plan.

**Headline:** Know what your community decided before the next event.

**Subheading:** Create a brief of confirmed decisions, open questions and responsibilities from selected conversations, with links to the evidence.

**Primary CTA during research:** Join the organizer pilot.

**Primary CTA after a working distribution route exists:** Connect your team.

**Supporting points:**

- Review what was agreed, what was proposed and what still needs an answer.
- Check the source behind each supported statement.
- Select the conversations relevant to your task.

Describe actual permission, retention and provider-sharing behavior in the setup flow and privacy page. “No messages sent or channels changed” is suitable only once the exposed operations and underlying permissions support it. Avoid broad “private,” “100% accurate,” “no data leaves Discord” and “official connector” claims.

**Proposed store display name:** GuildBrief

**Subtitle:** Event decisions and team handoffs from selected discussions.

**Description:** Prepare for an event or team handoff by reviewing decisions, responsibilities and unresolved questions in authorized conversations. Open the linked evidence to check each supported point. Availability depends on connected sources and permissions.

**Example prompts:**

1. What did we decide for Friday's LAN, who owns each task, and what remains unresolved?
2. Prepare an executive handoff from the selected event-planning discussions.
3. Which proposed dates were confirmed, and which are still suggestions?
4. Find the evidence for the venue decision and show any later change.
5. List questions we should resolve before the next planning meeting.

The source-specific wording must follow eligibility findings and implemented access. Do not claim that the product can read every server, personal DMs or all account history. Do not market pricing, free trials or discounts in directory metadata. Do not manipulate tool descriptions to favor this plugin over other tools.

Metadata evaluations should include direct, indirect and negative prompts. For example, “Summarize this unrelated document” should not activate a community-source tool. Keep prompt outcomes and metadata revisions in version control. [Official metadata guide](https://developers.openai.com/plugins/guides/optimize-metadata).

## Three Shorts/demo drafts

Use synthetic messages or separately consented, carefully redacted examples. Label synthetic examples clearly. Record the implemented product rather than simulate successful behavior as if live. Captions and simple edits should make the task legible; views are not the success metric.

### Demo 1 — Everyone remembers the meeting differently

- **0–3s hook:** “Everyone remembers the meeting differently.”
- **3–8s:** Show three sample messages: proposed Friday venue, confirmed Saturday venue, unanswered transport question.
- **8–18s:** Ask: “What's actually confirmed for the event?” Reveal agreed, proposed and unresolved sections.
- **18–26s:** Open the venue citation and show the original confirmation.
- **26–32s CTA:** “I'm testing this with event organizers. Join the pilot.” After launch, replace with the permitted install CTA.

### Demo 2 — The executive handoff

- **0–3s hook:** “The next club executive gets 40 channels and one sentence: good luck.”
- **3–9s:** Show a synthetic handoff with a pending sponsor answer, booking decision and assigned task.
- **9–20s:** Ask for a handoff brief. Show decision, owner and unresolved question with evidence.
- **20–27s:** Verify one responsibility against the message and correct an ambiguous assignment if necessary.
- **27–33s CTA:** “Would this help your next handoff? Try the organizer pilot.”

### Demo 3 — A suggestion is not a decision

- **0–3s hook:** “Someone said ‘Friday?’ That doesn't mean Friday is confirmed.”
- **3–10s:** Show a sample proposal, tentative reaction and later explicit agreement for a different day.
- **10–22s:** Ask for the current event date. Show the confirmed result, tentative proposal and change evidence.
- **22–29s:** Explain: “The useful part is checking what the conversation supports.”
- **29–34s CTA:** “See the walkthrough and tell me what your team needs.”

Testing: compare the three hooks with similar distribution and observe qualified visits, authorized activations and returned use. Do not select a hook solely because it earns more views. Do not promise numerical time savings until measured with participants.

## Unsent outreach drafts

**Warm organizer discovery request:**

> Hi [name] — I'm exploring a small tool for event decisions and club handoffs. Have you recently had to dig through chat to figure out what was agreed or who owned a task? I'd love a 15-minute conversation about how you handle that now. There's no installation required for the interview, and I can show an example using made-up messages. I'm building this personally, not on behalf of UBC.

**Pilot invitation after interview:**

> Thanks for explaining the [specific problem]. I've built a narrow version around [specific task]. If you're interested and have permission, I'd like to walk through setup with you and test it on selected authorized conversations before [event/date]. I'll explain what the service and AI provider receive, retention, access controls and how to disconnect first. Feedback is optional; I won't use your team's content or name publicly without separate consent.

**Partnership/demo offer:**

> Hi [name] — I built a tool for [validated task], and your community of [relevant operators] seems like a useful fit. Here's a short walkthrough using sample messages: [link]. If it helps, I'd be happy to run an optional demo or share a practical planning/handoff template. I'm the builder; no endorsement or promotion is expected.

Send manually only after Andy authorizes contact. No scraped lists, automated DMs, unsolicited server joins or fabricated personalization. Ask permission before posting in a community; respect its current promotion rules. Disclose compensation if a creator is paid.

## Search and content plan

Publish answers to actual operator questions:

| Proposed tutorial | Useful material | Intended audience |
|---|---|---|
| How to prepare a student-club executive handoff | Checklist, sample brief, ambiguous ownership examples | Club executives |
| A LAN event decision checklist | Date/venue confirmation, owners, unresolved dependencies | Esports organizers |
| How to distinguish chat proposals from confirmed decisions | Examples and a manual method as well as the product | Team leads |
| Building a permission-aware MCP workflow | Threat model, test cases, failure handling and synthetic fixtures | Developers/recruiters |
| What happens when access is revoked? | Implemented behavior, retention controls and observable checks | Operators/security-conscious testers |

Do not manufacture generic keyword pages, publish private threads for SEO or claim official affiliation. Add installation documentation only for supported clients/routes. Each article should work as a useful resource even for a reader who does not install.

## Budget and expansion decisions

Suggested **CAD 300 cap for 12 weeks**, not vendor quotes or purchase authorization. Research and organic recruiting come first. Review actual recurring costs before selecting services.

| Allocation | Cap | Condition |
|---|---:|---|
| Hosting and operations | CAD 90 | Choose only after architecture/access route is validated |
| Domain | CAD 30 | Check naming first |
| Recording/editing | CAD 0 | Existing equipment and tools |
| Late acquisition experiment | CAD 120 | Repeat-use and setup gates passed |
| Contingency | CAD 60 | Preserve for unexpected infrastructure/support |
| **Total** | **CAD 300** | Reassess before exceeding |

Spend no advertising money before the December 7 repeat-use and independent-installation review, or later if pilots start late. For any late paid test, choose one audience, one useful task and two creatives; log spend, setup, activation and cohort outcomes. Stop if it generates clicks without activations. Do not scale before observing retained use; no universal acceptable CAC is assumed without revenue and retention economics.

Stop/go gates:

- **Oct 12:** Continue if three operators commit to a real pilot and the problem recurs. If not, narrow or choose another avenue. A public-store strategy requires eligibility clarity; uncertainty must remain visible.
- **Nov 9:** Decide whether all identity/access, current-evidence, revocation/deletion, no-write and full synthetic brief-quality gates have passed. Only then may live pilots start November 10. Otherwise extend the schedule. A permission leak halts live onboarding.
- **Nov 23:** Review voluntary second-task counts for the earliest people and repeat use for their teams, keeping the metrics separate. Full 14-day rates for November 10 activations mature November 24, so this checkpoint must not score those rates early. Diagnose value and setup failures. Any teams added this week start a new cohort clock.
- **Dec 7:** Target three teams using the product in at least three of their four cycles, two distinct reasons to keep it, and independent installation/task success. Target directional four-week human retention ≥40% only when the individual cohort matures; report counts and uncertainty. If this gate fails, keep learning without public launch or paid acquisition.
- **Dec 21:** Continue when repeat use, referral interest and sustainable support costs exist. Narrow or archive if usage remains one-off. Preserve the evidence and infrastructure for another validated product.

## Resume and GitHub evidence

Commit real work as it happens. Tie interview synthesis, scope choices, access tests, eval changes and releases to issues/PRs. Do not backdate or manufacture activity. A research plan is research; it is not a deployed product.

Evidence package:

- Reproducible README and safe sample dataset.
- Architecture decisions explaining scope, access and distribution choices.
- CI and meaningful access/revocation/cross-tenant checks.
- Versioned prompt evaluations and cited-result quality evidence.
- Tagged releases, permitted-client setup instructions and recorded walkthrough.
- Anonymized user/team cohorts, cost/support measurements and limitations.

Current resume wording: “Researched and designed a permission-aware community brief workflow with proposed MCP interfaces and source-linked decisions.” Add “prototyped” only after a functioning prototype exists; use only components actually completed.

After deployment, replace placeholders with measured results, for example:

> Built a permission-aware MCP service for community event briefs; deployed to [N] consenting teams with [X]% four-week user retention.

> Implemented channel-access checks, revocation/deletion handling and cross-tenant tests; verified [measured result] across [N] cases.

> Evaluated [N] representative prompts and improved tool-selection precision from [A] to [B].

Never publish placeholders as achieved metrics. GitHub stars and total server membership are not substitutes for real users or technical evidence.
