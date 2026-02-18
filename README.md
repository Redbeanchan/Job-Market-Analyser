# Notebooks - Job Market Analysis

This folder contains the notebook-based workflow for the EGT305 Job Market Analyser project.

The notebooks are designed for:
- quick exploratory analysis and write-up (`BDeda.ipynb`)
- streamlined non-Spark cleaning + modeling (`nonspark_cleaning_model.ipynb`)
- streamlined Spark cleaning + modeling (`spark_cleaning_model.ipynb`)

Use them to compare non-Spark vs Spark performance and support Parts 2-5 of the assignment.

## Files

- `BDeda.ipynb` - main EDA notebook and report-style interpretation
- `nonspark_cleaning_model.ipynb` - focused Pandas + scikit-learn pipeline
- `spark_cleaning_model.ipynb` - focused PySpark pipeline
- `requirements.txt` - notebook dependencies

## Setup (Windows PowerShell)

From this `Notebooks` folder:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
pip install -r requirements.txt
python -m ipykernel install --user --name job-market-notebooks --display-name "Python (job-market-notebooks)"
```

Then start Jupyter:

```powershell
jupyter notebook
```

In Jupyter, select kernel: `Python (job-market-notebooks)`.

## Data paths

These notebooks expect the assignment CSVs as inputs. Update file paths inside notebook cells if your CSV location is different.

Example source files:
- `Employee_dataset.csv`
- `Employee_salaries.csv`

## Run order

1. Run `BDeda.ipynb` for analysis narrative and conclusions.
2. Run `nonspark_cleaning_model.ipynb` for non-Spark benchmark metrics.
3. Run `spark_cleaning_model.ipynb` for Spark benchmark metrics.

## Spark note

PySpark requires Java (JDK 17 recommended). If Spark fails to start, make sure `JAVA_HOME` is set.

## What to commit from this folder

Recommended:
- `BDeda.ipynb`
- `nonspark_cleaning_model.ipynb`
- `spark_cleaning_model.ipynb`
- `requirements.txt`
- `README.md`

Usually do not commit:
- `.venv/`
- `.ipynb_checkpoints/`
- `.html` exports (unless specifically required)

