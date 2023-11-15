# Pin Code Data Analysis

## Data Acquisition and Inspection

1. **Download Data:**
   - Download the All India Pincode Directory CSV from [data.gov.in](https://data.gov.in) (search for "All India Pincode Directory till last month").

2. **Read and Create DataFrame:**
   - Read the downloaded CSV file and create a pandas DataFrame.

3. **Data Frame Information:**
   - Count the number of rows and columns in the DataFrame.
   - List the column names.

4. **Missing Values:**
   - Count the number of rows with missing values.
   - Identify the columns with missing values.

## Data Cleaning

1. **Re-read CSV with Specific Column Data Types:**
   - Re-read the CSV file with 'Latitude' and 'Longitude' columns read as strings.
   - Use the dtype parameter in the `read_csv` method.

2. **Remove Rows with Missing Values:**
   - Remove rows with missing values.
   - Reset the indices of the DataFrame.

3. **Clean Latitude and Longitude Columns:**
   - Clean and convert the 'Latitude' and 'Longitude' columns to float type.
   - Use `.astype(float)` and handle errors during conversion.

4. **Retry Conversion:**
   - If errors occur during conversion, implement necessary cleaning steps and retry until successful.

## Instructions to Run

1. **Download Data:**
   - Visit [data.gov.in](https://data.gov.in) and search for "All India Pincode Directory till last month."
   - Download the CSV file.

2. **Run Jupyter Notebook or Python Script:**
   - Run the provided Jupyter Notebook or Python script that contains the data acquisition and cleaning code.

3. **Check Results:**
   - Review the output for DataFrame information, missing values, and cleaned data.

## Note

- Ensure that the necessary Python libraries, such as pandas, are installed before running the script.
- Carefully follow the data cleaning instructions, especially the steps related to converting 'Latitude' and 'Longitude' columns.
- Make sure to handle errors during conversion and retry until the process is successful.

## References

- [data.gov.in](https://data.gov.in) - Official Government Data Portal
- [pandas Documentation](https://pandas.pydata.org/pandas-docs/stable/index.html) - For information on DataFrame manipulation and cleaning techniques.
- Python Documentation - For additional resources on handling data in Python.
