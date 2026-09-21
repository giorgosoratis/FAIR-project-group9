# FAIRification of Premier League Player Statistics season 2024/2025 (Group 9)

## Overview
This repository contains the dataset and metadata artifacts produced as part of the **FAIR Data Engineering** course project. The goal of this project is to apply the FAIR (Findable, Accessible, Interoperable, Reusable) principles to non-FAIR Premier League player performance data for season 2024/2025.

## Group Members
* **Student 1:** Giorgos Oratis
* **Student 2:** Nefeli Kantouna
* **Course:** FAIR Data Engineering 

---

## Dataset Description & Provenance (R1.2)
* **Original Source:** [Premier League Data (2016-2024) on Kaggle](https://www.kaggle.com/datasets/danielijezie/premier-league-data-from-2016-to-2024)
* **Domain:** Association Football / Premier League Player Statistics
* **Format:** Non-FAIR tabular data (`.csv`) transformed into Linked Data / RDF (`.ttl`).

### Selected Attributes (Data Dictionary)
The cleaned dataset contains 10 selected attributes focused on individual player statistics:
1. `player_name`: The full name of the player.
2. `Nationality`: Country of nationality.
3. `Preferred Foot`: Dominant foot (Left/Right).
4. `Date of Birth`: Player's birth date (formatted in ISO `YYYY-MM-DD`).
5. `player_club`: Current or recorded football club.
6. `player_position`: Playing position on the field.
7. `Goals`: Total goals scored.
8. `Assists`: Total assists made.
9. `XG`: Expected Goals statistic.
10. `XA`: Expected Assists statistic.

---

## Repository Structure
* `data/raw_data.csv`: Cleaned initial CSV dataset (10 columns).
* `data/fairified_data.ttl`: FAIRified RDF dataset in Turtle format.
* `metadata/dataset_metadata.ttl`: DCAT/DCTERMS semantic metadata records.
* `LICENSE`: Data & repository usage license.
* `README.md`: Project documentation & provenance details.

---

## Data Usage License (R1.1)
* **Code & Repository:** Released under the [MIT License](LICENSE).
* **Dataset License:** Distributed under open data standards supporting reusability.