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

## Starter Code

You have to solve the different problems in the `LAB-Data-Cleaning.ipynb` notebook.

To get started, follow these steps:

1. Open your terminal and navigate to the `cloned-repo` directory:

    ```bash
    cd path/to/your/cloned-repo/
    ```

2. Launch Jupyter Notebook:

    ```bash
    jupyter lab
    ```

3. In the Jupyter Notebook interface, open the `LAB-Data-Cleaning.ipynb` file.

To test that everything is set up correctly, run the first cell in the notebook. This cell usually contains import statements and initial setup code. If it runs without errors, you are ready to start solving the exercises.

## Iteration 0: Install Dependencies

Make sure you have all the necessary libraries installed by using the `requirements.txt` file provided. You can install the dependencies with the following command:

```bash
pip install -r requirements.txt
```

## Iteration 1

Set up your Python environment and ensure you have pandas installed.

- Load the provided dataset into a pandas DataFrame.
**Note**: Make sure the file is properly encoded in UTF-8.
- Display the first 10 rows of the DataFrame.

## Iteration 2: Handling Missing Data

- Identify columns with missing data and the percentage of missing data in each column.
- For numerical columns, fill missing values with the mean of the column. (E.g., if price has missing values, fill them with the mean price.)
- For categorical columns, fill missing values with the mode of the column. (E.g., if category has missing values, fill them with the most frequent category.)
- Verify that all missing data has been handled appropriately.

## Iteration 3: Identifying and Correcting Inconsistent Data Entry

In this iteration, your task is to ensure that the values in the categorical columns are consistent. Sometimes, datasets contain **variations** or **typos** in category names, which can make analysis difficult. To correct these issues, you need to have a **reference list of the correct categories**, which is provided below.

#### **Reference List of Correct Categories:**
The valid categories in this dataset are as follows:

- **Toys**
- **Electronics**
- **Beauty**
- **Clothing**
- **Home**
- **Home Appliances**

Any other variation should be corrected to match one of these categories.

#### **Objective:**
- Identify and correct any inconsistent entries in the categorical columns, such as:
  - **Spelling variations** (e.g., "Toys" and "toys" should be unified as "Toys").
  - **Typos** (e.g., "Electroncs" should be corrected to "Electronics").

It is important to ensure that the category values are **consistent** and **uniform** for accurate analysis. In this iteration, you are not concerned with converting text to lowercase (that is handled in another step), but rather with unifying incorrect categories based on the reference list of valid categories.

#### **Steps to solve:**

1. **Identify inconsistent categories:**
   Use `df['category'].unique()` to review the categories in the `category` column. Compare these values with the provided reference list of valid categories to identify any errors or variations.

2. **Correct inconsistencies:**
   Use the pandas `replace()` method to correct the variations. Unify the incorrect names with the correct version from the reference list of valid categories.

3. **Verify corrections:**
   After making the corrections, check the unique values again to ensure all categories have been unified correctly.

## Iteration 4: Parsing Dates

In this iteration, your task is to properly handle and format any columns in the dataset that contain date information. Working with dates is a common requirement when analyzing time-based data, as it allows for more powerful insights such as trends over time, seasonality, or other temporal patterns.

The column we will focus on in this iteration is `sales_date`, which records the date of each sale. You will convert this column into a pandas datetime format, which allows for easier manipulation of the date information and enables the extraction of specific components, such as the year, month, and day.

#### **Objective:**
- Convert any columns with date information (e.g., `sales_date`) into pandas' `datetime` format.
- Extract the **year**, **month**, and **day** from the date column and create new columns for each. This step is useful if you later want to group data by month, year, or day for analysis.
- Set the `sales_date` column as the **index** of the DataFrame. This makes it easier to perform time-based indexing, filtering, or resampling.

## Iteration 5: Scaling and Normalization Techniques

In this iteration, your task is to apply **scaling** and **normalization** techniques to the numerical data in the dataset. Scaling and normalization are essential preprocessing steps in machine learning and data analysis, especially when working with algorithms that are sensitive to the ranges or distributions of the data.

Many machine learning models (such as linear regression, neural networks, and clustering algorithms) perform better when the numerical data is scaled or normalized because it helps avoid biases caused by different ranges or magnitudes in the features. For example, if one feature is measured in large units (like price) and another in small units (like the number of units sold), it can distort the model's performance if they are not scaled properly.

#### **Objective:**
- Use **Scikit-learn** to apply scaling and normalization techniques to the numerical data in the dataset. This step ensures that the features are on a similar scale and helps improve the performance of machine learning models.
- **Compare different scaling methods**, such as `MinMaxScaler` and `StandardScaler`, to determine which one is the most appropriate for the dataset. Each method has its own advantages, and the choice depends on the distribution and range of your data.
- Once you decide which scaling method is appropriate, apply it to the numerical columns of the DataFrame to standardize the data.

By the end of this iteration, your numerical features will be properly scaled or normalized, making them more suitable for analysis and modeling.

#### **Steps to solve:**

1. **Select the numerical columns:**
   Identify the numerical columns in your dataset that require scaling or normalization. For instance, in this dataset, numerical columns might include `price` and `units_sold`.

2. **Apply scaling techniques:**
   You will use **Scikit-learn** to apply two common scaling techniques:
   - **MinMaxScaler:** Scales the data to a fixed range, usually [0, 1]. It is useful when you need to preserve the relationships between values while bringing them into a standard range.
   - **StandardScaler:** Standardizes the data by subtracting the mean and scaling to unit variance (i.e., mean 0 and standard deviation 1). This is useful when the data has a normal distribution or when the model assumes normally distributed features.

   After applying each scaling method, you should compare the results to understand how each technique transforms the data.

3. **Compare the scaling results:**
   Compare the results of both scaling methods by printing a few rows of the scaled data. Based on the results, decide which method is most appropriate for the dataset.

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

