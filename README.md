# Lung Cancer Fatality Prediction
### Authors: Uku Kangur, Jaan Märten Huik

## Goal and motivation

The primary motivation behind this project is to address the critical challenge of predicting one-year mortality in lung cancer patients, a significant issue in healthcare. Lung cancer, due to its complex nature and high mortality rate, requires advanced predictive models for better treatment planning and patient care. The goal is to develop and validate a machine learning model that can accurately predict the likelihood of mortality within a year based on patients' medical intervention trajectories. Another important aspect is to solve this efficiently - medical data can be noisy, thus we must employ different feature selection methods to aid our model perform better.

## Structure of the repository

We employed several methods to arrive at a solution. Each method was split into a separate document, to aid interpreting results easier. The code files (in the form of Jupyter notebooks) found are the following:

* RandomForest Baseline: **RF_Baseline_Untuned.ipynb**
* Tuned RandomForest with Hyper-Parameter Selection: **Tuned_RF.ipynb**
* Tuned RandomForest with First Interventions Only: **Tuned_RF_First_Interventions.ipynb**
* Tuned RandomForest Dropping Binary Correlated Features: **Tuned_RF_Drop_Binary_Correlated.ipynb**
* Tuned RandomForest Dropping Weighed Correlated Features: **Tuned_RF_Drop_Weighed_Correlated.ipynb**
* Tuned RandomForest Dropping 'Measurements' Interventions: **Tuned_RF_Drop_Measurements.ipynb**
* Tuned RandomForest with SHAP-Based Feature Selection: **Tuned_RF_SHAP_Feature_Selection.ipynb**
* Tuned RandomForest with Variance-Based Feature Selection: **Tuned_RF_Variance_Feature_Selection.ipynb**
* Tuned K-Nearest Neighbours (KNN): **Tuned_KNN.ipynb**
* Tuned Support Vector Machine (SVM): **Tuned_SVM.ipynb**

In addition, the repository contains the following original data files:

* First dataset, used for developing the solution: **synthetic_data_lung_cancer.csv**
* Second dataset, used to check generalizability of the solutions: **synthetic_data_pca.csv**

## Running the code

You need to run **RF_Baseline_Untuned.ipynb** before running any other code. The reason for this is simple. That code will turn the intervention histories into machine interpretable datasets (wide1.csv and wide2.csv), which has nornmalized features. In additon it will create the binary version of wide1 called wide_data_binary_1.csv and the feature correlation matrices (both binary and weighed versions). These will be loaded in other methods directly for more efficiency.

After that the code is rather straightforward to run - Just open any program you wish to employ and run the code. We note that some code files might take longer to run than others (but no file should take longer than 30 mins). Either way, the Jupyter notebooks in the repository have the outputs saved so you do not need to re-run the code to inspect how it ran.

NB! Be vary of external libraries used. You might need install some packages (sklearn, numpy, pandas, smote, shap, seaborn).
