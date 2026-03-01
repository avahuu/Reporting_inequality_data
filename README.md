# Global Health Inequality Analysis

An R-based data analysis project exploring global health and economic indicators, regression modeling, and U.S. Census demographics.

## Project Structure

```
├── 01_descriptive_analysis.Rmd    # Summary statistics, correlations, distributions
├── 02_regression_analysis.Rmd     # Linear regression, residuals, outlier detection
├── 03_census_demographics.Rmd     # Census ACS data: race, age, multi-year joins
├── data/
│   ├── globalind.csv              # WHO Global Health Observatory indicators (222 countries)
│   └── schools.csv                # California schools dataset
└── README.md
```

## Analysis Overview

### 1. Descriptive Analysis
Explores distributions and correlations across 222 countries using data from the **WHO Global Health Observatory** — covering GNI, health expenditure, education spending, mortality rates, and more.

### 2. Regression Analysis
Builds linear models to quantify the relationship between national income and health spending (R² = 0.87). Also models the impact of poverty on academic performance in California schools.

### 3. Census Demographics
Uses the `tidycensus` package to pull ACS data, examining racial/ethnic composition at the census tract and county level in California, plus year-over-year household income changes.

## Data Sources

- **Global Health Observatory** (WHO) — Country-level health and economic indicators
- **California Schools Dataset** — School-level poverty, demographics, and academic performance
- **U.S. Census Bureau ACS** — American Community Survey 5-year estimates (2022–2023)

## How to Run

1. Open any `.Rmd` file in RStudio
2. Install required packages (if not already installed):
   ```r
   install.packages(c("tidyverse", "dplyr", "ggplot2", "knitr",
                       "psych", "janitor", "tidycensus", "modelr"))
   ```
3. For Census analysis (03), set up your API key:
   ```r
   census_api_key("YOUR_KEY", install = TRUE)
   ```
4. Click **Knit** to generate the HTML report

## Tools & Packages

`R` · `tidyverse` · `ggplot2` · `psych` · `tidycensus` · `modelr`

---

*Created by Ava Hu · February 2026*
