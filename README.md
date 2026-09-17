# Hospital Readmission Prediction

This repository presents a machine learning project dedicated to predicting the 30-day readmission risk for hospital patients, leveraging Logistic Regression with L2 regularization.

## Project Objective

The primary objective of this initiative is to develop a robust predictive model capable of identifying patients at an elevated risk of hospital readmission within 30 days post-discharge. Such early identification is crucial for enabling healthcare providers to implement targeted interventions, thereby enhancing patient outcomes and potentially mitigating healthcare expenditures.

## Key Features

-   **Data Ingestion & Preprocessing**: Comprehensive handling of CSV datasets, including the identification and cleaning of missing values. Features are meticulously prepared using `StandardScaler` for numerical attributes and `OneHotEncoder` for categorical variables.
-   **Model Development**: Implementation and comparative analysis of Logistic Regression models, exploring configurations both with and without L2 regularization to assess their impact on predictive performance.
-   **Rigorous Model Evaluation**: Performance assessment using the Receiver Operating Characteristic Area Under the Curve (ROC-AUC). A detailed analysis of False Negatives and False Positives is conducted, emphasizing their significant clinical implications.
-   **Prediction Generation**: The optimally performing model is retrained on the complete training dataset to generate predictions for a new, unseen test set. These predictions are formatted for submission.
-   **Visual Analytics**: Inclusion of an ROC curve plot to visually articulate the performance distinction between the regularized and non-regularized models.

## Technological Stack

-   **Python 3.x**: The foundational programming language for the project.
-   **Pandas**: Utilized for efficient data manipulation and analysis.
-   **NumPy**: Essential for numerical operations.
-   **Scikit-learn**: The core library for machine learning models, preprocessing techniques, and evaluation metrics.
-   **Matplotlib**: Employed for generating high-quality static visualizations.

## Getting Started

To execute this project locally, please follow these instructions:

1.  **Repository Cloning**:
    ```bash
    git clone <repository-url>
    cd hospital-readmission-prediction
    ```
2.  **Dataset Acquisition**: Ensure that `train_df.csv`, `test_df.csv`, and `sample_submission.csv` are present in your project root directory. (Note: These data files are typically sourced separately due to their proprietary or sensitive nature and are not directly included in this repository).
3.  **Dependency Installation**:
    ```bash
    pip install pandas numpy scikit-learn matplotlib
    ```
4.  **Notebook Execution**: Open the primary notebook (e.g., `hospital_readmission_prediction.ipynb`) in a Jupyter environment or Google Colab and sequentially execute all cells.

## Results and Clinical Insights

The accompanying notebook meticulously documents the entire modeling pipeline, providing detailed outputs from each stage, including data cleaning, model training, and performance evaluation. A significant portion of the discussion is dedicated to the clinical ramifications of False Negatives (missed readmissions, representing critical lost opportunities for intervention) versus False Positives (unnecessary follow-up care, incurring additional costs without direct patient benefit). The comparative ROC curve aids in visualizing these trade-offs.

Final prediction outcomes are stored in `submission_simple.csv`.

## Resources

-   **Dataset**: (Specify the source or nature of the `train_df.csv`, `test_df.csv`, and `sample_submission.csv` files, e.g., Kaggle competition, synthetic generation, internal database).
Kaggle Dataset Link :- https://www.kaggle.com/datasets/vanpatangan/readmission-dataset
-   **Scikit-learn Documentation**: Refer to the official documentation for in-depth understanding and usage of modules such as `LogisticRegression`, `StandardScaler`, `OneHotEncoder`, `Pipeline`, `ColumnTransformer`, `roc_auc_score`, `roc_curve`, `confusion_matrix`, and `classification_report`.
-   **Matplotlib Documentation**: For comprehensive guides on plot customization and generation, particularly for ROC curves.
-   **Pandas Documentation**: Consult the official Pandas documentation for advanced data manipulation techniques utilizing `DataFrame` objects, `read_csv`, `get_dummies`, `isna`, `duplicated`, `drop_duplicates`, `reset_index`, and `corr`.
