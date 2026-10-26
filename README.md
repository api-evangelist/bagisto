# Bagisto (bagisto)

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

Bagisto is a free and open-source Laravel e-commerce platform that provides REST and GraphQL APIs for managing products, categories, customers, orders, inventory, carts, and multi-channel selling. Built on Laravel Sanctum, the API offers both a public Storefront API and a full-control Admin API, making it suitable for headless commerce, mobile apps, and third-party integrations.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/bagisto/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/bagisto/refs/heads/main/apis.yml)

## Tags

- E-Commerce
- Laravel
- Open Source
- Products
- Orders
- Customers
- Inventory
- Multi-Channel
- Headless Commerce

## Timestamps

- **Created:** 2026-06-13
- **Modified:** 2026-06-13

## APIs

### Bagisto REST API

RESTful API for managing all Bagisto e-commerce operations including products, categories, customers, orders, inventory, cart, checkout, and administrative functions. Provides separate Shop and Admin API namespaces secured with Laravel Sanctum tokens.

- **Human URL:** [https://api-docs.bagisto.com/api/rest-api/introduction.html](https://api-docs.bagisto.com/api/rest-api/introduction.html)
- **Base URL:** `https://{your-domain}/api/`

#### Tags

- E-Commerce
- Products
- Orders
- Customers
- Inventory
- Cart
- REST

#### Properties

- [Documentation](https://api-docs.bagisto.com/api/rest-api/introduction.html)
- [Authentication](https://api-docs.bagisto.com/api/authentication)
- [OpenAPI](https://devdocs.bagisto.com/api/rest-api.html) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Bagisto GraphQL API

GraphQL API for Bagisto providing flexible query-based access to storefront and catalog data as an alternative to the REST API.

- **Human URL:** [https://devdocs.bagisto.com/api/graphql-api](https://devdocs.bagisto.com/api/graphql-api)
- **Base URL:** `https://{your-domain}/graphql`

#### Tags

- E-Commerce
- GraphQL
- Products
- Catalog

#### Properties

- [Documentation](https://devdocs.bagisto.com/api/graphql-api)
- [Graph Q L](graphql/bagisto-graphql.md)

## Common Properties

- [Website](https://bagisto.com/en/)
- [Documentation](https://devdocs.bagisto.com/)
- [Git Hub Org](https://github.com/bagisto)
- [GitHub Repository](https://github.com/bagisto/bagisto)
- [GitHub Repository](https://github.com/bagisto/rest-api)
- [LinkedIn](https://www.linkedin.com/company/bagisto/)
- [Blog](https://bagisto.com/en/blog/)
- [Pricing](https://bagisto.com/en/cloud-hosting/)
- [X (Twitter)](https://x.com/BagistoShop)
- [Forum](https://forums.bagisto.com/)
- [Plans](plans/bagisto-plans-pricing.yml)
- [Rate Limits](rate-limits/bagisto-rate-limits.yml)
- [Fin Ops](finops/bagisto-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
