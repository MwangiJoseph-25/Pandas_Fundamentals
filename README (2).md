# Pandas fundamentals

## Overview
This project is a hands-on learning exercise covering core **pandas** concepts for data loading, cleaning, manipulation, and visualization. It uses two datasets — a Nairobi housing statistics dataset and an order/transactions dataset — to practice fundamental and intermediate pandas operations along with **matplotlib** and **seaborn** for data visualization.

## Datasets
- **`nairobi_housing_statistics_dataset.csv`** — property listings with details such as property type, rent, location, amenities, satisfaction scores, and vacancy status
- **`order.csv`** — order/transaction records with date fields (order date, delivery date, last login, subscription start)

## Notebooks

### 1. `pandas2.ipynb` — Pandas Fundamentals
A step-by-step walkthrough of core pandas concepts:

- **Data structures:** Series vs DataFrame
- **Reading data:** CSV, Excel, JSON, and SQL examples
- **Exploring data:** `.head()`, `.tail()`, `.shape`, `.columns`, `.info()`, `.describe()`
- **Filtering:**
  - Selecting single/multiple columns
  - Row selection with `.loc` and `.iloc`
  - Conditional filtering (e.g., bedrooms > 2)
- **Handling missing values:**
  - Identifying nulls with `.isna().sum()`
  - Thresholds and strategies for dropping vs. filling (mean, median, mode)
  - `.dropna()` and `.fillna()`
- **Duplicates:** detecting and removing with `.duplicated()` / `.drop_duplicates()`
- **Sorting:** `.sort_values()` ascending/descending
- **Grouping & aggregation:** `.groupby()` with `.count()`, `.mean()`, `.median()`, `.sum()`
- **Value counts:** `.value_counts()`
- **Text/string operations:** `.str.lower()`, `.str.upper()`, `.str.capitalize()`, `.str.strip()`, `.str.contains()`
- **Renaming columns:** `.rename()`
- **Working with dates:**
  - Converting columns with `pd.to_datetime()` and `errors='coerce'`
  - Extracting year, month, day name, and quarter
- **Error types in Python:** SyntaxError, RuntimeError, and Logical (semantic) errors
- **Joining/merging datasets:** inner, left, right, and full outer joins with `pd.merge()`

### 2. `visualizations_morning.ipynb` — Data Visualization
Focused on visual exploratory data analysis (EDA) using the housing dataset:

- **Plot types covered:**
  - Count plots (categorical frequency)
  - Bar plots (aggregated comparisons, e.g., average rent by property type)
  - Histograms (distribution of numerical variables)
  - Box plots (spread, median, outliers)
  - Scatter plots (relationships between numerical variables)
  - Line plots (trends, e.g., rent trend 2024 → 2025)
  - Pie charts (category proportions, e.g., vacancy status, furnishing)
  - Heatmaps (correlation between numerical variables)

- **Analysis types:**
  - **Univariate analysis** — distribution of a single variable (numerical and categorical)
  - **Bivariate analysis** — relationships between two variables (numerical-numerical, numerical-categorical, categorical-categorical)
  - **Multivariate analysis** — relationships across three or more variables (e.g., average rent by property type and furnishing)

## Requirements
```
pandas
numpy
matplotlib
seaborn
sqlalchemy   # only needed for the SQL reading example
```

## How to Run
1. Place `nairobi_housing_statistics_dataset.csv` and `order.csv` in the project directory
2. Open `pandas2.ipynb` to work through pandas fundamentals
3. Open `visualizations_morning.ipynb` to explore visualization techniques
4. Run cells sequentially in Jupyter Notebook/JupyterLab

## Project Structure
```
.
├── pandas2.ipynb                          # Pandas fundamentals walkthrough
├── visualizations.ipynb           # Visualization & EDA walkthrough
├── nairobi_housing_statistics_dataset.csv # Housing dataset
├── order.csv                              # Orders/transactions dataset
└── README.md
```

## Key Takeaways
- Practiced reading, inspecting, cleaning, and transforming tabular data with pandas
- Learned strategies for handling missing values and duplicates
- Practiced date parsing and feature extraction (year, month, day, quarter)
- Learned merge/join operations for combining datasets
- Applied univariate, bivariate, and multivariate visual analysis using matplotlib and seaborn
