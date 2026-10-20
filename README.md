---
license: other
language:
  - en
pretty_name: Global Clinical, Pharmaceutical & Regulatory Open Metadata Index (2024–2026)
size_categories:
  - 1K<n<10K
task_categories:
  - text-classification
  - question-answering
  - feature-extraction
tags:
  - medical
  - clinical
  - pharmaceutical
  - fda
  - ema
  - mhra
  - who
  - regulatory
configs:
  - config_name: default
    data_files:
      - split: train
        path: clinical_index_2026.jsonl
---

# Global Clinical, Pharmaceutical & Regulatory Open Metadata Index (2024–2026)

**Primary Institutional Terminal:** [Clinical Index (https://www.clinicalindex.org)](https://www.clinicalindex.org)  
**Last Automated Sync:** `2026-10-20 16:47 UTC`  
**Total Indexed Clinical & Regulatory Dossiers in Catalog:** `936`

---

## Overview

This repository provides an automated, machine-readable metadata index (`CSV` and `JSONL`) of official drug approval evaluations, clinical guidelines, medical device assessments, pharmacovigilance determinations, and public health directives indexed by **[Clinical Index](https://www.clinicalindex.org)**.

Full analytical briefings, structured clinical compliance matrices, and unabridged source PDF dossiers are available directly via each record's `canonical_url` on [clinicalindex.org](https://www.clinicalindex.org).

## Covered Jurisdictions & Health Authorities

1. **[United States](https://www.clinicalindex.org/?gdi_country=United+States)** — FDA (`NDA`, `BLA`, `ANDA` Clinical Reviews & Labels), NIH, CDC, CMS & HHS Regulatory Notices (*17 U.S.C. § 105 Public Domain*)
2. **[United Kingdom](https://www.clinicalindex.org/?gdi_country=United+Kingdom)** — Medicines and Healthcare products Regulatory Agency (`MHRA`), UKHSA, DHSC & NHS England (*Open Government Licence v3.0*)
3. **[Canada](https://www.clinicalindex.org/?gdi_country=Canada)** — Health Canada & Public Health Agency of Canada (`PHAC`) (*Reproduction of Federal Law Order SI/97-5 & Open Government Licence – Canada*)
4. **[European Union](https://www.clinicalindex.org/?gdi_country=European+Union)** — European Medicines Agency (`EMA`), ECDC, EFSA & European Commission DG SANTE (`CELEX`) (*Commission Decision 2011/833/EU*)
5. **[Commonwealth of Australia](https://www.clinicalindex.org/?gdi_country=Australia)** — Therapeutic Goods Administration (`TGA`), FSANZ, OGTR & Department of Health and Aged Care (*Creative Commons Attribution 4.0 International / CC BY 4.0*)
6. **[United Nations](https://www.clinicalindex.org/?gdi_country=United+Nations)** — World Health Organization (`WHO IRIS`) Clinical Guidelines & Technical Reports (*UN Administrative Instruction ST/AI/189/Add.9/Rev.2*)

## Dataset Files & Schema

* `clinical_index_2026.csv` — UTF-8 comma-separated index of all published clinical and regulatory dossiers.
* `clinical_index_2026.jsonl` — Newline-delimited JSON records for programmatic ingestion and biomedical LLM/RAG citation pipelines.

| Field | Type | Description |
| :--- | :--- | :--- |
| `document_id` | `string` | Official clinical or regulatory identifier (e.g., `FDA-NDA218490-ORIG-1-Review`, `MHRA-2026-...`, `CELEX-52026PC...`, `TGA-F2026L...`, `WHO-IRIS-...`) |
| `jurisdiction` | `string` | Issuing sovereign jurisdiction or multilateral organization |
| `authority` | `string` | Issuing health agency, regulatory body, or scientific committee |
| `publication_date` | `string` | Official publication or authorization date (`YYYY-MM-DD`) |
| `page_count` | `integer` | Verified pagination of the unabridged source PDF dossier |
| `language` | `string` | Primary document language (`English`) |
| `title` | `string` | Official clinical, pharmaceutical, or regulatory dossier title |
| `canonical_url` | `string` | Direct permalink to the executive briefing and PDF dossier on [clinicalindex.org](https://www.clinicalindex.org) |

---

*Maintained autonomously by [Clinical Index](https://www.clinicalindex.org).*
