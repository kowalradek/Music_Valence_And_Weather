# 🌍 The Weather Vibe Check: How Climate Shapes the Music We Stream

[![Interactive Tableau Dashboard](https://img.shields.io/badge/Tableau-View_Dashboard-E97627?style=for-the-badge&logo=tableau)](https://public.tableau.com/views/DeosWeatherActaullyChangetheMoodofOurMusic/Dashboard1?:language=en-US&publish=yes&:sid=&:display_count=n&:origin=viz_share_link)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin)(https://www.linkedin.com/in/rados%C5%82aw-kowal-098663300/)

## Project Overview

This full-stack data analytics project explores the hidden relationship between local climate and our listening habits across 20 countries. By building a custom data pipeline to merge Spotify streaming data with historical weather metrics, this project uses **statistical testing (T-Tests & Moderation)** to prove how environmental factors impact the collective "mood" of the music we consume.

### Try the Interactive Dashboard
The final results, including interactive moderation maps and correlation scatter plots, are visualized in Tableau.

 <img width="740" height="1012" alt="tableau_image" src="https://github.com/user-attachments/assets/bd02f04c-5e26-435f-9ef3-a63f0e9aa92b" />
---

## Key Insights & Findings
1. **The Rain Paradox:** Contrary to popular belief, precipitation does *not* make us listen to sad music. An independent T-test ($p < 0.0001$) confirmed that listeners actually stream slightly **happier music** on rainy days (0.0532 valence) compared to dry days (0.0483)—likely using upbeat tracks to "brighten" the gray weather.
2. **The Sunshine Effect:** Both temperature and sunshine showed a negative correlation with valence. As days get hotter and sunnier, listeners tend to stream more melancholic music.
3. **Geographic Moderation:** A moderation analysis revealed that the weather's impact is not universal. Geography strongly moderates the "weather-to-mood" relationship—meaning a sunny day impacts music choices differently depending on a country's baseline climate and latitude.

---

## Data Architecture & Pipeline
This project required combining static datasets with live API calls to build a comprehensive analytical view.

* **Base Data:** Spotify Top 200 Charts (Sourced via Kaggle). **[Click here for it](https://www.kaggle.com/datasets/dhruvildave/spotify-charts)**
* **Audio Features Enrichment:** Utilized the **Last.fm API** to extract specific audio features, to get valence **Valence** (the musical positiveness conveyed by a track, scored 0.0 to 1.0).
* **Weather Data Extraction:** Polled the **Meteo API** to pull historical daily weather metrics (Temperature, Sun Hours, Rain Mm) for the capital cities of the 20 European countries analyzed.
* **Data Cleaning & Merging:** Handled in Python using `pandas`, ensuring dates and regions aligned perfectly across all three data sources.

---

## Methodology & Tech Stack
* **Language:** Python 3
* **Libraries:** `pandas`, `requests` (API handling), `scipy` / `statsmodels` (Statistical testing)
* **Visualization:** Tableau Public
* **Statistical Methods Used:**
  * Correlation Coefficients (Pearson)
  * Independent T-Tests
  * Moderation Analysis

