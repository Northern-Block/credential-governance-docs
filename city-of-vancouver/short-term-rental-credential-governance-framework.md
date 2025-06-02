
# City of Vancouver Business License Credential (Short-Term Rental Focus)

## 1. Primary Document

### 1.1. Introduction

This framework supports the issuance of a digital credential representing a valid business license issued by the City of Vancouver, starting with short-term rental licenses. While this implementation targets short-term rentals, it is the first phase in a broader journey to digitize all business license types (e.g., long-term rentals, out-of-town businesses). The initiative is designed to enhance municipal service delivery and promote standards for municipal interoperability across BC.

**_Acknowledgements:_** The development of this documentation follows the governance framework created by the [Trust over IP Foundation (ToIP)](https://trustoverip.org/), specifically the [Governance Metamodel Specification](https://trustoverip.org/wp-content/uploads/ToIP-Governance-Metamodel-Specification-V1.0-2022-12-21.pdf) created by the [Governance Stack Working Group (GSWG)](https://wiki.trustoverip.org/display/HOME/Governance+Stack+Working+Group).

### 1.2. Terminology and Notation

Please reference [Glossary - General Trust Over IP Terms](https://trustoverip.github.io/toip/glossary).

Requirements include any combination of Machine-Testable Requirements and Human-Auditable Requirements. Unless otherwise stated, all Requirements MUST be expressed as defined in [RFC 2119](https://www.rfc-editor.org/rfc/rfc2119).

- Mandates are Requirements that use a MUST, MUST NOT, SHALL, SHALL NOT, or REQUIRED keyword.
- Recommendations are Requirements that use a SHOULD, SHOULD NOT, or RECOMMENDED keyword.
- Options are Requirements that use a MAY or OPTIONAL keyword.

**Machine-Testable Requirements** are those with which compliance can be verified using an automated test suite and appropriate scripting or testing software.

**Rules** are Machine-Testable Requirements that are written in a Machine-Readable language and can be processed by a Rules Engine. They are expressed in a structured rules language as specified by the Governance Framework.

**Human-Auditable Requirements** are those with which compliance can only be verified by an audit of people, processes, and procedures.

**Policies** are Human-Auditable Requirements written using standard conformance terminology. The Policies used in the Governance Framework will use the standard terminology detailed in RFC 2119 keywords. Note that all RFC 2119 keywords have weight from an auditing perspective. An implementer MUST explain why a SHOULD or RECOMMENDED requirement was not implemented and SHOULD explain why a MAY requirement was implemented.

**Specifications** are documents containing any combination of Machine-Testable Requirements and Human-Auditable Requirements needed to produce technical interoperability.

### 1.3. Localization

The standard language for this governing framework (GF) is English.

### 1.4. Governing Authority

City of Vancouver Contact: 
- Name: Sarah Hicks
- Role: Chief License Officer, Business Licenses Division
- Contact: sarah.hicks@vancouver.ca

In future iterations, governance may evolve into a province-wide municipal steering committee, but for the proof-of-concept phase, the City of Vancouver holds governing responsibility.

### 1.5. Administering Authority

City of Vancouver Contact:
- Name: René Cravioto
- Role: Digital Services
- Contact: rene.cravioto@vancouver.ca

Responsible for day-to-day technical administration and support of the credentialing process, including implementation and technical oversight.

### 1.6. Purpose

To enable real-time digital service delivery while improving governance and reducing manual friction for verifying business license status. This allows for faster turnarounds, lower compliance costs, and the reuse of due diligence already performed by the City during the licensing process.

### 1.7. Scope

This governance framework applies to short-term rental business licenses issued within the City of Vancouver. Credential issuance will occur at application or renewal stages. While currently scoped to Vancouver, the design is meant to support eventual province-wide adoption through schema standardization.

### 1.8. Objectives

- Enable residents and businesses to access services in real time by providing verifiable credentials in the BC Wallet.

- Improve governance for municipal and private sector stakeholders (e.g., Airbnb) without adding manual processes.

- Facilitate schema and credential standardization across BC municipalities.

- Enable reuse of due diligence efforts across jurisdictions and levels of government.

### 1.9. Principles

- Data control remains with the credential holder, who chooses where and when to share their credential.

- Municipalities only issue credentials related to their governance mandate (e.g., business licenses, not personal identity).

- Flexibility to add optional fields while maintaining standard core schema.

- Alignment with open standards to ensure interoperability regardless of technology stack.

- Support for designated representatives (e.g., admins) to receive credentials for a business.

### 1.10. General Requirements

- Applicants must possess a BC Person Credential to be eligible.

- Optional: use of digital business card (DBC) as additional foundational credential in the future.

- Only valid license holders or designated business representatives may receive credentials.

- Credentials include expiry (Dec 31 of the license year) and are only revoked if the license is withdrawn or invalidated.

### 1.11. Revisions

Version 1.0

### 1.12. Extensions

There are no extensions to this Governance Framework at this time.

### 1.13. Schedule of Controlled Documents

N/A

## 2. Controlled Documents

### 2.1. Glossary

N/A

### 2.2. Risk Assessment

In accordance with B.C. government procedures and policies, the standard [Privacy Impact Assessment (PIA)](https://www2.gov.bc.ca/gov/content/governments/services-for-government/information-management-technology/privacy/privacy-impact-assessments) and [Security Threat and Risk Assessment (STRA)](https://www2.gov.bc.ca/gov/content/governments/services-for-government/information-management-technology/information-security/security-threat-and-risk-assessment) processes will be completed for the use of this credential technology.

### 2.3. Trust Assurance and Certification

N/A

### 2.4. Governance Requirements

The [City of Vancouver Business License Bylaw](https://vancouver.ca/your-government/licence-bylaw.aspx) governs all licensing rules, criteria, and conditions for compliance.

### 2.5. Business Requirements

- Represent valid business licenses issued by the City.

- Support both applicant and renewal processes.

- Enable multiple authorized representatives to receive credentials for the same business.

- Allow other jurisdictions or systems to verify the license status digitally.

### 2.6. Technical Requirements (Credential)

The Verifiable Credential format for this credential uses the [AnonCreds specification](https://hyperledger.github.io/anoncreds-spec/).

#### 2.6.1 Schema Definition

__Schema Name:__ bc_municipality_business_license

__Schema Version:__ 1.0

**Attributes** | **Format** | **Rules** | **Notes**
--- | --- | --- | ---
license_id | String | Not NULL | Unique license ID
property_address | String | Not NULL | Address of the long-term rental property
license_validity_start | Date | Not NULL | Start date of license
license_validity_end | Date | Not NULL | Expiry date of license
operator_name | String | Not NULL | Name of the rental operator
operator_id | String | Not NULL | Operator's unique ID

**Note**:
- Credential schema to be updated

#### 2.6.2 Credential Implementation

Ledger | SCHEMA DEF | CRED DEF | Notes
--- | --- | --- | ---
BCovrin Test | TBD | --- | ---

#### 2.6.3 OCA Bundle

TBA

### 2.7. Information Trust Requirements

The [Freedom of Information and Protection of Privacy Act](https://www.bclaws.gov.bc.ca/civix/document/id/complete/statreg/96165_00) sets out the access and privacy rights of individuals as they relate to the public sector in British Columbia.

### 2.8. Legal Agreements

N/A
