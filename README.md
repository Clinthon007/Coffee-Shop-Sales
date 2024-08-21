# Coffee Shop Sales Analysis

## Project Overview

It's a coffee shop chain with three (3) different locations in New York City (Astoria, Hell's Kitchen, and Lower Manhattan). 

To better understand the purchase behaviour and streamline operations through the raw transactional data collected from Jan-Jun 2023 (first half of the year). The goal is to transform the data into dynamic dashboard that the franchise owners can use to identify patterns, trends and opportunities for the business.

---

### Data Source

[Coffee Shop Sales.xlsx](https://github.com/user-attachments/files/16676277/Coffee.Shop.Sales.xlsx)

### Tools Used

- EXCEL

### Data Preparation

Since the data was in good conditions there were no cleaning to be made, rather, the following tasks were carried out;

- Data Loading and inspection in **Excel**
- A new column was added to calculate *"Revenue"* ( price * quantity ).
  
- Another Column was added to calculate _"Month"_ and _"Weekday"_ based on the transaction date column.
  Four (4) columns were created totally. Namely;
  - Month: the **MONTH ()** was used to get each number representing each month ( e.g, Jan was 1, Feb was 2, etc).
  - Month Name: the **TEXT ()** was used to get the shortened name of each month ( e.g, Jan, Feb, Mar, etc).
  - Weekday: the **WEEKDAY ()** was used to get the number representing each month ( e.g, Sun was 7, Sat was 6, etc).
  - Weekday Name:  the **TEXT ()** was used to get the shortened name of each week day ( e.g, Mon, Tue, Wed, etc).
   
_Note_: Both name columns created (Month Name and Weekday Name) were so users could understand what each number stood for. e.g, for weekday, 1 was for Monday, 2 for Tuesday etc. While for month, 1 was for January, 2 for February, etc.
  
- Another Column was added to extract _"Hour"_ from the transaction time column.
   Here, the **HOUR ()** was used to extract the hour from each cell row.

After creating the new fields, their headers were boldened as well as were being effected with unique colouring, seperating them from the rest columns.

![Calculated_fields](https://github.com/user-attachments/assets/4d6b33d4-c6e0-4a96-934e-9d7cbc656bf6)

---
### Exploratory Data Analysis

EDAs were carried out with the use of **Pivot Tables** and **Pivot Charts** to look into the following points;

-  **Revenue** by Month
-  Number of transactions by **Weekday** and by **Hour** of day (two Pivot tables)
-  Number of transactions by **Product Category**
-  Number of transactions and Revenue by **Product type**

    **Slicer** was added finally for the _Store_location_ to connect to the tables created and make it them dynamic in order for users to be able to update themselves with transaction information from the different locations.

---

### Data Analysis

  #### A) For Location in **ASTORIA:**
  
**1. **REVENUE** by Month**

![Monthly_Revenue](https://github.com/user-attachments/assets/8b63bacf-8a4b-493c-a28c-358fd4c42e6f)

**Summary:**

January: The total revenue was $27,313.66. This is the starting point for the year.

February: The revenue decreased to $25,105.34, indicating a slight decline from January.

March: There was a significant increase in revenue, rising to $32,835.43. This marks the beginning of a positive trend.

April: Revenue continued to increase, reaching $39,477.61.

May: The growth trend accelerated, with revenue jumping to $52,428.76.

June: The upward trend continued, with the highest revenue recorded at $55,083.11.

**Overall Trend:**

   - The coffee shop's revenue shows an overall increasing trend from January to June.
   - Despite a dip in February, the revenue consistently increased each month afterward.
   - The steepest growth occurred between March and April, and again between April and May.

 **2.**
 
   **I. Number of transactions by WEEKDAY**

   ![Weekday_transactions](https://github.com/user-attachments/assets/294b9c4c-5821-4c69-9f42-dd08a5ec8c5b)

   - Monday: The transactions are relatively high, with a count of just over 7,400. This is one of the busiest days of the week.

   - Tuesday: There is a noticeable drop in transactions, with the count slightly above 7,000. Tuesday has fewer transactions compared to other weekdays.

   - Wednesday: The number of transactions increases again, reaching around 7,300. This indicates a recovery after the drop on Tuesday.

   - Thursday: This is the peak day for transactions, with the highest count close to 7,500. Thursday is the busiest day of the week.

   - Friday: Transactions are slightly lower than Thursday but still strong, with counts around 7,400.

   - Saturday: There is a significant drop, with transactions falling to around 6,900. This is one of the less busy days of the week.

   - Sunday: The number of transactions increases slightly to about 7,000 but remains lower than most weekdays.

**Overall Trend:**

   - Mid-Week Peak: The coffee shop sees the highest transaction volume in the middle of the week, particularly on Thursday, followed closely by Monday and Friday.

   - Weekend Dip: There is a noticeable decline in transactions on the weekend, particularly on Saturday, which has the lowest number of transactions.

   - Tuesday Drop: Tuesday stands out as a day with fewer transactions compared to Monday and Wednesday.

   **II. Number of Transactions by HOUR**

   ![Astoria_Hourly_transactions](https://github.com/user-attachments/assets/397f0574-3371-473a-99e2-cfe09934bc9f)

- **Peak Hours (8 AM - 11 AM):**

    - The transactions are highest between 8 AM and 11 AM, with the peak at 10 AM.

    - The number of transactions during these hours ranges from approximately 4,500 to 5,500, indicating a busy period in the morning.
      Morning Spike (7 AM):

    - The transactions start at around 4,000 at 7 AM, showing a steady increase as the morning progresses.

- **Midday Stability (11 AM - 3 PM):**

    - From 11 AM to 3 PM, the number of transactions stabilizes, hovering around 4,000.

    - This period indicates a consistent level of activity during midday.

- **Afternoon Decline (4 PM - 7 PM):**

    - After 3 PM, the transactions gradually decline, reaching about 3,000 by 7 PM.

    - The decrease suggests a drop-off in activity as the day progresses into the evening.

Overall, the highest transaction volumes occur in the morning, with a peak around 10 AM. There's a consistent level of activity during midday, followed by a gradual decline in the afternoon and evening.

**3. Number of transactions by PRODUCT CATEGORY**

![Astoria_transactions_by_Product_Category](https://github.com/user-attachments/assets/f14c94ca-d039-4ae8-82a1-a3a02935aaf6)

- **Top Categories:**

   - Coffee is the most popular product category, with 20,025 transactions, making it the clear leader.

   - Tea follows with 16,260 transactions, showing significant popularity as well.

- **Mid-Range Categories:**

   - **Bakery items** are the third most popular category, with 7,289 transactions, indicating a strong preference for baked goods.

   - **Drinking Chocolate** has 4,300 transactions, which is notably lower than Bakery but still substantial.

- **Low-Volume Categories:**

    - **Flavours** have 1,490 transactions, suggesting they are a niche interest.

    - **Coffee beans** and **Loose Tea** are less popular, with 502 and 344 transactions, respectively. This might indicate that customers prefer ready-made 
        coffee and tea rather than preparing their own.

    - **Branded products** have 279 transactions, which could include specialty or luxury items.

    - **Packaged Chocolate** is the least popular category with only 110 transactions, indicating minimal interest in this product.

Overall, coffee and tea dominate the market in Astoria, with bakery items also showing strong performance. Categories like packaged chocolate and branded products are less popular, possibly due to their niche appeal or higher price points.

**4. Number of transactions and Revenue by PRODUCT TYPE**

![Astoria_top_15_Products](https://github.com/user-attachments/assets/a0941885-dd47-45af-9e2b-3d3a135dfb44)

- **Top Sellers:**

    - Brewed Chai Tea and Gourmet Brewed Coffee lead in transaction volume, with over 6,000 transactions each, generating $27,428 and $23,823 in revenue, 
        respectively.

    - Barista Espresso, while slightly behind in transaction volume (4,930), generates the highest revenue at $27,935, indicating a higher price point.

- **High Revenue Products:**

    - Products like Hot Chocolate and Brewed Herbal Tea show strong sales, with Hot Chocolate generating $26,335 from 4,300 transactions, and Brewed 
      Herbal Tea bringing in $16,282 from 4,008 transactions.

    - Premium and Organic Brewed Coffees also contribute significant revenue ($13,946 and $12,623, respectively) with around 3,000 transactions each.

- **Low-Volume, Low-Revenue Products:**

    - Sugar-Free Syrup and Regular Syrup have the lowest transaction volumes (379 and 1,111, respectively) and contribute minimally to revenue, with Sugar-Free 
       Syrup only generating $454.

- **Bakery Items:**
 
    - Scones and Pastries show decent sales, with Scones generating $11,630 from 3,205 transactions, highlighting a consistent demand for baked goods alongside 
      beverages.

  ---

  #### B) For Location in **HELL'S KITCHEN:**

**1. **REVENUE** by Month**

![Hell_Kitchen's_Monthly_Revenue](https://github.com/user-attachments/assets/f04bd6d6-502d-447c-aa8d-593dff24b53e)

**Initial Drop:** Revenue started at a relatively high point in January but declined slightly in February.

**Consistent Growth:** From March to June, there was a consistent upward trend in revenue, with the highest point recorded in June.

Overall, the analysis indicates that Hell's Kitchen has been gaining traction and increasing its revenue over the specified period.
