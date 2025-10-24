Mapping Survival and Mortality Trends of COVID-19: A Global Perspective

Overview
--------
This project presents a comprehensive analysis of global COVID-19 trends, focusing on mortality and recovery patterns across countries. Using over 12.5 million rows of raw, messy data, I cleaned, transformed, and visualized key indicators to uncover insights into the pandemic’s global footprint.

Objectives
----------
- Clean and preprocess a massive dataset of global COVID-19 statistics
- Identify the top 10 countries by total deaths
- Highlight the top 10 most affected countries by confirmed cases
- Create choropleth maps to visualize:
  - Total deaths across 221 countries
  - Recovery numbers across 19 countries (due to missing data in others)

Data Cleaning
-------------
- Parsed and validated over 12.5 million records from multiple sources
- Handled missing values, inconsistent formats, and country-level aggregation
- Ensured accurate alignment of cumulative metrics (confirmed, deceased, recovered)

Key Findings
------------
- Top 10 countries by total deaths include the United States, Brazil, India, Russia, and Mexico
- Top 10 most affected countries by confirmed cases include the United States, India, France, Germany, and Brazil
- Recovery data was only available for 19 countries, requiring selective mapping and annotation

Visualizations
--------------
- Global Choropleth Map of Total Deaths: Highlights mortality intensity across 221 countries
- Global Choropleth Map of Recoveries: Focused view of recovery trends where data was available
- Bar charts for top 10 countries by deaths and confirmed cases

Tools & Technologies
--------------------
- Python (pandas, numpy, plotly, cufflinks)
- Jupyter Notebook
- Excel (for initial filtering and validation)
- GeoJSON for choropleth mapping

Limitations
-----------
- Recovery data was missing for most countries, limiting global completeness
- Death rates may be affected by underreporting or inconsistent testing policies

Next Steps
----------
- Integrate vaccination data for survival analysis
- Explore time-series trends and variant-specific impacts

- Expand recovery mapping as more data becomes available
