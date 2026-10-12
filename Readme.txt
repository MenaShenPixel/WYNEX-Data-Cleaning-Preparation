# Retail Sales Data Cleaning & Preparation

## 📌 Project Overview

This project focuses on data cleaning and preparation for a retail sales dataset using Microsoft Excel.

The objective is to assess data quality, identify potential inconsistencies, validate important fields, and prepare the dataset for further analysis.

## 🎯 Objectives

- Inspect the dataset structure and data types.
- Identify missing values and duplicate records.
- Validate date fields and related columns.
- Review categorical data for inconsistencies.
- Investigate potential data quality issues.
- Prepare a clean dataset for future analysis.

## 📊 Dataset Overview

The dataset contains retail sales records with information about customers, products, orders, sales performance, and shipping.

**Dataset dimensions:**
- Rows: 51,252
- Columns: 26

**Key columns include:**
- **Customer Information:** Customer ID, Customer Name, Segment
- **Geographic Information:** City, State, Country, Region, Market
- **Product Information:** Product ID, Product Name, Category, Sub-Category
- **Order Information:** Order ID, Order Date, Order Priority
- **Sales Metrics:** Sales, Quantity, Discount, Profit
- **Shipping Information:** Ship Date, Ship Mode, Shipping Cost

## 🛠️ Tools Used

- **Microsoft Excel:** Data inspection, validation, and preparation.
- **Power Query:** Data transformation and cleaning, where applicable.

## 🧹 Data Cleaning & Validation

The following checks were performed:

1. **Missing Values:** Checked all columns for missing values.
2. **Duplicate Records:** Checked for exact duplicate rows and duplicate combinations of Order ID and Product ID.
3. **Data Types:** Reviewed column data types and date formats.
4. **Date Validation:** Checked the relationship between Order Date, Ship Date, Year, and Week Number.
5. **Text Validation:** Reviewed product names and text formatting.
6. **Categorical Consistency:** Examined product categories, subcategories, regions, and market classifications.
7. **Data Quality Issues:** Identified records and fields requiring further investigation.

## ⚠️ Data Quality Findings

### Discount Column

The original `Discount` column contained binary values (`0` and `1`), which were converted to Boolean values (`FALSE` and `TRUE`) for readability.

These values represent a binary indicator rather than actual discount percentages. Therefore, the column cannot be used to calculate or analyze discount rates without additional information about the underlying data.

### 2. Market Classification

Potential inconsistencies were identified in the mapping between countries and the Market2 column, particularly for Austria and Mongolia.

These cases require verification against the original source or an authoritative market mapping before any changes are made.

### 3. Zero Sales Record

One record contains zero sales and a negative profit value. This record was flagged for review rather than automatically deleted or modified.

### 4. Row ID Gaps

The Row ID column contains gaps in its sequence. Since records had previously been removed, the original records would need to be reviewed to confirm whether their removal was justified.

### 5. Record Count Column

The Record Count column contains a constant value of 1 in every row. Its analytical usefulness should be evaluated before deciding whether to remove it.

## ✅ Validation Results

- No missing values were detected in the inspected dataset.
- No exact duplicate rows were found in the current file.
- No duplicate Order ID and Product ID combinations were found in the current file.
- Year values were consistent with Order Date.
- Week Number values were consistent with the corresponding date calculation.
- No shipping dates earlier than order dates were detected.

## 📁 Project Files

- 'superstore.csv'— Raw data before cleaning.
- `Cleaned_Superstore_data.csv` — Dataset after cleaning and the used data for further analysis.
- `Cleaned_Superstore_data` — 
- `README.md` — Project documentation.



## 🚀 Next Steps

- Resolve or document outstanding data quality issues.
- Finalize and validate the cleaned dataset.
- Use the prepared data for exploratory data analysis (EDA).
- Develop business insights and visualizations in a future analysis stage.

## 📝 Conclusion

This project demonstrates the importance of data quality assessment before performing business analysis.

Rather than making unsupported assumptions, potential issues were documented for further investigation to help preserve data integrity and ensure reliable analytical results.