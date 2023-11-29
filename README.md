# Data-Wrangling-for-Auto-Mobile-Data-Set
provides a comprehensive guide on data wrangling techniques applied to an automobile dataset, including handling missing values, correcting data formats, standardizing variables, and transforming variables for analysis.
Data Wrangling for Automobile Dataset
summary
The document describes the steps taken to clean and prepare an automobile dataset for analysis. It involves identifying and handling missing values, correcting data formats, standardizing variables, and transforming variables into different formats suitable for modeling. The main goal is to obtain a clean dataset with no missing values and all variables in the proper format for further analysis.
Approach
Identify and handle missing values:
•
Replace missing '?' with NaN
•
Count missing values in each column
•
Deal with missing data by replacing with mean, mode or dropping rows
Correct data formats:
•
Check dtypes and convert to proper format (float, int etc.)
Standardize variables:
•
Transform mpg to L/100km
Normalize variables:
- Scale variables to range from 0-1
Bin continuous variables:
- Segment horsepower into bins
Create indicator variables:
- Convert categorical variables to dummy variables
Solutions
To identify and handle missing data:
•
Missing '?' were replaced with NaN
•
isnull() and notnull() functions identified missing values
•
For columns with few missing values, mean imputation was used
•
For a column with categorical missing values, mode imputation was used
•
Rows with missing price data were dropped
To correct data formats:
•
dtypes were checked and columns like 'bore', 'stroke' converted to float
•
'normalized-losses' converted to int
•
'price' converted to float
To standardize variables:
•
mpg was transformed to L/100km using a formula
To normalize variables:
•
'length', 'width' and 'height' were scaled to 0-1 range
For binning:
•
horsepower values were segmented into 3 equal bins ('Low', 'Medium', 'High')
To create indicator variables:
•
get_dummies() was used to convert categorical columns like 'fuel-type' to dummy/indicator variables
Finally, all the processing steps cleaned the data by removing missing values and inconsistencies in formats/units. The transformed data is now in a suitable form for analysis with variables encoded numerically.
The key advantages are: higher accuracy by removing invalid/incomplete data, common format enables comparative analysis, indicator/dummy variables allow categorical predictors for models.
The outputs were tested on sample data to validate the data cleaning steps. Overall, this systematic approach cleaned the automobile dataset thoroughly.
