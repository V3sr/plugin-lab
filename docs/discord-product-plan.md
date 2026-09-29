# GuildBrief: product and engineering plan

Research baseline: September 29, 2026. Working name only; domain, trademark, package, and product-name availability have not been checked. This document specifies proposed work. It does not describe a deployed product, approved plugin, completed integration, or validated customer demand.

## 1. Product decision

Build a community operations assistant that turns approved Discord discussions into a useful event brief and executive handoff. The first audience is volunteer-run clubs and esports communities coordinating recurring events. The central problem is that an event's time, responsibilities, decisions, and unresolved questions are scattered across messages and threads. New officers and absent organizers spend time reconstructing what happened and often act on an outdated proposal.

The main promise is: **“See what was decided, who owns the next step, and the messages behind it.”** A successful brief distinguishes confirmed decisions from suggestions, identifies conflicting instructions, and leaves an owner or deadline blank when no one explicitly committed to it. It makes the underlying evidence easy to inspect.

The first three jobs to support are:

1. Weekly event catch-up: “What changed about next week's tournament, what do I need to do, and what is still undecided?”
2. Event readiness: “Which confirmed tasks have explicit owners and deadlines? What conflicts could stop the event?”
3. Executive handoff: “Prepare a handoff about this event from the approved planning channels, including decision history and open questions.”

The differentiator is a reliable operations workflow, not the novelty of connecting Discord. Existing commercial integrations and open-source Discord MCP servers already offer retrieval or management capabilities.[^composio][^merge][^guildbridge][^pasympa] Permission handling, clear evidence, honest uncertainty, and short onboarding are the proposed advantages. Whether users value these enough to switch or pay is an experiment.

## 2. Platform eligibility is a prerequisite

OpenAI's current Plugin Guidelines exclude plugins whose primary role is an unofficial connector to a third-party service or a pass-through software layer.[^openai] That creates a material obstacle for publishing a generic third-party Discord connector in the ChatGPT Directory. Adding a different name, a polished interface, or brief templates does not establish eligibility. Meaningful independent functionality also does not automatically resolve the rule.

Before allocating a launch budget to ChatGPT Directory distribution, prepare a short functional description, architecture, data-flow diagram, authorization explanation, and demonstration of GuildBrief's standalone operations workflow. Use the applicable OpenAI submission or clarification channel to establish whether that exact product and its Discord integration can be accepted. Record the response and its scope. Obtain any necessary service-provider authorization. Treat an unclear response as unresolved, not as approval.

The project can initially validate utility with a standalone web application and, where the clients and providers permit it, a self-hosted or custom MCP installation. Those routes are separate distribution paths; neither overrides OpenAI's public-directory rules or Discord's policies. No public marketing should say “available in the ChatGPT store” before approval and listing actually exist. If public-directory eligibility remains unavailable, continue only if the standalone/custom-MCP product has a credible audience; otherwise choose another project with a clearer publication route.

Current OpenAI guidelines also restrict in-plugin sales of digital services and subscription upgrades, allow access to an existing paid account, and prohibit advertisements.[^openai] Pricing experiments therefore belong to the independently operated product, subject to the rules applicable there. Do not put checkout, promotional pricing, or upgrade persuasion into a ChatGPT plugin. Recheck these policies before any launch because they can change.

## 3. Scope and user experience

### Included in the first release

- One server selected for each brief; up to five admin-approved planning channels per pilot server.
- Guild text and announcement channels; explicitly approved public threads and forum threads after their parent-permission checks pass.
- A bounded time window, initially seven days and no more than 30 days for an individual request.
- Search, current-message retrieval, and a structured brief with direct message links.
- Explicit task ownership and deadlines; proposed ownership remains a proposal.
- A contradiction section showing both statements, their authors' display labels, dates, and evidence. A newer message alone does not prove that an older decision was reversed.
- Connection status, understandable access errors, deletion controls, and a content-free activity view for administrators.

### Deferred

Personal DMs, group DMs, private threads, voice transcription, automatic attachment downloads, moderation, message posting, member rankings, sentiment scoring, attendance tracking, and cross-server summaries are outside the MVP. Recurring unattended briefs and stored brief archives are later features because they change execution, retention, authorization, and consent requirements. No feature should infer an officer's performance or personality from their messages.

### Onboarding

