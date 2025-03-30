# Blinkit Analysis

### Dashboard Link :https://drive.google.com/file/d/1N0FC9f5G08ZhVKmPiul0St4VGuBj33lK/view?usp=drive_link
## Problem Statement

Blinkit, a leading online grocery delivery service, seeks to optimize its sales performance, customer satisfaction, and inventory distribution. The company faces challenges in understanding key sales trends, customer preferences, and the impact of various product attributes on overall revenue.

Assess Sales Performance – Identify total sales, average revenue per sale, and the number of items sold.

Evaluate Customer Satisfaction – Analyze average customer ratings for different products.

Optimize Inventory Distribution – Understand how factors like fat content, outlet type, and location influence sales.

Improve Business Strategy – Visualize trends using charts such as donut charts, bar charts, stacked column charts, line charts, and funnel maps to make informed decisions on product offerings and marketing strategies.


### Steps followed 

Step 1: Load Data into Power BI Desktop

    1️⃣ The dataset is provided in CSV/Excel format and    loaded into Power BI.
Step 2: Open Power Query Editor

    1️⃣ In the View tab under the Data Preview section, check "Column Distribution", "Column Quality", and "Column Profile" options.

    2️⃣Ensure "Column Profiling Based on Entire Dataset" is selected for a complete data overview.
Step 3: Handle Missing & Incorrect Data

    1️⃣ Data was checked for missing values and inconsistencies.

    2️⃣"Item Fat Content" contained inconsistencies like variations in labels (e.g., "Low Fat", "low fat"), which were standardized.

    3️⃣Null values in "Item Visibility" were replaced with the average value of the column.
Step 4: Apply Data Transformations

    1️⃣ Data Type Correction: Ensured numerical, categorical, and date fields were in correct formats.

2)New Columns Created:

    1️⃣ "Total Sales" = Quantity * Item Price

    2️⃣"Profit Margin" based on estimated cost-price ratios.
Step 5: Select Report Theme

    1️⃣ In the Report View, under the View Tab, a custom theme was applied for better visualization.
Step 6: Add Key Visuals for Insights

    KPIs and Measures Created:

    ✅ Total Sales - Aggregated revenue calculation using DAX.
    ✅ Average Sales per Transaction - Measure created using AVERAGE DAX function.
    ✅ Number of Items Sold - Using COUNT function.
    ✅ Customer Satisfaction Rating - Based on average rating values.

Visualizations Added:

    📊 Total Sales by Fat Content – Donut Chart
    📊 Total Sales by Item Type – Bar Chart
    📊 Fat Content by Outlet Type – Stacked Column Chart
    📊 Sales by Outlet Establishment Year – Line Chart
    📊 Sales by Outlet Size – Pie Chart
    📊 Sales by Outlet Location – Funnel Map
    📊 All Metrics by Outlet Type – Matrix Card

Slicers Added for Interactivity:

    "Item Type", "Outlet Type", "Outlet Location", and "Fat Content" slicers were implemented to filter data dynamically.
Step 7: DAX Calculations for Metrics

    1️⃣ Total Sales Calculation:

    Total Sales = SUM(BlinkitData[Sales])

    2️⃣ Average Sales Per Product:

    Avg Sales = AVERAGE(BlinkitData[Sales])

    3️⃣ Profit Margin Calculation:

    Profit Margin = SUM(BlinkitData[Profit]) / SUM(BlinkitData[Sales])


Step 8: Add Branding & Aesthetic Enhancements

    1️⃣Inserted Company Logo & Name on the report canvas.

    2️⃣Added Background Image for better UI appeal.

    3️⃣Used Shapes & Textboxes for additional labels.


        
- Step 9 : New measure was created to find: 

    Total Sales.

    Average Sales.

    No Of Items.

    Avearge Rating.

Following DAX expression was written for the same,
        
       Total Sales = SUM('BlinkIT Grocery Data'[Sales])

       Avg Sales = AVERAGE('BlinkIT Grocery Data'[Sales])

       No of Items = COUNTROWS('BlinkIT Grocery Data')

       Avg Rating = AVERAGE('BlinkIT Grocery Data'[Rating])
        


# Insights

Following inferences can be drawn from the dashboard;

### Total Sales = 1.20M 
Tier-1 

    Total sales - 0.34M

        >>Low Fat items sold - 0.22M
        >>Regular - 0.12M

        -->Meduim outlet size
            a)Total sales -0.13M
            b)Avg sales - $140
            c)No of items - 930
            d)Avg rating - 4

        In Tier-1 Meduim outlet highest sold item were snacks foods.


        -->Small oulet size 
            a)Total sales - 0.21M
            2)Avg sales - $141
            3)No of items - 1458
            4)Avg rating - 4
         
        In Tier-1 Small outlet highest sold item were fruits and vegetables. 

Tier-2

    Total sales - 0.39M

        >>Low Fat items sold - 0.25M
        >>Regular - 0.14M

        -->high outlet size
            a)Total sales - 0.08M
            b)Avg sales - $144
            c)No of items - 588
            d)Avg rating - 4

        In Tier-2 high outlet highest sold item were snacks foods.

        -->Meduim outlet size
            a)Total sales -0.08M
            b)Avg sales - $136
            c)No of items - 537
            d)Avg rating - 4
        
        In Tier-2 Meduim outlet highest sold item were fruits and vegetables. 

        -->Small outlet size
            a)Total sales -0.23M
            b)Avg sales - $142
            c)No of items - 1624
            d)Avg rating - 4
        In Tier-2 small outlet highest sold item were household.
Tier-3

    Total sales - 0.47M

        >>Low Fat items sold - 0.30M
        >>Regular - 0.17M

        -->high outlet size
            a)Total sales - 0.16M
            b)Avg sales - $141
            c)No of items - 1165
            d)Avg rating - 4

        In Tier-3 high outlet highest sold item were snacks foods.

        -->Meduim outlet size
            a)Total sales -0.30M
            b)Avg sales - $141
            c)No of items - 2128
            d)Avg rating - 4
        
        In Tier-3 Meduim outlet highest sold item were fruits and vegetables. 

        -->Small outlet size
            a)Total sales -0.1M
            b)Avg sales - $147
            c)No of items - 57
            d)Avg rating - 4
        In Tier-3 small outlet highest sold item were snacks foods.
