# Business Insights 360

## Project Overview

AtliQ Hardware a rapidly growing company in recent years, has decided to implement data analytics using PowerBi in their company for the first time to surpass their competitors  in the market and to make data-driven decisions. This project aims to answer stakeholder questions regarding aspects like finance, sales, marketing, and supply  chain.

I worked on this project by following the Codebasics PowerBi Course, Link to the course is [here](https://codebasics.io/)

[Live Report Link](https://app.powerbi.com/view?r=eyJrIjoiMmNjMDVhYmEtMmEwYS00OTk4LWE2ZTMtZDBiZWJkZGJkNTFkIiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9&pageName=ReportSectiond3171d78e1b90ae50a2e)

## Tech stacks

- SQL
- PowerBi Desktop
- Excel
- DAX language
- DAX studio (for optimizing the report)
- Project charter file

## PowerBI techniques Learnt

- Questions that should be asked before staring the project
- Creating calculated columns
- creating measure using DAX language
- Data modeling
- Using Bookmarks to switch between two visuals
- Page navigation with buttons
- Using divide function to prevent zero division errors
- creating date table using m language
- Dynamic titles based on the applied filters
- Using KPI indicators
- Conditional formatting of the values in visuals using icons or background color
- Data validation techniques
- PowerBi services
- Publishing reports to PowerBi services
- Setting up a personal gateway to set up the auto-refresh of data
- PowerBi App creation
- Collaboration, workspace, and access permissions in PowerBi services

## Business related terms

- Gross price
- Pre-invoice deductions
- Post-Invoice deductions
- Net Invoice sale
- Gross Margin
- Net sales
- Net profit
- COGC - cost of goods sold
- YTD - Year to Date
- YTG - Year to Go
- LY  - Last Year
- BM  - Bench Mark
- Direct
- Retailer
- Distributors
- Consumer

## Company’s background

AtliQ Hardware, a prominent player in the computer and accessories market, serves customers through retailers and direct distributors worldwide. Recent setbacks in their American store, attributed to decisions based on surveys, intuition, and limited Excel analysis, have underscored the need for a dedicated analytics team. This team will be pivotal in steering the company toward data-driven insights and decisions.

### Dataset **Understanding.**

Understanding what data is available will be more helpful before jumping into analysis. 

Dimension table: It will have static data like details of customers and products

Fact table: It will have the data about the transactions  

- gdb041:
    - dim_customer
        - **27** distinct markets (ex India, USA, Spain)
        - **75** distinct customers throughout the market
        - **2** types of platforms
            - Brick & Motors - Physical/offline store
            - E-commerce - Online Store (Amazon, Flipkart)
        - Three channels
            - Retailer
            - Direct
            - Distributors
    - dim_market
        - **27** distinct markets (ex India, USA, Spain)
        - 7 sub-zones
        - 4 regions
            - APAC
            - EU
            - nan
            - LATAM
    - dim_product
        - Divisions
            - P & A
                - Peripherals
                - Accessories
            - PC
                - Notebook
                - Desktop
            - N & S
                - Networking
                - Storage
        - There are 14 different categories, Like Internal HDD, keyboard
        - There are different variants available for the same product
    - fact_forecast_monthly
        - This table is used to forecast the customer’s needs in advance, which can help in
            - Higher customer satisfaction
            - Reduced cost in warehouses for storage purposes
        - The table is denormalized by the data engineering team, as it is a data warehouse that is aimed to be used for analytical work.
        - All the dates of the month will be replaced by the start date of the month
        - It will have all the column names and in the end, it will have the forecast quantity needed by the customer
    - fact_sales_monthly
        - This table is more or less the same as the fact_forecase_monthly table, but the last column has the value of the sold quantity instead of the forecast value.
- gdb056
    - freight_cost
        - This table has details of travel cost and other cost for each market with fiscal year
    - gross_price
        - Has the details of gross prices with product code
    - manufacturing_cost
        - Has the details of manufacturing cost with product code with year
    - Pre_invoice_dedutions
        - Has the details of pre-invoice deductions percentage for each customer with year
    - Post_invoice_deductions
        - Post invoice deductions and other deduction details

## Importing data into PowerBi

- In this project, the datasets are imported from Mysql database to PowerBi by providing the Database access credential

## Data Model

- Data modeling plays a vital role and is considered as the basement of the report. All the visuals will be built upon the data model.
- Poor data modeling affects the overall performance of the report.
- In this project, we have followed the Snowfall data modeling method.
<img src="https://github.com/femyrose/Business-Insights-360/blob/main/Data%20Model%20-%20bi30.png" class="center">

## Dashboard designing

### Home Page

On the Home Page, all the views button will be available. The user will be followed to the corresponding page by clicking the button 

- Info
- Finance View
- Sales View
- Marketing View
- Supply chain View
- Executive View
- Products
- Support

<img src="https://github.com/femyrose/Business-Insights-360/blob/main/Homepage-bi360.png" class="center">

### Finance View

<img src="https://github.com/femyrose/Business-Insights-360/blob/main/finance_view-bi360.png" class="center">

### Sales View

<img src="https://github.com/femyrose/Business-Insights-360/blob/main/Sales%20View-%20bi360.png" class="center">

### Marketing View

<img src="https://github.com/femyrose/Business-Insights-360/blob/main/Marketing%20View%20bi360.png" class="center">

### Supply chain View

<img src="https://github.com/femyrose/Business-Insights-360/blob/main/Supply%20chain%20view%20-bi360.png" class="center">

### Executive View

<img src="https://github.com/femyrose/Business-Insights-360/blob/main/Executive%20View-bi360.png" class="center">


you can find the Live Report here : [Live Report](https://app.powerbi.com/view?r=eyJrIjoiMmNjMDVhYmEtMmEwYS00OTk4LWE2ZTMtZDBiZWJkZGJkNTFkIiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9&pageName=ReportSectiond3171d78e1b90ae50a2e)


## Project Outcome

This report will help in providing insights based on the data to make correct decisions and will further help in answering n number of questions based on the situations.
