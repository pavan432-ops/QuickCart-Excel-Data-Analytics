# 🛒 QuickCart – Sales & Operations Analytics

> 📊 An end-to-end Excel Data Analyst portfolio project simulating a real-world Sales & Operations analytics workflow for a fictional e-commerce / quick-commerce company.

---

## 📌 1. Project Overview

QuickCart is a fictional e-commerce / quick-commerce company created for a practical Data Analyst project.

This project simulates the work of a **Junior Data Analyst – Sales & Operations** who receives business data, inspects raw datasets, identifies data-quality issues, cleans and validates the data, performs analysis, and creates an interactive Excel dashboard for management reporting.

The project focuses on the complete analytical workflow:

**Business Request → Data Inspection → Data Cleaning → Data Validation → Data Transformation → Analysis → PivotTables → PivotCharts → Slicers → Dashboard → Business Insights**

The objective was not simply to create a dashboard. The project focused on understanding the complete journey from raw business data to a validated management report.

---

## 🏢 2. Business Scenario

QuickCart operates as a fictional e-commerce / quick-commerce business with customers, products, stores, orders, deliveries, inventory and returns.

As a Junior Data Analyst supporting the Sales & Operations team, the analyst receives multiple raw Excel datasets.

### Manager Request

> "Please prepare an initial analysis of our order data. Before creating any report, inspect the raw data and identify the data-quality issues that could affect our analysis."

The project therefore started with **raw-data inspection and profiling** before major transformations were performed.

### Key Principle

> ⚠️ **Do not modify raw data before understanding what is wrong with it.**

Raw data was preserved separately from the cleaned working data.

---

## 🎯 3. Business Objective

The main objectives of the project were:

- 🔍 Understand the structure of QuickCart's business data.
- 📊 Profile the raw datasets.
- ⚠️ Identify data-quality issues.
- 🧹 Clean clearly invalid data.
- 🔐 Preserve legitimate missing information where appropriate.
- ⚠️ Distinguish data-quality errors from genuine business exceptions.
- 🧮 Create calculated fields.
- 🔎 Enrich transactional data using lookup functions.
- 📈 Analyze revenue and order performance.
- 🛍️ Analyze product categories.
- 🌐 Analyze order channels.
- 🚚 Analyze delivery performance.
- 📦 Analyze inventory exceptions.
- 🔄 Analyze returns.
- 📊 Build PivotTables.
- 📈 Build PivotCharts.
- 🎛️ Add interactive slicers.
- 💼 Build a professional management dashboard.
- 💡 Generate business insights.
- 📚 Document the complete analytical process.

---

## 👨‍💻 4. Analyst Role & Responsibilities

### Role

**Junior Data Analyst – Sales & Operations**

The project simulated responsibilities commonly associated with an entry-level Data Analyst.

### Responsibilities

- 📂 Receive raw business data.
- 🔍 Inspect datasets before modification.
- 📊 Profile data.
- 🧹 Clean invalid records.
- 🔎 Identify duplicates.
- ⚠️ Identify missing values.
- 🔢 Validate numeric values.
- 📅 Validate dates.
- 📝 Standardize inconsistent text.
- 🧮 Create calculated columns.
- 🔎 Apply XLOOKUP.
- 📊 Create analysis summaries.
- 📌 Create PivotTables.
- 📈 Create PivotCharts.
- 🎛️ Create interactive slicers.
- 🎨 Design a management dashboard.
- ✅ Validate calculations.
- 💡 Interpret business metrics.
- 📋 Document findings.

---

## 📂 5. Data Sources

The QuickCart project originally consisted of multiple Excel files representing different business areas.

### Raw datasets

1. 👥 Customers
2. 🛍️ Products
3. 🏪 Stores
4. 🛒 Orders
5. 🚚 Delivery
6. 📦 Inventory
7. 🔄 Returns

The datasets were combined into a working workbook:

**`QuickCart_Data.xlsx`**

A separate cleaned workbook was created:

**`QuickCart_Cleaned.xlsx`**

The raw workbook was preserved so that the original data could be referenced during validation.

---

## 🗃️ 6. Excel Tables

All seven datasets were converted into Excel Tables using:

**Ctrl + T**

The final table names were:

| Dataset | Excel Table |
|---|---|
| Customers | `customer_table` |
| Products | `products_table` |
| Orders | `orders_table` |
| Stores | `stores_table` |
| Delivery | `delivery_table` |
| Inventory | `inventory_table` |
| Returns | `returns_table` |

