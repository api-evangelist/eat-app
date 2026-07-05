# Eat App (eat-app)

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
