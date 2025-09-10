# Walmart Sales Data Pipeline & Analysis

Walmart is the largest retail store in the United States. Like other major retailers, they have been expanding their **e-commerce business**.  
By the end of **2022**, e-commerce represented **$80 billion in sales**, which is **13% of Walmart’s total sales**.  

One of the main factors that affects their sales is **public holidays**, such as:
- Super Bowl  
- Labour Day  
- Thanksgiving  
- Christmas  

In this project, you are tasked with:  
1. Creating a **data pipeline** for analyzing supply and demand around holidays.  
2. Conducting a **preliminary analysis** of the sales data.  

---

## Data Sources

You will be working with **two data sources**:

### 1. `grocery_sales` table (PostgreSQL database)
| Column | Description |
|--------|-------------|
| `index` | Unique ID of the row |
| `Store_ID` | Store number |
| `Date` | Week of sales |
| `Weekly_Sales` | Sales for the given store |

---

### 2. `extra_data.parquet` file
| Column | Description |
|--------|-------------|
| `IsHoliday` | Whether the week contains a public holiday (`1 = Yes`, `0 = No`) |
| `Temperature` | Temperature on the day of sale |
| `Fuel_Price` | Cost of fuel in the region |
| `CPI` | Prevailing consumer price index |
| `Unemployment` | Prevailing unemployment rate |
| `MarkDown1 - MarkDown4` | Number of promotional markdowns |
| `Dept` | Department number in each store |
| `Size` | Size of the store |
| `Type` | Store type (depends on `Size`) |

---

## Data Transformation

After merging and cleaning, create the `clean_data` DataFrame with the following columns:

- `Store_ID`  
- `Month`  
- `Dept`  
- `IsHoliday`  
- `Weekly_Sales`  
- `CPI`  
- `Unemployment`  

---

## Analysis

Analyze **monthly sales of Walmart** and store results in the `agg_data` variable.  
The final output should look like:

| Month | Weekly_Sales   |
|-------|----------------|
| 1.0   | 33174.178494   |
| 2.0   | 34333.326579   |
| ...   | ...            |

---

## Saving Results

Save the following as **CSV files**:
- `clean_data.csv`
- `agg_data.csv`

---

## Recommended Tools
- **Python**  
- **Pandas**  
- **PostgreSQL**  

---

✅ By completing this project, you will build a **data pipeline** that merges different sources, transforms them into a clean format, and provides aggregated insights about Walmart’s sales trends during **holidays**.
