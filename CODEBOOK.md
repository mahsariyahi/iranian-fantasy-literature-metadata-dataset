# Codebook

## Overview

This document describes the structure, variables, identifiers, and coding conventions used in the **Iranian Fantasy Literature Metadata Dataset (IFMD)**.

The IFMD is a bilingual bibliographic metadata dataset documenting fantasy literature published in Iran between 1270 and 1399 Solar Hijri (1891–2021 CE), including translations of foreign works into Persian and original works by Iranian authors.

This codebook should be read together with the project `README` and methodology documentation.

---

## Version Information

- **Dataset:** Iranian Fantasy Literature Metadata Dataset (IFMD)
- **Version:** 1.0
- **Release date:** 2026-07-08
- **File format:** CSV
- **Character encoding:** UTF-8
- **License:** CC BY 4.0
- **DOI:** 10.5281/zenodo.21267145

---

---

# Dataset Files

The repository contains six CSV datasets:

## ifmd_master.csv
Master bilingual bibliographic metadata dataset containing records for all fantasy literature published in Iran (1270–1399 Solar Hijri / 1891–2021 CE).

---

## Relational Organization
The IFMD is organized as a relational bibliographic metadata dataset. Relationships between works, authors, and translators are established through persistent identifiers (work_id, author_id, and translator_id) that link records across the repository. Additional details regarding the dataset architecture are provided in architecture.md.

---

## translated_works.csv
Metadata for translated fantasy works only.

---

## original_works_by_iranian_authors.csv
Metadata for original fantasy works by Iranian authors.

---

## iranian_authors.csv
Authority table containing standardized identifier records and canonical name forms for Iranian authors.

---

## foreign_authors.csv
Authority table containing standardized identifier records and canonical name forms for foreign authors.

---

## iranian_translators.csv
Authority table containing standardized identifier records and canonical name forms for Iranian translators.

---

# Variables

## id

**Description**
Unique identifier assigned to each record.

**Type**
Identifier

**Used in**
- All dataset files

**Allowed values**
```
IFMD_####
TRW_####
OPW_####
IA_####
FA_####
TR_####
```

---

## work_type

**Description**
Indicates whether a record represents an original work by an Iranian author or a translation of a foreign work into Persian.

**Type**
Categorical

**Used in**
- ifmd_master.csv

**Allowed values**
```
original
translation
```

---

## work_id

**Description**
Links each record in the master dataset to its corresponding record in either the translated works dataset or the original works by an Iranian author dataset.

**Type**
Identifier

**Used in**
- ifmd_master.csv

**Allowed values**
```
TRW_####
OPW_####
```

---

## title_original

**Description**
Original title in the source language.

**Type**
Text

**Used in**
- ifmd_master.csv
- translated_works.csv
- original_works_by_iranian_authors.csv

---

## title_fa

**Description**
Persian title as published in Iran.

**Type**
Text

**Used in**
- ifmd_master.csv
- translated_works.csv

---

## title_romanized

**Description**
Romanized form of the Persian title.

**Type**
Text

**Used in**
- ifmd_master.csv
- translated_works.csv
- original_works_by_iranian_authors.csv

---

## title_gloss_en

**Description**
English title provided to improve accessibility for non-Persian-speaking users. Where available, official published English titles are recorded; otherwise, AI-assisted literal English glosses are provided.

**Type**
Text

**Used in**
- ifmd_master.csv
- translated_works.csv
- original_works_by_iranian_authors.csv

---

## title_gloss_type

**Description**
Indicates whether the English title is an official published translation or an AI-assisted literal English gloss.

**Type**
Categorical

**Used in**
- ifmd_master.csv
- translated_works.csv
- original_works_by_iranian_authors.csv

**Allowed values**
```
official_translation
ai_literal_gloss
```

---

## author_id

**Description**
Unique identifier linking the work to the appropriate Iranian or foreign author authority table.

**Type**
Identifier

**Used in**
- ifmd_master.csv
- translated_works.csv
- original_works_by_iranian_authors.csv

**Allowed values**
```
IA_####
FA_####
```

---

## author_en

**Description**
Canonical English representation of the author's name corresponding to author_id.

**Type**
Text

**Used in**
- ifmd_master.csv
- translated_works.csv
- original_works_by_iranian_authors.csv

---

## author_fa

**Description**
Canonical Persian representation of the author's name corresponding to author_id.

**Type**
Text

**Used in**
- ifmd_master.csv
- translated_works.csv
- original_works_by_iranian_authors.csv

---

## translator_id

**Description**
Unique identifier linking the work to the Iranian translator authority table.

Not applicable to original works by Iranian authors.

**Type**
Identifier

**Used in**
- ifmd_master.csv
- translated_works.csv

**Allowed values**
```
TR_####
NA
```

---

## translator_en

**Description**
Canonical English representation of the translator's name corresponding to translator_id.

**Type**
Text

**Used in**
- ifmd_master.csv
- translated_works.csv

---

## translator_fa

**Description**
Canonical Persian representation of the translator's name corresponding to translator_id.

**Type**
Text

**Used in**
- ifmd_master.csv
- translated_works.csv

---

## year_original

**Description**
Original publication year of the source work (Gregorian calendar).

**Type**
Integer

**Used in**
- ifmd_master.csv
- translated_works.csv

