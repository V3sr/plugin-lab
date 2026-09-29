# Plugin opportunity landscape

Research date: 2026-09-29. Prepared for Andy Li's independent portfolio project.

## Recommendation

Start with one recurring job for communities Andy can reach: **turn approved club or esports source material into an event briefing, decisions, and an officer handoff, with links back to the evidence**. Discord can be a delivery surface and an authorized data source, rather than the entire value proposition. A connector alone is comparatively easy for another developer to reproduce.

Keep **institution-approved, export-first course content QA** as the strongest separate career-oriented option, and **uploaded receipts/return evidence** as the easiest consumer option without an integration approval dependency. Build a small **permission regression evaluation kit** from the flagship's actual tests as a reusable engineering artifact, rather than starting a second full SaaS at the same time.

These are recommendations from product and engineering judgment. This research does not establish market size, directory absence, willingness to pay, or future acquisition volume. It verifies several data-access routes and existing competitors, then proposes narrower wedges to test.

## Global distribution gate

Treat public ChatGPT/Codex directory eligibility as a separate release gate from technical feasibility. A working OAuth flow or MCP server does not establish permission to publish an unofficial connector for another company's product. Verify the current OpenAI submission rules and obtain any required service-owner authorization before relying on a directory listing. Revalidate those rules immediately before submission. An original product with uploaded or explicitly approved inputs still needs to meet all applicable submission requirements.

Separate these outcomes in the roadmap:

1. An independent product and an honest GitHub portfolio.
2. Private developer-mode testing or an appropriate local plugin.
3. Public distribution on the product's own website, when permitted.
4. Public directory publication only after eligibility and review are satisfied.

The ranking below rewards Andy's ability to reach a first cohort, usefulness of a narrow workflow, and demonstrable engineering. It does not assume that any third-party connector will be admitted to the directory.

## Comparative matrix

Scores are subjective, on a 1–5 scale: **Access** means ability to recruit a relevant first cohort; **Build** means simplicity of a useful narrow MVP; **Resume** means potential to demonstrate substantive engineering; **Repeat** means plausible repeated usage. Scores are not measured demand. Effort estimates are planning ranges for a solo student working roughly 8–12 focused hours weekly, after an appropriate data route is available; external approvals can add an unknown delay.

