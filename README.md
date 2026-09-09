# Superstore Sales & Profit Analysis — Tableau

## Project Overview

This project analyzes the **Superstore dataset** using Tableau.

The project was developed step by step while learning Tableau concepts from beginner to advanced level. Each lesson was applied directly to the dataset to answer business questions and generate insights.

The analysis covers sales, profit, customers, regions, categories, discounts, parameters, and time-based trends.

---

# Dataset

- **Dataset:** Superstore
- **Records:** 9,994
- **Columns:** 21

---

# Lesson 1–3 — Foundations and Basic Analysis

The first lessons focused on understanding the Tableau interface, dimensions, measures, visualizations, sorting, filters, and basic business analysis.

## Key Insights

### Sales by Region

| Region | Sales |
|---|---:|
| West | $725,457.82 |
| South | $391,721.91 |

**Insight:** West generated the highest sales, while South generated the lowest sales.

---

### Sales by Category

| Category | Sales |
|---|---:|
| Technology | $836,154.03 |
| Office Supplies | $719,047.03 |

**Insight:** Technology generated the highest sales, while Office Supplies generated the lowest sales.

---

### Monthly Sales Trend

- Highest sales month: **November 2017 — $118,447.83**
- Lowest sales month: **February 2014 — $4,519.89**

**Insight:** Monthly sales fluctuate over time, with November 2017 recording the highest sales in the analyzed period.

---

### Profit by Sub-Category

- Highest profit: **Copiers — $55,617.82**
- Lowest profit: **Tables — -$17,725.48**

**Insight:** High sales do not necessarily result in high profit. Tables are a clear example of a sub-category generating sales while producing a loss.

---

### Regional Profit

- Highest profit: **West — $108,418.45**
- Lowest profit: **Central — $39,706.36**

**Insight:** West performed strongly in both sales and profit.

---

# Lesson 4 — Groups and Sets

Lesson 4 focused on using Groups, Sets, Combined Sets, and Set Actions to analyze customer performance.

## Evidence

- Top 10 Sales customers: **10**
- Top 10 Profit customers: **10**
- Customers in both groups: **6**
- Customers in either group: **14**

## Insight

Only **6 customers** appeared in both the Top 10 Sales and Top 10 Profit groups.

This shows that strong sales performance does not automatically mean strong profit performance.

---

# Lesson 5 — Calculated Fields

Lesson 5 focused on creating calculated fields to generate new metrics and classify business performance.

## Profit Margin

### Regional Profit Margin

- Highest: **West — 14.94%**
- Lowest: **Central — 7.92%**

### Category Profit Margin

- Highest: **Technology — 17.40%**
- Lowest: **Furniture — 2.49%**

### Sub-Category Profit Margin

- Highest: **Labels — 44.42%**
- Lowest: **Tables — -8.56%**

**Insight:** Technology demonstrates strong performance in both sales and profitability, while Tables remain a major profitability concern.

---

## Average Sales per Unit

- Highest: **Copiers — $639.00**
- Lowest: **Fasteners — $3.30**

**Insight:** Copiers generate significantly higher sales value per unit compared with other sub-categories.

---

## Sales per Order

- Highest region: **East — $484.50**

**Insight:** East generated the highest average sales value per distinct order.

---

## Discount Analysis

| Discount Band | Profit Margin |
|---|---:|
| No Discount | 29.51% |
| Low Discount | 11.91% |
| Medium Discount | -15.30% |
| High Discount | -77.40% |

**Insight:** Higher discount bands are associated with substantially weaker profitability. Medium and High Discount bands are loss-making in this dataset.

---

## Profit Performance Classification

| Performance | Sub-Categories |
|---|---:|
| Loss | 3 |
| Low Profit | 5 |
| Strong Profit | 9 |

**Insight:** Although most sub-categories are profitable, not all generate strong profits.

---

# Lesson 6 — Parameters

Lesson 6 focused on creating dynamic and interactive visualizations using parameters.

The visualization can dynamically change the selected dimension and metric.

## Parameter Analysis Evidence

### Region + Profit

| Region | Profit |
|---|---:|
| West | $108,418.45 |
| East | $91,522.78 |
| South | $46,749.43 |
| Central | $39,706.36 |

**Insight:** West generated the highest regional profit.

---

### Category + Sales

| Category | Sales |
|---|---:|
| Technology | $836,154.03 |
| Furniture | $741,999.80 |
| Office Supplies | $719,047.03 |

**Insight:** Technology generated the highest category sales.

---

### Sub-Category + Quantity

- Highest quantity: **Binders — 5,974 units**

**Insight:** Binders recorded the highest quantity sold among the sub-categories.

---

## Lesson 6 Key Insight

Parameters allow the same visualization to answer multiple business questions without creating separate charts.

For example:

```text
Region + Profit
Category + Sales
Sub-Category + Quantity
```

# Lesson 7 — Table Calculations