**Allowed values**
```
Four-digit Gregorian year
NA
```

---

## year_persian

**Description**
Publication year in Iran (Solar Hijri calendar).

**Type**
Integer

**Used in**
- ifmd_master.csv
- translated_works.csv
- original_works_by_iranian_authors.csv

**Allowed values**
```
Four-digit Solar Hijri year
```

---

## reprint_status

**Description**
Indicates whether one or more reprints were identified.

**Type**
Categorical

**Used in**
- ifmd_master.csv
- translated_works.csv
- original_works_by_iranian_authors.csv

**Allowed values**
```
yes
no
NA
```

---

## reprint_number

**Description**
Highest documented edition or reprint number.

**Type**
Text

**Used in**
- ifmd_master.csv
- translated_works.csv
- original_works_by_iranian_authors.csv

**Allowed values**
```
Positive integer (e.g., 1, 2, 3, ...)
multiple
NA
```

---

## notes_fa

**Description**
Supplementary notes recorded in Persian.

**Type**
Text

**Used in**
- All dataset files


---

## notes_en

**Description**
English translation of notes provided for accessibility.

**Type**
Text

**Used in**
- All dataset files

---

## source_appendix

**Description**
Original appendix within the MA thesis from which the metadata was extracted.

**Type**
Text

**Used in**
- All dataset files

**Example values**
```
Appendix A
Appendix B
```

---

## iranian_author_fa

**Description**
Standardized Persian representation of the Iranian author's name.

**Type**
Text

**Used in**
- iranian_authors.csv

---

## iranian_author_en

**Description**
Standardized English representation of the Iranian author's name.

**Type**
Text

**Used in**
- iranian_authors.csv

---

## iranian_translators_fa

**Description**
Standardized Persian representation of the Iranian translator’s name.

**Type**
Text

**Used in**
- iranian_translators.csv

---

## iranian_translators_en

**Description**
Standardized English representation of the Iranian translator’s name.

**Type**
Text

**Used in**
- iranian_translators.csv

---

## foreign_author_en

**Description**
Standardized English representation of the non-Iranian author’s name.

**Type**
Text

**Used in**
- foreign_authors.csv

---

## foreign_author_fa

**Description**
Standardized Persian representation of the non-Iranian author’s name.

**Type**
Text

**Used in**
- foreign_authors.csv

---

# Controlled Vocabulary

## work_type

| Value | Meaning |
|--------|---------|
| original | Original work by an Iranian author |
| translation | Translated work |

---

## title_gloss_type

| Value | Meaning |
|--------|---------|
| official_translation | Published English title |
| ai_literal_gloss | AI-assisted literal English gloss |

---

## reprint_status

| Value | Meaning |
|--------|---------|
| yes | One or more reprints identified |
| no | No reprints identified |
| NA | Information unavailable |

---

## reprint_number

| Value | Meaning |
|--------|---------|
| 1,2,3... | Known number of editions/reprints |
| multiple | Multiple reprints recorded without exact count |
| NA | Unknown |

---

# Identifier Prefixes

| Prefix | Description |
|---------|-------------|
| IFMD | Master dataset record |
| TRW | Translated work |
| OPW | Original Persian work |
| FA | Foreign author |
| IA | Iranian author |
| TR | Iranian translator |

---

# Data Conventions

## Romanization
Persian titles and personal names are represented in Latin script using AI-assisted transliteration followed by manual review for consistency. The resulting forms are intended to improve discoverability and accessibility rather than to conform to a specific formal romanization standard.

---

## English Title Glosses
English title glosses are provided solely to improve accessibility for non-Persian-speaking users. Where an official English title exists, it is used. Otherwise, a literal English gloss generated using AI assistance and reviewed by the dataset author is provided. These glosses are intended for identification only and do not represent published translations.

---

## Missing Values
Missing, unavailable, or not applicable values are represented as:
```
NA
```

---

## Name Standardization
Author and translator names were standardized across the repository. Persistent identifiers (author_id, translator_id) serve as the authoritative references linking records across datasets, while standardized human-readable names are included in selected work-level datasets to improve usability.

---

## Calendar System
Original publication years use the Gregorian calendar.

Iranian publication years use the Solar Hijri (Persian) calendar.

## Repository Documentation
The IFMD repository includes the following supporting documentation:

| Document | Description |
|----------|-------------|
| README.md | Project overview, repository structure, and usage instructions. |
| CITATION.cff | Citation metadata for GitHub, Zenodo, and reference managers. |
| LICENSE | Creative Commons Attribution 4.0 International (CC BY 4.0) license. |
| methodology.md | Data collection, processing, and quality assurance methodology. |
| architecture.md | Dataset architecture, file relationships, and design principles. |
| limitations.md | Scope, limitations, and known constraints of the dataset. |
| CODEBOOK.md | Reference documentation for dataset variables, identifiers, data conventions, and controlled vocabularies. |

---

# Notes
The IFMD contains bibliographic metadata only. It does not include copyrighted literary texts, page images, or full-text content.
The dataset is intended to support bibliographic analysis, computational research, metadata reuse, and scholarship in Translation Studies, Digital Humanities, Bibliometrics, Publishing History, and Persian Literary Studies.

The dataset is intended for research in Translation Studies, Digital Humanities, Bibliometrics, Publishing History, and Persian Literary Studies.
