[README - Capstone.md](https://github.com/user-attachments/files/34440059/README.-.Capstone.md)
[Uploading README - Capstone.md…]()
# Capstone_1 
Repository for Capstone due on 11/6/26 
-- Hello! This README file is for my first Capstone Project at Year Up United for the Data Analytics program. This is where I will be storing all of my code, along with questions I have. Thank you!

# South Carolina Sales Territory Analysis (MySQL)

SQL analysis of the `sample_sales` database for the **South Carolina
sales territory (South region)**, ending with a recommendation on where
to focus sales attention next quarter.

## Dataset

The sample retail database covers **January 1, 2022--December 31, 2025**
and includes approximately **335,000 in-store transactions** and
**126,000 online orders** across **111 stores**.

  -----------------------------------------------------------------------
  Table                               Purpose
  ----------------------------------- -----------------------------------
  `Store_Sales`                       In-store transactions (date, store,
                                      product, amount)

  `Online_Sales`                      Online orders (date, product,
                                      total, ship-to state)

  `Store_Locations`                   Store name and state

  `Management`                        Region, regional director, state,
                                      and sales manager

  `Products`, `Inventory_Categories`, Product catalog and categories
  `Inventory_Subcategories`           

  `Shipper_List`                      Preferred shipper per state
  -----------------------------------------------------------------------

## Questions Answered

The queries use `INNER JOIN`, aggregate functions (`SUM`, `AVG`,
`COUNT`, `MIN`, `MAX`), date functions, and `GROUP BY` / `ORDER BY` to
answer:

1.  What is the total revenue and date range covered for South Carolina?
2.  What is revenue by year and month?
3.  How does South Carolina compare with the South region?
4.  How many transactions occur per month, and what is the average sale
    by product category?
5.  How do stores rank by in-store revenue?

## Key Findings

-   **Revenue:** \$648,812.56 in store sales from January 1, 2022, to
    December 30, 2025, across two stores: Greenville (\$337K) and
    Charleston (\$312K).
-   **Regional share:** South Carolina accounts for about 8% of South
    region store revenue (Florida: 49%; Texas: 43%). This share is
    steady year over year.
-   **Growth:** South Carolina's 2025 store revenue grew 68% over 2024,
    the fastest growth of any state.
-   **Sales mix:** Technology & Accessories accounts for 73% of South
    Carolina revenue.
-   **Area for improvement:** Textbooks grew only 21% from 2022 to 2025,
    compared with 158% growth for Technology. This is a company-wide
    trend, not specific to South Carolina.

## Recommendation

Focus next quarter's sales efforts on **Textbooks at both South Carolina
stores**. Textbooks are the one category showing comparatively weak
growth. At the same time, protect **Technology & Accessories**, which
generates most of the revenue.

## Notes and Limitations

-   The South region comparison includes **store sales only**. Online
    orders are associated with `ShiptoState`, and the `Management` table
    credits them to the West region, so online orders are excluded from
    these queries.
-   South Carolina has only two stores, so a change at one store can
    noticeably affect the state's totals.
-   "Next quarter" refers to **Q1 2026**, the quarter after the dataset
    ends. South Carolina shows no consistent seasonal pattern.

## Usage

Run the dataset's setup script first. Then select the database and run
the queries in this repository's `.sql` file:

``` sql
USE sample_sales;
```

## Requirements

-   MySQL
-   The queries use `YEAR()` and `MONTH()` and group by column aliases.
