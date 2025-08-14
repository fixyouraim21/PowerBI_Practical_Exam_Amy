# PowerBI_Practical_Exam_Amy
# Power BI Exam Project

## Project Approach
This project was structured around building a **star schema** with Sales as the fact table and Customers, Products, Dates, and Geography as dimension tables. Data cleaning and transformation were performed in **Power Query**, including the creation of calculated columns for Profit and Sales Category, and proper Date hierarchies for time intelligence. Key **DAX measures** such as Total Sales, Year-over-Year Growth, Running Total Sales, and Top N product filters were developed and applied across multiple report pages. The report includes interactive visualizations: a Sales Overview page for trends, a Product Overview page for product performance, and a Customer Insights page for key customer evaluation. **Bookmarks, slicers, and filters** were used to enhance interactivity, and **Row-Level Security (RLS)** was implemented to restrict data access based on user roles.

## Challenges and Solutions
Handling inconsistencies in the Date and Fiscal Year columns was a major challenge; months were labeled as “2017 Jul” while fiscal years were “FY 2018,” which initially caused sorting and time-based calculations to fail. This was resolved by splitting the month column, creating a “true year” column, and building proper Date hierarchies. Small categories in pie charts were initially hidden or grouped into “Other,” which was addressed by adjusting the small-slice threshold and enabling data labels. Conditional formatting in tables required the creation of dedicated DAX measures to handle Top N filters dynamically, ensuring that formatting remained consistent even when data was filtered.

## Assumptions and Limitations
- Forecasts and trend lines assume a **linear trend** and do not account for seasonality or external factors.  
- Top N product and customer analyses prioritize **Total Sales** as the ranking metric.  
- RLS filters are static based on pre-defined roles; dynamic user-specific filtering was not implemented.  
- Very small categories in charts may still appear visually minor despite enabling all slices due to limited chart space.

## Power Query Images
![Screenshot 29](screenshots/Screenshot%20%2829%29.png)
![Screenshot 30](screenshots/Screenshot%20%2830%29.png)
![Screenshot 31](screenshots/Screenshot%20%2831%29.png)
![Screenshot 32](screenshots/Screenshot%20%2832%29.png)
![Screenshot 33](screenshots/Screenshot%20%2833%29.png)
![Screenshot 34](screenshots/Screenshot%20%2834%29.png)
![Screenshot 35](screenshots/Screenshot%20%2835%29.png)



