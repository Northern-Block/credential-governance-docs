# Municipal Property Rental Business License Credential Documentation

## About this Document

This document describes the Municipal Property Rental Business Licence verifiable credential to help potential verifiers determine whether it is suitable for their needs. The intended audience includes policy analysts, privacy specialists, solution architects, developers, and data architects.

The credential is issued by the City of Vancouver, Business Licenses Division, and represents a valid municipal business licence for operating rental properties, initially covering short-term rental (STR) and long-term rental (LTR) business licence types.

### Version History

| Ver.      | Date | Notes |
| ----------- | ----------- | ----------- |
| <b>1.0</b>      | 25-Aug-2025       | Initial release |

## Credential Overview
The Municipal Property Rental Business Licence credential is a verifiable credential (VC) issued to individuals or authorized representatives of businesses to prove that they hold a valid City of Vancouver rental business licence.

The credential is intended to be used in a wide range of contexts, both alone or alongside other credentials (e.g., BC Person Credential, Digital Business Card), as a trusted source of business licence information for verifiers such as platforms (Airbnb, VRBO), municipal inspectors, or other government agencies.

<table>
  <tr>
    <th>Credential</th>
    <td>Municipal Property Rental Business Licence</td>
  </tr>
  <tr>
    <th>Issuer</th>
    <td>City of Vancouver, Business Licenses Division</td>
  </tr>
  <tr>
    <th>Issuer DID</th>
    <td><code>HFZfqC6Jzbt57FxcXqn78a</code></td>
  </tr>
  <tr>
    <th>Schema</th>
    <td>
      municipal-property-rental-business-licence, version 1.0
      <ul>
        <li>
          Schema ID: 
          <a href="https://candyscan.digitaltrust.gov.bc.ca/tx/CANDY_DEV/domain/37509">
            HFZfqC6Jzbt57FxcXqn78a:2:municipal-property-rental-business-licence:1.0
          </a>
        </li>
      </ul>
    </td>
  </tr>
  <tr>
    <th>Credential Definition</th>
    <td>
      municipal-property-rental-business-licence, version 1.0
      <ul>
        <li>
          Cred Def ID: 
          <a href="https://candyscan.digitaltrust.gov.bc.ca/tx/CANDY_DEV/domain/37511">
            HFZfqC6Jzbt57FxcXqn78a:3:CL:37509:municipal-property-rental-business-licence
          </a>
        </li>
      </ul>
    </td>
  </tr>
  <tr>
    <th>Data Registry</th>
    <td>
      BCovrin (CANdy Dev Ledger)
      <ul>
        <li>
          <a href="https://candyscan.digitaltrust.gov.bc.ca/home/CANDY_DEV">Ledger Browser</a>
        </li>
      </ul>
    </td>
  </tr>
  <tr>
    <th>Holders</th>
    <td>
      The credential is available to:
      <ul>
        <li>Licence applicants who successfully completed City of Vancouver’s standard review and approval process</li>
        <li>Designated business representatives authorized by the licence holder</li>
      </ul>
    </td>
  </tr>
  <tr>
    <th>Data Source</th>
    <td>
      City of Vancouver Business Licence System of Record (AMANDA).  
      Data is verified against foundational identity documents (e.g., BC Person Credential, government-issued photo ID),  
      property ownership records (LTSA), and authorization letters where applicable.
    </td>
  </tr>
  <tr>
    <th>Revocation</th>
    <td>
      Revoked if the business licence is withdrawn, invalidated, expired, or amended in the City’s licensing system.  
      Re-issued upon approved changes (e.g., address updates, new trade name).
    </td>
  </tr>
  <tr>
    <th>Assurance</th>
    <td>
      Issuance requires successful validation of the applicant’s identity via the BC Person Credential,  
      along with business and property checks (ICBC address history, LTSA property lookup, owner’s Letter of Authorization).
    </td>
  </tr>
</table>


### Attribute Summary

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
| Property Residence Type       | `property_residence_type`          | String        |
| Neighbourhood / Local Area    | `local_area`                       | String        |
| Location Type                 | `location_type`                    | String        |
| Number of Dwelling Units      | `number_of_dwelling_units`         | String        |
| Parcel Identifier (PID)       | `PID`                              | String        |
| Strata Property (Yes/No)      | `strata_flag`                      | String        |
| Map Coordinates (Lat/Long)    | `GIS_coordinates`                  | String        |

## Credential Details

### Issuer

