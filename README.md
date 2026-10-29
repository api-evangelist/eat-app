# Eat App

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

Eat App is a restaurant reservation and table management platform used by restaurants and restaurant groups to take bookings, manage floor plans and tables, build guest CRM profiles, and run front-of-house operations. Its developer surface is a partner/key-gated REST platform - a Partner API for booking channels to read availability and post reservations, and a Concierge API for restaurants, vendors, and groups to sync reservations, guests, availability, restaurants, and groups. Both use JSON:API-style responses, Bearer-token authentication, and an api.eat-sandbox.co sandbox mirroring api.eatapp.co production. Eat App also exposes a Restaurant MCP server for connecting AI assistants. API access is granted on request rather than fully self-serve.

**Areas:** Restaurant · Reservations · Table Management · Hospitality · Booking · Guest CRM · Availability

## Eat App on APIs.io

Everything profiled for Eat App is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/eat-app/](https://apis.io/providers/eat-app/)** — or go straight to one of the APIs or properties below.

### APIs (7)

- [Eat App Concierge - Availability API](https://apis.io/apis/eat-app/eat-app-concierge-availability-api/) — Concierge bookable time-slot lookups over a date range.
- [Eat App Concierge - Guests API](https://apis.io/apis/eat-app/eat-app-concierge-guests-api/) — Concierge guest search and profile retrieval.
- [Eat App Concierge - Reference API](https://apis.io/apis/eat-app/eat-app-concierge-reference-api/) — Concierge bootstrap data - resources, groups, restaurants.
- [Eat App Concierge - Reservations API](https://apis.io/apis/eat-app/eat-app-concierge-reservations-api/) — Concierge reservation create, list, get, and update/cancel.
- [Eat App Partner - Availability API](https://apis.io/apis/eat-app/eat-app-partner-availability-api/) — Partner API real-time availability lookups.
- [Eat App Partner - Reservations API](https://apis.io/apis/eat-app/eat-app-partner-reservations-api/) — Partner API reservation creation.
- [Eat App Tables and Floor Plans (Modeled) API](https://apis.io/apis/eat-app/eat-app-tables-and-floor-plans-modeled-api/) — Honestly-modeled table and floor-plan operations. Not documented in the public Partner or Concierge references; confirm before use.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Eat App Agentic Access](https://apis.io/agentic-access/eat-app/eat-app-agentic-access/)

#### Collections (7)

Postman and Open Collection request collections.

- [Eat App Platform Concierge - Availability API](https://apis.io/collections/eat-app/open-eat-app-concierge-availability-api/)
- [Eat App Platform Concierge - Availability Concierge - Guests API](https://apis.io/collections/eat-app/open-eat-app-concierge-guests-api/)
- [Eat App Platform Concierge - Availability Concierge - Reference API](https://apis.io/collections/eat-app/open-eat-app-concierge-reference-api/)
- [Eat App Platform Concierge - Availability Concierge - Reservations API](https://apis.io/collections/eat-app/open-eat-app-concierge-reservations-api/)
- [Eat App Platform Concierge - Availability Partner - Availability API](https://apis.io/collections/eat-app/open-eat-app-partner-availability-api/)
- [Eat App Platform Concierge - Availability Partner - Reservations API](https://apis.io/collections/eat-app/open-eat-app-partner-reservations-api/)
- [Eat App Platform Concierge - Availability Tables and Floor Plans (Modeled) API](https://apis.io/collections/eat-app/open-eat-app-tables-and-floor-plans-modeled-api/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Eat App Authentication](https://apis.io/security/eat-app/eat-app-authentication/)
- [Eat App Domain Security](https://apis.io/security/eat-app/eat-app-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Eat App Plans Pricing](https://apis.io/plans/eat-app/eat-app-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Eat App Rate Limits](https://apis.io/rate-limits/eat-app/eat-app-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Eat App Finops](https://apis.io/finops/eat-app/eat-app-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://eatapp.co)
- [Documentation](https://restaurant.eatapp.co/knowledge/documentation)
- [Sign up](https://eatapp.co/integrations)
- [Blog](https://restaurant.eatapp.co/blog)
- [GitHub](https://github.com/eatapp)

## API Evangelist rating

**Kin Score 30.1** — thin · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 66.1 |
| Contract quality | 50.7 |
| Contract governance | 0.0 |
| Operational transparency | 10.5 |
| Developer ergonomics | 32.1 |
| Access clarity | 21.1 |

**Agent readiness 26.1** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | verified |
| Error Semantics | — |
| OpenAPI Examples | — |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 11.8** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/eat-app/](https://apis.io/providers/eat-app/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Eat App: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/eat-app/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
