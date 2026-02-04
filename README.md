# StatsBomb JSON Familiarisation and Analytics Pipeline Foundations

## Overview

This repository contains exploratory work using publicly available StatsBomb football event data. The purpose of this work is to build a solid understanding of StatsBomb style JSON data formats and to use that understanding as a foundation for designing an end to end analytics pipeline for a future MSc thesis project.

The focus at this stage is on data structure, schema understanding, and abstraction rather than advanced analysis or modelling.

---

## Data Source

The data used in this repository comes from the StatsBomb Open Data repository. A single match events JSON file was selected as a representative sample for exploration.

StatsBomb event data is provided in JSON format, with each match represented as a list of event objects. Each event corresponds to a single on pitch action or state change, such as a pass, shot, duel, or lineup declaration.

---

## What Was Explored

The work in this repository covers the following:

- Exploration of StatsBomb open data structure and file conventions
- Inspection of raw event level JSON data
- Identification of key fields such as event type, team, player, time, location, and possession
- Examination of nested objects for complex actions such as passes, shots, and tactical information
- Extraction of Starting XI information from event data
- Creation of basic exploratory visualisations, including:
  - Shot location plots
  - Pass maps for a single team
  - Event timelines across a match
- Conversion of raw JSON data into analysis ready tabular structures

---

## Analysis Ready Tables

As part of the exploration, two simple tables were created to demonstrate how raw event data can be flattened and prepared for downstream analysis:

- `events_basic`: one row per event with common contextual fields
- `passes`: one row per pass event with start and end locations and key pass attributes

These tables represent the type of structured data that would later be stored in a database as part of a full analytics pipeline.

---

## Outputs

The `outputs` folder contains exported CSV files and basic visualisations generated during exploration. These outputs are included to demonstrate how raw JSON data can be transformed into usable analytical artefacts.

---

## Relevance to Future Work

This exploratory work provides a foundation for future pipeline design by clarifying:

- What football event data looks like at the raw input level
- How nested JSON structures need to be flattened and validated
- What minimum fields are required for analysis
- How StatsBomb style data can act as a template for integrating data from other providers

This understanding will inform later stages of the MSc thesis, including data ingestion design, database schema development, analysis workflows, and visualisation.