An administrator visits the product website, reviews the data-flow disclosure, signs into Discord, installs the bot, and chooses permitted planning channels. The app requests only the bot permissions necessary for retrieval. The onboarding screen shows the approved channel list, excluded data types, current processing mode, and how members can request deletion or report a problem. The administrator publishes the supplied plain-language notice in the community; installation alone is not treated as proof of every legal permission needed to process members' content.

Every management request must verify the requester is the current server owner or currently holds `MANAGE_GUILD` (the chosen MVP admin policy), then bind the operation to that server. Recheck this before channel-allowlist changes, installation configuration, telemetry access and tenant deletion/settings changes. Former admins lose management access immediately; an ordinary member can still disconnect their own account without server-admin status.

A member separately signs in to GuildBrief with Discord OAuth. The product shows the intersection of channels approved by the administrator, visible to that member, and readable by the bot. The member chooses an event, time window, and output type, reviews the resulting brief, and opens any source message needed to confirm a claim. Copying the result is a user action. The MVP does not automatically distribute it to other members or services.

Pilot prompt: “Create the weekly tournament organizer brief for the last seven days. Separate decisions, proposed changes, tasks, and unresolved conflicts. Show source messages.” Use synthetic event names and messages in public demos.

## 4. Discord access model

Discord user OAuth and bot access have different responsibilities. The documented `identify`, `guilds`, and `guilds.members.read` scopes support identity, guild metadata, and the current user's guild-member information. They do not grant general account-wide message access. A server-installed bot supplies message retrieval; ordinary account automation and user-token self-bots are excluded.[^oauth]

Discord now documents a native `Search Guild Messages` endpoint with channel/content/author/date-related filters. It is gated by `MESSAGE_CONTENT`; search can temporarily return an indexing response. Channel history retrieval supports bounded pagination and requires visibility and history permissions.[^messages] The default engineering choice is official, on-demand bot search rather than full-history ingestion or a persistent content index.

`MESSAGE_CONTENT` affects REST response content as well as Gateway data. Without it, broad message bodies are unavailable, with limited exceptions such as app mentions and a message selected through a context-menu interaction.[^gateway] Server membership or a working bot token does not remove this requirement.

As of June 10, 2026, apps that reach 10,000 unique users who can access the app across its servers must submit for privileged-intent access review; reviewed access requires annual reapplication. Notifications provide a submission window, and app verification is a separate process.[^intent-review] Reachable members are not equivalent to GuildBrief's active users. A single large server could trigger review during an early pilot. Prepare the stated-use-case and data-practices materials before expansion, and never promise that approval is guaranteed.

## 5. End-to-end architecture

| Component | Responsibility | Proposed boundary |
| --- | --- | --- |
| Web and optional assistant interface | Connection, channel selection, brief request, evidence review | No bot tokens; no independent permission decisions |
| MCP/API edge | Validate tool schemas, resolve session identity, enforce limits | Each reviewed operation has its own explicit schema |
| Authentication service | Discord OAuth and client authorization | Provider tokens remain encrypted on the server |
| Authorization service | Resolve guild membership, roles, channel overwrites, bot access, and channel allowlist | Fail closed before retrieval and before response delivery |
| Discord adapter | Official API calls, rate-limit buckets, retries, current-message fetch | Server-side bot credential; allowlisted endpoints only |
| Brief engine | Evidence selection, extraction, contradiction detection, structured synthesis | Receives only already-authorized, bounded source content |
| Configuration store | Tenant settings, approved channels, encrypted credentials, deletion status | No persistent message bodies in MVP |
| Operations telemetry | Latency, success/error category, request counts, deletion completion | No raw content, search text, or generated briefs |

A member's request proceeds through these steps:

1. Validate the session and resolve the Discord account from the authenticated context. Never accept a caller-supplied actor ID as identity.
2. Resolve the selected tenant/server and its configured channel allowlist. Reject unknown or disabled tenants uniformly.
3. Fetch current membership and relevant roles/overwrites. Compute the member's permissions and the bot's permissions separately.
4. Limit requested channels to the authorized intersection. Submit native Discord search only with permitted channel filters; do not search private channels and merely hide them afterward.
5. Fetch bounded surrounding context and refetch messages used for final evidence. Remove content that has been deleted, become inaccessible, or falls outside the request.
6. Extract structured candidates, then synthesize the brief. Source content is untrusted data, never instructions governing tool use or access.
7. Validate citations and key fields; reauthorize and check the final evidence versions immediately before returning data. If a source was edited or deleted, drop or regenerate the affected claims within a bounded retry budget. If current evidence cannot be verified, return a clearly labeled dated snapshot/degraded result rather than assert a current decision; if current permissions cannot be established, return an access error with no cached content. The result is a verified snapshot, not a guarantee that the source cannot change after response delivery.
8. Discard request content from application memory and record only the disclosed operational metadata.

