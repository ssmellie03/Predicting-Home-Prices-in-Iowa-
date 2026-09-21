# Predicting-Home-Prices-in-Iowa-
Predicting home sale prices in Ames, Iowa using Python, Pandas, and regression models, with time-based validation and model evaluation.
## Project Overview

This project uses residential housing data from Ames, Iowa to build regression models for predicting home sale prices.

The project demonstrates a data science workflow using Python, Pandas, NumPy, and scikit-learn, including data preparation, exploratory data analysis, baseline modeling, regression modeling, and model evaluation.

A time-based train-validation split was used to account for changes in housing prices over time.

## Objectives

* Explore and prepare residential housing data for analysis.
* Establish a baseline for predicting home sale prices.
* Build and compare Linear Regression and Ridge Regression models.
* Evaluate model performance using Mean Absolute Error (MAE) and R².
* Generate predictions for a separate test dataset.

## Dataset

The dataset contains residential property records from Ames, Iowa.

The target variable is:

* **SalePrice** — the sale price of the home.

The dataset also contains features describing characteristics of each property.

## Tools & Technologies

* **Python**
* **Pandas** — data manipulation and analysis
* **NumPy** — numerical computing
* **Matplotlib** — data visualization
* **Seaborn** — data visualization
* **Scikit-learn** — regression modeling and evaluation
* **Jupyter Notebook** — analysis and documentation

## Project Process

### 1. Data Preparation

The housing dataset was loaded and prepared for analysis. The `Yr_Sold` column was converted to a datetime format and used as the DataFrame index.

### 2. Exploratory Data Analysis

I explored the relationship between property characteristics and sale price using data visualizations.

One analysis examined the relationship between **above-ground living area (`Gr_Liv_Area`)** and **sale price (`SalePrice`)**.

### 3. Train-Validation Split

Rather than randomly splitting the data, I used a **time-based split**.

* **Training data:** Homes sold before 2009 — 1,920 observations
* **Validation data:** Homes sold during 2009 — 644 observations

This approach allowed the models to be evaluated using a later time period than the data used for training.

### 4. Baseline

I established a baseline prediction using the mean sale price from the training data.

The baseline was evaluated using **Mean Absolute Error (MAE)**.

This provided a reference point for comparing the regression models.

### 5. Linear Regression

A Linear Regression model was developed using a preprocessing pipeline that included:

* OneHotEncoder for categorical variables
* StandardScaler for feature scaling
* Linear Regression

### 6. Ridge Regression

A Ridge Regression model was also developed using the same preprocessing approach.

The Ridge model used an `alpha` value of 1.0.

### 7. Model Evaluation

The models were evaluated using:

* **Mean Absolute Error (MAE)**
* **R² score**

The validation results were used to compare model performance.

### 8. Test Predictions

The Ridge Regression model was used to generate predictions for a separate test dataset containing 340 observations.

## Key Skills Demonstrated

This project demonstrates experience with:

* Data cleaning and preparation
* Exploratory data analysis
* Data visualization
* Feature preprocessing
* Categorical variable encoding
* Feature scaling
* Regression modeling
* Time-based validation
* Model evaluation
* Python and Pandas
* Jupyter Notebook

## Future Improvements

Potential improvements to this project include:

* Comparing additional regression algorithms
* Performing cross-validation
* Tuning model hyperparameters
* Exploring additional feature engineering techniques
* Further investigating model coefficients and feature relationships
