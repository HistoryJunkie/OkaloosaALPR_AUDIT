# Data Dictionary

This document defines all data fields, sources, and transformations used in the investigation.

---

## Audit Log Data Fields

**Source:** `1_Source_Data/audit_logs/11_1_2025-12_8_2025-Okaloosa_County_FL_SO-Audit.pdf`
**Extracted To:** `2_Analysis/retention_analysis/11_1_2025-12_8_2025-Okaloosa_County_FL_SO-Audit_EXTRACTED.csv`

| Field | Type | Description | Notes |
|-------|------|-------------|-------|
| `ID` | UUID | Unique identifier for each search | Extracted via regex pattern |
| `Org_Name` | String | Organization conducting search | Always "Okaloosa County FL SO" in this dataset |
| `Total_Networks_Searched` | Integer | Number of ALPR networks queried | 1 = local only; >1 = multi-network |
| `Total_Devices_Searched` | Integer | Number of cameras/devices queried | Indicates search scope |
| `Time_Frame_Start` | DateTime | Beginning of search window | Used to calculate lookback period |
| `Time_Frame_End` | DateTime | End of search window | Usually same as Search_Time |
| `Reason` | String | Stated justification for search | May be blank (violation) |
| `Search_Time` | DateTime | When search was executed | Timestamp of query |
| `Search_Type` | String | Type of search | "lookup" or "search" |
| `Moderation` | String | Moderation status | Observed: "none" |

### Derived Fields

| Field | Calculation | Purpose |
|-------|-------------|---------|
| `Lookback_Days` | `Search_Time - Time_Frame_Start` | Identify retention violations (>30 days) |
| `Is_Multi_Network` | `Total_Networks_Searched > 1` | Categorize local vs. expanded searches |
| `Has_Justification` | `Reason != "" AND Reason != NULL` | Identify blank reason violations |

---

## Sharing Agencies Data Fields

**Source:** `1_Source_Data/contracts/Sharing_Agencies.pdf`
**Extracted To:** `2_Analysis/network_scale_analysis/Sharing_Agencies_EXTRACTED.csv`

| Field | Type | Description |
|-------|------|-------------|
| `Agency_Name` | String | Name of sharing agency |
| `State` | String | State/jurisdiction |
| `Agency_Type` | String | Type (Sheriff, PD, State, Federal, etc.) |
| `Sharing_Status` | String | Active/Inactive sharing relationship |

---

## Contract Data Fields

**Source:** `1_Source_Data/contracts/ocso_flock_msa.PDF`
**Extracted To:** `2_Analysis/contract_analysis/ocso_master_service_agreement_EXTRACTED.md`

Key contract elements tracked:

| Element | Location | Significance |
|---------|----------|--------------|
| Effective Date | Header | September 22, 2023 |
| Retention Period | Recitals, Order Form | 30-day rolling deletion |
| Liability Cap | Section 9.1 | 12 months of fees |
| Auto-Renewal | Section 7.1 | 30-day notice required |
| Data Rights | Section 4.1-4.3 | Customer owns, Flock licenses |
| Anonymization Rights | Section 4.3 | Perpetual license for ML training |

---

## Data Quality Notes

### Known Issues
- **UUID Concatenation:** Original PDF contained concatenated UUIDs requiring 808 splits
- **Month Suffix Duplication:** Some dates had duplicated month suffixes requiring correction
- **Redactions:** Officer names and case numbers 100% redacted

### Validation Rules Applied
1. UUID format validation (8-4-4-4-12 pattern)
2. DateTime parsing with timezone handling
3. Integer validation for network/device counts
4. Duplicate record detection

---

## Future Data Sources (Planned)

| Source | Status | Purpose |
|--------|--------|---------|
| Order Form (Exhibit A) | To Request | Pricing, device counts |
| Camera Locations | To Request | Geographic/demographic analysis |
| Unredacted Audit Logs | To Appeal | Officer accountability |
| Breach Notifications | To Request | Security incident history |
| Training Materials | To Request | Policy compliance analysis |
