# FAIRification of Premier League Player Statistics 2024/2025 - Group 9

## About

This repository contains the artifacts produced for the FAIRification of a Premier League football players dataset.

The source data were obtained from the Kaggle dataset:

https://www.kaggle.com/datasets/danielijezie/premier-league-data-from-2016-to-2024

The project focuses on player information and player statistics for the 2024/2025 Premier League season. The original data were prepared, reconciled, merged, and transformed into a semantically enriched RDF representation using a project-specific ontology.

## Source Data

Two CSV files from the original Kaggle dataset were used as source data.

The original files are preserved together in:

`data/original/original_dataset.zip`

The original data are kept unchanged to preserve the provenance of the source material.

The original dataset distribution is identified by the following W3ID:

https://w3id.org/FAIR-course-UT/2026/group09/data-original

## Data Preparation

The source data were processed before their transformation into RDF.

The main preparation steps were:

1. Selection of relevant columns from the original CSV files.
2. Removal of columns that were not relevant to the scope of the project.
3. Merging of the prepared data from the two source files into a single dataset.
4. Cleaning and preparation of the selected data.
5. Reconciliation of selected entities in OpenRefine with Wikidata, replacing relevant textual values with links to corresponding Wikidata entities.
6. Transformation of the prepared dataset into RDF triples.

The resulting prepared CSV is preserved as an intermediate artifact in:

`data/processed/football-players-final.csv`

This file documents the result of the data preparation and reconciliation process before RDF transformation.

## FAIRified Dataset

The final FAIRified dataset is provided as an RDF/Turtle file:

`data/fairified/football-players-final.ttl`

The FAIRified RDF distribution is identified by the following W3ID:

https://w3id.org/FAIR-course-UT/2026/group09/data

The RDF dataset represents information about Premier League players and their statistics using the semantic model and ontology developed for this project.

The dataset includes information such as:

- player name
- nationality
- team
- position
- preferred foot
- date of birth
- goals
- assists
- expected goals (xG)
- expected assists (xA)

Where appropriate, entities are linked to external identifiers, including Wikidata identifiers.

## Ontology

A project-specific ontology was developed in Protégé to provide the semantic model for the FAIRified dataset.

The ontology defines the main concept of the dataset as `FootballPlayer` and describes the information associated with each player using classes, object properties, and datatype properties.

The ontology reuses existing semantic vocabularies and external identifiers where appropriate. In particular, Wikidata properties and entities are used to represent concepts such as:

- country
- football position
- sports club
- footedness
- date of birth

The ontology also defines project-specific datatype properties for player statistics, including:

- `goals`
- `assists`
- `expectedGoals`
- `expectedAssists`

The `FootballPlayer` class and the project-specific properties are defined in the Group 9 ontology namespace:

https://w3id.org/FAIR-course-UT/2026/group09/ont#

The ontology was created and exported from Protégé in OWL/RDF Turtle format and is available in:

`ontology/football-players-ontology.ttl`

The ontology is also identified using the project W3ID:

https://w3id.org/FAIR-course-UT/2026/group09/ont

## Metadata

Metadata were created using the FAIR Data Point (FDP).

The metadata describe the project catalog, the dataset, and its two distributions:

- the original dataset distribution, represented by `data/original/original_dataset.zip`;
- the FAIRified/triplified distribution, represented by `data/fairified/football-players-final.ttl`.

Custom metadata schemas were defined in the FAIR Data Point for the dataset and distribution metadata. These schemas specify the metadata properties, datatypes, cardinalities, and required fields used for the metadata records.

The metadata include information about the dataset and distributions such as titles, descriptions, creators, publishers, dates, formats, licenses, access URLs, download URLs, identifiers, and the relationship between the dataset and its distributions.

The FAIR Data Point metadata schemas are stored in:

`metadata/schemas/`

The metadata records exported from the FAIR Data Point are stored in:

`metadata/records/`

The metadata records include:

- `catalog-record.ttl` — metadata for the project catalog;
- `dataset-record.ttl` — metadata for the dataset;
- `original-distribution-record.ttl` — metadata for the original dataset distribution;
- `fairified-distribution-record.ttl` — metadata for the FAIRified/triplified distribution.

The FAIRified RDF distribution also references the project ontology through `dct:conformsTo`.

## FAIRification

The FAIRification process improved the dataset by:

- preserving the original source data
- documenting the data preparation and transformation process
- assigning persistent W3ID identifiers
- representing the prepared data as RDF
- providing a project-specific ontology
- linking selected entities to external Wikidata identifiers
- providing structured metadata through the FAIR Data Point
- publishing the project artifacts in a version-controlled GitHub repository

## License

This project is released under the MIT License.

## Repository Structure

## Repository Structure

```text
.
├── data/
│   ├── original/
│   │   └── original_dataset.zip
│   ├── processed/
│   │   └── football-players-final.csv
│   └── fairified/
│       └── football-players-final.ttl
│
├── metadata/
│   ├── schemas/
│   │   ├── dataset-schema.ttl
│   │   └── distribution-schema.ttl
│   └── records/
│       ├── catalog-record.ttl
│       ├── dataset-record.ttl
│       ├── original-distribution-record.ttl
│       └── fairified-distribution-record.ttl
│
├── ontology/
│   └── football-players-ontology.ttl
│
├── LICENSE
└── README.md