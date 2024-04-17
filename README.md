# Data Wrangling for Automobile Dataset

This document provides a comprehensive guide on data wrangling techniques applied to an automobile dataset. It covers handling missing values, correcting data formats, standardizing variables, and transforming variables for analysis. The main goal is to obtain a clean dataset with no missing values and all variables in the proper format for further analysis.

## Summary

The document describes the steps taken to clean and prepare an automobile dataset for analysis. It involves identifying and handling missing values, correcting data formats, standardizing variables, and transforming variables into different formats suitable for modeling.

## Approach

1. **Identify and handle missing values:**
   - Replace missing '?' with NaN
   - Count missing values in each column
   - Deal with missing data by replacing with mean, mode, or dropping rows

2. **Correct data formats:**
   - Check data types (dtypes) and convert to the proper format (float, int, etc.)

3. **Standardize variables:**
   - Transform miles per gallon (mpg) to liters per 100 kilometers (L/100km)

4. **Normalize variables:**
   - Scale variables to a range from 0 to 1

5. **Bin continuous variables:**
   - Segment horsepower into bins

6. **Create indicator variables:**
   - Convert categorical variables to dummy variables

## Solutions

1. **To identify and handle missing data:**
   - Missing '?' were replaced with NaN
   - `isnull()` and `notnull()` functions identified missing values
   - For columns with few missing values, mean imputation was used
   - For a column with categorical missing values, mode imputation was used
   - Rows with missing price data were dropped

2. **To correct data formats:**
   - Data types were checked, and columns like 'bore' and 'stroke' were converted to float
   - 'normalized-losses' was converted to int
   - 'price' was converted to float

3. **To standardize variables:**
   - mpg was transformed to L/100km using a formula

4. **To normalize variables:**
   - 'length', 'width', and 'height' were scaled to the 0-1 range

5. **For binning:**
   - Horsepower values were segmented into 3 equal bins ('Low', 'Medium', 'High')

6. **To create indicator variables:**
   - `get_dummies()` was used to convert categorical columns like 'fuel-type' to dummy/indicator variables

Finally, all the processing steps cleaned the data by removing missing values and inconsistencies in formats/units. The transformed data is now in a suitable form for analysis, with variables encoded numerically. The key advantages are:

- Higher accuracy by removing invalid/incomplete data
- Common format enables comparative analysis
- Indicator/dummy variables allow categorical predictors for models

The outputs were tested on sample data to validate the data cleaning steps. Overall, this systematic approach thoroughly cleaned the automobile dataset.
