# Superstore Sales & Profit Analysis — Tableau

## Project Overview

This project analyzes the **Superstore dataset** using Tableau to understand sales, profit, customer, product, regional, and discount performance.

The project is being developed step by step while learning Tableau from beginner to advanced level.

Each lesson combines Tableau concepts with practical business analysis using the Superstore dataset. The Tableau workbook is continuously updated as new concepts are learned.

The goal is to build practical Tableau skills while creating a professional, portfolio-ready analytics project.

---

# Dataset

- **Dataset:** Superstore
- **Records:** 9,994
- **Columns:** 21

## Key Fields

- Order ID
- Order Date
- Ship Date
- Customer ID
- Customer Name
- Segment
- Country
- City
- State
- Region
- Product ID
- Category
- Sub-Category
- Product Name
- Sales
- Quantity
- Discount
- Profit

---

# Business Questions

The analysis currently explores questions such as:

- Which region generates the highest sales?
- Which category generates the highest sales?
- How do sales change over time?
- Which sub-categories generate the highest and lowest profit?
- Which region and category combinations generate the highest sales?
- Which regions generate the highest profit?
- Which customers generate the highest sales?
- Which customers are the top Technology customers by sales?
- Which customers are among the Top 10 in both Sales and Profit?
- How does profit margin differ across regions, categories, and sub-categories?
- Which sub-categories have high sales but low or negative profitability?
- How does discount level relate to profitability?
- Which sub-categories have low, medium, or high sales performance?

---

# Tableau Worksheets

The workbook currently contains **25 worksheets** covering Tableau concepts from foundational analysis through calculated fields.

---

## Lessons 1–3: Tableau Foundations and Analysis

### 1. Sales by Region

Compares total sales across the four regions.

### 2. Sales by Category

Compares total sales across Furniture, Office Supplies, and Technology.

### 3. Monthly Sales Trend

Shows monthly sales over time using Order Date and Sales.

### 4. Profit by Sub-Category

Compares profit across product sub-categories and identifies profitable and loss-making sub-categories.

### 5. Regional Highlight Table

Compares sales across Region and Category combinations using a highlight table.

### 6. Profit by Region

Compares total profit across regions.

### 7. Sales by Region

Shows sales by region with Category available as a filter.

### 8. Top 10 Customers

Identifies the top 10 customers based on total sales.

### 9. Top 10 Technology Customers

Identifies the top 10 customers by sales within the Technology category using a context filter.

---

# Lesson 4 — Groups and Sets

Lesson 4 focused on Tableau Groups, Sets, Combined Sets, and Set Actions.

## Concepts Practiced

- Creating Groups
- Creating Top N Sets
- IN vs OUT members
- Combining Sets
- AND logic
- OR logic
- Set Actions
- Interactive Set-based analysis

## Set Analysis Results

- Top 10 Sales customers: **10**
- Top 10 Profit customers: **10**
- Customers in both Sales and Profit Top 10: **6**
- Customers in Sales or Profit Top 10: **14**

## Key Finding

Only **6 customers** belong to both the Top 10 Sales and Top 10 Profit groups.

This demonstrates that high sales performance does not necessarily mean a customer ranks equally high in profit.

## Set Action

A Set Action was created to allow users to select a region and dynamically update the customer analysis.

---

# Lesson 5 — Calculated Fields

Lesson 5 focused on creating calculated fields and using conditional logic to generate new analytical metrics and business classifications.

---

## Calculated Fields Created

### Profit Margin

```text
SUM([Profit]) / SUM([Sales])
```

Measures the percentage of sales converted into profit.

### Average Sales per Unit

```text
SUM([Sales]) / SUM([Quantity])
```

Measures the average sales value associated with each unit sold.

### Sales per Order

```text
SUM([Sales]) / COUNTD([Order ID])
```

Measures the average sales value per distinct order.

### Profit Status

```text
IF SUM([Profit]) > 0 THEN
    "Profitable"
ELSE
    "Loss-making"
END
```

Classifies sub-categories based on whether their aggregated profit is positive or negative.

### Profit Performance

```text
IF SUM([Profit]) < 0 THEN
    "Loss"
ELSEIF SUM([Profit]) < 10000 THEN
    "Low Profit"
ELSE
    "Strong Profit"
END
```

Classifies sub-categories into three profit-performance groups.

### Discount Band

```text
IF [Discount] = 0 THEN
    "No Discount"
ELSEIF [Discount] <= 0.20 THEN
    "Low Discount"
ELSEIF [Discount] <= 0.40 THEN
    "Medium Discount"
ELSE
    "High Discount"
END
```

Classifies records according to discount level.

### Sales Performance

```text
IF SUM([Sales]) < 100000 THEN
    "Low Sales"
ELSEIF SUM([Sales]) <= 200000 THEN
    "Medium Sales"
ELSE
    "High Sales"
END
```

