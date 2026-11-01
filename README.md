# Zerion

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Zerion is an Ethereum and Solana wallet and developer platform focused on making onchain data easy to use. The Zerion API delivers clean, normalized wallet data, token analytics, DeFi positions, transaction history, PnL, NFTs, gas prices, swap and bridge quotes, and real-time transaction webhooks across EVM chains and Solana. The same infrastructure powers the Zerion wallet app used by millions. It is a JSON:API REST service with HTTP Basic (API key) authentication plus pay-per-request x402 (Base/Solana USDC) and MPP (Tempo USDC) options aimed at AI agents, an open-source CLI, six packaged agent skills, a hosted MCP server, and Kafka streaming for high-throughput pipelines.

**Areas:** Company · Web3 · Blockchain · Cryptocurrency · DeFi · Wallets · NFT · Ethereum · Solana · Portfolio · On-Chain Data · Transaction

## Zerion on APIs.io

Everything profiled for Zerion is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/zerion/](https://apis.io/providers/zerion/)** — or go straight to one of the APIs or properties below.

### APIs (9)

- [Zerion Chains API](https://apis.io/apis/zerion/zerion-chains-api/) — Operations related to chains, such as list all chains.
- [Zerion Dapps API](https://apis.io/apis/zerion/zerion-dapps-api/) — Operations related to decentralized applications, such as list them all, search or get by ID.
- [Zerion Fungibles API](https://apis.io/apis/zerion/zerion-fungibles-api/) — Operations related to fungible assets, such as list them all, search or get by ID.
- [Zerion Gas API](https://apis.io/apis/zerion/zerion-gas-api/) — Operations related to gas.
- [Zerion subscriptions to transactions API](https://apis.io/apis/zerion/zerion-subscriptions-to-transactions-api/) — Operations related to subscriptions to transactions.
- [Zerion Swap API](https://apis.io/apis/zerion/zerion-swap-api/) — Operations related to swapping and bridging assets.
- [Zerion wallet sets API](https://apis.io/apis/zerion/zerion-wallet-sets-api/) — Operations on a wallet set — aggregated portfolio data across at most one EVM address and one Solana address queried together.
- [Zerion Wallets API](https://apis.io/apis/zerion/zerion-wallets-api/) — Operations related to wallets, such as portfolio charts, positions, and transactions.
- [Zerion Nfts API](https://apis.io/apis/zerion/zerion-nfts-api/) — Operations related to non fungible assets, such list them, search or get by ID.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Arazzo workflows (2)

Multi-step workflows that chain operations into a business task.

- [Zerion wallet activity subscription](https://apis.io/arazzos/zerion/zerion-wallet-activity-subscription.arazzo/)
- [Zerion wallet overview](https://apis.io/arazzos/zerion/zerion-wallet-overview.arazzo/)

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Zerion Transactions Webhooks](https://apis.io/asyncapis/zerion/zerion-transactions-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [zerion-api](https://apis.io/servers/zerion/zerion-api/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Zerion Agentic Access](https://apis.io/agentic-access/zerion/zerion-agentic-access/)

#### Collections (18)

Postman and Open Collection request collections.

- [REST chains API](https://apis.io/collections/zerion/open-zerion-chains-api/)
- [REST chains dapps API](https://apis.io/collections/zerion/open-zerion-dapps-api/)
- [REST chains fungibles API](https://apis.io/collections/zerion/open-zerion-fungibles-api/)
- [REST chains gas API](https://apis.io/collections/zerion/open-zerion-gas-api/)
- [REST chains nfts API](https://apis.io/collections/zerion/open-zerion-nfts-api/)
- [REST chains subscriptions to transactions API](https://apis.io/collections/zerion/open-zerion-subscriptions-to-transactions-api/)
- [REST chains swap API](https://apis.io/collections/zerion/open-zerion-swap-api/)
- [REST chains wallet sets API](https://apis.io/collections/zerion/open-zerion-wallet-sets-api/)
- [REST chains wallets API](https://apis.io/collections/zerion/open-zerion-wallets-api/)
- [REST chains API](https://apis.io/collections/zerion/postman-zerion-chains-api/)
- [REST chains dapps API](https://apis.io/collections/zerion/postman-zerion-dapps-api/)
- [REST chains fungibles API](https://apis.io/collections/zerion/postman-zerion-fungibles-api/)
- [REST chains gas API](https://apis.io/collections/zerion/postman-zerion-gas-api/)
- [REST chains nfts API](https://apis.io/collections/zerion/postman-zerion-nfts-api/)
- [REST chains subscriptions to transactions API](https://apis.io/collections/zerion/postman-zerion-subscriptions-to-transactions-api/)
- [REST chains swap API](https://apis.io/collections/zerion/postman-zerion-swap-api/)
- [REST chains wallet sets API](https://apis.io/collections/zerion/postman-zerion-wallet-sets-api/)
- [REST chains wallets API](https://apis.io/collections/zerion/postman-zerion-wallets-api/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Zerion Api Overlay](https://apis.io/overlays/zerion/zerion-api-overlay/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Zerion Authentication](https://apis.io/security/zerion/zerion-authentication/)
- [Zerion Domain Security](https://apis.io/security/zerion/zerion-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Zerion Plans](https://apis.io/plans/zerion/zerion-plans/)

#### Rate limits (1)

Published request limits.

- [Zerion Rate Limits](https://apis.io/rate-limits/zerion/zerion-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.zerion.io/)
- [Documentation](https://developers.zerion.io/)
- [Getting started](https://developers.zerion.io/quickstart)
- [API reference](https://developers.zerion.io/api-reference/wallets/get-wallet-portfolio)
- [Pricing](https://developers.zerion.io/pricing)
- [Sign up](https://dashboard.zerion.io)
- [Blog](https://zerion.io/blog/tag/zerion-api/)
- [Terms of service](https://zerion.io/terms)
- [Privacy policy](https://zerion.io/privacy)
- [GitHub](https://github.com/zeriontech)

## API Evangelist rating

**Kin Score 60.8** — strong · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 75.0 |
| Contract quality | 59.9 |
| Contract governance | 4.5 |
| Operational transparency | 68.4 |
| Developer ergonomics | 69.6 |
| Access clarity | 76.3 |

**Agent readiness 38.6** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | platform (partial credit) |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | documented (partial credit) |
| OpenAPI Examples | partial |
| Rate Limit Signal | verified |
| Event Surface Described | yes |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | paginated |
| Operation Distinctiveness | distinct |

**Regulatory alignment 22.3** — Payments

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/zerion/](https://apis.io/providers/zerion/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Zerion: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/zerion/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
