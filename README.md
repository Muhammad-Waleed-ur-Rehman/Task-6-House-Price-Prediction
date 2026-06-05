# Task-6-House-Price-Prediction
House Price Prediction

# House Price Prediction Analysis

## Task Objective
The primary goal of this project is to build a machine learning model capable of estimating market values for residential properties based on structural and locational features. The focus is on implementing a robust regression pipeline to establish a performance baseline for automated real estate valuation.

## Dataset
*   **Source**: House Price Prediction Dataset
*   **Observations**: 2,000 records with 10 property features.
*   **Features include**: Area (sq. ft.), Bedrooms, Bathrooms, Floors, Year Built, Location (Downtown, Suburban, etc.), Condition, and Garage availability.
*   **Preprocessing**: Applied `StandardScaler` for numerical normalization and `OneHotEncoder` for categorical transformation within a scikit-learn `Pipeline` to ensure data integrity and prevent leakage.

## Models Applied
*   **Algorithm**: Linear Regression.
*   **Approach**: Supervised Machine Learning (Regression).
*   **Data Split**: 80% Training / 20% Testing (`random_state=42`).
*   **Engineering**: Utilized a `ColumnTransformer` to handle mixed data types simultaneously, expanding the feature space to 15 columns for the model.

## Key Results and Findings
*   **Mean Absolute Error (MAE)**: ~$243,242
*   **Root Mean Squared Error (RMSE)**: ~$279,860
*   **Model Performance Insights**:
    *   **High Variance**: The error magnitude is significant relative to the average house price (~$537k), indicating that a simple linear model struggles with the price volatility in this dataset.
    *   **Low Linear Correlation**: Numerical features like `Area` showed low linear correlation with `Price`, suggesting that property value is influenced by complex, non-linear interactions.
