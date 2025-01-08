# Comparing Classifiers: Insights on Test Sizes & Accuracy

## Overview
This project evaluates and compares the performance of five supervised learning classifiers—Random Forest, Support Vector Machines (SVMs), Logistic Regression, K-Nearest Neighbors (KNN), and Decision Trees—across four binary classification datasets. The analysis highlights the relationship between test sizes and model accuracy, providing insights into trends in machine learning performance metrics.

## Features
- **Datasets**: Analysis was conducted on datasets sourced from the UCI Machine Learning Repository. These include the Obesity, Student, Credit Clients, and Bank Marketing datasets, preprocessed for binary classification tasks.
- **Classifiers**: Models underwent Platt Scaling and Standard Scaling (where applicable) to normalize features and calibrate probability outputs.
- **Cross-Validation**: Hyperparameters were tuned using GridSearchCV with 5-fold cross-validation to ensure robust evaluations.
- **Metrics**: Performance was measured using accuracy scores for training, validation, and testing datasets.
- **Data Splits**: Each dataset was evaluated across three train/test splits—80/20, 50/50, and 20/80—to observe trends in performance as the training data size increases.

## Key Findings
- **Best Classifier**: Random Forest consistently outperformed other classifiers, achieving the highest mean accuracy across datasets and data splits.
- **Scaling & Calibration**: Applying Standard Scaling improved the performance of SVMs, KNN, and Logistic Regression, while Platt Scaling enhanced probabilistic outputs for fair comparisons.
- **Impact of Test Size**: Smaller test sizes (e.g., 20%) generally resulted in slightly better accuracy scores, but performance differences across splits were minimal.

## Results Summary
| **Classifier** | **Mean Accuracy (All Datasets)** |
|----------------|----------------------------------|
| Random Forest  | 0.837                            |
| SVM            | 0.835                            |
| Logistic Regression | 0.833                        |
| Decision Trees | 0.831                            |
| KNN            | 0.819                            |

## How to Run
1. **Preprocessing**: Use the provided preprocessing pipeline to encode categorical features and split datasets into training and testing sets.
2. **Model Training**: Train models using the `train_and_evaluate` function, which handles hyperparameter tuning, scaling, and calibration.
3. **Analysis**: Visualize results using the included plotting utilities, which generate bar charts comparing classifier performance across datasets and splits.

## References
This project builds on the insights from:
- Caruana, R., & Niculescu-Mizil, A. (2006). *An Empirical Comparison of Supervised Learning Algorithms*. [ICML 2006](https://doi.org/10.1145/1143844.1143865).

For dataset details and code usage, see the [project paper](https://github.com/kshtwr/Evaluating-Classifiers/blob/main/Final%20Paper%20-%20Comparing%20Classifiers.pdf).

