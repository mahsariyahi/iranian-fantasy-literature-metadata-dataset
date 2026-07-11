# Methodology

## Overview
The Iranian Fantasy Literature Metadata Dataset (IFMD) was developed as part of the MA thesis *The Role of Translation in the Formation of Modern Fantasy Literature in Iran*. The dataset documents bibliographic metadata for fantasy literature published in Iran between 1270 and 1399 Solar Hijri (1891–2021 CE), including both Persian translations of foreign fantasy works and original works by Iranian authors. This document describes the methodology used to compile, process, standardize, and organize the bibliographic metadata for public release. The published dataset contains bibliographic metadata only and does not include copyrighted literary texts.
For public release, the original bibliographic dataset was documented, assigned persistent identifiers, reorganized into a relational dataset, and made openly available to support transparent, reproducible, and reusable research.

## Research Context
The IFMD was developed during the preparation of the MA thesis The Role of Translation in the Formation of Modern Fantasy Literature in Iran. The underlying study investigated the role of translated fantasy literature in the emergence of modern fantasy literature in Iran within the framework of Even-Zohar's polysystem theory. To address its research objectives, the thesis combined systematic bibliographic research with paratextual analysis of interviews, biographies, and reviews relating to Iranian fantasy authors.
The public dataset represents the bibliographic component of that research. It documents the corpus of fantasy books identified through systematic bibliographic data collection and provides the structured metadata underlying the quantitative analyses presented in the thesis. The paratextual corpus and qualitative analytical materials used in the study are not included in this dataset.

## Scope
The Iranian Fantasy Literature Metadata Dataset (IFMD) documents published fantasy literature in Iran between 1270 and 1399 Solar Hijri (1891–2021 CE). The temporal scope was selected because the earliest identified fantasy publication in Iran dates to the late Qajar period, making this interval appropriate for documenting the historical development of modern fantasy publishing in Iran.
The dataset comprises two complementary bibliographic corpora:
- original fantasy works by Iranian authors; and
- Persian translations of foreign fantasy literature published in Iran.

The IFMD records bibliographic metadata relating to these publications, including information on authorship, translation, publication history, editions, and reprints where available. For translated works, metadata describing both the original work and its Persian translation are recorded where bibliographic evidence exists.
Although the underlying MA thesis also examined a corpus of paratextual materials—including interviews, biographies, and reviews—to investigate the influence of translation on Iranian fantasy authors, those materials are not included in the released dataset. The IFMD contains bibliographic metadata only.

### Inclusion Criteria
A bibliographic record was included in the IFMD only if it satisfied all of the following criteria:
- The work was published in Iran.
- The publication fell within the study period of 1270–1399 Solar Hijri (1891–2021 CE).
- The work was identified as fantasy literature according to the criteria adopted in the underlying research. To determine genre eligibility, the study drew on the approaches to defining fantasy proposed by James and Mendlesohn (2009), together with evidence from bibliographic and reference sources.
- The work was either:
  - an original work by an Iranian author, or
  - a Persian translation of a foreign fantasy work.
- Sufficient bibliographic metadata were available to permit reliable identification and documentation of the publication.

### Exclusion Criteria
The following materials were excluded from the IFMD:
- Works published outside the study period (1270–1399 Solar Hijri / 1891–2021 CE).
- Publications not identified as fantasy literature according to the criteria adopted in the underlying research.
- Works not published in Iran.
- Records lacking sufficient bibliographic metadata for reliable identification.
- Unpublished manuscripts, despite being consulted during the bibliographic research to verify early fantasy publications.
- Fan fiction and other non-commercially published works.
- Full-text literary works and other copyrighted content. The dataset contains bibliographic metadata only.

## Data Sources
The IFMD was compiled through systematic bibliographic research conducted during the author's MA research. Bibliographic records were identified, verified, and standardized using multiple complementary sources.

### National Bibliographic Records
The online catalogue of the **National Library and Archives of Iran (NLAI)** served as the principal bibliographic source for the dataset. Systematic catalogue searches were conducted to identify eligible fantasy publications, verify publication details, determine publication years, identify translators, and document available edition and reprint information. The NLAI catalogue formed the primary source for bibliographic verification throughout the data collection process.

### Secondary Reference Sources
Secondary reference works and genre-specific resources were consulted to identify authors and establish the scope of the fantasy corpus before bibliographic verification. These sources were used to compile preliminary lists of Iranian and foreign fantasy authors and works, which were subsequently verified through searches of the NLAI catalogue.
The principal secondary sources included:
- James, Edward, & Mendlesohn, Farah (Eds.). *The Cambridge Companion to Fantasy Literature* (2012).
- Mohammadi, Mohammad Hadi, & Qaeeni, Zohreh. *Fantasy in Children's Literature* (1999).
- Mousavi, Mohammad, & Jamali, Ahmad. *Fantasy: Its Nature and History in the World and Iranian Literature* (2009).
- Goodreads (genre discovery and author identification).
- Ranker (genre discovery and author identification).


### Additional Bibliographic Verification
Additional bibliographic catalogues and manuscript repositories were consulted to verify early fantasy publications and resolve ambiguous bibliographic records where necessary. These included:
- Aghabozorg database.
- National Library manuscript catalogue.
- Library, Museum and Documentation Center of the Islamic Consultative Assembly.
- Malek National Library and Museum Institution.
These resources supported bibliographic verification during data collection. Although manuscript catalogues were consulted to identify and verify early fantasy works during the data collection process, unpublished manuscripts are not included in the released dataset.

## Data Collection Workflow
Bibliographic records were collected through systematic library research conducted as part of the author's MA research. Data collection followed a sequential workflow designed to identify eligible fantasy works, verify their bibliographic information, and compile a comprehensive corpus of published fantasy literature in Iran.

