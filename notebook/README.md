## 🧹 Data Ingestion and Cleaning

The raw dataset presented several real-world data quality challenges:

- Malformed CSV rows and inconsistent quotation marks
- Mixed data types across multiple variables
- Non-standard missing value encodings (e.g., `"9999-99-99"`)
- File size constraints exceeding typical memory limits

To address these issues:
- Defensive loading strategies were applied to handle corrupted rows.
- Relevant columns were selected to reduce memory usage.
- Data types were normalized using safe conversion methods.
- A binary outcome variable (`DEATH`) was derived from the date-of-death field.
- The cleaned dataset was stored in **Parquet format** for efficiency and reproducibility.

---

- `02_feature_engineering.ipynb`  
  Construction of derived variables such as age groups and recoded comorbidities.

- `03_exploratory_data_analysis.ipynb`  
  Statistical summaries and visualizations to identify key mortality risk factors.

- `data/`  
  Cleaned dataset stored in Parquet format.
