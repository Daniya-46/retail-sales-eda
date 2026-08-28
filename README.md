# Retail Sales Exploratory Data Analysis (EDA)

##  Project Overview
This project focuses on performing an in-depth Exploratory Data Analysis (EDA) on a retail sales dataset. The primary objective is to clean the raw data, uncover hidden patterns, and generate actionable business insights regarding product categories, regional performance, and seasonal sales trends. 

##  Tech Stack
* **Language:** Python 3
* **Libraries:** Pandas, NumPy, Matplotlib, Seaborn
* **Environment:** Jupyter Notebook / Google Colab

##  Dataset Details
The dataset (`retail_sales.csv`) contains 1,825 records of daily sales transactions. 
* **Features:** `Date`, `Category`, `Sales`, `Quantity`, `Profit`, `Region`
* **Target Variables:** `Sales` and `Profit`

##  Project Workflow

### 1. Data Cleaning & Preprocessing
* **Missing Values:** Handled standard null values by dropping incomplete rows.
* **Data Type Conversion:** Converted the `Date` column to `datetime64[ns]` for time-series analysis.
* **Feature Engineering:** Extracted `Month`, `Quarter`, `DayOfWeek`, and `MonthName` from the Date column.
* **Anomaly Detection:** Identified and filtered out dirty string entries (e.g., `'Null'`, `'NaN?'`, `'Nan'`) disguised as legitimate categorical and regional data.

### 2. Statistical Analysis
* Generated descriptive statistics for dispersion and central tendency across numerical columns.
* Grouped and aggregated data to evaluate performance metrics by `Category` and `Region`.

### 3. Data Visualization
A robust suite of visualizations was created using Seaborn and Matplotlib to make the data easily digestible:
* **Time-Series Analysis:** Line plots tracking monthly Sales and Profit trends throughout the year.
* **Categorical Performance:** Horizontal bar charts ranking top-selling product categories.
* **Regional Distribution:** Vertical bar charts and pie charts showcasing revenue shares across different regions.
* **Correlation Analysis:** A heatmap displaying the statistical relationships between Sales, Quantity, and Profit.
* **Executive Dashboard:** A 2x2 grid subplot summarizing all major analytical findings in a single, high-level view.

##  Key Insights
1. **Top Categories:** **Books** and **Electronics** are the highest revenue-generating product categories.
2. **Regional Leaders:** The **West** and **South** regions dominate total sales, bringing in roughly 26.5% and 26.3% of the revenue, respectively. The East region lags slightly behind.
3. **Profitability Correlation:** There is a moderate positive correlation (0.53) between Sales and Profit, while Quantity sold has negligible correlation with overall Profit.

##  How to Run
1. Clone this repository to your local machine.
2. Ensure you have the required libraries installed:
   ```bash
   pip install pandas numpy matplotlib seaborn
