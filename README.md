# House Price Prediction with Linear Regression

A ML project that builds, trains, and validates a linear regression model to predict house prices based on key features from the Ames Housing dataset.

## Project Overview

This project demonstrates a fundamental machine learning workflow. The primary objective is to predict the sale price of houses using a linear regression model. The process involves loading and cleaning the data, performing feature engineering, splitting the dataset for robust model validation, training the model, and finally generating predictions on an unseen test dataset.

## Dataset Description

The project utilizes the Ames Housing dataset, which is split into two primary files:

* **`task1_train.csv`**: This file contains the training data, including various features (like living area, number of bedrooms, etc.) and the target variable, `SalePrice`.
* **`Task1_test.csv`**: This file contains the testing data. It has the same features as the training set but omits the `SalePrice` column.

## Workflow and Methodology

The Python script follows a structured workflow to ensure reproducibility and clarity.

1.  **Data Loading**: The `task1_train.csv` and `Task1_test.csv` files are loaded into pandas DataFrames.
2.  **Feature Engineering**: A new feature called **`TotalBath`** is created to provide a consolidated measure of all bathrooms. The formula used is:
    `TotalBath = FullBath + 0.5 * HalfBath + BsmtFullBath + 0.5 * BsmtHalfBath`
3.  **Handle Missing Values**: The script fills any missing values in the feature columns (`GrLivArea`, `TotalBath`, `BedroomAbvGr`) with the **median** value from the training set.
4.  **Data Splitting**: The training data is split into an **80% training set** and a **20% validation set**.
5.  **Model Training**: A `LinearRegression` model is trained on the 80% training data.
6.  **Prediction**: The trained model predicts prices for the `Task1_test.csv` dataset.
7.  **Save Output**: The final predictions are saved to a CSV file named **`prediction test.csv`**.

## Installation

To run this project locally, you will need Python and the following libraries installed.

1.  **Prerequisites**:
    * Python 3.x
    * pip (Python package installer)

2.  **Setup**:
    * Clone the repository or download the files into a single directory.
    * Install the required libraries:
        ```sh
        pip install pandas numpy scikit-learn
        ```

### Sample Predictions

The final output file (`prediction test.csv`) contains the predicted sale prices for each house in the test set. Here is a preview of the first 5 predictions:

| Id   | SalePrice     |
|------|---------------|
| 1461 | 105484.73    |
| 1462 | 138318.90    |
| 1463 | 196896.16    |
| 1464 | 194529.55    |
| 1465 | 172013.78    |


## How to Run the Project

1.  Ensure you have completed the **Installation** steps.
2.  Place your `task1_train.csv` and `Task1_test.csv` files in the same directory as your Python script.
3.  Execute the script from your terminal:
    ```sh
    python your_script_name.py
    ```
4.  After the script finishes, you will find the **`prediction test.csv`** file in the project directory.


## File Structure
```
Your project directory should look like this for the script to run correctly:
├── House_price_prediction.ipynb    # The main Python script
├── task1_train.csv                 # Training data
├── Task1_test.csv                  # Testing data
└── prediction_test.csv             # Generated file with predictions
```

## Developed by

**Tara Siddappa Busaraddi**

* **GitHub**: [TaraB287](https://github.com/TaraB287)
* **LinkedIn**: [tarabusaraddi](https://www.linkedin.com/in/tarabusaraddi)