Classifies sub-categories according to total sales.

---

# Lesson 5 Worksheets

### 16. Profit Margin Analysis

Analyzes profit margin across regions.

### 17. Profit Margin by Category

Compares profit margins across product categories.

### 18. Profit Margin by Sub-Category

Compares profit margins across product sub-categories.

### 19. Average Sales per Unit

Analyzes average sales value per unit across sub-categories.

### 20. Sub-Category Metrics

Compares Sales, Profit, Profit Margin, Quantity, and Average Sales per Unit.

### 21. Sales per Order

Analyzes average sales value per distinct order across regions.

### 22. Profit Status by Sub-Category

Classifies sub-categories as Profitable or Loss-making.

### 23. Profit Performance

Classifies sub-categories as Loss, Low Profit, or Strong Profit.

### 24. Discount Band

Analyzes sales, profit, and profit margin across discount levels.

### 25. Sales Performance

Classifies sub-categories into Low, Medium, and High Sales groups.

---

# Key Findings

## Sales Performance

- **West** has the highest overall sales at **$725,457.82**.
- **South** has the lowest overall sales at **$391,721.91**.
- **Technology** has the highest category sales at **$836,154.03**.
- **Office Supplies** has the lowest category sales at **$719,047.03**.
- **November 2017** recorded the highest monthly sales at **$118,447.83**.
- **February 2014** recorded the lowest monthly sales at **$4,519.89**.

---

## Profit Performance

- **Copiers** have the highest sub-category profit at **$55,617.82**.
- **Tables** have the lowest sub-category profit at **-$17,725.48**.
- **West** has the highest regional profit at **$108,418.45**.
- **Central** has the lowest regional profit at **$39,706.36**.

---

## Region × Category Analysis

- **West + Furniture** recorded the highest Region × Category sales combination at **$252,612.74**.
- **South + Furniture** recorded the lowest Region × Category sales combination at **$117,298.68**.
- **East** has the highest Technology sales at **$264,973**.
- **South** has the lowest Technology sales at **$148,771**.

---

## Customer Analysis

- Top customer by sales: **Tamara Chand — $25,043**
- 10th-ranked customer by sales: **Christopher — $12,129**
- Top Technology customer: **Sean Miller — $23,481**
- 10th-ranked Technology customer: **Becky Martin — $8,382**

---

# Profit Margin Analysis

## Regional Profit Margin

- Highest regional profit margin: **West — 14.94%**
- Lowest regional profit margin: **Central — 7.92%**

## Category Profit Margin

- Highest category profit margin: **Technology — 17.40%**
- Lowest category profit margin: **Furniture — 2.49%**

## Sub-Category Profit Margin

- Highest sub-category profit margin: **Labels — 44.42%**
- Lowest sub-category profit margin: **Tables — -8.56%**

---

# Unit Economics

## Average Sales per Unit

- Highest average sales per unit: **Copiers — $639.00**
- Lowest average sales per unit: **Fasteners — $3.30**

## Sales per Order

- Highest Sales per Order region: **East — $484.50**

### Key Insight

Average Sales per Unit and Sales per Order measure different aspects of the business.

**Average Sales per Unit** measures the average sales value associated with each unit sold.

**Sales per Order** measures the average sales value generated by each distinct order.

---

# Sub-Category Comparison

Three sub-categories were compared across Sales, Profit, Profit Margin, Quantity, and Average Sales per Unit.

| Metric | Copiers | Labels | Tables |
|---|---:|---:|---:|
| Sales | $149,528 | $12,486 | $206,966 |
| Profit | $55,618 | $5,546 | -$17,725 |
| Profit Margin | 37.20% | 44.42% | -8.56% |
| Quantity | 234 | 1,400 | 1,241 |
| Average Sales per Unit | $639.00 | $8.90 | $166.80 |

### Copiers

Copiers generate relatively high-value sales per unit and strong total profit.

- Sales: **$149,528**
- Profit: **$55,618**
- Profit Margin: **37.20%**
- Quantity: **234**
- Average Sales per Unit: **$639.00**

### Labels

Labels have the highest profit margin among the three but a much lower average sales value per unit.

- Sales: **$12,486**
- Profit: **$5,546**
- Profit Margin: **44.42%**
- Quantity: **1,400**
- Average Sales per Unit: **$8.90**

### Tables

Tables generate high sales but are loss-making.

- Sales: **$206,966**
- Profit: **-$17,725**
- Profit Margin: **-8.56%**
- Quantity: **1,241**
- Average Sales per Unit: **$166.80**

### Key Insight

Tables generate substantially higher sales than Copiers and Labels in this comparison, but they produce negative profit.

Copiers generate lower sales than Tables but produce substantially higher profit.

This demonstrates why **sales alone should not be used to evaluate business performance**.

---

# Profit Classification

The 17 sub-categories were classified into three groups based on total profit.

