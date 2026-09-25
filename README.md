# Jumia Product Performance Dashboard: Analyzing Pricing, Discounts, and Customer Reviews

A data analysis and visualization project analyzing Jumia e-commerce product performance using Microsoft Excel. This repository features an interactive dashboard evaluating relationships between prices, discount levels, ratings, and customer review counts, alongside a technical evaluation of Excel's role in business decision-making and predictive analytics.

---

## Project Overview & Objectives

The goal of this project is to analyze product listings on Jumia to extract actionable business insights on pricing strategy and customer engagement. 

Key objectives include:
* **Data Cleaning & Preparation**: Standardizing raw currency formats, missing review values, and string-formatted customer ratings.
* **Feature Enrichment**: Categorizing products by rating quality and discount depth, as well as calculating absolute price reductions.
* **Performance & Trend Analysis**: Examining how discount percentages influence total customer review counts and rating scores.
* **Interactive Dashboard Design**: Building a dynamic dashboard using Pivot Tables, Pivot Charts, Conditional Formatting, and Slicers.

---

## Data Cleaning & Transformation Workflow

The dataset was cleaned and transformed using standard Excel formula operations:

1. **Price Standardization**: Converted text prices (e.g., `"KSh 950"`) into numeric fields removing non-numeric characters.
2. **Rating Extraction**: Parsed numeric ratings from string formats (e.g., `"4.5 out of 5"` $\rightarrow$ `4.5`).
3. **Absolute Discount**: Computed price reduction values:
   $$\text{Absolute Discount} = \text{Old Price} - \text{Current Price}$$
4. **Category Groupings**:
   * **Discount Categories**:
     * `High Discount`: $> 40\%$
     * `Medium Discount`: $20\% - 40\%$
     * `Low Discount`: $< 20\%$
   * **Rating Categories**:
     * `Excellent`: Rating $\ge 4.5$
     * `Average`: Rating $3.0 - 4.4$
     * `Poor`: Rating $< 3.0$
     * `Unrated`: Missing review/rating data

---

## Key Insights & Findings

* **Discount Depth vs. Engagement**: High discounts ($>40\%$) account for over half of all product listings, but steep discounts alone do not guarantee higher review counts.
* **Rating Distribution**: Products categorized as `Excellent` ($\ge 4.5$) maintain consistent customer review counts regardless of whether the discount is low or medium.
* **Review Gap**: A significant portion of listed items ($47.8\%$) have zero customer reviews, indicating an opportunity for Jumia to incentivize post-purchase customer feedback.

---

## Dashboard Features

The dynamic dashboard sheet includes:
* **KPI Summary Cards**: Overview of overall average current prices, average discounts, total product counts, and overall mean ratings.
* **Top & Bottom Rankings**: Highlights top 10 discounted items, top 10 most reviewed products, and lowest-rated items.
* **Interactive Slicers**: Filter data dynamically by **Discount Category** and **Rating Category**.

---

##  Article: Excel's Strengths & Weaknesses in Predictive Analysis

### Excel's Role in Business Decision-Making
Microsoft Excel remains a core business intelligence tool due to its accessibility, immediate visual feedback, and intuitive formula engine. It enables decision-makers to rapidly prototype models, build dynamic summary reports, and run scenario analyses without technical coding prerequisites.

### Strengths in Predictive Analysis
* **Native Forecasting Tools**: Excel provides exponential smoothing (`FORECAST.ETS`) and linear regression trendlines built into chart tools.
* **Optimization with Solver**: Enables business leaders to optimize resource allocation subject to operational constraints.
* **Data Analysis ToolPak**: Offers statistical outputs including ANOVA, correlation matrices, and linear regression summaries.

### Weaknesses & Limitations
* **Scalability Bottlenecks**: Excel is limited to 1,048,576 rows, making it unsuitable for big data pipeline processing.
* **Lack of Advanced ML Algorithms**: Cannot natively construct complex non-linear models like Gradient Boosted Trees or Neural Networks.
* **Version Control & Manual Error Risk**: Formula dependencies can introduce hidden calculation bugs, and raw spreadsheets lack native version-control tracking.

---

## Repository Structure

```text
├── JUMIA DATA ANALYSIS.xlsx    # Main Excel workbook with raw data, cleaned data, & interactive dashboard
├── README.md                   # Project documentation and summary