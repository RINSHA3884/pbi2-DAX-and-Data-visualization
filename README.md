# Power BI Assignment 2

## Overview
This assignment focuses on data analysis and visualization using Microsoft Power BI. Different datasets were used to create charts, analyze business information, and perform calculations using DAX.

## Tasks Completed

### 1. Country-wise Order Analysis
- Imported the AmazingCart Excel dataset into Power BI Desktop.
- Created a clustered column chart to compare the number of orders across countries.
- Used Country on the X-axis and Count of Order ID on the Y-axis to identify countries with the highest order placement.

### 2. Daily Order Analysis
- Used the Customer Data dataset to create a line chart.
- Displayed the number of orders received per day using the Date field and order count.
- Analyzed daily order patterns over time.

### 3. Employee Layoff Analysis
- Imported the Employee Layoff Excel dataset.
- Created a pie chart to compare total layoffs by location.
- Used Location as the legend and Sum of Total Laid Off as the values.
- Identified locations with higher numbers of layoffs.

### 4. Calculated Column Using DAX
- Created a new calculated column in the Customer Data table.
- Multiplied product quantity by price per unit to calculate the total price.

Example DAX formula:

```dax
Calculated Total Price =
'Customer Data'[Quantity] *
'Customer Data'[Price per unit]
```

### 5. DAX Measures
Created measures to perform calculations and analyze the Customer Data table.

**Total Quantity**
```dax
Total Quantity =
SUM('Customer Data'[Quantity])
```

**Total Rows**
```dax
Total Rows =
COUNTROWS('Customer Data')
```

**Valid Records**
```dax
Valid Records =
COUNTA('Customer Data'[Order ID])
```

**Missing Values**
```dax
Missing Values =
COUNTROWS(
    FILTER(
        'Customer Data',
        ISBLANK('Customer Data'[Order ID])
    )
)
```

**Minimum Price**
```dax
Minimum Price =
MIN('Customer Data'[Price per unit])
```

**Maximum Price**
```dax
Maximum Price =
MAX('Customer Data'[Price per unit])
```

The Missing Values measure counts blank Order IDs, while Valid Records counts nonblank Order IDs.

## Tools and Technologies
- Microsoft Power BI Desktop
- Power Query Editor
- DAX (Data Analysis Expressions)
- Microsoft Excel
- GitHub
- Google Drive

## Conclusion
This assignment provided practical experience in importing datasets, creating visualizations, developing calculated columns, and writing DAX measures. It helped strengthen data preparation, visualization, and analytical skills using Power BI.

## Assignment File
The Power BI report file (`.pbix`) contains the completed report and can be opened using Microsoft Power BI Desktop.
# pbi2-DAX-and-Data-visualization
