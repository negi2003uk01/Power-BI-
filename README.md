## 📌 Acknowledgement
This project is based on an assignment provided by DataRoars.
The dataset and problem statement belong to DataRoars and are used here for learning purposes.

# Power-BI Financial Report-
# 📊 Power BI Sales Dashboard (G2N Analysis)

## 📌 Project Overview

This project is a **Power BI dashboard** built to analyze business performance using **Gross-to-Net (G2N)** logic.
It provides insights into **Net Revenue, Discounts, Volume, and Year-over-Year performance**.

---

## 🎯 Key Objectives

* Convert raw sales data into meaningful insights
* Calculate **Net Revenue (NR)** using business rules
* Analyze **Discount impact (G2N)**
* Compare performance with **Previous Year (PY)**
* Build interactive dashboards using slicers

---

## 📊 Key Metrics

### 🔹 Net Revenue (NR)

```DAX
Net Revenue = 
[Gross Revenue]
- [Resizing]
+ [Tax Incentives]
- [Free Goods]
- [Cut-Off]
+ [Royalty]
- [Customer Grade Discount]
```

---

### 🔹 NR vs PY

```DAX
NR vs PY = [Net Revenue] - [NR PY]
```

---

### 🔹 NR % vs PY

```DAX
NR % vs PY =
DIVIDE([NR vs PY], [Net Revenue])
```

---

### 🔹 NR Share %

```DAX
NR Share % =
DIVIDE(
    [Net Revenue],
    CALCULATE(
        [Net Revenue],
        ALL('Date Table'),
        ALL('Product'),
        ALL(Customer)
    )
)
```

---

## 🔄 Data Transformations

* Converted **Volume → Kg** using Product table
* Built **Date Table** for time intelligence
* Applied business rules for:

  * Resizing
  * Tax Incentives
  * Free Goods
  * Cut-Off
  * Royalty
  * Customer Grade Discount

---

## 📈 Dashboard Features

* 📅 Time-based analysis (Year, Quarter, Month)
* 📊 Matrix showing:

  * Net Revenue
  * PY Net Revenue
  * YTD
  * NR vs PY
  * NR % vs PY
* 🎨 Conditional formatting:

  * Positive values → Green
  * Negative values → Red
  * Year totals highlighted
* 📉 Line chart for trend analysis
* 🔎 Slicers for dynamic filtering

---

## 🧠 Key Learnings

* Understanding **filter context in DAX**
* Difference between:

  * `ALL()` vs `ALLSELECTED()`
* Importance of **data modeling & relationships**
* Using `ISINSCOPE()` for hierarchy-based formatting
* Building **dynamic and static KPIs**

---

## 🛠 Tools Used

* Power BI
* DAX (Data Analysis Expressions)
* Excel (Data source)

---

## 📂 Files

* `data.xlsx` → Source dataset
* `.pbix` file → Power BI dashboard

---

## 🚀 How to Use

1. Download the `.pbix` file
2. Open in Power BI Desktop
3. Interact using slicers (Year, Month, Product, etc.)

---

## 📌 Author

* Shrestha mohan negi

---





