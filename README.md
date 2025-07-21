# Feature Engineering Pipelines for RNA-Seq-Based Breast Cancer Prediction

This repository contains code and notebooks for a machine learning study comparing different feature engineering pipelines for early breast cancer prediction using RNA-Seq gene expression data from TCGA and GTEx.

## 🔬 Project Overview

- **Data Sources**: TCGA (cancer) and GTEx (benign)
- **Classifier**: Random Forest
- **Pipelines**:
  - **Pipeline 1**: Random gene selection
  - **Pipeline 2**: ANOVA F-test
  - **Pipeline 3**: ANOVA F-test + PCA

The goal is to evaluate how different feature engineering techniques affect model performance, interpretability, and generalization.

## 🗂 Folder Structure

```
data/
  initial/                      # Raw and split datasets from TCGA and GTEx
  interim/                      # Preprocessed training/testing sets

pipeline_01/                    # Outputs from Pipeline 1 (Random features)
pipeline_02/                    # Outputs from Pipeline 2 (ANOVA F-test)
pipeline_03/                    # Outputs from Pipeline 3 (ANOVA + PCA)

models/                         # Trained model files
reports/                        # Metrics and evaluation reports

00_raw_data_file_pre-processing.ipynb
01_pipeline_01.ipynb
02_pipeline_02.ipynb
03_pipeline_03.ipynb
```
**Note:** The `data/` folder is not included in this repository due to size limitations.  
Researchers interested in accessing the dataset structure or sample files may contact the author for more information.


## 📊 Results Summary

All three pipelines achieved perfect classification on an independent test set:
- **Accuracy**, **Precision**, **Recall**, **F1 Score**, **Specificity**, and **AUC**: 1.0000
- No false positives or false negatives were observed.

## ⚙️ Requirements

Install dependencies with:

```bash
pip install -r requirements.txt
```

Minimum required packages:
- Python 3.8+
- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn

## 🚀 How to Run

1. Run data preparation:
   - `00_raw_data_file_pre-processing.ipynb`
2. Run classification pipelines:
   - `01_pipeline_01.ipynb`
   - `02_pipeline_02.ipynb`
   - `03_pipeline_03.ipynb`

Each notebook is self-contained and outputs results, metrics, and visualizations.

## 📄 License

This project is licensed under the [MIT License](LICENSE).  
Feel free to use, adapt, and cite with attribution for academic purposes.
