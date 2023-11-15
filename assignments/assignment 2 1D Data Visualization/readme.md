# Data Analysis: Height and Gender

## Data Acquisition and Inspection

### Read Excel File

Use the following Python code to read the Excel file, extracting only the 'Gender' and 'Height' columns:

```python
import pandas as pd

# Install openpyxl package
# !pip install openpyxl

# Specify the filename
filename = '<your_filename.xlsx>'

# Read only the 'Gender' and 'Height' columns
df = pd.read_excel(filename, usecols=['Gender', 'Height'])
```

### Check Column Names

Check the exact name of the 'Height' data column:

```python
print(df.columns)
```

### Change Column Names

You can use the `rename` method to change column names for convenience:

```python
df.rename(columns={"Original_Name": "Shortened_Name"}, inplace=True)
```

## Data Cleaning

### Resolve Gender Non-Uniformity

Address non-uniformity in the 'Gender' column:

```python
# Convert all values in 'Gender' column to lowercase
df['Gender'] = df['Gender'].str.lower()
```

## Data Visualization

Use either Plotly Express or Seaborn to create the following distribution plots:

### Histogram Plot

```python
import plotly.express as px

fig = px.histogram(df, x='Height', color='Gender', marginal='rug', nbins=30, opacity=0.7,
                   title='Distribution of Height by Gender')
fig.show()
```

### Box Plot

```python
import seaborn as sns
import matplotlib.pyplot as plt

sns.boxplot(x='Gender', y='Height', data=df)
plt.title('Box Plot of Height by Gender')
plt.show()
```

### Violin Plot

```python
sns.violinplot(x='Gender', y='Height', data=df)
plt.title('Violin Plot of Height by Gender')
plt.show()
```

Note: Ensure you have the necessary packages installed (`openpyxl`, `pandas`, `plotly`, `seaborn`, `matplotlib`) before running the code.

## Dataset Source

This dataset contains height, weight, and fingerprint measurements collected from 200 participants. It was downloaded from [Loughborough University's repository](https://repository.lboro.ac.uk/articles/dataset/Height_weight_and_fingerprint_measurements_collected_from_200_participants/7539206).

Feel free to explore and analyze the data further based on your requirements.
