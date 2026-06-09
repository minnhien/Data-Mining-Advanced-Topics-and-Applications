# Data Mining 2 Project — IMDb Dataset

This repository contains the project developed for the Data Mining: Advanced Topics and Applications course, part of the Master Programme in Data Science and Business Informatics at the University of Pisa.

## Overview

The project conducts an end-to-end data mining analysis on a dataset of 149,531 film records and 1,134 movie revenue time series. The work covers data preparation, outlier detection, imbalance learning, advanced classification, regression, explainability, and time series analysis.

## Main Contributions

### Data Preparation and Outlier Detection

The dataset was cleaned and transformed through missing value handling, feature engineering, categorical encoding, and feature scaling.

For outlier detection, six methods were applied:

- LOF
- LODA
- Isolation Forest
- HBOS
- CBLOF
- ABOD

A **majority voting strategy** was used to identify the final top 1% outliers.
Dimensionality reduction techniques such as PCA and t-SNE were used to visualize outliers and compare the behavior of different algorithms.

### Imbalance Learning

A binary imbalanced classification task was created using the `rating` variable, with a class distribution of approximately **92% vs. 8%**.

Several imbalance handling techniques were compared:

- Random Under Sampler
- Condensed Nearest Neighbors
- Edited Nearest Neighbors
- Tomek Links
- Cluster Centroids
- Random Over Sampler
- SMOTE
- ADASYN
- Class Weight Adjustment
- Decision Threshold Moving

Among the tested methods, **Class Weight Adjustment**, **SMOTE**, and **Cluster Centroids** showed the most relevant trade-offs depending on the goal: balanced performance, better generalization, or higher minority-class recall.

### Advanced Classification and Explainability

A multi-class classification task was developed to predict movie rating classes. The tested models include:

- Logistic Regression
- Support Vector Machines
- Neural Networks
- Random Forest
- AdaBoost
- Gradient Boosting
- XGBoost

Among all classifiers, **XGBoost achieved the best overall performance**, with a macro-average ROC-AUC of **0.78**, showing strong ability to handle complex and overlapping rating classes.

### Explainability

Explainability was performed using **SHAP**, including waterfall and beeswarm plots.

### Advanced Regression

The regression task focused on predicting `averageRating` using multiple input features.

The tested models were:

- Neural Networks
- Random Forest
- Gradient Boosting

**Gradient Boosting achieved the best regression performance**, with the highest R² score of \*_0.3669_

### Time Series Analysis

The time series part analyzed the **100-day revenue lifecycle** of **1,134 films**.

The analysis included:

- K-Means clustering with Euclidean distance and DTW distance
- DBSCAN clustering
- Matrix Profile for motif and discord detection
- KNN classification with Euclidean and DTW distances
- Shapelet-based classification
- ROCKET classifier

The **ROCKET classifier** achieved the best time-series classification performance, outperforming KNN and Shapelets with an accuracy of **52%**.

## Repository Structure

```text
.
├── Advanced Regression.ipynb
├── Ensemble.ipynb
├── ExtremeGradientBoosting.ipynb
├── GradientBoosting.ipynb
├── Imbalance.ipynb
├── Neural_Networks.ipynb
├── Neural_Networks 3layers Drop Out.ipynb
├── SVM.ipynb
├── TS Classification.ipynb
├── TS Clustering DBSCAN.ipynb
├── TS Clustering Kmeans.ipynb
├── TS Matrix Profile.ipynb
├── TS Preprocessing 2.ipynb
├── TS Understanding and Preprocessing.ipynb
├── Project_Do_Nguyen.pdf
└── README.md
```
