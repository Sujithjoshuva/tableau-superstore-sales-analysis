# Superstore Sales & Profit Analysis — Tableau

## Project Overview

An end-to-end Tableau project using the **Superstore dataset** to analyze sales, profit, customers, regions, categories, discounts, and business performance.

The project progresses from basic Tableau concepts to **interactive dashboards, Sets, Parameters, Table Calculations, and LOD Expressions**.

## Dataset

- **Dataset:** Superstore
- **Records:** 9,994
- **Columns:** 21

---

# Lessons & Key Outcomes

## Lesson 1–3 — Tableau Foundations

Learned:

- Dimensions and Measures
- Basic charts and visualizations
- Sorting and filtering
- Sales and profit analysis
- Customer analysis
- Regional and category analysis

### Key Findings

- West Sales: **$725,457.82**
- South Sales: **$391,721.91**
- Technology Sales: **$836,154.03**
- Copiers Profit: **$55,617.82**
- Tables Profit: **-$17,725.48**

---

## Lesson 4 — Groups & Sets

Learned:

- Groups
- Sets
- Top N Sets
- Combined Sets
- Set Actions
- IN / OUT analysis

### Finding

- Top 10 Sales & Profit overlap: **6 customers**

Sales performance and profit performance do not always identify the same customers.

---

## Lesson 5 — Calculated Fields

Created calculations for:

- Profit Margin
- Average Sales per Unit
- Sales per Order
- Profit Status
- Profit Performance
- Discount Band
- Sales Performance

### Key Findings

- Technology Profit Margin: **17.40%**
- Furniture Profit Margin: **2.49%**
- Labels Profit Margin: **44.42%**
- Tables Profit Margin: **-8.56%**
- High Discount Profit Margin: **-77.40%**

**Insight:** Sales volume alone does not fully represent profitability.

---

## Lesson 6 — Parameters

Created dynamic parameters for:

- Metric Selection
- Dimension Selection

The same visualization can dynamically analyze:

```text
Region + Profit
Category + Sales
Sub-Category + Quantit
```

# Lesson 7 — Table Calculations

Learned Tableau Table Calculations for time-based and comparative analysis.

## Concepts

- Running Total
- Difference From Previous
- Percent Difference From Previous
- Percent of Total
- Moving Average
- Table Across / Table Down

### Category Sales Contribution

| Category | Contribution |
|---|---:|
| Technology | 36.40% |
| Furniture | 32.20% |
| Office Supplies | 31.30% |

**Key Insight:** Technology contributed the largest share of total sales.

---

# Lesson 8 — Interactive Dashboard

Built the **Superstore Sales Performance Dashboard**.

## Features

- Monthly Sales Trend
- Sales by Region
- Sales by Category
- Profit by Sub-Category
- Year Filter
- Region Filter Action
- Category Highlight Action
- Custom Tooltips

**Outcome:** Created an interactive dashboard for exploring sales, profit, regional, category, and time-based performance.

---

# Lesson 9 — Dashboard Navigation

Focused on dashboard navigation and user flow.

## Concepts

- Navigation Buttons
- Two-Way Navigation
- Floating Objects
- Navigation Tooltips

```text
Main Dashboard
      ↓
Detailed Analysis
      ↓
Back to Sales Dashboard
```
Outcome: Created seamless navigation between dashboards.

# Lesson 10 — Dashboard Usability

Improved dashboard usability and filter management.

## Concepts
- Show/Hide Containers
- Vertical Containers
- Collapsible Filter Panel
- Show/Hide Buttons
- Filter Organization

**Outcome:** Created a cleaner and more user-friendly dashboard experience.

---

# Lesson 11 — Dashboard Design & UX

Focused on improving dashboard layout and visual consistency.

## Improvements
- Fixed dashboard size: **1155 × 592 px**
- Visual hierarchy
- Chart alignment
- Spacing
- Control positioning
- Readability

**Outcome:** Improved dashboard structure and user experience.

---

# Lesson 12 — Dashboard Performance

Focused on workbook cleanup and performance optimization.

## Reviewed
- Unused worksheets
- Duplicate actions
- Unnecessary filters
- Unused calculations
- Dashboard responsiveness

**Outcome:** Improved workbook organization and verified smooth dashboard performance.

---

# Lesson 13 — Advanced Sets

Focused on interactive Tableau Sets.

## Concepts
- Dynamic Sets
- Set Controls
- Set Actions
- IN / OUT Membership
- Interactive Filtering

Created a `Category Control Set` to dynamically filter sub-category analysis.

**Outcome:** Learned to build interactive Set-based analysis.

---

# Lesson 14 — LOD Expressions

Focused on advanced Tableau calculations using Level of Detail expressions.

## Concepts
- FIXED
- INCLUDE
- EXCLUDE
- Context Filters
- LOD Aggregations
- Customer & Regional Analysis

### Average Sales per Customer

```text
AVG(
    { FIXED [Region], [Customer Name] : SUM([Sales]) }
)
```
| Region | Average Sales per Customer |
|---|---:|
| West | $1,057.52 |
| East | $1,007.09 |
| Central | $796.88 |
| South | $765.08 |

### LOD Comparison

- **FIXED** → Calculate at a specified level
- **INCLUDE** → Add a dimension to the calculation
- **EXCLUDE** → Remove a dimension from the calculation

Also practiced Context Filters and customer benchmarking against regional averages.

**Outcome:** Learned to use LOD expressions for advanced customer, regional, and profitability analysis.

---

## Skills Practiced

- Tableau
- Dashboard Design
- Dashboard Usability
- Sets & Set Actions
- Calculated Fields
- LOD Expressions
- FIXED / INCLUDE / EXCLUDE
- Context Filters
- Customer Analysis
- Regional Analysis
- Business Analysis
