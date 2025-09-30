# Python-Data-Analysis-Missing-values

## 1. Project Overview
This project focuses on exploring and handling missing data within real-world datasets, including both a sample dataframe and the `penguins.csv` dataset from the Palmer Penguins project.  

Using **Python** and the **pandas library**, we demonstrate how to:  
- Identify missing values  
- Quantify missing data by row and column  
- Handle missing data using various DataFrame operations, including dropping rows or columns  

This notebook-style analysis is ideal for learners and analysts looking to strengthen their **data wrangling and cleaning skills** using pandas.

---

## 2. Tools and Libraries Used
The following tools and libraries were used for this analysis:  
- **Python 3.8+**  
- **Pandas** – for data manipulation and analysis  
- **NumPy** – for numeric operations  
- **Jupyter Notebook** or any Python script environment  
- **Matplotlib / Seaborn** (optional) – for visualization if extended for EDA  

---

## 3. Objectives
The objectives of this project are:  
- Explore a dataset containing missing values and understand the types of missing data (`NaN` for numeric columns, `None` for object columns)  
- Count missing values by column and by row  
- Calculate the proportion of missing values  
- Apply strategies to handle missing data, including dropping rows, dropping columns, or selectively removing specific entries  
- Apply these techniques to a real-world dataset (`penguins.csv`) to prepare it for further analysis or modeling  

---

## 4. Key Concepts Learned
- Identifying missing values using `.isna()` or `.isnull()`  
- Counting and summarizing missing values with `.sum()` and `.mean()`  
- Dropping rows or columns with `.dropna()`  
- Selectively removing columns or rows using `drop()` or boolean filtering  
- Understanding the impact of missing data on data analysis and preprocessing

## 5.Exploratory Data Analysis (EDA)
**Task:** Read the `penguins.csv` file into a Pandas DataFrame named `penguins`.

import pandas as pd

### Load CSV into DataFrame
penguins = pd.read_csv("penguins.csv")

### Display first few rows
penguins.head()

<img width="833" height="412" alt="image" src="https://github.com/user-attachments/assets/ab464410-1e3b-4976-b3a2-5be6dce9b287" />

**Task:** Use `.isna()` to count the number of missing values in each column of the `penguins` DataFrame.

### Count missing values by column
penguins.isna().sum()

<img width="450" height="296" alt="image" src="https://github.com/user-attachments/assets/876f5277-f60e-44d0-8887-f99be21da2d5" />

## ➤ Proportion of Missing Values by Row

**Task:** Calculate the proportion of missing values for each row and store it in a variable named `percent_missing_by_row`.

### Calculate proportion of missing values by row
percent_missing_by_row = penguins.isna().mean(axis=1)

###  Display the results
print(percent_missing_by_row)

<img width="661" height="236" alt="image" src="https://github.com/user-attachments/assets/238afcb9-ed5e-4747-b312-34b6cee8a2ef" />

**Task:** Sort the `percent_missing_by_row` series in descending order to identify rows with the most missing values.

### Sort rows by proportion of missing values (highest to lowest)
percent_missing_by_row.sort_values(ascending=False)

<img width="553" height="426" alt="image" src="https://github.com/user-attachments/assets/46334038-3ca8-4957-8d95-6a431376bf6a" />

penguins.isna().sum(axis=1)

<img width="373" height="418" alt="image" src="https://github.com/user-attachments/assets/c8daa1ef-8869-455e-b795-e1e90fcb2303" />

