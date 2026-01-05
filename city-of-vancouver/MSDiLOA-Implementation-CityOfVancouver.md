# City of Vancouver - MSDiLOA Implementation Guide

## 1. City of Vancouver Implementation Overview

### 1.1 Introduction

The City of Vancouver is the founding governing authority for the Municipal Services Digital Letter of Authorization (MSDiLOA) credential and serves as the first issuing municipality. This implementation guide describes Vancouver-specific processes, systems, and procedures for issuing the MSDiLOA credential.

As the initial governing authority, Vancouver is responsible for establishing the credential schema and governance framework. In future iterations, governance may evolve into a province-wide municipal steering committee as other BC municipalities (such as Kelowna and Victoria) adopt the credential.

### 1.2 Governance and Administration Contacts

**Governing Authority Contact:**
- Name: René Cravioto
- Role: Sr. Manager – Innovation and Service Delivery / Identity & Verification
- Contact: rene.cravioto@vancouver.ca

**Administering Authority Contact:**
- Name: René Cravioto
- Role: Sr. Manager – Innovation and Service Delivery / Identity & Verification
- Contact: rene.cravioto@vancouver.ca

Within the City of Vancouver, this role is responsible for Verification & Identity product roadmap, backlog and day-to-day technical administration and support of the credentialing process, including implementation and technical oversight.

Within the Municipal Ecosystem of Verifiable Credentials, this role is responsible for achieving standardization of MSDiLOA schema across municipalities; evangelizing and communicating value to drive adoption.

## 2. Vancouver-Specific Systems and Processes

### 2.1 AMANDA - Business Licence System of Record

AMANDA is the City of Vancouver's Business Licence System of Record. It manages:
- Business licence applications, renewals, and amendments
- Licence issuance, revocations, and changes to attributes
- Business trade name and location tracking
- Authorization records and delegated authority relationships

### 2.2 VCIA - Verifiable Credential Issuing App

VCIA (Verifiable Credential Issuing App) is used by the City of Vancouver to issue municipal service credentials including:
- Business Licence credentials
- Digital Letters of Authorization credentials (MSDiLOA)

### 2.3 Data Collection and Verification Process

The MSDiLOA is issued after collecting and verifying personal details, location information, and property ownership for individuals applying for a business licence and the individual delegating authority for the applicant to act on their behalf.

**For the Applicant (Authorized Party):**
The City of Vancouver matches the identity details contained in the Person Credential and may extend the review to confirm the current principal residency by reviewing additional documents.

**For the Authorizer:**
The City of Vancouver matches the identity and property ownership details of the authorizer. During this process, personal details such as first and last name, as well as property ownership details are reviewed.

### 2.4 Data Updates and Revocation Triggers

When the MSDiLOA is issued, its data reflects the records at that time. The following events trigger changes to the credential:

**Authorizer Revokes MSDiLOA:**
This triggers a change to the related business licence record, as the requestor no longer has delegated authority, leading to the business licence itself being revoked.

**Authorized Party Changes Business Information:**
Where the requestor changes their business/trade name, ownership information, business location, or mailing address, they must do so by first presenting a valid MSDiLOA. Subsequent changes are updated in the business licence record, triggering a revocation process, with a prompt for re-issuance of the Municipal Property Rental Business Licence, including the updated, revised information.

**Business Licence Expiration:**
Where a Rental Property Business Licence is issued via the MSDiLOA and thereafter expires (Dec 31 of the license year), the delegated authority would only be revoked if the authority cancels the MSDiLOA, or the license is withdrawn or invalidated in AMANDA.

## 3. Implementation Roadmap

### 3.1 Phase 1: 2026 Q1

**Scope:** Schema V1.0 to accommodate Rental Property Business Licence use-cases

**Authorization Type:** Person-to-Person

**Use Case:** Authorizing a Person to apply for a Short-term rental (STR) business licence on behalf of another Person who is an owner of a given property.

**First Implementation:** Property owner will be able to use the MSDiLOA to authorize a tenant interested in applying for a short-term rental, facilitating a digitally trusted submission of a STR business licence application form.

### 3.2 Phase 2: 2026 Q2

**Scope:** Schema V2.0 expansion

**Authorization Type:** Business-to-Person

**Use Case:** Additionally accommodate authorizations issued by a Business to a Person to consume municipal services, starting with applying for a STR Business Licence.

### 3.3 Future Phases

**Person-to-Business Authorization:** Enable persons to authorize businesses to act on their behalf

**Business-to-Business Authorization:** Enable businesses to authorize other businesses

## 4. Vancouver Verification Procedures

The MSDiLOA is issued following a series of authentications during the licence request intake process to prove the relationship between the applicant and authorizer.

### 4.1 Applicant Identity Verification Method

| Manual Validation | Digital Validation |
|-------------------|-------------------|
| N/A | BC Government's Person Credential |

