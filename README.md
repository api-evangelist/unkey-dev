# Unkey (unkey-dev)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Unkey is an open-source developer platform for modern APIs, providing globally distributed API key management, authentication, and rate limiting. The platform lets API providers issue, verify, update, reroll, and revoke keys with metadata, expiration, usage credits, permissions, and roles, plus standalone rate limiting, identities, RBAC, and key-verification analytics. Unkey exposes an RPC-style REST API (all operations use POST) with a stable v2 at `https://api.unkey.com` and a legacy v1 at `https://api.unkey.dev`, authenticated with Bearer root keys.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/unkey-dev/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/unkey-dev/refs/heads/main/apis.yml)

> Note: A separate `unkey` entry already exists in this catalog under the slug `unkey`. This `unkey-dev` entry is a distinct, freshly researched build with a per-namespace APIs breakdown grounded in Unkey's published v2 OpenAPI; the two overlap in subject matter by design.

## Tags

- API Keys
- Rate Limiting
- Authentication
- Access Control
- Identity
- RBAC
- Analytics
- Open Source

## Timestamps

- **Created:** 2026-07-02
- **Modified:** 2026-07-02

## APIs

### Unkey Keys API

Full API key lifecycle - create, verify, get, update, delete, reroll, updateCredits, and whoami. Keys carry metadata, expiration, usage credits, external identity links, permissions, and roles. `keys.verifyKey` is the hot-path endpoint API providers call to authenticate and authorize each request.

- **Human URL:** [https://www.unkey.com/docs/api-reference/keys/create](https://www.unkey.com/docs/api-reference/keys/create)
- **Base URL:** `https://api.unkey.com`

#### Tags

- API Keys
- Verification
- Lifecycle

#### Properties

- [Documentation](https://www.unkey.com/docs/api-reference/overview)
- [API Reference](https://www.unkey.com/docs/api-reference/keys/create)
- [OpenAPI](openapi/unkey-dev-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/unkey-dev.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/unkey-dev.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Unkey APIs (Namespaces) API

Manage APIs - the namespaces (keyspaces) that group and isolate keys. Create, get, and delete an API, and list all keys belonging to it. Each API is the container against which keys are issued and verified.

- **Human URL:** [https://www.unkey.com/docs/api-reference/apis/create](https://www.unkey.com/docs/api-reference/apis/create)
- **Base URL:** `https://api.unkey.com`

#### Tags

- Namespaces
- API Management
- Keyspaces

#### Properties

- [API Reference](https://www.unkey.com/docs/api-reference/apis/create)
- [OpenAPI](openapi/unkey-dev-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/unkey-dev.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/unkey-dev.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Unkey Ratelimit API

Standalone, key-independent rate limiting. Check or enforce a limit for any identifier (`ratelimit.limit`), evaluate several limits at once (`multiLimit`), and manage per-identifier overrides within a namespace (set, get, list, delete override).

- **Human URL:** [https://www.unkey.com/docs/api-reference/ratelimits/limit](https://www.unkey.com/docs/api-reference/ratelimits/limit)
- **Base URL:** `https://api.unkey.com`

#### Tags

- Rate Limiting
- Overrides
- Namespaces

#### Properties

- [API Reference](https://www.unkey.com/docs/api-reference/ratelimits/limit)
- [OpenAPI](openapi/unkey-dev-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/unkey-dev.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/unkey-dev.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Unkey Identities API

Model your users, tenants, or organizations as identities and attach multiple keys and shared rate limits to each via an `externalId`. Create, get, list, update, and delete identities so limits and metadata follow the entity rather than a single key.

- **Human URL:** [https://www.unkey.com/docs/api-reference/identities/create-identity](https://www.unkey.com/docs/api-reference/identities/create-identity)
- **Base URL:** `https://api.unkey.com`

#### Tags

- Identities
- Tenants
- Users

#### Properties

- [API Reference](https://www.unkey.com/docs/api-reference/identities/create-identity)
- [OpenAPI](openapi/unkey-dev-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/unkey-dev.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/unkey-dev.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Unkey Permissions and Roles API

Role-based access control. Define permissions and roles and manage their lifecycle (create, get, list, delete), then attach or detach them on keys with the `keys.addPermissions` / `setPermissions` / `addRoles` / `setRoles` family so `verifyKey` can enforce fine-grained authorization.

- **Human URL:** [https://www.unkey.com/docs/api-reference/permissions/create-permission](https://www.unkey.com/docs/api-reference/permissions/create-permission)
- **Base URL:** `https://api.unkey.com`

#### Tags

- RBAC
- Permissions
- Roles

#### Properties

- [API Reference](https://www.unkey.com/docs/api-reference/permissions/create-permission)
- [OpenAPI](openapi/unkey-dev-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/unkey-dev.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/unkey-dev.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Unkey Analytics API

Query key-verification analytics (`analytics.getVerifications`) to understand usage over time, by key, identity, or outcome. Powers usage dashboards, billing, and abuse detection built on top of Unkey verifications.

- **Human URL:** [https://www.unkey.com/docs/api-reference/analytics/get-verifications](https://www.unkey.com/docs/api-reference/analytics/get-verifications)
- **Base URL:** `https://api.unkey.com`

#### Tags

- Analytics
- Verifications
- Usage

#### Properties

- [API Reference](https://www.unkey.com/docs/api-reference/analytics/get-verifications)
- [OpenAPI](openapi/unkey-dev-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/unkey-dev.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/unkey-dev.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Unkey Key Migrations API

Bulk-import existing keys from another system into an Unkey namespace via `keys.migrateKeys`, letting providers move onto Unkey without forcing every customer to rotate their key.

- **Human URL:** [https://www.unkey.com/docs/api-reference/keys/create](https://www.unkey.com/docs/api-reference/keys/create)
- **Base URL:** `https://api.unkey.com`

#### Tags

- Migration
- Import
- Bulk

#### Properties

- [API Reference](https://www.unkey.com/docs/api-reference/keys/create)
- [OpenAPI](openapi/unkey-dev-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/unkey-dev.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/unkey-dev.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Unkey Deploy API

Deployment operations (`deploy.createDeployment`, `deploy.getDeployment`) from Unkey's newer "ship APIs, not infrastructure" deploy platform, exposed in the v2 API alongside the key-management surface.

- **Human URL:** [https://www.unkey.com/docs/api-reference/overview](https://www.unkey.com/docs/api-reference/overview)
- **Base URL:** `https://api.unkey.com`

#### Tags

- Deployments
- Platform

#### Properties

- [API Reference](https://www.unkey.com/docs/api-reference/overview)
- [OpenAPI](openapi/unkey-dev-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/unkey-dev.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/unkey-dev.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Unkey Liveness API

Simple health-check endpoint (`liveness`) for verifying API availability from monitors and load balancers.

- **Human URL:** [https://www.unkey.com/docs/api-reference/overview](https://www.unkey.com/docs/api-reference/overview)
- **Base URL:** `https://api.unkey.com`

#### Tags

- Health
- Monitoring

#### Properties

- [API Reference](https://www.unkey.com/docs/api-reference/overview)
- [OpenAPI](openapi/unkey-dev-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/unkey-dev.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/unkey-dev.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/unkeyed)
- [LinkedIn](https://www.linkedin.com/company/unkeyed)
- [Website](https://www.unkey.com)
- [Documentation](https://www.unkey.com/docs)
- [Plans](plans/unkey-dev-plans-pricing.yml)
- [Rate Limits](rate-limits/unkey-dev-rate-limits.yml)
- [Fin Ops](finops/unkey-dev-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
