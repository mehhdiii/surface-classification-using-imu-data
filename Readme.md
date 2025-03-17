
# ML Pipeline for Surface Classification Based on IMU data

## Team
Mehdi Raza Khorasani & Ozan Pali

## Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Pipeline Overview](#pipeline-overview)
- [Data Exploration](#data-exploration)
- [Data Preprocessing](#data-preprocessing)
- [Data Visualization](#data-visualization)
- [Class Imbalance & Evaluation Metrics](#class-imbalance--evaluation-metrics)
- [Machine Learning Models](#machine-learning-models)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Introduction
This project aims to develop a machine learning pipeline for classifying different surface types using IMU sensor data. The dataset consists of non-linear and imbalanced features, making classification a challenging task. The project applies multiple classifiers and evaluates their performance using appropriate metrics.

## Dataset
The dataset contains input features (X) and labels (y). The data is highly non-linear and exhibits class imbalance. The primary goal is to process this data effectively and build robust classification models.

## Installation
To set up the project, you can use locally hosted jupyter backend or colab/kaggle.

## Pipeline Overview
The pipeline consists of the following steps:
- Data exploration and preprocessing
- Splitting the dataset into training and testing subsets
- Visualizing the data
- Training multiple classifiers (LGBM, KNN, Gradient Boosting, Random Forest)
- Evaluating performance using accuracy, precision, recall, and F1-score

## Data Exploration
The dataset was analyzed for missing values and inconsistencies. The conclusion was that the data is not sparse and is ready for further processing.

## Data Preprocessing
- **Scaling Features (X):** The features were standardized to have zero mean and unit variance, ensuring fair distance-based comparisons.
- **Label Encoding (y):** Labels were converted into numerical format to be compatible with machine learning algorithms.
- **Train/Test Split:** The dataset was divided into 80% training and 20% testing sets.

## Data Visualization
- **Class Distribution:** The dataset exhibits class imbalance, where certain surface types have significantly fewer samples.
- **Feature Distribution:** PCA and t-SNE were applied to visualize feature separability, but the data remains highly non-linear and difficult to separate.

## Class Imbalance & Evaluation Metrics
- Due to class imbalance, accuracy alone is not a reliable metric.
- Instead, precision, recall, and F1-score were used for model evaluation.
- **Metric Definitions:**
  - *Precision:* Measures how many predicted positive cases are actually positive.
  - *Recall:* Measures how many actual positive cases were correctly identified.
  - *F1-Score:* A balanced measure that considers both precision and recall.
  - *Confusion Matrix:* Provides a breakdown of correct and incorrect predictions.

## Machine Learning Models
The following models were implemented:
- **Random Forest:** An ensemble method combining multiple decision trees for robust classification.
- **Gradient Boosting:** Sequentially improves weak learners by minimizing residual errors.
- **LightGBM (LGBM):** A faster and more efficient variant of gradient boosting.
- **K-Nearest Neighbors (KNN):** A distance-based algorithm relying on the majority class of neighbors.

## Results
- **Best Performing Models:** Random Forest and LGBM
- **Performance Metrics:**
  - *Accuracy:* ~97%
  - *Precision:* ~97%
  - *Recall:* ~97%
  - *F1-Score:* ~97%

## Contributing
Contributions are welcome! Please follow these steps:
1. Fork the repository
2. Create a new branch (`git checkout -b feature-branch`)
3. Commit your changes (`git commit -m 'Add feature'`)
4. Push to the branch (`git push origin feature-branch`)
5. Open a Pull Request