Use a TypeScript service with the official MCP SDK, a small web interface, a relational configuration database, and a secret manager as a reasonable first implementation. This is a proposed stack, not a requirement inferred from Discord. Keep the Discord adapter and permission engine independent of the UI and model provider so they can be tested with fixtures.

## 6. Authentication and authorization details

There are two authorization steps: an administrator authorizes the server installation, and an individual user authenticates for their own view. An admin's consent to install the bot must not become a blanket permission for all GuildBrief members to see everything the bot can read.

For web sign-in, use Discord's authorization-code flow with validated state and exact registered redirects.[^oauth] For a remote MCP endpoint, use the currently supported MCP/client authorization flow, including the necessary resource metadata, client registration behavior, PKCE, token audience checks, and access-token validation.[^mcp-auth] Validate the flow with the target client before release; do not assume Discord OAuth alone satisfies MCP authentication. The MCP client receives an app-issued, audience-bound token. Discord credentials are used only internally for upstream Discord calls; they are not accepted as the MCP bearer token or passed through to the assistant client.

Create opaque app sessions or appropriately scoped app tokens; bind them to a user and permitted tenant context. Encrypt refresh tokens with managed keys, rotate application secrets, revoke sessions on disconnect, and redact credentials from errors and logs. Bot tokens never leave the server and never appear in model inputs. Store OAuth grants separately from bot installation/configuration records.

The intended bot permissions are `VIEW_CHANNEL` and `READ_MESSAGE_HISTORY`. Request the `bot` installation scope; add `applications.commands` only if a separately tested interaction feature needs it. Use the current user's OAuth member endpoint and on-demand role information rather than enumerating the entire server. Do not request `GUILD_PRESENCES` or the full `GUILD_MEMBERS` intent for the MVP.

Compute member permissions from `@everyone`, applicable roles, administrator/owner cases, and channel overwrites in Discord's documented order.[^permissions] History requires the member and the bot to satisfy both visibility and message-history requirements. Apply the same policy to list, search, fetch, citation previews, and brief generation. Counts and channel names can themselves reveal hidden resources, so access filtering covers metadata as well as message text.

Private-thread access is not established by parent-channel visibility alone.[^threads] The MVP denies it. Public-thread access must map to an approved parent and current visibility. Any inability to resolve membership, channel type, or the parent produces denial. Avoid permission caches during the pilot; if later measurements justify a short cache, document revocation behavior and invalidate it conservatively. Revalidate before returning content even when a request began with valid access.

## 7. Exact MVP tool surface

All six proposed tools are synchronous, bounded retrieval or computation. They do not store output artifacts, start background jobs, send messages, or change Discord state. Proposed annotations are `readOnlyHint: true`, `destructiveHint: false`, and `openWorldHint: false`, because the surface is confined to configured private tenants. Reassess if behavior changes; annotations are descriptive, not authorization.

| Tool | Inputs | Output and limits |
| --- | --- | --- |
| `connection_status` | No user or token parameter | Sign-in state, approved-server connection state, content-access capability, current degradation; no secrets |
| `list_accessible_servers` | Optional opaque cursor | Only enabled servers shared by the member and bot; maximum 25 per page |
| `list_accessible_channels` | `server_id`, optional opaque cursor | Approved channels currently readable by the member and bot; maximum 50 per page |
| `search_messages` | `server_id`, approved `channel_ids`, `query`, `after`, `before`, optional opaque cursor | Maximum 25 authorized hits, source IDs/links, timestamps, bounded excerpts, indexing/truncation status |
| `fetch_message_context` | `server_id`, `channel_id`, `message_id`, `before_count`, `after_count` | Current focal message and at most 10 nearby messages on each side; every result independently filtered |
| `build_event_brief` | `server_id`, approved `channel_ids`, `event_label`, `after`, `before`, `brief_type` (`weekly`, `readiness`, `handoff`) | Structured, nonpersistent brief with evidence, gaps, contradictions, explicit coverage, and request completion time |

