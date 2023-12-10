# Lung Cancer Fatality Prediction
### Authors: Uku Kangur, Jaan Märten Huik

## Goal and motivation

The primary motivation behind this project is to address the critical challenge of predicting one-year mortality in lung cancer patients, a significant issue in healthcare. Lung cancer, due to its complex nature and high mortality rate, requires advanced predictive models for better treatment planning and patient care. The goal is to develop and validate a machine learning model that can accurately predict the likelihood of mortality within a year based on patients' medical intervention trajectories. Another important aspect is to solve this efficiently - medical data can be noisy, thus we must employ different feature selection methods to aid our model perform better.

## Structure of the repository

We employed several methods to arrive at a solution. Each method was split into a separate document, to aid interpreting results easier. The code files (in the form of Jupyter notebooks) found are the following:

* RandomForest Baseline: **RF_Baseline_Untuned.ipynb**
* Tuned RandomForest with Hyper-Parameter Selection: **Tuned_RF_Hyperparam_Selection.ipynb**
* Tuned RandomForest with First Interventions Only: **Tuned_RF_First_Interventions.ipynb**
* Tuned RandomForest Dropping Binary Correlated Features: **Tuned_RF_Drop_Binary_Correlated.ipynb**
* Tuned RandomForest Dropping Weighted Correlated Features: **Tuned_RF_Drop_Weighted_Correlated.ipynb**
* Tuned RandomForest Dropping 'Measurements' Interventions: **Tuned_RF_Drop_Measurements.ipynb**
* Tuned RandomForest with SHAP-Based Feature Selection: **Tuned_RF_SHAP_Feature_Selection.ipynb**
* Tuned RandomForest with Variance-Based Feature Selection: **Tuned_RF_Variance_Feature_Selection.ipynb**
* K-Nearest Neighbours Sanity Check: **KNN_Sanity_Check_Model_Selection.ipynb**

In addition, the repository contains the following data files:

* First dataset, used for developing the solution: **synthetic_data_lung_cancer.csv**
* Second dataset, used to check generalizability of the solutions: **synthetic_data_pca.csv**
* First dataset after turing interventions into features and normalizing weights per subject: **wide1.csv**
* Second dataset after turing interventions into features and normalizing weights per subject: **wide2.csv**
* First dataset after turning intervention into features and binarizing the weights: **wide_data_binary_1.csv**

## Running the code

The code is rather straightforward to run - Just open the code you wish to employ and run the code. We note that some code files might take longer to run than others (but no file should take longer than 30 mins). Either way, the Jupyter notebooks in the repository have the outputs saved so you do not need to re-run the code to inspect how it ran.
