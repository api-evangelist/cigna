# Cigna GraphQL Schema

## Overview

This document describes a conceptual GraphQL schema for Cigna Healthcare, one of the largest global health services companies. Cigna's Developer Portal exposes CMS-mandated FHIR APIs for Patient Access, Provider Directory, Drug Formulary, and Provider Access. This GraphQL schema unifies those capabilities into a single queryable graph covering member management, insurance plans, claims, provider directories, pharmacy benefits, authorizations, and supporting clinical and administrative data.

## Provider

- **Name**: Cigna
- **Developer Portal**: https://developer.cigna.com/
- **Documentation**: https://developer.cigna.com/docs/service-apis
- **Base APIs**: Patient Access API, Provider Directory API, Drug Formulary API, Provider Access API
- **Standards**: FHIR R4, SMART on FHIR, HL7 Da Vinci PDex, CMS Interoperability

## Schema Source

This schema is conceptual and synthesized from:
- Cigna Developer Portal documentation at https://developer.cigna.com/
- CMS Interoperability and Patient Access final rule requirements
- HL7 Da Vinci PDex implementation guides
- Cigna's FHIR R4 API surface covering Patient Access, Provider Directory, Drug Formulary, and Provider Access

## Types

### Member and Identity

| Type | Description |
|------|-------------|
| `Member` | A Cigna health plan member with demographic and enrollment data |
| `MemberProfile` | Detailed profile including contact, demographics, and plan associations |
| `MemberID` | Member identification including member number, group number, and subscriber ID |

### Insurance Plans and Benefits

| Type | Description |
|------|-------------|
| `InsurancePlan` | A Cigna health insurance product including HMO, PPO, EPO, HDHP variants |
| `PlanDetails` | Detailed attributes of a plan including network type, effective dates, and market segment |
| `PlanBenefits` | Benefits covered under a plan including medical, dental, vision, pharmacy |
| `Deductible` | Individual and family deductible amounts, accumulations, and periods |
| `OutOfPocketMax` | Out-of-pocket maximum limits, accumulations, and reset periods |
| `Copay` | Fixed cost-sharing amounts for specific service categories |
| `Coinsurance` | Percentage-based cost sharing applied after deductible is met |

### Network and Provider Access

| Type | Description |
|------|-------------|
| `NetworkType` | Classification of provider network (HMO, PPO, Open Access, LocalPlus) |
| `NetworkProvider` | A provider that participates in a specific Cigna network |
| `PreferredProvider` | A provider designated as preferred within a tiered network |
| `InNetwork` | Metadata and cost-sharing for in-network provider access |
| `OutOfNetwork` | Metadata and cost-sharing for out-of-network provider access |

### Prior Authorization

| Type | Description |
|------|-------------|
| `PriorAuthorization` | An authorization requirement for a service or procedure |
| `AuthorizationRequest` | A submitted request for prior authorization with clinical details |
| `AuthorizationStatus` | Current status and disposition of an authorization request |
| `ClinicalReview` | Clinical review details associated with an authorization decision |
| `MedicalNecessity` | Medical necessity determination criteria and outcome |

### Claims and Payments

| Type | Description |
|------|-------------|
| `Claim` | A medical claim submitted to Cigna for services rendered |
| `ClaimLine` | An individual line item on a claim representing a single service |
| `ClaimStatus` | Current processing status of a claim (received, processing, adjudicated, paid) |
| `ClaimPayment` | Payment details including amount paid, payment date, and check/EFT information |
| `EOB` | Explanation of Benefits summary record |
| `ExplanationOfBenefits` | Detailed EOB including member liability, plan payment, and adjustments |

### Provider Directory

| Type | Description |
|------|-------------|
| `Provider` | A licensed healthcare provider or practitioner in the Cigna directory |
| `ProviderDirectory` | Searchable directory of Cigna network providers and facilities |
| `PCP` | Primary Care Physician with panel status and accepting-patients indicator |
| `Specialist` | Specialist provider with specialty taxonomy and referral requirements |
| `PhysicyGroup` | A medical practice or physician group with affiliated providers |
| `Hospital` | An acute care hospital or health system facility |
| `UrgentCare` | An urgent care center with hours and accepted plans |
| `EmergencyRoom` | An emergency department with 24-hour availability data |
| `Telehealth` | A virtual care provider or telehealth platform available under the plan |
| `VirtualCare` | Virtual care services including synchronous video and asynchronous messaging |

### Pharmacy and Drug Benefits

