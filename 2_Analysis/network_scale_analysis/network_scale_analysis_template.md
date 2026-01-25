# Network Scale Analysis

## Overview

This document analyzes the scope of ALPR network access in OCSO searches, examining single-network vs. multi-network queries and the implications of nationwide surveillance capability.

**Data Source:** `2_Analysis/retention_analysis/11_1_2025-12_8_2025-Okaloosa_County_FL_SO-Audit_EXTRACTED.csv`
**Total Records:** 7,273 searches
**Audit Period:** November 1 - December 8, 2025

---

## 1. Network Access Summary

### Key Metrics

| Metric | Value |
|--------|-------|
| Total Searches | 7,273 |
| Single-Network Searches | 3,867 (53.17%) |
| Multi-Network Searches | 3,406 (46.83%) |
| Maximum Networks (Single Search) | 6,709 |
| Maximum Devices (Single Search) | 100,034 |
| Average Networks (Multi-Network) | ~1,800 |

---

## 2. Distribution Analysis

### Network Count Distribution

| Networks Queried | Search Count | Percentage | Cumulative % |
|------------------|--------------|------------|--------------|
| 1 (Local only) | 3,867 | 53.17% | 53.17% |
| 2-100 | [N] | [%] | [%] |
| 101-1,000 | [N] | [%] | [%] |
| 1,001-5,000 | [N] | [%] | [%] |
| 5,001+ | [N] | [%] | [%] |

### Device Count Distribution

| Devices Queried | Search Count | Percentage |
|-----------------|--------------|------------|
| <1,000 | [N] | [%] |
| 1,000-10,000 | [N] | [%] |
| 10,001-50,000 | [N] | [%] |
| 50,001-100,000 | [N] | [%] |
| >100,000 | [N] | [%] |

---

## 3. Single vs. Multi-Network Comparison

### Characteristics

| Attribute | Single-Network | Multi-Network |
|-----------|----------------|---------------|
| Count | 3,867 | 3,406 |
| Percentage | 53.17% | 46.83% |
| Avg Devices | [Calculate] | [Calculate] |
| Avg Lookback (days) | [Calculate] | [Calculate] |
| Blank Justification | [N] | [N] |

### Search Type Distribution

| Search Type | Single-Network | Multi-Network |
|-------------|----------------|---------------|
| Lookup | [N] | [N] |
| Search | [N] | [N] |
| [Other] | [N] | [N] |

---

## 4. Extreme Cases Analysis

### Largest Network Searches (Top 10)

| Rank | Search ID | Networks | Devices | Reason | Date |
|------|-----------|----------|---------|--------|------|
| 1 | [UUID] | 6,709 | [N] | [Reason] | [Date] |
| 2 | [UUID] | [N] | [N] | [Reason] | [Date] |
| ... | ... | ... | ... | ... | ... |

### Largest Device Searches (Top 10)

| Rank | Search ID | Networks | Devices | Reason | Date |
|------|-----------|----------|---------|--------|------|
| 1 | [UUID] | [N] | 100,034 | [Reason] | [Date] |
| 2 | [UUID] | [N] | [N] | [Reason] | [Date] |
| ... | ... | ... | ... | ... | ... |

### Analysis Questions

- What justified searching 6,709 networks simultaneously?
- What operational need requires querying 100,034 devices?
- Are these searches proportionate to stated purposes?

---

## 5. Sharing Agencies Analysis

**Source:** `2_Analysis/network_scale_analysis/Sharing_Agencies_EXTRACTED.csv`

### Agency Categories

| Category | Count | Percentage |
|----------|-------|------------|
| Sheriff's Offices | [N] | [%] |
| Police Departments | [N] | [%] |
| State Agencies | [N] | [%] |
| Federal Agencies | [N] | [%] |
| Other | [N] | [%] |

### Geographic Distribution

| State | Agencies | Notes |
|-------|----------|-------|
| Florida | [N] | In-state |
| [State] | [N] | [Notes] |
| [State] | [N] | [Notes] |

### Notable Agencies

| Agency | Type | Concern |
|--------|------|---------|
| [Agency] | [Type] | [Concern] |

---

## 6. Authorization Analysis

### Questions About Network Access

1. **Who authorized access to 6,709 networks?**
   - Individual MOU with each agency?
   - Blanket Flock network agreement?
   - Automatic opt-in?

2. **What governs cross-jurisdictional searches?**
   - Are there restrictions?
   - Is supervisor approval required?
   - Can any deputy search nationwide?

3. **Did citizens consent to nationwide tracking?**
   - Were they informed of network scope?
   - Do local policies apply to multi-state data?

### Data Sharing Governance

| Governance Element | Status | Source |
|-------------------|--------|--------|
| Written data sharing policy | [Yes/No/Unknown] | [Source] |
| Inter-agency agreements | [Yes/No/Unknown] | [Source] |
| Restrictions on external access | [Yes/No/Unknown] | [Source] |
| Audit of cross-agency searches | [Yes/No/Unknown] | [Source] |

---

## 7. Privacy Implications

### Scale of Surveillance Capability

| Capability | Implication |
|------------|-------------|
| 6,709 networks | Potential access to thousands of jurisdictions |
| 100,034 devices | Geographic coverage spanning states/nation |
| 46.83% multi-network | Nearly half of searches go beyond local |
| No apparent restrictions | Any search can be nationwide |

### Mosaic Effect

With multi-network access, OCSO can:
- Track vehicle movements across state lines
- Reconstruct travel patterns over time
- Access data from jurisdictions with different retention policies
- Build comprehensive movement histories

### Constitutional Questions

- Does nationwide scope change constitutional analysis?
- Is there a reasonable expectation of privacy against multi-state tracking?
- Does network scale require warrant?

---

## 8. Comparison to OCSO Public Statements

### Public Claim

> [Quote OCSO statement about system scope]

### Reality

| Claimed | Actual |
|---------|--------|
| [Claim] | [Evidence] |

---

## 9. Recommendations

### Technical Controls

1. **Network Scope Limits** - Cap maximum networks without supervisor approval
2. **Geographic Restrictions** - Require justification for out-of-state queries
3. **Device Thresholds** - Alert on searches exceeding device count thresholds

### Policy Changes

1. **Define Multi-Network Criteria** - When is expanded search justified?
2. **Approval Process** - Supervisor sign-off for large-scale searches
3. **Documentation** - Require explanation for network scope selection

### Transparency

1. **Public Disclosure** - Report multi-network search statistics
2. **Network List** - Disclose which agencies are accessible
3. **Sharing Agreements** - Make inter-agency agreements public

---

## 10. Research Tasks

- [ ] Calculate complete distribution statistics
- [ ] Identify top network/device searches
- [ ] Analyze sharing agencies list fully
- [ ] Research authorization/governance structure
- [ ] Compare to other jurisdictions' network access
- [ ] Document constitutional implications

---

## Sources

1. Audit Data: `2_Analysis/retention_analysis/*.csv`
2. Sharing Agencies: `2_Analysis/network_scale_analysis/Sharing_Agencies_EXTRACTED.csv`
3. MSA Network Provisions
4. OCSO Public Communications
5. Florida Law on Inter-Agency Sharing