| Rank | Avenue and narrow product | First user and job | Access / Build / Resume / Repeat | MVP effort | Why it merits a test |
|---|---|---|---|---|---|
| 1 | **Club decision and event handoff**, with an authorized Discord adapter | Club officers: identify commitments, unresolved questions, deadlines, and event responsibilities from selected source material | 5 / 3 / 5 / 5 | 4–7 weeks | Andy has campus leadership and esports context; event briefings provide weekly utility and officer transitions provide a concrete artifact |
| 2 | **Permission regression kit for agent connectors** | MCP maintainers: prove that forbidden channels, revoked roles, and other tenants' records remain inaccessible | 3 / 3 / 5 / 4 | 3–5 weeks for a narrow kit | Strong engineering companion to the flagship; produce reproducible failures and CI evidence rather than a generic risk score |
| 3 | **Course author QA with reviewed patch diffs** | Learning technologists/instructors: catch broken structure, missing required sections, and inconsistent course templates in approved exports | 4 / 3 / 5 / 4 | 4–6 weeks | Direct fit with Andy's learning technology experience; a small professional cohort may be more valuable than a large casual install count |
| 4 | **Uploaded receipt, return, and warranty evidence** | Students and frequent buyers: know which purchases need action and find the exact proof of purchase | 4 / 4 / 4 / 4 | 3–4 weeks | A useful initial product can work without broad mailbox access; privacy and traceable dates are visible differentiators |
| 5 | **Small esports event readiness coordinator** | Club tournament organizers: reconcile roster, player availability, bracket state, and announcements before a LAN/scrim | 5 / 3 / 5 / 4 | 4–6 weeks | Andy can pilot with organizers; cross-tool readiness is a clearer wedge than another bracket generator |
| 6 | **Creator experiment and production-cost ledger** | Small gaming/animation creators: connect a hypothesis and script/edit decisions to subsequent channel outcomes and production costs | 4 / 4 / 4 / 4 | 3–5 weeks | Andy can use it personally; the ledger must solve a job beyond existing channel analytics or AI advice |
| 7 | **Zotero claim and citation trail** | Undergraduates/researchers: show which source supports each statement and whether the draft overstates the source | 4 / 3 / 5 / 4 | 4–6 weeks | Strong reproducibility and provenance story; compete on an inspectable claim trail rather than generic paper chat |
| 8 | **Course deadline change reconciler** | Working students: see what changed in their schedules, why it changed, and whether their remaining capacity is sufficient | 5 / 4 / 4 / 4 | 3–5 weeks export-first | ICS and syllabus uploads reduce initial institutional OAuth dependence; avoid rebuilding an entire student planner |
| 9 | **Campus/public deadline evidence assistant** | Students: find applicable official dates, distinguish general from program-specific deadlines, and prepare an action checklist | 5 / 4 / 4 / 3 | 2–4 weeks for one campus | Source freshness and traceable applicability are more useful than a generic calendar chatbot |
| 10 | **Game patch-to-build impact notebook** | Deadlock/CS2 players and creators: identify which saved builds or previous claims need retesting after a patch | 5 / 3 / 4 / 4 | 3–5 weeks for one game | Strong creator fit; versioned user builds and explicit calculations can be differentiated from news summaries |
| 11 | **OBS recording preflight and capture checklist** | Gaming creators: verify expected scene, audio, resolution, recording state, and output location before a take | 4 / 3 / 5 / 4 | 3–5 weeks local-first | Concrete failures are testable; a local Codex plugin/companion fits the data route better than a hosted-only connector |
| 12 | **Wardrobe purchase-gap and budget capsule planner** | Students refreshing their wardrobe: compare a prospective bundle with owned pieces, sizes, actual gaps, and a fixed budget | 4 / 4 / 3 / 3 | 3–5 weeks upload-first | Personal fit and visual demos; catalog onboarding burden and established wardrobe apps are substantial obstacles |
| 13 | **PC bundle value splitter** | GPU buyers and friends sharing hardware: compare a standalone GPU with a full machine, including conservative resale and transaction scenarios | 4 / 4 / 4 / 3 | 2–4 weeks pasted-listing-first | Andy has a real use case; separate arithmetic from unverified resale assumptions and avoid dependence on Marketplace scraping |
| 14 | **Campus outing and commute feasibility planner** | Commuter students: find an event that actually fits class/work times, travel time, cost, and the return journey | 5 / 3 / 4 / 4 | 3–5 weeks one region | Official event feeds and regional transit data make an attainable local pilot; generic event discovery is already served |

## Avenue details, competition, and routes to a first cohort

### 1. Club decision and event handoff

- **MVP:** accept a small set of approved meeting notes, pinned event instructions, a roster sheet, and selected messages. Return an evidence-linked brief containing decisions, owners, pending questions, and the next event checklist. A human approves anything that is posted externally.
- **Technical route:** file uploads first; an authorized Discord bot for specifically configured channels later. Use a selected-page Notion integration if necessary, rather than treating every workspace document as available. Discord ordinary user-account automation is prohibited; bot and interaction routes have materially different access limits [S01–S03].
- **Competition:** CampusGroups already offers organization, communication, event, membership, and budgeting workflows. Notion integrations already exist. The proposed wedge is continuity across officer turnover and reliable evidence about commitments, not an empty student-club market [S04–S05].
- **First distribution:** privately recruit 3–5 club executive teams through Andy's own campus network, with administrator-approved sources. Demonstrate a real recurring event workflow using synthetic or explicitly approved data. Offer a shareable handoff template that naturally reaches the incoming officer.
- **Validation gate:** at least 3 teams use the briefing for 3 separate events or weekly meetings; at least 2 incoming officers can find a prior decision without asking the outgoing officer. These are proposed acceptance criteria, not achieved results.
- **Confidence:** high confidence in a limited authorized technical route; medium confidence in Andy's cohort access; demand and directory eligibility unvalidated.

### 2. Permission regression kit for agent connectors

