# Effect of COVID-19 Lockdown on Air Pollutant Levels in California



## Introduction

The COVID-19 pandemic prompted an unprecedented societal response. On **March 19, 2020**, California became the first U.S. state to issue a mandatory stay-at-home order, signifucantly reducing traffic, industrial and human activity. This created a rare natural experiment: the opportunity to isolate and measure the short-term effect of reduced human activity on air quality and whether intentional lockdown policies will have a positive effect in controling greenhouse gas emmissions.

This project explores how California's lockdown affected concentrations of five key air pollutants — **CO, NO₂, O₃, PM₂.₅, and PM₁₀** — using 2019 as a pre-pandemic baseline for year-over-year comparison.

---

## Data

<<<<<<< HEAD
=======
### **Data**
>>>>>>> 60e12aaf9fe0362eef387d132ce9a83162f3fb5b
The data used in this analysis is as follows:

1. [Outdoor Ari Quality Data - U.S. Environmental Protection Agency](https://www.epa.gov/outdoor-air-quality-data/download-daily-data)
2. [California state COVID-19 cases/deaths/tests - California Open Data](https://data.ca.gov/dataset/covid-19-time-series-metrics-by-county-and-state1)

Complete data dictionary can be found at 'data' folder in this reposiroty.

---

## Tech Stack

| Category | Tools |
|---|---|
| **Language** | Python |
| **Data manipulation** | `pandas`, `numpy` |
| **Visualisation** | `matplotlib`, `seaborn` |
| **Statistical analysis** | `scipy.stats` |
| **Environment** | Jupyter , VS Code |
| **Version control** | Git, GitHub |

---

## Method

### Analytical Approach

**Year-over-year comparison**: 2019 served as the baseline representing normal seasonal patterns; 2020 is the treatment year. This controls for seasonality without requiring a formal regression model, making findings interpretable and reproducible.

The analysis proceeded in three phases:

**Phase 1 — Data Wrangling**

*See complete data wrangling conducted in the Jupyter Notebook*

**Phase 2 — Results and Exploratory Data Analysis**

Monthly mean concentrations were calculated for each pollutant. The lockdown period (March 19 – June 30, 2020) was defined as the comparison window. Percentage change relative to 2019 was calculated for each pollutant during this window. 

**Phase 3 — Discussion and Limitations**

Primary traffic-related pollutants (NO₂, CO) were expected to respond readily to lockdown. PM.25 and PM10 results were examined separately due to their unusual rise late 2020.

---

## Results

*See full data wrangling and EDA conducted in the Jupyter Notebook. Interactive results available at the project HTML page.*

### Figure 1 — month-by-month pollutant comparison: 2019 vs. 2020 vs. 2021



Statewide monthly averages across all five pollutants reveal consistent year-over-year patterns for CO, NO₂, and O₃, with 2020 values dip slightly below 2019 during the lockdown period. The clearest divergence appears in PM₁₀ and PM₂.₅, where 2020 and 2021 both spike sharply above 2019 levels from August onward consistent with the record 2020 wildfire season and its lingering particulate impact into 2021.

---

### Figure 2 — Counties with the most significant air pollution reduction during lockdown (March 19 – June 15 2020 vs. 2019)



Comparing each county's average pollutant concentration during the lockdown period against the same period in 2019 isolates changes related to seasonal variation. Trinity showed the largest overall reduction (average −37.7% across all pollutants), followed by Mono (−27.2%) and Mariposa (−27.1%). All 15 counties shown recorded net reductions, with steeper drops generally observed in rural counties.

---

### Figure 3 — Monthly Average Air Pollutant Concentrations: Humboldt vs. Trinity (2019–2021)


Trinity's 2020 pollutant levels exceed both 2019 and 2021 across PM₂.₅ and PM₁₀ despite the lockdown, with post-lockdown PM₁₀ and PM₂.₅ spiking to 42.9 and 17.5 µg/m³, respectively. This is inconsistent with reduced human activity as the sole driver and is more likely attributable to wildfire smoke given Trinity's predominantly wilderness geography. Humboldt, which borders Trinity to the west, shows a similar PM pattern — PM₁₀ and PM₂.₅ remained elevated into 2021 — suggesting smoke spillover across county lines. For CO, NO₂, and O₃, both counties returned closer to 2019 levels by 2021.---

## Discussion

Trinity is one of California's least populated counties, with a total population of 16,112 ranking 54th most popultaed county in California. In terms of land size, Trinity covers a total area of 3,208 square miles, of which 3,179 square miles is land and 28 square miles is water, according to the U.S. Census Bureau reports. While Trinity is physically sizeable, it's nearly empty with only 5 people per square mile (one of the emptiest counties in the state), compared to California's overall figure of roughly 250. Thus, it's not entirely surprising to see that the least populated counties see a significant drop in air pollution.

However, Trinity's 2020 air pollutant levels surpass that of 2019 and 2021, specifically PM25 and PM10 levels, despite lockdown. PM10 and PM2.5 levels spiked to 42.934 and 17.526 µg/m³ post-lockdown, respectively. This significant increrase is unlikely due to just human activity returning to normal and more likely linked to the record-breaking California wildfire season in late 2020, given that Trinity is mostly wildreness. 

---

## Limitations

PM25 was consistently recorded in Trinity in comparison to other counties; this might have skewed the results. Suggestion for reproducing this analysis is to set a threshold for which counties are to be included (e.g. a minimum of 3 or 4 or 5 air pollutant recorded.)

---

## References

Bao, R., & Zhang, A. (2020). Does lockdown reduce air pollution? Evidence from 44 cities in northern China. *Science of the Total Environment, 731*, 139052. https://doi.org/10.1016/j.scitotenv.2020.139052

California Department of Public Health. (2023). *COVID-19 time-series metrics by county and state (archived)*. California Health and Human Services Open Data Portal. https://data.chhs.ca.gov/dataset/covid-19-time-series-metrics-by-county-and-state

U.S. Environmental Protection Agency. *Download daily data*. AirData: Air Quality Data Collected at Outdoor Monitors Across the US. https://www.epa.gov/outdoor-air-quality-data/download-daily-data

Newsom, G. (2020, March 19). *Executive Order N-33-20*. Office of the Governor of California. https://www.gov.ca.gov/wp-content/uploads/2020/03/3.19.20-attested-EO-N-33-20-COVID-19-HEALTH-ORDER.pdf

California Department of Forestry and Fire Protection (CAL FIRE). (n.d.). *2020 fire season incident archive*. https://www.fire.ca.gov/incidents/2020