Using Excel Tables made it easier to:

- Use structured references.
- Create dynamic formulas.
- Maintain expanding ranges.
- Build PivotTables.
- Build lookup formulas.
- Work with larger datasets.
- Keep calculations consistent.

---

## 👥 7. Customer Dataset

The Customer dataset contained customer master information.

### Columns

- Customer_ID
- Customer_Name
- Gender
- Age
- City
- Customer_Segment
- Signup_Date

### Dataset Size

**5,002 customer records**

### Data Profiling Findings

The following issues were identified:

- 🔴 2 duplicate Customer_ID cells.
- 🔴 2 missing Age values.
- 🔴 City inconsistency:
  - `Hyd`
  - `Hyderabad`

### Cleaning Performed

Duplicate customer records were removed using Excel's **Remove Duplicates** feature.

The city inconsistency was standardized:

`Hyd → Hyderabad`

The replacement was performed using **Find & Replace** with **Match entire cell contents**.

An initial replacement attempt caused an unintended result:

`Hyderabad → Hyderabaderabad`

The mistake was immediately reversed using:

**Ctrl + Z**

The replacement was then correctly performed using **Match entire cell contents**.

The two missing Age values were intentionally left blank.

No age was invented because there was insufficient evidence to determine the correct value.

### Learning

Missing data should not automatically be replaced with assumptions simply to make the dataset appear complete.

---

## 🛍️ 8. Products Dataset

The Products dataset represented product master information.

### Columns

- Product_ID
- Product_Name
- Category
- Subcategory
- Brand
- Cost_Price
- Selling_Price

### Dataset Size

**500 products**

### Product Categories

Six product categories were identified:

- Electronics
- Beauty
- Beverages
- Grocery
- Fashion
- Home

### Data Quality Issue

One negative Selling_Price value was identified.

### Cleaning Decision

The negative Selling_Price value was cleared because a negative selling price was considered invalid for this analysis.

Product_ID uniqueness was also checked.

No duplicate Product_ID was observed during profiling.

---

## 🏪 9. Stores Dataset

The Stores dataset represented QuickCart's store and operational locations.

### Columns

- Store_ID
- Store_Name
- City
- State
- Region
- Store_Type

### Dataset Size

**40 stores**

### Findings

A city inconsistency was identified:

`Hyd` vs `Hyderabad`

The source also contained store types such as:

- `darkstore`
- `fullfillment center`

The original source terminology was preserved rather than silently changing business terminology without a defined requirement.

The dataset contained:

- 7 states
- 4 regions
- 2 store types

---

## 🛒 10. Orders Dataset

The Orders dataset was the main transactional dataset used for sales and revenue analysis.

### Columns

- Order_ID
- Order_Date
- Customer_ID
- Product_ID
- Store_ID
- Quantity
- Unit_Price
- Discount
- Payment_Method
- Order_Channel
- Net_Sales

### Dataset Size

**50,003 orders**

### Issues Identified

The profiling process identified:

- Missing Customer_ID values.
- Negative Quantity.
- Negative Unit_Price.
- Invalid Order_Date.
- Negative Discount values.
- Missing inputs affecting Net_Sales.
- One order without an Order_Date.

### Cleaning Performed

The following invalid values were cleared:

- 3 missing Customer_ID records.
- 1 negative Quantity.
- 1 negative Unit_Price.
- 1 invalid Order_Date (`not available`).
- 53 negative Discount records.

The objective was to clean clearly invalid source values without inventing unsupported replacements.

---

## 🧮 11. Net Sales Calculation

The Net_Sales calculation was recalculated to validate the transactional values.

Formula:

`=F2*G2-H2`

Meaning:

**Quantity × Unit Price − Discount**

The formula was filled down using:

**Ctrl + D**

After recalculation, two negative Net_Sales values remained.

Instead of manually changing these values, the underlying records were investigated.

The two records were caused by missing input values:

1. One record had missing Quantity.
2. One record had missing Unit_Price.

Therefore, these records were retained rather than artificially changing the calculated result.

### Learning

When a calculated value looks incorrect, trace the result back to its source inputs before modifying it.

---

## 📅 12. Order Month Transformation

An `Order_Month` column was added to support monthly revenue analysis.

The final formula was:

`=IF([@[Order_Date]]="","",EOMONTH([@[Order_Date]],0))`

The initial formula was:

`=EOMONTH([@[Order_Date]],0)`

However, blank Order_Date values resulted in an unexpected:

**Jan-1900**

This was corrected using the IF condition.

The final Order_Month column was formatted as:

`mmm-yy`

### Learning

Excel date functions can behave unexpectedly with blank values, so missing dates should be handled explicitly.

---

## 🔎 13. Lookup Transformations

Lookup functions were used to enrich the Orders table with information from other datasets.

This simulated a common real-world Data Analyst requirement:

> Transaction data often needs to be enriched using master or reference data.

### 🏷️ Product Category Lookup

Product Category was added to Orders using:

`=XLOOKUP(D2,products_table[Product_ID],products_table[Category],"")`

This supported:

- Product category revenue analysis.
- PivotTables.
- PivotCharts.
- Dashboard filtering.

### 👥 Customer Segment Lookup

Customer Segment was added using:

`=XLOOKUP(C2,customer_table[Customer_ID],customer_table[Customer_Segment],"Unknown")`

The `"Unknown"` result was intentionally used for missing Customer_ID relationships.

This prevented blank lookup results from creating an unnecessary blank item in the dashboard slicer.

Resulting values included:

- New
- Premium
- Regular
- Unknown

### 🚚 Delivery Status Lookup

Delivery Status was added to Orders using:

`=TRIM(XLOOKUP(A2,delivery_table[Order_ID],delivery_table[Delivery_Status],""))`

The `TRIM()` function was important because the raw Delivery dataset contained a trailing space in the `Delayed ` value.

Without cleaning the text, Excel could treat:

`Delayed`

and

`Delayed `

as different categories.

---

## 🚚 14. Delivery Dataset

The Delivery dataset contained operational delivery information.

### Columns

- Order_ID
- Store_ID
- Delivery_Partner
- Promised_Minutes
- Actual_Minutes
- Distance_KM
- Delivery_Status

### Dataset Size

**50,003 delivery records**

### Validation Checks

The following checks were performed:

- Order_ID blanks.
- Duplicate Order_ID.
- Missing Actual_Minutes.
- Delivery_Status blanks.
- Distance_KM <= 0.
- Promised_Minutes <= 0.
- Actual_Minutes <= 0.
- Delivery_Partner blanks.
- Store_ID blanks.
- Distance_KM blanks.

### Findings

- 2 missing Actual_Minutes records.
- No blank Delivery_Status.
- No invalid Distance_KM values.
- No invalid Promised_Minutes values.
- No invalid Actual_Minutes values.
- No blank Delivery_Partner values.
- No blank Store_ID values.
- No blank Distance_KM values.

The missing Actual_Minutes values were retained because there was no reliable information available to replace them.

---

## 📦 15. Inventory Dataset

The Inventory dataset represented stock movement across products and stores.

### Columns

- Stock_Date
- Store_ID
- Product_ID
- Opening_Stock
- Received_Stock
- Sold_Units
- Reorder_Level
- Closing_Stock

### Dataset Size

**30,002 inventory records**

### Validation Performed

The following fields were checked:

- Stock_Date
- Store_ID
- Product_ID
- Opening_Stock
- Received_Stock
- Sold_Units
- Closing_Stock

No negative values were observed in:

- Opening_Stock
- Received_Stock
- Sold_Units

---

## 🧮 16. Closing Stock Calculation

Closing Stock was recalculated using:

`=Opening_Stock+Received_Stock-Sold_Units`

This was done to validate whether the Closing_Stock values were mathematically consistent.

After recalculation, negative Closing_Stock values were identified.

---

## ⚠️ 17. Inventory Exceptions

The project identified:

**3,458 negative Closing_Stock records**

The inventory exception rate was calculated as:

`=COUNTIF(inventory_table[Closing_Stock],"<0")/COUNTA(inventory_table[Product_ID])`

Result:

**11.53%**

Negative inventory values were not automatically deleted or converted to zero.

They were treated as **business exceptions** that may require operational investigation.

The important analytical distinction was:

**Data-quality error vs Business exception**

A negative inventory balance may indicate operational situations such as stock-outs, inventory timing differences or stock reconciliation issues.

### Learning

An analyst should understand the business meaning of an unusual value before deciding that it is incorrect.

---

## 🔄 18. Returns Dataset

The Returns dataset contained return transactions.

### Columns

- Return_ID
- Order_ID
- Product_ID
- Return_Date
- Return_Quantity
- Return_Reason