| Type | Description |
|------|-------------|
| `Pharmacy` | A retail, mail-order, or specialty pharmacy in the Cigna network |
| `PharmacyBenefits` | Summary of a member's pharmacy benefit including formulary and cost sharing |
| `FormularyDrug` | A drug listed on the Cigna formulary with tier and coverage details |
| `Tier` | Formulary tier classification affecting cost sharing (generic, preferred brand, etc.) |
| `DrugCoverage` | Coverage details for a specific drug including quantity limits and restrictions |
| `RxClaim` | A pharmacy claim for a dispensed prescription |
| `PrescriptionHistory` | A member's prescription fill history within the benefit period |

### Referrals and Clinical Coding

| Type | Description |
|------|-------------|
| `Referral` | A referral from a PCP to a specialist or facility |
| `Diagnosis` | A diagnosis associated with a claim, authorization, or encounter |
| `ICD10Code` | International Classification of Diseases 10th Revision diagnosis code |
| `ProcedureCode` | A procedure identifier used for claims and authorizations |
| `CPTCode` | Current Procedural Terminology code for professional services |

### Wellness and Behavioral Health

| Type | Description |
|------|-------------|
| `Preventive` | Preventive care services covered at no cost-sharing under ACA |
| `Wellness` | Wellness program offerings including incentives, screenings, and coaching |
| `EAP` | Employee Assistance Program with counseling and work-life services |
| `BehavioralHealth` | Behavioral health benefits covering mental health and substance use disorder |
| `MentalHealth` | Mental health benefit details including session limits and network options |

### Ancillary Benefits

| Type | Description |
|------|-------------|
| `Dental` | Dental plan benefits including preventive, basic, and major services |
| `Vision` | Vision plan benefits including exams, frames, and contacts allowances |

### API Infrastructure

| Type | Description |
|------|-------------|
| `APIKey` | An API credential used to authenticate application requests |
| `Token` | An OAuth 2.0 / SMART on FHIR access token for member-authorized requests |
| `Webhook` | A webhook endpoint registered to receive Cigna event notifications |

## Queries

```graphql
type Query {
  member(id: ID!): Member
  memberProfile(memberId: ID!): MemberProfile
  insurancePlan(planId: ID!): InsurancePlan
  planBenefits(planId: ID!): PlanBenefits
  providers(
    name: String
    specialty: String
    networkType: String
    location: String
    radius: Int
    acceptingNewPatients: Boolean
    limit: Int
    offset: Int
  ): [NetworkProvider!]!
  provider(id: ID!): Provider
  providerDirectory(planId: ID!): ProviderDirectory
  claim(claimId: ID!): Claim
  claims(memberId: ID!, dateFrom: String, dateTo: String): [Claim!]!
  explanationOfBenefits(memberId: ID!, eobId: ID): ExplanationOfBenefits
  priorAuthorization(authId: ID!): PriorAuthorization
  authorizationStatus(authId: ID!): AuthorizationStatus
  formularyDrug(rxNorm: String, planId: ID!): FormularyDrug
  formularySearch(name: String!, planId: ID!): [FormularyDrug!]!
  pharmacy(id: ID!): Pharmacy
  pharmacies(zipCode: String!, radius: Int): [Pharmacy!]!
  prescriptionHistory(memberId: ID!): PrescriptionHistory
  referral(referralId: ID!): Referral
  wellness(memberId: ID!): Wellness
  behavioralHealth(planId: ID!): BehavioralHealth
}
```

## Mutations

```graphql
type Mutation {
  submitAuthorizationRequest(input: AuthorizationRequestInput!): AuthorizationRequest
  updateAuthorizationRequest(authId: ID!, input: AuthorizationUpdateInput!): AuthorizationRequest
  createReferral(input: ReferralInput!): Referral
  registerWebhook(input: WebhookInput!): Webhook
  updateWebhook(webhookId: ID!, input: WebhookInput!): Webhook
  deleteWebhook(webhookId: ID!): Boolean
}
```

## Subscriptions

```graphql
type Subscription {
  claimStatusUpdated(memberId: ID!): ClaimStatus
  authorizationStatusUpdated(authId: ID!): AuthorizationStatus
  eobAvailable(memberId: ID!): ExplanationOfBenefits
}
```

## Authentication

Cigna's APIs use OAuth 2.0 with SMART on FHIR extensions for member-authorized access. Application-level access for public APIs (Provider Directory, Drug Formulary) uses client credentials flow. Member-facing queries require an access token obtained through the SMART on FHIR authorization code flow with the member's Cigna credentials.

- **Client Credentials**: Provider Directory API, Drug Formulary API
- **SMART on FHIR Authorization Code**: Patient Access API, Provider Access API
- **Scopes**: `patient/*.read`, `launch`, `openid`, `fhirUser`

## Notes

This is a conceptual GraphQL schema. Cigna currently exposes FHIR R4 REST APIs rather than a native GraphQL endpoint. This schema represents how those APIs could be surfaced as a unified GraphQL graph for application developers.
