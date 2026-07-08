# Limitations

## Overview

The Iranian Fantasy Literature Metadata Dataset (IFMD) is intended as an openly accessible bibliographic metadata resource documenting fantasy literature published in Iran between 1270 and 1399 Solar Hijri (1891–2021 CE). Although every effort was made to ensure the accuracy, consistency, and completeness of the published metadata, users should be aware of the dataset's scope, methodological boundaries, and practical limitations when interpreting or reusing the data. The following sections summarize the principal considerations relevant to the use of the dataset.

---

# Scope of Coverage

The IFMD documents bibliographic metadata for fantasy literature published in Iran within the temporal scope of the underlying research. The dataset includes Persian translations of foreign fantasy works and original works by Iranian authors that satisfied the inclusion criteria described in the accompanying methodology documentation.
The dataset does not constitute a comprehensive national bibliography of all speculative fiction published in Iran. Publications outside the defined temporal scope, works published outside Iran, unpublished manuscripts, magazines, fan fiction, and literary forms excluded from the research design are not represented. Consequently, the absence of a publication from the dataset should not be interpreted as evidence that no such publication exists.

---

# Genre Classification

Fantasy literature does not possess universally accepted boundaries, and distinctions between fantasy and related genres may vary across scholarly traditions, publishers, and readers. Consequently, the inclusion of individual works necessarily reflects the operational definition of fantasy adopted for the underlying research.
All records were selected according to the inclusion criteria and genre classification procedures described in the accompanying methodology document. Researchers adopting substantially different definitions of fantasy may classify certain works differently. Users should therefore interpret the dataset within the conceptual framework under which it was compiled.

---

# Bibliographic Metadata

The IFMD contains bibliographic metadata only. It does not include copyrighted literary texts, page images, scanned books, or other protected content.
The repository is intended to facilitate bibliographic research, quantitative analysis, historical investigation, and metadata reuse rather than providing access to the literary works themselves.

---

# English Title Glosses

To improve accessibility for researchers who do not read Persian, the dataset includes English representations of Persian titles wherever appropriate.
Where an official published English title exists, that title is recorded in the dataset. In cases where no official English title could be identified, an AI-assisted literal English gloss, reviewed by the dataset author, is provided solely to facilitate identification and discovery of the work. These glosses are descriptive rather than authoritative translations and should not be cited as official published titles.
The distinction between official English titles and AI-assisted glosses is explicitly documented through the `title_gloss_type` variable.

---

# Authority Records and Name Standardization

Author and translator names have been standardized to improve consistency throughout the repository. In some cases, these standardized forms may differ from spellings found in publishers' catalogs, library records, previous editions, or alternative romanization systems.
The authority tables are intended to provide internally consistent identifiers for computational analysis rather than to establish definitive or universally accepted forms of personal names.

---

# Reprint Information

Information relating to reprints is based on the bibliographic records available during dataset preparation. Although considerable effort was made to identify successive editions and reprints, publishing records are not always complete or uniformly documented.
Accordingly, the recorded reprint information should be interpreted as representing the available bibliographic evidence rather than an exhaustive history of every edition published.

---

# Calendar and Dates

Publication years for works published in Iran are recorded using the Solar Hijri (Persian) calendar to preserve consistency with the original bibliographic records.
Where applicable, original publication years of foreign works are recorded using the Gregorian calendar. Users combining IFMD with external datasets should account for these different calendar systems during comparative analyses.

---

# Data Quality

The published datasets underwent multiple stages of review, standardization, identifier assignment, and consistency checking prior to release. Nevertheless, as with any manually curated bibliographic dataset, occasional transcription errors, omissions, or inconsistencies may remain despite these quality assurance procedures.
Users identifying potential errors or ambiguities are encouraged to report them through the project's GitHub repository. Verified corrections may be incorporated into future versioned releases of the dataset.

---

# Appropriate Use

The IFMD was developed primarily to support research in Translation Studies, Persian Literary Studies, Digital Humanities, Bibliometrics, Publishing History, and related disciplines. The dataset is designed for bibliographic analysis, metadata exploration, computational research, and scholarly reuse.
Because the repository reflects the scope and methodology of a specific research project, it should not be interpreted as a complete record of all fantasy-related publishing activity in Iran or as a substitute for comprehensive national library catalogs and specialized bibliographic databases.

---

# Future Updates

Version 1.0 represents the bibliographic metadata underlying the author's MA thesis _The Role of Translation in the Formation of Modern Fantasy Literature in Iran_. Future versioned releases may incorporate corrections, metadata refinements, additional bibliographic records, or other improvements identified after publication.
Each public release will remain independently archived and citable through GitHub releases and Zenodo, allowing researchers to reference the specific dataset version used in their work while ensuring the long-term reproducibility of published analyses.
