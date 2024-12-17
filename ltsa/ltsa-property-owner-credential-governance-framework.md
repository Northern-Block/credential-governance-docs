
# Property Owner Credential Governance Framework (Primary Document)

## 1. Primary Document

### 1.1. Introduction

This document establishes the Governance Framework for the LTSA credential, a digital credential designed to represent an individual’s ownership interest in land as registered in BC’s land title register. 

All land titles in British Columbia are managed by the [Land Title and Survey Authority of BC (LTSA)]((https://ltsa.ca/)), a publicly accountable statutory corporation responsible for operating the land title and survey systems of BC. This credential is designed to be issued by LTSA. The structure of the credential is designed to encapsulate essential information contained on a land title, such as owner names, title number and Parcel Identifier (PID).

The following legislation and regulations govern the management and registration of land title interests:
-	[Land Title Act](https://www.bclaws.gov.bc.ca/civix/document/id/complete/statreg/96250_00)
-	[Land Title Act (Board of Directors) Regulation](https://www.bclaws.gov.bc.ca/civix/document/id/complete/statreg/332_2010)
-	[Land Title Act Regulation](https://www.bclaws.gov.bc.ca/civix/document/id/complete/statreg/334_79)


**This document has been drafted for use by LTSA and others to support a proof of concept of the LTSA credential and should not be referred to for guidance on the production use of this credential.**

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

The standard language for this governance framework is English.

### 1.4. Governing Authority

LTSA is the governing authority for this Governance Framework. 

The contact information is TBD:
-	Name: 
-	Title: 
-	Organization: 
-	Email: 

### 1.5. Administering Authority

The Administering Authority on behalf of LTSA during the proof-of-concept phase of development is [LandSure Systems Ltd.](https://www.landsure.ca/).

The contact information is TBD:
-	Name: 
-	Title: 
-	Organization: 
-	Email:

### 1.6. Purpose

The purpose of this Governance Framework is to define what the LTSA credential is and who is responsible for the authority and administration of its use.

### 1.7. Scope

An LTSA credential issued according to this Governance Framework provides proof of an individual’s ownership interest in land as registered in BC’s land title register. Interest is held through fee simple ownership. 

**Exclusions:** Interests held by corporations are not eligible to hold an LTSA credential.

### 1.8. Objectives

1.	To allow the credential holder evidence that they are an owner on title in a verifiable credential format that is both secure and tamperproof
2.	To enable the credential holder to authenticate and access public sector services in BC in place of manual ways to prove ownership

### 1.9. Principles

LTSA’s purpose has one overarching mandate under the [Land Title and Survey Authority Act](https://www.bclaws.ca/civix/document/id/complete/statreg/00_04066_01) which is ‘to manage, operate and maintain the land title and survey systems of British Columbia’. These services are an essential underpinning to BC’s real property market and the civil justice system, and to BC’s civic governance, taxation and Crown land management frameworks. The use of a secure and verifiable credential modernizes the security features of how LTSA identifies individuals and their ownership and thereby strengthens the land title system to the benefit of all British Columbians.

### 1.10. General Requirements

For the purposes of the proof of concept, credential holders must proceed through the LTSA credential demo for issuance. Other general requirements TBD.

### 1.11. Revisions

Version 0.1 (DRAFT)

### 1.12. Extensions

No extensions are applicable to this Governance Framework at this time.

### 1.13. Schedule of Controlled Documents

N/A

## 2. Controlled Documents

### 2.1. Glossary

[ToIP Core Glossary](https://trustoverip.github.io/toip/glossary)

[Land Title and Survey Act definitions](https://www.bclaws.gov.bc.ca/civix/document/id/complete/statreg/04066_01#section1)

-	**Credential Holder:** Individual who owns a fee simple interest in land registered on a land title in BC.

### 2.2. Risk Assessment

(TBD) In accordance with B.C. government procedures and policies, the standard [Privacy Impact Assessment (PIA)](https://www2.gov.bc.ca/gov/content/governments/services-for-government/information-management-technology/privacy/privacy-impact-assessments) and [Security Threat and Risk Assessment (STRA)](https://www2.gov.bc.ca/gov/content/governments/services-for-government/information-management-technology/information-security/security-threat-and-risk-assessment) processes will be completed for the use of this credential technology.


### 2.3. Trust Assurance and Certification

TBD

### 2.4. Governance Requirements

Legislation and regulation governs the registration of land title interests in BC: [Land Title Act](https://www.bclaws.gov.bc.ca/civix/document/id/complete/statreg/96250_00).

### 2.5. Business Requirements

The primary requirement of the LTSA credential is to provide proof of ownership of a property owner to their interests in land in British Columbia.

### 2.6. Technical Requirements (Credential)

The Verifiable Credential format for this credential uses the [AnonCreds specification](https://hyperledger.github.io/anoncreds-spec/).

#### 2.6.1 Schema Definition

__Schema Name:__ ltsa_newcred_credential

__Schema Version:__ 0.1

**Name** | **Attributes** | **Format** | **Rules** | **Notes**
--- | --- | --- | --- | ---
Given Names on Title | givenName | String | Mandatory | N/A
Last Name on Title | LastNameOrCorpName1 | String | Mandatory | N/A
Parcel Identifier (PID) | parcelIdentifier | String | Mandatory | N/A
Street Address | streetAddress | String | Mandatory | N/A
City | city | String | Mandatory | N/A
Postal Code | postalCode | String | Mandatory | N/A
Title Number | titleNumber | String | Mandatory | N/A
Taxation Authority | authorityName | String | Mandatory | N/A

#### 2.6.2 Credential Implementation

Ledger | SCHEMA DEF | CRED DEF | Notes
--- | --- | --- | ---
CANdy Dev | TBA | --- | ---

#### 2.6.3 OCA Bundle
The OCA bundle for this credential is located in the [BC Gov Aries OCA Bundles repository](https://bcgov.github.io/aries-oca-bundles/OCABundles/schema/bcgov-digital-trust/LTSA/NewCredCredential/demo/).

### 2.7. Information Trust Requirements

The [Freedom of Information and Protection of Privacy Act](https://www.bclaws.gov.bc.ca/civix/document/id/complete/statreg/96165_00) sets out the access and privacy rights of individuals as they relate to the public sector in British Columbia.

### 2.8. Inclusion, Equitability, and Accessibility Requirements

TBD

### 2.9. Legal Agreements

TBD
