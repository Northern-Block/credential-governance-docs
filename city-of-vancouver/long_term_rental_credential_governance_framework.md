
# Long-term Business Rental Credential Governance Framework (Primary Document)

## 1. Primary Document

### 1.1. Introduction

This document articulates the Governance Framework (GF) for the [City of Vancouver](https://vancouver.ca/)’s **Long-Term Rental Business License Digital Credential**, part of Vancouver's broader commitment to transparent and efficient regulation of long-term rental properties.

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

*Placeholder for City of Vancouver’s designated governing authority.*

**Questions**:
- Who will be the governing authority responsible for overseeing the digital credential?
- What is the contact information for the governing body within the City of Vancouver?

### 1.5. Administering Authority

[Northern Block (NB)](https://northernblock.io/) is the Administering Authority on behalf of the City of Vancouver during the pilot phase.

### 1.6. Purpose

*Placeholder for specific purpose related to the long-term rental credential.*

**Questions**:
- What primary goal does the City of Vancouver aim to achieve with the long-term rental business license credential?
- What are the anticipated benefits for rental operators, the city, and residents?

### 1.7. Scope

*Placeholder for the scope specific to the long-term rental business license credential.*

**Questions**:
- Will the credential apply to all long-term rental operators within Vancouver?
- Are there specific exemptions or limitations that need to be included?

### 1.8. Objectives

*Placeholder for Vancouver-specific objectives related to credential use.*

**Questions**:
- What are the long-term and long-term objectives of issuing this credential?
- Are there specific compliance or regulatory goals associated with the credential?

### 1.9. Principles

*Placeholder for principles guiding Vancouver's approach to long-term rental credentialing.*

**Questions**:
- What guiding principles does the city want to reflect (e.g., transparency, data security, compliance)?
- Are there principles unique to Vancouver’s local context to incorporate?

### 1.10. General Requirements

*Placeholder for baseline requirements for obtaining and maintaining the credential.*

**Questions**:
- What criteria must be met by operators to receive and retain the credential?
- Are there specific requirements for credential renewal or revocation?

### 1.11. Revisions

Version 1.0

### 1.12. Extensions

There are no extensions to this Governance Framework at this time.

### 1.13. Schedule of Controlled Documents

*Placeholder for a list of controlled documents related to this framework.*

**Questions**:
- Are there any supplementary documents required to support this framework (e.g., code of conduct, user guide)?

## 2. Controlled Documents

### 2.1. Glossary

*Placeholder for terms relevant to Vancouver’s credential use case.*

**Questions**:
- Are there specific terms unique to the long-term rental industry in Vancouver that should be defined here?

### 2.2. Risk Assessment

*Placeholder for risk considerations.*

**Questions**:
- What risks does Vancouver foresee in issuing these digital credentials (e.g., data privacy, potential misuse)?
- Are there specific risk mitigation strategies Vancouver would like to prioritize?

### 2.3. Trust Assurance and Certification

*Placeholder for trust assurance and certification details.*

**Questions**:
- Will there be certification or accreditation standards that operators must comply with?
- How does Vancouver plan to ensure trust in the credentialing process?

### 2.4. Governance Requirements

The Long-Term Rental Business License Digital Credential is governed by this framework.

**Questions**:
- Are there additional governance requirements or standards Vancouver wants to enforce?

### 2.5. Business Requirements

*Placeholder for business-related requirements and use cases.*

**Questions**:
- What specific business or operational needs will this credential address?
- Are there any ancillary use cases for this credential beyond licensing?

### 2.6. Technical Requirements (Credential)

The verifiable credential format for this project will be based on Vancouver’s specifications.

#### 2.6.1 Schema Definition

__Schema Name:__ long_term_rental_license

__Schema Version:__ 1.0

**Attributes** | **Format** | **Rules** | **Notes**
--- | --- | --- | ---
license_id | String | Not NULL | Unique license ID
property_address | String | Not NULL | Address of the long-term rental property
license_validity_start | Date | Not NULL | Start date of license
license_validity_end | Date | Not NULL | Expiry date of license
operator_name | String | Not NULL | Name of the rental operator
operator_id | String | Not NULL | Operator's unique ID

**Questions**:
- Are there additional attributes or details Vancouver wants to include in the schema?

#### 2.6.2 Credential Implementation

Ledger | SCHEMA DEF | CRED DEF | Notes
--- | --- | --- | ---
BCovrin Test | TBD | --- | ---

### 2.7. Information Trust Requirements

*Placeholder for any information trust requirements.*

**Questions**:
- Does Vancouver have specific privacy policies or data storage requirements?
- Are there additional transparency or audit requirements for credential data?

### 2.8. Legal Agreements

*Placeholder for legal terms.*

**Questions**:
- Will Vancouver require users to agree to any specific terms of service or legal agreements?
- Are there specific liability terms that should be covered?

---

# Backlog/Comments (Additional Information to Add)

- How the revocation process will work
- Managing multiple rentals per operator, if applicable
- Updated schema if multiple properties are registered by a single operator
