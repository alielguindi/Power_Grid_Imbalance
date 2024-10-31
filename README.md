# Grid Imbalance Prediction Project

## Overview

This project focuses on predicting the directionality and magnitude of the Swiss power grid imbalance using a combination of time series models and machine learning algorithms. The goal is to forecast the imbalance at time \( t+1 \), leveraging data from Swissgrid as well as engineered features for improved accuracy.

## Repository Structure

- **control-area-balance-2024.xlsx**: The dataset obtained from [Swissgrid](https://www.swissgrid.ch/en/home/customers/topics/energy-data-ch.html#imbalance-of-the), containing data on grid imbalances, market prices, and other grid metrics.

- **notebook.ipynb**: A Jupyter Notebook containing the code for the entire project. This notebook performs the following:
  - Data preprocessing and feature engineering, including lagged features, rolling statistics, and interaction terms.
  - Exploratory data analysis (EDA) and visualization.
  - Model training using time series models (ARIMA + GARCH) and machine learning models (Logistic Regression, Random Forest, XGBoost).
  - Evaluation and comparison of models based on directional accuracy and feature importance.

- **report.pdf**: A comprehensive report with:
  - A quick introduction to the project goals and methodologies.
  - Results for each model, including model accuracy and feature importance.
  - A conclusion summarizing the findings and discussing the potential benefits of using tree-based models (Random Forest and XGBoost) over traditional time series models in this context.

## Feature Engineering

The project includes extensive feature engineering to enhance the prediction capability of machine learning models. Key engineered features include:
- **Lagged Features**: Hourly and weekly lags for all main variables to capture temporal dependencies.
- **Rolling Statistics**: Rolling means and standard deviations to represent short-term trends and volatility.
- **Interaction Terms**: Features capturing the interaction between imbalance values and market prices.
- **Time-Based Features**: Indicators for business hours, weekends, and time of day to account for temporal patterns in grid behavior.
- **Other Aggregates**: Features such as cumulative imbalance and ratios of certain metrics over time.

## Results Summary

The results demonstrate that tree-based models (Random Forest and XGBoost) show superior performance in predicting the imbalance direction compared to logistic regression and traditional time series approaches. Feature importance analysis further highlights the utility of specific lagged and rolling features in improving model accuracy.

## Installation and Usage

1. **Requirements**: Ensure Python 3.x is installed with required packages listed in `requirements.txt`.
2. **Data**: Place `control-area-balance-2024.xlsx` in the same directory as the notebook.
3. **Run the Notebook**: Open `notebook.ipynb` and execute each cell to reproduce the analysis and results.
4. **View the Report**: Refer to `report.pdf` for a detailed summary of the project.

## Conclusion

This project highlights the potential of Time series models, machine learning models, especially Random Forest and XGBoost, in accurately predicting the direction of grid imbalances using engineered features derived from grid data. The intent is that these predictive signals could be valuable for power and gas traders (given the similarities between gas and elec-
tricity markets) to take positions or hedge based on the forecasted imbalance direction for t + 1. Trading strategies can be developed around these signals to optimize profit and loss (P&L) outcomes




Please reach out if you have any questions or need further assistance.
