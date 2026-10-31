# Openhandle

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

Openhandle is a public social data API for Instagram, TikTok, X (Twitter), and Reddit. Public profiles, posts, comments, followers, and search come back in one normalized schema, with a capture time and a source on every answer and nulls where a platform hides a value. Pricing is per answered request with cheaper cached tiers (free at 30 days), caps per account and per key, and a full Test environment on synthetic data at $0.000. The API is read-only over OpenAPI 3.1, three first-party SDKs (TypeScript, Python, Go), and a remote OAuth-protected MCP server. Operated as a Netherlands sole proprietorship (KvK 89247647).

**Areas:** Social Data · Instagram · TikTok · twitter · Reddit · Public Data · social-media-api · MCP · creator-analytics · Social Listening

## Openhandle on APIs.io

Everything profiled for Openhandle is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/openhandle/](https://apis.io/providers/openhandle/)** — or go straight to one of the APIs or properties below.

### APIs (6)

- [Openhandle Instagram API](https://apis.io/apis/openhandle/openhandle-instagram-api/) — The Instagram API from Openhandle — 43 operation(s) for instagram.
- [Openhandle Reddit API](https://apis.io/apis/openhandle/openhandle-reddit-api/) — The Reddit API from Openhandle — 20 operation(s) for reddit.
- [Openhandle Test Data API](https://apis.io/apis/openhandle/openhandle-test-data-api/) — The Test Data API from Openhandle — 2 operation(s) for test data.
- [Openhandle Tiktok API](https://apis.io/apis/openhandle/openhandle-tiktok-api/) — The Tiktok API from Openhandle — 28 operation(s) for tiktok.
- [Openhandle Twitter API](https://apis.io/apis/openhandle/openhandle-twitter-api/) — The Twitter API from Openhandle — 15 operation(s) for twitter.
- [Openhandle Utilities API](https://apis.io/apis/openhandle/openhandle-utilities-api/) — The Utilities API from Openhandle — 1 operation(s) for utilities.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [Openhandle](https://apis.io/servers/openhandle/dev-openhandle-social-data/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Openhandle Agentic Access](https://apis.io/agentic-access/openhandle/openhandle-agentic-access/)

#### JSON Schema (6)

The data models the API reads and writes.

- [InstagramPost](https://apis.io/schemas/openhandle/openhandle-instagram-post/)
- [InstagramProfile](https://apis.io/schemas/openhandle/openhandle-instagram-profile/)
- [InstagramStory](https://apis.io/schemas/openhandle/openhandle-instagram-story/)
- [TikTokMusic](https://apis.io/schemas/openhandle/openhandle-tik-tok-music/)
- [TikTokPost](https://apis.io/schemas/openhandle/openhandle-tik-tok-post/)
- [TikTokProfile](https://apis.io/schemas/openhandle/openhandle-tik-tok-profile/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Openhandle Context](https://apis.io/jsonld/openhandle/openhandle-context/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Openhandle Openapi Overlay](https://apis.io/overlays/openhandle/openhandle-openapi-overlay/)

#### Governance rules (1)

Spectral rulesets for the provider's contracts.

- [Openhandle API Rules](https://apis.io/rules/openhandle/openhandle-rules/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Openhandle Authentication](https://apis.io/security/openhandle/openhandle-authentication/)
- [Openhandle Domain Security](https://apis.io/security/openhandle/openhandle-domain-security/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Openhandle Scopes](https://apis.io/scopes/openhandle/openhandle-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Openhandle Plans Pricing](https://apis.io/plans/openhandle/openhandle-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Openhandle Rate Limits](https://apis.io/rate-limits/openhandle/openhandle-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://openhandle.dev)
- [Documentation](https://openhandle.dev/docs)
- [Pricing](https://openhandle.dev/pricing)
- [Sign up](https://app.openhandle.dev)
- [Support](https://openhandle.dev/contact)
- [Terms of service](https://openhandle.dev/legal/terms-of-service)
- [Privacy policy](https://openhandle.dev/legal/privacy-policy)
- [GitHub](https://github.com/openhandlehq)

## API Evangelist rating

**Kin Score 61.7** — strong · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 75.0 |
| Contract quality | 66.0 |
| Contract governance | 35.6 |
| Operational transparency | 26.3 |
| Developer ergonomics | 61.3 |
| Access clarity | 76.3 |

**Agent readiness 54.6** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | documented (partial credit) |
| Auth Clarity | served (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | verified |
| Rate Limit Signal | verified |
| Event Surface Described | — |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | served (partial credit) |
| Protected Resource Metadata | verified |
| Dynamic Client Registration | yes |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | distinct |

**Regulatory alignment 34.3** — Government & Public Sector

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/openhandle/](https://apis.io/providers/openhandle/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Openhandle: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/openhandle/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
