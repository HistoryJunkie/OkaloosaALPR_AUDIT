# Project Knowledge Base Documentation
## ALPR Compliance & Oversight Project - Okaloosa County Sheriff's Office

**Last Updated:** January 17, 2026  
**Project Focus:** Automated License Plate Reader (ALPR) policy compliance, operational transparency, and privacy protection analysis

---

## Document Inventory & Descriptions

### **1. Legal & Regulatory Framework**

#### **1.1 Florida Statutes**

**FL_Statute_119.011.md** - *Public Records Definitions*
- **Type:** State Statute
- **Purpose:** Defines key terms used throughout Florida's public records law
- **Key Definitions:**
  - "Agency" - Any state, county, municipal officer/department/division
  - "Criminal Intelligence Information" - Info collected to anticipate/prevent/monitor possible criminal activity
  - "Criminal Investigative Information" - Info compiled during a criminal investigation
  - "Active" investigation criteria
- **Use Case:** Reference for understanding what constitutes a public record and what qualifies as exempt information

**FL_Statute_119.07.md** - *Public Records Access & Inspection*
- **Type:** State Statute  
- **Purpose:** Establishes rights and procedures for public access to government records
- **Key Provisions:**
  - Right to inspect and copy public records
  - Procedures for handling record requests
  - Remote electronic access provisions
  - Photography of public records
  - Enforcement mechanisms for denied requests
- **Use Case:** Legal basis for requesting ALPR audit logs and other law enforcement records

**FL_Statute_316.0777.md** - *Automated License Plate Recognition Systems (Use Authorization)*
- **Type:** State Statute
- **Purpose:** Authorizes law enforcement use of ALPR systems and establishes data protection requirements
- **Key Provisions:**
  - Criminal justice purpose requirement
  - Data security mandates
  - Sharing restrictions
  - Protection of ALPR data under public records exemptions
- **Use Case:** Primary statute governing lawful ALPR deployment and use

**FL_Statute_316.0778.md** - *ALPR Data Retention & Deletion*
- **Type:** State Statute
- **Purpose:** Mandates retention schedules and deletion procedures for ALPR data
- **Key Provisions:**
  - 30-day general retention period for tactical use
  - 3-year maximum for ongoing investigations
  - Mandatory deletion requirements
  - Penalties for violations
- **Use Case:** Benchmark for evaluating whether agencies comply with data retention limits

**FL_Statute_501.171.md** - *Security of Confidential Personal Information*
- **Type:** State Statute
- **Purpose:** Defines personal information (PII) and requires security measures for its protection
- **Key Provisions:**
  - Definition of "Personal Information" including geolocation data
  - "Breach of security" definitions
  - Data protection requirements for covered entities
  - Notification requirements for data breaches
- **Use Case:** Determine whether ALPR geolocation tracking constitutes PII requiring special protection

**FL_Senate_Bill_599_2014.md** - *Legislative History*
- **Type:** Session Law / Bill Text
- **Purpose:** Original legislation authorizing ALPR use in Florida
- **Content:** Background on why ALPR statute was created, legislative intent, original provisions
- **Use Case:** Understanding legislative intent behind current ALPR statutes

---

#### **1.2 State Guidelines**

**FDLE_ALPR_Guidelines_2024.md** - *Official State ALPR Policy Guidelines*
- **Type:** Administrative Guidelines
- **Issuing Authority:** Florida Department of Law Enforcement (FDLE), Criminal and Juvenile Justice Information Systems (CJJIS) Council
- **Approval Date:** November 13, 2024
- **Purpose:** Provide statewide direction to law enforcement agencies on ALPR use and data management
- **Key Sections:**
  1. **Purpose & Objectives** - Balance public safety with privacy rights
  2. **Policy Requirements:**
     - Agency implementation mandates
     - Criminal justice purpose only
     - Supervisory approval requirements
  3. **Definitions** - ALPR, Extract, PII, CJI
  4. **Management** - Strategic alignment, ownership, data classification
  5. **Operations** - Training, deployment, recordkeeping
  6. **Data Collection, Access, Use & Retention:**
     - 30-day tactical access window
     - 3-year maximum for investigations
     - Logging requirements
  7. **Oversight, Evaluation, Auditing & Enforcement:**
     - Annual assessments
     - Audit schedules
     - Compliance enforcement
- **Status:** These are *recommended* guidelines; compliance with Florida Statutes is mandatory
- **Use Case:** Gold standard for evaluating whether agencies have proper policies and procedures

---

### **2. Vendor Documentation**

