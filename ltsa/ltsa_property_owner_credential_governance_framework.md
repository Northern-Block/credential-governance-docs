
# Property Owner Credential Governance Framework (Primary Document)

## 1. Primary Document

### 1.1. Introduction

This document establishes the Governance Framework (GF) for the Land Title and Survey Authority of British Columbia (LTSA) Property Owner Digital Credential. This framework is part of LTSA’s initiative to streamline and secure property ownership verification processes, enabling trusted digital credentials within British Columbia’s property ecosystem.

### 1.2. Terminology and Notation

Please refer to the Glossary for definitions of general and specific terms relevant to the LTSA Property Owner Credential use case.

Requirements include Machine-Testable Requirements and Human-Auditable Requirements, all expressed per RFC 2119.

- **Mandates**: Indicated by MUST, MUST NOT, SHALL, or REQUIRED keywords.
- **Recommendations**: Indicated by SHOULD, SHOULD NOT, or RECOMMENDED keywords.
- **Options**: Indicated by MAY or OPTIONAL keywords.

### 1.3. Localization

The standard language for this governance framework is English.

### 1.4. Governing Authority

*Placeholder for LTSA as the Governing Authority.*

**Questions**:
- Who is the designated governing authority within LTSA for managing the credentialing framework?
- Are there specific contacts or teams responsible for oversight and compliance?

### 1.5. Administering Authority

Northern Block Inc. (NB) will serve as the Administering Authority on behalf of LTSA during the proof-of-concept phase.

### 1.6. Purpose

*Placeholder for the purpose of the Property Owner Credential.*

**Questions**:
- What primary objectives does LTSA have for the Property Owner Credential?
- How will this credential improve efficiency, trust, and security within property-related transactions?

### 1.7. Scope

*Placeholder for scope relevant to the Property Owner Credential.*

**Questions**:
- Which property owners or transactions are within the scope of this credential framework?
- Are there any exclusions or specific use cases that should be documented?

### 1.8. Objectives

*Placeholder for LTSA-specific objectives related to credential issuance and management.*

**Questions**:
- What short-term and long-term objectives does LTSA aim to accomplish with this credential?
- Are there compliance or regulatory goals tied to the Property Owner Credential?

### 1.9. Principles

*Placeholder for guiding principles for LTSA’s Property Owner Credential.*

**Questions**:
- Which principles (e.g., transparency, security, accessibility) does LTSA prioritize in this framework?
- Are there principles specifically relevant to property transactions in BC?

### 1.10. General Requirements

*Placeholder for general requirements for obtaining and holding the Property Owner Credential.*

**Questions**:
- What criteria must property owners meet to be eligible for the credential?
- Are there revocation or renewal requirements for maintaining this credential?

### 1.11. Revisions

Version 1.0

### 1.12. Extensions

No extensions are applicable to this Governance Framework at this time.

### 1.13. Schedule of Controlled Documents

*Placeholder for any additional controlled documents.*

**Questions**:
- Are there supporting documents (e.g., compliance guidelines or user agreements) relevant to this framework?

## 2. Controlled Documents

### 2.1. Glossary

*Placeholder for definitions specific to the LTSA Property Owner Credential.*

**Questions**:
- Are there terms specific to BC property law or digital credentials that should be defined?

### 2.2. Risk Assessment

*Placeholder for risk assessment related to the Property Owner Credential.*

**Questions**:
- What risks does LTSA anticipate in issuing and managing this credential (e.g., data privacy, legal liability)?
- Are there risk mitigation strategies LTSA would like to implement?

### 2.3. Trust Assurance and Certification

*Placeholder for trust assurance standards and certification criteria.*

**Questions**:
- Are there certification or trust standards that property owners or stakeholders must comply with?
- How will LTSA ensure ongoing trust and compliance with this credential?

### 2.4. Governance Requirements

This Governance Framework governs the issuance and management of LTSA’s Property Owner Credential.

**Questions**:
- Are there additional governance requirements LTSA wishes to enforce for credentialing?

### 2.5. Business Requirements

*Placeholder for business-related requirements and value propositions.*

**Questions**:
- What business or operational requirements does LTSA have for this credential?
- Are there additional use cases beyond property ownership verification for this credential?

### 2.6. Technical Requirements (Credential)

The verifiable credential format will adhere to BC Digital Trust specifications, customized for LTSA.

#### 2.6.1 Schema Definition

__Schema Name:__ property_owner_credential

__Schema Version:__ 1.0

**Attributes** | **Format** | **Rules** | **Notes**
--- | --- | --- | ---
owner_id | String | Not NULL | Unique ID for the property owner
property_address | String | Not NULL | Address of the owned property
ownership_start_date | Date | Not NULL | Start date of ownership
ownership_end_date | Date | Not NULL | End date of ownership (if applicable)
owner_name | String | Not NULL | Name of the property owner

**Questions**:
- Are there additional attributes that LTSA wants to include in the credential schema?

#### 2.6.2 Credential Implementation

Ledger | SCHEMA DEF | CRED DEF | Notes
--- | --- | --- | ---
BCovrin Test | TBD | --- | ---

### 2.7. Information Trust Requirements

*Placeholder for LTSA’s information trust policies.*

**Questions**:
- Does LTSA have specific data privacy or storage policies for the credential data?
- Are there additional transparency or audit requirements?

### 2.8. Legal Agreements

*Placeholder for legal terms applicable to LTSA and credential holders.*

**Questions**:
- Are there specific legal agreements LTSA requires credential holders to acknowledge?
- What limitations of liability or terms of use should be included?

---

# Backlog/Comments (Additional Information to Add)

- Detailed revocation process for the Property Owner Credential
- Multi-property ownership scenarios
- Requirements for credential updates and schema modifications

