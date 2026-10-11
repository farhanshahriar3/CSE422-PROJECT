# CSE422 Bank Marketing Project

Machine learning analysis of the bank marketing dataset for CSE422. The project explores the data, prepares mixed numerical and categorical features, compares several classification models, and evaluates K-Means clustering against the subscription target.

## Project Contents

- `CSE422_PROJECT_Final.ipynb`: Complete analysis notebook.
- `Bank Marketing.csv`: Dataset used by the notebook.
- `CSE422_Project_Report.pdf`: Written project report.

## Analysis Workflow

The notebook includes:

1. Dataset inspection and exploratory visualizations.
2. Duplicate detection and removal.
3. Treatment of `unknown` values as missing data.
4. Mean imputation and standardization for numerical features.
5. Most-frequent imputation and one-hot encoding for categorical features.
6. An 80/20 stratified train-test split.
7. Evaluation of K-Nearest Neighbors, Decision Tree, Logistic Regression, and Neural Network classifiers.
8. K-Means clustering with an elbow-method review of cluster count.

The target column is `y`, encoded as `0` for `no` and `1` for `yes`.

## Setup

Create and activate a virtual environment, then install the dependencies:

```bash
python -m venv .venv
```

Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
```

macOS/Linux:

```bash
source .venv/bin/activate
python -m pip install -r requirements.txt
```

Open `CSE422_PROJECT_Final.ipynb` in Jupyter Notebook, JupyterLab, or VS Code and run the cells in order.

## Notebook Path Note

The notebook currently loads the dataset from `/content/Bank Marketing.csv`, which is a Google Colab path. When running locally, change that line to:

```python
df = pd.read_csv("Bank Marketing.csv")
```

## Reproducibility

The train-test split and model initialization use `random_state=42` where applicable. Reported results can still vary slightly with library versions and execution environments.

## License

This repository is an academic project. Verify the dataset's original terms before redistributing it outside this repository.