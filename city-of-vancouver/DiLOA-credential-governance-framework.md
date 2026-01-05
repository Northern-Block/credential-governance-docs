# Municipal Services Digital Letter of Authorization (MSDiLOA) Credential Documentation

## 1. About this Document

This document describes the **Municipal Services Digital Letter of Authorization (MSDiLOA)** verifiable credential to help potential verifiers determine whether it is suitable for their needs. The intended audience includes policy analysts, privacy specialists, solution architects, developers, and data architects.

The MSDiLOA credential can be issued by any British Columbia municipality. The first municipality to govern and issue this credential is the **City of Vancouver**. The MSDiLOA represents a digital authorization for a person to consume municipal services on behalf of another person or on behalf of a business.

> **Note:** While the MSDiLOA has applicability across various interactions within the municipal context, its first use-case covers the issuance of authorization to apply for a Rental Property Business Licence for Short-term Rentals (STR). A property owner will be able to use the MSDiLOA to authorize a tenant interested in applying for a short-term rental, facilitating a digitally trusted submission of a STR business licence application form.

The initiative is designed to enhance municipal service delivery, increase governance, protect homeowners and aims to establish a standard across municipalities in BC. This means that the MSDiLOA is designed to align with the digital verifiable credential ecosystem and can become a standard across BC municipalities, able to accommodate the distinct attributes needed by the ecosystem.

**Acknowledgements:** The development of this documentation follows the governance framework created by the Trust over IP Foundation (ToIP), specifically the Governance Metamodel Specification created by the Governance Stack Working Group (GSWG).

### 1.1 Version History

| Ver. | Date | Notes |
| --- | --- | --- |
| **0.9** | 05-Jan-2026 | Draft Release |

### 1.2 Terminology and Notation

Please reference Glossary - General Trust Over IP Terms.

Requirements include any combination of Machine-Testable Requirements and Human-Auditable Requirements. Unless otherwise stated, all Requirements MUST be expressed as defined in RFC 2119.

- **Mandates** are Requirements that use a MUST, MUST NOT, SHALL, SHALL NOT, or REQUIRED keyword.
- **Recommendations** are Requirements that use a SHOULD, SHOULD NOT, or RECOMMENDED keyword.
- **Options** are Requirements that use a MAY or OPTIONAL keyword.

**Machine-Testable Requirements** are those with which compliance can be verified using an automated test suite and appropriate scripting or testing software.

**Rules** are Machine-Testable Requirements that are written in a Machine-Readable language and can be processed by a Rules Engine. They are expressed in a structured rules language as specified by the Governance Framework.

**Human-Auditable Requirements** are those with which compliance can only be verified by an audit of people, processes, and procedures.

**Policies** are Human-Auditable Requirements written using standard conformance terminology. The Policies used in the Governance Framework use the standard terminology detailed in RFC 2119 keywords. Note that all RFC 2119 keywords have weight from an auditing perspective. An implementer MUST explain why a SHOULD or RECOMMENDED requirement was not implemented and SHOULD explain why a MAY requirement was implemented.

**Specifications** are documents containing any combination of Machine-Testable Requirements and Human-Auditable Requirements needed to produce technical interoperability.

### 1.3 Localization

The standard language for this governing framework (GF) is English.

## 2. Credential Overview

The Municipal Services Digital Letter of Authorization (MSDiLOA) credential is a verifiable credential (VC) issued to individuals (authorized parties) to prove that they have been granted authorization by another individual or business (authorizer) to consume specific municipal services on their behalf.

The credential is intended to be used in a wide range of municipal service contexts, both alone or alongside other credentials (e.g., BC Person Credential, Business Licence credentials), as a trusted source of authorization information for verifiers such as municipal service departments, licensing offices, or other government agencies.