- **MVP:** a fixture-driven test runner with two users, two tenants, a forbidden channel, a revoked role, and malicious text embedded in an allowed record. Assert backend authorization directly and report a reproducible failing tool call. Export JSON plus a readable evidence report for CI.
- **Competition:** MCP Inspector already tests connections and schemas; Promptfoo already offers direct MCP testing and red teaming. A generic MCP tester would duplicate existing work [S06–S07].
- **Wedge:** connector-specific access invariants, cache invalidation after revocation, source deletion, and permission changes. Integrate with existing tools rather than claiming a new general-purpose security framework.
- **First distribution:** publish the flagship's synthetic permission fixtures and a short failure/fix walkthrough. Ask 3 open-source maintainers whether the fixtures expose a real bug or missing regression test. Expand only if maintainers use it in CI.
- **Confidence:** high feasibility for deterministic fixtures; unvalidated market demand. Highest resume value if tests exercise the real deployed service rather than merely checking mocked functions.

### 3. Course author QA with reviewed patch diffs

- **MVP:** ingest instructor-approved HTML or a course content export. Detect invalid structure, missing configured sections, inconsistent repeated templates, and selected accessibility issues. Produce a proposed patch and before/after preview; changes remain reviewable.
- **Technical route:** independently built rules and synthetic fixtures first. Use only authorized exports; institution-approved Canvas OAuth can follow. Canvas Cloud developer keys require institutional administration, and its OAuth guidance says asking other users to manually generate and paste tokens violates its API policy [S08]. Keep the independent project separate from employer assets, private course material, and employer-owned implementations.
- **Competition:** Canvas has its own accessibility checker and Cidi Labs offers UDOIT. W3C says an automated tool alone cannot establish accessibility conformance [S09–S11].
- **Wedge:** instructor-configured course template semantics, bulk regression checks across repeated pages, and reviewed patch diffs. Report exactly which checks ran; do not market it as a complete accessibility certification.
- **First distribution:** recruit 2–3 approved instructional design or learning technology users for an export-based pilot. A synthetic public course provides a credible demo and benchmark without private material.
- **Confidence:** high for HTML QA; lower for cross-institution deployment timing. Strong domain fit and professional portfolio value, but smaller initial user volume than a student consumer product.

### 4. Uploaded receipt, return, and warranty evidence

- **MVP:** upload a receipt and the applicable policy/warranty document. Extract the purchase date, item, vendor, and explicitly supported deadline. Show the quoted evidence span and allow corrections. Produce a checklist or draft return request, with user-selected calendar export.
- **Technical route:** uploads and explicit user input avoid broad Gmail scopes. Broad Gmail read scopes are restricted and can require additional verification and security assessment, so automatic inbox ingestion is a later gate [S12]. Do not silently infer return eligibility from a generic store policy if exclusions or final-sale terms are missing.
- **Competition:** Itemtopia already stores receipts, warranties, manuals, and purchase records [S13].
- **Wedge:** “what should I act on this week, and what evidence do I need?” for students making clothing/technology purchases. Provenance and correct handling of uncertain dates matter more than another full inventory database.
- **First distribution:** opt-in pilots with student buyers and repair/resale communities. Demonstrate with a synthetic purchase that has a clear deadline; measure completed actions, extraction corrections, and repeat uploads.
- **Confidence:** high upload-first feasibility; medium differentiation; demand unvalidated.

### 5. Small esports event readiness coordinator

- **MVP:** accept a roster and approved schedule; read one tournament source; identify missing registrations, conflicts, match readiness, and the next announcement to prepare. Keep result reporting behind organizer review.
- **Technical route:** FACEIT provides publicly available data through its Data API and server-side API keys. Challonge has API and OAuth routes; validate current plans and required scopes before committing to the integration [S14–S16].
- **Competition:** FACEIT and Challonge already handle game/tournament data and bracket workflows. Existing event management does not prove an empty market for coordination.
- **Wedge:** readiness across attendance, roster, bracket, room, and stream production for smaller campus organizers, with a clear “what is blocking the next match?” view.
- **First distribution:** one approved UBCEA event followed by 2 other university esports organizers. Share an organizer checklist and incident review, not unsolicited messages to server members.
- **Confidence:** high for one documented data source; actual cross-organizer demand unvalidated. Strong potential for external APIs, state reconciliation, and operational metrics.

### 6. Creator experiment and production-cost ledger

