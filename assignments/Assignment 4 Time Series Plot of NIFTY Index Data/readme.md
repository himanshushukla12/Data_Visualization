# NSE Market Data Analysis

## Goal

The goal of this analysis is to access live NSE (National Stock Exchange) market data using the `nsepython` package and compare the relative changes of three NIFTY index funds over the last 9 years.

## Details

### Data Acquisition Component

- Install the `nsepython` package using the following command:
  ```bash
  pip install nsepython
  ```

- Use the `index_total_returns` function from `nsepython` for the following index funds: NIFTY 50, NIFTY BANK, NIFTY IT.
- Acquire historical index data for the period:
  - Start Date: "01-May-2014"
  - End Date: "10-Sept-2023"
- Refer to the [nse-python documentation](https://unofficed.com/nse-python/documentation/) for more details.

### Data Cleaning and Data Preparation Component

- Compute the relative percent change in the index return value from the start date for every acquired timeseries index data.
  - Use the formula: \( \frac{100 \times (\text{Return at the date of interest} - \text{Return at the start date})}{\text{Return at the start date}} \)

- Combine the updated index data into a single data frame.
- Rename the columns to distinguish the relative percent change data for the three index funds.

### Data Visualization

- Use either Plotly Express or Seaborn to create line plots on a single chart.
- Compare the relative changes of NIFTY 50, NIFTY BANK, and NIFTY IT over the specified period.

## Instructions to Run

1. Install the required packages:
   ```bash
   pip install nsepython plotly seaborn pandas
   ```

2. Run the provided Python script to perform data acquisition, cleaning, and visualization.

## Sample Plots

Sample plots for reference are attached to this readme.

Feel free to explore and analyze the data further based on your requirements.