### Dataset Size

**3,617 return records**

### Return Reasons

The dataset contained:

- Customer Changed Mind
- Damaged
- Quality Issue
- Wrong Item

### Issue Identified

One negative Return_Quantity value was identified.

The negative quantity was cleared while retaining the return transaction itself.

The return record was therefore preserved rather than deleting the entire transaction.

---

## 🔍 19. Data Profiling Approach

Before creating the dashboard, each dataset was profiled individually.

### 📊 Structural Checks

- Row count.
- Column count.
- Last used cell.
- Data range.

### 🔍 Data Completeness

- Blank values.
- Missing IDs.
- Missing dates.
- Missing numeric values.

### 🔁 Duplicate Checks

- Duplicate Customer_ID.
- Duplicate Product_ID.
- Duplicate Order_ID.
- Duplicate inventory records.

### 🔢 Numeric Validation

- Negative quantities.
- Negative prices.
- Negative discounts.
- Negative stock.

### 📅 Date Validation

- Invalid dates.
- Blank dates.
- Monthly grouping.

### 📝 Text Validation

- City inconsistencies.
- Trailing spaces.
- Category values.
- Status values.

### 🧮 Calculation Validation

- Net Sales.
- Closing Stock.
- Revenue totals.
- KPI reconciliation.

---

## 🧹 20. Data Cleaning Philosophy

The cleaning process followed this principle:

> **Do not change data simply because it looks unusual. Investigate first.**

### Clearly Invalid Values

Examples:

- Negative Quantity.
- Negative Unit Price.
- Negative Discount.
- Invalid Order Date.
- Negative Selling Price.
- Negative Return Quantity.

These were cleared where appropriate.

### Missing Information

Examples:

- Missing Customer Age.
- Missing Actual Delivery Minutes.
- Missing Order Date.

These were not artificially filled because the correct values were unknown.

### Business Exceptions

Example:

- Negative Closing Stock.

These were retained for analysis.

This approach prevented the cleaning process from introducing unsupported assumptions.

---

## 📊 21. Analysis Sheet

A dedicated **Analysis** worksheet was created.

The Analysis sheet contained business calculations for:

- Sales Category revenue.
- Total Revenue.
- Total Orders.
- Units Sold.
- Average Order Value.
- Sales Category order count.
- Product Category revenue.
- Monthly revenue.
- Order Channel revenue.
- Delivery performance.
- Return Rate.
- Inventory exception count.
- Inventory exception rate.

The Analysis sheet acted as a validation layer before the dashboard.

---

## 💰 22. Sales Category Revenue Analysis

Sales Category revenue was calculated using `SUMIFS`.

The categories were:

- Very High
- High
- Medium
- Low

### Results

| Sales Category | Total Revenue |
|---|---:|
| Very High | ₹267,999,181.70 |
| High | ₹89,986,066.45 |
| Medium | ₹43,780,389.70 |
| Low | ₹8,827,685.41 |
| **Total** | **₹410,593,323.20** |

The category revenue total was reconciled against Total Revenue.

---

## 🛒 23. Sales Category Order Count

Order volume by Sales Category was calculated using `COUNTIFS`.

### Results

| Sales Category | Orders |
|---|---:|
| Very High | 16,381 |
| High | 12,282 |
| Medium | 12,597 |
| Low | 8,743 |
| **Total** | **50,003** |

This provided a comparison between revenue contribution and order volume.

---

## 🛍️ 24. Product Category Revenue Analysis

Revenue was calculated for all six product categories.

| Product Category | Total Revenue |
|---|---:|
| Electronics | ₹72,934,904.36 |
| Beauty | ₹62,941,158.12 |
| Beverages | ₹70,691,797.38 |
| Grocery | ₹53,964,258.77 |
| Fashion | ₹71,699,867.68 |
| Home | ₹78,361,336.90 |
| **Total** | **₹410,593,323.20** |

The category totals matched the overall Total Revenue.

This reconciliation helped validate the product category analysis.

---

## 📅 25. Monthly Revenue Analysis

Monthly revenue was calculated using the derived `Order_Month` column.

### Results

| Month | Total Revenue |
|---|---:|
| Aug-2026 | ₹230,781,417.60 |
| Sep-2026 | ₹179,809,771.00 |

One order had a blank Order_Date:

- Order ID: `O0000401`
- Customer ID: `C00582`
- Product ID: `P0273`
- Store ID: `S019`
- Quantity: `1`
- Unit Price: `2246.91`
- Discount: `112.35`
- Payment Method: `UPI`
- Order Channel: `Online`
- Net Sales: `₹2,134.56`

Instead of assigning a fake date, the order was retained as an undated exception.

This explained the small difference between monthly revenue totals and the overall revenue total.

---

## 🌐 26. Order Channel Analysis

Revenue was analyzed across three order channels:

- App
- Online
- Web

### Revenue Results

| Order Channel | Total Revenue |
|---|---:|
| App | ₹62,096,041.99 |
| Online | ₹307,660,608.80 |
| Web | ₹40,836,672.38 |

The channel revenue totals were reconciled against overall revenue.

---

## 📌 27. KPI Calculations

The main project KPIs were:

### 💰 Total Revenue

`=SUM(orders_table[Net_Sales])`

Result:

**₹410,593,323.20**

Displayed on dashboard as:

**₹410.59M**

### 🛒 Total Orders

`=COUNTA(orders_table[Order_ID])`

Result:

**50,003**

### 📦 Units Sold

`=SUM(orders_table[Quantity])`

Result:

**149,695**

### 💵 Average Order Value

`=Total Revenue / Total Orders`

Result:

**₹8,211.37**

### 🚚 On-Time Delivery %

`=COUNTIFS(delivery_table[Delivery_Status],"On time")/COUNTA(delivery_table[Order_ID])`

Result:

**21.60%**

### 🔄 Return Rate

`=SUM(returns_table[Return_Quantity])/SUM(orders_table[Quantity])`

Result:

**3.52%**

### 📦 Inventory Exception Rate

`=COUNTIF(inventory_table[Closing_Stock],"<0")/COUNTA(inventory_table[Product_ID])`

Result:

**11.53%**

---

## 🚚 28. Delivery Performance Analysis

Delivery performance was analyzed using Delivery Status.

The final categories were:

- Delayed
- On Time

### Delivery Performance

| Delivery Status | Percentage |
|---|---:|
| Delayed | 78.40% |
| On Time | 21.60% |
| **Total** | **100.00%** |

The dashboard displayed:

**21.60% On-Time Delivery**

This was calculated using the total number of delivery records.

---

## 🔄 29. Return Rate Analysis

Return Rate was calculated using returned units compared with total sold units.

Formula:

`=SUM(returns_table[Return_Quantity])/SUM(orders_table[Quantity])`

Result:

**3.52%**

This metric was used as an operational KPI.

---

## 📦 30. Inventory Exception Analysis

The inventory analysis identified:

**3,458 negative Closing_Stock records**

The exception rate was:

**11.53%**

The metric was presented as an operational exception indicator rather than automatically labeling all negative stock values as data errors.

---

## 📊 31. PivotTable Analysis

PivotTables were used as the analytical layer supporting the dashboard.

The main PivotTables covered:

1. Revenue by Product Category.
2. Revenue by Sales Category.
3. Revenue by Order Channel.
4. Delivery Performance.
5. Daily Revenue Trend.

PivotTables were configured using:

- Rows.
- Values.
- Sum.
- Count.
- % of Grand Total.

The PivotTables were also validated against independent Analysis calculations.

---

## 📊 32. Revenue by Product Category PivotTable

The Product Category PivotTable used:

### Rows

`Product_Category`

### Values

`Sum of Net_Sales`

The resulting Grand Total was:

**₹410,593,323.20**

This matched the Analysis sheet's Total Revenue.

---

## 📊 33. Revenue by Sales Category PivotTable

The Sales Category PivotTable used:

### Rows

`Sales_Category`

### Values

`Sum of Net_Sales`

The Grand Total was:

**₹410,593,323.20**

This provided another validation point for the revenue analysis.

---

## 🌐 34. Revenue by Order Channel PivotTable

The Order Channel PivotTable contained:

### Rows

- App
- Online
- Web

### Values

`Sum of Net_Sales`

This PivotTable was used as the supporting data source for the **Revenue by Order Channel** chart.

---

## 🚚 35. Delivery Performance PivotTable

The Delivery Performance PivotTable used:

### Rows

`Delivery_Status`

### Values

`Count of Order_ID`

The Value Field Settings were changed to:

**Show Values As → % of Grand Total**

Final results:

- Delayed → **78.40%**
- On Time → **21.60%**
- Grand Total → **100.00%**

This PivotTable directly supported the Delivery Performance chart.