- **MVP:** log the hypothesis before publication, script hook, edit choice, target audience, model/tool spend, and time spent. Import owner-provided analytics exports and generate an evidence-based review of what should be tested next.
- **Technical route:** owner-authorized YouTube Analytics can follow once OAuth is available. The Analytics API supports custom owner/channel reports; public competitor data is not a substitute for another creator's private retention information [S17].
- **Competition:** vidIQ already has an official ChatGPT app and MCP endpoint; TubeBuddy offers analytics and testing. A missing YouTube connector is not a credible novelty claim [S18–S19].
- **Wedge:** retain the link between a creator's pre-publication choices, production cost, and outcomes. Focus initially on one format, such as low-budget animated Shorts or gaming commentary. Avoid treating uncontrolled before/after results as causal proof.
- **First distribution:** Andy uses it for his own published work, then recruits 5 creators in the same format. Share a consented experiment breakdown and reusable log template. Success means creators log before publishing and return for the post-publication review.
- **Confidence:** high export-first feasibility; substantial existing competition; niche adoption unvalidated.

### 7. Zotero claim and citation trail

- **MVP:** connect an explicitly selected collection or upload an export plus permitted papers. For a supplied draft, map claims to source passages, identify missing support, and export an inspectable evidence matrix. Keep bibliographic metadata separate from claims about full-text evidence.
- **Technical route:** Zotero has Web API v3, granular library access, and OAuth 1.0a credentials. A remote MCP-facing auth layer and Zotero's upstream auth are separate implementation concerns. Semantic Scholar can enrich publication metadata, but metadata availability does not establish full-text access [S20–S22].
- **Competition:** several Zotero MCP implementations already exist, including 54yyyu/zotero-mcp. Generic library search, summarization, and citation generation are established [S23].
- **Wedge:** a versioned claim-to-source audit that exposes unsupported wording and preserves the passage/context a reviewer needs.
- **First distribution:** 3 undergraduate writing/research groups and a small graduate cohort. Publish a synthetic or openly licensed example with intentional unsupported claims and a reproducible evaluation.
- **Confidence:** high for metadata and user-provided content; medium for faithful claim assessment; research willingness to adopt unvalidated.

### 8. Course deadline change reconciler

- **MVP:** ingest the user's Canvas ICS file/feed and syllabus files, then compare snapshots. Show added, moved, and removed deadlines with the original source. Ask users for their own effort estimates and work availability; calculate capacity transparently.
- **Technical route:** Canvas documents an iCal feed for calendar events and assignments. It does not cover every syllabus instruction or all student To Do content, and freshness must be checked. Institutional OAuth is a later route, not a prerequisite for an upload prototype [S08, S24].
- **Competition:** Shovel already imports Canvas assignments and combines syllabus/LMS information with study planning. StudyFetch has institutional LMS integrations [S25–S26].
- **Wedge:** visible deadline changes and conflicting sources, especially for working students. Avoid another all-purpose planner unless user interviews reveal a concrete failure in existing options.
- **First distribution:** 10 working students in Andy's network for one academic term. Measure corrections, missed-source rates, and whether users return when an assignment changes.
- **Confidence:** high for snapshot comparison; comprehensive assignment coverage and differentiated demand unvalidated.

### 9. Campus/public deadline evidence assistant

- **MVP:** maintain a small, versioned corpus of official UBC dates and user-uploaded notices. Show each date's program, session, source, and last checked time; produce an action checklist with a link to the actual official application or office.
- **Technical route:** the official UBC Academic Calendar and Student Services publish dates and deadlines. Start with one institution and a bounded set of deadlines instead of scraping an unbounded benefits or scholarship ecosystem [S27–S28].
- **Competition:** the official calendars and campus calendars already serve discovery; student planners provide scheduling. This research does not verify that no deadline-specific competitor exists.
- **Wedge:** resolve ambiguity between a general date and a program-specific/internal notice, preserving disagreement rather than confidently inventing eligibility.
- **First distribution:** opt-in residence/commuter student pilots and approved campus resource links. Measure whether users reach the correct official form and identify applicable deadlines; do not claim guaranteed award eligibility.
- **Confidence:** high public-source feasibility; repeated use likely seasonal and unvalidated.

