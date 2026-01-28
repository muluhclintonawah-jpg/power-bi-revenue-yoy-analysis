# Power BI Revenue & Year-over-Year Analysis

## 📊 Project Overview
This project demonstrates a complete Power BI revenue analysis workflow, including data modeling, DAX time intelligence, and business-focused dashboard design.

The dashboard analyzes monthly revenue performance and year-over-year (YoY) growth to help stakeholders understand business trends and performance changes over time.

---

## 🧠 Key Business Questions Answered
- How does revenue trend over time?
- How does current performance compare to the previous year?
- Are there clear growth or decline patterns over time?

--

## 🛠 Tools & Technologies
- Power BI
- DAX (Time Intelligence)
- Data Modeling
- Calendar Table Design

---

## 📐 Data Modeling
A dedicated calendar table was created to enable accurate time-intelligence calculations such as YoY growth.

**Relationship**
- Calendar_Table[Date] → monthly_revenue[MonthDate]
---

## 🗄️ SQL Analysis

SQL was used to extract, aggregate, and prepare revenue data before visualization.

### Example: Monthly Revenue Aggregation
```sql
SELECT
    DATE_TRUNC(order_date, MONTH) AS month_date,
    SUM(revenue) AS revenue
FROM transactions
GROUP BY month_date
ORDER BY month_date;

---

## 📈 DAX Measures Used

### Total Revenue
```DAX
Total Revenue =
SUM(monthly_revenue[revenue])
