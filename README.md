# Power BI Revenue & Year-over-Year Analysis

## 📊 Project Overview
This project demonstrates a complete Power BI revenue analysis workflow, including data modeling, DAX time-intelligence, and business-focused dashboard design.

The dashboard analyzes monthly revenue performance and year-over-year (YoY) growth to help stakeholders understand business trends and performance changes over time.

---

## 🧠 Key Business Questions Answered
- How does revenue trend over time?
- How is current performance compared to the previous year?
- Are there growth or decline patterns month-over-month?

---

## 🛠 Tools & Technologies
- Power BI
- DAX (Time Intelligence)
- Data Modeling
- Calendar Table Design

---

## 📐 Data Modeling
A dedicated calendar table was created to enable proper time-intelligence calculations such as YoY growth.

**Relationship**
- Calendar_Table[Date] → Sales[Order Date]

---

## 📈 DAX Measures Used

### Total Revenue

Year-over-Year Revenue

YoY Revenue =
CALCULATE(
    [Total Revenue],
    SAMEPERIODLASTYEAR(Calendar_Table[Date])
)

```DAX
Total Revenue = SUM(Sales[Revenue])
