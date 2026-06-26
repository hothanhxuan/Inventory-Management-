# 🍣 Project 8: Inventory Management System - USER GUIDE | Microfsoft Excel

**Domain:** 
F&B | Restaurant | Sushi Restaurant in Finland

![Image](https://github.com/user-attachments/assets/640515ad-09d2-440f-9100-5f24476c346f)

Author: Susan Ho 
Date: 2026-06-26 
Tools Used: Excel 

---

## 📖 OVERVIEW
The Sushi Inventory Management System is an Excel-based application designed to digitize and automate the supply chain management process for small-to-medium sushi restaurants (SMEs).

The system tracks **34 core ingredients** across 3 categories (Dry Goods, Frozen, and Fresh Produce) through a dataset of over 6,000 daily transaction records, enabling restaurant owners to make data-driven purchasing decisions and optimize cash flow.

**Target Users:** Kitchen staff, Head chefs, Store managers, Sushi restaurant owners
**Data Scale:** 6,120 records | 34 products | 3 categories | 3 suppliers | 6 months (H1 2025)  
---

## 🚀 SHEET STRUCTURE & HOW TO USE

### 1. Dashboard (Central Control Panel)
- **Purpose:** Provides a bird's-eye view of the restaurant's inventory health at a glance.
- **How to Use:**
  - **KPI Cards:** Instantly monitor total products tracked, total transaction records, alert status, and category count.
  - **Stock Status Summary:** Quick-reference table listing all 34 products with their ID, name, supplier, and lead time.
  - **Heatmap (Monthly Consumption Heat Map):**
    - 🟩 Green: High consumption (Best-selling / High-usage items).
    - 🟧 Orange: Medium consumption.
    - 🟦 Blue: Low consumption (Monitor expiration dates closely).

### 2. Raw Data (Daily Transaction Log)
- **Purpose:** The single point of data entry for the entire system.
- **How to Use (For Staff):**
  - Enter daily figures into `received_qty` (Stock received from supplier), `used_qty` (Stock consumed/sold), and `waste_qty` (Damaged/expired stock).
  - The system automatically calculates `closing_stock` (End-of-day inventory balance).
  - *Note:* Rows with `Critical` status are automatically highlighted in orange via Conditional Formatting for immediate visibility.
  - **AutoFilter:** Click the dropdown arrows on the header row to filter by date, product, or status.
  - **Freeze Panes:** The header row is frozen so column names remain visible when scrolling through 6,000+ rows.

### 3. Stock Alerts (Inventory Warning Center)
- **Purpose:** Crisis management hub — ensures the restaurant never runs out of key ingredients mid-service.
- **How to Use (For Head Chef / Manager):**
  - Open this sheet at the beginning of every shift.
  - **Red Zone (OUT OF STOCK):** Closing stock has reached zero. Immediately contact the supplier for emergency delivery or purchase from local markets.
  - **Orange Zone (LOW STOCK):** Inventory has dropped to a critical threshold. Add these items to tomorrow's Purchase Order list.

### 4. Monthly Analysis (Trend Analysis by Month)
- **Purpose:** Provides historical data to support bulk purchasing negotiations and demand forecasting.
- **How to Use:**
  - Review the **H1 Total** column (Total consumption for the first half of the year) and **Monthly Avg** (Average monthly usage).
  - Use the monthly average to negotiate volume discounts with suppliers when committing to large-quantity contracts.
  - **Heatmap Color Coding:**
    - 🟢 Dark Teal: Very high consumption (> 150 units/month).
    - 🔵 Light Blue: Medium consumption (51–150 units/month).
    - 🟢 Light Green: Low consumption (11–50 units/month).

### 5. Product Details (Individual Product Profiles)
- **Purpose:** Deep-dive reference for any specific ingredient.
- **How to Use:** Scroll through the color-coded product cards. Each card displays:
  - **Unit:** Measurement unit (kg, unit, etc.).
  - **Lead Time:** Supplier delivery time (in days).
  - **Reorder Point:** Minimum stock level — when stock hits this number, a new order must be placed.
  - **Reorder Qty:** Standard order quantity per purchase.
  - **Jan – Jun Used:** Actual monthly consumption breakdown for the past 6 months.

### 6. Supplier Report (Vendor Performance Evaluation)
- **Purpose:** Evaluate and compare supplier performance for strategic sourcing decisions.
- **How to Use:** Review the following key metrics:
  - **Total POs:** Total number of purchase orders placed with the supplier.
  - **Total Recv (Qty):** Total quantity of goods received.
  - **Avg Lead Time:** Average delivery time (in days).
  - **Activity Grade:** Supplier engagement level (Active / Steady / Low) — use this to decide whether to continue the partnership or explore alternative vendors (especially critical for perishable seafood).

### 7. Pivot Summary (Executive Insights)
- **Purpose:** High-level diagnostic report on product lifecycle and inventory risk.
- **How to Use:**
  - **Category Breakdown:** Identify which category (Dry / Frozen / Fresh) consumes the most budget and has the most shortage days.
  - **Stockout Health:** The most critical metric. Based on `Days Until Stockout`, the system assigns a health label:
    - 🔴 **CRITICAL (< 5 days):** Restock immediately — no exceptions.
    - 🟠 **WARNING (< 15 days):** Plan a restock order within this week.
    - 🟢 **HEALTHY (≥ 15 days):** Stock levels are safe — no action needed.

---

## 👥 ROLE-BASED ACCESS GUIDE

| Role | Primary Sheets | Frequency | Key Actions |
|---|---|---|---|
| Kitchen Staff | Raw Data | Daily | Enter end-of-shift inventory data |
| Head Chef | Stock Alerts | Start of each shift | Check for shortages & place urgent orders |
| Store Manager | Dashboard, Monthly Analysis | Weekly | Plan restocking & review consumption trends |
| Restaurant Owner | Supplier Report, Pivot Summary | Monthly / Quarterly | Negotiate with suppliers, optimize costs |

---

## 📊 ADVANCED EXCEL TECHNIQUES USED

| Technique | Application in This Project |
|---|---|
| Conditional Formatting | Auto-highlights Critical status rows with orange background on Raw Data |
| AutoFilter | Enables instant data filtering across 6,000+ records by any column |
| Freeze Panes | Locks header row for seamless scrolling through large datasets |
| Dynamic Color Palette | 34 unique hex color codes auto-rotate for Product Detail cards |
| Heatmap Visualization | Color-gradient consumption maps on Dashboard and Monthly Analysis |
| KPI Dashboard Cards | Professional metric cards with custom borders and color schemes |
| Multi-Sheet Architecture | 7 purpose-built sheets with cross-referencing data flow |
| Print-Ready Layout | Pre-configured page setup with margins, headers, and footers |

---

## 💡 TIPS FOR EFFICIENT USE

1. **Quick Navigation:** Press `Ctrl + Page Down` / `Ctrl + Page Up` to switch between sheets instantly.
2. **Quick Search:** Press `Ctrl + F` to search for any product name or PO number across all sheets.
3. **Data Filtering:** On the Raw Data sheet, click the filter dropdown arrows on the header row, then select "Text Filters" > "Contains" to search by keyword.
4. **Export to PDF:** Press `Ctrl + P` > Select "Microsoft Print to PDF" to save any report as a PDF for email distribution to management.

---

> *"This project demonstrates advanced Excel proficiency applied to a real-world supply chain management problem in the F&B industry — from daily data entry operations to strategic analytics for executive decision-making."*
