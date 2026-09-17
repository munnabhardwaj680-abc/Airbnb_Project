# Airbnb Data Analysis & Price Optimization Project

![Airbnb Project Banner](https://raw.githubusercontent.com/airbnb/aerosolve/master/docs/svg/aerosolve_header.svg)

This repository contains a comprehensive data analysis and machine learning project focused on short-term rental listings (Airbnb). The primary objective is to clean raw listing data, conduct exploratory data analysis (EDA) to uncover market trends, and build predictive pricing models to guide property hosts and real estate investors.

---

## Executive Summary & Key Findings

Our evaluation of the rental listing dataset revealed several key drivers impacting pricing, guest satisfaction, and host performance:

### Price Determinants
* **Room Type & Accommodation Capacity:** Entire homes and apartments command a significant price premium over private or shared rooms. Capacity (`accommodates`, `bedrooms`, `bathrooms`) is the strongest linear predictor of price.
* **Geographic Location:** Clustering analysis indicates pricing varies drastically across neighborhoods and proximity to central points of interest or transit hubs.
* **Property Amenities:** Key luxury amenities (e.g., hot tubs, pools, free parking, self check-in) positively correlate with higher daily rates.

### Host Metrics & Reviews
* **Superhost Status:** Superhosts consistently maintain higher review scores (`review_scores_rating`, `review_scores_cleanliness`), slightly higher occupancy rates, and can price properties modestly above market average without sacrificing booking frequency.
* **Review Volume vs. Price:** High-frequency listings tend to be priced competitively within their region, whereas premium luxury listings see fewer total reviews per year.

---

## Repository Structure

```text
├── Airbnb.ipynb / Airbnb.html  # Primary notebook containing raw code, outputs, & visualizations
├── data/                       # Dataset directory (raw and processed CSV files)
├── models/                     # Saved predictive models and scalers
└── README.md                   # Project documentation and summary of findings
