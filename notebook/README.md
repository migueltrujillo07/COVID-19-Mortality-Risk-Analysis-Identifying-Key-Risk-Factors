# 📓 Notebooks Overview

This directory contains the main analysis notebooks for the **COVID-19 Mortality Risk Factors** project.  
Each notebook corresponds to a specific phase in the data analysis pipeline, following best practices in data science and epidemiological analysis.

---

## 📘 01. Data Overview

**Objective**  
Provide an initial understanding of the dataset structure, scope, and limitations before any analytical processing is performed.

**Key aspects covered**
- High-level inspection of dataset size and dimensionality.
- Identification of relevant demographic, clinical, and outcome-related variables.
- Detection of data quality issues such as missing values, mixed data types, and malformed records.
- Verification of the temporal scope, confirming that the analysis focuses on records from the year 2021.
- Initial observations on how mortality information is encoded through the `FECHA_DEF` field.

> **Note**  
> Due to formatting inconsistencies and file size constraints, a minimal ingestion-level cleaning step was required to load and inspect the dataset. These steps were strictly technical and did not involve analytical transformations or variable engineering.

---

## 🧹 02. Data Cleaning and Preprocessing

**Objective**  
Transform the raw dataset into a clean, consistent, and analysis-ready format.

**Key aspects covered**
- Robust data ingestion strategies for a dataset exceeding 14 million records under limited memory conditions.
- Resolution of CSV parsing issues caused by malformed rows.
- Standardization and normalization of data types for clinical and demographic variables.
- Handling of special encodings for missing or unknown values (e.g., `"9999-99-99"`).
- Creation of a binary mortality outcome variable (`DEATH`) derived from the date-of-death field.
- Export of the cleaned dataset in Parquet format to ensure efficient reuse and reproducibility.

---

## ⚙️ 03. Exploratory Data Analysis

**Objective**  
Explore the cleaned dataset to identify patterns, distributions, and initial relationships between variables.

**Key aspects covered**
- Descriptive statistics for demographic and clinical variables.
- Analysis of mortality distributions across age, sex, and patient type.
- Visualization of key variables to identify trends and potential risk factors.
- Initial insights guiding deeper risk factor analysis.

---

## 📊 04. Risk Factor Analysis

**Objective**  
Assess the association between clinical risk factors and patient mortality.

**Key aspects covered**
- Comparative analysis of mortality rates across comorbidities.
- Stratified analysis by age group and sex.
- Identification of high-risk patient profiles based on combinations of factors.
- Interpretation of results within an epidemiological context.

---

## 📝 05. Conclusions

**Objective**  
Summarize findings and contextualize results within the scope of the project objectives.

**Key aspects covered**
- Synthesis of key insights regarding mortality risk factors.
- Discussion of limitations related to data quality and observational analysis.
- Final conclusions addressing the original research questions.
- Potential directions for future work and model-based extensions.

---

## 🔎 Notes on Reproducibility

- All analytical steps are documented in sequential notebooks.
- Raw data remains unchanged and is stored separately under `data/raw/`.
- Cleaned and processed data is stored under `data/processed/`.
- Figures used in reports and external publications are exported to `reports/figures/`.


- `data/`  
  Cleaned dataset stored in Parquet format.
