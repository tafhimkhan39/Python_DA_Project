# ASOS Product Analysis: Stockouts & Lost Revenue Insights

## Introduction

This project analyzes ASOS product data to identify how stock availability impacts potential revenue loss. The analysis focuses on detecting stockouts across product sizes and estimating **lost revenue ("phantom revenue")**, helping uncover missed sales opportunities.

The goal is to simulate a real-world business problem:
**How much revenue is being lost due to products being out of stock, and which brands are most affected?**

---

## Project Overview

In this project, I performed data cleaning, feature engineering, and exploratory analysis to evaluate product availability and its financial impact.

The workflow includes:

1. Data loading and cleaning
2. Brand extraction from product descriptions
3. Feature engineering (stockout metrics & revenue loss)
4. Brand-level aggregation and analysis
5. Visualization of pricing vs stockout behavior
6. Identification of high-impact brands

---

## Dataset

The dataset contains product-level data scraped from ASOS, including:

* **Product information**

  * Product name
  * Description
  * Brand (extracted from text)

* **Pricing**

  * Product price

* **Availability**

  * Size availability
  * Out-of-stock indicators

---

## Tools & Technologies Used

* **Python**
* **Pandas** – data cleaning and transformation
* **Matplotlib & Seaborn** – data visualization
* **Google Colab** - environment

---

## Data Cleaning & Preparation

Key preprocessing steps:

* Converted `price` column to numeric format
* Removed rows with missing or invalid prices
* Cleaned text data in the `description` column
* Filtered brands with low sample sizes to ensure reliable analysis

---

## Feature Engineering

Several custom features were created to quantify stock availability and revenue impact:

### 1. Brand Extraction

Extracted brand names from product descriptions using string parsing logic.

### 2. Stockout Metrics

* **Stockout_Count** → number of unavailable sizes per product
* **Stockout_Rate** → proportion of sizes out of stock

### 3. Lost Revenue (Phantom Revenue)

* **Lost_Revenue = price × Stockout_Count**

This metric estimates how much revenue could have been generated if all sizes were available.

---

## Analysis

### Brand-Level Aggregation

Grouped data by brand to calculate:

* Average product price
* Average stockout rate
* Total lost revenue
* Number of products

### Strategic Visualization

A scatter plot was created to analyze:

* **X-axis:** Average price
* **Y-axis:** Stockout rate
* **Bubble size:** Total lost revenue

Threshold lines were added to highlight:

* High-price brands (> $40)
* High stockout rate (> 40%)

---

## Key Insights

* Brands with **high prices and high stockout rates** represent the **largest missed revenue opportunities**
* Frequent stockouts suggest **supply chain inefficiencies or understocking**
* High-demand products are selling out quickly, indicating potential for:

  * Better inventory planning
  * Increased production
* Some brands generate disproportionately high **lost revenue**, making them prime targets for optimization

---

## Business Impact

This analysis demonstrates how companies can:

* Identify **revenue leakage due to stockouts**
* Optimize **inventory management strategies**
* Prioritize **high-performing brands and products**
* Improve **customer satisfaction by reducing unavailable sizes**

---

## What I Learned

* Cleaning and preparing real-world messy datasets
* Extracting structured insights from unstructured text
* Designing custom business metrics
* Translating data into actionable business insights
* Visualizing multi-dimensional relationships (price, demand, revenue)

---

## Future Improvements

* Build a predictive model for stockout risk
* Analyze demand trends over time
* Incorporate customer behavior data
* Create an interactive dashboard (Power BI / Tableau)

---

## Credit

Credit to the original author of this portfolio project that is displayed in this video: https://www.youtube.com/watch?v=ux9uxKM171E&t=131s

