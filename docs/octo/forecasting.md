# Forecasting

Octo's forecasting feature enables users to predict their future cloud costs. This functionality is crucial for budget planning and understanding potential future expenditures based on historical data.

The system utilizes an ARIMA+ (Autoregressive Integrated Moving Average) model for these predictions. Currently, the model uses one year of past cost data to generate a forecast for the upcoming year. The forecast data is also integrated into the budget management feature for comprehensive financial planning.

## Viewing Forecasting Data

To view forecasting data in Octo, follow these steps:

1. **Navigate to the Overview Page:**
   * The forecasting data is primarily displayed on the "Overview" page within the cost group.

2. **Adjust the Date Range to Include Future Dates:**
   * The forecast cost will only appear if the selected date range includes future dates.
   * Click on the date range selector.
   * Choose a date range that extends into the future (e.g., select the current month to the end of the month, or a future month).
   * Click "Apply" to update the view.

3. **Identify Forecasted Costs:**
   * Once the date range is adjusted, you will see a "Forecast Cost" line or section, typically colored gray, on the cost chart and in the data table.
   * This "Forecast Cost" represents the predicted future spending.

4. **Understand Grouping Limitations:**
> **Note:**  
> * A text indicator is displayed to inform users that the graph includes forecast data.  
> * There's a forecast data shown in the graph for the current day since the Cost and Usage Report (CUR) is still being processed.

## Technical Background

* **Model Used:** Octo uses the ARIMA+ model from GCP BigQuery ML for cost forecasting.
* **Data Source:** The model is fed with one year of historical cost data to predict one year of future costs.
* **Data Storage:** After prediction, the forecast data is stored in Spanner tables, separated by vendor (e.g., `cover_aws_forecast`, `cover_gcp_forecast`, `cover_azure_forecast`).
* **API:** An API endpoint `costusage` is used to retrieve this data from Spanner and display it in the UI.