---

## 📅 36. Daily Revenue Trend PivotTable

A Daily Revenue Trend PivotTable was created to analyze revenue by date.

Initially, Excel automatically grouped the dates.

The dates were then manually **ungrouped** so individual daily values could be analyzed.

The PivotTable included daily dates across the available period.

The blank date was retained separately because one order did not contain an Order_Date.

The supporting chart was configured using the daily data while excluding the blank and Grand Total rows.

The chart's date-axis label interval was changed to:

**Specify interval unit = 5**

This reduced label overcrowding while keeping the underlying daily data.

---

## 📈 37. PivotCharts & Dashboard Visuals

Five main dashboard visuals were created.

### 1️⃣ Revenue by Product Category

Shows revenue generated by each product category.

### 2️⃣ Revenue by Sales Category

Shows revenue distribution across Sales Categories.

### 3️⃣ Revenue by Order Channel

Shows revenue generated through:

- App
- Online
- Web

### 4️⃣ Delivery Performance

Shows:

- Delayed %
- On-Time %

### 5️⃣ Daily Revenue Trend

Shows daily revenue movement across the available period.

Data labels across the charts were formatted into a compact currency style:

`₹0.0,,"M"`

Example:

`₹70.7M`

Chart titles were also reviewed for clarity.

For example:

**Revenue by Order Channel**

was used instead of a generic title such as:

**Total**

---

## 🎛️ 38. Interactive Slicers

Exactly four slicers were created.

### 1️⃣ Order Channel

Filters the dashboard by:

- App
- Online
- Web

### 2️⃣ Product Category

Filters the dashboard by product category.

### 3️⃣ Customer Segment

Filters by:

- New
- Premium
- Regular
- Unknown

### 4️⃣ Payment Method

Filters by payment method.

All four slicers were connected to the relevant PivotTables.

The four-slicer setup was intentionally kept limited to avoid unnecessary dashboard clutter.

---

## 🎨 39. Dashboard Design Principles

The dashboard followed ten locked design principles.

### 1. 🎯 Business Purpose

Every visual should answer a business question.

### 2. 📊 Correct Visual Choice

The visual type should match the question being answered.

### 3. 🚫 No Duplication

Avoid repeating the same information in multiple visuals.

### 4. 👨‍💼 Senior-Level Credibility

The dashboard should demonstrate analytical thinking.

### 5. 👨‍🎓 Fresher Readability

The dashboard should remain understandable to entry-level analysts and viewers.

### 6. 👁️ Visual Hierarchy

Important KPIs should be easy to identify.

### 7. 🧹 Clean Presentation

Avoid unnecessary clutter.

### 8. 💡 Actionable Insight

The analysis should help identify areas requiring attention.

### 9. 🔐 Data Integrity

Dashboard results should be based on validated calculations.

### 10. 💼 LinkedIn Showcase Quality

The dashboard should be suitable for professional portfolio presentation.

---

## 📌 40. Final Dashboard KPIs

The final dashboard displayed five primary KPI cards.

### 💰 Total Revenue

**₹410.59M**

### 🛒 Total Orders

**50,003**

### 📦 Units Sold

**149,695**

### 💵 Average Order Value

**₹8,211.37**

### 🚚 Delivery On-Time %

**21.60%**

These KPIs were placed at the top of the dashboard to provide a quick management-level overview.

---

## 🧩 41. Major Challenges & How We Solved Them

The project involved several practical challenges.

### 🔥 Challenge 1 – Find & Replace Mistake

While standardizing:

`Hyd → Hyderabad`

an initial Find & Replace operation unintentionally changed:

`Hyderabad → Hyderabaderabad`

#### Solution

The mistake was reversed using:

**Ctrl + Z**

The correct replacement was then performed using:

**Match entire cell contents**

#### Learning

Always verify the replacement scope before modifying business data.

---

### 🔥 Challenge 2 – Blank Dates Becoming January 1900

The initial Order_Month formula caused blank Order_Date values to appear as January 1900.

#### Solution

The formula was changed to:

`=IF([@[Order_Date]]="","",EOMONTH([@[Order_Date]],0))`

#### Learning

Missing dates must be explicitly handled when using Excel date functions.

---

### 🔥 Challenge 3 – Understanding Negative Values

Not every negative number is automatically a data error.

#### Invalid examples

- Negative Quantity.
- Negative Unit Price.
- Negative Discount.
- Negative Selling Price.
- Negative Return Quantity.

