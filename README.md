# PowerBI_Practical_Exam_Amy

## Project Approach
This project was structured around building a **star schema** with Sales as the fact table and Customers, Products, Dates, and Geography as dimension tables. Data cleaning and transformation were performed in **Power Query**, including the creation of calculated columns for Profit and Sales Category, and proper Date hierarchies for time intelligence. Key **DAX measures** such as Total Sales, Year-over-Year Growth, Running Total Sales, and Top N product filters were developed and applied across multiple report pages. The report includes interactive visualizations: a Sales Overview page for trends, a Product Overview page for product performance, and a Customer Insights page for key customer evaluation. **Bookmarks, slicers, and filters** were used to enhance interactivity, and **Row-Level Security (RLS)** was implemented to restrict data access based on user roles.

--- 

## Challenges and Solutions
Handling inconsistencies in the Date and Fiscal Year columns was a major challenge; months were labeled as “2017 Jul” while fiscal years were “FY 2018,” which initially caused sorting and time-based calculations to fail. This was resolved by splitting the month column, creating a “true year” column, and building proper Date hierarchies. Small categories in pie charts were initially hidden or grouped into “Other,” which was addressed by adjusting the small-slice threshold and enabling data labels. Conditional formatting in tables required the creation of dedicated DAX measures to handle Top N filters dynamically, ensuring that formatting remained consistent even when data was filtered.

---

## Assumptions and Limitations
- Forecasts and trend lines assume a **linear trend** and do not account for seasonality or external factors.  
- Top N product and customer analyses prioritize **Total Sales** as the ranking metric.  
- RLS filters are static based on pre-defined roles; dynamic user-specific filtering was not implemented.  
- Very small categories in charts may still appear visually minor despite enabling all slices due to limited chart space.

---

## Custom DAX Measures

Below are the custom DAX measures created during the project, along with their purpose and how they were used in visuals.



### 1. **Year-over-Year Growth (%)**
**Purpose:**  
Calculates the percentage growth in sales compared to the same period in the previous year. This helps identify business performance trends over time.

**Usage in Visuals:**  
- **Sales Overview Page:** Added to a **Line Chart** alongside Total Sales to visualize growth trends.  
- Plotted with a **secondary Y-axis** to compare growth percentage and total sales in the same visual.



### 2. **Running Total Sales**
**Purpose:**  
Generates a cumulative total of sales up to the selected date in the filter context, making it easy to track year-to-date progress and performance pacing.

**Usage in Visuals:**  
- **Sales Overview Page:** Displayed in a **Line Chart** to show cumulative sales growth over time.  
- Helps identify seasonal trends and progress toward targets.



### 3. **Top 5 Products by Sales (Dynamic)**
**Purpose:**  
Ranks products by sales and dynamically filters to include only the top 5, making it simple to focus on best performers without manually adjusting filters.

**Usage in Visuals:**  
- **Product Analysis Page:** Displayed in a **Bar Chart** to highlight top 5 products by sales.  
- Used to compare changes in product performance rankings over time.



**Formatting Notes:**  
- All percentage-based measures (e.g., Year-over-Year Growth) are formatted as **Percentage** in the Modeling tab.  
- Forecast visuals assume a **linear trend** unless otherwise specified.

--- 

## Power Query Images
![Screenshot 29](screenshots/Screenshot%20%2829%29.png)
![Screenshot 30](screenshots/Screenshot%20%2830%29.png)
![Screenshot 31](screenshots/Screenshot%20%2831%29.png)
![Screenshot 32](screenshots/Screenshot%20%2832%29.png)
![Screenshot 33](screenshots/Screenshot%20%2833%29.png)
![Screenshot 34](screenshots/Screenshot%20%2834%29.png)
![Screenshot 35](screenshots/Screenshot%20%2835%29.png)

## Data Model
![Data Model](screenshots/data%20model.png)

## Visualisation Images
![Screenshot 36](screenshots/Screenshot%20(36).png)
![Screenshot 37](screenshots/Screenshot%20(37).png)
![Screenshot 38](screenshots/Screenshot%20(38).png)
![Screenshot 39](screenshots/Screenshot%20(39).png)
![Screenshot 40](screenshots/Screenshot%20(40).png)
![Screenshot 41](screenshots/Screenshot%20(41).png)
![Screenshot 42](screenshots/Screenshot%20(42).png)
![Screenshot 43](screenshots/Screenshot%20(43).png)
![Screenshot 44](screenshots/Screenshot%20(44).png)

## Report Images
![Screenshot 45](screenshots/Screenshot%20(45).png)
![Screenshot 46](screenshots/Screenshot%20(46).png)
![Screenshot 47](screenshots/Screenshot%20(47).png)

## RLS Images
![Screenshot 48](screenshots/Screenshot%20(48).png)  
![Screenshot 49](screenshots/Screenshot%20(49).png)  

