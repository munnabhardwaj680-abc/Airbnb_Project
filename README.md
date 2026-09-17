# 🏡 Airbnb Data Analysis & Visualization Project

An end-to-end Exploratory Data Analysis (EDA) of Airbnb listings dataset using Python, Pandas, Seaborn, and Matplotlib. This project performs data cleaning, handles missing values and data type conversions, removes duplicate entries, and identifies key insights across listing prices, room types, and geographical locations.
![Airbnb Seattle](seattle.jpg)

---

## 📌 Table of Contents
- [Project Overview](#-project-overview)
- [Dataset Features](#-dataset-features)
- [Key Data Cleaning Steps](#-key-data-cleaning-steps)
- [Exploratory Data Analysis (EDA) & Insights](#-exploratory-data-analysis-eda--insights)
- [Installation & Setup](#-installation--setup)
- [Project Structure](#-project-structure)
- [Future Improvements](#-future-improvements)

---

## 🔍 Project Overview

The primary goal of this project is to clean, analyze, and visualize Airbnb listing data to understand pricing distributions, geographical room availability, and customer behavior patterns over time.

**Key Objectives:**
- Clean raw tabular data (handle mixed data types, missing records, currency symbols).
- Analyze listing price distributions across different accommodation types.
- Evaluate the concentration of listings across major neighborhood groups.
- Visualize review trends over time.

---

## 📊 Dataset Features

The raw dataset contains **102,599 records** across **26 columns**:

| Column Name | Description | Data Type |
| :--- | :--- | :--- |
| `id` / `host id` | Unique identifiers for listings and hosts | Integer |
| `NAME` / `host name` | Name of the listing and host | Object (String) |
| `neighbourhood group` | Broad geographic region (e.g., Brooklyn, Manhattan) | Object (String) |
| `neighbourhood` | Specific local neighborhood | Object (String) |
| `room type` | Entire home/apt, Private room, Shared room, Hotel room | Object (String) |
| `price` | Nightly rate in USD | Float (Cleaned) |
| `service fee` | Additional Airbnb service charge | Float (Cleaned) |
| `minimum nights` | Minimum length of stay required | Float |
| `number of reviews` | Total reviews received | Float |
| `last review` | Date of the most recent review | Datetime |
| `availability 365` | Days available per year | Float |

---

## 🧹 Key Data Cleaning Steps

1. **Date Standardisation:** Converted `last review` to `datetime` objects and imputed missing dates using baseline values.
2. **Handling Missing Values:** Dropped unidentifiable rows where `NAME` or `host name` were missing, and removed non-essential high-null columns (`license`, `house_rules`).
3. **Currency Conversion:** Removed `$` currency signs and commas from `price` and `service fee` columns, converting them to numerical floats.
4. **Deduplication:** Dropped duplicate records, reducing the dataset size to **101,410 clean records**.

---

## 📈 Exploratory Data Analysis (EDA) & Insights

### Key Visualizations & Questions Explored:
* **Q1. Price Distribution:** Analyzed overall price distributions using histograms and KDE plots. Listings exhibit a fairly uniform distribution ranging from $50 to $1,200 per night.
* **Q2. Room Type Distribution:** Entire homes/apartments (~53k) and Private rooms (~46k) dominate the market, making up over 97% of total inventory.
* **Q3. Neighborhood Group Volume:** **Manhattan** and **Brooklyn** represent over 83% of all Airbnb listings in the dataset.
* **Q4. Price vs. Room Type:** Analyzed price distributions across room types using box plots.
* **Q5. Review Trends Over Time:** Tracked customer activity over time by grouping review timestamps on a monthly basis.

---
