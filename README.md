# ML-Driven Talent Identification in Youth Chess

This repository contains the data, code, figures, and reports for the QM640 Data Analytics Capstone project.

## Project Structure

- `data/raw/` - Raw FIDE monthly rating files and extracted calculation-page files
- `data/processed/` - Cleaned player-level and opponent-level datasets
- `data/interim/` - Intermediate datasets created during feature engineering
- `notebooks/` - Jupyter notebooks for data collection, cleaning, EDA, and modelling
- `scripts/` - Reusable Python scripts
- `outputs/figures/` - EDA and modelling figures
- `outputs/tables/` - Summary tables and model outputs
- `reports/` - Interim and final report PDFs
- `docs/` - Supporting documentation

## Data Sources

Primary public data sources include FIDE monthly rating downloads and FIDE rating-calculation pages.


The final report results are reproduced from:
notebooks/04_final_modelling/09_Modelling_and_Hypothesis_Testing_FROZEN_SAMPLE_1000.ipynb

This notebook uses the fixed 1,000-player modelling sample stored in:
data/processed/final_frozen_sample_1000/

The exploratory and intermediate notebooks are provided separately under:
notebooks/00_legacy_original_notebooks/
notebooks/01_data_preparation/
notebooks/02_fide_calculation_extraction/
notebooks/03_eda/

The final modelling notebook should not be rerun with a newly sampled dataset unless the report tables are intentionally being regenerated.

## Current Status

Final report prepared

