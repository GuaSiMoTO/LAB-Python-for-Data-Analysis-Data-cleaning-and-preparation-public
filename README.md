# LAB-Python-for-Data-Analysis-Data-cleaning-and-preparation
## Introduction

> ***Note:*** _This can be a pair programming activity or done independently._

Hello everyone, welcome to this lab where we will delve into data manipulation and cleaning techniques using the pandas library. This includes learning how to handle missing data, filter and sort data, and perform various data transformations to prepare data for analysis. Imagine you are part of a small team at a company, and you need to manage and analyze the team's data using Python.

## Initial Setup

### Fork The Repository
First things first, head over to GitHub and click the fork button to create a copy of this repository in your personal account. This will allow you to make changes and save your progress.

## Scenario

You've been hired as a data analyst for a small company. They have given you a set of product data that needs cleaning and analysis. Your task is to manage this data using pandas and provide insights to the management team.

## Iteration 1: Introduction to Data Cleaning

Set up your Python environment and ensure you have pandas installed. You can do this using pip:

bash
pip install pandas
Task:
Load the provided dataset into a pandas DataFrame.
Display the first 10 rows of the DataFrame.
Check for any missing values in the dataset and list the columns with missing data.
Iteration 2: Handling Missing Data
Task:
Identify columns with missing data and the percentage of missing data in each column.
Use appropriate methods to handle missing data:
For numerical columns, fill missing values with the mean of the column.
For categorical columns, fill missing values with the mode of the column.
Verify that all missing data has been handled appropriately.
python
Copy code
import pandas as pd

# Load the dataset
df = pd.read_csv('products.csv')

# Display the first 10 rows
print(df.head(10))

# Check for missing values
missing_data = df.isnull().sum()
print(missing_data)

# Fill missing values
df['Price'].fillna(df['Price'].mean(), inplace=True)
df['Category'].fillna(df['Category'].mode()[0], inplace=True)

# Verify missing data handling
print(df.isnull().sum())
Iteration 3: Parsing Dates
Task:
Convert any columns with date information into pandas datetime format.
Extract year, month, and day from the date column and create new columns for each.
Set the date column as the index of the DataFrame.
python
Copy code
# Assuming there is a column named 'Date'
df['Date'] = pd.to_datetime(df['Date'])

# Extract year, month, and day
df['Year'] = df['Date'].dt.year
df['Month'] = df['Date'].dt.month
df['Day'] = df['Date'].dt.day

# Set the date column as index
df.set_index('Date', inplace=True)

print(df.head())
Iteration 4: Character Encoding
Task:
Detect and resolve any issues with character encoding in the dataset.
Ensure all text data is properly encoded in UTF-8.
Normalize text data to ensure consistency (e.g., all text in lowercase, removing special characters).
python
Copy code
# Detect and resolve encoding issues
df['Product Name'] = df['Product Name'].str.encode('utf-8').str.decode('utf-8')

# Normalize text data
df['Product Name'] = df['Product Name'].str.lower().str.replace('[^a-zA-Z0-9 ]', '')

print(df.head())
Iteration 5: Scaling and Normalization Techniques
Task:
Use Scikit-learn to apply scaling and normalization techniques to the numerical data.
Compare different scaling methods (e.g., MinMaxScaler, StandardScaler) and determine which one is most appropriate for the dataset.
Apply the chosen scaling method to the numerical columns in the DataFrame.
python
Copy code
from sklearn.preprocessing import MinMaxScaler, StandardScaler

# Initialize scalers
min_max_scaler = MinMaxScaler()
standard_scaler = StandardScaler()

# Apply MinMaxScaler
df['Price_MinMaxScaled'] = min_max_scaler.fit_transform(df[['Price']])

# Apply StandardScaler
df['Price_StandardScaled'] = standard_scaler.fit_transform(df[['Price']])

print(df.head())
Iteration 6: Identifying and Correcting Inconsistent Data Entry
Task:
Identify inconsistent data entries (e.g., variations in spelling, incorrect data types).
Correct these inconsistencies using appropriate pandas methods.
Ensure all corrections are applied throughout the entire dataset consistently.
python
Copy code
# Identify inconsistent entries
inconsistent_entries = df['Category'].unique()
print(inconsistent_entries)

# Correct inconsistencies
df['Category'] = df['Category'].replace({'electronics': 'Electronics', 'furnitures': 'Furniture'})

# Verify corrections
print(df['Category'].unique())
How to Submit
To submit this LAB, upload the file to your forked repository.

Additional Resources
Pandas Documentation
Scikit-learn Documentation
Python Data Analysis Library (Pandas) Tutorial;
devuelveme esto en markdown de github

