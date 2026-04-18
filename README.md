# Experiment-No.13:
# Aim:
To perform preprocessing on a dataset and handle missing values using Python libraries such as Pandas and NumPy.

# Theory:
Data preprocessing is a crucial step in data analysis and machine learning.
Real-world datasets are often incomplete, inconsistent, and noisy. Handling missing values and cleaning data ensures accurate analysis and better model performance.

Step 1. Handling Missing Values
Missing values are commonly represented as NaN (Not a Number) in datasets.
These can arise due to data entry errors, system issues, or unavailable information.
pd.DataFrame()
Creates a DataFrame (tabular structure) from given data.
np.nan
Represents missing values in numerical datasets.
isna()
Returns a boolean DataFrame showing True where values are missing.
notna()
Returns True where values are present (not missing).
isna().sum()
Counts missing values column-wise.
isna().sum(axis=1)
Counts missing values row-wise.
Step 2. Removing Missing Values
dropna()
Removes rows containing missing values.
dropna(axis=1)
Removes columns containing missing values.
 Use when missing data is minimal and can be safely discarded.

Step 3. Filling Missing Values
Instead of removing data, missing values can be replaced:
fillna(0)
Replaces all missing values with 0.
fillna(df.mean())
Replaces missing values with the mean of each column.
fillna(df.mean(axis=1))
Replaces missing values with row-wise mean.
Helps preserve dataset size and structure.

Step 4. Data Cleaning and Preprocessing
Real datasets often contain inconsistent formats and invalid entries.
Functions Used:
replace("-", np.nan)
Replaces placeholder values (like '-') with actual missing values.
pd.to_numeric(column, errors="coerce")
Converts data to numeric type. Invalid values are converted to NaN.
fillna() with mean/median
Mean → used for continuous data (e.g., Age)
Median → better for skewed data (e.g., Marks)
 Step 5. Text Standardization
str.upper()
Converts text data to uppercase to maintain consistency
(e.g., "cse" → "CSE")
Step 6. Date Formatting
pd.to_datetime()
Converts date strings into standard datetime format.
errors="coerce"
Invalid date formats are converted to NaT (missing datetime).
Ensures uniform date format for analysis.
# Summary of Workflow
Create dataset
Identify missing values
Replace invalid entries with NaN
Convert data types
Fill missing values (mean/median)
Standardize text data
Format date columns
# Conclusion:
In this experiment, we successfully performed data preprocessing by identifying and handling missing values using Pandas and NumPy.
Various techniques such as removing missing data, filling values using statistical methods, and standardizing text and date formats were applied.
