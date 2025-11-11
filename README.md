# SQL Layoffs Dataset - Exploratory Data Analysis (EDA)

This project focuses on **Exploratory Data Analysis (EDA)** on the global tech layoffs dataset.  
The analysis is performed entirely in **SQL** using the cleaned table `layoffs_staging2` from the previous step of the project.

## Objectives
- Explore layoffs across companies, industries, countries, and years.
- Identify patterns, trends, and outliers in the data.
- Analyze the timeline of layoffs and cumulative impact over time.
- Compare yearly top companies by layoffs.

## Dataset
- **Table:** `layoffs_staging2`
- **Key Fields:**  
  `company`, `industry`, `country`, `total_laid_off`, `percentage_laid_off`,
  `funds_raised_millions`, `date`, `stage`

## SQL Techniques Used
- Aggregation & Grouping (`SUM`, `MAX`, `MIN`)
- Trend and time-series analysis using date functions
- **CTEs** for structured analysis
- **Window Functions** for ranking and rolling totals
- Filtering & comparison queries

## Key Insights Generated
- Companies with the most layoffs overall.
- Industries and countries most affected.
- How layoffs evolved by year and month.
- Funding stage correlation with layoffs.
- **Top 3 companies with the highest layoffs per year.**

## Example Query Snippets
```sql
SELECT company, SUM(total_laid_off)
FROM layoffs_staging2
GROUP BY company
ORDER BY 2 DESC;

