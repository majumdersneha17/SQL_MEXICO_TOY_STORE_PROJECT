# SQL_MEXICO_TOY_STORE_PROJECT

This project involves the analysis of sales, profit, and inventory data for a fictitious toy store chain in Mexico. The objective is to optimize business decisions by analyzing key metrics such as revenue, profit margin, stock levels, and sales trends.

## Project Overview:
The toy store chain has over 800,000 transactions recorded from January 1st, 2017 to September 30th, 2018. The database consists of four key tables:
- **Products**: Product details, including price and cost.
- **Stores**: Information on store locations and identifiers.
- **Sales**: Transactional data with product sales per store.
- **Inventory**: Stock data for each product at each store.

## Data Model

The project utilizes four key tables to store and manage toy store data:

### 1. **Products Table**
- **Purpose**: Contains product details like `Product_ID`, `Product_Name`, `Product_Price`, and `Product_Cost`.
- **Relationships**: Linked to **Sales** (via `Product_ID`) and **Inventory** (via `Product_ID`).

### 2. **Stores Table**
- **Purpose**: Stores details about each store such as `Store_ID`, `Store_Name`, and `Store_Location`.
- **Relationships**: Linked to **Sales** and **Inventory** via `Store_ID`.

### 3. **Inventory Table**
- **Purpose**: Tracks stock levels (`Stock_On_Hand`) of each product per store.
- **Relationships**: Linked to **Stores** and **Products** via `Store_ID` and `Product_ID`.

### 4. **Sales Table**
- **Purpose**: Records sales transactions, including `Sale_ID`, `Selling_Date`, `Store_ID`, `Product_ID`, and `Units`.
- **Relationships**: Linked to **Stores** and **Products** via `Store_ID` and `Product_ID`.

### Relationships Overview:
- **Products** ↔ **Sales** ↔ **Stores**
- **Products** ↔ **Inventory** ↔ **Stores**

This model supports the analysis of sales, inventory, and profit data across various stores, products, and categories.


## Key Features:
- **Revenue, Profit & Cost Calculation**: Calculated total revenue, profit, and cost of goods sold (COGS) using SQL aggregation functions.
- **Profit Margin Analysis**: Analyzed profit margin by product category and store, identifying high-margin products and categories.
- **Sales Trends**: Visualized monthly sales trends, identifying growth periods and volatile months.
- **Top & Bottom Products**: Ranked products by sales and profit, identifying the most and least profitable items.
- **Inventory Optimization**: Assessed inventory stock levels, highlighting low stock and overstocked products.
- **Store & Location Analysis**: Evaluated performance across stores and cities, identifying the best-performing locations.
- **Restocking Alerts**: Generated restocking alerts for products based on sales velocity and current stock levels.

## SQL Functions & Techniques Used:
- **Aggregation**: `SUM()`, `ROUND()`, `COUNT()`, `AVG()`, `GROUP BY` for summarizing sales and inventory data.
- **Joins**: `INNER JOIN` to combine data from multiple tables (e.g., sales with products, inventory with products).
- **Window Functions**: `ROW_NUMBER()` and `LAG()` for ranking and calculating percentage changes over time.
- **Date Formatting & Calculation**: Used `STR_TO_DATE()` to convert string dates and calculate sales trends by month.
- **Data Transformation**: Applied `UPDATE`, `REPLACE()`, and `CONCAT()` for data cleaning and transformation.
- **Subqueries**: Used for filtering and ranking products, stores, and categories based on performance metrics.

## Key Insights:
- **Revenue**: The toy store generated over $14M in revenue and $4M in profit.
- **Top Products**: Lego Bricks, Action Figures, and Colorbuds were top sellers, contributing significantly to both sales and profit.
- **Store Performance**: Downtown stores generate the highest profit, but airport stores showed high revenue potential, suggesting an area for further business expansion.
- **Inventory Management**: Some products (e.g., Uno Cards, Play Foam) showed low sales and high inventory, indicating potential for inventory reduction. 

## Recommendations

### 1. **Inventory Optimization**
   - **Action Figure** and **Lego Bricks** have high sales potential but are frequently out of stock. Ensure these products are restocked more frequently to avoid revenue loss.
   - Review and clear **low-performing products** like **Uno Cards** and **Play Foam** that generate minimal sales and contribute significantly to tied-up inventory.

### 2. **Sales Analysis**
   - **Toys** and **Art & Crafts** categories contribute more than 50% of total revenue. Focus on enhancing stock and promotional strategies for these categories.
   - Focus on **high-profit categories** like **Electronics** and **Games** for targeted marketing and promotion to increase overall profitability.

### 3. **Store Performance**
   - **Downtown stores** are the highest revenue generators, but the **Airport stores** are performing well too, making them ideal candidates for potential expansion.
   - Monitor sales patterns closely for **seasonal changes** (e.g., holiday seasons like Christmas) to optimize inventory and sales strategies.

### 4. **Profit Margin Focus**
   - Focus on **high-margin products** to maximize profitability, especially in categories like **Electronics** and **Games**, where profit margins are significantly higher.

### 5. **Restocking and Demand Forecasting**
   - Identify top-selling products and ensure they are restocked **within 10-15 days** to meet rising demand, especially in the lead-up to **holiday seasons**.
   - Conduct **demand forecasting** to predict the right stock levels for key products, preventing both stockouts and overstock situations.

### 6. **Location-Based Strategy**
   - **Store locations** with high sales volume should receive targeted marketing and stock replenishment strategies.
   - Conduct further studies on **airport stores** to explore their expansion potential and optimize their inventory and sales.

These recommendations aim to improve **inventory management**, **sales forecasting**, and **profitability**, optimizing the store chain's overall performance.
