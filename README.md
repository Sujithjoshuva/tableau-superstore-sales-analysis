# Superstore Sales & Profit Analysis — Tableau

## Project Overview

This project analyzes the Superstore dataset using Tableau to understand sales, profit, customer, product, and regional performance.

The project is being developed step by step while learning Tableau from beginner to advanced level.

The Tableau workbook contains the analysis created during the learning process and will be expanded as new Tableau concepts are learned.

## Dataset

- Dataset: Superstore
- Records: 9,994
- Columns: 21

### Key Fields

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

## Business Questions

The analysis currently explores questions such as:

- Which region generates the highest sales?
- Which category generates the highest sales?
- How do sales change over time?
- Which sub-categories generate the highest and lowest profit?
- Which region and category combinations generate the highest sales?
- Which regions generate the highest profit?
- Which customers generate the highest sales?
- Which customers are the top Technology customers by sales?

## Tableau Worksheets

The current workbook contains 9 worksheets.

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

## Tableau Skills Practiced

### Foundations

- Dimensions and Measures
- Discrete and Continuous fields
- Date fields
- Geographic fields
- Aggregation
- SUM of measures

### Visualizations

- Bar charts
- Line charts
- Highlight tables
- Sales trends
- Profit analysis

### Analysis

- Sorting
- Basic filters
- Show Filters
- Top N filters
- Context filters

## Initial Findings

- West has the highest overall sales at **$725,457.82**.
- South has the lowest overall sales at **$391,721.91**.
- Technology has the highest category sales at **$836,154.03**.
- Office Supplies has the lowest category sales at **$719,047.03**.
- Copiers have the highest sub-category profit at **$55,617.82**.
- Tables have the lowest sub-category profit at **-$17,725.48**.
- November 2017 recorded the highest monthly sales at **$118,447.83**.
- February 2014 recorded the lowest monthly sales at **$4,519.89**.
- West + Furniture recorded the highest Region × Category sales combination at **$252,612.74**.
- West has the highest regional profit at **$108,418.45**.
- Central has the lowest regional profit at **$39,706.36**.

## Project Structure

```text
tableau-superstore-sales-analysis/
│
├── tableau/
│   └── Superstore_Sales_Analysis.twbx
│
└── README.md
