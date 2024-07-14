# LAB: Python for Data Analysis - Data Cleaning and Preparation

![Excel Image](https://user-images.githubusercontent.com/970858/63474771-d6734700-c469-11e9-83bb-9429da563909.png)

## Introduction

> ***Note:*** _This can be a pair programming activity or done independently._

Hello everyone, welcome to this lab where we will delve into data manipulation and cleaning techniques using the pandas library. This includes learning how to handle missing data, filter and sort data, and perform various data transformations to prepare data for analysis. Imagine you are part of a small team at a company, and you need to manage and analyze the team's data using Python.

## Initial Setup

## Requirements
Start by forking the provided GitHub repository to your account and then clone it locally. This will be your workspace for completing the lab exercises.
- [Learn how to fork this repo](https://guides.github.com/activities/forking/)
- Clone this repo into your `code/labs` folder

## Scenario

You've been hired as a data analyst for a small company that sells various products online. The company has provided you with a dataset containing information about their products, including prices, categories, and sales dates. However, the data is not clean and requires significant preparation before it can be analyzed effectively.

Your task is to clean and prepare this data using pandas, a powerful data manipulation library in Python. By the end of the lab, you will have a clean dataset ready for analysis and will be able to provide valuable insights to the management team.

## Iteration 0: Install Dependencies

Make sure you have all the necessary libraries installed by using the `requirements.txt` file provided. You can install the dependencies with the following command:

```bash
pip install -r requirements.txt
```

## Iteration 1

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

For this bonus section, you’ll get to practice your data cleaning skills with a real-world dataset from Kaggle. This is a great opportunity to apply what you’ve learned in a new context. The dataset provides detailed information about Airbnb listings. To start, create a new Jupyter Notebook for your work. You can find the dataset at [Airbnb Dataset on Kaggle](https://www.kaggle.com/datasets/yagunnersya/fifa-21-messy-raw-dataset-for-cleaning-exploring).

## Submission
Once you have completed your analysis and visualizations, push your Jupyter notebook to your forked GitHub repository. Ensure that your final submission includes narratives explaining your visualizations and insights.
Run the following commands:

```
$ git add .
$ git commit -m "done"
$ git push origin main
```

Then create a Pull Request!!

## Additional Resources
- [Pandas Documentation](https://pandas.pydata.org/pandas-docs/stable/)
- [Python Data Analysis Library (Pandas) Tutorial](https://pandas.pydata.org/pandas-docs/stable/getting_started/intro_tutorials/index.html)


![happy_coding](https://user-images.githubusercontent.com/970858/63899010-c23fc480-c9ea-11e9-84a2-542907e42362.png)

