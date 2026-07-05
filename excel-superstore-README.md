# Retail Sales Analysis (Excel)

![Excel](https://img.shields.io/badge/Excel-Data%20Analysis-217346?logo=microsoftexcel&logoColor=white)
![PivotTables](https://img.shields.io/badge/PivotTables-Data%20Summarization-blue)
![License](https://img.shields.io/badge/License-MIT-green)

An Excel-based data analysis project exploring regional and category-level
sales performance in a real retail dataset, with a focus on data quality
checks before drawing conclusions.

## Overview
This project analyzes the Sample Superstore dataset (9,800 rows of retail
transactions) to answer: which regions and product categories generate the
most revenue? Before summarizing the data, it was checked for common data
quality issues — duplicates and missing values — to make sure the results
could be trusted.

## Tools Used
- **Microsoft Excel** — Pivot Tables, PivotCharts, conditional formatting,
  formula-based data quality checks

## Data Cleaning Process
- **Duplicate check:** Used Excel's "Remove Duplicates" tool across Order ID,
  Product ID, and Sales columns → **no duplicates found**
- **Missing value check:** Used `=COUNTBLANK()` across the full dataset →
  **11 blank cells found, all isolated to the Postal Code column**
- **Decision:** Retained all rows, since Postal Code is not used in the
  Region/Category/Sales analysis — removing otherwise-complete sales
  records over one unrelated missing field would discard valid data

## Key Findings

- **West is the top-performing region** at RM710,219.68 in total sales,
  followed closely by East (RM669,518.73). Central (RM492,646.91) and
  South (RM389,151.46) trail behind.

- **Technology is the highest-grossing category overall**, at
  RM827,455.87 — ahead of Furniture (RM728,658.58) and Office Supplies
  (RM705,422.33) — despite Office Supplies likely having the highest
  volume of individual transactions.

- **East + Technology is a standout combination**, generating
  RM263,116.53 — the single highest region/category pairing in the
  dataset alongside West + Technology (RM247,404.93).

- **Data was largely clean**, with only 11 missing values (0.1% of all
  cells) across the entire 9,800-row dataset, and zero duplicate
  transactions — reflecting the dataset's status as a well-maintained
  practice dataset.

## Pivot Table Summary

| Region  | Furniture | Office Supplies | Technology | Total |
|---------|-----------|------------------|------------|-------|
| Central | RM160,317 | RM163,590 | RM168,739 | RM492,647 |
| East    | RM206,461 | RM199,941 | RM263,117 | RM669,519 |
| South   | RM116,531 | RM124,425 | RM148,195 | RM389,151 |
| West    | RM245,348 | RM217,467 | RM247,405 | RM710,220 |
| **Total** | **RM728,659** | **RM705,422** | **RM827,456** | **RM2,261,537** |

## Skills Demonstrated
- Data cleaning: duplicate detection, missing value analysis (`COUNTBLANK`)
- Pivot Tables: multi-dimensional data summarization
- PivotCharts: automated chart generation from summarized data
- Conditional formatting: color scales for visual trend identification
- Currency and column formatting

## Data Source
[Sample Superstore Dataset](https://www.kaggle.com) (Kaggle)

## License
This project is licensed under the MIT License — see the [LICENSE](LICENSE)
file for details.
