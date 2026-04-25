# Cigna (cigna)

Cigna Healthcare is a leading global health services company offering medical, dental, behavioral, and pharmacy plans for individuals, families, and employers. The Cigna Developer Portal exposes CMS-mandated FHIR APIs for Patient Access, Provider Directory, Drug Formulary, and Provider Access, along with member and provider service APIs that enable third-party applications, electronic health record systems, and partners to access member health data with consent and look up Cigna network providers and formulary information.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/cigna/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Consumer
- **Access:** 3rd-Party

## Tags

- CMS Interoperability, Da Vinci, Drug Formulary, FHIR, Health Insurance, Healthcare, Patient Access, Provider Directory, SMART on FHIR

## Timestamps

- **Created:** 2025-02-21
- **Modified:** 2026-04-23

## APIs

### Cigna Patient Access API

FHIR R4 API that allows authorized third-party applications to access a Cigna member's claims, encounters, clinical data, coverage, and pharmacy information after the member completes SMART on FHIR authorization. Conforms to the CMS Interoperability and Patient Access final rule and the HL7 Da Vinci PDex implementation guide.

- **Human URL:** [https://developer.cigna.com/docs/service-apis/patient-access/implementation-guide](https://developer.cigna.com/docs/service-apis/patient-access/implementation-guide)
- **Base URL:** `https://fhir.cigna.com/PatientAccess/v1`
- **OpenAPI:** [openapi/cigna-patient-access-api-openapi.yml](openapi/cigna-patient-access-api-openapi.yml)

### Cigna Provider Directory API

Public FHIR-based Provider Directory API listing Cigna's contracted network providers, organizations, locations, healthcare services, and practitioner roles. Conforms to the HL7 Da Vinci PDex Plan Network IG and CMS Provider Directory API requirements.

- **Human URL:** [https://developer.cigna.com/docs/service-apis/provider-directory/implementation-guide](https://developer.cigna.com/docs/service-apis/provider-directory/implementation-guide)
- **Base URL:** `https://fhir.cigna.com/ProviderDirectory/v1`
- **OpenAPI:** [openapi/cigna-provider-directory-api-openapi.yml](openapi/cigna-provider-directory-api-openapi.yml)

### Cigna Drug Formulary API

Public FHIR-based Drug Formulary API exposing Cigna's covered drug lists, formulary tiers, prior authorization requirements, step therapy, and quantity limits. Implements the HL7 Da Vinci PDex US Drug Formulary IG required by the CMS Interoperability and Patient Access rule.

- **Human URL:** [https://developer.cigna.com/docs/service-apis](https://developer.cigna.com/docs/service-apis)
- **Base URL:** `https://fhir.cigna.com/DrugFormulary/v1`
- **OpenAPI:** [openapi/cigna-drug-formulary-api-openapi.yml](openapi/cigna-drug-formulary-api-openapi.yml)

### Cigna Provider Access API

FHIR API that allows in-network providers, with appropriate authorization, to retrieve a Cigna member's clinical and claims data to support care coordination. Implements the HL7 Da Vinci PDex Provider Access IG and conforms to the CMS Interoperability and Prior Authorization final rule.

- **Human URL:** [https://developer.cigna.com/docs/service-apis](https://developer.cigna.com/docs/service-apis)
- **Base URL:** `https://fhir.cigna.com/ProviderAccess/v1`
- **OpenAPI:** [openapi/cigna-provider-access-api-openapi.yml](openapi/cigna-provider-access-api-openapi.yml)

## Common Properties

- [Website](https://www.cigna.com/)
- [Developer Portal](https://developer.cigna.com/)
- [Documentation](https://developer.cigna.com/docs/service-apis)
- [Support](https://developer.cigna.com/support)
- [Terms of Service](https://www.cigna.com/legal/terms-of-use)
- [Privacy Policy](https://www.cigna.com/legal/privacy)
- [JSON-LD Context](json-ld/cigna-context.jsonld)
- [Patient JSON Schema](json-schema/cigna-patient-schema.json)
- [Spectral Rules](spectral/cigna-spectral.yml)
- [Naftiko Capabilities](naftiko/cigna-capabilities.yml)

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