### 10. Game patch-to-build impact notebook

- **MVP:** save a user's build and the exact game version, ingest selected official patch notes, flag affected items/abilities, and show the numerical assumptions behind before/after calculations. Generate a list of in-game tests or content claims to revisit.
- **Technical route:** Valve documents Steam news access. For Deadlock analytics, clearly label the community-operated Deadlock API as independent of Valve; use documented endpoints and graceful degradation. Official patch evidence should anchor balance claims [S29–S31].
- **Competition:** Deadlock API already offers MCP and data dumps. PatchDiff and Patchbook already summarize or organize updates. A generic Deadlock connector or patch summary is not novel [S32–S34].
- **Wedge:** changes relative to the user's own saved build and previously recorded claims, with explicit versioning and uncertainty. Observational win-rate changes alone do not prove patch causation.
- **First distribution:** Andy's own Deadlock videos and an opt-in cohort of players who repeatedly test builds. A shareable before/after calculation can drive referral if the inputs and patch version remain visible.
- **Confidence:** high for user-provided notes and deterministic math; medium for community API continuity; adoption unvalidated.

### 11. OBS recording preflight and capture checklist

- **MVP:** inspect a defined subset of OBS state and a user-approved local profile. Confirm expected scene/audio setup and recording state, then produce a timestamped checklist and optional recording marker log.
- **Technical route:** OBS publishes a WebSocket protocol and includes obs-websocket in current supported releases. A hosted ChatGPT app cannot simply reach arbitrary localhost services; prefer a local Codex plugin or explicitly paired companion, with authentication [S35–S36].
- **Competition:** OBS already has remote-control APIs and a broad plugin ecosystem. Simple start/stop control is a commodity; do not assume the directory lacks OBS integrations without a direct check.
- **Wedge:** “will this take contain the expected picture and sound?” with reproducible configuration checks, privacy-safe diagnostic artifacts, and recovery advice grounded in actual state.
- **First distribution:** 5 gaming creators and small campus stream teams, using Andy's own capture workflow as a demonstration. Measure avoided re-recordings and setup errors, not only installations.
- **Confidence:** high local feasibility; public hosted-product transport and demand unvalidated.

### 12. Wardrobe purchase-gap and budget capsule planner

- **MVP:** upload owned pieces and a prospective clothing bundle. Compare sizes, colors, occasions, duplication, and a fixed budget; show which new pieces enable usable outfit combinations. Keep all prices and available sizes tied to user-supplied listings.
- **Technical route:** uploads and pasted links are sufficient initially. Live commerce requires a permitted data source and verified terms; do not assume Facebook Marketplace offers a generally available official search API.
- **Competition:** Whering and Indyx already offer digital wardrobes, styling, outfit planning, shopping assistance, and related services [S37–S38].
- **Wedge:** decide whether a specific affordable bundle fills actual gaps, rather than digitizing an entire wardrobe before any useful output. Support corrections to fit and preferences instead of treating a photo as precise sizing evidence.
- **First distribution:** student thrift/bundle-shopping cohorts and resale sellers who opt into a pilot. Share a practical before/after capsule board with permitted product images.
- **Confidence:** high upload-first feasibility; competition and onboarding friction make differentiation uncertain.

### 13. PC bundle value splitter

- **MVP:** compare a pasted standalone GPU listing with a full-machine offer. Show component allocation, conservative resale ranges supplied by the user, travel/shipping, fees, and scenario sensitivity. Treat uncertain condition and resale estimates as explicit inputs.
- **Technical route:** pasted listings and screenshots first. eBay Browse offers listing search, but production Buy API access has business-model/approval requirements. Third-party Marketplace scrapers are not equivalent to an authorized official integration [S39–S40].
- **Competition:** eBay, local listings, and existing hardware price tools already serve parts of the task. No absence claim about deal-comparison products is supported by this research.
- **Wedge:** a documented split-purchase decision for two buyers, including the downside if other parts do not sell or the machine has defects. Build exact arithmetic and evidence freshness into the product.
- **First distribution:** a handful of local PC buyers and friends splitting machines; publish a synthetic, reproducible comparison with adjustable assumptions.
- **Confidence:** high for calculators and uploads; low-to-medium for durable automated sourcing. Purchasing is episodic, so retention may be weaker than club operations.

