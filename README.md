# OCSO ALPR Audit & Accountability Investigation

This repository contains an ongoing investigation into the Okaloosa County Sheriff's Office (OCSO) Automated License Plate Recognition (ALPR) system, examining operational practices, contract terms, ethical implications, and compliance with Florida law.

The source data for this analysis came from [this post on Muckrock.](https://www.muckrock.com/foi/okaloosa-county-10449/florida-public-records-act-request-flock-safety-audit-okaloosa-county-sheriffs-department-199490/)

## Quick Links

| Document | Description |
|----------|-------------|
| [Executive Summary](EXECUTIVE_SUMMARY.md) | High-level findings and investigation status |
| [Full Findings](2_Analysis/retention_analysis/FINDINGS.md) | Detailed retention and network analysis |
| [Contract Issues](2_Analysis/contract_analysis/contract_issues_template.md) | MSA analysis framework |
| [Constitutional Concerns](4_Ethical_Issues/constitutional_concerns.md) | Fourth Amendment analysis |
| [Records Request Templates](5_Methodology/records_request_templates/) | Templates for additional requests |

## Key Findings

| Finding | Evidence |
|---------|----------|
| **Retention Policy Violated** | 463 searches exceeded 30-day limit (max: 524 days) |
| **Nationwide Surveillance** | 46.8% of searches queried multiple networks (up to 6,709) |
| **Accountability Blocked** | 100% of officer names and case numbers redacted |
| **Weak Contract Terms** | Liability capped at 12 months fees; no breach notification |

## Repository Structure

```
OkaloosaALPR_AUDIT/
├── README.md                              # This file
├── EXECUTIVE_SUMMARY.md                   # High-level findings
├── Project_Knowledge.md                   # Detailed knowledge base
│
├── 1_Source_Data/                         # Original public records
│   ├── audit_logs/                        # ALPR search audit PDFs
│   ├── contracts/                         # MSA and related documents
│   └── correspondence/                    # OCSO communications
│
├── 2_Analysis/                            # Investigation findings
│   ├── retention_analysis/                # 30-day policy violations
│   ├── contract_analysis/                 # MSA deep dive
│   ├── network_scale_analysis/            # Multi-network surveillance
│   └── justification_analysis/            # Search reason analysis
│
├── 3_Legal_Framework/                     # Applicable law
│   ├── florida_statutes/                  # FL state law
│   ├── federal_cases/                     # Constitutional precedent
│   └── guidelines/                        # FDLE and other guidance
│
├── 4_Ethical_Issues/                      # Civil liberties analysis
│   ├── constitutional_concerns.md         # 4th Amendment issues
│   ├── disparate_impact.md               # Discrimination analysis
│   ├── vendor_accountability.md          # Flock Safety practices
│   └── mission_creep.md                  # Scope expansion tracking
│
├── 5_Methodology/                         # Research methods
│   ├── notebooks/                         # Jupyter analysis code
│   ├── data_dictionary.md                # Field definitions
│   └── records_request_templates/         # FOIA templates
│
├── 6_Output/                              # Generated materials
│   ├── reports/                           # HTML/PDF reports
│   ├── visualizations/                    # Charts and maps
│   └── press_materials/                   # Media resources
│
└── 7_Research/                            # Background research
    ├── other_jurisdictions/               # Comparative analysis
    ├── litigation/                        # Relevant court cases
    └── vendor_background/                 # Flock Safety profile
```

## Investigation Areas

### Completed
- [x] Audit log extraction (7,273 records parsed)
- [x] Retention violation analysis (463 violations identified)
- [x] Network scale documentation (6,709 network searches)
- [x] Contract extraction and initial review

### In Progress
- [ ] Contract issues deep dive (liability, data rights, etc.)
- [ ] Constitutional analysis (Carpenter, mosaic theory)
- [ ] Vendor accountability research

### Planned
- [ ] Camera location analysis (pending records request)
- [ ] Disparate impact mapping
- [ ] Comparative jurisdiction research
- [ ] Additional public records requests

## Data Sources

### Primary
- **Audit Log**: 809-page PDF covering Nov 1 - Dec 8, 2025 (7,273 searches)
- **Master Service Agreement**: Flock Safety contract dated September 2023
- **Sharing Agencies List**: Inter-agency data sharing documentation

### Supporting
- Florida Statutes (316.0777, 316.0778, 119.07, 501.171)
- FDLE ALPR Guidelines (2024)
- OCSO public statements and FAQ

## Legal Framework

| Statute | Subject | Key Provision |
|---------|---------|---------------|
| FL 316.0777 | ALPR Authorization | Criminal justice purpose requirement |
| FL 316.0778 | Data Retention | 30-day tactical / 3-year investigation limit |
| FL 501.171 | Privacy | Geolocation as PII |
| FL 119.07 | Public Records | Disclosure requirements |

## How to Contribute

### File Public Records Requests
Templates are available in `5_Methodology/records_request_templates/` for:
- Contract documents and exhibits
- Camera locations
- Policies and training materials
- Data sharing agreements
- Security incident records

### Research
- Document ALPR practices in other jurisdictions
- Track relevant litigation
- Research Flock Safety corporate background

### Analysis
- Extend audit log analysis
- Map camera locations against demographics
- Calculate cost-per-search metrics

## Replication

To replicate or extend this analysis:

1. Review source documents in `1_Source_Data/`
2. Examine parsing methodology in `5_Methodology/notebooks/`
3. Reference data dictionary in `5_Methodology/data_dictionary.md`
4. Use records request templates for additional data
5. Follow analysis frameworks in `2_Analysis/` and `4_Ethical_Issues/`

## About

This project documents an independent investigation of publicly available ALPR data. The goal is to provide empirical examination of surveillance technology deployment, assess alignment with stated policies and legal requirements, and contribute to informed public discourse on law enforcement surveillance practices.

## License

Analysis, code, and documentation are provided for transparency and public interest purposes. Source documents remain subject to their original terms and Florida public records law.