#### Business exception example

- Negative Closing Stock.

#### Learning

The analyst must understand the business meaning of a value before deciding whether to remove or modify it.

---

### 🔥 Challenge 4 – Net Sales Validation

Two negative Net_Sales values remained after recalculation.

#### Solution

The underlying records were investigated.

The issue was caused by missing Quantity / Unit_Price inputs.

The records were retained.

#### Learning

Trace unexpected calculated results back to their source inputs.

---

### 🔥 Challenge 5 – Revenue Reconciliation

Monthly revenue did not immediately match total revenue.

#### Investigation

One order had:

- Order ID: `O0000401`
- Blank Order Date
- Net Sales: `₹2,134.56`

#### Solution

The order was retained as an undated exception rather than assigning a fake date.

#### Learning

Reconciliation is essential when validating analytical results.

---

### 🔥 Challenge 6 – Trailing Space in Delivery Status

The source contained:

`Delayed `

with a trailing space.

#### Solution

The lookup used:

`=TRIM(XLOOKUP(A2,delivery_table[Order_ID],delivery_table[Delivery_Status],""))`

#### Learning

Invisible text characters can affect filtering, grouping and PivotTables.

---

### 🔥 Challenge 7 – Missing Lookup Results

Some Orders had missing Customer_ID values.

#### Solution

The Customer Segment lookup used:

`=XLOOKUP(C2,customer_table[Customer_ID],customer_table[Customer_Segment],"Unknown")`

#### Learning

Missing lookup results should be handled deliberately instead of allowing unexplained blank categories.

---

### 🔥 Challenge 8 – PivotTable Configuration

Understanding how to configure:

- Rows.
- Values.
- Value Field Settings.
- % of Grand Total.
- PivotChart source ranges.

required practical experimentation.

#### Learning

PivotTables are an analytical tool, not simply a chart-generation feature.

---

### 🔥 Challenge 9 – Delivery Percentage

Delivery status initially appeared as counts.

#### Solution

The PivotTable Value Field was changed to:

**Show Values As → % of Grand Total**

Result:

- Delayed → 78.40%
- On Time → 21.60%

#### Learning

PivotTables can transform the same underlying data into different business metrics.

---

### 🔥 Challenge 10 – Daily Revenue Chart

The daily revenue chart initially contained crowded date labels.

#### Solution

The date axis was configured with:

**Specify interval unit = 5**

#### Learning

Good visualization design can improve readability without removing analytical data.

---

### 🔥 Challenge 11 – Power Pivot Availability

Power Pivot / Data Model was explored during the project.

The required feature was not readily available in the Excel environment.

#### Solution

The project continued using:

- Excel Tables.
- XLOOKUP.
- SUMIFS.
- COUNTIFS.
- PivotTables.
- PivotCharts.
- Slicers.

#### Learning

An analyst should be able to use alternative approaches when a particular Excel feature is unavailable.

---

### 🔥 Challenge 12 – Dashboard Design

One of the biggest challenges was deciding what **not** to include.

The goal was not to fill the dashboard with unnecessary charts.

The dashboard was therefore designed around purposeful business questions.

#### Learning

A strong dashboard is not defined by the number of visuals. It is defined by how clearly it communicates useful business information.

---

## 🛠️ 42. Excel Skills Demonstrated

The QuickCart project demonstrated practical Excel skills across multiple areas.

### 📌 Excel Fundamentals

- Workbook management.
- Worksheet management.
- Excel Tables.
- Cell references.
- Formatting.
- Sorting.
- Filtering.
- Freeze Panes.
- Find & Replace.
- Navigation.

### 🧹 Data Cleaning

- Remove Duplicates.
- Conditional Formatting.
- Blank-value identification.
- Missing-value identification.
- Invalid-value identification.
- Text standardization.
- Data validation.

### 🧮 Excel Formulas

- IF
- SUM
- SUMIFS
- COUNTIF
- COUNTIFS
- COUNTA
- EOMONTH
- UNIQUE
- FILTER
- SUMPRODUCT

### 🔎 Lookup Functions

- XLOOKUP.
- Structured references.
- Missing lookup handling.
- Lookup enrichment.
- TRIM + XLOOKUP.

### 📅 Date Analysis

- EOMONTH.
- Monthly grouping.
- Daily analysis.
- Blank-date handling.

### 📊 PivotTables

