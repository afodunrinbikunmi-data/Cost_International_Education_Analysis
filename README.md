# International Education Cost Analysis: Decoding the "Tuition Trap" and Geographic Cost Disparity
A data-driven analysis of 622 universities across 71 countries revealing why geography and accommodation, not tuition are the primary drivers of international education costs

## Project Summary
A comprehensive cost analysis of international higher education across 622 universities in 71 countries. The goal was to identify the true cost of studying abroad beyond tuition fees and determine which countries, cities, and degree levels offer the best financial value for international students.

**Key finding: Only 27% of the cost of studying abroad is tuition.
The remaining 73% funds hidden costs that most students never plan for.**

## Dataset Overview
| Field | Detail |
|---|---|
| **Universities** | 622 institutions |
| **Countries** | 71 nations |
| **Degree Levels** | Bachelor's, Master's, PhD |
| **Currency** | All values standardised to USD |
| **Source** | Cost of International Education Dataset (Kaggle) |

**Period:** 2024 – 2025 Academic Year  
**Coverage:** 71 Countries across 6 Continents and 622 Accredited Universities.

## Key Columns in the Dataset
| Column | Description |
|---|---|
| **Country / City / University** | Geographic and institutional identifiers |
| **Program / Level / Duration_Years** | Academic program details |
| **Tuition_USD** | Total tuition for entire program |
| **Rent_USD** | Average monthly accommodation cost |
| **Insurance_USD** | Annual health/student insurance |
| **Visa_Fee_USD** | One-time visa application fee |
| **Living_Cost_Index** | Cost of living vs New York City baseline (100) |
| **Exchange_Rate** | Local currency units per USD |

## Tools Used
| Tool | Purpose |
|---|---|
| **Microsoft Excel** | Data cleaning, feature engineering, PivotTable analysis |
| **Power Query** | Encoding error resolution, data type verification |
| **Microsoft Power BI** | DAX measures, interactive 3-page dashboard |
| **DAX** | Custom cost measures and aggregations |

## Data Cleaning & Preparation
- Re-imported dataset via Power Query to resolve City column encoding errors
- Verified all financial columns as correct numeric format
- Confirmed zero duplicate records
- Standardised all monetary values to USD
- Engineered 5 calculated columns in Excel:
  - **`Total Cost`** — Tuition + (Rent×12×Duration) + (Insurance×Duration) + Visa
  - **`Cost Per Year`** — Total Cost ÷ Duration Years
  - **`Total Rent`** — Full accommodation cost across program duration
  - **`Non-Tuition Cost`** — Total Cost minus Tuition
  - **`Tuition Percentage`** — Tuition as % of Total Cost

## Data Modeling
This project uses a single flat table structure no relational joins required. All DAX measures were built in a dedicated measures table in Power BI and calculated directly from the enriched dataset. Key measures include 
- **Avg Total Cost**
- **Avg Cost Per Year**
- **Avg Tuition**
- **Avg Non-Tuition Cost**
- **Avg Rent, Avg Tuition %**
- **Total Countries**
- **Total Universities**

## Key Questions & Analysis
1. Which countries offer the most affordable total cost of study?
2. How do non-tuition costs compare to tuition across destinations?
3. Do "free tuition" countries actually offer lower total costs?
4. Which degree level is most financially intense per year?
5. Which cities are most and least expensive for international study?
6. What drives the cost gap between the most and least expensive destinations?

## Key Insights
- **73% of study abroad cost is non-tuition** — hidden costs dominate globally
- **Tuition Trap confirmed** — Germany ($177 tuition) costs $30K+ in living expenses
- **$187K city cost gap** — Stanford ($193K) vs Gabes, Tunisia ($5.7K)
- **Every top-10 most expensive city is American** — the Institutional Tax is real
- **Master's: highest annual intensity** — $19,898/year despite lowest total cost
- **PhD: best annual value** — $16,492/year with highest total investment
- **Rent = 64% of global student budget** — accommodation is the primary risk
- **North Africa dominates affordability** — Tunisia and Algeria lead the value tier
- **Geography beats all other variables** — location determines cost more than degree type

## Recommendations
1. **Plan around monthly burn rate, not tuition headline** — Germany costs more monthly than Malaysia
2. **Target second-tier cities and regional value hubs** — save $50K–$180K without sacrificing quality
3. **Secure housing before departure** — rent is 64% of the budget and the most volatile variable

## Dashboard / Visualization
The Power BI dashboard contains 3 report pages:

- **Global Overview**: KPIs, cost by country, world map, cost per year comparison
- **Cost Structure**: Tuition vs Non-Tuition, degree level analysis, rent by country, scatter
- **City Intelligence**: Top 10 expensive cities, Top 10 affordable cities, full data table |

## Project Structure

```text
├── data/
│   └── cost_of_international_education.xlsx
├── dashboard/
│   └── education_cost_dashboard.pbix
├── report/
│   └── Cost_Of_International_Education_Analysis.pptx
├── screenshots/
│   ├── global_overview.png
│   ├── cost_structure.png
│   └── city_intelligence.png
└── README.md
```

## About me
Afodunrinbi Samad Akinkunmi
I am a Certified Data Analyst with a strong passion for transforming raw data into meaningful insights that support informed decision-making. My work focuses on exploring datasets, identifying patterns, and communicating findings in a clear and impactful way. I enjoy approaching problems analytically, breaking them down into structured steps, and uncovering the story behind the data. Beyond data analysis, I am actively expanding towards becoming a Data Scientist, with an interest in building predictive modeling and advanced analytics.

Data Analyst | Excel | Power BI | Python | SQL | Figma

Connect With Me On - [LinkedIn](https://www.linkedin.com/in/akinkunmiafod) | [Medium](https://medium.com/@afodunrinbikunmi) | Gmail: afodunrinbikunmi@gmail.com
