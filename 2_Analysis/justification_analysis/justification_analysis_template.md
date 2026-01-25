# Search Justification Analysis

## Overview

This document analyzes the stated justifications ("Reason" field) in OCSO ALPR searches to assess compliance with Florida's criminal justice purpose requirement.

**Data Source:** `2_Analysis/retention_analysis/11_1_2025-12_8_2025-Okaloosa_County_FL_SO-Audit_EXTRACTED.csv`
**Total Records:** 7,273 searches
**Audit Period:** November 1 - December 8, 2025

---

## 1. Justification Categories

### Categorization Framework

| Category | Description | Legitimate? |
|----------|-------------|-------------|
| **Investigation** | Active criminal investigation | Yes |
| **BOLO** | Be On the Lookout alert | Yes |
| **Stolen Vehicle** | Vehicle theft investigation | Yes |
| **Missing Person** | Missing/endangered person search | Yes |
| **Warrant** | Outstanding warrant service | Yes |
| **Traffic Enforcement** | DWLSR, traffic violations | Questionable |
| **Patrol** | General patrol activity | Questionable |
| **Vague** | LEO, deputy request, etc. | Insufficient |
| **Blank** | No justification provided | Violation |
| **Test** | System testing | Administrative |

---

## 2. Distribution Analysis

### Raw Counts

| Justification | Count | Percentage |
|---------------|-------|------------|
| [Category 1] | [N] | [%] |
| [Category 2] | [N] | [%] |
| (Blank) | 9 | [%] |
| **Total** | 7,273 | 100% |

### By Legitimacy

| Classification | Count | Percentage |
|----------------|-------|------------|
| Clearly Legitimate | [N] | [%] |
| Questionable | [N] | [%] |
| Insufficient | [N] | [%] |
| Violation (Blank) | 9 | [%] |

---

## 3. Blank Justification Analysis

### The 9 Searches Without Reason

| Search ID | Date/Time | Networks | Devices | Search Type |
|-----------|-----------|----------|---------|-------------|
| [UUID] | [DateTime] | [N] | [N] | [Type] |

### Concerns

1. Florida law requires "criminal justice purpose" for ALPR use
2. No stated reason = no verifiable purpose
3. These searches should have been blocked by system controls

### Questions

- [ ] Were these searches for legitimate purposes despite blank field?
- [ ] Is there a technical issue allowing blank submissions?
- [ ] What oversight exists to catch blank-reason searches?

---

## 4. Questionable Justification Analysis

### "Patrol" Searches

**Count:** [N] searches
**Concern:** General patrol is not a specific criminal justice purpose

| Metric | Value |
|--------|-------|
| Total "Patrol" searches | [N] |
| With >30 day lookback | [N] |
| Multi-network "Patrol" | [N] |
| Avg devices queried | [N] |

**Analysis:**
[Assessment of whether "Patrol" justification is appropriate for ALPR use]

---

### "DWLSR" Searches (Driving While License Suspended)

**Count:** [N] searches
**Concern:** Traffic enforcement may not qualify as criminal justice purpose

| Metric | Value |
|--------|-------|
| Total DWLSR searches | [N] |
| Historical lookback used | [N] |
| Multi-network queries | [N] |

**Analysis:**
[Assessment of DWLSR as ALPR justification]

---

### Vague Justifications ("LEO", "Deputy Request", etc.)

**Count:** [N] searches
**Concern:** These provide no specific purpose

| Justification | Count | Assessment |
|---------------|-------|------------|
| "LEO" | [N] | No specific purpose |
| "Deputy Request" | [N] | No specific purpose |
| "Test" | [N] | Non-operational |
| [Other] | [N] | [Assessment] |

---

## 5. Cross-Tabulation Analysis

### Justification vs. Lookback Period

| Justification | <30 Days | 30-90 Days | 90-180 Days | >180 Days |
|---------------|----------|------------|-------------|-----------|
| Investigation | [N] | [N] | [N] | [N] |
| BOLO | [N] | [N] | [N] | [N] |
| Patrol | [N] | [N] | [N] | [N] |
| (Blank) | [N] | [N] | [N] | [N] |

### Justification vs. Network Scope

| Justification | Single Network | Multi-Network | Avg Networks |
|---------------|----------------|---------------|--------------|
| Investigation | [N] | [N] | [N] |
| BOLO | [N] | [N] | [N] |
| Patrol | [N] | [N] | [N] |
| (Blank) | [N] | [N] | [N] |

---

## 6. Legal Compliance Assessment

### Florida Statute 316.0777 Requirements

> [Quote relevant statutory language on permitted purposes]

### Compliance Matrix

| Justification Category | Statutory Basis | Compliant? |
|-----------------------|-----------------|------------|
| Investigation | [Cite] | Yes |
| BOLO | [Cite] | Yes |
| Stolen Vehicle | [Cite] | Yes |
| Missing Person | [Cite] | Yes |
| Patrol | [Cite?] | Questionable |
| DWLSR | [Cite?] | Questionable |
| Blank | None | No |

### FDLE Guidelines Alignment

> [Quote FDLE guidance on acceptable purposes]

---

## 7. Recommendations

### Technical Controls

1. **Require Justification Field** - Block searches with blank reason
2. **Standardize Categories** - Drop-down menu of approved purposes
3. **Case Number Linking** - Require case/incident number for certain searches

### Policy Changes

1. **Define Permitted Uses** - Enumerate specific authorized purposes
2. **Prohibit Vague Reasons** - "Patrol" and "LEO" should not be sufficient
3. **Supervisor Review** - Flag unusual justifications for review

### Oversight

1. **Regular Audits** - Review justification patterns monthly
2. **Anomaly Detection** - Flag searches with unusual reasons
3. **Public Reporting** - Disclose justification distribution

---

## 8. Research Tasks

- [ ] Complete categorization of all 7,273 justifications
- [ ] Calculate cross-tabulation statistics
- [ ] Research statutory basis for each category
- [ ] Compare to FDLE guidelines
- [ ] Identify patterns in blank/vague searches
- [ ] Develop recommendations

---

## Sources

1. Audit Data: `2_Analysis/retention_analysis/*.csv`
2. FL Statute 316.0777
3. FDLE ALPR Guidelines 2024
4. OCSO ALPR Policy (if obtained)
