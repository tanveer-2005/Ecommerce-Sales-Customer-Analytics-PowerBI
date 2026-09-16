\# E-Commerce Sales \& Customer Analytics Dashboard



\## 📊 Project Overview



The \*\*E-Commerce Sales \& Customer Analytics Dashboard\*\* is a 4-page interactive Power BI project designed to analyze e-commerce sales performance, product performance, customer behavior, marketing activities, delivery performance, and returns.



The project transforms raw e-commerce data into meaningful business insights using \*\*Power BI, Power Query, Data Modeling, and DAX\*\*.



\---



\## 🎯 Project Objectives



\- Analyze overall sales and profitability

\- Track revenue, profit, orders, and customer metrics

\- Analyze product and category performance

\- Understand customer segments and behavior

\- Analyze marketing and sales channels

\- Monitor delivery performance

\- Analyze returns and customer ratings

\- Build interactive dashboards using DAX and slicers



\---



\## 📁 Dataset



The project uses the following CSV files:



\- `ecommerce\_sales\_customer\_analytics\_150k.csv`

\- `customer\_master.csv`

\- `order\_items.csv`

\- `product\_catalog.csv`



The main sales dataset contains approximately \*\*138K orders\*\* covering the period \*\*2021–2025\*\*.



\### Important Fields



\- Order ID

\- Order Date

\- Order Status

\- Sales Channel

\- Customer ID

\- Customer Segment

\- Customer Type

\- Region

\- Payment Method

\- Shipping Method

\- Delivery Status

\- Return Status

\- Marketing Channel

\- Campaign Name

\- Quantity

\- Gross Sales

\- Discount Amount

\- Tax Amount

\- Shipping Cost

\- Net Sales

\- Product Cost

\- Profit

\- Customer Rating

\- Customer Lifetime Value



\---



\# 📑 Dashboard Pages



\## 1. Executive Overview



Provides a high-level overview of e-commerce business performance.



\### KPIs



\- Total Revenue

\- Total Profit

\- Total Orders

\- Total Customers

\- Average Order Value

\- Profit Margin

\- Return Rate

\- Cancellation Rate



\### Visualizations



\- Revenue \& Profit Trend

\- Revenue by Year

\- Revenue by Region

\- Revenue by Sales Channel

\- Orders by Order Status

\- Profit by Region



\*\*Theme:\*\* Blue 🔵



\---



\## 2. Sales \& Product Analysis



Focuses on product and sales performance.



\### KPIs



\- Total Quantity Sold

\- Total Products

\- Product Profit

\- Average Unit Price

\- Product Sales Revenue

\- Average Discount %

\- Average Product Rating



\### Visualizations



\- Top 10 Products by Revenue

\- Revenue by Brand

\- Quantity Sold by Product Category

\- Revenue by Product Category

\- Profit by Product Category

\- Average Discount % vs Product Profit



\*\*Theme:\*\* Orange 🟠



\---



\## 3. Customer Analytics



Analyzes customer demographics, segmentation, lifetime value, and acquisition cost.



\### KPIs



\- Total Customers

\- Repeat Customers

\- Repeat Customer %

\- Average Customer Lifetime Value

\- Average Customer Age

\- Average Acquisition Cost



\### Visualizations



\- Customers by Customer Segment

\- Customers by Customer Type

\- Customers by Gender

\- Customer Lifetime Value by Customer Segment

\- Customers by Region

\- Top 10 States by Customers

\- Customers by Age Group

\- Average Acquisition Cost by Customer Segment



\*\*Theme:\*\* Purple 🟣



\---



\## 4. Marketing, Delivery \& Returns



Analyzes marketing channels, delivery performance, returns, and customer ratings.



\### KPIs



\- Total Orders

\- Total Revenue

\- Return Rate

\- Cancellation Rate

\- Average Delivery Days

\- Average Customer Rating



\### Visualizations



\- Revenue by Marketing Channel

\- Orders by Marketing Channel

\- Revenue by Sales Channel

\- Orders by Delivery Status

\- Average Delivery Days by Shipping Method

