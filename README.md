# Shopify-E-Commerce-Sales_Dashboard 


## 📊 Project Overview

This Power BI dashboard provides a **comprehensive analysis of Shopify e-commerce sales** performance and customer behavior. It enables stakeholders to explore **net sales**, **customer retention**, **payment preferences**, **regional trends**, and **product performance** through **interactive visualizations and drillthrough features**.

The goal is to **empower data-driven decisions** by uncovering insights in customer loyalty, order trends, and sales performance across various dimensions.

---

## 🧠 Business Objective

To harness Power BI for uncovering insights into Shopify store performance, including:

- Customer behavior and segmentation
- Product category performance
- Payment method analysis
- Geographic distribution of sales
- Repeat customer value and trends

By building this interactive report, stakeholders can **optimize product strategies**, **improve regional marketing**, and **enhance customer retention**.

---

## 🗂️ Dataset

> **Note**: Sample Shopify sales dataset is used for this project.

Key tables include:
- `Orders`
- `Customers`
- `Products`
- `Payments`
- `Regions`

---

## ❓ Key Business Questions (KPIs)

1. 💰 What is the overall transaction performance in terms of **Net Sales**, **Quantity**, and **Average Order Value**?
2. 🔁 How many customers are **repeat buyers** vs. **one-time purchasers**?
3. 🧾 What is the **Customer Lifetime Value (LTV)**, **repeat rate**, and **purchase frequency**?
4. 🌍 Which **regions, provinces, or cities** contribute most to sales and engagement?
5. 💳 What are the **most and least used payment methods**?
6. 📦 Which **product categories** are driving the highest revenue and orders?
7. ⏰ How do **sales and customer activity vary by day and hour**?

---

## 🛠️ Tools & Technologies

| Category              | Tools Used              |
|-----------------------|--------------------------|
| Dashboard & Reporting | Power BI Desktop         |
| Data Processing       | Power Query              |
| Data Modeling         | Power BI Data Model      |
| Calculations          | DAX (Data Analysis Expressions) |
| Data Source           | Sample Shopify Dataset   |

---

## 🧮 Key DAX Measures

```DAX
Net Sales = SUM(Orders[Total Amount])
Total Quantity = SUM(Orders[Quantity])
Average Order Value = [Net Sales] / DISTINCTCOUNT(Orders[Order ID])
Repeat Customer Count = CALCULATE(DISTINCTCOUNT(Customers[Customer ID]), FILTER(Customers, Customers[Order Count] > 1))
Repeat Rate = [Repeat Customer Count] / DISTINCTCOUNT(Customers[Customer ID])
Lifetime Value = [Net Sales] / DISTINCTCOUNT(Customers[Customer ID])
Purchase Frequency = [Total Quantity] / DISTINCTCOUNT(Customers[Customer ID])
