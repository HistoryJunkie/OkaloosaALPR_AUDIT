# OCSO ALPR Audit Analysis

This repository contains an analysis of Automated License Plate Recognition (ALPR) search audit data from the Okaloosa County Sheriff's Office (OCSO) in Florida. The analysis examines operational practices, data retention patterns, and system usage against stated policies and applicable Florida law.

## Background

The Okaloosa County Sheriff's Office deployed a Flock Safety ALPR system with a stated 30-day rolling data retention policy. This project analyzes audit logs from November 1, 2025 through December 8, 2025 to examine actual system usage patterns, data retention practices, and search behaviors.

## Repository Structure

```
├── Source_Data/
│   ├── 11_1_2025-12_8_2025-Okaloosa_County_FL_SO-Audit.pdf
│   └── Sharing_Agencies.pdf
├── Generated_Data/
│   └── 11_1_2025-12_8_2025-Okaloosa_County_FL_SO-Audit_EXTRACTED.csv
├── Jupyter_Notebooks/
│   └── Okaloosa_Parser_CLEAN.ipynb
├── Supporting_Documents/
│   ├── FDLE_ALPR_Guidelines_2024.md
│   ├── FL_Senate_Bill_599_2014.md
│   ├── FL_Statute_119.011.md
│   ├── FL_Statute_119.07.md
│   ├── FL_Statute_316.0777.md
│   ├── FL_Statute_316.0778.md
│   ├── FL_Statute_501.171.md
│   ├── Flock_Safety_Policy_Pulse_Series_Complete.md
│   └── ocso_flock_safety_press_release.md
├── FINDINGS.md
└── README.md
```

