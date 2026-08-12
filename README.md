

# Amul- The Taste of India Business Analytics Dashboard
An end-to-end Power BI business intelligence project built using a synthetic Amul dataset to analyze sales performance, product and category trends, customer purchasing behaviour, regional and state-wise performance and returns & quality to identify key business drivers, performance trends and opportunities for improvement.
<p align="center">
<img width="800" height="500" alt="amulpic" src="https://github.com/user-attachments/assets/1feb5d77-5c7e-4cfb-8aef-dd652d8f31c1" />
</p>

## 📌 Project Overview
This project demonstrates an end-to-end **Data Analytics and Power BI workflow** using a synthetically generated sales dataset inspired by Amul's product and distribution ecosystem.
The project presents a complete BI workflow I followed:

**Synthetic Data Generation → Data Understanding → Business Understanding → Data Cleaning → Data Modelling → Date Table creation → DAX → Understanding Brand Guidelines → Generating Power BI Theme → Designing Dashboard Pages → Interactive Visualisation → Advanced Analytics → Business Insights**

The final solution consists of an interactive Power BI report that allows users to explore:

* Overall business performance
* Sales and target achievement
* Product performance → Product-level details
* Customer behaviour and segmentation → Customer-level details
* Regional performance
* Returns and quality

> **Note:** The dataset used in this project is synthetic and created solely for this portfolio project. It is not official Amul business data.

## 🛠️ Tools & Technologies
* Microsoft Excel
* Power Query
* PowerBI Desktop
* DAX
* Canva
* Figma
* AI assisted data generation
  
## 📊 Dashboard Preview
<img width="1323" height="737" alt="01_landing_page" src="https://github.com/user-attachments/assets/db988f59-b2f0-47fa-973a-0a2de094c1de" />
<img width="1320" height="737" alt="02_overview" src="https://github.com/user-attachments/assets/7060f979-fdf1-4ed9-8a1e-f0e9135e1cc1" />
<img width="1325" height="740" alt="03_sales" src="https://github.com/user-attachments/assets/21329bea-9d55-4528-9a4f-ff12675d8d55" />
<img width="1321" height="738" alt="04_products" src="https://github.com/user-attachments/assets/1008e9c3-2501-426c-beb5-4c19cdafb636" />
<img width="1322" height="738" alt="05_customers" src="https://github.com/user-attachments/assets/316ef305-8af4-4bb2-854a-691b977299cd" />
<img width="1322" height="737" alt="06_regions" src="https://github.com/user-attachments/assets/93b1f6ba-78a7-4657-a467-e797d0ec6d9b" />
<img width="1318" height="737" alt="07_returns" src="https://github.com/user-attachments/assets/136b0cc1-27ef-469d-a4dc-55dc1cd28431" />

## 🎥 Dashboard Walkthrough
https://github.com/user-attachments/assets/5e17ce73-a5c1-4907-84e0-3088254ca261

## 🤖 AI-Powered Analytics
Across the 6 report pages, I incorporated **AI-powered visuals such as Decomposition Tree and Key Influencers** to perform deeper data analysis, uncover underlying patterns and identify meaningful business insights.
<img width="1110" height="598" alt="Screenshot 2026-08-12 221920" src="https://github.com/user-attachments/assets/887021c1-34cd-4e90-b71c-12db82345d53" />
<img width="1112" height="600" alt="Screenshot 2026-08-12 221941" src="https://github.com/user-attachments/assets/cacfc305-a5c2-4efa-b25d-a0818cd55dc2" />
<img width="1023" height="578" alt="Screenshot 2026-08-12 222001" src="https://github.com/user-attachments/assets/956ba335-59c6-465c-a09a-caec229556a9" />
<img width="1035" height="591" alt="Screenshot 2026-08-12 222019" src="https://github.com/user-attachments/assets/c8240365-5bdb-49a3-a501-c70e13312e33" />
<img width="1110" height="597" alt="Screenshot 2026-08-12 222033" src="https://github.com/user-attachments/assets/d45ee53d-ffec-40f7-9314-410d163363b6" />
<img width="1036" height="592" alt="Screenshot 2026-08-12 222048" src="https://github.com/user-attachments/assets/c4498d8b-1746-4bb6-8d5c-c3ebbdb447bc" />

## 🎛️ Interactive Power BI Features
    ├── Slicers
    ├── Bookmarks
    ├── Field Parameters
    ├── Drill Down / Drill Up
    ├── Drill Through
    ├── Page Navigation
    └── Conditional Formatting

## 🔄 Project Workflow

### 1. Data Generation
   * Created a synthetic Amul sales and business dataset using AI.
   * Generated data covering sales, inventory, returns, customers, products, stores, sales channels, warehouses and marketing campaigns. The dataset used for this project contains total 11 transaction tables.
> Refer dataset folder for list of fact and dimensional tables used for the project.

### 2. Business Understanding
   The dashboard was designed around a series of business questions. The main analytical areas were defined as:
   * Executive Overview
   * Sales Performance
   * Products Performance
   * Customer Insights
   * Regional Performance
   * Returns & Quality

The report pages created helped to answer several business questions like:
* How was overall sales performance and growth?
* Which products and categories drive the most sales?
* Are sales meeting the monthly targets?
* Which customers contribute the most to sales and orders?
* Which sales channels contribute the most revenue?
* Which region and states perform the best?
* What are the major reasons for product returns?
* Which products have higher return rates? etc.

### 3. Data cleaning using PowerQuery
   The raw data was prepared using **Power Query** before being loaded into the analytical model.

