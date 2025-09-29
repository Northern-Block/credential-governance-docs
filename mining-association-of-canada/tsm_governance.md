# Schema: tsm-performance-2023  
**Credential Name:** 2023 TSM Performance Credential  

| Category | Name | Attribute | Format | Rules | Notes |
|----------|------|-----------|--------|-------|-------|
| Facility | Company Name | company_name | String | Not NULL | name of business entity |
| Facility | Facility Name | facility_name | String | Not NULL | name of facility |
| Facility | Facility Address | facility_address | String | Not NULL | address of facility |
| Facility | Country of Operation | country_operation | String | Not NULL | country of facility |
| Facility | Products | products_name | String | Not NULL | name of products or metals produced on site |
| Facility | Operation | operation_type | String | Not NULL | lists all types of operations included in scope: mining, milling, hydrometallurgical, concentrate blending, smelting, refining, other |
| Verification | Verification Company | verification_company_name | String | Not NULL | name of verification company |
| Verification | Audit conducted by Accredited TSM Verifier | accredited_tsm_verifier | String | Not NULL | yes, no: confirms all verifiers involved are accredited TSM verifiers |
| Verification | Verification Dates | verification_dates | String | Not NULL | comment field that provides the dates of verification activities, list each date in format YYYY/MM/DD |
| Verification | Verification Method | verification_method_summary | String | Not NULL | textbox, summary description of verification method - includes disclosure of sampling methodology employed |
| Verification | Verification Activities | verification_activities_summary | String | Not NULL | textbox, summary description of verification activities |
| Verification | Verification Site Visit Conducted | verification_site_visit | String | Not NULL | yes, no: confirms if verification included a site visit |
| Verification | Verification Statement | verification_statement_tor | String | Not NULL | yes, no - confirms if external verification was conducted in accordance with the Terms of Reference for Verifiers and, accordingly, consisted primarily of interviews, data analysis, and examination (on a sample basis) of other evidence relevant to management’s assertion of conformance to the requirements of the TSM performance indicators. |
| Verification | Verification Accuracy | verification_statement_accuracy | String | Not NULL | yes, no - confirms scores indicated by verification activities are accurate based on the evidence reviewed during the external verification |
| Verification | Verification Limitations | verification_statement_limitations | String | Not NULL | textbox, verifier identified limitations |
| Verification | Verification Comments | verification_statement_comments | String | Not NULL | textbox, verifier comments |
| Verification | Verification Assurance Statement Provided | verification_assurance | String | Not NULL | yes, no - confirms if an additional assurance statement provided by verifier |
| Verification | Lead Verifier | verification_statement_lead_name | String | Not NULL | textbox, the full legal name of the lead verifier with the option to include the names of all verifiers who participated in the audit. |
| Verification | Verification Statement Date | verification_statement_dateint | String | Not NULL | date field as an integer, using format YYYYMMDD |
| Verification | Verification Signature | verification_statement_signature | String | Not NULL | textbox, printed signature of lead verifier |
| Indigenous and Community Relationships | COI Identification | indigenous_q1 | String | Not NULL | levels C - AAA, Community of Interest (COI) Identification |
| Indigenous and Community Relationships | COI Identification Evidence | indigenous_q1_evidence | String | Not NULL | textbox, verification examples of evidence consulted |
| Indigenous and Community Relationships | COI Engagement | indigenous_q2 | String | Not NULL | levels C - AAA, Community of Interest (COI) Engagement |
| Indigenous and Community Relationships | COI Engagement Evidence | indigenous_q2_evidence | String | Not NULL | textbox, verification examples of evidence consulted |
| Indigenous and Community Relationships | Indigenous Engagement | indigenous_q3 | String | Not NULL | levels C - AAA, effective Indigenous engagement and dialogue |
| Indigenous and Community Relationships | Indigenous Engagement Evidence | indigenous_q3_evidence | String | Not NULL | textbox, verification examples of evidence consulted |
| Indigenous and Community Relationships | Community impact | indigenous_q4 | String | Not NULL | levels C - AAA, community impact and benefit management |
| Indigenous and Community Relationships | Community impact Evidence | indigenous_q4_evidence | String | Not NULL | textbox, verification examples of evidence consulted |
| Indigenous and Community Relationships | COI Response | indigenous_q5 | String | Not NULL | levels C - AAA, Community of Interest (COI) response mechanism |
| Indigenous and Community Relationships | COI Response Evidence | indigenous_q5_evidence | String | Not NULL | textbox, verification examples of evidence consulted |
| Safety and Health | Commitments/Accountability | safety_health_q1 | String | Not NULL | levels C - AAA, commitments and accountability |
| Safety and Health | Commitments/Accountability Evidence | safety_health_q1_evidence | String | Not NULL | textbox, verification examples of evidence consulted |
| Safety and Health | Planning/Implementation | safety_health_q2 | String | Not NULL | levels C - AAA, planning and implementation |
| Safety and Health | Planning/Implementation Evidence | safety_health_q2_evidence | String | Not NULL | textbox, verification examples of evidence consulted |
| Safety and Health | Training/Behaviour/Culture | safety_health_q3 | String | Not NULL | levels C - AAA, training, behaviour and culture |
| Safety and Health | Training/Behaviour/Culture Evidence | safety_health_q3_evidence | String | Not NULL | textbox, verification examples of evidence consulted |
| Safety and Health | Monitoring/Reporting | safety_health_q4 | String | Not NULL | levels C - AAA, monitoring and reporting |
| Safety and Health | Monitoring/Reporting Evidence | safety

