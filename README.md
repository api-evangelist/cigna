# Cigna (cigna)

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

Cigna Healthcare is a leading global health services company offering medical, dental, behavioral, and pharmacy plans for individuals, families, and employers. The Cigna Developer Portal exposes CMS-mandated FHIR APIs for Patient Access, Provider Directory, Drug Formulary, and Provider Access, along with member and provider service APIs that enable third-party applications, electronic health record systems, and partners to access member health data with consent and look up Cigna network providers and formulary information.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/cigna/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/cigna/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Consumer
- **Access:** 3rd-Party

## Tags

- CMS Interoperability
- Da Vinci
- Drug Formulary
- FHIR
- Health Insurance
- Healthcare
- Patient Access
- Provider Directory
- SMART on FHIR

## Timestamps

- **Created:** 2025-02-21
- **Modified:** 2026-05-19

## APIs

### Cigna Patient Access API

FHIR R4 API that allows authorized third-party applications to access a Cigna member's claims, encounters, clinical data, coverage, and pharmacy information after the member completes SMART on FHIR authorization. Conforms to the CMS Interoperability and Patient Access final rule and the HL7 Da Vinci PDex implementation guide.

- **Human URL:** [https://developer.cigna.com/docs/service-apis/patient-access/implementation-guide](https://developer.cigna.com/docs/service-apis/patient-access/implementation-guide)
- **Base URL:** `https://fhir.cigna.com/PatientAccess/v1`

#### Tags

- CMS Interoperability
- FHIR
- Patient Access
- SMART on FHIR

#### Properties

- [Documentation](https://developer.cigna.com/docs/service-apis/patient-access/implementation-guide)
- [OpenAPI](openapi/cigna-patient-access-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cigna-patient-access-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cigna-patient-access-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cigna Provider Directory API

Public FHIR-based Provider Directory API listing Cigna's contracted network providers, organizations, locations, healthcare services, and practitioner roles. Conforms to the HL7 Da Vinci PDex Plan Network implementation guide and the CMS Provider Directory API requirements.

- **Human URL:** [https://developer.cigna.com/docs/service-apis/provider-directory/implementation-guide](https://developer.cigna.com/docs/service-apis/provider-directory/implementation-guide)
- **Base URL:** `https://fhir.cigna.com/ProviderDirectory/v1`

#### Tags

- CMS Interoperability
- FHIR
- Provider Directory
- Public API

#### Properties

- [Documentation](https://developer.cigna.com/docs/service-apis/provider-directory/implementation-guide)
- [OpenAPI](openapi/cigna-provider-directory-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cigna-provider-directory-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cigna-provider-directory-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cigna Drug Formulary API

Public FHIR-based Drug Formulary API exposing Cigna's covered drug lists, formulary tiers, prior authorization requirements, step therapy, and quantity limits. Implements the HL7 Da Vinci PDex US Drug Formulary implementation guide required by the CMS Interoperability and Patient Access rule.

- **Human URL:** [https://developer.cigna.com/docs/service-apis](https://developer.cigna.com/docs/service-apis)
- **Base URL:** `https://fhir.cigna.com/DrugFormulary/v1`

#### Tags

- CMS Interoperability
- Drug Formulary
- FHIR
- Public API

#### Properties

- [Documentation](https://developer.cigna.com/docs/service-apis)
- [OpenAPI](openapi/cigna-drug-formulary-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cigna-drug-formulary-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cigna-drug-formulary-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cigna Provider Access API

FHIR API that allows in-network providers, with appropriate authorization, to retrieve a Cigna member's clinical and claims data to support care coordination. Implements the HL7 Da Vinci PDex Provider Access implementation guide and conforms to the CMS Interoperability and Prior Authorization final rule.

- **Human URL:** [https://developer.cigna.com/docs/service-apis](https://developer.cigna.com/docs/service-apis)
- **Base URL:** `https://fhir.cigna.com/ProviderAccess/v1`

#### Tags

- CMS Interoperability
- FHIR
- Provider Access

#### Properties

- [Documentation](https://developer.cigna.com/docs/service-apis)
- [OpenAPI](openapi/cigna-provider-access-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cigna-provider-access-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cigna-provider-access-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/Cigna)
- [LinkedIn](https://www.linkedin.com/company/the-cigna-group)
- [Website](https://www.cigna.com/)
- [Developer Portal](https://developer.cigna.com/)
- [Portal](https://developer.cigna.com/)
- [Documentation](https://developer.cigna.com/docs/service-apis)
- [Support](https://developer.cigna.com/support)
- [Terms of Service](https://www.cigna.com/legal/terms-of-use)
- [Privacy Policy](https://www.cigna.com/legal/privacy)
- [J S O N L D Context](json-ld/cigna-context.jsonld)
- [JSON Schema](json-schema/cigna-patient-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [Spectral Rules](spectral/cigna-spectral.yml) — [Spectral](https://docs.stoplight.io/docs/spectral)
- [L L Ms Txt](https://developer.cigna.com/llms.txt)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