**Flock_Safety_Policy_Pulse_Series_Complete.md** - *Vendor Compliance Blog Series*
- **Type:** Vendor Communications / Marketing Content
- **Source:** Flock Safety (ALPR system vendor)
- **Authors:** Josh Thomas
- **Publication Dates:** September 2025 - November 2025 (3-part series)
- **Purpose:** Flock Safety's public statements on compliance features and policy commitments
- **Part 1 (Sept 2025):** "Compliance Doesn't Have to Be So Hard"
  - Acknowledges 50-state compliance challenge
  - Introduces "Policy Pulse" initiative
  - Commits to supporting local autonomy while maintaining accountability
- **Part 2 (Oct 2025):** "The Work Already Underway"
  - **Keyword Filters** - Blocks searches prohibited by state law (immigration, reproductive healthcare)
  - **Federal Organization Designation** - Labels federal agency requests
  - **Limitations on Federal Access** - Restricts federal access to state data
- **Part 3 (Nov 2025):** "Transparency, Control, and the Path Forward"
  - **Customizable Public Audit Exports** - Agencies control what fields appear in transparency reports
  - **Mandatory Offense Type Selection** - Forces officers to categorize searches by NIBRS offense codes
- **Critical Note:** These are vendor *claims* about features; may not reflect actual implementation or agency usage
- **Use Case:** Compare vendor promises against actual operational data to identify gaps

---

### **3. Agency-Specific Documentation**

**ocso_flock_safety_press_release.md** - *OCSO Public Announcement*
- **Type:** Press Release / Public Communication
- **Source:** Okaloosa County Sheriff's Office (OCSO)
- **Purpose:** Official announcement of Flock Safety ALPR system deployment
- **Key Claims:**
  - System purpose (crime detection/prevention)
  - Technology description
  - Privacy protections claimed
  - Public transparency commitments
- **Use Case:** Baseline for what OCSO publicly promised citizens about the system

**ocso_flock_faq_01-12-26.md** - *OCSO Official FAQ Document*
- **Type:** Public Information / FAQ
- **Source:** Okaloosa County Sheriff's Office website
- **Date:** January 12, 2026
- **Purpose:** Answer public questions about ALPR deployment
- **Key Representations:**
  - **Data Retention:** "Deletes its data every 30 days on a rolling basis"
  - **Hot Lists:** Two types (NCIC auto-sync, local 30-day entries)
  - **Data Ownership:** Flock does not own or sell customer data
  - **Access Controls:** Flock employees require CJIS training for data access
  - **Transparency Portal:** "Evaluating use" (not currently active as of Jan 2026)
  - **No Facial Recognition:** Confirmed
  - **No Cell Phone Data:** Confirmed
- **Critical Discrepancy:** This document claims 30-day deletion, but audit data shows searches going back 524 days
- **Use Case:** Primary source for OCSO's official policy representations to the public

**ocso_master_service_agreement_EXTRACTED.md** - *OCSO-Flock Contract Terms*
- **Type:** Legal Contract (excerpts)
- **Parties:** Okaloosa County Sheriff's Office & Flock Safety
- **Purpose:** Defines contractual terms, data ownership, service level agreements
- **Expected Content:**
  - Data ownership provisions
  - Access rights
  - Retention commitments
  - Liability terms
  - Service performance standards
- **Use Case:** Legal obligations that may differ from public statements

---

### **4. Operational Data**

**11_1_2025-12_8_2025-Okaloosa_County_FL_SO-Audit_EXTRACTED.csv** - *ALPR System Usage Audit Log*
- **Type:** Database Export / Audit Log
- **Source:** Flock Safety system (OCSO public records disclosure)
  - ID (unique identifier)
  - Org_Name
  - Total_Networks_Searched (count)
  - Total_Devices_Searched (count)
  - Start_Time_Frame (lookback window begin)
  - End_Time_Frame (lookback window end)
  - Reason (officer justification)
  - Search_Time (when search executed)
  - Search_Type ("lookup" vs "search")
  - Case_Number (redacted)
  - Officer_Name (redacted)
- **Use Case:** Empirical evidence of actual system usage vs. stated policy

**Sharing_Agencies_EXTRACTED.csv** - *Inter-Agency Data Sharing Network*
- **Type:** Network Configuration / Partnership List
- **Source:** Flock Safety system (OCSO public records disclosure)
- **Purpose:** Documents which agencies share ALPR data with OCSO and vice versa
- **Data Fields:**
  - Page (this column can be ignored)
  - Organization Name (these agencies can either share networks with ocso, access ocso network, or both)
  - Networks Shared With Me (networks shared with ocso, from the organization name)
  - Networks I'm Sharing (ocso only has one network, and ocso shares with the organization name)
- **Use Case:** Map the scope of surveillance network; identify which agencies have access to OCSO data


## Document Relationships & Cross-References

### **Legal Hierarchy**
1. **Florida Statutes** (mandatory law)
   - 119.011, 119.07 → Public records framework
   - 316.0777, 316.0778 → ALPR-specific mandates
   - 501.171 → PII security requirements