Lesson 7 focused on using Tableau Table Calculations to analyze values already displayed in visualizations.

The analysis included:

- Running Total
- Difference From Previous
- Percent Difference From Previous
- Percent of Total
- Moving Average
- Table (Across)
- Table (Down)

---

## Running Total

The Running Total calculation shows how sales accumulate over time.

### Insight

Cumulative analysis provides a clearer view of overall sales growth across the analyzed period.

---

## Difference From Previous

This calculation compares each period's sales with the previous period.

### Insight

It helps identify whether sales increased or decreased between consecutive periods.

- Positive value indicates an increase.
- Negative value indicates a decrease.

---

## Percent Difference From Previous

This calculation shows the percentage change in sales compared with the previous period.

### Insight

Percentage change provides relative context for sales growth or decline between periods.

- Positive percentage indicates growth.
- Negative percentage indicates decline.

---

## Percent of Total Sales by Category

| Category | Contribution to Total Sales |
|---|---:|
| Technology | 36.40% |
| Furniture | 32.20% |
| Office Supplies | 31.30% |

### Insight

**Technology** contributes the largest share of total sales at **36.40%**.

Furniture contributes **32.20%**, while Office Supplies contributes **31.30%**.

---

## Moving Average

The Moving Average calculation smooths short-term sales fluctuations to make the overall trend easier to observe.

### Insight

A moving average helps identify the broader sales trend by reducing the impact of short-term fluctuations.

---

## Table (Across) vs Table (Down)

### Table (Across)

Calculates values from left to right.

This was used for time-based calculations such as:

- Running Total
- Difference From Previous
- Percent Difference From Previous
- Moving Average

### Table (Down)

Calculates values from top to bottom.

This was used for the category-level Percent of Total calculation because the categories were displayed vertically.

---

## Lesson 7 Key Insight

Table calculations add another layer of analysis to Tableau visualizations.

They make it possible to analyze:

- Cumulative performance
- Period-to-period changes
- Percentage changes
- Contribution to total
- Smoothed trends

These calculations help transform basic visualizations into more meaningful time-based and comparative business analysis.

# Lesson 8 — Interactive Dashboard

Lesson 8 focused on creating and formatting an interactive Tableau dashboard using the Superstore dataset.

## Concepts Practiced

- Dashboard creation and layout
- Worksheet positioning
- Dashboard title and subtitle
- Chart formatting
- Gridline removal
- Number and currency formatting
- Dashboard filters
- Applying filters to multiple worksheets
- Filter Actions
- Highlight Actions
- Clearing filter selections
- Tooltip customization
- Dashboard usability and testing

## Dashboard Components

The dashboard combines four worksheets:

- Monthly Sales Trend
- Sales by Region
- Sales by Category
- Profit by Sub-Category

## Year Filter

The `Year of Order Date` filter was applied to all four worksheets.

Selecting a year updates the complete dashboard, while clearing the filter returns the dashboard to the overall view.

```text
Select Year
     ↓
All Charts Update
     ↓
Clear Filter
     ↓
Overall Dashboard Returns
```
## Region Filter Action

A Filter Action was created using Sales by Region.

Selecting a region filters the other dashboard charts. Clearing the selection returns the charts to their original state.

## Category Highlight Action

A Highlight Action was created using Sales by Category.

Selecting a category highlights the related sub-categories in Profit by Sub-Category while keeping other sub-categories visible.

The Category field was added to the Detail shelf to enable the highlight interaction.
```
Select Category
     ↓
Related Sub-Categories Highlight
     ↓
Other Data Remains Visible
```
## Tooltip Customization

Custom tooltips were created for all four charts:

Monthly Sales Trend → Date and Sales
Sales by Region → Region and Sales
Sales by Category → Category and Sales
Profit by Sub-Category → Sub-Category and Profit
Dashboard Formatting

The dashboard was cleaned using:
```
Gridline removal
Currency formatting
Consistent chart presentation
Clear titles
Subtitle
Improved spacing
Clean layout
Interactive filters and actions
```
## Outcome

The Superstore analysis was transformed into an interactive Tableau dashboard that allows users to filter by year, filter by region, highlight categories, and explore detailed information through customized tooltips.

# Lesson 9 — Dashboard Navigation

Lesson 9 focused on making the Tableau workbook easier to navigate and explore.

## Key Concepts

- Created a `Detailed Analysis Dashboard`
- Added navigation buttons between dashboards
- Configured two-way dashboard navigation
- Used floating objects for button positioning
- Added tooltips to navigation buttons
- Tested the complete dashboard navigation flow

## Navigation Flow

```text
Main Dashboard
      ↓
Detailed Analysis
      ↓
Detailed Analysis Dashboard
      ↓
Back to Sales Dashboard
      ↓
Main Dashboard
```
## Outcome

Created a user-friendly Tableau workbook with seamless navigation between the main dashboard and detailed analysis dashboard.
