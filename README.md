# LAB: Python for Data Analysis - Data Cleaning and Preparation

![Excel Image](https://user-images.githubusercontent.com/970858/63474771-d6734700-c469-11e9-83bb-9429da563909.png)

## Introduction

> ***Note:*** _This can be a pair programming activity or done independently._

Hello everyone, welcome to this lab where we will delve into data manipulation and cleaning techniques using the pandas library. This includes learning how to handle missing data, filter and sort data, and perform various data transformations to prepare data for analysis. Imagine you are part of a small team at a company, and you need to manage and analyze the team's data using Python.

## Initial Setup

### Fork The Repository
First things first, head over to GitHub and click the fork button to create a copy of this repository in your personal account. This will allow you to make changes and save your progress.

## Scenario

You've been hired as a data analyst for a small company that sells various products online. The company has provided you with a dataset containing information about their products, including prices, categories, and sales dates. However, the data is not clean and requires significant preparation before it can be analyzed effectively.

Your task is to clean and prepare this data using pandas, a powerful data manipulation library in Python. By the end of the lab, you will have a clean dataset ready for analysis and will be able to provide valuable insights to the management team.

## Iteration 1: Introduction to Data Cleaning

Set up your Python environment and ensure you have pandas installed.

- Load the provided dataset into a pandas DataFrame.
- Display the first 10 rows of the DataFrame.
- Check for any missing values in the dataset and list the columns with missing data.

## Iteration 2: Handling Missing Data

- Identify columns with missing data and the percentage of missing data in each column.
- For numerical columns, fill missing values with the mean of the column. (E.g., if price has missing values, fill them with the mean price.)
- For categorical columns, fill missing values with the mode of the column. (E.g., if category has missing values, fill them with the most frequent category.)
- Verify that all missing data has been handled appropriately.

## Iteration 3: Identifying and Correcting Inconsistent Data Entry

- Identify inconsistent data entries in categorical columns (e.g., variations in spelling, incorrect data types in category).
- Use pandas methods to correct these inconsistencies (e.g., standardize category names to lowercase).
- Ensure all corrections are applied throughout the entire dataset consistently.

## Iteration 4: Character Encoding

- Detect and resolve any issues with character encoding in the dataset.
- Ensure all text data is properly encoded in UTF-8.
- Normalize text data to ensure consistency (e.g., all text in lowercase, removing special characters).

## Iteration 5: Parsing Dates

- Convert any columns with date information into pandas datetime format (e.g., sales_date).
- Extract year, month, and day from the date column and create new columns for each.
- Set the date column as the index of the DataFrame.

## Iteration 6: Scaling and Normalization Techniques

- Use Scikit-learn to apply scaling and normalization techniques to the numerical data.
- Compare different scaling methods (e.g., MinMaxScaler, StandardScaler) and determine which one is most appropriate for the dataset.
- Apply the chosen scaling method to the numerical columns in the DataFrame.

## Bonus

For this bonus section, you will practice your data cleaning skills on a real-world dataset from Kaggle. This will help you solidify the techniques you have learned and apply them to a new context. The dataset you will use contains detailed information about Airbnb listings. You will need to create a new Jupyter Notebook to work on this task. The dataset you will use can be found at [Airbnb Dataset](https://www.kaggle.com/datasets/yagunnersya/fifa-21-messy-raw-dataset-for-cleaning-exploring) on Kaggle.

## How to Submit

To submit this LAB, upload the file to your forked repository.

## Additional Resources

- [Pandas Documentation](https://pandas.pydata.org/pandas-docs/stable/)
- [Scikit-learn Documentation](https://scikit-learn.org/stable/documentation.html)
- [Python Data Analysis Library (Pandas) Tutorial](https://pandas.pydata.org/pandas-docs/stable/getting_started/intro_tutorials/index.html)
