# Reform

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

Reform is a developer-first, conversion-optimized form builder with a REST API for creating type-safe forms, managing form definitions, collecting submissions, and embedding forms in web applications including React. It offers headless form capabilities, webhooks, and deep integrations with CRMs and marketing platforms.

## Links

- **Website:** https://www.reform.app/
- **Documentation:** https://docs.reform.app/
- **Pricing:** https://www.reform.app/pricing
- **Blog:** https://www.reform.app/blog
- **LinkedIn:** https://www.linkedin.com/company/reformapp
- **X:** https://x.com/heyreform

## APIs.json

This repository contains an APIs.json profile for Reform, cataloging its public API surface and associated resources.

- [apis.yml](apis.yml) — Main APIs.json index
- [llms/reform-llms.txt](llms/reform-llms.txt) — Reform's own llms.txt, saved verbatim from https://www.reform.app/llms.txt
- [asyncapi/reform-webhooks.yml](asyncapi/reform-webhooks.yml) — The `form.submitted` webhook contract (HMAC-SHA256 `Signature` header)
- [components/reform-components.yml](components/reform-components.yml) — Embed loader, hosted forms, headless forms, and the two event APIs
- [packages/reform-packages.yml](packages/reform-packages.yml) — Distribution surface (no SDK exists; one CDN embed loader)
- [conventions/reform-conventions.yml](conventions/reform-conventions.yml) — Cross-cutting integration semantics
- [authentication/reform-authentication.yml](authentication/reform-authentication.yml) — Credential model (no API credentials are issued)
- [data-model/reform-data-model.yml](data-model/reform-data-model.yml) — Form → Block → Submission → Answer entity graph
- [conformance/reform-conformance.yml](conformance/reform-conformance.yml) — Standards conformance, asserted and denied, with evidence
- [lifecycle/reform-lifecycle.yml](lifecycle/reform-lifecycle.yml) — Versioning, deprecation, changelog, status page (all absent) and decay signals
- [security/reform-trust-center.yml](security/reform-trust-center.yml) — SOC 2 / ISO 27001 / GDPR / DPF posture
- [security/reform-domain-security.yml](security/reform-domain-security.yml) — TLS/HSTS/DNSSEC/CAA/SPF/DMARC probe
- [well-known/reform-well-known.yml](well-known/reform-well-known.yml) — `/.well-known/` probe across all five live hosts (no documents found)
- [plans/reform-plans-pricing.yml](plans/reform-plans-pricing.yml) — API Commons Plans 0.1
- [rate-limits/reform-rate-limits.yml](rate-limits/reform-rate-limits.yml) — API Commons Rate Limits 0.1
- [finops/reform-finops.yml](finops/reform-finops.yml) — FinOps Framework 1.0 FOCUS-aligned cost guidance

### Note on Reform's API surface

Reform publishes **no REST API, SDK, OpenAPI definition or developer portal**. The host
`api.reform.app` — recorded as the API base in an earlier round of this profile — does not
resolve (NXDOMAIN as of 2026-08-14). Reform's real, documented integration surface is three
things: a signed outbound `form.submitted` webhook, a CDN-hosted browser embed loader with a
parent-page event API, and a "headless" mode that posts your own HTML form to
`forms.reform.app`. Those are what this profile now describes.

## Maintainer

Kin Lane — kin@apievangelist.com