|                         |                                                                                                     |
|-------------------------|-----------------------------------------------------------------------------------------------------|
| **Credential:**         | Municipal Services Digital Letter of Authorization (MSDiLOA)                                        |
| **Schema:**             | Municipal Services Digital Letter of Authorization                                                  |
| **Governing Authority:**| City of Vancouver (Founding Authority) <br/> Future: Municipal Consortium                          |
| **First Issuer:**       | City of Vancouver <br/> [https://vancouver.ca/](https://vancouver.ca/)                             |

### 2.1 Attribute Summary

The full set of attributes is described in [Section 4.3 Attributes](#43-attributes).

| **#** | **Name**                          | **Attribute**                          | **Data Type** |
|-------|-----------------------------------|----------------------------------------|---------------|
| 001   | Service Name                      | `service_name`                         | String        |
| 002   | Authorized Business               | `authorized_business`                  | String        |
| 003   | Proof of Homeownership            | `proof_of_homeownership`               | String        |
| 004   | Authorized Person Given Names     | `authorized_person_given_names`        | String        |
| 005   | Authorized Person Family Name     | `authorized_person_family_name`        | String        |
| 006   | Authorized Location Full Address  | `authorized_location_full_address`     | String        |
| 007   | Authorizer Role Type              | `authorizer_role_type`                 | String        |
| 008   | Authorizer Business               | `authorizer_business`                  | String        |
| 009   | Credential Proof ID               | `cred_proof_ID`                        | String        |
| 010   | Service Authorizations            | `service_authorizations`               | String        |
| 011   | Authorization Body                | `authorization_body`                   | String        |
| 012   | Credential Issued Date            | `credential_issued_date`               | Integer       |

### 2.2 Purpose and Objectives

**Purpose:**
To enable real-time digital service delivery while improving governance and reducing manual friction for verifying the legitimacy of Letters of Authorization. The roadmap envisions expanding from initial Person-to-Person authorization to Person-to-Business, Business-to-Business, and Business-to-Person authorizations. This will enable well-governed real-time digital service delivery and lower compliance costs, resulting in improved governance.

**Objectives:**
- Enable residents and businesses that would normally not be eligible to consume certain municipal services to present digital proof of "authorization by an eligible entity" to consume such services.
- Increase the level of assurance and trustworthiness of a Letter of Authorization by leveraging other digital verifiable credentials, such as the Person Credential.
- Expedite Digital Service Delivery without compromising governance.
- Facilitate schema and credential standardization across BC municipalities.

### 2.3 Scope

This governance framework applies to instances where an entity (a business or a person) wishes to authorize another party (a business or a person) to consume services on their behalf where the services offered by a municipality (credential Issuer) require that a specific party (such as a homeowner or business owner) be the applicant/consumer of such services.

The MSDiLOA credential can only be used to consume municipal services offered by the Issuing Authority. Initially, issuance is limited to the City of Vancouver, with plans to expand as other BC jurisdictions adopt the credential.

### 2.4 Principles

- The MSDiLOA credential will only be issued if a digital Person Credential is used by both the authorizer (to approve) and authorized party (when requesting authorization).
- Authorizers of the MSDiLOA retain the ability to cancel the MSDiLOA at any time before it expires.
- Data control remains with the credential holder (the authorized party), who chooses where and when to share their credential.
- Attributes of the authorizer other than the "authorizer_role" are not published to the MSDiLOA credential.
- Municipalities only issue MSDiLOA credentials related to the consumption of services offered under their mandate (e.g., business licenses, permits, etc.).
- Flexibility to add optional fields while maintaining standard core schema.
- Alignment with open standards to ensure interoperability regardless of technology stack.

When the necessary digital proof exists in the wallet ecosystem, proof of authority of the MSDiLOA-Authorizer will be established via digital credentials. Example: if a Digital Property Owner Credential issued by a Land Title authority exists, digital proof of home ownership will have to be digitally verified before issuing a letter of authorization with the authorizer_role = "Home Owner"

## 3. Credential Details

### 3.1 Issuer

The Municipal Services Digital Letter of Authorization (MSDiLOA) is governed and issued by municipalities within British Columbia.

**Governing Authority:**
The City of Vancouver currently serves as the governing authority for the MSDiLOA credential schema and framework. The governing authority is responsible for:
- Establishing and maintaining the credential schema
- Setting governance policies and principles
- Coordinating standardization across municipalities
- Evangelizing and communicating value to drive adoption

In future iterations, governance may evolve into a province-wide municipal steering committee as other municipalities adopt the credential.

**Issuing Municipalities:**
Municipalities that issue MSDiLOA credentials are responsible for:
- Administering their local authorization processes
- Reviewing authorization applications and approving issuances
- Operating their Business Licence Systems of Record
- Reviewing foundational identity, property ownership, and authorization documentation
- Revoking and re-issuing credentials as circumstances change

The City of Vancouver is the first issuing municipality. Implementation-specific details for each issuing municipality are maintained in separate implementation guides.

### 3.2 Schema and Credential Definition Governance

The MSDiLOA credential definition implements the schema governed by the City of Vancouver (as founding authority). Both the schema and credential definitions are registered on a verifiable data registry (ledger).

The governing authority may, after appropriate consultation and notification, update the credential definition and/or schema to reflect policy or operational changes. Updates will follow the broader municipal credential governance framework and are designed for eventual province-wide interoperability.

Individual issuing municipalities maintain their own credential definitions based on the governed schema.

### 3.3 Issuer Data Source

The MSDiLOA is issued after collecting and verifying personal details, location information, and authorization relationships between parties. Some information is generated directly by the Issuer, while other elements are verified against trusted sources.

General data sources include:
- **Authorization Request** – the information provided by the applicant (authorized party) during the authorization request process
- **Municipal Systems** – system-generated data and verification records
- **Foundational Identity Verification** – identity confirmation using trusted digital credentials (such as Person Credentials)
- **Property or Business Ownership Verification** – records checked through authoritative sources to confirm the authorizer's eligibility
- **Authorization Documentation** – collected authorization agreements and supporting evidence

The source of each attribute is described in [Section 4.3 Attributes](#43-attributes).

#### 3.3.1 Data Updates

When a credential is issued, its data reflects the authorization and related records at the time of issuance. Changes to authorization records (e.g., revocation by authorizer, changes to authorized services, or changes to the authorized party) trigger a revocation and may result in re-issuance of the credential to reflect current information.

### 3.4 Assurance

To minimize risk to verifiers, municipalities, and credential holders, the MSDiLOA credential is only issued following successful authentication and validation of:

- **Authorized Party Identity** – verified using a high-assurance digital identity credential (such as a Person Credential)
- **Authorizer Identity** – verified using a high-assurance digital identity credential
- **Authorizer's Authority** – verified against authoritative records (e.g., property ownership records, business registration records)
- **Authorization Agreement** – verified through documented authorization by the authorizer

These checks ensure the authenticity of the relationship between the authorized party, the authorizer, and the services being authorized.

Specific verification methods used by each issuing municipality are detailed in their respective implementation guides.

### 3.5 Revocation

A MSDiLOA credential will be revoked in the following cases:

1. **The authorizer revokes the authorization** – the party who granted authorization may cancel it at any time before expiration
2. **The authorization expires** – authorizations have default expiration dates specific to each service type
3. **The authorization record is updated** – changes to authorized services, parties, or other key details require credential revocation and re-issuance
4. **The underlying service licence or permission is withdrawn or invalidated** – if the service that was authorized becomes invalid, the authorization credential is also revoked

In some cases, a revocation triggers a **re-issuance** of the credential with updated details to reflect the new authorization record.

## 4. Credential Definition

### 4.1 Credential Schema

The Municipal Services Digital Letter of Authorization credential is based on the `Municipal Services Digital Letter of Authorization` schema, version 1.0, governed by the City of Vancouver and maintained on an appropriate verifiable data registry.

The Verifiable Credential format for this credential uses the AnonCreds specification.

### 4.2 Subject of the Credential

The subject of the credential is the authorization record, which establishes:

- The individual or business (authorized party/credential holder) who has been granted authorization, and
- The services, location, and authorizing party associated with the authorization.

The credential enables the holder to prove, in real time, that they are authorized to consume specific municipal services on behalf of another party at a specified location or for a specified purpose.

### 4.3 Attributes

The attributes of the Municipal Services Digital Letter of Authorization credential are organized by topic and described below.

#### 4.3.1 Attributes about the Authorization

*Service Name (001)*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>service_name</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>The type of municipal service or business licence being authorized through the MSDiLOA.</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>Municipal system of record (authorization application).</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>Short-Term Rental Business Licence</code><br/><code>Long-Term Rental Business Licence</code></td>
  </tr>
</table>

*Service Authorizations (010)*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>service_authorizations</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>A JSON object containing the specific services and actions that the authorized party is permitted to perform, including expiration details.</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>Municipal system of record (based on authorization agreement and service policies).</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String (JSON format)</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>["Apply for a STR BL", "The default STR Authorization expires 30 days after issuance date"]</code></td>
  </tr>
</table>

*Authorization Body (011)*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>authorization_body</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>Human readable natural language statement of the authorization (e.g., "I, [Authorizer Name], hereby authorize [Authorized Party Name]...").</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>Municipal system of record (generated from authorization record).</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>I, Jane Smith, hereby authorize John Doe to apply for a Short-Term Rental Business Licence for the property located at 123 Main Street.</code></td>
  </tr>
</table>

*Credential Issued Date (012)*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>credential_issued_date</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>The date on which the MSDiLOA credential was issued.</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>Municipal system of record (system-generated timestamp).</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>Integer (YYYYMMDD)</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>20260105</code></td>
  </tr>
</table>

#### 4.3.2 Attributes about the Authorized Party

*Authorized Person Given Names (004)*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>authorized_person_given_names</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>The given names of the person who has been granted authorization to consume municipal services.</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>Verified via digital Person Credential.</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>John</code><br/><code>Mary Anne</code></td>
  </tr>
</table>

*Authorized Person Family Name (005)*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>authorized_person_family_name</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>The family name of the person who has been granted authorization to consume municipal services.</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>Verified via digital Person Credential.</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>Doe</code><br/><code>Smith</code></td>
  </tr>
</table>

*Authorized Business (002)*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>authorized_business</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>If applicable, the name of the business on whose behalf the authorized person is requesting authorization. If not applicable, this value will be "N/A".</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>Municipal system of record (as reported by applicant, may be verified against business registration records).</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>Coastal Rentals Inc.</code><br/><code>N/A</code></td>
  </tr>
</table>

#### 4.3.3 Attributes about the Authorizer

*Authorizer Role Type (007)*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>authorizer_role_type</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>The role or capacity in which the authorizer is granting authorization (e.g., property owner, business owner).</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>Municipal system of record (verified against property or business ownership records).</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>Property Owner</code><br/><code>Business Owner</code></td>
  </tr>
</table>

*Authorizer Business (008)*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>authorizer_business</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>If applicable, the name of the business that is authorizing the consumption of services. The authorizing person may use a digital Business Licence credential to share this information. If not applicable, this value will be "N/A".</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>Verified via digital Business Licence credential or municipal business records.</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>Downtown Properties Ltd.</code><br/><code>N/A</code></td>
  </tr>
</table>

#### 4.3.4 Attributes about the Location

*Authorized Location Full Address (006)*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>authorized_location_full_address</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>The complete address of the location for which the applicant is requesting authorization to consume services.</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>Municipal system of record (verified against civic address records and property records).</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>Suite 301, 123 Main Street, Vancouver, BC, V6B 2Y5, Canada</code><br/><code>456 Oak Avenue, Victoria, BC, V8W 1N7, Canada</code></td>
  </tr>
</table>

#### 4.3.5 Attributes about Evidence

*Proof of Homeownership (003)*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>proof_of_homeownership</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>Indicates whether digital credentials were used as proof of home ownership. Value = "Manual" if no digital credentials were used. If a Property Owner Credential was used, value = "Digital".</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>Municipal system of record (based on verification method used).</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>Manual</code><br/><code>Digital</code></td>
  </tr>
</table>

*Credential Proof ID (009)*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>cred_proof_ID</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>A unique identifier that correlates to the underlying proof data and authorization documentation, stored in the system of record.</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>Municipal system of record (system-generated).</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>AUTH-2026-00123-PROOF</code><br/><code>LOA-456789-VER</code></td>
  </tr>
</table>

## 5. Implementations

### 5.1 Technical Format

This credential uses the [Hyperledger AnonCreds](https://github.com/hyperledger/anoncreds/) specification.

### 5.2 Issuer List

The Governing Authority of this Credential document attests that the following issuer information is accurate and can be relied upon by verifiers.

| Environment | Issuer Name | Issuer DID |
|------|------|-------|
| BCovrin Test  | City of Vancouver (TEST)  | TBD   |
| BCovrin Dev  | City of Vancouver (DEV)   | TBD   |

> **Note:** Additional municipalities will be added to this list as they adopt the MSDiLOA credential.

### 5.3 Schema Implementation

|Environment|Ledger|Schema ID|
|---|---|---|
|BCovrin Test|Municipal Services Digital Letter of Authorization| TBD |
|BCovrin Dev|Municipal Services Digital Letter of Authorization| TBD |

### 5.4 Credential Implementation

|Environment|Ledger|Credential Definition ID|OCA Bundle|
|---|---|---|---|
|BCovrin Test|Municipal Services Digital Letter of Authorization|TBD|TBD|
|BCovrin Dev|Municipal Services Digital Letter of Authorization|TBD|TBD|

## Appendix A: Glossary

**Authorized Party** – Either an 'Authorized Person' or an 'Authorized Business'; the party who has been granted authorization to consume municipal services on behalf of another party.

**Authorized Person** – The holder of an MSDiLOA issued through a given jurisdiction with the approval of the authorizer party.

**Authorizer Person** – Person approving the issuance of the Municipal Services Digital Letter of Authorization credential for specified services.

**MSDiLOA** – Municipal Services Digital Letter of Authorization credential.

**Person Credential** – A high-assurance digital identity credential (e.g., BC Person Credential) used to verify the identity of both the authorizer and authorized party.

## Appendix B: Risk Assessment

Issuing municipalities are responsible for completing appropriate risk assessments in accordance with their jurisdiction's procedures and policies. This may include Privacy Impact Assessments (PIA) and Security Threat and Risk Assessments (STRA) as required by local governance frameworks.
