# Disparate Impact Analysis

## Overview

This document analyzes whether the OCSO Flock Safety ALPR deployment has disparate impacts on protected communities based on camera placement, search patterns, or alert list composition.

---

## 1. Camera Placement Analysis

### Hypothesis
If ALPR cameras are disproportionately placed in minority or low-income neighborhoods, the system may function as discriminatory surveillance infrastructure regardless of individual officer intent.

### Data Required

| Data Point | Source | Status |
|------------|--------|--------|
| Camera GPS coordinates | Public Records Request | NOT OBTAINED |
| Number of cameras per area | Public Records Request | NOT OBTAINED |
| Camera installation dates | Public Records Request | NOT OBTAINED |

### Demographic Data Sources

- U.S. Census Bureau (census.gov)
- American Community Survey
- Florida demographic data
- Okaloosa County GIS data

### Planned Analysis

1. **Geographic Distribution**
   - [ ] Map all camera locations
   - [ ] Calculate cameras per square mile by census tract
   - [ ] Identify clustering patterns

2. **Demographic Overlay**
   - [ ] Overlay racial/ethnic composition data
   - [ ] Overlay median household income data
   - [ ] Overlay housing density data

3. **Statistical Testing**
   - [ ] Correlation analysis: cameras vs. demographics
   - [ ] Chi-square test for placement independence
   - [ ] Regression analysis controlling for crime rates

### Comparison Framework

| Area Type | Expected Cameras (Neutral) | Actual Cameras | Disparity |
|-----------|---------------------------|----------------|-----------|
| High income, majority white | [Calculate] | [Measure] | [Ratio] |
| Low income, majority white | [Calculate] | [Measure] | [Ratio] |
| High income, majority minority | [Calculate] | [Measure] | [Ratio] |
| Low income, majority minority | [Calculate] | [Measure] | [Ratio] |

---

## 2. Search Pattern Analysis

### Available Data

From audit logs, we can analyze:
- Search frequency by time
- Search justifications
- Network scope of searches

### Limitations

- **Redacted:** Officer identities (cannot identify individual patterns)
- **Redacted:** Case numbers (cannot verify legitimate basis)
- **Missing:** Geographic scope of individual searches
- **Missing:** Target demographic information

### Possible Analyses

1. **Justification Distribution**
   - [ ] Categorize all stated reasons
   - [ ] Identify low-level justifications (traffic stops, patrol)
   - [ ] Compare to crime statistics for proportionality

2. **Temporal Patterns**
   - [ ] Day/time distribution of searches
   - [ ] Correlation with shift patterns
   - [ ] Weekend vs. weekday analysis

---

## 3. Alert List Composition

### Hot List Categories (from MSA)

- Stolen vehicles
- Stolen plates
- Wanted persons
- Missing persons
- AMBER Alerts
- Suspected criminal/terrorist activity
- Manually entered plates

### Concerns

- [ ] Who decides which plates are added manually?
- [ ] What oversight exists for list additions?
- [ ] Are certain communities over-represented?
- [ ] How long do plates remain on lists?

### Data Required

| Data Point | Source | Status |
|------------|--------|--------|
| Hot list composition | Public Records Request | NOT OBTAINED |
| Manual addition criteria | Policy documents | NOT OBTAINED |
| List retention policies | Policy documents | NOT OBTAINED |

---

## 4. Legal Framework

### Title VI of Civil Rights Act (1964)
- Prohibits discrimination by programs receiving federal funds
- Does OCSO receive federal grants?
- Disparate impact liability

### Florida Civil Rights Act
- State-level protections
- Enforcement mechanisms

### 14th Amendment Equal Protection
- Intentional discrimination standard
- Village of Arlington Heights factors

---

## 5. Comparative Research

### Jurisdictions with ALPR Disparate Impact Findings

| Jurisdiction | Year | Finding | Source |
|--------------|------|---------|--------|
| [City/County] | [Year] | [Summary] | [Link] |

### Academic Studies on ALPR Bias

| Study | Authors | Year | Key Findings |
|-------|---------|------|--------------|
| [Title] | [Authors] | [Year] | [Summary] |

### Advocacy Organization Reports

- ACLU reports on ALPR
- EFF surveillance analysis
- Brennan Center studies
- Local civil rights organizations

---

## 6. Interview/FOIA Strategy

### Questions for OCSO

1. What criteria determine camera placement locations?
2. Who approves new camera installations?
3. Is demographic impact considered in placement decisions?
4. What oversight exists for manual hot list additions?
5. Are there prohibited categories for ALPR searches?

### Records Requests

```
1. Camera installation locations (GPS coordinates)
2. Camera installation approval documents
3. Hot list composition by category
4. Manual hot list addition logs
5. Any demographic analysis of camera coverage
6. Complaints alleging discriminatory ALPR use
7. Training on non-discriminatory ALPR use
```

---

## 7. Findings Template

### Camera Placement Findings

**Finding:** [Statement]

**Evidence:**
- [Data point 1]
- [Data point 2]

**Statistical Significance:** [p-value, confidence interval]

**Comparison to Neutral Baseline:** [Ratio/percentage]

---

### Search Pattern Findings

**Finding:** [Statement]

**Evidence:**
- [Data point 1]
- [Data point 2]

**Limitations:** [What we cannot determine from available data]

---

## 8. Action Items

- [ ] File public records request for camera locations
- [ ] Obtain Okaloosa County demographic data
- [ ] Build GIS analysis framework
- [ ] Research comparable disparate impact studies
- [ ] Identify statistical methodology
- [ ] Consult with civil rights organizations

---

## Sources

1. [Census data links]
2. [Florida demographic sources]
3. [Academic studies]
4. [Legal precedents]
