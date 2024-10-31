---
layout: default
title: Verified .CA Domain Credential
parent: Credential Schemas
---

# Verified .CA Domain Credential Governance Framework (Primary Document)

# 1. Primary Document

## 1.1. Introduction

The [Canadian Internet Registration Authority (CIRA)](https://www.cira.ca/en/) (French: Autorité canadienne pour les enregistrements internet ACEI) is the organization that manages the .ca country code top-level domain (ccTLD) for Canada. CIRA sets the policies and agendas that support Canada's internet community and Canada's involvement in international internet governance. It is a member-driven organization with membership open to all that hold a .ca domain. As of March 2023, there were more than 3.3 million active .ca domains.

As digital trust technologies evolve, they present Canadians with innovative ways to engage with individuals, organizations, and digital entities online. CIRA aims to capitalize on its authoritative role as the overseer of .CA credentials. By transforming these credentials into machine-readable digital formats, CIRA hopes to offer versatile solutions that enhance protection for Canadians against fraud and cyber threats.

The development of this documentation follows the governance framework created by the [Trust over IP Foundation (ToIP)](https://trustoverip.org/) [Governance Metamodel Specification](https://trustoverip.org/wp-content/uploads/ToIP-Governance-Metamodel-Specification-V1.0-2022-12-21.pdf) created by the [Governance Stack Working Group (GSWG)](https://wiki.trustoverip.org/display/HOME/Governance+Stack+Working+Group).

These materials are made available under and are subject to the [Creative Commons Attribution 4.0 International license](http://creativecommons.org/licenses/by/4.0/legalcode).

THESE MATERIALS ARE PROVIDED “AS IS.” The Trust Over IP Foundation, established as the Joint Development Foundation Projects, LLC, Trust Over IP Foundation Series ("ToIP"), and its members and contributors (each of ToIP, its members and contributors, a "ToIP Party") expressly disclaim any warranties (express, implied, or otherwise), including implied warranties of merchantability, non-infringement, fitness for a particular purpose, or title, related to the materials. The entire risk as to implementing or otherwise using the materials is assumed by the implementer and user. 

IN NO EVENT WILL ANY ToIP PARTY BE LIABLE TO ANY OTHER PARTY FOR LOST PROFITS OR ANY FORM OF INDIRECT, SPECIAL, INCIDENTAL, OR CONSEQUENTIAL DAMAGES OF ANY CHARACTER FROM ANY CAUSES OF ACTION OF ANY KIND WITH RESPECT TO THESE MATERIALS, ANY DELIVERABLE OR THE ToIP GOVERNING AGREEMENT, WHETHER BASED ON BREACH OF CONTRACT, TORT (INCLUDING NEGLIGENCE), OR OTHERWISE, AND WHETHER OR NOT THE OTHER PARTY HAS BEEN ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

***Acknowledgements***

This governance framework includes structural elements from the Trust over IP Metamodel that were developed by Governance Stack Working Group of the Trust over IP Foundation, the eSSIF Lab Glossary and Mental Models, were contributed to the Trust Over IP Foundation under the CC BY-SA 4.0 license.  There have also been contributions from the Concepts & Terminology Working Group at ToIP, the Human Experience Working Group at ToIP and the Ecosystem Foundry Working Group at ToIP, the work of the Governance Framework Working Group at Sovrin Foundation is also acknowledged in providing support.

## 1.2. Terminology and Notation

Please reference [Glossary - General Trust Over IP Terms](https://trustoverip.github.io/toip/glossary).

**Requirements** include any combination of Machine-Testable Requirements and Human-Auditable Requirements. Unless otherwise stated, all Requirements MUST be expressed as defined in [RFC 2119](https://www.rfc-editor.org/rfc/rfc2119).

- Mandates are Requirements that use a MUST, MUST NOT, SHALL, SHALL NOT or REQUIRED keyword.
- Recommendations are Requirements that use a SHOULD, SHOULD NOT, or RECOMMENDED keyword.
- Options are Requirements that use a MAY or OPTIONAL keyword.

**Machine-Testable Requirements** are those with which compliance can be verified using an automated test suite and appropriate scripting or testing software.

**Rules** are Machine-Testable Requirements that are written in a Machine-Readable language and can be processed by a Rules Engine. They are expressed in a structured rules language as specified by the Governance Framework.

**Human-Auditable Requirements** are those with which compliance can only be verified by an audit of people, processes, and procedures.

**Policies** are Human-Auditable Requirements written using standard conformance terminology. The Policies used in the Governance Framework will use the standard terminology detailed in RFC 2119 keywords. Note that all RFC 2119 keywords have weight from an auditing perspective. An implementer MUST explain why a SHOULD or RECOMMENDED requirement was not implemented and SHOULD explain why a MAY requirement was implemented.

**Specifications** are documents containing any combination of Machine-Testable Requirements and Human-Auditable Requirements needed to produce technical interoperability.

## 1.3. Localization

The standard language for this governing framework (GF) is English.

## 1.4. Governing Authority

[The Canadian Internet Registration Authority (CIRA)](https://www.cira.ca/en/) is the governing authority that manages the Governance Framework (GF) for the .ca country code top-level domain (ccTLD) for Canada.

The contact information for [The Canadian Internet Registration Authority (CIRA)](https://www.cira.ca/en/) is:
* 	**Name:** Jacques Latour
* 	**Title:** CTO
* 	**Organization:** The Canadian Internet Registration Authority (CIRA)
* 	**Email:** [Jacques.Latour@cira.ca](mailto:Jacques.Latour@cira.ca)

## 1.5. Administering Authority

[Northern Block (NB)](https://northernblock.io/) is the Administering Authority on behalf of CIRA during the pilot phase of development.

The contact information for Northern Block is:
* 	**Name:** Mathieu Glaude
* 	**Title:** CEO
* 	**Organization:** Northern Block Inc.
* 	**Email:** [mathieu@northernblock.io](mailto:mathieu@northernblock.io)

## 1.6. Purpose

The purpose of this Governance Framework (GF) is to define the parameters of a Verified .CA Domain credential.

## 1.7. Scope

This Governance Framework applies to the .CA Domain credential from CIRA.

## 1.8. Objectives

TBA

## 1.9. Principles

*  **Canadian**: There is a Canadian presence requirement for individuals, organizations and businesses to register a .CA domain. It’s the only domain name extension that identifies a website as 100% Canadian.
*  **Trust**: .CA is an established top-level domain and recognized as a safe, secure and trusted resource for Canadians. CIRA has been managing the registry since 2000.
*  **Availability**: Avoid thatreallylongdomainname.com. You might have a better chance of getting the domain name you really want in a .CA.
*  **Community**: Proceeds from every .CA sold are reinvested directly into the Canadian internet community through the Net Good program.

## 1.10. General Requirements

Below are the requirements for a Registrant to receive a Verified .CA Domain Credential offer by CIRA:

![Signing Up for a Verified  CA Credential (Verified by CIRA) (2)](https://github.com/Northern-Block/CIRA-Digital-Trust/assets/67612904/32392da4-3f11-429c-9629-589035dacc0b)


## 1.11. Revisions
Version 1.0

## 1.12. Extensions
There are no extensions to this Governance Framework.

## 1.13. Schedule of Controlled Documents
TBD

# 2. Controlled Documents

## 2.1. Glossary

*  **Domain Registrant**: An individual or organization that registers a domain name. Holds the rights to use that domain name for a specified period. Responsible for renewing the domain and maintaining accurate contact information.
*  **Domain Registrar**: An organization or company authorized to register domain names on behalf of registrants. Manages the reservation of domain names. Provides services such as domain renewal, transfer, and management.
*  **Domain Authority**: Refers to the organization or entity responsible for managing and setting policies for a specific top-level domain (TLD) or country code top-level domain (ccTLD). Oversees the registration and administration of domain names under its TLD or ccTLD. Ensures the domain's stability, security, and adherence to international standards.

## 2.2. Risk Assessment
TBD

## 2.3. Trust Assurance and Certification
TBD

## 2.4. Governance Requirements
The Verified .CA Domain Credential is governed by the [**Verified .CA Domain Governance**](TBA) 

## 2.5. Business Requirements

The purpose of the Verified .CA Domain is to provide .CA registrants with a way to prove to anyone in the internet ecosystem that they are the rightful owners of a domain. 

One use case is to enable registrants to use their .CA Domain Credential as a high assurance authentication method to request for a RegistryLock service.

## 2.6. Technical Requirements (Credential)

The Verifiable Credential format for this credential is AnonCreds specification (https://anoncreds-wg.github.io/anoncreds-spec/)

### 2.6.1 Schema Definition

__Schema Name:__ verified_domain_credential

__Schema Version:__ 1.0

This schema definition follows the AnonCreds specification (https://anoncreds-wg.github.io/anoncreds-spec/)

Attribute | Format | Rules | Notes
--- | --- | --- | ---
domain_name | String | Not NULL | name of domain name
domain_ownership_date_start | Date | Not NULL | start date of domain ownership
domain_ownership_date_end | Date | Not NULL | end date of domain ownership
registrant_id | String | Not NULL | unique id of the registrant
admin_name | String | Not NULL | name of the domain admin
admin_id | String | Not NULL | id of the domain admin

### 2.6.2. Credential Implementation
Ledger | SCHEMA DEF | CRED DEF | Notes	
--- | --- | --- | ---
BCovrin Test | TBD | --- | ---

## 2.7. Information Trust Requirements

[CIRA Privacy of Information](https://www.cira.ca/en/privacy-policy/)

## 2.8. Legal Agreements
TBD

# End of Document

# Backlog/Comments (Info to add into document)

- How the Revocation process will work
- There's a requirement that the domain owner need to be transparent, and not privacy anonymized (also add into UI disclosure)
- Managing multiple domains
- Update schema for multiple domains (actor) – update schema doc
