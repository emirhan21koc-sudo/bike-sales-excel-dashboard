# Bike Sales Analysis – Excel Dashboard

An interactive Excel dashboard analyzing which customer profiles are most likely to buy a bike.

![Dashboard](Screenshot%202026-10-16%20at%2018.42.29.png)

## Business Question
**Which customer segments should the company target to increase bike sales?**

## Dataset
- **Source:** [Bike Buyers dataset (Kaggle)](https://www.kaggle.com/datasets/heeraldedhia/bike-buyers)
- **Size:** 1,000 customers, 13 columns (income, age, marital status, children, education, occupation, cars, commute distance, region, purchase outcome)

## Process
1. **Data cleaning**
   - Kept the raw data untouched (`bike_buyers` sheet) and worked on a copy (`Working Sheet`)
   - Removed 26 duplicate rows (1,026 → 1,000 customers)
   - Replaced coded values with readable labels (`M/S` → `Married/Single`, `M/F` → `Male/Female`)
2. **Feature engineering**
   - Created an `Age Brackets` column with a nested `IF` formula:
     Adolescent (<31), Middle Age (31–54), Old (55+)
   - Pivot tables use an exact data range, so no `(blank)` items appear
3. **Analysis with pivot tables**
   - Average income by gender and purchase outcome
   - Purchases by commute distance
   - Purchases by age group
4. **Dashboard**
   - Combined three clustered column pivot charts on one sheet
   - Added slicers (Gender, Marital Status, Region) connected to all charts for interactive filtering

## Key Findings
| Segment | Purchase rate |
|---|---|
| Overall | 48% |
| Middle Age (31–54) | **55%** |
| Adolescent (<31) / Old (55+) | 36% / 31% |
| Commute 2–5 miles | **59%** |
| Commute 10+ miles | 30% |
| Pacific region | **59%** |
| Single vs. Married | 54% vs. 43% |
| 0 cars vs. 2+ cars | 61% vs. ~36% |

- Buyers have a higher average income than non-buyers (≈ $58.0K vs. $54.9K).
- Middle-aged customers with a short commute (0–5 miles) and few or no cars are the strongest buyer group.

## Recommendation
Focus marketing on **middle-aged, single customers with 0–1 cars and a commute under 5 miles**, especially in the **Pacific** region. Customers commuting more than 10 miles are the least likely to buy and should be a lower priority.

## Tools
Microsoft Excel: data cleaning, `IF` formulas, pivot tables, pivot charts, slicers

## Files
| File | Description |
|---|---|
| `bike_sales_dashboard_7.xlsx` | Workbook with raw data, cleaned data, pivot tables and dashboard |
| `Screenshot 2026-10-16 at 18.42.29.png` | Screenshot of the dashboard |

---
*Part of my data analytics bootcamp portfolio.*
