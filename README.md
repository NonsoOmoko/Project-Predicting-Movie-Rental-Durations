# DVD Rental Length Prediction Project

## Overview

This project aims to predict the number of days a customer will rent a DVD based on various features provided by a DVD rental company. The goal is to develop a regression model that achieves a mean squared error (MSE) of 3 or less on a test set, aiding the company in efficient inventory planning.

## Data

The dataset `rental_info.csv` contains the following features:
- `rental_date`: The date (and time) the customer rents the DVD.
- `return_date`: The date (and time) the customer returns the DVD.
- `amount`: The amount paid by the customer for renting the DVD.
- `amount_2`: The square of `amount`.
- `rental_rate`: The rate at which the DVD is rented.
- `rental_rate_2`: The square of `rental_rate`.
- `release_year`: The year the movie being rented was released.
- `length`: Length of the movie being rented, in minutes.
- `length_2`: The square of `length`.
- `replacement_cost`: The cost to replace the DVD.
- `special_features`: Any special features the DVD has, such as trailers or deleted scenes.
- Dummy variables for movie ratings: `NC-17`, `PG`, `PG-13`, `R`.

## Project Structure

- `rental_info.csv`: The dataset containing DVD rental information.
- `dvd_rental_prediction.ipynb`: Jupyter notebook containing the code for data exploration, preparation, and model building.
- `README.md`: This file.

## Steps and Methodology

### 1. Data Exploration and Preparation
- Import libraries and read the data.
- Calculate rental length in days.
- Create dummy variables for special features.

### 2. Data Splitting
- Separate the DataFrame into feature and target sets.
- Split the data into training and test sets.

### 3. Lasso Regression
- Create and train a Lasso regression model.
- Perform feature selection using Lasso coefficients.
- Perform OLS regression on the selected features.

### 4. Random Forest Regression
- Define the hyperparameter space for Random Forest.
- Perform Randomized Search CV to find optimal hyperparameters.
- Train the Random Forest model with optimal hyperparameters.
- Evaluate the model performance.

## Results

- The OLS regression with Lasso feature selection achieved an MSE of 4.85.
- The Random Forest model achieved an MSE of 2.16, making it the better model for predicting DVD rental lengths.

## Usage

1. Clone the repository:
   ```sh
   git clone https://github.com/NonsoOmoko/Project-Predicting-Movie-Rental-Durations.git
