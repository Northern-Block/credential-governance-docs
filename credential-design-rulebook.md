# Rulebook for Designing Verifiable Credentials

**Version 0.1 (Living Document)**  

This Rulebook guides you in designing verifiable credentials that are:

- **Useful** to relying parties (verifiers)
- **Grounded** in your authority as issuer
- **Clear** in purpose
- **Appropriate** to the ecosystem they participate in

This document will evolve over time as more lessons are learned.


## ⚖️ Principles & Rules


### Principle 1 — Issue Only What You Are the Authoritative Source For

You should only issue attributes you are truly authoritative for.  

#### Rule 1.1
Include only attributes for which your organization is the recognized source of truth.  

✅ Example:  
- A municipality **is authoritative** for business license number, business type, issuance dates  
- A BC municipality **is not authoritative** for personal identity or foundational address (which come from the BC Person credential)  

#### Rule 1.2
Do not include attributes just because you have them on file—include them only if you are the authoritative issuer.  

#### Rule 1.3 
If verifiers will need other attributes (like proof of identity), design your credential assuming the verifier will request a **compound proof** that includes both your credential and credentials from other authoritative issuers.


## Principle 2 — Think in Terms of Attribute Presentations, Not Credential Presentations

A credential is **a container of attributes**. Verifiers do not always require every attribute, nor must they always rely on the container itself.  

#### Rule 2.1
Design credentials so holders can share individual attributes as needed (selective disclosure).  

#### Rule 2.2
Recognize that in some cases, verifiers **do** rely on knowing a holder possesses the credential as a whole—for example, “this person has a BC Person credential” or “this business has a City of Vancouver Business License.” This is valid when the presence of the credential itself conveys meaningful status.  

#### Rule 2.3
When designing, think primarily about **what attributes verifiers are likely to request** for their business needs, rather than assuming the entire credential will always be presented.

✅ Example:  
- An Airbnb verifier may only need:
  - License Number
  - Business Type
  - Expiry Date

✅ Also valid:
- A regulator may simply need proof that a Business License credential was issued.


## Principle 3 — Keep Attributes Relevant to the Ecosystem

Only include attributes that are meaningful for verifiers beyond your organization.  

#### Rule 3.1
Avoid cluttering credentials with internal-use data that has no external purpose.  

✅ Example:  
- License issue/expiry dates, license number, business type

❌ Example:
- Application fees paid, processing timestamps

#### Rule 3.2  
If certain data is important for your internal processes (e.g., fee tracking), **manage that data internally**—it does not belong in the credential.  


## Principle 4 — Prove Everything Cryptographically

Everything you include in your credential should be provable through cryptographic evidence, not just stored as unverified statements.

#### Rule 4.1
Do not include “proof” fields that merely record that you looked at a document or did a manual check.  

✅ Example:
- A cryptographic signature or a verifiable presentation proving an identity check happened.

❌ Example:
- A text field that says “passport was visually inspected on Jan 1, 2024.”

#### Rule 4.2
If you perform checks that are important context for relying parties but cannot be cryptographically proven, document them **in your governance documentation**, not in the credential itself.


## Principle 5 — Document Your Issuance Process Clearly

Ensure your governance documentation fully describes how and **why** your credential can be trusted, so verifiers understand the context behind the attributes you issue.

#### Rule 5.1 
Your governance documentation must clearly describe:
- How the credential is issued
- Data sources
- Verification steps (e.g., identity proofing)
- Revocation conditions

#### Rule 5.2
Include references to relevant laws, regulations, or bylaws establishing your authority.

✅ Example from the Lawyer Credential:
> "The credential is issued under the Legal Profession Act of BC. Only lawyers in 'Practicing' status are eligible, as recorded in the Law Society's official registry."

---

## Checklist Before You Finalize a Credential Schema

✅ Are you authoritative for every attribute?  
✅ Are attributes relevant to external verifiers?  
✅ Can attributes be selectively disclosed?  
✅ Are all proofs cryptographic?  
✅ Does the governance document fully describe issuance, verification, and revocation processes?  
✅ Is the credential designed to support both attribute-level and whole-credential presentations where appropriate?

---

## Examples of Good Design Choices

**Person Credential**  
- All attributes come from the BC Services Card identity record (foundational source)  
- Attributes are relevant to almost any verifier that needs proof of identity  
- Self-asserted data (like address) is clearly labelled and explained in documentation  

**Lawyer Credential**  
- Only includes data the Law Society is authoritative for (status, membership ID, name)  
- The credential itself is evidence of membership in good standing  
- No internal-only attributes are included  

**Digital Business Card**  
- Combines business and person data only when the issuer is authoritative for both  
- Attributes about the person come from their BC Services Card identity  
- Attributes about the business come from the BC Registries system  

---

# 📘 Next Steps

1. Validate this Rulebook with your partners (e.g., BC Government) to confirm alignment.
2. Apply it to analyze and revise the City of Vancouver Business License Credential.
3. Continue updating this Rulebook as new examples and lessons emerge.
