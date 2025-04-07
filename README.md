# Wayfair A/B Testing Case Study

Welcome to the Wayfair Case Study repository. This project analyzes a large-scale A/B test conducted by Wayfair during the 2016 holiday season. The focus of the test was to determine whether displaying a **"Ships in Time"** guarantee to one-third of customers would influence shopping behavior, particularly in terms of purchases, cancellations, and returns.

---

## 📊 Project Overview

Wayfair ran an A/B test to evaluate whether a delivery guarantee shown during the holiday season would justify the associated operational costs. The report is divided into two major components:

1. **Exploratory Data Analysis (EDA)** – Understand and visualize customer behavior across user types and product categories.
2. **Campaign Effectiveness Analysis** – Evaluate the impact of the guarantee on shopping behavior, cancellations, and returns.

---

## 🧪 1. Exploratory Data Analysis (EDA)

**Objective:** Understand customer behavior by examining interactions between user types and product categories, including purchase structure and data quality.

### 🔍 Key Insights:
- **Level of Detail:** The finest level is `Order Product ID`. Some products can be purchased in sets (e.g., dining sets), others individually.
- **Data Quality Issues:** Inconsistencies in `Purchased Quantity` and duplicated `Order Product IDs` suggest data cleaning is necessary for deep analysis.
- **User Type Behavior:** Distinct purchasing patterns emerge across user groups — *New Visitors, Returning Visitors, Acquired Members,* and *Activated Customers*.

**Visualization Dashboard:**  
[Wayfair EDA - Tableau Sheet 15](https://public.tableau.com/views/WayfairABtesting2/Sheet15)

---

## 🎯 2. Campaign Effectiveness Analysis

### Business Question 1:
**Did certain product categories perform better in terms of sales or lower return rates?**

**Visualization:**  
[Campaign Sales & Return Comparison - Tableau Sheet 14](https://public.tableau.com/views/WayfairABtesting2/Sheet14)

**Findings:**
- 10 out of 34 categories had higher-than-average sales in the Guarantee group:
  - *Mattresses, Small Electrics, Kitchen, Office Supplies, Education, Rugs, Outdoors,* etc.
- However, some of these categories also had higher return rates, implying delivery expectations may not have been met.
- Flooring saw notably more purchases in the control group, suggesting less urgency for timely delivery.

**Implication:** Target the guarantee toward fast-moving, time-sensitive categories while improving messaging to reduce return rates.

---

### Business Question 2:
**Was there a significant difference in cancellation and return rates between orders with the guarantee and those without?**

**Visualization:**  
[Cancellation & Return Rates - Tableau Sheet 5](https://public.tableau.com/views/WayfairABtestq1/Sheet5)

**Findings:**
- **Cancellations:** Guarantee group had significantly fewer cancellations (0.021) vs control group (0.058).
- **Returns:** No meaningful difference (Guarantee: 0.057 vs Control: 0.058).

**Implication:** The guarantee increased customer confidence (fewer cancellations) but didn’t reduce dissatisfaction (returns).

---

## ✅ Conclusions and Recommendations

- The "Ships in Time" guarantee impacted behavior **differently by category**.
- **Higher purchases** in categories like *Mattresses* and *Kitchen* imply customers value delivery speed for certain products.
- **Higher returns** in those same categories suggest **expectation mismatches**.
- Guarantee **reduced cancellations** but did **not significantly affect returns**.
- **Future Strategies:**
  - Target the guarantee on **time-sensitive, high-demand items**.
  - Improve **communication of delivery expectations**.
  - Use behavioral data by **user type** for **personalized marketing**.
  - Monitor and clean product/order-level data for accuracy in future experiments.

---

## 📁 File Structure

```bash
├── README.md                 # Project documentation
├── data/                     # Dataset files (not included here)
├── dashboards/               # Tableau links and screenshots
├── notebooks/                # Jupyter/EDA scripts (optional)
├── insights/                 # Summary slides or report files