The Municipal Property Rental Business Licence credential is issued by the **City of Vancouver, Business Licenses Division**. The City is responsible for the creation, approval, renewal, and revocation of all municipal business licences within its jurisdiction.

The City of Vancouver is responsible for:

- Administering the <a href="https://vancouver.ca/your-government/licence-bylaw.aspx">Business Licence Bylaw</a>, including processing applications, renewals, and amendments to licences.
- Operating the **Business Licence System of Record (AMANDA)**, which records licence issuance, renewals, revocations, and changes to attributes such as business trade name or location.
- Reviewing foundational identity, property ownership, and authorization documentation as part of the licensing process.

### Schema and Credential Definition Governance

The Municipal Property Rental Business Licence credential definition implements the schema published by the City of Vancouver. Both the schema and credential definition are registered on the CANdy Dev Ledger.

The City of Vancouver may, after appropriate consultation and notification, update the credential definition and/or schema to reflect policy or operational changes. Updates will follow the broader municipal credential governance framework and are designed for eventual province-wide interoperability

### Issuer Data Source

The data in the Municipal Property Rental Business Licence credential comes from the City of Vancouver’s Business Licence system (AMANDA). The City generates some information directly and verifies others against trusted sources.

- **Business Licence Filing** – the information provided by or on behalf of the applicant during the licence application or renewal process.
- **City of Vancouver Business Licence System (AMANDA)** – system-generated data such as licence number, revision number, and timestamps.
- **Foundational Identity Verification** – records checked through the <a href="https://ltsa.ca/">Land Title and Survey Authority (LTSA)</a> to confirm ownership or authorized use of the property.
- **Property Ownership Verification** – the information is provided to the BC Registries system directly from a CRA system.
- **Authorization Verification** – an Owner’s Letter of Authorization, where applicable, is collected and retained.