Validate server/channel/message IDs as strings and never coerce large IDs into imprecise JavaScript numbers. Restrict dates to valid ranges and reject oversized queries. Bind cursors to the user, tenant, query, and short expiration so one user's pagination token cannot replay another user's access. A guessed ID should not reveal whether an inaccessible resource exists.

`build_event_brief` calls the internal authorized retrieval pipeline, not another plugin. It has its own model-provider configuration and clearly disclosed data recipients if backend inference is enabled. A retrieval-only deployment can omit that capability and let the host synthesize; it must then describe that limited behavior accurately and cannot claim independently validated brief generation. A functioning standalone brief engine helps the product's utility, but does not establish ChatGPT Directory eligibility.

The brief contract contains `coverage`, `decisions`, `tasks`, `proposals`, `contradictions`, `open_questions`, and `evidence`. Each extracted claim has source message IDs. Each task has `owner`, `deadline`, `status`, and corresponding evidence; unsupported fields are `null`. Deadline normalization includes the server's configured timezone and records ambiguous phrases. The system does not equate an author's statement with organizational approval.

## 8. Retrieval fallback and honest coverage

First validate native bot search against a private synthetic test server. If the endpoint is unavailable, returns an unsupported result, or stays unindexed beyond the bounded retry budget, offer a bounded recent-history scan of the selected channels. Use official history pagination and the same content and permission requirements. Label this mode “recent messages scanned,” report the time range and truncation, and do not claim comprehensive server search. Limit a request to a proposed 500-message scan until performance and quota measurements justify another limit.

If `MESSAGE_CONTENT` is unavailable or denied, broad catch-up is unavailable. A selected-message context-menu workflow may support a much smaller explicit-input task within Discord's documented exceptions.[^gateway] User-authored event notes can also be accepted by a standalone workflow with appropriate rights and disclosure. Neither option reconstructs unprovided history, nor is either a route around Discord intent review or OpenAI's unofficial-connector restriction. Never fall back to a user token, scraped export, undocumented endpoint, or browser session extraction.

Search pages, retrieval budgets, missing permissions, removed messages, and unavailable threads appear in the brief's coverage section. “No decision found in the messages reviewed” is distinct from “No decision was made.” For weekly handoffs, prefer a short accurate brief over unsupported completion of every template field.

Handle rate limits with route/bucket queues, parsed response headers, and bounded retries honoring Discord's specified delay.[^rate-limits] Stop requests after revoked credentials or access-denied results until the state is resolved. Return an actionable degraded status when a request cannot finish within its budget; do not keep a user waiting through unbounded retries.

## 9. Retention, disclosure, and deletion

Discord requires collection for stated functionality, prohibits AI training on API message content without express permission, and bars data commercialization and user profiling.[^discord-policy] Use the product to help run events, not to create member dossiers or resell community data. Restrict pilots to planning channels that do not intentionally contain sensitive records, and establish a procedure for excluding or removing accidentally encountered sensitive content.

Discord's terms require a clear privacy policy, permitted data sharing, and accessible modification/deletion requests.[^discord-terms] The following are proposed maximums and operational targets to validate before launch:

| Data category | Proposed handling |
| --- | --- |
| Retrieved message bodies, excerpts, and generated briefs | Transient request memory only; no application database or debug logs |
| OAuth access/refresh tokens | Encrypted while connection is active; revoke and remove on disconnect |
| Channel allowlists and tenant settings | Retain while enabled; erase after uninstall/tenant deletion completes |
| Minimal operational/audit records | Up to 30 days, with purpose disclosed and user identifiers minimized |
| Security logs | Separate access controls and defined retention; no content or credentials |
| Backups | Defined expiry and deletion propagation; no raw message store to back up in MVP |

Provide a website form and in-product deletion/disconnect controls. Disable access immediately on disconnect, complete active-store removal within a proposed 24-hour target, and document backup expiry rather than implying instantaneous deletion everywhere. Legal retention exceptions, if any, need specific justification and disclosure. A stopped service must have a documented tenant-data wind-down process.

Sending content to ChatGPT, another assistant client, or a backend model provider is still processing and disclosure even when GuildBrief itself does not store it. Describe recipients and processing settings accurately. Do not advertise “never used to train AI” for every downstream provider unless the applicable configuration and agreements support that claim. The defensible product statement is limited to GuildBrief's own conduct and verified provider settings.

Revoking source access prevents later requests; it cannot retract a brief already copied by a user or retained by an assistant provider. Explain that boundary and give guidance for deleting provider-side conversations where available. Do not promise end-to-end erasure of copies the service cannot control.

