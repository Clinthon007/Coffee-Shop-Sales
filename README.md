# Coffee Shop Sales Analysis

## Project Overview

It's a coffee shop chain with three (3) different locations in New York City. 

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

EDAs were carried out with the use of **Pivot Tables** to look into the following points;

-  **Revenue** by Month
-  Number of transactions by **Weekday** and by **Hour** of day (two Pivot tables)
-  Number of transactions by **Product Category**
-  Number of transactions and Revenue by **Product type**

