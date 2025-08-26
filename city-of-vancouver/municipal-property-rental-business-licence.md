# Municipal Property Rental Business Licence Credential Documentation

## 1. About this Document

This document describes the **Municipal Property Rental Business Licence** verifiable credential to help potential verifiers determine whether it is suitable for their needs. The intended audience includes policy analysts, privacy specialists, solution architects, developers, and data architects.

The credential is issued by the **City of Vancouver, Business Licenses Division**, and represents a valid municipal business licence for operating rental properties, initially covering short-term rental (STR) and long-term rental (LTR) business licence types.

### 1.1 Version History

| Ver.      | Date | Notes |
| ----------- | ----------- | ----------- |
| <b>1.0</b>      | 26-Aug-2025       | Initial release |

## 2 Credential Overview
The Municipal Property Rental Business Licence credential is a verifiable credential (VC) issued to individuals or authorized representatives of businesses to prove that they hold a valid City of Vancouver rental business licence.

The credential is intended to be used in a wide range of contexts, both alone or alongside other credentials (e.g., BC Person Credential, Digital Business Card), as a trusted source of business licence information for verifiers such as platforms (Airbnb, VRBO), municipal inspectors, or other government agencies.

|              |                                                                |
|-------------------------|---------------------------------------------------------------------------------|
| **Credential:**         | Municipal Property Rental Business Licence                                          |
| **Schema:**             | Municipal Property Rental Business Licence                                          |
| **Issuer:**             | City of Vancouver (Business Licenses Division) <br/> [https://vancouver.ca/](https://vancouver.ca/) |     



### 2.1 Attribute Summary

Attributes are fully described below in the [Attributes](#bookmark=id.d4k15yq1kvi3) section.

| **Name**                     | **Attribute**                      | **Data Type** |
|-------------------------------|------------------------------------|---------------|
| Business Licence Type         | `business_licence_type`            | String        |
| Business Sub-Type             | `business_sub_type`                | String        |
| Business / Trade Name         | `business_trade_name`              | String        |
| Licence Number                | `licence_number`                   | String        |
| Licence Revision Number       | `licence_revision_number`          | String        |
| Licence Holder First Name     | `licence_holder_given_name`        | String        |
| Licence Holder Last Name      | `licence_holder_family_name`       | String        |
| Licence Year                  | `validity_year`                    | String        |
| Issue Date                    | `licence_issued_dateint`           | Integer       |
| Expiry Date                   | `licence_expiry_dateint`           | Integer       |
| Unit Number                   | `unit`                             | String        |
| Unit Type                     | `unit_type`                        | String        |
| Street Number                 | `street_number`                    | String        |
| Street Name                   | `street_name`                      | String        |
| Municipality                  | `municipality`                     | String        |
| Municipality Type             | `municipality_status`              | String        |
| Regional District             | `regional_district`                | String        |
| Province / Territory          | `province_territory`               | String        |
| Postal Code                   | `postal_code`                      | String        |
| Country                       | `country`                          | String        |
| Full Licence Address          | `full_licence_address`             | String        |
| Property Residence Type       | `property_residence_type`          | String        |
| Neighbourhood / Local Area    | `local_area`                       | String        |
| Location Type                 | `location_type`                    | String        |
| Number of Dwelling Units      | `number_of_dwelling_units`         | String        |
| Parcel Identifier (PID)       | `PID`                              | String        |
| Strata Property (Yes/No)      | `strata_flag`                      | String        |
| Map Coordinates (Lat/Long)    | `GIS_coordinates`                  | String        |
| Identity Verification Method  | `identity_verification_method`     | String        |
| Primary Address Verification Method    | `primary_address_verification_method`     | String        |

## 3. Credential Details

### 3.1 Issuer

The Municipal Property Rental Business Licence credential is issued by the **City of Vancouver, Business Licenses Division**. The City is responsible for the creation, approval, renewal, and revocation of all municipal business licences within its jurisdiction.

The City of Vancouver is responsible for:

- Administering the <a href="https://vancouver.ca/your-government/licence-bylaw.aspx">Business Licence Bylaw</a>, including processing applications, renewals, and amendments to licences.
- Operating the **Business Licence System of Record (AMANDA)**, which records licence issuance, renewals, revocations, and changes to attributes such as business trade name or location.
- Reviewing foundational identity, property ownership, and authorization documentation as part of the licensing process.

### 3.2 Schema and Credential Definition Governance

The Municipal Property Rental Business Licence credential definition implements the schema published by the City of Vancouver. Both the schema and credential definition are registered on the CANdy Dev Ledger.

The City of Vancouver may, after appropriate consultation and notification, update the credential definition and/or schema to reflect policy or operational changes. Updates will follow the broader municipal credential governance framework and are designed for eventual province-wide interoperability

### 3.3 Issuer Data Source

The data in the Municipal Property Rental Business Licence credential comes from the City of Vancouver’s Business Licence system (AMANDA). The City generates some information directly and verifies others against trusted sources.

- **Business Licence Filing** – the information provided by or on behalf of the applicant during the licence application or renewal process.
- **City of Vancouver Business Licence System (AMANDA)** – system-generated data such as licence number, revision number, and timestamps.
- **Foundational Identity Verification** – the applicant’s identity is confirmed using the BC Person Credential or other government-issued photo identification.  
- **Property Ownership Verification** – records are checked through the <a href="https://ltsa.ca/">Land Title and Survey Authority (LTSA)</a> to confirm ownership or authorized use of the property.  
- **Authorization Verification** – an Owner’s Letter of Authorization, where applicable, is collected and retained.

The source of each attribute is described in the Attributes section.

#### 3.3.1 Data Updates

When a credential is issued, its data reflects the business licence record at the time of issuance. Changes to licence records (e.g., business trade name, ownership, address) trigger a revocation and re-issuance of the credential so that the holder’s credential always reflects current information.

### 3.4 Assurance

To minimize risk to verifiers, the City, and licence holders, the Municipal Property Rental Business Licence credential is only issued following successful authentication and validation of:

- **Applicant identity** – via the BC Person Credential (high-assurance, Level 3 trusted digital identity).
- **Primary address history** – verified using ICBC address records or the Person Credential.
- **Property ownership** – verified against LTSA property records.
- **Authorization** – verified by requiring an Owner’s Letter of Authorization if the applicant is not the property owner.

These checks ensure the authenticity of the relationship between the applicant, the business, and the property location.

### 3.5 Revocation

A Municipal Property Rental Business Licence credential will be revoked in the following cases:

1. The underlying business licence is withdrawn, invalidated, or expires.
2. The business licence record is updated (e.g., new address, ownership, or trade name).
3. The licence holder or designated representative is no longer authorized.

In most cases, a revocation triggers a **re-issuance** of the credential with updated details to reflect the new licence record

## 4. Credential Definition

### 4.1 Credential Schema

The Municipal Property Rental Business Licence credential is based on the municipal-property-rental-business-licence schema, version 1.0, published by the City of Vancouver and maintained in BCovrin.

### 4.2 Subject of the Credential

The subject of the credential is the licence record, which ties:

- The individual or authorized representative (credential holder), and
- The business/property information associated with the licence.

The credential enables the holder to prove, in real time, that they are licensed by the City of Vancouver to operate a rental business (short-term or long-term).

### 4.3 Attributes

The attributes of the Municipal Property Rental Business Licence credential are organized by topic and described below.

---

#### 4.3.1 Attributes about the Licence

*Business Licence Type*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>business_licence_type</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>The category of licence issued by the City of Vancouver (e.g., Short-Term Rental, Long-Term Rental).</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>City of Vancouver Business Licence System (AMANDA).</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>Short-Term Rental</code><br></br><code>Long-Term Rental</code></td>
  </tr>
</table>

*Business Sub-Type*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>business_sub_type</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>A sub-classification of the licence type, reflecting specific business activity.</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>AMANDA.</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>Bed & Breakfast</code><br></br><code>Apartment Rental</code></td>
  </tr>
</table>

*Licence Number*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>licence_number</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>A unique number assigned to each business licence by the City of Vancouver.</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>AMANDA.</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>24-123456</code></td>
  </tr>
</table>

*Licence Revision Number*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>licence_revision_number</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>Identifier representing the revision of the licence record (incremented when changes occur).</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>AMANDA.</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>1</code><br></br><code>2</code></td>
  </tr>
</table>

*Licence Year*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>validity_year</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>The year in which the licence is valid.</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>AMANDA.</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>2025</code></td>
  </tr>
</table>

*Issue Date*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>licence_issued_dateint</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>The date the business licence was issued.</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>AMANDA.</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>Integer (YYYYMMDD)</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>20250115</code></td>
  </tr>
</table>

*Expiry Date*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>licence_expiry_dateint</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>The date the business licence expires.</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>AMANDA.</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>Integer (YYYYMMDD)</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>20251231</code></td>
  </tr>
</table>

---

#### 4.3.2 Attributes about the Business / Licence Holder

*Business / Trade Name*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>business_trade_name</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>The trade name or operating name under which the business is licensed.</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>AMANDA (as reported by the applicant).</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>West End Suites</code><br></br><code>Maple Rentals</code></td>
  </tr>
</table>

*Licence Holder First Name*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>licence_holder_given_name</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>The given name(s) of the licence holder, verified against foundational identity.</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>Verified via BC Person Credential and government-issued photo ID.</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>Jane</code></td>
  </tr>
</table>

*Licence Holder Last Name*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>licence_holder_family_name</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>The family name (surname) of the licence holder, verified against foundational identity.</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>Verified via BC Person Credential and government-issued photo ID.</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>Doe</code></td>
  </tr>
</table>

---

#### 4.3.3 Attributes about the Location

*Unit*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>unit</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>The unit number of the licensed property, if applicable.</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>AMANDA; provided by the applicant and verified against property records.</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>101</code><br></br><code>3B</code></td>
  </tr>
</table>

*Unit Type*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>unit_type</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>Type of unit designation (e.g., Apartment, Suite, Basement).</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>AMANDA.</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>Suite</code><br></br><code>Basement</code></td>
  </tr>
</table>

*Street Number*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>street_number</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>The street number of the licensed property.</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>AMANDA; verified against civic address records.</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>1234</code></td>
  </tr>
</table>

*Street Name*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>street_name</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>The street name of the licensed property.</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>AMANDA; verified against civic address records.</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>Main Street</code><br></br><code>West 4th Avenue</code></td>
  </tr>
</table>

*Municipality*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>municipality</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>The municipality where the property is located (always Vancouver for this credential).</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>AMANDA.</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>Vancouver</code></td>
  </tr>
</table>

*Municipality Status*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>municipality_status</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>Status of the municipality (e.g., City, Township).</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>AMANDA.</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>City</code></td>
  </tr>
</table>

*Regional District*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>regional_district</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>The regional district for the property’s location.</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>AMANDA; derived from property records.</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>Metro Vancouver</code></td>
  </tr>
</table>

*Province or Territory*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>province_territory</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>The province or territory of the licensed property.</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>AMANDA.</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>British Columbia</code></td>
  </tr>
</table>

*Postal Code*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>postal_code</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>The postal code of the licensed property.</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>AMANDA; verified against Canada Post format.</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>V6B 2Y5</code></td>
  </tr>
</table>

*Country*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>country</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>The country of the licensed property.</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>AMANDA.</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>Canada</code></td>
  </tr>
</table>

*Full Licence Address*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>full_licence_address</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>The complete address of the property associated with the business licence, including unit (if applicable), street number, street name, municipality, province/territory, postal code, and country.</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>City of Vancouver Business Licence System (AMANDA); derived from applicant submissions and verified against property and identity records.</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>Unit 201, 123 Main Street, Vancouver, BC, V6B 2Y1, Canada</code></td>
  </tr>
</table>

*Local Area*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>local_area</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>The neighbourhood or local planning area where the property is located.</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>AMANDA; derived from City of Vancouver planning datasets.</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>Kitsilano</code><br></br><code>Downtown</code></td>
  </tr>
</table>

*GIS Coordinates*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>GIS_coordinates</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>Geographic coordinates of the licensed property (latitude and longitude).</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>City of Vancouver GIS dataset.</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String (lat,long)</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>49.2827,-123.1207</code></td>
  </tr>
</table>

---

#### 4.3.4 Attributes about the Property

*Property Residence Type*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>property_residence_type</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>Indicates the type of residence (e.g., single-family home, condo, apartment).</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>AMANDA; may be cross-verified with LTSA records.</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>Condominium</code><br></br><code>Single Family</code></td>
  </tr>
</table>

*Location Type*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>location_type</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>Specifies whether the rental is the principal residence or another type of dwelling.</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>Applicant declaration in AMANDA; validated against BC Person Credential address history.</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>Principal Residence</code><br></br><code>Secondary Suite</code></td>
  </tr>
</table>

*Number of Dwelling Units*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>number_of_dwelling_units</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>The number of dwelling units at the licensed property address.</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>AMANDA; verified against property assessment and LTSA records.</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>Integer</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>1</code><br></br><code>12</code></td>
  </tr>
</table>

*Parcel Identifier (PID)*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>PID</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>The Land Title and Survey Authority’s Parcel Identifier for the property.</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>LTSA property records; integrated with AMANDA.</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String (9-digit numeric)</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>012-345-678</code></td>
  </tr>
</table>

*Strata Flag*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>strata_flag</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>Indicates whether the property is part of a strata (condominium) development.</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>LTSA property records; confirmed by AMANDA during application review.</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>Boolean</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>true</code><br></br><code>false</code></td>
  </tr>
</table>

#### 4.3.5 Attributes about Evidence

*Identity Verification Method*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>identity_verification_method</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>Specifies the method used to confirm the applicant’s identity (e.g., BC Person Credential, government-issued photo ID).</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>City of Vancouver Business Licence System (AMANDA); validated against BC Person Credential or supporting identity documents.</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>BC Person Credential</code><br></br><code>Driver’s Licence</code></td>
  </tr>
</table>

*Primary Address Verification Method*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>primary_address_verification_method</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>Specifies the method used to verify the applicant’s primary residential address (e.g., ICBC driver’s licence address, LTSA property records).</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>AMANDA; verified against ICBC address history, LTSA property records, or supporting documentation.</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>ICBC Address Record</code><br></br><code>LTSA Property Ownership</code></td>
  </tr>
</table>


## 5. Implementations

## 5.1 Technical Format

This credential uses the [Hyperledger AnonCreds](https://github.com/hyperledger/anoncreds/) specification and the "Municipal Property Rental Business Licence" schema which has the following defined attributes.

### 5.2 Issuer List
The Governing Authority of this Credential document attests that the following issuer information is accurate and can be relied upon by verifiers.
| Environment | Issuer Name | Issuer DID |
|------|------|-------|
| CANdy Production  | City of Vancouver     | TBA   |
| CANdy Dev  | City of Vancouver     | <code>HFZfqC6Jzbt57FxcXqn78a</code>   |

### 5.3 Schema Implementation
|Environment|Ledger|Schema ID|
|---|---|---|
|CANdy Production|TBA|TBA|TBA|
|CANdy Dev|[municipal-property-rental-business-licence](https://candyscan.digitaltrust.gov.bc.ca/tx/CANDY_DEV/domain/37509)|<code>HFZfqC6Jzbt57FxcXqn78a:2:municipal-property-rental-business-licence:1.0</code>|

### 5.4 Credential Implementation
|Environment|Ledger|Credential Definition ID|OCA Bundle|
|---|---|---|---|
|CANdy Production|TBA|TBA|TBA|
|CANdy Dev|[municipal-property-rental-business-licence](https://candyscan.digitaltrust.gov.bc.ca/tx/CANDY_DEV/domain/37511)|<code>HFZfqC6Jzbt57FxcXqn78a:3:CL:37509:municipal-property-rental-business-licence</code>|[City of Vancouver TEST Property Rental Business License](https://github.com/bcgov/aries-oca-bundles/tree/main/OCABundles/schema/CityOfVancouver/test-property-rental-business-licence)|
