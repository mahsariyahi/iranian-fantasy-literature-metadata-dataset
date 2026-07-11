# Iranian Fantasy Literature Metadata Dataset (IFMD)
[![Version](https://img.shields.io/github/v/release/mahsariyahi/iranian-fantasy-literature-metadata-dataset?label=version)](https://github.com/mahsariyahi/iranian-fantasy-literature-metadata-dataset/releases)
[![DOI](https://zenodo.org/badge/1293909235.svg)](https://doi.org/10.5281/zenodo.21267144)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC--BY--4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

The Iranian Fantasy Literature Metadata Dataset (IFMD) is an open-access bilingual bibliographic metadata dataset documenting Persian translations of fantasy literature and original fantasy works by Iranian authors published in Iran between 1270 and 1399 Solar Hijri (1891–2021 CE). Developed as part of the MA thesis *The Role of Translation in the Formation of Modern Fantasy Literature in Iran*, the dataset provides a structured relational bibliographic metadata dataset for the systematic study of fantasy publishing and translation in Iran. It is intended to support reproducible and reusable research in Translation Studies, literary history, bibliography, and the digital humanities. The dataset contains bibliographic metadata only and does not include copyrighted literary texts.

## Research Background
Translation has played an important role in the introduction and development of literary genres within many literary systems. Building on Even-Zohar's polysystem theory, the underlying research investigated the position of translated fantasy literature within the Persian literary polysystem and examined its contribution to the emergence of modern fantasy literature in Iran.
The published IFMD repository is derived from the bibliographic dataset compiled for the MA thesis and has been enhanced for public dissemination through additional documentation, identifier assignment, and relational organization.

## Related Publication
The IFMD was developed as part of the following MA thesis:

> Riyahi, Mahsa. *The Role of Translation in the Formation of Modern Fantasy Literature in Iran*. MA thesis, Allameh Tabataba'i University, 2021.

The dataset provides the structured bibliographic metadata dataset underlying the analyses presented in the thesis.

## Scope
The dataset includes bibliographic metadata for fantasy literature that satisfies the following criteria:

- Published in Iran
- Published between 1270 and 1399 Solar Hijri (1891–2021 CE)
- Original works by Iranian authors
- Persian translations of foreign fantasy literature
- Books with sufficient bibliographic information for identification

The dataset excludes:
- Full-text literary works
- Unpublished manuscripts
- Fan fiction
- Works lacking sufficient bibliographic metadata

## Repository Structure
``` 
iranian-fantasy-literature-metadata-dataset/
|
|── README.md
|── LICENSE
|── CITATION.cff
|── CODEBOOK.md
|
|── data/
|      |── raw/
|      |     └── original_dataset.docx
|      |
|      └── processed/
|            ├── foreign_authors.csv
|            ├── ifmd_master.csv
|            ├── iranian_translators.csv
|            ├── iranian_authors.csv
|            ├── original_works_by_iranian_authors.csv
|            └── translated_works.csv
|
|── docs/
|     |── methodology.md
|     |── architecture.md
|     └── limitations.md
|
|── visualizations/
|── analysis/
└── notebooks/
``` 

## Dataset Organization

The IFMD is organized as a relational bibliographic metadata dataset distributed as interoperable UTF-8 encoded CSV files. Literary works, authors, and translators are represented in separate datasets linked through persistent identifiers (work_id, author_id, and translator_id).
To improve usability for researchers working directly with CSV files, selected descriptive metadata, including standardized author and translator names, are intentionally included in work-level datasets alongside their identifiers. The identifiers serve as the authoritative mechanism for linking records across the repository.

## Documentation
Detailed documentation of the dataset is provided in the accompanying documentation files. `CODEBOOK.md`  documents the dataset variables, identifier conventions, and controlled vocabularies.
The documents in the `docs/` directory describe the dataset methodology, architecture, and known limitations. 

## Methodology
The dataset was compiled through systematic bibliographic data collection undertaken as part of the author's MA research. Records were identified, standardized, cleaned, assigned persistent identifiers, and organized into a relational bibliographic metadata dataset consisting of work-level datasets and authority tables linked through identifier-based relationships. Selected descriptive metadata (such as standardized author and translator names) are intentionally retained in work-level datasets to improve usability while persistent identifiers provide the authoritative links between related records.

Further details regarding data sources, inclusion criteria, data processing procedures, and quality assurance are available in `docs/methodology.md`.

## Research Applications
The IFMD may support research in areas including:
- Translation Studies
- Digital humanities
- Persian literature
- Fantasy literature
- Comparative literature
- Book history
- Publishing studies
- Bibliometrics
- Literary network analysis
- Metadata research

## Citation
If you use this dataset in research, teaching, or derivative works, please cite the dataset using the citation information provided in `CITATION.cff`.

DOI: 10.5281/zenodo.21267145

## License
This dataset is licensed under the Creative Commons Attribution 4.0 International (CC BY 4.0). You are free to share and adapt the metadata provided that appropriate attribution is given. See the `LICENSE` file for the full license text.
