# **Bank-Customer-Churn-Analysis**
 This analysis examines customer churn at NADEX Bank
 ***
 
<img width="1500" height="654" alt="image" src="https://github.com/user-attachments/assets/d109f435-05a4-4ab2-871f-98d534ad520e" />

***

## INTRODUCTION

In today's highly competitive banking environment, customer retention is critical to long-term profitability. NADEX Bank has recently experienced a noticeable rise in customer churn, with over 2,000 customers exiting the bank. This project aims to analyze the bank's customer data to uncover key patterns and drivers behind the churn. Using a dashboard-based approach, the analysis focuses on customer demographics, product usage, tenure, account balance, and geography to identify high-risk segments and provide actionable insights. The goal is to support data-driven strategies that will help reduce churn and improve customer loyalty.
***

## Problem Statement

NADEX Bank is currently experiencing a significant customer churn rate of 20.38%, with 2,037 out of 9,997 customers exiting the bank. Preliminary analysis shows that churn is especially high among middle-aged customers (35–54 years), single-product holders, and those with 3–6 years of tenure.
This trend poses a risk to the bank's revenue, customer lifetime value, and market competitiveness. Without identifying the root causes and at-risk customer segments, NADEX may continue to lose valuable customers, impacting long-term growth and profitability.
***

## Project Objectives
1. Determine the overall churn rate and assess the scale of customer loss at NADEX Bank.
2. Identify customer segments most at risk of churning based on demographic and behavioral patterns (e.g., age, tenure, product usage, balance).
3. Analyze differences between churned and retained customers to understand key churn drivers.
4. Visualize insights using a dashboard for clear, data-driven storytelling.
5. Support the development of targeted retention strategies to reduce churn and improve customer loyalty.
6. 
### Tools Used
· **Microsoft Excel**

 Used for data cleaning, sorting, filtering, and creating pivot tables.
 
· **Excel Charts & Dashboarding**

 Used to build interactive visuals such as bar charts, pie/doughnut charts, and KPI cards to represent churn insights.
 
· **Data Analysis Techniques**

 Basic descriptive analysis (count, percentage, grouping) was applied to explore customer attributes and behavior.
 ***
 ## DATA DESCRIPTION
 
The original dataset consisted of 10,000 customer records from NADEX Bank. During the data cleaning phase, 3 records were identified as errors, as they contained incomplete or inconsistent information that could not be analyzed. These records were removed, resulting in a final working dataset of 9,997 customers.
### **Key Features in the Dataset:**

· Customer ID - Unique identifier for each customer

· Gender - Male or Female

· Age - Numeric value, grouped for analysis

· Geography - France, Germany, Spain

· Tenure - Number of years the customer has been with the bank

· Balance - Account balance.

· Number of Products - Total products/services held

· Churn Status - Indicates if the customer has exited or remained

· Estimated Salary - May support financial behavior analysis

### **Data Quality Note:**

· 3 invalid records were removed due to data entry errors (No customer name, no Age and the estimated salary is negative values across fields).

· The final dataset used for the dashboard contains 9,997 clean and analyzable customer records.
***

## DATA CLEANING PROCESS
1. ### **Handling Incomplete and Invalid Data**
· Started by sorting the dataset to easily locate and remove incomplete records.

· Deleted rows with missing names and missing salary values.

· Identified and removed 3 corrupted records, reducing the dataset from 10,000 to 9,997 valid entries.

2. ### **Formatting and Standardization**
· Used Excel's PROPER function to align name formatting (e.g., converting all caps/lowercase to proper case).

· Standardized date formats to ensure uniformity across the dataset.

· Replaced special characters (e.g., removed "€" from the Balance field) and corrected geography entries (e.g., changed "FRA" or "French" to "France") using Find and Replace.

3. ### **Handling Special Characters**
· Replaced names containing "?" with "I", using the Find and Replace feature:

o Find: ~? → Replace with: I
 (Note: the tilde ~ tells Excel to treat ? as a literal character, not a wildcard)

4. ### **Duplicate and Consistency Checks**
· Used the Data ribbon to identify and remove duplicate records.

· Verified all fields to ensure data type consistency (e.g., numeric values in Balance, text values in Geography).

· Confirmed that categorical variables were standardized and cleaned.

5. ### **Final Review**
· Performed a thorough final check of the dataset to confirm that all entries were clean, complete, and properly formatted before proceeding to analysis and dashboard creation.

### **Merging:**

The data sets (Customer Info and Account Info) were merged using Excel's `VLOOKUP` function to create a unified dataset analysis.

**New Fields Created:**

