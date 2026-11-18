# Hepatocellular Carcinoma (HCC) Survival Prediction

This project explores machine learning models for predicting survival outcomes for patients with hepatocellular carcinoma (HCC). It includes three Jupyter notebooks that implement and evaluate an Extreme Learning Machine (ELM), Support Vector Machine (SVM), and XGBoost, along with the internship report and certificate.

## Project files

- `HCC_ELM.ipynb` — ELM classifier and ensemble experiments.
- `HCC_SVM.ipynb` — SVM pipeline and evaluation experiments.
- `HCC_XG.ipynb` — XGBoost tuning, evaluation, and feature explanations.
- `Internship_Report.pdf` — project report.
- `Certificate_Surya.pdf` — internship certificate.

## Requirements

Use Python 3 with Jupyter Notebook or JupyterLab. The notebooks use common data science libraries including pandas, NumPy, scikit-learn, imbalanced-learn, LIME, and XGBoost. `HCC_ELM.ipynb` and `HCC_XG.ipynb` include setup cells for some dependencies; install any missing packages in your environment before running the notebooks.

For example:

```bash
python -m pip install jupyter pandas numpy scikit-learn imbalanced-learn lime xgboost
jupyter notebook
```

## Dataset
This project uses the HCC dataset from the UCI ML Repository. The dataset itself was collected from the hospital, Centro Hospitalar e Universitario de Coimbra in Portugal. The dataset consists 165 data points and 50 features, of which 17 are clinical features.

The notebooks expect an HCC dataset in CSV format with a target column named `Class`. The CSV is not included in this repository. In the notebook entry cells, the dataset path is currently set to `/content/hcc.csv` (a Google Colab path). Place the dataset there when using Colab, or change the path to the CSV location in your environment.

The notebooks treat `Class` as the label and the remaining columns as input features. Their preprocessing handles `?` values and missing data; some notebooks also scale features, select features, and apply SMOTE with Tomek links to address class imbalance.

## Running the notebooks

1. Obtain the dataset from the project/source that supplied it and check that it has a `Class` column.
2. Open one of the notebooks in Jupyter or Google Colab.
3. Update the dataset path in the final execution cell if needed.
4. Run the notebook from top to bottom. Each notebook performs model fitting and cross-validation, reports evaluation metrics and timing, and includes LIME-based local explanations.

The notebooks are independent; run whichever model you want to examine. They may take time to complete because they include repeated cross-validation and, in some cases, hyperparameter search.

## Notes

- Results depend on the dataset version and the runtime environment.
- LIME explanations describe individual predictions and should be interpreted alongside the model evaluation and clinical context.
- This repository is for an internship project and is not a clinical diagnostic tool.