## 10. Evaluation and release acceptance

Use synthetic fixtures for public tests and demos. A private pilot may use consented, appropriately authorized examples with restricted access and a deletion process. Never publish real community conversations or names in the repository.

### Security gate: zero tolerated leaks

The meaningful acceptance suite must cover cross-tenant guessed IDs, expired sessions, removed members, revoked administrator authority for management routes, bot uninstall, member-specific denies, overlapping roles, administrator/owner behavior, permission changes between retrieval and response, inaccessible channels in native search, private threads, forged cursors, and credential redaction. No inaccessible content or metadata may appear in output. A failed security case blocks release regardless of answer-quality metrics.

Include adversarial messages that instruct the assistant to ignore permissions, reveal tokens, search an unapproved channel, or publish the conversation. Retrieval and synthesis must treat those as quoted community content. Test deleted/edited evidence and upstream errors. Verify that every purported read-only tool actually avoids writes and background jobs.

### Answer-quality gate

Create at least 40 synthetic scenarios with independently reviewed expected facts: explicit decisions, proposals that never became decisions, ambiguous owners, missing deadlines, changed event times, contradictory instructions, cancellations, implicit dates, and unrelated chatter. Score individual claims rather than the overall tone of a brief.

Proposed launch thresholds are at least 95% supported-claim precision, at least 90% recall of explicit decisions in the bounded material, zero invented owners/deadlines in the evaluation set, and 100% valid links for cited live fixture messages. Every claim presented as confirmed needs support; unclear evidence must be labeled. These are release targets, not results already achieved. Compare against ordinary Discord search plus a manually written brief so improvement is measured against the real alternative.

### Product and performance gate

Run three to five willing communities through at least four weekly cycles. Target first useful brief within ten minutes of administrator onboarding, median interactive retrieval under five seconds excluding provider outages, and a bounded brief response under 30 seconds for the standard window. Native API rate limits and model latency must be measured before promising these times.[^rate-limits]

Track activated administrators, members who inspect citations, briefs judged usable without substantive corrections, time saved against the participants' existing process, and weekly repeated usage. Define an activated community as one that completes onboarding and produces a rated useful brief; total server membership is not usage. Proceed toward growth only if at least three communities use the workflow in three of four consecutive weeks and at least two articulate a concrete reason to keep it. Otherwise revise the job or stop expansion.

## 11. Pricing hypotheses and cost discipline

Begin with a free, explicitly time-bounded pilot on the standalone product. Test willingness to pay per active organizing team/server, rather than per community member. Initial interview hypotheses, in Canadian dollars, are CAD 9–15/month for a small team and CAD 25–40/month for a heavier organizer group. These figures are proposed experiments, not researched market prices or validated demand. A student-club option may be free or discounted if acquisition/support costs justify it.

Paid value could be additional approved channels, larger bounded analysis windows, or a later handoff archive with a separately reviewed retention model. Do not charge for bypassing Discord access rules or sell underlying message data. Free self-hosting of the retrieval core can build trust; hosting, maintenance, and the independent workflow can be separately evaluated as the paid service.

Budget model-provider spend per completed brief; measure input tokens, output tokens, calls, and retries with content-free usage records. Avoid fetching an entire channel when filtered native search suffices. Set an explicit monthly pilot spend cap, per-tenant request budgets, and visible limit errors. Verify current model prices when choosing an implementation. ChatGPT-host inference and backend inference have different cost and data-flow models; do not count user plan capacity as free backend infrastructure.

Do not display those price hypotheses or sales prompts inside a ChatGPT plugin. Access for an existing subscriber is a separate policy question from promoting or initiating a new subscription.[^openai]

## 12. Implementation milestones and decision gates

| Milestone | Deliverable | Proceed only when |
| --- | --- | --- |
| M0: publication and demand | Eligibility memo, policy review, twelve organizer interviews, synthetic demo storyboard | There is a permitted distribution route and repeated evidence of the event-handoff problem |
| M1: access proof | Test bot, OAuth sign-in, approved channels, official search/history capability results | Required access works without scraping or account automation |
| M2: reliable retrieval | Explicit tools, authorization engine, bounded fallback, citation links | Security scenarios pass and inaccessible resources reveal nothing |
| M3: brief workflow | Extraction contract, contradiction handling, quality evaluation report | Synthetic accuracy thresholds pass with honest coverage |
| M4: private pilot | Three to five communities, four weeks of feedback, deletion and support operations | Retention, usefulness, and support workload justify expansion |
| M5: distribution | Standalone release; optional allowed MCP routes; store submission only if eligible | Product is complete, approvals are satisfied, and claims match deployed behavior |

