# Global COVID-19 Impact Analysis: Policy, Comorbidities, and Mortality Trends

## Project Overview

This project presents a comprehensive, two-stage analysis of global COVID-19 data, focusing on the interplay between government intervention (**Stringency Index**), underlying health factors (**comorbidities**), and resulting mortality rates.

The analysis utilizes advanced techniques, including **time-lagged correlation** and **geographical mapping**, to provide a data-driven understanding of the pandemic's severity and policy outcomes across different nations.

---

## Project Structure

The project is organized into dedicated folders for clarity and reproducibility:

| Folder | File | Purpose |
| :--- | :--- | :--- |
| `data/notebooks/` | `covid_analysis.csv` | **Original Raw Data** (Source for the entire analysis). |
| `data/notebooks/` | `data_cleaning.ipynb` | **Stage 1:** Cleans, preprocesses, and refines the original data. |
| `data/notebooks/` | `data_exploration_visualization.ipynb` | **Stage 2:** Loads refined data, performs analysis, and generates all final visualizations. |
| `data/notebooks/` | `covid_countries.csv`, etc. | **Refined Data Files** used by the visualization notebook. |
| `visuals/` | `*.png` | Contains exported images for easy viewing (No HTML). |

---

## Key Data Sources

The analysis begins with the primary dataset provided by **Our World in Data (OWID)**. The refined CSV files used for exploration are generated in the `data_cleaning.ipynb` step.

* **Primary Source URL:** `https://raw.githubusercontent.com/owid/covid-19-data/master/public/data/owid-covid-data.csv`
* `data/notebooks/covid_analysis.csv` (The primary raw file used to start the cleaning process).
* `data/notebooks/covid_countries.csv` (Country-day level data after initial cleaning)
* `data/notebooks/covid_latest_valid_mortality.csv` (Aggregated data for cross-country comparisons)

---

## Environment and Prerequisites

To successfully run both Jupyter Notebooks, you need a Python environment with the following libraries and data dependencies:

* Python: `pandas`, `numpy`, `seaborn`, `matplotlib`, `plotly`, `cufflinks`, `jupyter`
* GeoJSON (for choropleth mapping)
* pip install pandas numpy seaborn matplotlib plotly cufflinks jupyter
---

## Core Analysis & Visualizations

The `data_exploration_visualization.ipynb` notebook explores three core analytical themes:

### 1. Analysis of Policy Effectiveness (Stringency Index)

This investigation uses a **21-day time lag** to assess the potential impact of non-pharmaceutical interventions (NPIs) on mortality.

* **Global Correlation Distribution:** A **histogram** summarizing the Pearson correlation coefficient ($r$) between the lagged Stringency Index and Daily Deaths Per Million (DPM).
* **Geographic Correlation:** A **Choropleth Map** visualizing the correlation coefficient ($r$) for each country, showing where policy was effective (negative $r$) or driven by mortality (positive $r$).
* **Country-Specific Time Series:** A dual-axis **line plot** tracking the 7-day average of DPM and the lagged Stringency Index over time for a specific country (e.g., Bangladesh).

### 2. Global Mortality Trend Analysis

* **Continental Mortality Waves:** A **line plot** tracking the **7-day rolling average of new deaths per million** for each continent, essential for comparing the timing and severity of different waves globally.
* **Absolute Impact Comparison:** A dual **bar plot** comparing **Total Cumulative Cases** and **Total Cumulative Deaths** for the Top 10 most affected countries in absolute terms.

### 3. Impact of Comorbidity

* **Diabetes Prevalence vs. Mortality:** A **scatter plot** visualizing the relationship between a country's baseline **Diabetes Prevalence (%)** and its **Total COVID-19 Deaths per Million**, assessing the influence of pre-existing health on outcome.

---

## Key Findings

Based on the statistical and visual evidence generated:

* **Policy & Causality:** The **mean global correlation ($r$) is near zero or slightly positive**, suggesting that **reverse causality** (high mortality rates forcing governments to adopt stricter measures) is the dominant global trend, masking any direct negative policy effect. Policy effectiveness was highly **country-specific**.
* **Continental Disparities:** The line plot clearly shows **distinct mortality waves** across continents, with varying peak heights and timing, reflecting differences in policy, healthcare capacity, and population demographics.
* **Mortality Burden:** The DPM choropleth and continental waves confirm that the mortality burden (relative to population) was unevenly distributed, with specific regions bearing disproportionately high death rates.
* **Absolute Scale:** The Top 10 bar plot underscores the sheer **scale of the pandemic's footprint** in absolute numbers across a handful of major nations.

---

## Limitations

* **Data Completeness:** Several socio-demographic indicators and recovery data columns contained high proportions of missing values, limiting the scope of some cross-country comparisons.
* **Recovery Data:** Recovery data was missing for most countries, limiting global completeness.
* **Data Consistency:** Death rates may be affected by underreporting or inconsistent testing policies.
* **Reverse Causality:** The Stringency Index correlation is heavily influenced by the government's reactive behavior, making it difficult to isolate the true causal effect of the policy itself.

---

## Future Enhancements

* **Vaccination Impact:** Integrate vaccination data for survival analysis.
* **Advanced Time Series:** Explore time-series trends and variant-specific impacts.
* **Recovery Mapping:** Expand recovery mapping as more data becomes available.
* **Cross-Correlation Function (CCF):** Implement CCF to find the *optimal* lag time between policy action and mortality.

---

