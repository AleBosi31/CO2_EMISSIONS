# 🌍 The Invisible Footprint: A Global CO2 Emissions Analysis

**Authors**: Alessandro Bosi, Denis Bugaenco, Eleonora Zullo  
**Project for**: Data Management – Master's in Data Science

## 📌 Abstract

This project explores the relationship between **CO2 emissions**, **population density**, and **territorial extension** across countries. Using two different datasets—one on demographic and geographic data and another on CO2 emissions per capita—we aimed to uncover significant patterns and correlations, and to assess the role of population and area in influencing emission levels.

## 📊 Objectives

- Identify which countries contribute the most to CO2 emissions.
- Analyze the evolution of emissions from 1990 to 2020.
- Investigate the impact of **population density** and **land area** on emission levels.

## 🗂️ Data Sources

- **Demographic and geographic data** via [REST Countries API](https://restcountries.com)
- **CO2 emissions per capita** from [World Bank Open Data](https://data.worldbank.org/indicator/EN.ATM.CO2E.PC)

## 🔧 Methodology

### 1. **Data Acquisition**
- Collected country-level data using REST API and MongoDB.
- Downloaded CO2 emissions dataset (1960–2023) from the World Bank.

### 2. **Data Preparation**
- Cleaned data by removing null values and redundant columns.
- Trimmed years with incomplete data (only 1990–2020 kept).
- Handled missing data via imputation (e.g., linear regression for Namibia).

### 3. **Data Integration**
- Harmonized country names using ASCII normalization and `fuzzywuzzy` matching.
- Merged datasets using `pandas.merge()` with inner join logic.
- Added new variable: `density = population / area`.

### 4. **Data Storage**
- Final dataset (`CO2_emission`) uploaded to MongoDB.
- Structure includes country details and yearly CO2 emissions from 1990–2020.

### 5. **Data Analysis**
- Top 10 countries with highest per capita emissions in 2020.
- Countries with the greatest reduction from 1990 to 2020.
- Scatter plot of total CO2 emissions vs population (log scale).

## 📈 Key Insights

- Gulf countries (e.g., Qatar, Bahrain, Kuwait) lead in per capita emissions.
- Luxembourg showed the most significant emission decrease (−17.10 tons).
- Population alone does not explain emissions—industrialization plays a key role.

## 👥 Team Roles

- **Alessandro Bosi**: Data sourcing and acquisition
- **Denis Bugaenco**: Data cleaning and integration
- **Eleonora Zullo**: Data analysis and result interpretation

## 📚 References

- [REST Countries API](https://restcountries.com)
- [World Bank Data](https://data.worldbank.org/indicator/EN.ATM.CO2E.PC)
- Cielen et al. *Introducing Data Science*, Manning, 2016
- Rezzani, *Big Data Analytics*, Apogeo, 2017

---

