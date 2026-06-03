cat > README.md <<'EOF'
# ML-Driven Talent Identification in Youth Chess

This repository contains the data, notebooks, outputs, and reports for the QM640 Data Analytics Capstone project: **ML-Driven Talent Identification in Youth Chess**.

The project develops a machine-learning-based decision-support framework for identifying future rating development among Indian youth FIDE-rated chess players. The final analysis predicts 12-month FIDE Standard rating gain, evaluates milestone crossing at 1800 and 2000, and classifies players into developmental trajectory categories such as high-growth, stable progress, plateau, decline, and inactivity risk.

---

## Project Objective

The main objective is to test whether rating history, tournament activity, inactivity, opponent strength, and performance-quality variables can improve prediction of future chess rating development beyond current rating alone.

The primary target variable is:

`rating_gain_12m = FIDE Standard rating in April 2026 - FIDE Standard rating in April 2025`

The final modelling dataset uses a fixed 1,000-player Indian youth sample.

---

## Repository Structure

```text
data/
├── raw/              Raw FIDE source files and player sample files
├── interim/          Intermediate datasets created during cleaning and feature engineering
└── processed/        Final cleaned modelling datasets

notebooks/
├── 00_legacy_original_notebooks/       Original exploratory notebooks
├── 01_data_preparation/                Data cleaning, monthly history, and sampling notebooks
├── 02_fide_calculation_extraction/     FIDE calculation-page extraction notebooks
├── 03_eda/                             Exploratory data analysis and report figures
└── 04_final_modelling/                 Final frozen modelling and hypothesis-testing notebook

outputs/
├── figures/          EDA and report figures
└── tables/           Model results, hypothesis-test outputs, and summary tables

reports/              Interim and final report PDFs
docs/                 Supporting documentation
scripts/              Reusable Python scripts, if applicable



## Data Sources

The project uses publicly available chess data from the following sources:

1. **FIDE monthly Standard rating downloads**  
   Used for player rating history, federation, games played, K-factor, title, sex, and birth-year fields.

2. **FIDE rating-calculation pages**  
   Used for opponent-level enrichment, including opponent rating, score, tournament name, rating change, and K-adjusted rating change.

Chess-Results and the All India Chess Federation website were retained only for context and verification, not as primary modelling inputs.


## Final Reproducible Analysis

The final report results are reproduced from:

```text
notebooks/04_final_modelling/09_Modelling_and_Hypothesis_Testing_FROZEN_SAMPLE_1000.ipynb


## Main Workflow

The project workflow follows these stages:

1. Build monthly FIDE Standard rating history.
2. Filter the Indian youth FIDE-rated player pool.
3. Create the fixed 1,000-player modelling sample.
4. Extract FIDE rating-calculation pages for opponent-level enrichment.
5. Clean and combine player-level and opponent-level records.
6. Engineer rating, activity, inactivity, opponent-strength, and performance features.
7. Perform exploratory data analysis and generate report figures.
8. Run hypothesis testing for RQ1 and RQ2.
9. Train regression models for 12-month rating gain.
10. Train milestone classification models for 1800 and 2000 crossing.
11. Create and classify developmental trajectory labels.
12. Export report-ready tables and figures.


| Notebook                                                                 | Purpose                                                                 |
| ------------------------------------------------------------------------ | ----------------------------------------------------------------------- |
| `01_build_fide_monthly_history_and_player_pool.ipynb`          | Builds cleaned monthly FIDE Standard rating history and player pool     |
| `03_create_remaining_player_pool_excluding_3000.ipynb`         | Creates remaining eligible pool after excluding already sampled players |
| `04_extract_calculation_pages_sample_1000.ipynb`               | Extracts FIDE calculation-page data for the fixed 1,000-player sample   |
| `08_eda_and_report_figures.ipynb`                              | Performs EDA and creates report figures                                 |
| `09_Modelling_and_Hypothesis_Testing_FROZEN_SAMPLE_1000.ipynb` | Final modelling and hypothesis-testing notebook                         |


## Current Status

Final capstone report completed.

Completed components include:

- Data collection
- Data cleaning
- Feature engineering
- Exploratory data analysis
- Hypothesis testing
- Regression modelling
- Milestone classification
- Trajectory classification
- Final report preparation
- GitHub reproducibility documentation


## Technology Used

The project was developed using Python and Jupyter notebooks. Major libraries/packages include:

- pandas and NumPy for data processing
- pathlib for file-path handling
- scikit-learn for preprocessing, regression, classification, pipelines, and model evaluation
- statsmodels for nested OLS regression and ANOVA hypothesis testing
- matplotlib and seaborn for EDA visualisation



cat > README.md <<'EOF'
# ML-Driven Talent Identification in Youth Chess

...your full README content...

## Author

**Arun Kumar**  
QM640: Data Analytics Capstone  
Walsh College  
May 2026
EOF



