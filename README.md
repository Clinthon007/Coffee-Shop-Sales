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
- i. Number of transactions by **Weekday** and
 
  ii. by **Hour** of day (two Pivot tables)
-  Number of transactions by **Product Category**
-  Number of transactions and Revenue by **Product type**

    **Slicer** was added finally for the _Store_location_ to connect to the tables created and make it them dynamic in order for users to be able to update themselves with transaction information from the different locations.

   ![Select Location](https://github.com/user-attachments/assets/fb5594f5-430c-4928-b8f7-54629208ea3e)


---

### Data Analysis

  #### A) For Location in ASTORIA:
  
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

  #### B) For Location in HELL'S KITCHEN:

**1. REVENUE by Month**

![Hell_Kitchen's_Monthly_Revenue](https://github.com/user-attachments/assets/f04bd6d6-502d-447c-aa8d-593dff24b53e)

**Initial Drop:**

  Revenue started at a relatively high point in January but declined slightly in February.

**Consistent Growth:** 

  From March to June, there was a consistent upward trend in revenue, with the highest point recorded in June.

Overall, the analysis indicates that Hell's Kitchen has been gaining traction and increasing its revenue over the specified period.

**2.**

**I. Number of transactions by WEEKDAY**

![Hell_Kitchen's_Weekday_transactions](https://github.com/user-attachments/assets/616f2490-5de4-45e9-9ae6-d079b8c49e37)

**Peak Days:**

   Thursday and Friday consistently have the highest number of transactions, indicating they are the busiest days for the location.

**Midweek Consistency:** 

  Wednesday, Thursday, and Friday show relatively similar transaction levels, suggesting a fairly consistent customer flow during the middle of the week.

**Weekend Dip:** 

  Saturday and Sunday see a noticeable decrease in transactions compared to weekdays, suggesting a decline in customer activity on weekends.

Overall, the analysis indicates that Hell's Kitchen's busiest days are during the middle of the week, with a significant drop in transactions on weekends.

**II. Number of transactions by HOUR**

![Hell_Kitchen's_Hourly_transaction](https://github.com/user-attachments/assets/2faead38-eaf5-49c8-a5c5-f9255c81c00f)

**Peak Hours:** 
       The busiest hours are between 8 am and 10 am, with 9 am being the absolute peak. This suggests a strong breakfast or brunch crowd.

**Lunch Rush:** 
       There's a noticeable dip after 10 am, followed by a smaller peak around 1 pm, indicating a more moderate lunch rush compared to breakfast.

**Steady Afternoon:** 
       Transactions remain relatively consistent between 1 pm and 6 pm, suggesting a steady flow of customers throughout the afternoon.

**Dinner Decline:** 
       There's a decline in transactions starting around 6 pm, with a small spike at 7 pm before tapering off significantly. This indicates dinner is not as busy 
       as breakfast or lunch.

**Late Night:** 
       Activity drops significantly after 8 pm.

**3. Number of transactions by PRODUCT CATEGORY**

![Hell_Kitchen's_transactions_by_Product_Category](https://github.com/user-attachments/assets/b4e801f0-4d3f-4a3b-b0c1-3fb388127edb)

**Coffee Dominance:** Coffee is the clear leader in terms of transactions, significantly outselling all other categories.

**Tea and Bakery:** Tea and bakery items occupy the second and third positions, respectively, indicating a strong demand for these products.

**Smaller Categories:** The remaining categories (Drinking Chocolate, Flavors, Coffee Beans, Loose Tea, Packaged Chocolate, and Branded) have considerably fewer transactions, suggesting they are less popular or niche products.

**4. Number of transactions and Revenue by PRODUCT TYPE**

![Hell_Kitchen's_Top_15_Products](https://github.com/user-attachments/assets/bf9dabb0-f62d-4f88-ae8d-137681257453)

**Espresso Dominance:** Barista Espresso leads in both transactions and revenue, indicating its strong appeal to customers.

**Coffee and Tea Popularity:** Coffee-based drinks (Barista Espresso, Gourmet brewed coffee, Organic brewed coffee, Drip coffee, Premium brewed coffee) and teas (Brewed Chai tea, Brewed Black tea, Brewed herbal tea, Brewed Green tea) dominate the top 15, suggesting a strong preference for these beverages.

**Pastries and Syrups:** Pastries (Scone, Pastry, Biscotti) and syrups (Regular syrup, Sugar-free syrup) are also represented in the top 15, though with fewer transactions and revenue compared to coffee and tea.

---

#### C) For location in LOWER MANHATTEN:

**1. REVENUE by Month**

![Lower_Manhattan's_Monthly_Revenue](https://github.com/user-attachments/assets/9552dffd-38f5-4675-bb15-afd369c63e2b)

**January:** $26,543.43

**February:** $25,320.05 (Slight dip)

**March:** $32,888.68 (Significant increase)

**April:** $39,159.33 (Continued growth)

**May:** $51,700.07 (Large increase)

**June:** $54,445.69 (Continued growth, highest revenue)

Overall, the coffee shop's revenue more than doubled from January to June, indicating a successful period. The biggest jump in revenue occurred between April and May. This could be due to a number of factors, such as seasonality (warmer weather leading to increased coffee sales), successful marketing campaigns, or new product offerings.

**2.**

   **I. Number of transactions by WEEKDAY**

 **Peak Days:** Monday and Friday consistently have the highest number of transactions, indicating they are the busiest days for the location.
 
**Midweek Consistency:** Tuesday, Wednesday, Thursday, and Friday show relatively similar transaction levels, suggesting a fairly consistent customer flow during the middle of the week.

**Weekend Dip:** Saturday and Sunday see a noticeable decrease in transactions compared to weekdays, suggesting a decline in customer activity on weekends.

Overall, the analysis indicates that the Lower Manhattan coffee shop's busiest days are Monday and Friday, with a significant drop in transactions on weekends.

  **II. Number of transactions by HOUR**

  ![Lower_Manhattan's_Hourly_transactions](https://github.com/user-attachments/assets/caaaca46-cb93-4b9e-a803-ab50a809d1ee)

**Peak Hours:** The hours between 8 AM and 10 AM consistently have the highest number of transactions, indicating they are the busiest times for the location.

**Morning Rush:** The early morning hours (6 AM to 10 AM) see a significant increase in transactions, likely due to customers grabbing coffee on their way to work or school.

**Afternoon Slump:** The afternoon hours (12 PM to 3 PM) experience a relatively lower number of transactions, suggesting a decline in customer activity during this time.

**Evening Surge:** The late afternoon and early evening hours (4 PM to 7 PM) see a slight increase in transactions, potentially due to customers seeking a caffeine boost or relaxing after work.

**Quiet Hours:** The hours after 7 PM experience a significant drop in transactions, indicating that the coffee shop is less busy during the late evening.

Overall, the analysis indicates that the Lower Manhattan coffee shop's busiest times are in the morning, with a noticeable decline in transactions during the afternoon and a slight increase in the late afternoon and early evening.

**3. Number of transactions by PRODUCT CATEGORY**

![Lower_Manhattan's_Product_Category_transactions](https://github.com/user-attachments/assets/7655efcb-3cb4-4c56-9aee-e19b2060e9da)

**Coffee Dominance:** Coffee is the clear leader in terms of transactions, significantly outselling all other categories.

**Tea and Bakery:** Tea and bakery items occupy the second and third positions, respectively, indicating a strong demand for these products.

**Smaller Categories:** The remaining categories (Drinking Chocolate, Flavors, Coffee Beans, Loose Tea, Packaged Chocolate, and Branded) have considerably fewer transactions, suggesting they are less popular or niche products.

Overall, the analysis indicates that coffee is the driving force behind the coffee shop's sales, while tea and bakery items are also significant contributors.

**4. Number of transactions and Revenue by PRODUCT TYPE**

![Lower_Manhattan's_Top_15_Products](https://github.com/user-attachments/assets/046ea0ee-e49d-4070-be6e-1b24a0eae443)

**Espresso Dominance:** Barista Espresso leads in both transactions and revenue, indicating its strong appeal to customers.

**Coffee and Tea Popularity:** Coffee-based drinks (Barista Espresso, Gourmet brewed coffee, Organic brewed coffee, Drip coffee, Premium brewed coffee) and teas (Brewed Chai tea, Brewed Black tea, Brewed herbal tea, Brewed Green tea) dominate the top 15, suggesting a strong preference for these beverages.

**Pastries and Syrups:** Pastries (Scone, Pastry, Biscotti) and syrups (Regular syrup, Sugar-free syrup) are also represented in the top 15, though with fewer transactions and revenue compared to coffee and tea.

Overall, the analysis indicates that coffee and tea are the driving forces behind the coffee shop's sales, with Barista Espresso being the standout product.

---

### FINDINGS
 
**Location in LOWER MANHATTEN**
 
   - Lower Manhatten has a huge spike during the morning commute, especially within the hours 
     of 7am to 10am.

   - But their 7pm to 8pm mark isn't really selling much products at all which might result to 
     huge loss within those periods.
 
   -  Another major spike in sales is on Monday over other week days which hits above $7,000.

   - Coffee and tea are the top products in Manhatten.

**Location in Astoria**

   - Astoria's Monday traffic isn't as heavy as that of Manhatten's, rather, Thursday has more 
     traffic in that location. There's still some pattern between both locations.

   - Transactions stays high till closing time (evening period)

   - Coffee and tea are the top products as well.

**Location in HELL'S KITCHEN**

   - Lower traffic on Monday compared to the previous locations. Tuesday and Friday are its 
    traffic-filled days.
  
   - Lower transactions at early hours between 6am and 7am, but highest between 8am to 10am. 
     It drops again from 11am and stays same throughout afternoon periods. Lesser sales at 8pm.

   - Coffee and tea are its top products as well.


RECOMMENDATIONS

- Since there seemed to be lesser products sold after 6pm for the Manhatten location, it might be better to close the shop after 6pm mark which might help to improve margin if the operating hours is changed.

- Evening Menu: offering a more extensive evening menu, including light meals or desserts could bring in more customers seeking not just tea or coffee during such hours.

-  Customer Feedback: Gather customer feedback to understand their preferences and address any concerns.

- Local Events: Take advantage of local events or festivals to attract additional customers. 