2. **FDLE Guidelines** (recommended best practices, based on statutes)
3. **Agency Policy** (must comply with statutes, should align with guidelines)

### **Promise vs. Reality Chain**
1. **Vendor Claims** (Flock_Safety_Policy_Pulse_Series_Complete.md)
2. **Agency Representations** (ocso_flock_faq_01-12-26.md, press release)
3. **Contractual Obligations** (ocso_master_service_agreement_EXTRACTED.md)
4. **Operational Reality** (11_1_2025-12_8_2025-Okaloosa_County_FL_SO-Audit_EXTRACTED.csv)

### **Network Scope Documents**
- **Sharing_Agencies_EXTRACTED.csv** → Who has access to data
- **Audit Log** → How many networks/devices are queried
- **FDLE Guidelines § 6.c** → Legal requirements for information sharing

---

## Usage Guidance for Researchers/Analysts

### **When Evaluating Compliance:**
1. Start with **Florida Statutes** (316.0777, 316.0778) - these are mandatory
2. Cross-reference **FDLE Guidelines** - these show best practices
3. Compare against **OCSO FAQ** - what the agency publicly claims
4. Validate with **Audit Log** - what actually happens in practice
5. Document discrepancies in your analysis

### **When Assessing Privacy Impact:**
1. Check **FL Statute 501.171** for PII definitions
2. Review **FDLE Guidelines § 3** for definitions of Extract, PII, CJI
3. Analyze **Audit Log** for geolocation tracking patterns
4. Consider **Sharing_Agencies_EXTRACTED.csv** for data exposure scope

### **When Investigating Transparency:**
1. Read **FL Statute 119.07** for public records rights
2. Review **FDLE Guidelines § 7.c** for auditing requirements
3. Compare **Flock Policy Pulse Part 3** (transparency portal claims)
4. Examine **OCSO FAQ** (transparency portal status: "evaluating")
5. Note redactions in **Audit Log** (100% of officer names, case numbers)

### **When Documenting Retention Violations:**
1. **FL Statute 316.0778** → 30-day tactical access mandate
2. **FDLE Guidelines § 6.e** → 3-year investigation maximum
3. **OCSO FAQ** → "deletes data every 30 days"
4. **Audit Log** → Calculate actual lookback periods

---

## Document Status & Reliability

| Document | Authoritative? | Date Sensitivity | Reliability |
|----------|----------------|------------------|-------------|
| Florida Statutes | Yes (law) | Check for amendments | High |
| FDLE Guidelines | Yes (guidance) | Updated Nov 2024 | High |
| Flock Policy Pulse | No (marketing) | Sept-Nov 2025 | Medium (verify claims) |
| OCSO FAQ | Official representation | Jan 2026 | High (for stated policy) |
| OCSO Press Release | Official representation | Feb 2022 | Medium |
| Master Service Agreement | Binding contract | Sep 2023 | High (legal obligation) |
| Audit Log | Empirical data | Nov-Dec 2025 | Very High (operational fact) |
| Sharing Agencies | Configuration data | Dec 2025 | High (network map) |

---

## Research Questions This Knowledge Base Can Answer

✅ **What does Florida law require for ALPR use?**
- See: FL_Statute_316.0777.md, FL_Statute_316.0778.md

✅ **How long can ALPR data be retained?**
- Law: FL_Statute_316.0778.md (30 days tactical, 3 years investigation)
- Guidelines: FDLE_ALPR_Guidelines_2024.md § 6.e
- OCSO Claims: ocso_flock_faq_01-12-26.md ("30 days")
- OCSO Reality: 11_1_2025-12_8_2025-Okaloosa_County_FL_SO-Audit_EXTRACTED.csv (524 days max)

✅ **What constitutes "criminal justice purpose"?**
- See: FDLE_ALPR_Guidelines_2024.md § 2.b

✅ **Is ALPR geolocation data considered PII in Florida?**
- See: FL_Statute_501.171.md (defines geolocation as PII when "reasonably linkable")

✅ **What agencies share data with OCSO?**
- See: Sharing_Agencies_EXTRACTED.csv

✅ **Does Flock Safety sell customer data?**
- See: ocso_flock_faq_01-12-26.md (claims no)
- Verify with: ocso_master_service_agreement_EXTRACTED.md

✅ **What oversight mechanisms exist?**
- See: FDLE_ALPR_Guidelines_2024.md § 7 (Auditing requirements)
- Compare: ocso_flock_faq_01-12-26.md (Transparency Portal "evaluating")

---

## Version Control

| Version | Date | Changes |
|---------|------|---------|
| 1.0 | Jan 17, 2026 | Initial knowledge base documentation created |

---

**Project Contact:** [Your contact info if applicable]  
**Data Sources:** Florida Legislature, FDLE, OCSO, Flock Safety, Public Records Requests  
**Classification:** Public Information / Open Source Intelligence


