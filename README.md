# Pizza-Sales-Analysis
A full-stack data analytics project using MySQL and Power BI to explore pizza sales trends, optimize marketing, improve inventory, and boost customer satisfaction.

# 🍕 Pizza Sales Analysis – Data Insights Project

This project analyzes pizza sales data using **MySQL** and **Power BI** to uncover key business insights. It explores order patterns, revenue drivers, peak hours, and product performance, ultimately helping to optimize business strategies in the competitive food industry.

---

## 🧾 Project Objective

- Analyze pizza sales data to derive actionable insights.
- Identify best-selling pizzas, peak ordering hours, and revenue trends.
- Improve inventory management, marketing, and customer experience.
- Use data-driven strategies to enhance decision-making and profitability.

---

## 🛠️ Tools & Technologies Used

- **MySQL** – Data storage and querying
- **Power BI** – Data visualization and interactive dashboards
- **CSV/Excel** – Data source files
- **SQL** – For data analysis and metric calculation

---

## 📁 Project Structure

| File | Description |
|------|-------------|
| `Pizza_sales.pbix` | Power BI dashboard with all visualizations |
| `Pizza Sales queries.sql` | SQL script containing 15+ business queries |
| `Pizza Sales Analysis Data Files.rar` | Raw CSV files used for analysis |
| `Pizza Sales Analysis.docx` | Full academic project report with insights and visuals |

---

## 📊 Key Metrics & Queries

- Total orders, total revenue, average order value
- Most & least popular pizzas
- Top 5 pizzas by quantity and revenue
- Hourly & weekly order trends
- Category-wise sales and revenue
- Revenue contribution by pizza size
- Cumulative sales over time

✅ Sample SQL Query:
```sql
SELECT pizza_types.name, 
       SUM(order_details.quantity * pizzas.price) AS revenue
FROM pizzas
JOIN pizza_types ON pizzas.pizza_type_id = pizza_types.pizza_type_id
JOIN order_details ON pizzas.pizza_id = order_details.pizza_id
GROUP BY pizza_types.name
ORDER BY revenue DESC
LIMIT 5;
