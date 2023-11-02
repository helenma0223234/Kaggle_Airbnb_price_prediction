# Project 1 Part 1 Write-Up: Airbnb Price Regression Project

## By Yuchuan Ma and Shay McBride

### Introduction
This project aims to construct a regression model to estimate the prices of Airbnb listings in New York City using various relevant factors. The process involves data analysis, preprocessing, modeling, and evaluation. This write-up provides a comprehensive overview of the project, outlining data insights, data processing, modeling decisions, and performance assumptions.

### Data
#### Dataset Description
The dataset contains information about Airbnb listings in New York City from 2008 to 2019. It consists of 18 columns, including both feature and target variables.

#### Data Exploration
Key insights from initial data exploration:
- Most columns have no missing values except for the license column.
- The dataset includes a mix of categorical and numeric columns.

#### Data Samples
Here are three selected data samples with observations for each.

[Data samples included here...]

#### Columns for Consideration
- `room_type`: Expected to have a considerable influence on listing prices.
- `number_of_reviews`: Shows a slight correlation with the price.
- `neighbourhood_group`: Indicates the listing price to some extent.

### Methods
#### Data Preprocessing
- Log Transformation: To address the right-skewed distribution, a log transformation was applied to the price, resulting in a new variable, `price_log`.
- Categorical Encoding: Columns were encoded using Label Encoding for modeling.
- Feature Selection: Certain columns were excluded as they did not significantly contribute to predictive power.
- Multicollinearity Check: No significant multicollinearity was detected.

#### Model Building
**Model 1**
- Used Linear Regression with selected features.
- Trained on the training dataset and assessed using performance metrics such as RMSE and R-squared.

**Model 2**
- Utilized a Linear Regression model after performing specific transformations and feature engineering.

### Results
#### Model Evaluation
- Model 1 achieved an RMSE of approximately 0.515 with a R-squared value of 0.397.
- Model 2 achieved an RMSE of around 0.510 with a R-squared value of 0.428.

#### Prediction on Test Data
Predictions were made on the test dataset, and the results were saved to a CSV file, achieving a score of 128.87954. Model 2 improved this to 126.71580.

### Future Work
- **Feature engineering:** Exploring additional features that might impact the price.
- **Model expansion:** Considering other regression models like Lasso regression or Random forest regression.
