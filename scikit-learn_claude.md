# Scikit-learn Project Context

Welcome to the **scikit-learn** repository. This project focuses on building, training, and evaluating machine learning models using the `scikit-learn` ecosystem for data science and predictive analytics.

## Project Goal
To develop robust, scalable, and reproducible machine learning workflows, from data preprocessing and feature engineering to model training and evaluation.

## Key Principles for AI Assistants
When assisting with this project, please adhere to these guidelines:

1.  **Pipeline-First Approach:** Always prioritize using `sklearn.pipeline.Pipeline` or `ColumnTransformer` to prevent data leakage and ensure reproducible preprocessing steps.
2.  **API Consistency:** Stick to the standard `fit`, `predict`, and `transform` interface. Ensure custom estimators or transformers follow the scikit-learn API contract.
3.  **Data Handling:** Always assume input data is in a format compatible with NumPy/Pandas. Include validation steps to handle missing values or incorrect data types.
4.  **Model Evaluation:** Emphasize rigorous evaluation strategies (e.g., Cross-Validation, StratifiedKFold) over simple train/test splits, especially for imbalanced datasets.
5.  **Performance & Scaling:** Be mindful of computational cost. For large datasets, suggest techniques like batch processing or dimensionality reduction (e.g., PCA, TruncatedSVD).

## Key Components
* `data/`: Datasets for training and inference.
* `models/`: Serialized models (e.g., using `joblib` or `pickle`) and versioning logs.
* `src/`: Modular code for feature engineering, preprocessing, and model training.
* `notebooks/`: Exploratory Data Analysis (EDA) and model prototyping.
* `tests/`: Unit tests for custom transformers and pipeline components.

## Workflow & Standards
* **Version Control:** Use Git LFS for large datasets and model files.
* **Documentation:** Document hyperparameter search spaces and the rationale behind feature selection.
* **Security:** Avoid loading untrusted `pickle` files; emphasize the use of safe formats or robust model serialization practices.
* **Clarity:** If a model's performance is poor, suggest checking for data leakage, feature importance, or hyperparameter tuning (GridSearchCV/RandomizedSearchCV) first.

---
*Last updated: 2026-06-16*
