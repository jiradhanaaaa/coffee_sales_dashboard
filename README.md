# Coffee Sales Data Analysis

## Project Overview
![prev](https://github.com/user-attachments/assets/546bd988-bf6f-4ef2-ae70-bd3e2255f8d4)
This project is a comprehensive analysis of coffee sales data using Excel, focusing on data cleaning, analysis, and visualization. The dataset, sourced from Mo Chen's GitHub, contains 1,000 columns of uncleaned data across three interconnected sheets. Following Mo Chen's tutorial, with adding new insights in it, I developed an interactive dashboard to provide actionable insights into coffee sales trends.

The final dashboard includes:
- Filters for dynamic data exploration.
- Charts to visualize revenue and sales by country.
- Slicers for detailed analysis by roast type, coffee type, size, and loyalty card usage.

## Objectives
- Clean and structure raw coffee sales data.
- Extract insights using advanced Excel formulas and tools.
- Create an interactive, user-friendly dashboard for better data understanding.

## Techniques Used

### 1. Data Acquisition
- Dataset sourced from [Mo Chen's GitHub](https://github.com).

### 2. Data Preparation
- Removed unnecessary tables and columns.
- Reorganized rows and columns for better readability and usability.
- Added appropriate units to data entries for clarity.

### 3. Data Cleaning
- Addressed inconsistencies, missing values, and formatting issues.
- Automated the cleaning process using Excel tools and formulas.

### 4. Analysis Techniques
#### **XLOOKUP Formula**
- Used to retrieve specific data points from different datasets dynamically.
- **Used on:** Retrieve total revenue for specific coffee types or regions.
- **Benefits:** Simplifies data retrieval compared to traditional VLOOKUP
- **Example:** ```excel
  =XLOOKUP(C6,customers!$A$1:$A$1001,customers!B5:B1005,,0)

#### **INDEX Formula**
- Combined with other functions like MATCH for flexible data extraction.
- **Used on:** Locate sales figures based on selected rows (e.g., month) and columns (e.g., coffee size).
- **Benefits:** Enables precise control over data retrieval.
- **Example:** ``` excel
  =INDEX(products!$A$1:$G$49,MATCH(orders!$D7,products!$A$1:$A$49,0),MATCH(orders!L$1,products!$A$1:$G$1,0))

#### **IF Formula**
- Applied for conditional categorization.
- **Used on:** Changing the shortened words when cleaning the data.
- **Example:** ```excel
 =IF(J14="M","Medium",IF(J14="L","Light",IF(J14="D","Dark","")))
 

#### **Combining Formulas : XLOOKUP and IF**
- Used for conditional lookups and dynamic data retrieval.
- **Example:** Retrieve revenue for specific coffee types only if the region exceeds a revenue threshold.
  ```excel
  =IF(XLOOKUP(C12,customers!$A$1:$A$1001,customers!$C11:$C1011,,0)=0,"",XLOOKUP(C12,customers!$A$1:$A$1001,customers!$C11:$C1011,,0))


#### **PivotTables and PivotCharts**
- Summarized trends, revenue distribution, and performance by regions, coffee types, and sizes.
- Visualized data trends and patterns effectively.

#### **Slicers**
- Enhanced interactivity, enabling users to filter data dynamically by date, roast type, coffee size, and loyalty card usage.

## Key Insights
- **Seasonal Trends:** Coffee sales peak during winter and holiday seasons.
- **Top Products:** Arabica and Excelsa coffee types generate the highest revenue.
- **Regional Performance:** The Unit

## Acknowledgement 
- Data and tutorial by Mo Chen on [Youtube](https://www.youtube.com/watch?v=m13o5aqeCbM).

