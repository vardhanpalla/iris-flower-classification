# Iris Flower Classification using Machine Learning

A machine learning classification project that predicts the species of an Iris flower based on its sepal and petal measurements.

## Project Overview

This project uses the classic Iris dataset to classify flowers into three species:

* Setosa
* Versicolor
* Virginica

The project covers the complete machine learning workflow, from exploratory data analysis and preprocessing to model evaluation, cross-validation, hyperparameter tuning, and prediction using a saved model.

## Dataset

The project uses the Iris dataset provided by `scikit-learn`.

The dataset contains:

* 150 samples
* 4 features
* 3 target classes

### Features

* Sepal length (cm)
* Sepal width (cm)
* Petal length (cm)
* Petal width (cm)

### Target Classes

* Setosa
* Versicolor
* Virginica

## Machine Learning Models

Three classification algorithms were evaluated:

1. Logistic Regression
2. K-Nearest Neighbors (KNN)
3. Decision Tree

### Cross-Validation Results

| Model               | Mean Accuracy | Standard Deviation |
| ------------------- | ------------: | -----------------: |
| Logistic Regression |        96.00% |              3.89% |
| KNN                 |        96.00% |              2.49% |
| Decision Tree       |        95.33% |              3.40% |

KNN was selected as the final model because it achieved 96% mean cross-validation accuracy with the lowest variation among the three models.

## Hyperparameter Tuning

Different values of `K` were tested for KNN:

|  K | Mean CV Accuracy |
| -: | ---------------: |
|  1 |           94.67% |
|  3 |           95.33% |
|  5 |           96.00% |
|  7 |           96.00% |
|  9 |           96.00% |
| 11 |           94.67% |

`K = 5` was selected as the final value.

## Final Model Performance

The final KNN model achieved:

**Test Accuracy: 93.33%**

The classification report showed:

| Class      | Precision | Recall | F1-Score |
| ---------- | --------: | -----: | -------: |
| Setosa     |      1.00 |   1.00 |     1.00 |
| Versicolor |      0.83 |   1.00 |     0.91 |
| Virginica  |      1.00 |   0.80 |     0.89 |

The main classification errors occurred between Versicolor and Virginica.

## Project Workflow

```text
Load Dataset
      ↓
Exploratory Data Analysis
      ↓
Train/Test Split
      ↓
Feature Scaling
      ↓
Train Multiple Models
      ↓
Evaluate Models
      ↓
5-Fold Cross-Validation
      ↓
KNN Hyperparameter Tuning
      ↓
Select Final Model
      ↓
Save Model & Scaler
      ↓
Make Predictions
```

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Joblib
* Google Colab

## Project Files

```text
iris-flower-classification/
│
├── iris_classification.ipynb
├── iris_knn_model.pkl
└── iris_scaler.pkl
```

### File Description

* `iris_classification.ipynb` — Complete analysis, model training, evaluation, tuning, and prediction workflow.
* `iris_knn_model.pkl` — Saved trained KNN model.
* `iris_scaler.pkl` — Saved StandardScaler used to preprocess input features.

## How to Run

1. Clone or download this repository.
2. Open `iris_classification.ipynb` in Jupyter Notebook or Google Colab.
3. Run the notebook cells from top to bottom.
4. Use the prediction function to classify new Iris flower measurements.

## Example Prediction

Example input:

```text
Sepal length: 5.1 cm
Sepal width: 3.5 cm
Petal length: 1.4 cm
Petal width: 0.2 cm
```

Prediction:

```text
Setosa
```

## Key Learning Outcomes

Through this project, I practiced:

* Exploratory Data Analysis
* Data preprocessing
* Train/test splitting
* Feature scaling
* Classification algorithms
* Accuracy and classification metrics
* Confusion matrices
* Cross-validation
* Hyperparameter tuning
* Model persistence using Joblib
* Making predictions using a saved ML model
