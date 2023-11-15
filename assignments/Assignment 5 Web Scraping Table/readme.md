# Project Title

## Reproduction of "Killer Quakes" Bar Plot from Sept 10, TOI

### Goal

Reproduce the bar plot "Killer Quakes" from Sept 10, TOI using data from [Our World in Data](https://ourworldindata.org). Acquire the data from two different sources on the Our World in Data website and verify the match with the sample plot.

### Data Sources

1. Web scrape data from the webpage [The World's Deadliest Earthquakes](https://ourworldindata.org/the-worlds-deadliest-earthquakes) using pandas `read_html` method.
2. Acquire the natural disaster dataset from the OurWorldInData servers using the owid-catalog API.

### Data Acquisition

(i) Use the pandas `read_html` method to web scrape data from [The World's Deadliest Earthquakes](https://ourworldindata.org/the-worlds-deadliest-earthquakes). [See examples from pandas documentation](https://pandas.pydata.org/docs/user_guide/io.html#html). Note that `read_html` returns an array of tables.

(ii) Acquire the natural disaster dataset using the owid-catalog API. Install owid-catalog (`pip install owid-catalog`) and import catalog as `from owid import catalog`. Use `catalog.find('natural_disasters')` to get a table (dataframe) listing two datasets. Choose the `natural_disasters_yearly` dataset (2nd row in the table) with `data.iloc[1].load()`.

### Data Preparation and Cleaning

(i) Choose rows corresponding to earthquakes and for years 2020 or higher from the owid catalog acquired data.

(ii) Remove data rows for "World", "European Union (27)", and Continents. You can manually list continents or use a Python API such as `a-world-of-countries` to get continent names. Remove names from the list: `['Upper-middle-income countries', 'Lower-middle-income countries', 'High-income countries', 'Low-income countries']`.

(iii) Sort the resulting dataframe in decreasing order. Pick only 5 rows to concatenate with the scraped dataset. Ensure both dataframes have the same column names.

(iv) Use `drop_duplicates(subset=["country", "year"])` to avoid row duplication.

### Visualization

Use the bar plot method of [Plotly express](https://plotly.com/python/plotly-express/) or [Seaborn](https://seaborn.pydata.org/) to create horizontal bar plots. Set color (for Plotly) or hue (for Seaborn) to distinguish bars before 2020 and the others.

### Sample Plot Mismatches

Notice a couple of mismatches, which may be attributed to manual addition of some data and possible typographic errors during manual data addition.

### Instructions to Run

1. Install required packages: `pip install pandas plotly seaborn owid-catalog a-world-of-countries`
2. Run the script or Jupyter notebook containing the code.

### References

- [Our World in Data](https://ourworldindata.org)
- [Pandas Documentation - `read_html`](https://pandas.pydata.org/docs/user_guide/io.html#html)
- [Owid Catalog API](https://github.com/owid/owid-catalog-py)
- [Plotly Express Documentation](https://plotly.com/python/plotly-express/)
- [Seaborn Documentation](https://seaborn.pydata.org/)
- [`a-world-of-countries` Package](https://pypi.org/project/a-world-of-countries/)

### Notes

- Make sure to replace the sample plot with the generated plot for comparison.
- Adjust the code as needed based on the mismatches observed.
- 
# Sample 1
![Sample 1](https://raw.githubusercontent.com/himanshushukla12/Data_Visualization/main/assignment5/earthquake.png)

# Sample 2
![Sample 2](https://raw.githubusercontent.com/himanshushukla12/Data_Visualization/main/assignment5/newspaperPlot.png)

