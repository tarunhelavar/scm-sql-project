# 🚚 Supply Chain Management – SQL Project

This project contains SQL queries developed to analyze and optimize supply chain operations. It was created during my internship at **AI Variant** as part of the **Business Analyst Certification Program by ExcelR Edtech, Bangalore**.

## 🧠 Project Objective
The goal was to use data analytics to uncover operational inefficiencies, track inventory and order performance, and support data-driven decision-making in supply chain management.

## 🗂 Key Functional Areas Covered
- 📦 **Inventory Management:** Identify fast-moving and slow-moving items, stock-outs, and reorder levels.
- 🛒 **Order Performance:** Analyze order volume, fulfillment rates, and cycle times.
- 🚚 **Logistics Efficiency:** Calculate delivery time averages and delays across regions.
- 📍 **Supplier Metrics:** Measure supplier reliability, delivery frequency, and fulfillment rates.
- 📈 **Revenue Trends:** Identify high-revenue products and regions using aggregated order data.

## 🔧 Tools & Technologies Used
- **SQL** (PostgreSQL / MySQL syntax)
- **Excel** (for source data and prototyping)
- **Power BI / Tableau** (for visual dashboards)

## 📁 Files Included
- `SCM SQL.sql`: Complete SQL script including queries for supply chain KPIs and performance tracking.
- `Hospitality tableau.twbx`: A Tableau dashboard file (related project)
- `Blinkit Dashboard.pbip`: A Power BI dashboard (retail delivery domain)

## 🧾 Sample Queries
```sql
-- Total Orders by City
SELECT customer_city, COUNT(order_id) AS total_orders
FROM orders
GROUP BY customer_city;

-- Average Delivery Time
SELECT AVG(DATEDIFF(day, order_purchase_timestamp, order_delivered_customer_date)) AS avg_delivery_days
FROM orders
WHERE order_status = 'delivered';
