# Architecture

## Overview
The Iranian Fantasy Literature Metadata Dataset (IFMD) is organized as a relational bibliographic metadata dataset designed to promote transparency, consistency, and long-term reusability. Rather than presenting the underlying research data as a single spreadsheet, the dataset is structured as a collection of linked CSV files that separate publication records from authority records while preserving explicit relationships through persistent identifiers.
The repository consists of one master dataset containing all bibliographic records, two work-level datasets distinguishing translated works from original works by Iranian authors, and three authority tables containing standardized information for Iranian authors, foreign authors, and Iranian translators. This relational organization improves consistency while supporting computational analysis and future expansion of the dataset.
In addition to the machine-readable data files, the repository includes comprehensive documentation describing the dataset's methodology, architecture, variables, coding conventions, limitations, citation metadata, and licensing information. Together, these components provide a transparent and reproducible framework for the preservation, dissemination, and reuse of the bibliographic metadata underlying the author's MA thesis *The Role of Translation in the Formation of Modern Fantasy Literature in Iran*.

## Design Principles
The architecture of the Iranian Fantasy Literature Metadata Dataset (IFMD) was guided by a set of design principles intended to improve the dataset's transparency, usability, and long-term value as a research resource.

### Relational Organization
The dataset is organized as a relational collection of linked tables rather than a single spreadsheet. Bibliographic records, work-level datasets, and authority tables are connected through persistent identifiers. Selected descriptive metadata are intentionally retained in work-level datasets to improve usability, while the identifiers preserve explicit relationships between publications, authors, and translators.

### Transparency
The repository includes comprehensive documentation describing the dataset's methodology, structure, variables, coding conventions, and limitations. Together with the original source document used during data preparation, these materials enable users to understand how the published metadata were compiled, processed, and organized.

### Reproducibility
The repository preserves the bibliographic metadata underlying the author's MA thesis in a structured and openly accessible form. The inclusion of the original source document, processed datasets, and supporting documentation promotes transparency and facilitates the verification and reuse of the published metadata.

### Bilingual Accessibility
To improve accessibility for both Persian-speaking and international researchers, the dataset incorporates bilingual metadata wherever appropriate. Persian titles and personal names are accompanied by standardized English representations, romanized forms, and English title glosses where available, enabling broader discovery and interpretation of the dataset.

### Interoperability
The IFMD is distributed as UTF-8 encoded CSV files using standardized variable names, controlled vocabularies, and persistent identifiers. These design choices facilitate use across spreadsheet software, statistical packages, programming environments, and Digital Humanities workflows.

### Long-term Preservation
The repository has been designed for sustainable scholarly dissemination through GitHub and Zenodo. Version-controlled releases, persistent identifiers, open documentation, and an open license support the long-term preservation, citation, and reuse of the dataset.

---
# Repository Structure
The IFMD repository is organized into separate directories for data, documentation, and supporting research materials. This structure separates the published datasets from their accompanying documentation while preserving the original source material used during dataset preparation. The repository organization is intended to improve discoverability, facilitate long-term maintenance, and support reproducible research.

The repository is structured as follows:

```text
iranian-fantasy-literature-metadata-dataset/
│
├── README.md
├── CODEBOOK.md
├── LICENSE
├── CITATION.cff
│
├── data/
│   ├── raw/
│   │   └── original_dataset.docx
│   │
│   └── processed/
│       ├── ifmd_master.csv
│       ├── translated_works.csv
│       ├── original_works_by_iranian_authors.csv
│       ├── iranian_authors.csv
│       ├── foreign_authors.csv
│       └── iranian_translators.csv
│
├── docs/
│   ├── methodology.md
│   ├── architecture.md
│   └── limitations.md
│
├── analysis/
├── notebooks/
└── visualizations/
```

The principal components of the repository serve the following purposes:

| Component           | Purpose                                                                                                     |
| ------------------- | ----------------------------------------------------------------------------------------------------------- |
| **README.md**       | Provides an overview of the dataset, repository contents, and instructions for use and citation.            |
| **CODEBOOK.md**     | Documents dataset variables, identifiers, controlled vocabularies, and data conventions.                    |
| **LICENSE**         | Specifies the terms under which the dataset may be reused and redistributed.                                |
| **CITATION.cff**    | Provides standardized citation metadata for GitHub, Zenodo, and reference management software.              |
| **data/raw/**       | Preserves the original source document from which the published datasets were derived.                      |
| **data/processed/** | Contains the machine-readable CSV datasets distributed as part of the IFMD.                                 |
| **docs/**           | Contains supporting documentation describing the methodology, architecture, and limitations of the dataset. |
| **analysis/**       | Reserved for scripts and materials used for quantitative analyses of the dataset.                           |
| **notebooks/**      | Reserved for computational notebooks demonstrating data exploration and reproducible analyses.              |
| **visualizations/** | Reserved for figures, charts, and other visual outputs derived from the dataset.                            |

This organization separates data from documentation while preserving the complete research context required for transparent interpretation, computational reuse, and future maintenance of the dataset.

---

# Dataset Structure
The IFMD is distributed as six interoperable UTF-8 encoded CSV datasets organized according to a relational metadata structure. Rather than storing all information in a single table, the dataset separates bibliographic records, work-level metadata, and authority records into distinct files linked through persistent identifiers. This design improves consistency and supports efficient computational analysis.
The dataset comprises one master dataset, two work-level datasets, and three authority tables.

| Dataset                                   | Description                                                                                                                                                                                                                                |
| ----------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **ifmd_master.csv**                       | Master bilingual bibliographic metadata dataset containing all fantasy works published in Iran within the scope of the study. Each record links to the appropriate work-level dataset and authority tables through persistent identifiers. |
| **translated_works.csv**                  | Contains bibliographic metadata for Persian translations of foreign fantasy works, including information on the original work and its Persian publication where available.                                                                 |
| **original_works_by_iranian_authors.csv** | Contains bibliographic metadata for original fantasy works by Iranian authors.                                                                                                                                                             |
| **iranian_authors.csv**                   | Authority table containing persistent identifier assignments and canonical name forms for Iranian authors referenced throughout the dataset.                                                                                                                                     |
| **foreign_authors.csv**                   | Authority table containing persistent identifier assignments and canonical name forms for foreign authors referenced throughout the dataset.                                                                                                                                     |
| **iranian_translators.csv**               | Authority table containing persistent identifier assignments and canonical name forms for Iranian translators referenced throughout the dataset.                                                                                                                                 |

The master dataset serves as the central access point to the repository by integrating all bibliographic records into a single bilingual table. The work-level datasets provide subsets of records for translated works and original works by Iranian authors, while the authority tables provide authoritative identifier assignments and canonical name forms for authors and translators.
Relationships between datasets are established through persistent identifiers. Selected descriptive metadata (such as standardized author and translator names) are intentionally retained within work-level datasets to improve readability and usability when individual CSV files are used independently. Work records are linked through the `work_id` field, while author and translator records are connected through the `author_id` and `translator_id` fields. This relational organization supports consistent representation of bibliographic entities and facilitates computational analysis across the dataset.

---

# Relational Data Model

The IFMD is organized as a relational metadata dataset in which bibliographic records and authority records are distributed across multiple linked tables. Relationships between publications, authors, and translators are maintained through persistent identifiers, while selected descriptive metadata are intentionally repeated in work-level datasets to improve usability.

The `ifmd_master.csv` dataset functions as the central table of the repository. Each record represents a single bibliographic publication and contains references to the corresponding work-level dataset and authority records through unique identifiers.

The two work-level datasets provide more specific bibliographic information according to publication type:

* `translated_works.csv` contains records for Persian translations of foreign fantasy works.
* `original_works_by_iranian_authors.csv` contains records for original fantasy works by Iranian authors.

These datasets are linked to the master dataset through the `work_id` field, allowing each publication to be associated with its corresponding work-level record.

Information relating to authors and translators is managed separately through three authority tables:

* `iranian_authors.csv`
* `foreign_authors.csv`
* `iranian_translators.csv`

These authority tables are connected to the work-level and master datasets through the `author_id` and `translator_id` fields. The authority tables provide the authoritative identifier assignments and canonical name forms for authors and translators. Work-level datasets reference these entities through persistent identifiers while retaining human-readable names as descriptive labels. This organization improves consistency across the dataset and provides stable identifier-based relationships between related records.

The overall relationships among the datasets are illustrated below.
```text
                        ifmd_master.csv
                         ───────────────
                          work_id
                              │
          ┌───────────────────┴───────────────────┐
          │                                       │
          ▼                                       ▼
  translated_works.csv           original_works_by_iranian_authors.csv
          │                                       │
          │                                       │
      author_id                                author_id
          │                                       │
          ▼                                       ▼
  foreign_authors.csv                   iranian_authors.csv
          │
          │
    translator_id
          │
          ▼
Iranian_translators.csv
```

This relational architecture enables users to analyze the complete corpus through the master dataset while also supporting more specialized analyses of translated works, original works by Iranian authors, authorship, and translation networks through the linked work-level and authority tables.
---
## Controlled Denormalization

Although IFMD follows a relational organization, selected descriptive metadata, including standardized author and translator names, are intentionally retained in work-level datasets alongside their persistent identifiers. This controlled denormalization improves readability and usability for researchers working directly with CSV files in spreadsheet software, statistical environments, and programming languages while preserving the identifier-based relationships between related entities.

Within the repository, persistent identifiers (`work_id`, `author_id`, and `translator_id`) constitute the authoritative mechanism for linking related records across datasets.

---
# Identifier System

The IFMD uses persistent, human-readable identifiers to establish explicit relationships between records across the relational datasets. Each identifier is unique within its corresponding table and remains stable across dataset releases, enabling consistent cross-referencing, computational analysis, and future expansion of the repository.

Identifiers are assigned to all bibliographic records in the master dataset, work-level datasets, and authority tables. Identifiers establish explicit relationships between related records while descriptive metadata remain available within individual datasets for usability.

The identifier system consists of the following prefixes:

| Prefix   | Entity                             |
| -------- | ---------------------------------- |
| **IFMD** | Master dataset record              |
| **TRW**  | Translated work                    |
| **OPW**  | Original work by an Iranian author |
| **IA**   | Iranian author                     |
| **FA**   | Foreign author                     |
| **TR**   | Iranian translator                 |

Identifiers follow a standardized format consisting of a prefix followed by a sequential numerical value (e.g., `IFMD_0001`, `TRW_0001`, `IA_0001`). The prefixes indicate the type of entity represented, while the numerical component provides a unique identifier within that category.

These identifiers establish the relationships between the repository's datasets. The work_id field links records in ifmd_master.csv to the corresponding work-level dataset, while the author_id and translator_id fields connect publications to the appropriate authority tables. The identifier system provides stable references between related records and supports consistent linkage across the repository.

A complete reference for identifier formats and their usage is provided in the accompanying `CODEBOOK.md`.

---

# Authority Tables
The IFMD separates information about authors and translators from publication records through dedicated authority tables. These tables provide the authoritative identifier assignments and canonical name forms for authors and translators represented throughout the repository. Work-level datasets reference these entities through persistent identifiers while retaining selected descriptive fields to improve usability.

---

# Bilingual Metadata Design
The IFMD was designed as a bilingual bibliographic dataset to improve accessibility for both Persian-speaking and international researchers. Wherever appropriate, bibliographic metadata are provided in both Persian and English, allowing users with different linguistic backgrounds to identify, interpret, and analyze the recorded publications.
The bilingual design extends across the principal descriptive metadata fields. Persian titles and personal names are accompanied by English representations, while Persian titles are additionally provided in romanized form to facilitate searching and citation by users who do not read the Persian script. Where official English titles exist, they are recorded in the dataset. Otherwise, AI-assisted literal English glosses, reviewed by the dataset author, are provided solely to improve discoverability and identification of the works.
This multilingual representation improves the interoperability of the dataset across international research environments while preserving the original Persian bibliographic information. At the same time, the distinction between official published translations and AI-assisted English glosses is explicitly recorded through controlled vocabulary, enabling users to distinguish between published English titles and descriptive translations created for accessibility purposes.
The bilingual metadata design reflects the interdisciplinary nature of the IFMD, supporting research in Translation Studies, Digital Humanities, Bibliometrics, Publishing History, Persian Literary Studies, and related fields by making the dataset accessible to a broader scholarly community.

---

# Data Flow
The published IFMD datasets were derived from the bibliographic appendices prepared during the author's MA research. Before publication, the original bibliographic records were reviewed, standardized, reorganized into a relational metadata structure, and exported as machine-readable CSV files. The resulting workflow transforms the original research data into an openly accessible and reusable bibliographic dataset.
The overall data flow is illustrated below.

```text
                MA Thesis Appendices
                          │
                          ▼
               Data Cleaning & Review
                          │
                          ▼
            Metadata Standardization
                          │
                          ▼
              Authority Table Creation
                          │
                          ▼
          Persistent Identifier Assignment
                          │
                          ▼
           Relational Dataset Construction
                          │
                          ▼
           UTF-8 Encoded CSV Dataset Export
                          │
                          ▼
       GitHub Repository & Zenodo Publication
```

This workflow summarizes the principal stages involved in preparing the published dataset. Detailed descriptions of the data collection, processing, and quality assurance procedures are provided in the accompanying `methodology.md` document.

---
# Repository Documentation

The IFMD repository includes a collection of supporting documentation intended to facilitate the interpretation, citation, and reuse of the published datasets. Together, these documents describe the dataset's scope, methodology, architecture, variables, limitations, licensing, and citation metadata, providing the contextual information necessary for transparent and reproducible research.

The repository documentation comprises the following components:

| Document            | Purpose                                                                                                                                                                          |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **README.md**       | Introduces the dataset, outlines the repository contents, and provides guidance on installation, usage, citation, and licensing.                                                 |
| **CODEBOOK.md**     | Documents the dataset variables, identifier system, controlled vocabularies, data conventions, and coding practices used throughout the repository.                              |
| **methodology.md**  | Describes the research context, data sources, collection procedures, processing workflow, quality assurance measures, and reproducibility considerations underlying the dataset. |
| **architecture.md** | Explains the repository organization, relational data model, identifier system, and design principles adopted for the published dataset.                                         |
| **limitations.md**  | Describes the scope of the dataset, known limitations, and considerations for interpretation and reuse.                                                                          |
| **CITATION.cff**    | Provides standardized citation metadata compatible with GitHub, Zenodo, and reference management software.                                                                       |
| **LICENSE**         | Specifies the terms under which the dataset may be reused and redistributed under the Creative Commons Attribution 4.0 International (CC BY 4.0) license.                        |

Collectively, these documents complement the machine-readable datasets by providing the descriptive and contextual metadata required for their accurate interpretation, responsible reuse, and long-term preservation as an open scholarly resource.

---
# Versioning
The IFMD follows a versioned release model to ensure transparency, reproducibility, and the long-term preservation of the published dataset. Each public release represents a stable snapshot of the repository and is archived through GitHub releases and Zenodo.
Version 1.0 represents the first public release of the IFMD. It is based on the bibliographic dataset compiled during the author's MA thesis *The Role of Translation in the Formation of Modern Fantasy Literature in Iran* and includes additional documentation, persistent identifier assignment, relational organization, and metadata standardization undertaken to prepare the dataset for public dissemination.
Each released version will preserve its own citation metadata and archived record, enabling researchers to cite the specific version of the dataset used in their work. This versioning strategy supports reproducible research by ensuring that published analyses remain linked to the exact dataset on which they were based.
Substantive changes between releases will be documented through the repository's release history and accompanying documentation.
