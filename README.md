# Zomato-Data-Manipulation-and-Reporting-with-Power-BI

## 📋 Project Overview

Zomato, a global restaurant aggregator and food delivery company, aims to uncover insights from its data across various continents. The goal of this project is to build an **interactive, consolidated Power BI report** that empowers stakeholders to analyze and assess business performance across global markets.

This project involves cleaning, transforming, and visualizing restaurant data sourced from multiple Excel files—each corresponding to a continent—while following business-specific requirements for filtering, grouping, and mobile responsiveness.

---

## 🎯 Project Objectives

- ✅ Consolidate restaurant data from various continents into a unified Power BI model.
- ✅ Provide global drill-down insights from continent → country → city.
- ✅ Identify:
  - Top-rated restaurants
  - Lowest-cost restaurants
  - Restaurants serving the most cuisines
- ✅ Enable dynamic filtering based on:
  - Geography (continent, country, city)
  - Service availability (online ordering, reservation)
  - Rating slabs (with color codes)
- ✅ Design a **multi-page, Zomato-themed** Power BI dashboard.
- ✅ Ensure accessibility across both **web browsers and mobile devices**.

---

## 🗂️ Data Preparation Steps

1. **Import Datasets:**
   - Load all Excel files corresponding to different continents.

2. **Data Cleaning & Transformation (Power Query):**
   - Standardize `City` names:
     - "Sí£o Paulo" ➝ "São Paulo"
     - "ÛÁstanbul" ➝ "Istanbul"
     - "Cedar Rapids/Iowa City" ➝ "Cedar Rapids"
   - Remove unused or irrelevant columns.
   - Create a combined **`Restaurant Name & Address`** column.
   - Split cuisines into a separate **cuisine dimension table**.
   - Ensure `Country Code` table has **unique, non-null** values only.

---

## 📐 Data Modeling

- Establish relationships between:
  - Restaurants
  - Country & continent
  - Cuisines
- Set up a **star schema** for optimized performance.

---

## 🧠 DAX Calculations

### ➕ Columns:
- **Rating Color**
  - Based on `Aggregate Rating`, map:
    - Above 4.5 → `Dark Green`
    - 4.0 – 4.4 → `Green`

- **Continent Column**
  - Add to `Country Code` table using custom logic:
    - Example: `Africa` → `South Africa`
    - Ensure each country is correctly mapped to its respective continent.

### 📏 Measures:
- `Restaurant Count`
- `Average Cost`
- `Average Rating`
- `Cuisine Count`

---

## 🧭 Dashboard Features

- 🌍 **World Map Drill Down**  
  Start from a high-level view of continents and drill down to countries and cities.
  
- 🌟 **Top-Rated & Most Popular**  
  Highlight top restaurants based on average ratings and cuisine variety.

- 💲 **Cost Insights**  
  Identify locations with the lowest average restaurant costs.

- 🎨 **Rating Color Legends**  
  Use color codes for better UX: Dark Green, Green, etc.

- 📱 **Mobile-Friendly Design**  
  Optimized layout and bookmarks for mobile view.

- 📄 **Multi-Page Report Navigation**  
  Pages include: Overview, Cost Analysis, Cuisine Insights, Location Drilldowns.

---

## 📎 Technologies Used

- **Power BI Desktop**
- **Power Query Editor**
- **DAX**
- **Excel (source data)**

---

## 🛠 Folder Structure