### 14. Campus outing and commute feasibility planner

- **MVP:** combine an approved timetable with public UBC events and a one-region transit route model. Return a few feasible plans with travel buffers, event cost, latest return, and sources.
- **Technical route:** UBC explicitly provides event REST/RSS resources. TransLink publishes GTFS static and realtime feeds; access registration, terms, current coverage, and service-alert handling must be checked [S41–S43].
- **Competition:** UBC events, campus engagement platforms, transit tools, and calendar planners already exist. Generic aggregation alone offers little distinction.
- **Wedge:** solve “what can I actually attend between these commitments and still get home?” rather than listing all available events. Display timetable/realtime uncertainty.
- **First distribution:** 10 commuter students during a 2-week pilot. Measure accepted plans and return visits. Event organizers can distribute their own event link through approved channels.
- **Confidence:** high for public data; routing complexity and differentiated user retention unvalidated.

## Ideas to defer

- **General WhatsApp personal inbox connector:** Meta's official Cloud API is for WhatsApp Business, with business account/number requirements. This does not establish broad consumer personal-history access [S44].
- **General Gmail life-admin app:** broad mailbox permissions create a verification/security dependency before a small upload-first product has demonstrated value [S12].
- **Automated Facebook Marketplace search as the core:** this research did not find a generally available official Meta search route. Do not treat third-party scraper marketing as proof of durable or permitted access. Upload-first decision support avoids making scraping availability the product's foundation.
- **Generic GitHub or Notion connector:** both ecosystems already have mature integration routes; GitHub maintains an official MCP server [S05, S45]. A new project needs a differentiated job or a contribution to existing infrastructure.
- **Generic YouTube, Zotero, or Deadlock MCP wrapper:** primary competitor documentation already establishes existing implementations [S18, S23, S32].
- **Many simultaneous plugins:** ship one independently useful product, verify usage, and extract reusable infrastructure only where a real implementation justifies it.

## First decision experiment

Before committing to a large implementation, show 3 narrow interactive or recorded demonstrations: an evidence-linked club handoff, an uploaded receipt action list, and a course QA patch preview. Use synthetic inputs. Recruit approximately 5 relevant users per demonstration from opt-in networks. Ask each to use the demonstration on a real task with approved inputs, identify the last time the problem happened, and choose whether they would use it again next week.

Compare completion, corrections, setup friction, source availability, and repeat demand. The strongest signal is a user bringing a second real task. A waitlist or enthusiastic comment alone is weaker evidence. If Discord service-owner or directory approval is unavailable, the club handoff can still be evaluated as an original upload-based product while that distribution gate remains unresolved.

## Primary sources and competitor references

The sources establish interfaces, restrictions, or current competitor features. They do not independently validate the proposed products' demand. Official provider documentation is used for technical claims; competitor-operated pages are used only to establish what the competitor says it offers. No store absence claim is made.

