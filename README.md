# Mental-wellbeing-study

# Depression Prevalence and Deprivation across ICBs in England

An interactive dashboard exploring how depression prevalence relates to deprivation across England's 36 Integrated Care Boards (ICBs), with a focus on employment deprivation.

**Live dashboard:** (https://depression-vs-deprivation-stats-study.streamlit.app/)

## What it shows
- A scatter plot of depression prevalence against a chosen deprivation domain score
- A Spearman correlation heat map of all measures
- Two choropleth maps: depression prevalence, and the chosen deprivation score

## Method
Small-area (LSOA) deprivation scores were aggregated to ICB level using population-weighted averages (working-age population for employment) and joined to ICB depression prevalence. Processing was done in Python with pandas and SQLite; the dashboard uses Streamlit, Plotly and GeoPandas.

## Files
- `dashboard_determinants_of_mental_wellbeing.py` – the Streamlit app
- `depression_vs_deprivation.csv` – the processed ICB-level dataset
- `Integrated_Care_Board_Boundaries.geojson` – ICB boundaries for the maps
- `requirements.txt` – packages needed to run the app
- The Colab notebook – the data processing pipeline

## Data sources
- Quality and Outcomes Framework (QOF), 2025-26 – NHS England
- English Indices of Deprivation 2025 – Ministry of Housing, Communities and Local Government
- LSOA (2021) to SICBL to ICB to NHSER to LAD (April 2026) Lookup in EN – Office for National Statistics
- Integrated Care Boards (April 2026) Boundaries EN BGC – Office for National Statistics

Contains public sector information licensed under the Open Government Licence v3.0. Contains OS data © Crown copyright and database right 2026.

## Limitations
- These are area-level associations, not causal effects.
- QOF counts only diagnosed depression recorded by GP practices, not all depression.
- With 36 ICBs, correlations should be interpreted with caution.
