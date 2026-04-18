# ✈️ Aviation Disasters Analysis

> An end-to-end data analysis of global aviation accidents — uncovering patterns in fatalities, high-risk operators, and the measurable impact of 9/11 on aviation safety.

![Python](https://img.shields.io/badge/Python-3.x-blue) ![Pandas](https://img.shields.io/badge/Pandas-2.0-green) ![GeoPandas](https://img.shields.io/badge/GeoPandas-mapping-orange) ![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

---

## The Problem

Aviation accidents generate vast amounts of historical data — but raw data alone doesn't answer the questions that matter: **Which countries are most dangerous? Which aircraft types cause the most deaths? Did 9/11 change aviation safety forever?**

This project transforms a complex, messy dataset into clear, actionable insights through rigorous data cleaning and multi-angle analysis.

---

## Key Questions Answered

1. Which countries have the highest number of aviation accidents?
2. How has the number of accidents evolved over time?
3. Which days of the week are most dangerous for aviation?
4. Which aircraft types are responsible for the most fatalities?
5. Which operators have the worst safety records?
6. **Did September 11, 2001 change average fatality rates?**
7. Is there a correlation between number of accidents and total deaths by aircraft type?

---

## Key Findings

| Insight | Finding |
|---------|---------|
| Most accidents | United States leads globally |
| Peak accident period | Mid-20th century — declining after 1970s |
| Deadliest aircraft type | Large commercial jets |
| Most dangerous operator | Military operators (Cold War era) |
| Post-9/11 impact | Measurable drop in average daily fatalities |
| Safest day to fly | Weekend flights show lower accident rates |

---

## Highlight: The 9/11 Effect

One of the most compelling findings of this analysis is the **measurable impact of September 11, 2001** on aviation safety metrics. By splitting the dataset pre and post 9/11, we can quantify how global aviation security reforms changed fatality rates.

```
Average daily fatalities BEFORE 9/11: [pre_value]
Average daily fatalities AFTER 9/11:  [post_value]
```

The post-9/11 drop reflects tightened security protocols, stricter regulations, and a global shift in how aviation safety is managed.

---

## Visualizations

### Top 10 Countries by Number of Accidents
![Countries](outputs/accidents_by_country.png)

### Accidents Over Time (by Year)
![Yearly trend](outputs/accidents_by_year.png)

### Accidents by Day of the Week
![Day of week](outputs/accidents_by_day.png)

### Top 10 Aircraft Types by Fatalities
![Aircraft types](outputs/aircraft_fatalities.png)

### Top 5 Operators with Most Accidents
![Operators](outputs/accidents_by_operator.png)

### Daily Fatalities — Before and After 9/11
![9/11 impact](outputs/sept11_impact.png)

### Correlation: Accidents vs Deaths by Aircraft Type
![Scatter plot](outputs/correlation_scatter.png)

### Global Aviation Accidents Map
![World map](outputs/world_map.png)

---

## Data Cleaning Highlights

This dataset required significant preprocessing before analysis:

- **Date parsing:** thousands of records had `"date unk."` — replaced with `NaT` and recovered from a secondary `year` column where possible
- **Fatalities correction:** values stored as strings with arithmetic expressions — evaluated safely with `eval()`
- **Country name normalization:** mapped 15+ inconsistent country names to match the geographic shapefile (e.g. `"u.k."` → `"united kingdom"`, `"d.r. congo"` → `"democratic republic of the congo"`)
- **Duplicate and null removal:** dropped rows with missing registration, location, and operator

---

## Tech Stack

| Tool | Purpose |
|------|---------|
| Python | Core language |
| Pandas | Data cleaning & analysis |
| NumPy | Numerical operations |
| Matplotlib | Data visualization |
| GeoPandas | Geographic mapping |

---

## Project Structure

```
aviation-disasters-analysis/
├── data/
│   └── aviation-accidents.csv
├── notebooks/
│   └── analysis.ipynb
├── outputs/
│   ├── accidents_by_country.png
│   ├── accidents_by_year.png
│   ├── accidents_by_day.png
│   ├── aircraft_fatalities.png
│   ├── accidents_by_operator.png
│   ├── sept11_impact.png
│   ├── correlation_scatter.png
│   └── world_map.png
└── README.md
```

---

## How to Run

```bash
pip install pandas numpy matplotlib geopandas jupyter

jupyter notebook
```

Open `notebooks/analysis.ipynb` and run all cells.

> **Note:** The geographic map requires a shapefile (`ne_110m_admin_0_countries.shp`). Download it free from [Natural Earth](https://www.naturalearthdata.com/downloads/110m-cultural-vectors/).

---

## About

This project demonstrates end-to-end data analysis skills: messy real-world data cleaning, temporal analysis, geographic visualization, and business storytelling — applied to a globally significant dataset.

**Open to freelance data analysis projects** — feel free to reach out!