The cleaning process included:
* Removing unnecessary columns
* Checking and correcting data types
* Handling blank/null values
* Removing duplicate records where required
* Standardising text values
* Cleaning category and subcategory names
* Validating date columns
* Formatting numeric fields
* Creating/transforming fields required for analysis
* Ensuring consistent values across dimension and fact tables

### 4. Data Modelling
   * Creation of fact and dimensional tables
   * Creation of Galaxy Schema (Fact Constellation Schema)
   * Created dimension tables for Customer, Product, Store, Sales Channel, Marketing, and Warehouse.
   * Established relationships between fact and dimension tables using appropriate keys.
   <img width="1372" height="717" alt="image" src="https://github.com/user-attachments/assets/bfea5450-d3c0-4f51-b717-fcbde2b7920c" />

   #### FACT TABLES
* Fact Sales
* Fact Target
* Fact Inventory
* Fact Marketing
* Fact Returns
      
  #### DIMENSION TABLES
* Dim customer
* Dim product
* Dim marketing
* Dim sales channel
* Dim store
* Dim warehouse

### 5. Date Table creation
Created a dynamic Date table using DAX to work with time intelligence functions. The date table was then related to the relevant fact table date field.

``` dax
Date =
ADDCOLUMNS(
    CALENDARAUTO(),
    "Year", YEAR([Date]),
    "Month no", MONTH([Date]),
    "Month name", FORMAT([Date], "mmm"),
    "Quarter", "Q" & QUARTER([Date]),
    "Day", WEEKDAY([Date], 2),
    "Day name", FORMAT([Date], "ddd")
)
```

### 6. DAX measures and calculated columns creation
Created DAX measures to calculate important business metrics and support interactive analysis.
Key KPIs include:
* Total Sales
* Total Orders
* Total Customers
* Total Products
* YoY Sales Growth
* MoM Sales Growth
* YoY Order Growth
* MoM Order Growth
* Sales Contribution
* Customer Segmentation
* Top product
* Top customer
* Total returns
* Return rate %
* Repeat customer rate etc.

### 6. Amul Brand Guidelines and Theme development using AI
Before designing the final dashboard, a separate **brand guidelines presentation** was developed to establish a consistent visual identity.
The brand guidelines considered brand colors and visual identity.

The brand guidelines were translated into a customized Power BI theme.
The theme was used to maintain consistency across:
<ul>
  <li>Charts</li>
   <li>Titles</li>
   <li>Data labels</li>
   <li>KPI cards</li>
   <li>Buttons</li>
   <li>Slicers</li>
   <li>Tables</li>
   <li>Background elements</li>
   <li>Accent colours</li>
</ul>
This helped create a consistent visual language across all report pages.

### 7. Dashboard development
Designed an interactive multi-page dashboard following the Amul visual identity.

The report contains:
1. Overview
2. Sales Analysis
3. Product Analysis
4. Customer Analysis
5. Regional Analysis
6. Returns Analysis

The dashboard includes KPI cards, charts, slicers, navigation buttons, and interactive analytical components.

### 7. Advanced PowerBI features
Several Power BI features were implemented to make the report interactive and user-friendly.
* Bookmarks for interactive filter panels
* Drill-through for detailed analysis
* Drill-down for hierarchical exploration
* Field Parameters for dynamic visual analysis
* Navigation Buttons for page navigation
* Tooltips for additional context
* Interactive slicers and filters

# 📄 Report Pages

| Page | Focus |
|------|-------|
| **Executive Overview** | Overall business performance and key KPIs at a glance |
| **Sales** | Track sales trends, sales channels and overall sales performance |
| **Product** | Analyze product sales and demands |
| **Customer** | Understand customer performance, purchasing behavior and segmentation |
| **Region** | Regional and state-level sales performance and comparison |
| **Returns** | Monitor return trends, return quantities, refund amounts and return reasons |

## 💡 Key Insights

1. Executive Overview
   <img width="782" height="467" alt="image" src="https://github.com/user-attachments/assets/f02ddeb2-dafe-4ec6-a304-53e6273b94c5" />

2. Sales Performance
   <img width="772" height="407" alt="image" src="https://github.com/user-attachments/assets/821a7b77-2431-4d20-9dd7-15df4ca2e4f2" />

3. Products Performance
   <img width="781" height="387" alt="image" src="https://github.com/user-attachments/assets/4a0d03bc-99be-4d74-834d-f786c78a24a5" />

4. Customer Insights
   <img width="780" height="375" alt="image" src="https://github.com/user-attachments/assets/1633316c-fc55-4eb7-9c1e-f40152554f1f" />

5. Regional Performance
   <img width="780" height="400" alt="image" src="https://github.com/user-attachments/assets/702d7b4f-060b-463c-a2fd-d736769154ef" />

6. Returns & Quality
   <img width="777" height="357" alt="image" src="https://github.com/user-attachments/assets/1cad0e6d-905d-4506-9d21-48e045e826c1" />

<p>If you found this project helpful, consider giving it a ⭐ on GitHub!<br> Thank you❤️</p>
<div>
  <h2>Connect with Me</h2>
<a href="mailto:aiswarya2000mohan@gmail.com">
  <img src="https://img.shields.io/badge/-Gmail-red?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail">
</a>
<a href="https://www.linkedin.com/in/aiswarya-mohan-950948221/">
  <img src="https://img.shields.io/badge/-LinkedIn-blue?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn">
</a>
</div>


