# Task5_Cleaning
# Task 5 — House Prices Dataset Cleaning (Pandas)

This repository contains a complete **data cleaning workflow** for a **House Prices dataset** using **Python (Pandas, NumPy)**.  
The goal is to demonstrate how Python can replace manual Excel cleaning for large datasets in a reproducible way.

---

## Tools & Environment
- **Primary:** Google Colab (free)
- **Alternatives:** Jupyter Notebook, Kaggle Notebooks
- **Libraries:** `pandas`, `numpy`

---

## Dataset
- **Input file:** `Bangalore.csv` (House Prices dataset)

---

## Cleaning Steps Performed
1. **Loaded dataset** using `pd.read_csv()`
2. **Checked structure** using:
   - `df.head()`
   - `df.info()`
3. **Detected missing values** using `df.isnull().sum()`
4. **Handled missing values**:
   - Numeric columns → filled with **median**
   - Categorical columns → filled with **mode**
5. **Removed duplicates** using `df.drop_duplicates()` and verified before/after row count
6. **Converted datatypes** (example: date-like columns to `datetime` if present)
7. **Feature engineering**:
   - Created `Price_Band` (Low / Medium / High) using quantile binning **if a price column exists**
8. **Exported cleaned dataset** to `cleaned_data.csv`

---

## Repository Files
- `Task5_Cleaning.ipynb` — Notebook with code + 5–10 markdown notes
- `cleaned_data.csv` — Final cleaned dataset output
- `README.md` — Project documentation

---

## How to Run

### Option 1: Google Colab
1. Open Google Colab
2. Upload:
   - `Task5_Cleaning.ipynb`
   - `Bangalore.csv`
3. Run all cells
4. Download `cleaned_data.csv` from the Files panel or via the notebook download cell

### Option 2: Jupyter Notebook (Local)
```bash
pip install pandas numpy
jupyter notebook
