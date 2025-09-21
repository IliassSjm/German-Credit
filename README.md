# German Credit Risk Prediction Model

## Description

This project aims to develop a machine learning model to predict credit risk based on the German Credit dataset. The objective is to determine whether a loan applicant poses a risk by analyzing various financial and demographic characteristics.

The model uses a historical dataset to predict the probability that a new applicant represents a credit risk, allowing financial institutions to make informed decisions about granting loans.

---

## Dataset

The German Credit dataset contains 4,000 observations with 21 variables, including:

-   **Demographic variables**: Age, sex, residence status
-   **Financial variables**: Loan amount, duration, credit history, existing savings
-   **Behavioral variables**: Loan purpose, employment status, collateral
-   **Target variable**: Risk (Risk/No Risk)

### Class Distribution:
-   **No Risk**: ~67% of cases
-   **Risk**: ~33% of cases

---

## Installation

### Prerequisites

-   Python 3.8+
-   Jupyter Notebook

### Installation Instructions

1.  Clone the repository:
    ```bash
    git clone <REPOSITORY_URL>
    cd German-Credit-main
    ```

2.  Install the dependencies:
    ```bash
    pip install -r requirements.txt
    ```

3.  Launch Jupyter Notebook:
    ```bash
    jupyter notebook
    ```

4.  Open the `notebooks/ML2project.ipynb` file and run all the cells.

---

## Usage

To use this project:

1.  **Exploratory Analysis**: The notebook begins with a comprehensive data analysis featuring visualizations and descriptive statistics.

2.  **Data Preparation**:
    -   Outlier detection and handling
    -   Analysis of variable distributions
    -   Statistical tests (Chi-squared) to evaluate the independence of variables

3.  **Modeling**:
    -   Uses the `HistGradientBoostingClassifier` from scikit-learn
    -   Hyperparameter optimization with Optuna
    -   Stratified cross-validation

4.  **Evaluation**: The model is assessed using performance metrics and a custom cost metric.

---

## Results

### Custom Cost Metric

The project uses a custom cost metric that takes into account:
-   Costs associated with false positives and false negatives
-   The real-world vs. training distribution of risk classes
-   The loan amount in the cost calculation

### Model Performance

The `HistGradientBoostingClassifier` model, optimized with Optuna, demonstrated excellent performance:
-   Optimization based on cross-validation
-   Use of a custom cost metric to reflect economic reality
-   Class balancing with sample weights

### Important Features

The analysis revealed that the most important features for prediction are:
-   **Checking account status** (CheckingStatus)
-   **Credit history** (CreditHistory)
-   **Loan amount** (LoanAmount)
-   **Loan duration** (LoanDuration)
-   **Loan purpose** (LoanPurpose)

---

## Project Structure