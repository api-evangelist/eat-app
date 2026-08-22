# Eat App (eat-app)

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

Eat App is a restaurant reservation and table management platform used by restaurants and restaurant groups to take bookings, manage floor plans and tables, build guest CRM profiles, and run front-of-house operations. Its developer surface is a **partner/key-gated** REST platform: a **Partner API** for booking channels to read availability and post reservations, and a **Concierge API** for restaurants, vendors, and groups to sync reservations, guests, availability, and reference data. Both use JSON:API-style responses, Bearer-token authentication, and a sandbox host (`api.eat-sandbox.co`) that mirrors production (`api.eatapp.co`). Eat App also exposes a **Restaurant MCP** server for connecting AI assistants.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/eat-app/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/eat-app/refs/heads/main/apis.yml)

## Access Model (Honest Note)

Eat App's API is **documented but not fully self-serve**. The Partner and Concierge APIs are publicly documented (Eat App Help Center plus a published Postman documenter), but an **API key is issued by Eat App as part of custom-integration / partner onboarding** - the integrations FAQ says to "reach out to learn how you can gain access to your reservations and guests through our open API." There is no public developer signup that mints a key without contact. Endpoints for **Reservations, Guests, Availability**, and reference data (**Resources / Groups / Restaurants**) are confirmed from the public docs. **Tables and floor plans** are core to the product but have **no documented public endpoints**; those operations are honestly modeled here and flagged as `endpointsModeled` - confirm them against a live partner key before use.

## Tags

- Restaurant
- Reservations
- Table Management
- Hospitality
- Bookings
- Guest CRM
- Availability

## Timestamps

- **Created:** 2026-07-05
- **Modified:** 2026-07-05

## APIs

### Eat App Partner API

Partner-facing API for booking platforms and reservation channels to query real-time availability and post reservations. JSON:API responses, Bearer auth, ~60 requests/minute. Endpoints confirmed from public docs.

- **Base URL:** `https://api.eatapp.co/partners/v2` (sandbox `https://api.eat-sandbox.co/partners/v2`)
- `GET /availability`
- `POST /reservations`

### Eat App Concierge Reservations API

Create, list, retrieve, and modify/cancel reservations across a restaurant group. Create requires `X-Restaurant-ID` and an `idempotency_token`. Endpoints confirmed from public docs.

- **Base URL:** `https://api.eatapp.co/concierge/v2`
- `GET /reservations`, `POST /reservations`, `GET /reservations/{id_or_key}`, `PATCH /reservations/{id_or_key}`

### Eat App Concierge Guests API

Search the guest CRM and retrieve individual guest profiles. Endpoints confirmed from public docs.

- `GET /guests`, `GET /guests/{guest_id}`

### Eat App Concierge Availability API

Query bookable time slots for a restaurant across a date range. Endpoint confirmed from public docs.

- `POST /availability/range`

### Eat App Concierge Restaurants and Groups API

Bootstrap and reference surface - reference data, accessible groups, and restaurants within a group (via `X-Group-ID`). Endpoints confirmed from public docs.

- `GET /resources`, `GET /groups`, `GET /restaurants`

### Eat App Tables and Floorplan API (Modeled)

Table and floor-plan management is core to the platform but has **no documented public endpoints**. The operations below are honestly modeled on Eat App's documented conventions and marked `endpointsModeled` - confirm before use.

- `GET /tables`, `GET /tables/{table_id}`, `GET /floor_plans` (MODELED)

## Common Properties

- [GitHub Organization](https://github.com/eatapp)
- [LinkedIn](https://www.linkedin.com/company/eat-app)
- [Website](https://eatapp.co)
- [Documentation](https://restaurant.eatapp.co/knowledge/documentation)
- [Sign Up / Integrations](https://eatapp.co/integrations)
- [Plans](plans/eat-app-plans-pricing.yml)
- [Rate Limits](rate-limits/eat-app-rate-limits.yml)
- [Fin Ops](finops/eat-app-finops.yml)
- [Blog](https://restaurant.eatapp.co/blog)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