Use small, reviewable commits tied to milestones: architecture decision record; synthetic permission fixtures; OAuth/session boundaries; authorization engine; native search adapter; bounded-history fallback; citation validation; brief extraction/evaluation; deletion controls; onboarding and documentation. Commit truthful dates and only completed work. The repository should contain design decisions, threat model, synthetic fixtures, evaluation reports, setup instructions, and limitations so a reviewer can assess engineering judgment independently of adoption claims.

Resume claims become stronger after real results: “Built a permission-aware Discord event-handoff assistant with OAuth, scoped retrieval, and citation-backed briefs; evaluated on N scenarios and used by N organizing teams.” Replace N only with measured figures. A planning repository is a valid research/design artifact, but is not a shipped integration or user traction.

## 13. Sources and research limits

All links below are primary sources reviewed on September 29, 2026. Competitor pages establish advertised or documented features; they do not prove production reliability, customer counts, or public-store approval. Discord API capabilities were checked in documentation, not exercised against a live bot in this research stage. Name availability, OpenAI eligibility, Discord intent approval, customer demand, and willingness to pay remain unresolved.

[^openai]: OpenAI, [Plugin Guidelines](https://developers.openai.com/plugins/plugin-guidelines), especially third-party integrations, commerce, privacy, and tool behavior. The unofficial-connector restriction is the publication gate; proposed workflow differentiation is not an exemption.
[^oauth]: Discord, [OAuth2](https://docs.discord.com/developers/topics/oauth2), supported scopes, authorization-code flow, bot accounts, and account-automation restrictions.
[^messages]: Discord, [Message Resource](https://docs.discord.com/developers/resources/message), Get Channel Messages and Search Guild Messages.
[^gateway]: Discord, [Gateway](https://docs.discord.com/developers/events/gateway), privileged intent, HTTP restrictions, message-content fields, and limited exceptions.
[^intent-review]: Discord, [Changes to Privileged Intent Access for Discord Apps](https://support-dev.discord.com/hc/en-us/articles/40281523410967-Changes-to-Privileged-Intent-Access-for-Discord-Apps), June 2026 user threshold, annual review, and separated verification.
[^permissions]: Discord, [Permissions](https://docs.discord.com/developers/topics/permissions), permission bits and overwrite precedence.
[^threads]: Discord, [Threads](https://docs.discord.com/developers/topics/threads), parent inheritance, private-thread access, and archived threads.
[^rate-limits]: Discord, [Rate Limits](https://docs.discord.com/developers/topics/rate-limits), response headers, bucket behavior, and retry guidance.
[^discord-policy]: Discord, [Developer Policy](https://support-dev.discord.com/hc/en-us/articles/8563934450327-Discord-Developer-Policy), stated functionality, profiling, commercialization, scraping, and AI-training restrictions.
[^discord-terms]: Discord, [Developer Terms of Service](https://support-dev.discord.com/hc/en-us/articles/8562894815383-Discord-Developer-Terms-of-Service), privacy policy, permitted sharing, retention, deletion, and publicity.
[^composio]: Composio, [How to connect Discord MCP with ChatGPT](https://composio.dev/toolkits/discord/framework/chatgpt). The concrete examples emphasize user identity/server metadata; broad message-summary marketing was not verified by a live integration.
[^merge]: Merge, [Discord MCP Server](https://www.merge.dev/connectors/discord), documented bot history/search and broader management tool surface.
[^guildbridge]: GitHub, [dend/guildbridge](https://github.com/dend/guildbridge), self-hosted remote MCP reference with OAuth, bot-token access, permission checks, and metadata audit logging. Hosted access is described as restricted.
[^pasympa]: GitHub, [PaSympa/discord-mcp](https://github.com/PaSympa/discord-mcp), broad bot management/retrieval tools and npm/Docker distribution. Tool breadth is already available elsewhere.
[^mcp-auth]: Model Context Protocol, [Authorization specification, July 28, 2026](https://modelcontextprotocol.io/specification/2026-07-28/basic/authorization), resource-server roles, metadata discovery, client registration, resource indicators, and audience-bound access tokens. Pin an implemented protocol version and test client compatibility before release.
