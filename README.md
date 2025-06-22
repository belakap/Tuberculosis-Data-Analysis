# Climate change influence on TB incidence

# Plan

Data Collection Find two datasets covering the past 20 years: Climate and Tuberculosis dataset.

Save Raw Data Rename and save both datasets as CSV files in the project folder DATA/RAW DATA

Raw Data Overview Use pandas for exploratory analysis: raw.info(), raw.describe(), raw.head(), Check for: missing values, duplicates, inconsistent formats (strings, etc), plot initial trends.

Clean the Data In pandas: drop unnecessary columns, standardize column names, ensure consistent formats for year and country, sort years in ascending order, and remove duplicates by calculating the average values per year.

Merge and Analyze Create common subsets: group both datasets by country and year, and merge them.

Analyze merged data: correlation, visualization, scatter plots, regression.