### Identification of Fantasy Authors
The data collection process began with the compilation of preliminary lists of foreign and Iranian fantasy authors.
Foreign fantasy authors were identified using *The Cambridge Companion to Fantasy Literature*, Goodreads, and Ranker. Iranian fantasy authors were identified through *Fantasy in Children's Literature*, *Fantasy: Its Nature and History in the World and Iranian Literature*, and searches of the National Library and Archives of Iran (NLAI) catalogue.

### Identification of Fantasy Works
Because not all works by the identified authors belong to the fantasy genre, each publication was evaluated for genre eligibility. The study adopted the approaches to defining fantasy proposed by James and Mendlesohn (2009), together with evidence from bibliographic and reference sources, to determine whether individual works should be included in the corpus.

### Bibliographic Metadata Collection
The names of eligible Iranian and foreign authors were systematically searched in the NLAI catalogue to identify published fantasy works and extract their bibliographic metadata.
For original works by Iranian authors, metadata including publication year, publisher, and documented reprint history were recorded where available.
For translated works, metadata relating to both the original publication and its Persian translation were collected where available, including the original title, original publication year, translator, translated title, Persian publication year, publisher, and documented reprint history.
Where multiple Persian translations of the same foreign work existed, publication histories were examined to identify the earliest available translation and document subsequent editions and reprints.

### Verification of Early Publications
Because manuscript records are not comprehensively represented in the NLAI catalogue, additional bibliographic catalogues and manuscript repositories were consulted to identify and verify early fantasy publications. These searches supported the completeness of the historical bibliographic corpus, although unpublished manuscripts are not included in the released dataset.

## Data Processing
During preparation of the public dataset, the original bibliographic records compiled for the MA thesis were reviewed, standardized, assigned persistent identifiers, and reorganized into linked work-level and authority-level datasets. This structure reduces unnecessary redundancy, improves consistency, and enables relationships between publications, authors, and translators through persistent identifiers.
The data processing workflow included the following steps:
### Data Cleaning
Bibliographic records were manually reviewed to identify inconsistencies, correct typographical errors, remove duplicate entries where appropriate, and ensure consistency across publication metadata.

### Metadata Standardization
Personal names, publication information, and bibliographic fields were standardized to ensure consistent representation throughout the dataset.
Controlled vocabularies, standardized variable names, and persistent identifier conventions were adopted to improve consistency and interoperability across the published datasets.

### Authority Control
Separate authority tables were created for Iranian authors, foreign authors, and Iranian translators. These tables provide the authoritative identifier assignments and canonical name forms used throughout the repository. This approach reduces unnecessary redundancy, ensures consistent representation of individuals across multiple records, and supports relational analyses. For usability, selected descriptive attributes (e.g., author and translator names) are also retained in work-level datasets while persistent identifiers remain the authoritative links between tables.


### Identifier Assignment
Persistent identifiers were assigned to all works and authority records. These identifiers establish explicit relationships between the master dataset and the corresponding authority tables while providing stable references within the dataset.

### Relational Restructuring
The original appendix tables were reorganized into a relational bibliographic metadata structure consisting of one master dataset and multiple linked authority and work-level datasets. This organization reduces unnecessary redundancy, improves consistency, and facilitates computational analysis.

### Data Export
The processed datasets were exported as UTF-8 encoded CSV files to maximize interoperability across statistical software, spreadsheet applications, programming environments, and digital humanities workflows.

## Quality Assurance
Several quality assurance procedures were applied throughout the preparation of the IFMD to improve the accuracy, consistency, and reliability of the published metadata.
During data collection, bibliographic records were verified against the National Library and Archives of Iran (NLAI) catalogue, which served as the principal bibliographic authority for publication metadata. Additional bibliographic and manuscript catalogues were consulted where necessary to verify early publications and resolve ambiguous records.
Prior to publication, the dataset underwent manual review to identify typographical errors, resolve inconsistencies in bibliographic fields, standardize personal names and publication metadata, and ensure consistency across the linked datasets. Duplicate records were identified and removed where appropriate, and persistent identifiers were checked to ensure that relationships between work-level and authority-level tables were maintained correctly.
Despite these quality assurance procedures, the IFMD should be regarded as a scholarly bibliographic resource rather than a definitive national bibliography. The dataset reflects the bibliographic evidence available at the time of compilation and may be updated in future releases to incorporate corrections or additional metadata.
Users who identify errors or omissions are encouraged to report them through the project's GitHub repository so they may be considered in future dataset releases.

## Dataset Outputs
The processed dataset is distributed as a collection of interoperable CSV files organized according to a relational metadata structure. The master dataset contains all bibliographic records, while separate authority tables provide authoritative identifier assignments and canonical name forms for Iranian authors, foreign authors, and Iranian translators. Additional datasets separate translated works from original works by Iranian authors to facilitate different types of bibliographic and quantitative analyses.
The accompanying repository documentation describes the dataset architecture, variables, identifier system, controlled vocabularies and known limitations in greater detail.

## Reproducibility
The repository includes both the original source document used during dataset preparation and the processed machine-readable datasets together with comprehensive documentation, including the project README, codebook, architecture description, limitations document, citation metadata, and licensing information.
This documentation is intended to promote transparency, reproducibility, and long-term reuse of the dataset.

## Versioning
Version 1.0 of the Iranian Fantasy Literature Metadata Dataset (IFMD) derived from the bibliographic dataset compiled during the author's MA thesis and represents its first public release as a documented relational bibliographic metadata dataset.
Future releases may incorporate corrections, expanded metadata, or additional records. All substantive changes will be documented through versioned GitHub releases and archived Zenodo records to preserve a transparent version history.