**Process:** The applicant must present a valid BC Person Credential in the BC Wallet. No manual identity verification is accepted.

### 4.2 Applicant's Principal Address Verification Method

| Manual Verification | Digital Verification |
|---------------------|---------------------|
| ICBC residential address history | BC Government's Person Credential |

**Process:** The City verifies the applicant's principal residence using either ICBC address records or attributes from the BC Person Credential. This is required for short-term rental licence applications.

### 4.3 Authorizer's Identity Verification Method

| Manual Verification | Digital Verification |
|---------------------|---------------------|
| N/A | BC Government's Person Credential |

**Process:** The authorizer (property owner) must present a valid BC Person Credential in the BC Wallet. No manual identity verification is accepted.

### 4.4 Authorizer's Property Ownership Verification Method

| Manual Verification | Digital Verification |
|---------------------|---------------------|
| LTSA Look-up | N/A (Future State: Property Owner Credential) |

**Current Process:** The City performs a manual look-up through the Land Title and Survey Authority (LTSA) system to verify property ownership.

**Future State:** When a Digital Property Owner Credential issued by Land Title and Survey Authority of BC exists, digital proof of home ownership will have to be digitally verified before issuing a letter of authorization with the authorizer_role = "Home Owner"

### 4.5 High Assurance Digital Identity

Note that obtaining a MSDiLOA requires both the applicant and authorizer to validate their identity using the BC Government issued Person Credential. This is considered a high assurance digital identity credential by the City of Vancouver, Government of British Columbia, and the Government of Canada.

## 5. Vancouver-Specific Requirements

### 5.1 General Requirements

- **BC Person Credential Mandatory:** Authorizers (i.e. the property owner) and Authorized parties must possess a valid BC Person Credential in the BC Wallet to be eligible to request or approve an MSDiLOA for the requesting Person.

- **Name Matching:** The party requesting municipal services must match both the Authorized Person's given and family name, as well as the service address location for which the applicant is requesting authorization to consume services.

- **Expiration and Revocation:** The authorization to consume each municipal service has a default expiration date. Such authorization can also be canceled/revoked at any time by the Authorizer.

- **Authority Verification:** The name of the person delegating authority to another party (i.e. service applicant) must correspond to the authority record (i.e. property owner noted on the property title).

### 5.2 Business Requirements

- Represent valid business licenses issued by the City of Vancouver
- Support both application and renewal processes
- Enable granting authorization to a person to consume municipal services on behalf of another person or on behalf of a local business within Vancouver's jurisdiction
- Enable multiple authorized representatives to receive credentials for the same business
- Allow other jurisdictions or systems to verify the license status digitally

### 5.3 Principles Specific to Vancouver Implementation

- The MSDiLOA credential will only be issued if the digital Person Credential is used by both the authorizer (to approve) and authorized (when requesting authorization) parties.
- Authorizers of the MSDiLOA retain the ability to cancel the MSDiLOA at any time before it expires.
- The party requesting municipal services must match both the Authorized Person's given and family name, as well as the service address location.

## 6. Vancouver Governance Framework References

### 6.1 Legislative and Policy Framework

**City of Vancouver Business License Bylaw**
The [City of Vancouver Business License Bylaw](https://vancouver.ca/your-government/licence-bylaw.aspx) governs all licensing rules, criteria, and conditions for compliance for the underlying business licencing framework.

**Freedom of Information and Protection of Privacy Act**
The [Freedom of Information and Protection of Privacy Act](https://www.bclaws.gov.bc.ca/civix/document/id/complete/statreg/96165_00) sets out the access and privacy rights of individuals as they relate to the public sector in British Columbia.

### 6.2 Risk Assessments

**Privacy Impact Assessment (PIA)**
In accordance with B.C. government procedures and policies, the standard [Privacy Impact Assessment (PIA)](https://www2.gov.bc.ca/gov/content/governments/services-for-government/information-management-technology/privacy/privacy-impact-assessments) has been or will be completed for the use of this credential technology.

**Security Threat and Risk Assessment (STRA)**
In accordance with B.C. government procedures and policies, the standard [Security Threat and Risk Assessment (STRA)](https://www2.gov.bc.ca/gov/content/governments/services-for-government/information-management-technology/information-security/security-threat-and-risk-assessment) has been or will be completed for the use of this credential technology.

### 6.3 Legal Agreements

N/A

## 7. Glossary of Vancouver-Specific Terms

**AMANDA** - City of Vancouver's Business Licence System of Record

**LTR BL** – Long-term rental Business Licence

**RPBL** – Rental Property Business Licence

**STR BL** – Short-term rental Business Licence

**VCIA** – Verifiable Credential Issuing App used by the City of Vancouver to issue municipal service credentials such as Business Licence credentials and Digital Letters of Authorization credentials.
