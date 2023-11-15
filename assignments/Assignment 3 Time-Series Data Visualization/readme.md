# Time-Series Visualization of Local Monthly Temperatures

## Goal

Create a time-series visualization of local monthly temperatures over a few years using data from the Telangana Temperature Data (2013-2017).

### Data Source

[Link to Dataset](https://data.telengana.gov.in/dataset/telengana-temperature-data-2013-2017)

### Data Acquisition

You can either directly download the Maximum and Minimum datasets from the provided URL or use the following Python API requests to get the datasets as Pandas dataframes:

```python
import requests
import pandas as pd

# Query metadata from the dataset URL
r = requests.get("https://data.telangana.gov.in/api/1/metastore/schemas/dataset/items/62a1cc18-7613-460b-a0b1-4b71c78fa1ce")
dataInfo = r.json()

# Use the URLs listed in the metadata to read_csv
df_max = pd.read_csv(dataInfo["distribution"][0]["downloadURL"])
df_min = pd.read_csv(dataInfo["distribution"][1]["downloadURL"])
```

### Data Preparation and Cleaning

Extract the data rows corresponding to Medchal district and Kapra Mandal from the data frames. Transpose the table columns into rows and rows into columns. Convert months and year data to Pandas Datetime format.

### Data Visualization

Create line plots using either Plotly Express or Seaborn to show the minimum and maximum temperatures for the months and years available in the dataset.

### Instructions to Run

1. Download the datasets from the provided URL or use the API requests to fetch the data.
2. Run the data preparation and cleaning code to extract relevant data and format it properly.
3. Run the data visualization code to generate line plots for minimum and maximum temperatures.

### Sample Visuals

![Sample Plot - Plotly Express](https://github.com/himanshushukla12/Data_Visualization/blob/main/lab3/seaborn_plot.png?raw=true)
![Sample Plot - Seaborn](https://raw.githubusercontent.com/himanshushukla12/Data_Visualization/main/lab3/seaborn_plot.png)

**Note:** Concepts covered in this assignment will be discussed during the practice session in Week 4.