To enrich analysis and segment behavior more effectively, several "calculated fields" were introduced:

 - `Cleaned Surname`: Text-normalized for consistency (using" TRIM" to remove unwanted or unseen spaces, "PROPER" to capitalize uniformly)

 - `Estimated Salary Clean` / `Balance`: Parsed to numeric form for ease of calculation
 
 - `Surname Flag`, `Geography Flag`: Flagged anomalies and data quality issues (using conditional formatting.
 
 - `Age Range`, `Balance Range`, `Number Of Products` (Transformed product count into groups).
 
### **Data Categorization and Grouping**
 To enable aggregated analysis and segmentation, key numerical and categorical variables were grouped:
 
Age Grouping: Customers were categorized into 18–24, 25–34, 35–44, 45–54, 55+ using `IF` and nested logic.

Balance Grouping: Ranged from 0–49K, 50K–99K, 100K–149K, 150K–199K, 200K+ based on the `Balance` field. This was critical for identifying churn patterns across financial tiers.

Product Count Grouping: Converted raw counts into `Single', 'Basic`, `Standard`, and `Multiple' for easier interpretation.

These were used to make the raw data more interpretable and helped simplify PivotTable construction.

<img width="940" height="435" alt="image" src="https://github.com/user-attachments/assets/83a6e846-6011-407c-959f-3732f5c51c1f" />

### **Churn Analysis Setup:**
Churn Rate = (COUNTIF(Exited=1) ÷ total customers) *100

Retention Rate = (COUNTIF(Exited=0) ÷ total customers) *100

PivotTables were used to break down churn by Gender, Geography etc.

Slicers and field arrangements enabled dynamic analysis through Rows, Columns, and Values.
***

## **Visualization**
All final visualizations were created within Excel using Pivot Charts, slicers, and formatting tools:

Pivot Charts: Bar and column charts were used to show churn distribution across dimensions.

Chart Titles: Custom titles reflected precise interpretations, e.g., "Churn Distribution by Age Range".

Slicers: Interactive slicers allowed for segmentation by Age Range, Gender, Balance Range and Number of Products.

Color Coding: Used corporate-style themes for professionalism. Churned vs Retained customers had clearly defined color codes.

Dashboard Integration: Final visuals were arranged in a one-page dashboard with linked filters for stakeholder presentations.

<img width="940" height="410" alt="image" src="https://github.com/user-attachments/assets/aeae4470-0588-4007-99f6-c615c48becd5" />
***

## Key Insights
### **High Overall Churn Rate**
Out of 9,997 customers, 2,037 have exited, resulting in a churn rate of 20.38%.

 This suggests that 1 in every 5 customers leaves the bank, which is a substantial loss for a financial institution. A churn rate this high could signal customer dissatisfaction, strong competition, or a gap in engagement strategies.
 
### **Middle-Aged Customers Are the Most Likely to Churn**
The 35–44 and 45–54 age groups recorded the highest number of churned customers 703 and 702 respectively.

 Interestingly, these groups also represent a large part of the active customer base, which could suggest they are either more demanding, more aware of alternatives, or not seeing continued value from NADEX Bank.

 <img width="628" height="347" alt="image" src="https://github.com/user-attachments/assets/2a9194c7-3df1-4a87-8d22-46432c45da14" />

### **Single-Product Holders Drive Most of the Churn**
Customers with only one product account for more than 65% of all churned customers.

 In contrast, churn is lower among customers with multiple products. This highlights a strong correlation between product engagement and loyalty the more products a customer holds, the less likely they are to leave. However, it's important to note that retention is strongest among dual-product users, with 4,242 retained customers the highest across all categories.
 
 This trend suggests a strong correlation between product usage depth and loyalty: the more products a customer uses, the less likely they are to leave, and the more likely they are to remain engaged with the bank.

 <img width="851" height="347" alt="image" src="https://github.com/user-attachments/assets/0134739d-5752-4a5d-8e0c-0ef96ce6a81b" />

### **3–6 Years Tenure Customers Are at Greatest Risk**
Customers with 3–6 years of tenure churn the most 821 out of 2,037 churned customers.

 This suggests a mid-lifecycle satisfaction drop, possibly due to unaddressed needs, lack of ongoing engagement, or the absence of loyalty incentives.

 <img width="860" height="345" alt="image" src="https://github.com/user-attachments/assets/1577878b-19d0-4dad-98b2-ba326f11be14" />

### **Churn Distribution by Geography Shows Regional Gaps**
· Germany: 814 churned

· France: 810 churned

· Spain: 413 churned

France and Germany show nearly equal and significantly higher churn than Spain. This may be due to regional service differences, marketing strategy effectiveness, or even external competition.

<img width="624" height="343" alt="image" src="https://github.com/user-attachments/assets/5058549f-8ef0-49e3-b7c1-b1e31bdd2353" />
***

## Recommendations
To reduce churn and improve customer retention at NADEX Bank, it is recommended to implement a targeted, data-driven retention strategy that focuses on the most at-risk segments including middle-aged customers (35–54 years), single-product users, and those with 3–6 years of tenure.

 **This strategy should include:**
 
Cross-selling and product bundling to increase engagement,

Mid-tenure re-engagement programs such as loyalty rewards and account reviews,

Personalized communication and offers based on demographics and balance levels,

And region-specific customer experience improvements, particularly in France and Germany.


Additionally, the bank should invest in improved data collection including behavioral and satisfaction metrics and develop a predictive churn model to proactively identify and retain at-risk customers before they exit.
***
## Conclusion
This customer churn analysis has revealed critical insights into the behavior of NADEX Bank's exiting customers. With a churn rate of 20.38%, the bank is losing a significant portion of its customer base, especially among middle-aged, single-product, and mid-tenure customers. Additionally, regional churn patterns show that France and Germany require targeted attention.

By identifying these key risk segments, the analysis provides a foundation for data-driven decision-making. While the current data offers valuable insights, enhancing it with behavioral, transactional, and satisfaction data will allow for deeper analysis and predictive modelling.

Implementing the recommended strategies including personalized retention efforts, product bundling, regional engagement, and data enhancement will enable NADEX Bank to reduce churn, strengthen customer loyalty, and protect long-term revenue.