| Profit Performance | Number of Sub-Categories |
|---|---:|
| Loss | **3** |
| Low Profit | **5** |
| Strong Profit | **9** |
| **Total** | **17** |

### Loss-Making Sub-Categories

- Tables
- Bookcases
- Supplies

### Key Insight

Although **14 of 17 sub-categories are profitable**, only **9** generate strong profit based on the classification threshold.

---

# Discount Analysis

| Discount Band | Sales | Profit | Profit Margin |
|---|---:|---:|---:|
| No Discount | $1,087,908 | $320,988 | 29.51% |
| Low Discount | $846,522 | $100,785 | 11.91% |
| Medium Discount | $234,138 | -$35,817 | -15.30% |
| High Discount | $128,632 | -$99,559 | -77.40% |

## Discount Analysis Findings

Profitability declines sharply across the discount bands.

- No Discount: **29.51% profit margin**
- Low Discount: **11.91% profit margin**
- Medium Discount: **-15.30% profit margin**
- High Discount: **-77.40% profit margin**

### Key Insight

Higher discount bands are **associated with substantially weaker profitability** in this dataset.

Medium and High Discount bands are loss-making.

The analysis shows an association rather than proving that higher discounts directly cause the losses. Further analysis would be required before making a causal conclusion.

---

# Sales Performance Classification

The 17 sub-categories were classified into three sales-performance groups.

| Sales Performance | Number of Sub-Categories |
|---|---:|
| Low Sales | **7** |
| Medium Sales | **5** |
| High Sales | **5** |
| **Total** | **17** |

---

# Tableau Skills Practiced

## Foundations

- Dimensions and Measures
- Discrete and Continuous fields
- Date fields
- Geographic fields
- Aggregation
- SUM
- AVG
- Number formatting

## Visualizations

- Bar charts
- Line charts
- Highlight tables
- Sales trends
- Profit analysis
- Multi-measure comparisons

## Filters and Analysis

- Sorting
- Basic filters
- Show Filters
- Top N filters
- Context filters

## Groups and Sets

- Groups
- Sets
- Combined Sets
- AND logic
- OR logic
- IN and OUT members
- Set Actions
- Interactive set analysis

## Calculated Fields

- Mathematical calculations
- Aggregated calculations
- Ratio calculations
- `SUM()`
- `AVG()`
- `COUNTD()`
- `IF`
- `ELSEIF`
- `ELSE`
- Conditional classification
- Profit Margin
- Average Sales per Unit
- Sales per Order
- Profit Status
- Profit Performance
- Discount Band
- Sales Performance

---

# Key Business Insights

Several important patterns have emerged from the analysis.

### 1. West is the strongest region overall

West has the highest overall sales and the highest regional profit margin.

### 2. Technology is the strongest category by sales and margin

Technology has the highest category sales and the highest category profit margin.

### 3. Tables are a major profitability concern

Tables generate substantial sales but produce negative profit and a negative profit margin.

### 4. Copiers demonstrate strong unit economics

Copiers have the highest average sales per unit and the highest sub-category profit.

### 5. Labels have the highest profit margin

Labels have a **44.42% profit margin**, although their low average sales per unit limits their total sales and profit.

### 6. Discounting is strongly associated with weaker profitability

Profit margin falls from **29.51% with no discount** to **-77.40% at high discounts**.

### 7. Sales and profitability are not always aligned

A sub-category can generate high sales while producing low or negative profit.

This highlights the importance of analyzing **Sales, Profit, Profit Margin, Quantity, and unit-level metrics together**.

---

# Project Structure

```text
tableau-superstore-sales-analysis/
│
├── tableau/
│   ├── Superstore_Sales_Analysis.twbx
│   └── Superstore_Sales_Analysis_Lesson_5.twbx
│
└── README.md
```

---

# Project Progress

## Completed

- Tableau Foundations
- Basic Visualizations
- Dimensions and Measures
- Aggregation
- Sorting
- Filters
- Top N Filters
- Context Filters
- Groups
- Sets
- Combined Sets
- AND / OR Set Logic
- Set Actions
- Calculated Fields
- Conditional Calculations
- Profitability Analysis
- Customer Analysis
- Discount Analysis
- Sales Performance Analysis

## Current Stage

**Lesson 5 — Calculated Fields completed**

The Lesson 5 Tableau workbook has been uploaded to the repository.

## Next

Continue learning advanced Tableau concepts and apply each new concept to the Superstore dataset while maintaining a professional, portfolio-ready project structure.

---

# Learning Approach

This project follows a practical learning workflow:

```text
Learn Tableau Concept
        ↓
Practice the Concept
        ↓
Apply It to Superstore
        ↓
Analyze the Results
        ↓
Document Business Findings
        ↓
Update GitHub
```

The objective is not only to learn Tableau features, but to understand **how Tableau can be used to answer real business questions and communicate data-driven insights**.
