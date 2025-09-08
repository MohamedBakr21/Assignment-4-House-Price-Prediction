🏡 Housing Price Classification (Logistic Regression)


📌 Project Overview

-----

#### 1\. Introduction

This project aims to predict the median house values in California districts using a machine learning model. The analysis is based on a dataset containing various demographic and location-based features. The primary goal is to build a robust regression model that can estimate house prices with a reasonable degree of accuracy.

-----

#### 2\. Dataset

The dataset used is `housing (1).csv`, which contains 20,640 entries with 10 features. The key features include:

  * `longitude` & `latitude`: Geographical coordinates of the district.
  * `housing_median_age`: Median age of the houses in the district.
  * `total_rooms` & `total_bedrooms`: Total number of rooms and bedrooms.
  * `population`: The population of the district.
  * `households`: Total number of households.
  * `median_income`: Median income for households in the district.
  * `ocean_proximity`: Proximity to the ocean (a categorical feature).
  * `median_house_value`: The target variable to be predicted.

-----

#### 3\. Methodology

The machine learning pipeline for this project consists of the following steps:

1.  **Data Preprocessing**: The `total_bedrooms` column had missing values, which were imputed using the median value to maintain data integrity.
2.  **Feature Engineering**: Several new features were created to enhance the model's predictive capability, including:
      * `rooms_per_household`
      * `bedrooms_per_room`
      * `population_per_household`
3.  **Categorical Encoding**: The `ocean_proximity` feature was converted into a numerical format using one-hot encoding, a necessary step for most machine learning algorithms.
4.  **Model Training**: A **Random Forest Regressor** model was trained on the preprocessed data. The data was split into training and testing sets to ensure the model's performance was evaluated on unseen data.
5.  **Model Evaluation**: The model's performance was measured using two standard regression metrics:
      * **Root Mean Squared Error (RMSE)**: Measures the average magnitude of the error.
      * **R-squared ($R^2$) Score**: Represents the proportion of variance in the target variable that is explained by the model.

-----

#### 4\. Results

The trained `RandomForestRegressor` model achieved the following performance on the test dataset:

  * **Root Mean Squared Error (RMSE)**: $50356.60
  * **R-squared ($R^2$) Score**: $0.8065$

The R-squared score of approximately 0.81 indicates that the model explains a significant portion of the variance in house prices, demonstrating good predictive performance. The RMSE value suggests that, on average, the model's predictions are within approximately $50,000 of the actual house price.

-----

#### 5\. How to Run the Code

To replicate this analysis, you will need to have Python and the necessary libraries installed.

1.  **Install Dependencies**: Install the required libraries using `pip`.
    ```bash
    pip install pandas scikit-learn numpy
    ```
2.  **Download the Data**: Ensure the `housing (1).csv` file is in the same directory as the script.
3.  **Run the Script**: Execute the Python script.
    ```bash
    python your_script_name.py
    ```

You can find the preprocessed data used for this project in the file named `processed_housing_data.csv`.
