# Demand, Supply & Inventory Planning – Power BI

An end-to-end Power BI dashboard designed to support demand planning, supply planning, inventory management, and replenishment decisions.

The project connects demand forecasting with inventory and supply analysis to provide a practical view of SKU-level planning performance and inventory risk.

---

## 📊 Project Overview

This project demonstrates how Power BI and DAX can be used to transform transactional sales and inventory data into actionable supply chain insights.

The dashboard is divided into two main areas:

1. Demand Planning
2. Supply & Inventory Planning

The objective is to help planners answer questions such as:

- What is the current demand trend?
- How does actual demand compare with forecast?
- How accurate is the forecast?
- Is forecast bias creating planning risk?
- Which SKUs are approaching their reorder point?
- Which SKUs have inventory deficits?
- How much inventory is currently available?
- How many days of inventory coverage remain?
- Which SKUs require replenishment?

---

# 🏗️ Dashboard Structure

## 1. Demand Planning

The Demand Planning page focuses on understanding historical demand and evaluating forecast performance.

### Key Analysis

- Total Demand
- Total Net Sales
- Monthly Demand Trends
- 3-Month Moving Average Forecast
- Forecast Accuracy
- Forecast Bias
- Forecast Error
- Actual vs Forecast comparison
- Year and Month analysis

### Business Questions

The dashboard helps answer:

> Is demand increasing or decreasing?

> How closely does the forecast track actual demand?

> Is the forecast consistently overestimating or underestimating demand?

> Which periods show significant forecast error?

---

# 2. Supply & Inventory Planning

The Supply & Inventory Planning page focuses on inventory health and replenishment decisions.

### Key KPIs

- Current Inventory
- Average Daily Demand
- Inventory Coverage Days
- Reorder Point
- Inventory Value
- Inventory Risk

### Inventory Analysis

The dashboard includes:

- SKU-level inventory analysis
- Lead Time Days
- Reorder Point
- Inventory Surplus / Deficit
- Days Until Reorder
- Inventory Risk classification
- Top 10 SKU Inventory vs Reorder Point

### Business Questions

The dashboard helps planners identify:

> Which SKUs are below their reorder point?

> Which SKUs have an inventory deficit?

> Which SKUs need to be reordered?

> How many days remain before reaching the reorder point?

> Which SKUs have sufficient inventory coverage?

> Where is inventory risk concentrated?

---

# 📈 Key Metrics & DAX Logic

The project uses DAX measures to calculate planning KPIs dynamically.

### Average Daily Demand

Average daily demand is calculated using demand over the available date range.

### Inventory Coverage Days

Inventory coverage measures approximately how many days the current inventory can support demand.

Conceptually:

    Inventory Coverage Days =
    Current Inventory / Average Daily Demand

### Reorder Point

The reorder point incorporates demand and supplier lead time.

Conceptually:

    Reorder Point =
    Average Daily Demand × Lead Time
    + Safety Stock

### Inventory Surplus / Deficit

This metric compares current inventory with the reorder point.

    Inventory Surplus / Deficit =
    Current Inventory - Reorder Point

Positive value:
- Inventory is above the reorder point.

Negative value:
- Inventory is below the reorder point.

### Days Until Reorder

This metric estimates how many days remain before inventory reaches the reorder threshold.

    Days Until Reorder =
    Inventory Surplus / Average Daily Demand

Negative values indicate that the SKU has already crossed the reorder threshold.

---

# 🚦 Inventory Risk

Inventory risk is classified using inventory coverage and supplier lead time.

The dashboard categorizes SKUs into:

- High Risk
- Medium Risk
- Low Risk
- Reorder Required

Conditional formatting is used to make inventory risk easier to identify.

### Visual Indicators

🔴 Red = Inventory deficit / reorder attention

🟡 Yellow = Approaching reorder threshold

🟢 Green = Sufficient inventory position

---

# 🎯 Forecasting Approach

The demand planning dashboard uses a 3-month moving average approach to establish a simple demand forecast baseline.

A moving average smooths short-term fluctuations and provides a baseline for comparing actual demand against expected demand.

The forecast is evaluated using:

- Forecast Accuracy
- Forecast Bias
- Forecast Error

This provides a practical framework for identifying forecast performance issues.

---

# 🗂️ Data Model

The Power BI model uses a dimensional structure with a central sales dataset and supporting dimension tables.

### Main Tables

**Sales Data**

Contains transactional sales, demand, inventory, supplier and operational information.

**Dim_product**

Contains product and SKU attributes such as:

- SKU ID
- SKU Name
- Brand
- Category
- Subcategory

**Dim_store**

Contains store-related attributes such as:

- Store ID
- City
- Country
- Channel
- Geographic information

**Dim_Supplier**

Contains supplier information including:

- Supplier ID
- Lead Time
- Purchase Cost

**Time**

Provides the date dimension used for time-based analysis.

---

# 🛠️ Tools & Technologies

- Power BI Desktop
- DAX
- Power Query
- Data Modeling
- Interactive Dashboards
- Conditional Formatting
- KPI Cards
- Slicers
- Tables
- Combo Charts

---

# 📌 Dashboard Features

### Demand Planning

- Monthly demand trend analysis
- Actual vs forecast analysis
- Moving average forecasting
- Forecast accuracy monitoring
- Forecast bias analysis

### Supply & Inventory Planning

- Current inventory monitoring
- Reorder point analysis
- Lead time analysis
- Inventory surplus / deficit
- Days until reorder
- Inventory risk classification
- Top SKU analysis
- Interactive Category and SKU filtering

---

# 💡 Key Supply Chain Concepts Demonstrated

This project demonstrates practical understanding of:

- Demand Planning
- Demand Forecasting
- Forecast Accuracy
- Forecast Bias
- Supply Planning
- Inventory Management
- Replenishment Planning
- Reorder Point
- Safety Stock
- Lead Time
- Inventory Coverage
- SKU-level Analysis
- Inventory Risk Management

---

# 📷 Dashboard Preview

## Demand Planning

_Add Demand Planning dashboard screenshot here._

## Supply & Inventory Planning

_Add Supply & Inventory Planning dashboard screenshot here._

---

# 🎯 Business Impact

The dashboard is designed to support planners in moving from descriptive reporting toward actionable planning decisions.

Instead of only showing historical inventory and sales, the dashboard connects:

**Demand → Forecast → Supply → Inventory → Replenishment**

This allows planners to identify potential inventory risks and prioritize SKUs requiring attention.

---

# 👤 Author

**Abhijeet Mane**

Power BI | Supply Chain Analytics | Demand Planning | Supply Planning

---

## Disclaimer

This project is created for portfolio and learning purposes.
