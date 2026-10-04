# Case-Study-Project-Documentation
# Brazilian E-Commerce Analytics (Olist) - SWYNEX Technologies

## Project Overview
This project presents an end-to-end data analytics case study on the Brazilian E-Commerce public dataset by Olist. The analysis focuses on understanding customer purchasing patterns, payment methods, delivery status, and product category performance to derive actionable business insights.

---

## Problem Statement
The primary objectives of this analysis are:
- Analyze order fulfillment and delivery trends across Brazilian states and cities.
- Identify the most revenue-generating product categories.
- Examine customer payment preferences (credit card, boleto, voucher, etc.) and installment behavior.
- Provide business recommendations to optimize logistics and enhance customer retention.

---

## Dataset Architecture & Data Model
The project utilizes a relational schema containing 5 primary tables:
- **`olist_orders_dataset`**: Order lifecycle timestamps (`order_purchase_timestamp`, `order_delivered_customer_date`), status, and customer identifiers.
- **`olist_order_items_dataset`**: Line-item details (`price`, `freight_value`, `product_id`, `seller_id`).
- **`olist_order_payments_dataset`**: Payment transactions (`payment_type`, `payment_installments`, `payment_value`).
- **`olist_customers_dataset`**: Geographic and demographic attributes (`customer_city`, `customer_state`, `customer_unique_id`).
- **`olist_products_dataset`**: Product catalog details (`product_category_name`, dimensions, weight).

### Relationships:
- `olist_orders_dataset` (1) ⟷ (*) `olist_order_items_dataset` via `order_id`
- `olist_orders_dataset` (1) ⟷ (*) `olist_order_payments_dataset` via `order_id`
- `olist_customers_dataset` (1) ⟷ (*) `olist_orders_dataset` via `customer_id`
- `olist_products_dataset` (1) ⟷ (*) `olist_order_items_dataset` via `product_id`

---

## Data Cleaning & Transformation
- **Null Value & Consistency Audits:** Validated order delivery dates and handling missing delivery timestamps for canceled/in-transit orders.
- **Data Types Configuration:** Configured date-time formats for timestamps and numerical formatting for financial fields (`price`, `payment_value`, `freight_value`).
- **Model Integrity:** Relied on established relational star-snowflake schema without redundant custom columns, utilizing native DAX aggregations for dashboard efficiency.

---

## Dashboard Visualizations
*(Add screenshot of your Power BI dashboard report page here)*

Key dashboard components:
1. **Executive KPI Cards:** Total Orders, Total Sales Volume, Average Order Value (AOV), and Freight Share.
2. **Category Performance:** Top product categories by revenue and item volume.
3. **Payment Method Breakdown:** Distribution of payment types (Credit Card dominance vs. Boleto).
4. **Geographic Distribution:** Order volume across states (`customer_state`) and major metropolitan cities.

---

## Key Business Insights
1. **Regional Concentration:** High volume of orders originates from core metropolitan areas like São Paulo (SP) and Rio de Janeiro (RJ), indicating logistical density benefits in southeast regions.
2. **Payment Dynamics:** Credit cards account for the largest share of transactions, with installment options heavily utilized for higher-ticket orders.
3. **Category Contributions:** Electronics, home goods, and health & beauty drive the majority of top-line revenue.
4. **Logistics Optimization:** Freight value heavily impacts conversion and delivery times in peripheral regions, suggesting a need for regional distribution hubs.

---

## Repository Structure# Brazilian E-Commerce Analytics (Olist) - SWYNEX Technologies

## Project Overview
This project presents an end-to-end data analytics case study on the Brazilian E-Commerce public dataset by Olist. The analysis focuses on understanding customer purchasing patterns, payment methods, delivery status, and product category performance to derive actionable business insights.

---

## Problem Statement
The primary objectives of this analysis are:
- Analyze order fulfillment and delivery trends across Brazilian states and cities.
- Identify the most revenue-generating product categories.
- Examine customer payment preferences (credit card, boleto, voucher, etc.) and installment behavior.
- Provide business recommendations to optimize logistics and enhance customer retention.

---

## Dataset Architecture & Data Model
The project utilizes a relational schema containing 5 primary tables:
- **`olist_orders_dataset`**: Order lifecycle timestamps (`order_purchase_timestamp`, `order_delivered_customer_date`), status, and customer identifiers.
- **`olist_order_items_dataset`**: Line-item details (`price`, `freight_value`, `product_id`, `seller_id`).
- **`olist_order_payments_dataset`**: Payment transactions (`payment_type`, `payment_installments`, `payment_value`).
- **`olist_customers_dataset`**: Geographic and demographic attributes (`customer_city`, `customer_state`, `customer_unique_id`).
- **`olist_products_dataset`**: Product catalog details (`product_category_name`, dimensions, weight).

### Relationships:
- `olist_orders_dataset` (1) ⟷ (*) `olist_order_items_dataset` via `order_id`
- `olist_orders_dataset` (1) ⟷ (*) `olist_order_payments_dataset` via `order_id`
- `olist_customers_dataset` (1) ⟷ (*) `olist_orders_dataset` via `customer_id`
- `olist_products_dataset` (1) ⟷ (*) `olist_order_items_dataset` via `product_id`

---

## Data Cleaning & Transformation
- **Null Value & Consistency Audits:** Validated order delivery dates and handling missing delivery timestamps for canceled/in-transit orders.
- **Data Types Configuration:** Configured date-time formats for timestamps and numerical formatting for financial fields (`price`, `payment_value`, `freight_value`).
- **Model Integrity:** Relied on established relational star-snowflake schema without redundant custom columns, utilizing native DAX aggregations for dashboard efficiency.

---

## Dashboard Visualizations
*(Add screenshot of your Power BI dashboard report page here)*

Key dashboard components:
1. **Executive KPI Cards:** Total Orders, Total Sales Volume, Average Order Value (AOV), and Freight Share.
2. **Category Performance:** Top product categories by revenue and item volume.
3. **Payment Method Breakdown:** Distribution of payment types (Credit Card dominance vs. Boleto).
4. **Geographic Distribution:** Order volume across states (`customer_state`) and major metropolitan cities.

---

## Key Business Insights
1. **Regional Concentration:** High volume of orders originates from core metropolitan areas like São Paulo (SP) and Rio de Janeiro (RJ), indicating logistical density benefits in southeast regions.
2. **Payment Dynamics:** Credit cards account for the largest share of transactions, with installment options heavily utilized for higher-ticket orders.
3. **Category Contributions:** Electronics, home goods, and health & beauty drive the majority of top-line revenue.
4. **Logistics Optimization:** Freight value heavily impacts conversion and delivery times in peripheral regions, suggesting a need for regional distribution hubs.

---

## Repository Structure