**Quick Links:**
- [📊 View Analysis Findings](https://github.com/HistoryJunkie/OkaloosaALPR_AUDIT/blob/main/FINDINGS.md)
- [💻 Parsing Notebook](https://github.com/HistoryJunkie/OkaloosaALPR_AUDIT/blob/main/Jupyter_Notebooks/Okaloosa_Parser_CLEAN.ipynb)
- [📁 Source Data](https://github.com/HistoryJunkie/OkaloosaALPR_AUDIT/tree/main/Source_Data)
- [📈 Parsed Audit (CSV)](https://github.com/HistoryJunkie/OkaloosaALPR_AUDIT/blob/main/Generated_Data/11_1_2025-12_8_2025-Okaloosa_County_FL_SO-Audit_EXTRACTED.csv)
- [📚 Supporting Documents](https://github.com/HistoryJunkie/OkaloosaALPR_AUDIT/tree/main/Supporting_Documents)

### Directory Descriptions

- **[Source_Data/](https://github.com/HistoryJunkie/OkaloosaALPR_AUDIT/tree/main/Source_Data)**: Original audit documents obtained through public records requests, including the raw ALPR search audit log and sharing agency information.

- **[Generated_Data/](https://github.com/HistoryJunkie/OkaloosaALPR_AUDIT/tree/main/Generated_Data)**: Processed data extracted from source documents. The CSV file contains parsed and structured audit log entries for analysis.

- **[Jupyter_Notebooks/](https://github.com/HistoryJunkie/OkaloosaALPR_AUDIT/tree/main/Jupyter_Notebooks)**: Analysis notebooks containing the data extraction, parsing, and analytical methods used to process the audit logs.

- **[Supporting_Documents/](https://github.com/HistoryJunkie/OkaloosaALPR_AUDIT/tree/main/Supporting_Documents)**: Relevant legal statutes, guidelines, policy documents, and official statements that provide context for the analysis. Includes Florida statutes on ALPR usage, public records law, and privacy protections.

- **[FINDINGS.md](https://github.com/HistoryJunkie/OkaloosaALPR_AUDIT/blob/main/FINDINGS.md)**: Comprehensive analysis of discrepancies between stated policies and operational data, including retention practices, network scale, and accountability measures.

## Data Sources

The primary data source is an audit log covering ALPR searches conducted by OCSO personnel from November 1, 2025 through December 8, 2025. The audit log was obtained through Florida's public records law and contains:

- Search timestamps and lookback periods
- Stated justifications for searches
- Network and device query scope
- Redacted officer and case identifiers

Additional context is provided by official OCSO communications, Flock Safety policy documents, and applicable Florida statutes governing ALPR use and data privacy.

## Methodology

The analysis employs a systematic approach to examine audit log data:

1. **Data Extraction**: PDF audit logs are parsed and converted to structured CSV format for analysis
2. **Temporal Analysis**: Calculation of lookback periods to identify searches exceeding stated retention limits
3. **Network Scope Analysis**: Examination of single-network versus multi-network search patterns
4. **Justification Analysis**: Categorization and evaluation of stated search reasons
5. **Compliance Assessment**: Comparison of operational practices against stated policies and legal requirements

Detailed methodology and code are available in [`Jupyter_Notebooks/Okaloosa_Parser_CLEAN.ipynb`](https://github.com/HistoryJunkie/OkaloosaALPR_AUDIT/blob/main/Jupyter_Notebooks/Okaloosa_Parser_CLEAN.ipynb).

## Key Findings

The analysis identified several areas of concern:

- **Data Retention Discrepancies**: 463 searches exceeded the stated 30-day retention limit, with the longest lookback period reaching 524 days (approximately 1.5 years)
- **Network Scale**: 46.83% of searches queried multiple networks, with some searches reaching across 6,709 networks and 100,034 devices simultaneously
- **Documentation Gaps**: 9 searches contained no stated justification in the required reason field
- **Limited Accountability**: 100% redaction of officer identifiers and case numbers prevents verification of search legitimacy

Full findings are documented in [**FINDINGS.md**](https://github.com/HistoryJunkie/OkaloosaALPR_AUDIT/blob/main/FINDINGS.md).

## Legal Framework

Florida law establishes specific requirements for ALPR system operation and data handling:

- **[FL Statute 316.0777](https://github.com/HistoryJunkie/OkaloosaALPR_AUDIT/blob/main/Supporting_Documents/FL_Statute_316.0777.md)**: Governs ALPR usage by law enforcement agencies
- **[FL Statute 316.0778](https://github.com/HistoryJunkie/OkaloosaALPR_AUDIT/blob/main/Supporting_Documents/FL_Statute_316.0778.md)**: Prohibits unauthorized ALPR data retention and sharing
- **[FL Statute 119](https://github.com/HistoryJunkie/OkaloosaALPR_AUDIT/blob/main/Supporting_Documents/FL_Statute_119.011.md)**: Public records law requirements
- **[FL Statute 501.171](https://github.com/HistoryJunkie/OkaloosaALPR_AUDIT/blob/main/Supporting_Documents/FL_Statute_501.171.md)**: Digital Bill of Rights establishing geolocation data as personally identifiable information
- **[FDLE Guidelines (2024)](https://github.com/HistoryJunkie/OkaloosaALPR_AUDIT/blob/main/Supporting_Documents/FDLE_ALPR_Guidelines_2024.md)**: State-level best practices for ALPR deployment

All referenced statutes and guidelines are available in the [`Supporting_Documents/`](https://github.com/HistoryJunkie/OkaloosaALPR_AUDIT/tree/main/Supporting_Documents) directory.

## Usage

To replicate or extend this analysis:

1. Review the source audit data in [`Source_Data/`](https://github.com/HistoryJunkie/OkaloosaALPR_AUDIT/tree/main/Source_Data)
2. Examine the data extraction and parsing methodology in [`Jupyter_Notebooks/Okaloosa_Parser_CLEAN.ipynb`](https://github.com/HistoryJunkie/OkaloosaALPR_AUDIT/blob/main/Jupyter_Notebooks/Okaloosa_Parser_CLEAN.ipynb)
3. Access the structured data in [`Generated_Data/`](https://github.com/HistoryJunkie/OkaloosaALPR_AUDIT/tree/main/Generated_Data) for further analysis
4. Reference applicable legal frameworks in [`Supporting_Documents/`](https://github.com/HistoryJunkie/OkaloosaALPR_AUDIT/tree/main/Supporting_Documents)
5. Review comprehensive findings in [`FINDINGS.md`](https://github.com/HistoryJunkie/OkaloosaALPR_AUDIT/blob/main/FINDINGS.md)

## About This Project

This project documents methods and findings from an independent analysis of publicly available ALPR audit data. The goal is to provide empirical examination of ALPR system usage patterns, assess alignment with stated policies, and contribute to informed public discourse on surveillance technology deployment and oversight.

## License

The analysis, code, and documentation in this repository are provided for transparency and public interest purposes. Source documents remain subject to their original terms and Florida public records law.
