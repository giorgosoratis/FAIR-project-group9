# FAIRification of Premier League Player Statistics 2024/2025 - Group 9

## About

This repository contains the artifacts produced for the FAIRification
of a Premier League football players dataset.

The original data were obtained from the Kaggle dataset:
https://www.kaggle.com/datasets/danielijezie/premier-league-data-from-2016-to-2024

Two CSV files were used as source data. Relevant columns were selected
and combined to create the dataset used in the FAIRification process.

## Repository structure

- `data/original/` - original source CSV files
- `data/fairified/` - final CSV and RDF/Turtle dataset
- `ontology/` - semantic ontology
- `metadata/` - metadata schemas and metadata records

## FAIRified data

The final dataset contains football player information such as:

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

The final RDF dataset uses the ontology defined for this project and
links entities to Wikidata.

## Identifiers

Ontology:
https://w3id.org/FAIR-course-UT/2025-2026/group9/ont

Data:
https://w3id.org/FAIR-course-UT/2025-2026/group9/data#

## Files

The original source files are preserved unchanged.
The final CSV represents the prepared dataset after data cleaning,
column selection/addition and reconciliation.
The Turtle file is the RDF representation of the final dataset.