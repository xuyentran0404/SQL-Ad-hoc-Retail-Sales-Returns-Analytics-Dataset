# [SQL Ad_hoc] Retail Sales Returns Analytics Dataset
---
## 1. Introduction 
This dataset provides a comprehensive view of a retail business's operations over a three-year period (2015–2017). It includes detailed records of sales transactions, customer profiles, product catalog, and return data, making it an excellent foundation for conducting end-to-end business analysis.  

The data is structured into multiple relational tables that simulate a real-world retail environment, enabling advanced SQL queries for revenue analysis, customer segmentation, product performance evaluation, and return behavior tracking.  

🧱 **Dataset Structure**
- **Customers**: Demographic and behavioral data for each customer, including income, education, occupation, and homeownership status.
- **Products**: Details about products such as name, model, color, size, cost, and price, along with their subcategories and categories.
- **Sales (2015, 2016, 2017)**: Transactional records with order details, customer IDs, product IDs, and quantity sold.
- **Returns**: Data on returned products, including quantity and date.
- **Product Categories & Subcategories**: Hierarchical mapping of products to subcategories and main categories.

---

## 2. Database Access  
This dataset is hosted on a remote Azure SQL Database. You can connect to it using tools like SQL Server Management Studio (SSMS), Azure Data Studio, DBeaver, or any SQL client that supports Microsoft SQL Server.  
🛠️ **Connection Details**:
- Server Name: learnsqlwithmaz.database.windows.net
- Database: (select or connect to the default database after login)
- Username: sql_reader
- Password: cungmazhocdata10@
- Authentication Type: SQL Server Authentication

---

## 3. Exploring the Dataset
In this project, I will write 05 queries in SQL Server Management Studio to tackle the problems defined above  
**Business Objective**:
- Does revenue tend to increase or decrease over time?
- Top-selling products each year (by number of units sold) 
- Compare revenue and growth rate year by year
- Top 5 products with the most returns 
- Calculate the total sales, revenue and profit, profit margin, and total number of returns for each modelName  

**Query 01: Total revenue by month/quarter/year**
- SQL code
![image](https://github.com/user-attachments/assets/da0097a8-202e-4569-8591-c9bed1632a76)

- Query results
![image](https://github.com/user-attachments/assets/c5a0d46f-8c08-4f65-827d-93ed58232e08)

- Visualization
![image](https://github.com/user-attachments/assets/9673a1dd-80b4-4d64-a6f0-74d384f93ef0)

**Insights**
- Consistent revenue growth: Revenue shows a strong upward trend from 2015 to mid-2017, with the overall trajectory confirmed by the trendline.  
- Noticeable revenue fluctuations: Several sharp dips and spikes occur, especially around mid-2015 and early 2017, indicating potential volatility.

**Recommendations**
- Scale what works: Identify and double down on strategies or campaigns that drive peak revenue months to sustain long-term growth.
 Stabilize performance: Investigate causes of revenue dips and implement forecasting or inventory strategies to reduce fluctuations.

**Query 02: Best-Selling Products by Year (by quantity sold)**
- SQL code
![image](https://github.com/user-attachments/assets/77f918f4-8ec5-4c4a-be54-3a3609e1aa0f)

- Query results
![image](https://github.com/user-attachments/assets/7d43df15-7170-4fe3-a3bb-cd6ac3c8d8a0)


**Query 03: Revenue Comparison & Growth Rate**
- SQL code
![image](https://github.com/user-attachments/assets/00af6925-0968-4eae-b468-0f4a1a22cbcb)

- Query results
![image](https://github.com/user-attachments/assets/c9bece4c-8b08-4925-8dc6-604a5330ef8e)

**Query 04: Retrieve the Top 5 products with the highest number of returns**
- SQL code
![image](https://github.com/user-attachments/assets/b38ebf9e-4086-445e-ba28-d3f93c74336e)

- Query results
![image](https://github.com/user-attachments/assets/6f588eeb-554d-4038-bb0d-f6a8b0cb91ed)

**Query 05:  Extract total sales, revenue, profit, margin, and returned quantity for each modelName**
- SQL code
![image](https://github.com/user-attachments/assets/a05de7e1-83d6-4dd4-a9fa-4be2c0106c92)
![image](https://github.com/user-attachments/assets/852f1b28-8b17-4bc7-8fc4-e29704769db5)


- Query results
![image](https://github.com/user-attachments/assets/3bbc00a7-d676-4c9c-89a1-1442117340c1)

**Insights**
- High-profit concentration: A small number of models (e.g., Mountain-200, Road-550-W) contribute the majority of overall profit, with strong margins and solid sales volume.
- Unprofitable models: Several products (e.g., Touring-1000, Road-150, Road-750) generate high revenue but suffer from negative profit margins, indicating pricing, cost, or return issues.

**Recommendations**
- Double down on winners: Prioritize investment in high-performing models through increased marketing, optimized inventory, and bundling with accessories to drive higher revenue per transaction.
- Fix or phase out poor performers: Audit unprofitable products to identify causes (e.g., costs, pricing, returns) and take action — either improve their economics or discontinue to reduce losses.