- **S01 — Discord OAuth2:** https://discord.com/developers/docs/topics/oauth2
- **S02 — Discord self-bot policy:** https://support.discord.com/hc/en-us/articles/115002192352-Automated-User-Accounts-Self-Bots
- **S03 — Discord message content review:** https://support-dev.discord.com/hc/en-us/articles/5324827539479-Message-Content-Intent-Review-Policy . Recheck current scale thresholds; historical indexed snippets can describe older thresholds.
- **S04 — CampusGroups group management:** https://www.campusgroups.com/product/groups-membership/
- **S05 — Notion integration authorization/access:** https://www.notion.com/help/create-integrations-with-the-notion-api
- **S06 — Official MCP Inspector:** https://github.com/modelcontextprotocol/inspector and https://github.com/modelcontextprotocol/inspector/blob/main/clients/cli/README.md
- **S07 — Promptfoo MCP testing:** https://www.promptfoo.dev/docs/red-team/mcp-security-testing/
- **S08 — Canvas OAuth and token policy:** https://canvas.instructure.com/doc/api/file.oauth.html ; indexed official deployment copy: https://www.k12.instructure.com/doc/api/file.oauth.html
- **S09 — Canvas accessibility checker:** https://community.instructure.com/en/kb/articles/664351-how-do-i-use-the-accessibility-checker-in-canvas
- **S10 — Cidi Labs UDOIT:** https://support.cidilabs.com/knowledgebase/udoit
- **S11 — W3C accessibility evaluation limitations:** https://www.w3.org/WAI/test-evaluate/
- **S12 — Gmail scope restrictions:** https://developers.google.com/workspace/gmail/api/auth/scopes and https://developers.google.com/identity/protocols/oauth2/production-readiness/restricted-scope-verification
- **S13 — Itemtopia purchase records:** https://www.itemtopia.com/inventory-app-for-receipts-and-warranties/
- **S14 — FACEIT Data API:** https://docs.faceit.com/docs/data-api/
- **S15 — FACEIT server-side API keys:** https://docs.faceit.com/getting-started/authentication/api-keys/
- **S16 — Challonge API/integrations:** https://docs.challonge.com/features/integrations and https://connect.challonge.com/docs.json
- **S17 — YouTube Analytics:** https://developers.google.com/youtube/analytics
- **S18 — vidIQ ChatGPT app and MCP:** https://vidiq.com/chatgpt/ and https://vidiq.com/mcp/
- **S19 — TubeBuddy analytics/testing:** https://www.tubebuddy.com/ and https://support.tubebuddy.com/hc/en-us/articles/21191305824027-A-B-Testing-FAQs
- **S20 — Zotero API v3:** https://www.zotero.org/support/dev/web_api/v3/
- **S21 — Zotero authentication:** https://www.zotero.org/support/dev/web_api/v3/oauth and https://www.zotero.org/support/dev/web_api/v3/basics
- **S22 — Semantic Scholar API:** https://www.semanticscholar.org/product/api . Search indexing currently also exposes the official https://webflow.semanticscholar.org/product/api version.
- **S23 — Existing Zotero MCP implementation:** https://github.com/54yyyu/zotero-mcp
- **S24 — Canvas iCal feed:** https://community.instructure.com/en/kb/articles/662804-how-do-i-view-the-calendar-ical-feed-to-subscribe-to-an-external-calendar
- **S25 — Shovel planner:** https://shovelapp.io/ and https://shovelapp.io/faq/
- **S26 — StudyFetch institutional integrations:** https://www.studyfetch.com/enterprise/institution
- **S27 — Official UBC Academic Calendar dates:** https://vancouver.calendar.ubc.ca/dates-and-deadlines
- **S28 — UBC Student Services dates:** https://students.ubc.ca/enrolment/dates-deadlines/
- **S29 — Valve Steam news interface:** https://partner.steamgames.com/doc/webapi/ISteamNews
- **S30 — Community Deadlock API docs:** https://api.deadlock-api.com/docs
- **S31 — Deadlock API independent-provider statement:** https://deadlock-api.com/
- **S32 — Existing Deadlock MCP/data dumps:** https://www.deadlock-api.com/data-dumps
- **S33 — PatchDiff:** https://patchdiff.com/
- **S34 — Patchbook:** https://patchbook.gg/
- **S35 — Official OBS WebSocket protocol:** https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md
- **S36 — OBS remote-control guide:** https://obsproject.com/kb/remote-control-guide
- **S37 — Whering wardrobe product:** https://www.whering.co/
- **S38 — Indyx wardrobe product:** https://www.myindyx.com/how-it-works
- **S39 — eBay Browse API:** https://developer.ebay.com/api-docs/buy/api-browse.html
- **S40 — eBay Buy API requirements:** https://developer.ebay.com/api-docs/buy/buy-requirements.html
- **S41 — UBC event developer resources:** https://events.ubc.ca/resources/webdev/
- **S42 — TransLink GTFS realtime:** https://www.translink.ca/about-us/doing-business-with-translink/app-developer-resources/gtfs/gtfs-realtime
- **S43 — TransLink developer resources:** https://www.translink.ca/about-us/doing-business-with-translink/app-developer-resources
- **S44 — Meta's official WhatsApp Business collection:** https://www.postman.com/meta/whatsapp-business-platform/documentation/wlk6lh4/whatsapp-cloud-api
- **S45 — GitHub official MCP server:** https://github.com/github/github-mcp-server

