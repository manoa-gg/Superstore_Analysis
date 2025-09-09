# Superstore_Analysis
Sales Performance & Customer Profitability Dashboard
## 📖 Overview
This repository contains a comprehensive data analysis project built in Google Sheets. The project transforms raw sales transaction data into a cleaned, analyzable dataset and performs an in-depth analysis to uncover key business insights regarding discount strategies, customer acquisition costs, and customer lifetime value.

The analysis reveals critical findings about the sustainability of the company's discount-heavy sales strategy and provides actionable strategic recommendations.

## 📊 Live Dashboard
Access the Google Sheet here: [LINK TO YOUR GOOGLE SHEET]
(Note: Ensure the sharing permissions are set to "Anyone with the link can view")

## 🗂️ Repository Structure & Documentation
The Google Sheet is organized into several key tabs:

Tab Name	Description
raw	The original, unaltered dataset as received.
cleaned	The processed data ready for analysis. Key transformations applied are listed below.
pivot_overview	Preliminary pivot tables for a high-level assessment of the data.
metric_1_discount_grossmargin	Contains the analysis and charts for Discount Rate and Gross Margin.
metric_2_cac	Contains the analysis and charts for Customer Acquisition Cost (CAC).
metric_3_clv	Contains the analysis and charts for Customer Lifetime Value (CLV).
key_insights	A summary of the final key insights and strategic recommendations.
🔧 Data Cleaning & Transformation
The following operations were performed on the raw data to create the cleaned dataset:

Data Integrity: Removed blank rows and deleted duplicate entries.

Column Management: Deleted unrelated columns (e.g., row id, country, postal code). Split text to columns where necessary.

Numerical Transformations:

Added Unit Price (Sales / Quantity)

Added Discount Amount (Sales * Discount)

Added Profit Margin (Profit / Sales)

Added COGS (Sales - Profit)

Applied conditional formatting to numerical columns to visualize value ranges clearly.

Temporal Transformations:

Extracted Order Day, Order Month, and Order Year from Order Date.

Calculated Shipping Time in Days (Ship Date - Order Date).

Boolean Transformation: Created a Discount (B) column (Yes/No) based on the presence of a discount.

Customer Analysis: Added an Is New Customer flag (implementation logic may vary).

## 📈 Analysis Performed
The analysis answered the following key business questions:

1. General Data Assessment:

Statistical analysis (sum, average, count) on Sales, Profit, Quantity, and Discount.

Count of orders with/without discount and with profit/loss.

Temporal analysis: orders by year, month, and day of the week.

Count of unique customers, cities, states, and products.

Sub-category performance: total sales, number of orders, and discount penetration.

2. Key Metrics Calculated:

Discount Rate & Gross Margin: Analyzed the relationship and impact on overall profitability.

Customer Acquisition Cost (CAC): Calculated and analyzed the trend over time. (Total Discount Amount / Number of New Customers).

Customer Lifetime Value (CLV): Calculated for each customer. Identified the top and bottom 10 customers by profitability.

3. Preliminary Charts Created:

Relation between discount and quantity sold.

Profit vs. COGS by sub-category.

Profit/Loss trend between years.

Dedicated charts for each of the three main metrics.

## 🔍 Key Insights
The analysis uncovered several critical insights about the business:

Unsustainable Discount Strategy: High discount rates (averaging ~73%) consume nearly all gross margin, creating significant financial risk. Sales growth is parallelled by rising discount costs.

Ineffective Customer Acquisition: The cost to acquire a new customer (CAC) became prohibitively expensive by 2017 ($3,613), indicating deep discounts have severely diminishing returns.

Extreme Customer Polarization: A small cohort of "Champion" customers is highly profitable (avg. 39.6% GM), while a large group of "Liability" customers is catastrophically unprofitable (avg. -53.8% GM), masking massive losses.

## 💡 Strategic Recommendations
Based on the insights, the following strategic actions are recommended:

Immediate Actions (0-3 Months):

Revise Discount Strategy: Immediately prohibit discounts on low-margin products (<15% GM). Implement a system-wide "Red Line" policy to block discounts that push margin below a set threshold.

Customer Triage: Freeze all sales activity for the top 10 least profitable customers and begin cost-to-serve analysis.

Medium-Term Actions (3-12 Months):

Diversify Marketing: Reallocate 50% of the discount budget to brand-building activities (content, SEO, social media) to reduce reliance on price-based acquisition.

Renegotiate or Exit: For unprofitable customers, renegotiate terms to achieve minimum profitability or exit the relationship entirely.

Long-Term Strategy (12+ Months):

Implement CLV Segmentation: Formalize customer tiers (A, B, C) based on profitability and lifetime value. Direct resources to acquiring and retaining high-CLV customers.

Shift to Value-Based Selling: Develop loyalty programs and value-added services to compete on value rather than price.

## 🛠️ How to Use This Analysis
View the Dashboard: Open the Google Sheet and navigate through the tabs to see the raw data, cleaning process, and analysis.

Interact with Pivots: Feel free to filter the pivot tables on the pivot_overview and metric tabs to slice the data by different dimensions (e.g., year, segment, category).

Understand the Logic: Formulas are used throughout the cleaned and metric tabs. You can click on cells to see the calculations for metrics like Profit Margin, CLV, and CAC.

## ⁉️ Notes & Limitations
The Is New Customer flag is a simplification. A more robust implementation would require a complete transaction history to accurately identify a customer's first order.

CAC is calculated using Discount Amount as a proxy for marketing spend. A real-world calculation would include all marketing and sales expenses.

The analysis is based on historical data. Market conditions and customer behavior can change.