The source of each attribute is described in the [Attributes](#bookmark=id.d4k15yq1kvi3) section.

#### Data Updates

When a credential is issued, its data reflects the business licence record at the time of issuance. Changes to licence records (e.g., business trade name, ownership, address) trigger a revocation and re-issuance of the credential so that the holder’s credential always reflects current information.

### Assurance

To minimize risk to verifiers, the City, and licence holders, the Municipal Property Rental Business Licence credential is only issued following successful authentication and validation of:

- **Applicant identity** – via the BC Person Credential (high-assurance, Level 3 trusted digital identity).
- **Primary address history** – verified using ICBC address records or the Person Credential.
- **Property ownership** – verified against LTSA property records.
- **Authorization** – verified by requiring an Owner’s Letter of Authorization if the applicant is not the property owner.

These checks ensure the authenticity of the relationship between the applicant, the business, and the property location.

### Revocation

A Municipal Property Rental Business Licence credential will be revoked in the following cases:

1. The underlying business licence is withdrawn, invalidated, or expires.
2. The business licence record is updated (e.g., new address, ownership, or trade name).
3. The licence holder or designated representative is no longer authorized.

In most cases, a revocation triggers a **re-issuance** of the credential with updated details to reflect the new licence record

## Credential Definition

### Credential Schema

The Municipal Property Rental Business Licence credential is based on the municipal-property-rental-business-licence schema, version 1.0, published by the City of Vancouver and maintained in BCovrin.

### Subject of the Credential

The subject of the credential is the licence record, which ties:

- The individual or authorized representative (credential holder), and
- The business/property information associated with the licence.

The credential enables the holder to prove, in real time, that they are licensed by the City of Vancouver to operate a rental business (short-term or long-term).

### Attributes

The attributes of the DBC credential are organized by topic and described below.

#### Attributes about the Credential

*Credential ID*

<table>
  <tr>
    <th>Attribute</th>
    <td><code>credential_id</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>A unique identifier assigned by BC Registries that is specific to the relationship between the individual and the business.<br></br>
    This is intended to aid verifiers when the name of the individual and/or the business changes.</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>BC Registries system, created when a credential is first issued to the individual for the business.</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Format</th>
    <td><ul><li>8 digits, padded left with zeros</li></ul></td>
  </tr>
  <tr>
    <th>Rules</th>
    <td>
        <ul>
            <li>Never blank</li>
            <li>When a different credential is issued to the same individual for the same organization, the value of the Credential ID will be the same in both credentials unless BC Registries cannot confirm it is the same individual.</li>
        </ul>
    </td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>00000001</code><br></br><code>00012345</code></td>
  </tr>
  <tr>
    <th>Notes</th>
    <td>
        <ul>
            <li>This attribute is intended to aid verifiers when they transact with:</li>
                <ul>
                    <li>Multiple individuals affiliated with a single business</li>
                    <li>Single individuals who represent multiple businesses</li>
                    <li>Individuals who have changed their name</li>
                </ul>
        </ul>
    </td>
  </tr>
</table>

### Attributes about the Individual

The DBC credential includes the business contact name for the individual, as well as their role with the business, if any has been filed with BC Registries.

The DBC credential gets the values for its name attribute from the BC Services Card Program, which obtains them from the individual’s Canadian foundational identity documents. Due to limitations in the source systems of the BC Services Card program partners, some individual’s names – in the BC Services Card and by extension the DBC credential – will not match what is on their foundational identity documents in the following cases:

- If an individual's name has a special character (e.g., Á, Ê, Ç) or a number in their name on their foundational identity document, it will not be reflected in the name attributes of the Person credential
- The name in the Person credential will normally reflect the name on foundational identity documents, but those documents may not reflect the individual’s name. For example:
  - Some names have special characters that BC Vital Statistics will not accept and print on a birth certificate
  - Immigration, Refugees and Citizenship Canada (IRCC) will truncate an individual’s name (the combined given names and family name) at 45 characters on IIRC foundational identity documents (e.g., permanent resident card and the student, work, visitor, and temporary-resident permits)
- An individual may use the last name of their spouse without getting a legal name change. In these cases, their Person credential should reflect their foundational identity documents, as individuals are required by law to update their BC Services Card when they change their name by marriage or otherwise. Individuals who do this may continue to use their original name in other contexts, and so their Person credential may not be consistent with their other identity documents or credentials bearing their name

Note that the Person credential gets the values for its name attribute values from the BC Services Card and so has the same data limitations as the BC Services Card.

#### Given Names

<table>
  <tr>
    <th>Attribute</th>
    <td><code>given_names</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>The individual's documented given names (first and middle) recorded from valid identification.</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>The individual’s Registries Account name attributes, which come from the individual’s BC Services Card digital identity.</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Format</th>
    <td>
        <ul>
            <li>Maximum 47 characters</li>
            <li>Always upper case</li>
            <li>Consists of three names, a first name and up to two middle names, delimited by spaces</li>
            <ul><li>Each name may be up to 15 characters long</li></ul>
            <li>The only characters allowed are the letters A through Z and the following "special characters": hyphen, apostrophe, period, and space</li>
        </ul>
    </td>
  </tr>
  <tr>
    <th>Rules</th>
    <td>
        <ul>
            <li>May be blank</li>
            <li>First and middle names over 15 characters are truncated</li>
            <li>If the individual has a mononym this attribute will <i>normally</i> have no value and the mononym will appear in the family_name attribute</li>
        </ul>
    </td>
  </tr>
  <tr>
    <th>Notes</th>
    <td>
        <ul>
            <li>Names can start with special characters</li>
            <li>First Names and Middle Names with spaces or punctuation (e.g., “JO ANNE”, “JIAN U”, “D’ARCY”) will have the spaces and punctuation removed (e.g., “JOANNE”, “JIANU”, “DARCY”)</li>
            <li>To work around the removal of spaces, described above, a first name with a space (e.g. “JO ANNE”) may be entered as a first name and a middle name (e.g., “JO ANNE” is entered as “JO” and “ANNE”). This will appear as “JO ANNE” in the given_names attribute, which is indistinguishable from an individual whose first name is “JO” and whose middle name is “ANNE”. Similarly, a middle name with a space (e.g., “MARY LOU”) may be entered as two middle names (e.g., “MARY” and “LOU”). As such, spaces in the given_names attribute are not a reliable delimiter between names</li>
            <li>Some legacy records have only an initial for a middle name (e.g., "J" for "James")</li>
            <li>A mononym may be duplicated in this attribute and the family_name unless it has a space in it, in which case the first part may be recorded in this attribute and the second part in the family_name attribute</li>
        </ul>
    </td>
  </tr>
</table>


#### Family Name

<table>
  <tr>
    <th>Attribute</th>
    <td><code>family_name</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>The individual's documented family name (i.e. surname) recorded from valid identification.</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>The individual’s Registries Account name attributes, which come from the individual’s BC Services Card digital identity.</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Format</th>
    <td>
        <ul>
            <li>Maximum 35 characters</li>
        </ul>
    </td>
  </tr>
  <tr>
    <th>Rules</th>
    <td>
        <ul>
            <li>Never blank</li>
            <li>Always upper case</li>
            <li>Family names over 35 characters are truncated</li>
            <li>The only characters allowed are the letters A through Z and the following "special characters": hyphen, apostrophe, period, and space</li>
        </ul>
    </td>
  </tr>
  <tr>
    <th>Notes</th>
    <td>
        <ul>
            <li>Last Names with spaces or punctuation (e.g., “St. John”, “O’Brian”, “van Cleef”, “Scott-Bigsby”) will have the spaces and punctuation included if the individual has a photo BC Services Card but removed if the individual has a non-photo BC Services Card</li>
            <li>A mononym may be duplicated in this attribute and the family_name unless it has a space in it, in which case the first part may be recorded in this attribute and the second part in the family_name attribute</li>
        </ul>
    </td>
  </tr>
</table>

#### Role

<table>
  <tr>
    <th>Attribute</th>
    <td>role</td>
  </tr>
  <tr>
    <th>Description</th>
    <td>
        The person's role(s) with the business, if any. <br></br>
        Roles are limited to those tracked by BC Registries, and do not normally correspond to job titles.
    </td>
  </tr>
  <tr>
    <th>Source</th>
    <td>
        Currently a business filing, either from when an individual sets up the entity or a subsequent filing, creates the record of the invidual's role.
        The relationship between the individual being issued the credential and their role is determined at issuance by matching the name of the individual to that in the filing and either:
        <ul>
            <li>Confirming in the system that the individual was the person who registered the entity</li>
            <li>Having the individual self-attest that they are the individual with the matching role</li>
        </ul>
    </td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Format</th>
    <td>
        <ul>
            <li>Maximum 30 characters</li>
        </ul>
    </td>
  </tr>
  <tr>
    <th>Rules</th>
    <td>
        <ul>
            <li>Roles are limited to those defined by BC Registries (and/or its governing legislation) and by the Business Type. (For clarity, this will not include the person's role within or in relation to the organization, e.g., CEO, Accountant.)</li>
            <li>Allowable values (currently) are:</li>
            <ul>
                <li>Proprietor</li>
                <li>Partner</li>
                <li>Director</li>
                <li><em>blank</em>, indicating that the individual does not have any of the other roles, or if their role(s) cannot be confidently determined by BC Registries</li>
            </ul>
            <li>In future, allowable values may include:</li>
            <ul>
                <li>Incorporator</li>
            </ul>
            <li>An individual who is an Incorporator may have another role. In future, multiple roles will be separated by commas</li>
        </ul>
    </td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>Partner</code><br></br><code>Proprietor</code><br></br><code>Incorporator, Proprietor</code></td>
  </tr>
</table>

### Attributes about the Business

#### Identifier

<table>
  <tr>
    <th>Attribute</th>
    <td><code>identifier</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>A unique and permanent identifier that BC Registries creates and assigns to the business at the time the business is incorporated or registered with BC Registries.</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>BC Registries system, created when the business is registered or incorporated</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Format</th>
    <td>
        <ul>
            <li>10 characters</li>
            <li>Typically two letters followed by eight digits</li>
        </ul>
    </td>
  </tr>
  <tr>
    <th>Rules</th>
    <td>
        <ul>
            <li>Never blank</li>
            <li>Depending on the Business Type, the source of the BC Number is:</li>
            <ul>
                <li>Registration Number – Sole Proprietorship, General Partnership, and extra-provincial entities</li>
                <li>Incorporation Number – Corporations, Societies, Cooperative Associations</li>
            </ul>
        </ul>
    </td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>FM0055205</code></td>
  </tr>
  <tr>
    <th>Notes</th>
    <td>
        <ul><li>This identifier can be used to get additional information about the business from BC Registries through <a href="https://orgbook.gov.bc.ca/">OrgBook</a> or <a href="https://developer.api.bcregistry.gov.bc.ca/">BC Registries API Gateway</a>.</li></ul>
        This attribute is in close alignment with:
        <ul><li>Open Ownership schema: <code>Identifier ID</code></li></ul>
    </td>
  </tr>
</table>

#### CRA Business Number

<table>
  <tr>
    <th>Attribute</th>
    <td><code>cra_business_number</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>A unique identifier assigned to the business’ BC Registries business program area by the Canada Revenue Agency (CRA), a “BN15”.</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>Canada Revenue Agency,<ul><li>A business number is automatically provided to new B.C. corporations, businesses or societies as part of the registration or incorporation process.</li></ul></td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Format</th>
    <td>
        <ul><li>15 characters</li></ul>
    </td>
  </tr>
  <tr>
    <th>Rules</th>
    <td>
        <ul>
            <li>May be blank</li>
            <ul><li>This will be blank if CRA has not created the business number or BC Registries does not know the Business Number assigned by CRA</li></ul>
            <li>This will be a 15-digit (BN15) number</li>
        </ul>
    </td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>123456789BC0001</code></td>
  </tr>
  <tr>
    <th>Notes</th>
    <td>
        <ul>
            <li>A business may change its Business Number with CRA, and CRA will normally update BC Registries of the change</li>
            <li>For more information on Business Numbers, refer to the CRA</li>
        </ul>
        This attribute is in close alignment with:
        <ul><li>XBRL schema: <code>identifierTaxCode</code></li></ul>
    </td>
  </tr>
</table>


#### Business Name

<table>
  <tr>
    <th>Attribute</th>
    <td><code>business_name</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>The operating name the business has registered for itself with BC Registries.<br></br>In future this may also be the operating name of a general partnership or the legal name of an incorporated company, a society, or a cooperative association.</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>Business filing</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Format</th>
    <td>
        <ul><li>Maximum 150 characters</li></ul>
    </td>
  </tr>
  <tr>
    <th>Rules</th>
    <td>
        <ul><li>Never blank</li></ul>
    </td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>Rogers Communications Canada Inc.</code><br></br><code>12345676, Inc</code><br></br><code>Twelve Oaks Construction</code></td>
  </tr>
  <tr>
    <th>Notes</th>
    <td>
        This attribute is in close alignment with:
        <ul><li>Open Ownership schema: <code>name</code></li></ul>
    </td>
  </tr>
</table>

#### Business Type

<table>
  <tr>
    <th>Attribute</th>
    <td><code>business_type</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>The type of business as defined by the legislation governing BC Registries.</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>Business filing</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Format</th>
    <td>
        <ul><li>Maximum 100 characters</li></ul>
    </td>
  </tr>
  <tr>
    <th>Rules</th>
    <td>
        <ul>
            <li>Never blank</li>
            <li>The possible values are:</li>
            <ul>
              <li>Sole Proprietorship</li>
              <li>General Partnership</li>
              <li>Benefit Company</li>
            </ul>
        </ul>
    </td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>Sole Proprietorship</code><br></br><code>Benefit Company</code></td>
  </tr>
  <tr>
    <th>Notes</th>
    <td>
        <ul><li>Credential issuance will be limited to businesses that are created in the new BC Registries system. Additional business types may be added in the future</li></ul>
        This attribute is in close alignment with:
        <ul><li>Open Ownership schema: <code>entityType</code></li></ul>
    </td>
  </tr>
</table>

#### Registered On

<table>
  <tr>
    <th>Attribute</th>
    <td><code>registered_on_dateint</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>The date the business was incorporated or registered in BC with BC Registries.</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>BC Registries system</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Format</th>
    <td>
        <ul><li>Eight digits in the format YYYYMMDD</li></ul>
    </td>
  </tr>
  <tr>
    <th>Rules</th>
    <td>
        <ul><li>Never blank</li></ul>
    </td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>20180816</code></td>
  </tr>
  <tr>
    <th>Notes</th>
    <td>
        For companies incorporated in BC, this attribute is in close alignment with:
        <ul><li>Open Ownership schema: <code>foundingDate</code></li></ul>
    </td>
  </tr>
</table>


#### Company Status

<table>
  <tr>
    <th>Attribute</th>
    <td><code>company_status</code></td>
  </tr>
  <tr>
    <th>Description</th>
    <td>The status of the business at the time the credential is issued.</td>
  </tr>
  <tr>
    <th>Source</th>
    <td>BC Registries system, set when the business is first registered or incorporated and updated either by business filings or the Registrar (e.g., due to failure to file)</td>
  </tr>
  <tr>
    <th>Data Type</th>
    <td>String</td>
  </tr>
  <tr>
    <th>Format</th>
    <td></td>
  </tr>
  <tr>
    <th>Rules</th>
    <td>
        <ul>
            <li>Never blank</li>
            <li>This may be either:</li>
            <ul>
                <li>Active</li>
                <li>Historical</li>
            </ul>
        </ul>
    </td>
  </tr>
  <tr>
    <th>Examples</th>
    <td><code>Active</code><br></br><code>Historical</code></td>
  </tr>
  <tr>
    <th>Notes</th>
    <td>
        There are cases where a person may represent a “Historic” business (e.g., tax audits can occur several years after a business is dissolved), and so it is possible for an individual have a DBC credential for such a business
    </td>
  </tr>
</table>