- Rows.
- Values.
- Sum.
- Count.
- % of Grand Total.
- PivotTable refresh.
- Supporting PivotTables.

### 📈 PivotCharts

- Product category revenue.
- Sales category revenue.
- Channel revenue.
- Delivery performance.
- Daily revenue trend.

### 🎛️ Slicers

- Order Channel.
- Product Category.
- Customer Segment.
- Payment Method.

### ⌨️ Shortcuts Practiced

| Shortcut | Purpose |
|---|---|
| Ctrl + T | Create Excel Table |
| Ctrl + F | Find |
| Ctrl + H | Find & Replace |
| Ctrl + Z | Undo |
| Ctrl + S | Save |
| Ctrl + End | Go to last used cell |
| Ctrl + Down | Move to last data cell |
| Ctrl + D | Fill Down |
| Ctrl + Shift + L | Toggle Filter |
| Ctrl + 1 | Format Cells |
| F2 | Edit Cell |
| F4 | Repeat / control references |
| Ctrl + A | Select data |
| Ctrl + Home | Go to beginning |
| Ctrl + G | Go To |
| Alt + = | AutoSum |

---

## 🔄 43. Complete End-to-End Project Workflow

The complete QuickCart project workflow was:

**🏢 Business Request**

↓

**📂 Receive Raw Excel Files**

↓

**🔍 Inspect Raw Data**

↓

**📊 Profile Each Dataset**

↓

**⚠️ Identify Data-Quality Issues**

↓

**🧹 Clean Invalid Data**

↓

**🔐 Preserve Raw Data**

↓

**✅ Validate Cleaned Data**

↓

**🧮 Create Calculated Fields**

↓

**🔎 Apply Lookup Functions**

↓

**📊 Perform Business Analysis**

↓

**📌 Create Analysis Sheet**

↓

**📊 Build PivotTables**

↓

**📈 Create PivotCharts**

↓

**🎛️ Add Slicers**

↓

**🎨 Design Dashboard**

↓

**💡 Generate Business Insights**

↓

**📋 Document Project**

↓

**🐙 Prepare Project for GitHub**

### 📊 Final Project Summary

| Metric | Result |
|---|---:|
| 👥 Customer Records | 5,002 |
| 🛍️ Products | 500 |
| 🏪 Stores | 40 |
| 🛒 Orders | 50,003 |
| 🚚 Delivery Records | 50,003 |
| 📦 Inventory Records | 30,002 |
| 🔄 Return Records | 3,617 |
| 💰 Total Revenue | ₹410.59M |
| 🛒 Total Orders | 50,003 |
| 📦 Units Sold | 149,695 |
| 💵 Average Order Value | ₹8,211.37 |
| 🚚 On-Time Delivery | 21.60% |
| 🔄 Return Rate | 3.52% |
| 📦 Negative Inventory Exceptions | 3,458 |
| ⚠️ Inventory Exception Rate | 11.53% |
| 📊 Product Categories | 6 |
| 📈 Dashboard Visuals | 5 |
| 🎛️ Dashboard Slicers | 4 |
| 📌 Dashboard KPIs | 5 |

### 💡 Final Project Learning

The QuickCart project demonstrates that Data Analysis is more than creating charts.

The complete process involved:

**Understanding the business requirement → Understanding the data → Finding data-quality issues → Cleaning carefully → Validating calculations → Transforming data → Performing analysis → Building PivotTables → Creating visualizations → Building an interactive dashboard → Communicating business insights.**

The most important learning from the project was:

> **A good Data Analyst does not immediately change unexpected data. They investigate it first, understand the business context, validate the result, and then decide what action is appropriate.**

### ⚠️ Disclaimer

QuickCart is a **fictional company created for educational and portfolio purposes**.

All datasets used in this project are **synthetic data created for learning and demonstration purposes**.

This project does not contain or represent confidential, proprietary or internal data from Amazon, Flipkart, Zepto or any other real organization.

The business scenario is inspired by common e-commerce / quick-commerce analytical workflows but does not represent the internal systems, operations, customers or financial data of any specific company.

### 👨‍💻 Author

**Pavan**

📊 Aspiring Data Analyst  
🧮 Excel | SQL | Power BI | Python  
📈 Interested in Data Analytics, Business Intelligence & Operations Analytics

### ⭐ Project Focus

**Excel Data Analytics | Sales Analytics | Operations Analytics | Data Cleaning | Data Validation | Business Analysis | PivotTables | PivotCharts | Dashboard Development**