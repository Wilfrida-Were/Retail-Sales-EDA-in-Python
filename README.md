# **Retail Sales EDA in Python**

This **[Retail Sales Dataset](https://www.kaggle.com/datasets/mohammadtalib786/retail-sales-dataset/data)** is a snapshot of a fictional retail landscape, capturing essential attributes that drive retail operations and customer interactions. It includes key details such as `Transaction ID`, `Date`, `Customer ID`, `Gender`, `Age`, `Product Category`, `Quantity`, `Price per Unit`, and `Total Amount`. 

Check out the full code in this **[Kaggle Notebook](https://www.kaggle.com/code/wilfridawere/retail-sales-eda-in-python)**

I will limit myself to these three questions:

* Analysis 1: Customer `Age`, `Gender`, and Purchasing Behaviour
* Analysis 2: Top `Product Category` for each `Age` and `Gender`
* Analysis 3: Total Daily and Monthly Spending grouped by `Date`, Number of Customers (`Customer ID`), `Gender`and`Product Category`

# Data Cleaning

The dataset has **1000 rows and 9 columns**

Since this particular dataset has **No Missing values**, I will confirm if there are unexpected values by checking for *unique values* in each column and identifying potential *outliers*

* There are 1000 distinct Transaction IDs and 1000 distinct Customers (Customer ID)s
* Since there are only 345 unique dates, some customers likely made purchases on the same dates
* The Product categories are only *Beauty*, *Clothing* and *Electronics*

# Analysis 1: Customer Age, Gender, and Purchasing Behaviour

# Total spending for each combination of Age and Gender

| Age | Female | Male |
|---|---|---|
| 18 | 7940 | 3275 |
| 19 | 7335 | 7535 |
| 20 | 5175 | 3470 |
| 21 | 5400 | 7185 |
| 22 | 5425 | 8275 |
| 23 | 2895 | 5325 |
| 24 | 1750 | 3665 |
| 25 | 3550 | 6350 |
| 26 | 10375 | 3605 |
| 27 | 4280 | 5105 |
| 28 | 5400 | 3270 |
| 29 | 4000 | 2570 |
| 30 | 6285 | 3505 |
| 31 | 2020 | 8200 |
| 32 | 1850 | 3700 |
| 33 | 2040 | 4200 |
| 34 | 12050 | 4735 |
| 35 | 6815 | 4475 |
| 36 | 3080 | 6025 |
| 37 | 5730 | 5920 |
| 38 | 6020 | 5080 |
| 39 | 3355 | 1240 |
| 40 | 7630 | 1785 |
| 41 | 1195 | 4455 |
| 42 | 5290 | 3210 |
| 43 | 10260 | 7710 |
| 44 | 3590 | 3970 |
| 45 | 585 | 5740 |
| 46 | 5380 | 7710 |
| 47 | 6315 | 6190 |
| 48 | 5410 | 1830 |
| 49 | 2650 | 2460 |
| 50 | 4300 | 5545 |
| 51 | 7270 | 8795 |
| 52 | 4270 | 2770 |
| 53 | 4890 | 4620 |
| 54 | 5755 | 4750 |
| 55 | 7070 | 2710 |
| 56 | 6025 | 3415 |
| 57 | 3630 | 5660 |
| 58 | 3680 | 3715 |
| 59 | 3785 | 5685 |
| 60 | 7660 | 3930 |
| 61 | 2840 | 3890 |
| 62 | 3060 | 5060 |
| 63 | 1205 | 8045 |
| 64 | 6325 | 2800 |

# Insights from Analysis 1

Analysis 1 shows how **Total spending** varies with `Age` and `Gender`

For example: For 18 year olds, Females collectively spent **more** than Males. The opposite is shown for 22 year olds, and so on. 

See the Barplot below

# Barplot of Total Spending by Age and Gender

![Alt text](./Barplot%20of%20Total%20Spending%20by%20Age%20and%20Gender.png)

# Analysis 2: Top Product Categories for each Age and Gender

The table shows from **Age 18 - Age 25**, and **Age 56 - Age 64**. See the **FULL** output **[Here](https://www.kaggle.com/code/wilfridawere/retail-sales-eda-in-python)**

| Age | Product Category | Female | Male |
|---|---|---|---|
| 18 | Beauty            | 3195.0 | 1765.0 |
|   | Clothing          | 2575.0 | 1510.0 |
|   | Electronics       | 2170.0 | NaN |
| 19 | Beauty            | 2225.0 | 2140.0 |
|   | Clothing          | 1200.0 | 1530.0 |
|   | Electronics       | 3910.0 | 3865.0 |
| 20 | Beauty             | 365.0 | 2160.0 |
|   | Clothing            | 80.0  | 360.0 |
|   | Electronics       | 4730.0 | 950.0 |
| 21 | Beauty            | 3300.0 | 4700.0 |
|   | Clothing          | 1200.0 | 1885.0 |
|   | Electronics        | 900.0  | 600.0 |
| 22 | Beauty            | 1300.0 | 4230.0 |
|   | Clothing          | 3275.0 | 2075.0 |
|   | Electronics        | 850.0  | 1970.0 |
| 23 | Beauty             | 475.0  | 165.0  |
|   | Clothing          | 1270.0 | 3050.0 |
|   | Electronics       | 1150.0 | 2110.0 |
| 24 | Beauty            | 1575.0 | 1310.0 |
|   | Clothing            | 25.0   | 2125.0 |
|   | Electronics        | 150.0  | 230.0  |
| 25 | Beauty            | 1000.0 | 1375.0 |
|   | Clothing          | 2200.0 | 2150.0 |
|   | Electronics        | 350.0  | 2825.0 |
| 56 | Beauty            | 1635.0 | 500.0 |
|   | Clothing          | 1790.0 | 2100.0 |
|   | Electronics       | 2600.0 | 815.0 |
| 57 | Beauty             | 425.0  | 3200.0 |
|   | Clothing          | 2895.0 | 750.0 |
|   | Electronics        | 310.0  | 1710.0 |
| 58 | Beauty            | 2800.0 | 990.0 |
|   | Clothing           | 760.0  | 1525.0 |
|   | Electronics        | 120.0  | 1200.0 |
| 59 | Beauty            | 2700.0 | NaN     |
|   | Clothing           | 525.0  | 3585.0 |
|   | Electronics        | 560.0  | 2100.0 |
| 60 | Beauty             | 490.0  | 80.0  |
|   | Clothing          | 3250.0 | 750.0 |
|   | Electronics       | 3920.0 | 3100.0 |
| 61 | Beauty               | NaN  | 1340.0 |
|   | Clothing          | 2240.0 | 250.0 |
|   | Electronics        | 600.0  | 2300.0 |
| 62 | Beauty             | 920.0  | 305.0 |
|   | Clothing           | 440.0  | 175.0 |
|   | Electronics       | 1700.0 | 4580.0 |
| 63 | Beauty             | 105.0  | 50.0  |
|   | Clothing           | 150.0  | 2320.0 |
|   | Electronics        | 950.0  | 5675.0 |
| 64 | Beauty             | 640.0  | 1690.0 |
|   | Clothing          | 4735.0 | 820.0 |
|   | Electronics        | 950.0  | 290.0 |

# Insights from Analysis 2

Analysis 2 helps to identify **Trends in Customer Spending behaviour** based on `Age`, `Gender`, and `Product Category`

The insights:

* Age Preferences: Spending habits change with Age for certain Product Categories
* Gender Differences: There are significant differences in spending patterns between Genders for specific Product Categories

For a larger Real-life dataset, using such analysis can help to refine the **Target Audience for Marketing Campaigns**. Specific Age groups and Genders have a higher propensity to spend on certain Product Categories

# Analysis 3: Total Daily and Monthly Spending

The Total Daily and Monthly Spending are grouped by the ***Most bought Product Category***, ***Number of Customers*** and ***Gender***

# Total Daily Spending

**Uncomment** the **[Code](https://www.kaggle.com/code/wilfridawere/retail-sales-eda-in-python)** to get the Total Daily Spending. The output consists of **345 different Dates**

# Total Monthly Spending

| Month | Most Bought Product Category | Number of Customers | Male Customers | Female Customers | Total Spending |
|---|---|---|---|---|---|
| 1 | Beauty | 78 | 38 | 40 | 36980.00 |
| 2 | Clothing | 85 | 49 | 36 | 44060.00 |
| 3 | Clothing | 73 | 32 | 41 | 28990.00 |
| 4 | Clothing | 86 | 36 | 50 | 33870.00 |
| 5 | Electronics | 105 | 60 | 45 | 53150.00 |
| 6 | Clothing | 77 | 38 | 39 | 36715.00 |
| 7 | Beauty | 72 | 35 | 37 | 35465.00 |
| 8 | Electronics | 94 | 44 | 50 | 36960.00 |
| 9 | Electronics | 65 | 30 | 35 | 23620.00 |
| 10 | Electronics | 96 | 53 | 43 | 46580.00 |
| 11 | Electronics | 78 | 39 | 39 | 34920.00 |
| 12 | Electronics | 91 | 36 | 55 | 44690.00 |

# Insights from Analysis 3 

Analysis 3 examins **Customer Spending Trends throughout the Year**, segmented by **Month**. I look at:

* Most Popular Product Category: The Product Category with the highest total spending in each month.
* Number of Customers: The total number of unique customers who made purchases each month.
* Gender Distribution: The breakdown of customers by Gender (Male and Female) for each month.
* Total Spending: The total amount of money spent by all Customers each month.
* 
The Findings:

1. Spending Fluctuations: There are variations in total spending throughout the year, with some months seeing higher spending than others (e.g., May had the highest spending at 53,150).
2. Category Preferences: The most popular Product Category shifts across months. For instance, *Beauty* was popular in January and July, while *Electronics* dominated in several months (May, and August-December).
3. Customer Trends: The number of customers also fluctuates, with May showing the highest number (105) and September showing the lowest (65). 
4. Gender difference: There are slighlty more Female customers each month than Male

**Actionable Insights**

Once again, in a Real-life dataset the findings can help with:

* Promotions and Marketing: Understanding popular categories by month can help tailor promotions and marketing campaigns to target the right products at the right time.
* Inventory Management: Analyzing monthly sales trends can inform inventory management strategies, ensuring you have adequate stock of popular categories during peak demand months.
* Customer Acquisition: Months with lower customer traffic might be good times to implement customer acquisition campaigns to attract new buyers.

# Total Monthly Spending Trend by Gender

This table shows the total spending by Male and Female customers for each Month.

| Month | Male Spending | Female Spending |
|---|---|---|
| 1 | 12255.00 | 24725.00 |
| 2 | 29665.00 | 14395.00 |
| 3 | 15670.00 | 13320.00 |
| 4 | 16570.00 | 17300.00 |
| 5 | 29220.00 | 23930.00 |
| 6 | 19840.00 | 16875.00 |
| 7 | 18580.00 | 16885.00 |
| 8 | 14880.00 | 22080.00 |
| 9 | 7085.00 | 16535.00 |
| 10 | 19980.00 | 26600.00 |
| 11 | 20030.00 | 14890.00 |
| 12 | 19385.00 | 25305.00 |

Using the table and lineplot, we can visually compare **Spending patterns between Genders throughout the year.**

Spending fluctuates for each Gender throughout the year

For instance, in **May**, *Male* spending is the highest at 29220.00, while *Female* spending is the highest in **October** at 26600.00.

![Alt text](./Lineplot%20of%20Total%20Monthly%20Spending%20Trend%20by%20Gender.png)

I will use this same dataset to perform *Retail Sales EDA in SQL*

Feel free to do more analyses. Contact me for any changes and feedback

***Explore and be teachable***
