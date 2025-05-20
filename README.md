# 🚗 Data Wrangling for Automobile Dataset

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Pandas](https://img.shields.io/badge/pandas-DataCleaning-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

> This project provides a comprehensive walkthrough of data wrangling techniques applied to an automobile dataset, focusing on preparing the data for meaningful analysis and machine learning modeling.

---

## 📋 Summary

The notebook details a structured approach to cleaning and preparing an automobile dataset. It addresses:
- Handling missing values
- Correcting data formats
- Standardizing and normalizing variables
- Transforming continuous and categorical data

The ultimate goal is to create a clean, well-formatted dataset ready for analysis and modeling.

---

## 🔧 Approach

### 1. 🔍 Identify and Handle Missing Values
- Replaced `'?'` with `NaN`
- Counted missing values column-wise
- Imputed missing numeric values with **mean**
- Imputed missing categorical values with **mode**
- Dropped rows where critical values like `price` were missing

### 2. 🧮 Correct Data Formats
- Converted string-type numerics to proper types:  
  e.g., `'bore'`, `'stroke'` → `float`; `'normalized-losses'` → `int`
- Converted `price` column to `float`

### 3. ⚙️ Standardize Variables
- Converted `mpg` (miles per gallon) to `L/100km` for consistent units

### 4. 📏 Normalize Variables
- Scaled continuous variables (`length`, `width`, `height`) to a [0, 1] range

### 5. 📊 Bin Continuous Variables
- Segmented `horsepower` into 3 bins: `Low`, `Medium`, `High`

### 6. 🏷️ Create Indicator Variables
- Applied one-hot encoding to categorical features using `get_dummies()`  
  e.g., `'fuel-type'`, `'aspiration'`

---

## ✅ Solutions Applied

- Missing values handled using a mix of **imputation** and **row removal**
- Non-numeric data types were cleaned and **converted** appropriately
- Unit conversion and normalization ensured **consistency** across variables
- Binning and encoding enabled models to handle **categorical and continuous features**

---

## 🎯 Benefits of This Approach

- 🚫 Removes incomplete and invalid data
- 📐 Ensures consistent formats for all variables
- 💡 Enables categorical variables in modeling via dummy encoding
- 🔍 Prepares dataset for meaningful statistical and ML analysis

---

## 🧪 Validation

Each step was validated using exploratory analysis and visual inspection. Final output was a clean, fully numeric dataset suitable for regression or classification models.

---

## 📜 License

This project is licensed under the **MIT License**.

---

## 🙌 Acknowledgments

Special thanks to the open data science community and IBM’s Data Science curriculum for inspiring this exercise.

---

*Made with 🧼, 📊, and 🧠 for cleaner, smarter data.*
