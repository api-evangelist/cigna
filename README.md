# Cigna (cigna)

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
