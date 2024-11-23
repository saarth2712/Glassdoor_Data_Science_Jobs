# Glassdoor Data Science Jobs

This Python script demonstrates a data cleaning for a dataset containing data science job listings from Glassdoor. It involves several steps, including handling missing values, cleaning columns, converting data types, and applying various transformations to the dataset for further analysis.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

## Prerequisites

To run this script, ensure the following libraries are installed:
1. pandas
2. numpy
3. re

## Data Overview
The dataset contains multiple columns related to job listings, including but not limited to:

- **Salary Estimate**: Salary Estimate for the job position
- **Job Description**: Textual description of the job role
- **Company Name**: The company offering the job
- **Revenue**: Revenue of the company
- **Competitors**: List of competitors for the company
- **Location**: The location where the job is based
  

## Steps Involved

### 1. Drop Missing Values and Duplicates
- Use `df.dropna()` to remove rows with missing values.
- Use `df.drop_duplicates()` to eliminate duplicate rows.

### 2. Process Salary Estimates
- Parse the `Salary Estimate` column to extract numerical ranges (e.g., `50K-60K`).
- Compute the average salary and store it in the `Average Salary` column.

### 3. Clean Job Descriptions
- Remove extra newlines and whitespace from the `Job Description` column.

### 4. Standardize Company Names
- Strip non-alphabetical characters, digits, and extra spaces from `Company Name`.

### 5. Remove Negative Values
- Filter out rows with negative values in numerical columns.

### 6. Clean Revenue Column
- Remove unwanted text like ` (USD)` from the `Revenue` column.

### 7. Handle Missing Competitors Data
- Replace `-1` in the `Competitors` column with `NaN` to mark missing values.

### 8. Extract State Information
- Create a `State` column by extracting the last two characters from the `Location` column.

## Conclusion

This script performs essential data-cleaning tasks to prepare the dataset for further analysis or modeling. You can easily adapt this pipeline to fit other datasets or adjust the functions to handle specific edge cases.


## Authors

* **Saarth Soparkar** 



