# Personal Consumption Expenditure Forecasting and Hotel Reviews Analysis

## Assessed Coursework Overview

This project is divided into two parts:

- **Part 1**: Forecasting personal consumption expenditures (PCE) using US seasonally adjusted data. The data is analyzed using three forecasting models: Simple forecasting, Exponential smoothing, and ARIMA.
- **Part 2**: Text analysis of online hotel reviews to identify factors that contribute to customer satisfaction or grievances.

The goal is to apply different modeling techniques to forecast data and evaluate the effectiveness of each model, followed by text analysis to identify topics related to positive and negative hotel reviews.

## Part 1: PCE Forecasting

### 1. Introduction

The goal of this analysis is to forecast personal consumption expenditures using US seasonally adjusted data from 1959 to 2023. Three forecasting methods are used:

- **Simple Forecasting Method**
- **Exponential Smoothing (Holt Method)**
- **ARIMA Model**

The accuracy of each model is evaluated to determine which model provides the best forecast for October 2024.

### 2. Data Description and Preprocessing

The dataset contains monthly expenditure data starting from January 1959 to November 2023. It is evident that the data has a non-linear trend, with a sharp decline around 2020 due to the global pandemic. Missing values are imputed using Stineman interpolation to preserve the non-linear trend of the data.

### 3. Model Building and Evaluation

Three models are applied to the data and evaluated:

- **Simple Forecasting (Drift)**: Used as a baseline model, which does not capture the trend or seasonality effectively.
- **Exponential Smoothing (Holt Method)**: Performed best, effectively capturing the underlying trend in the data.
- **ARIMA Model**: Applied after ensuring stationarity using differencing. An ARIMA(3,2,2) model was fitted.

### 4. Evaluation and Conclusion

Based on Root Mean Squared Error (RMSE) and Mean Absolute Error (MAE), the Holt Exponential Smoothing model performed best. The estimated PCE for October 2024 is **19566.92 USD**.

## Part 2: Hotel Reviews Analysis

### 1. Introduction

The second part involves analyzing a dataset of 10,000 hotel reviews. The task aims to determine factors that positively or negatively influence customer satisfaction.

### 2. Data Preprocessing

After removing non-English reviews and neutral reviews, the data is divided into **positive** (score > 3) and **negative** (score < 3) subsets. The data is further processed into Document Term Matrices (DTM) to explore word frequencies.

### 3. Topic Modeling with LDA

Latent Dirichlet Allocation (LDA) was used to identify underlying topics in both positive and negative reviews. Optimal topic numbers were determined by evaluating multiple metrics, resulting in 14 topics for positive reviews and 11 for negative reviews.

### 4. Top Factors Influencing Reviews

- **Positive Reviews**: The top factors discussed include *Accessibility and Proximity to Transportation*, *Staff and Service Quality*, and *Exceptional Hospitality*.
- **Negative Reviews**: The main topics revolved around *Breakfast and Location Problems*, *General Hotel Issues*, and *Bathroom and Shower Issues*.

### 5. Conclusion

The analysis shows that *location* and *quality of hospitality* are key factors influencing both positive and negative reviews, highlighting the importance of these features in customer satisfaction.

## Getting Started

To replicate the analysis, follow these steps:

1. Clone this repository:
   ```bash
   git clone <repository-url>
   ```
2. Run the analysis scripts for forecasting or text analysis as needed.

## Dependencies

- R (with `imputeTS`, `forecast`, `tm`, `topicmodels`, `ldatuning` packages)
- Python (optional for data visualization)

## License

This project is licensed under the MIT License.

## Acknowledgments

Thanks to the instructors and peers who provided feedback and guidance throughout the coursework.