\- Returns by Return Reason

\- Revenue by Campaign

\- Customer Rating Distribution



\*\*Theme:\*\* Red/Coral 🔴



\---



\# 🛠️ Tools \& Technologies



\- Microsoft Power BI

\- Power Query

\- DAX

\- Data Modeling

\- CSV

\- Git

\- GitHub



\---



\# 🔗 Data Model



The project uses relationships between multiple tables:



```text

customer\_master

&#x20;      │

&#x20;      │ 1 : \*

&#x20;      ▼

ecommerce\_sales\_customer\_analytics\_150k

&#x20;      │

&#x20;      │ 1 : \*

&#x20;      ▼

order\_items

&#x20;      │

&#x20;      │ \* : 1

&#x20;      ▼

product\_catalog



A dedicated DateTable is also used for time-based analysis.



📐 Important DAX Measures

Total Revenue

Total Revenue =

SUM(ecommerce\_sales\_customer\_analytics\_150k\[net\_sales])

Total Profit

Total Profit =

SUM(ecommerce\_sales\_customer\_analytics\_150k\[profit])

Total Orders

Total Orders =

DISTINCTCOUNT(ecommerce\_sales\_customer\_analytics\_150k\[order\_id])

Total Customers

Total Customers =

DISTINCTCOUNT(ecommerce\_sales\_customer\_analytics\_150k\[customer\_id])

Average Order Value

Average Order Value (AOV) =

DIVIDE(

&#x20;   \[Total Revenue],

&#x20;   \[Total Orders],

&#x20;   0

)

Profit Margin

Profit Margin % =

DIVIDE(

&#x20;   \[Total Profit],

&#x20;   \[Total Revenue],

&#x20;   0

)

Return Rate

Return Rate =

DIVIDE(

&#x20;   CALCULATE(

&#x20;       \[Total Orders],

&#x20;       ecommerce\_sales\_customer\_analytics\_150k\[return\_status] = "Returned"

&#x20;   ),

&#x20;   \[Total Orders],

&#x20;   0

)

Cancellation Rate

Cancellation Rate =

DIVIDE(

&#x20;   CALCULATE(

&#x20;       \[Total Orders],

&#x20;       ecommerce\_sales\_customer\_analytics\_150k\[order\_status] = "Cancelled"

&#x20;   ),

&#x20;   \[Total Orders],

&#x20;   0

)

📅 Date Analysis



A dedicated Date Table was created for time-based analysis.



The Date Table contains:



Year

Month

Month Number

Month Year

Month Year Sort

Quarter

Day

Day Name

Day of Week Number

Year Month



Month and day fields were sorted using their corresponding numeric sort columns to maintain correct chronological order.



📊 Key Business Metrics



The dashboard analyzes:



Revenue

Profit

Profit Margin

Orders

Customers

Average Order Value

Quantity Sold

Product Revenue

Product Profit

Return Rate

Cancellation Rate

Customer Lifetime Value

Acquisition Cost

Delivery Time

Customer Rating

🎛️ Interactive Features



The dashboards include interactive slicers for:



Year

Month

Region

Sales Channel

Customer Segment

Product Category

Brand

Product Subcategory

Supplier

Marketing Channel

Shipping Method

Customer Type

Gender



These slicers allow users to dynamically filter the dashboards and explore different business segments.



📌 Project Highlights

Built a 4-page interactive Power BI dashboard

Created reusable DAX measures

Built a dedicated Date Table

Created relationships between multiple datasets

Applied data modeling principles

Used Power Query for data preparation

Designed KPI cards and interactive visualizations

Applied page-level color themes

Analyzed sales, products, customers, marketing, delivery, and returns

🚀 How to Use

Clone or download this repository.

Open the .pbix file using Microsoft Power BI Desktop.

If required, update the CSV file paths in Power Query.

Refresh the dataset.

Use the slicers and visuals to explore the analysis.

📷 Dashboard Preview



Screenshots of the dashboard can be added here.



👨‍💻 Author



Tanveer Zafar Shaikh



Data Analytics | Power BI | SQL | Python | Web Development

