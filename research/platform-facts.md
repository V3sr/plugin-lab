# Platform facts and uncertainties

Verified date: 2026-09-29. Recheck before implementing, distributing or submitting. These platforms are changing; sources describe capability, not approval of this proposed product.

## Current OpenAI plugin system

OpenAI announced improved plugin creation, submission and discovery at DevDay on September 29, 2026. Its docs describe a universal ChatGPT/Codex directory and packages containing skills, MCP and optional UI/hooks. This is the current system, not the older 2023 plugin manifest flow. [Announcement](https://openai.com/index/devday-2026-recap/) · [Architecture](https://developers.openai.com/plugins/concepts/plugins)

Public submissions are open. A verified publishing identity uploads a ZIP, resolves automated findings, supplies review material and publishes after approval. An MCP integration needs a publicly reachable production HTTPS service and reviewer access. One MCP can be connected per submitted plugin. [Submission](https://developers.openai.com/plugins/deploy/submission)

Portable packages use root `plugin.json`, optional `skills/` and `mcp.json`, plus OpenAI settings in `extensions.com.openai`. Compatibility layouts remain supported. Public publication and local/repository marketplaces are separate. Developer-mode connection availability varies by account and workspace. [Packaging](https://developers.openai.com/plugins/build/plugins) · [Testing](https://developers.openai.com/plugins/deploy/connect-chatgpt)

## Eligibility and business constraints

OpenAI currently restricts plugins whose primary role is unofficial third-party connectivity. GuildBrief eligibility is unresolved; adding workflow features does not guarantee approval. Integration authorization is separate from store review. Plugins cannot serve ads or sell/upsell digital subscriptions inside the experience; existing paid entitlements may be accessed. Store metadata must be accurate. [Guidelines](https://developers.openai.com/plugins/plugin-guidelines)

Recommendation: request specific guidance early, then document the response. Until then, store publication is conditional. Private testing, self-hosting and other MCP clients remain subject to their own rules and Discord authorization; they are not a bypass for a rejected integration.

## Discord access essentials

Normal user OAuth establishes identity and server membership, not arbitrary personal message access. A server-installed bot is needed for the proposed history workflow. The current Message API documents bot guild search, subject to access and content-intent requirements. The permissions of the bot and of the requesting human must both be checked. [OAuth](https://docs.discord.com/developers/topics/oauth2) · [Messages](https://docs.discord.com/developers/resources/message) · [Permissions](https://docs.discord.com/developers/topics/permissions)

The June 10, 2026 intent-policy update uses **10,000 reachable unique users**, rather than the old server-count rule, for privileged-intent review and requires annual reapplication. App verification is separate. Recheck total eligible reach before expanding. [Current intent policy](https://support-dev.discord.com/hc/en-us/articles/40281523410967-Changes-to-Privileged-Intent-Access-for-Discord-Apps)

No live bot/API proof has been completed in this research. A technical spike must verify scopes, native search, history, user authorization and failure modes. Details and release criteria belong in [the product plan](../docs/discord-product-plan.md).

## Competitor evidence

Discord connectivity and summaries are established categories: [Merge](https://www.merge.dev/connectors/discord), [GuildBridge](https://github.com/dend/guildbridge), [read-only Discord MCP](https://github.com/Vorakorn1001/discord-readonly-mcp), [Answer Overflow](https://github.com/AnswerOverflow/AnswerOverflow), [SummaryBot](https://discordsummarybot.com/features), and [Discord's native experimental summaries](https://support.discord.com/hc/en-us/articles/12926016807575-In-Channel-Conversation-Summaries).

Primary product pages establish advertised capabilities, not verified reliability, customer numbers or revenue. No competitor was installed or benchmarked during this work.

## Catalog observation

Read-only inspection of the user's live `chatgpt.com/plugins` page showed public and personal tabs and a broad featured catalog, including Slack, Teams, GitHub, vidIQ, Higgsfield and multiple research tools. A search for Discord did not display a Discord-named result; the visible result was an unrelated Vercel listing. Other focused queries also returned Vercel, so these search observations are insufficient for a comprehensive absence claim. Do not advertise “first Discord plugin” or infer an empty market from them.

The plugin-management discovery search function was not exposed in this session; the live UI plus primary provider evidence were used. This is a scoped research snapshot, not an exhaustive marketplace census.

## Outstanding questions

- Would OpenAI approve the exact proposed original workflow and integration relationship?
- Does Discord permit the proposed third-party inference/data flow under the relevant terms and configurations?
- Can pilot servers authorize the bot and provide transparent member notice?
- Does the intended audience prefer an assistant plugin, Discord command or standalone workflow?
- Will native search and content-intent access work for the initial app? How does review timing affect expansion?
- Which packaging/testing capabilities are available to each intended user account?
- Are the tentative names available? No domain, npm namespace or trademark availability has been established.

Resolve these before presenting the product as publicly available.
