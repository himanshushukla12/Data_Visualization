
# Geo-visualization of Thematic Data Using Choropleth

## Goal
The objective of this project is to create an aesthetically pleasing and informative Choropleth map to visualize the population variation among the states of India.

## Data Preparation

**Geometric Data**
Geo-visualization requires geometric information about geographical locations/spaces. This data may or may not be available with the thematic data. If not present, the creator must identify the location/space by using commonly accepted geographical identities, such as names or ISO codes. For Indian states, you can find ISO codes at [ISO 3166-2:IN](https://en.wikipedia.org/wiki/ISO_3166-2:IN), and for countries, consult [ISO 3166 Country Codes](https://en.wikipedia.org/wiki/List_of_ISO_3166_country_codes).

For this project, you can acquire geometric data for Indian states and Union territories from [HindustanTimesLabs/shapefiles](https://github.com/HindustanTimesLabs/shapefiles).

**Thematic Data**
We have attached a CSV data file containing the estimated 2023 population of Indian states and most Union Territories. This data has been sourced from [FindEasy](https://www.findeasy.in/top-indian-states-by-population/) and ensures a one-to-one correspondence between the names in the data file and the `properties.ST_NM` key of the feature dictionary in `IndiaState.json` (available in the shapefiles folder).

## Data Visualization

You have two options for creating the Choropleth map: `plotly.express` and `geopandas`.

### Option 1: `plotly.express`
- Utilize `plotly.express` to create the Choropleth map.
- You can choose from two methods: `px.choropleth` or `px.choropleth_mapbox`.

**Sample Plots:**
- Below, you can find two sample plots created using `px.choropleth`.

![Sample Choropleth 1](sample_choropleth_1.png)
![Sample Choropleth 2](sample_choropleth_2.png)

Remember to explore the documentation for `plotly.express` for further customization and options.

### Option 2: `geopandas`
- Alternatively, you can use `geopandas` to visualize the data spatially.

## Project Structure
Here's an organized structure of this project's contents:

