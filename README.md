# Advertisement_Analysis


## 📊 Ad Analytics Data Insights

This project explores digital advertisement performance by analyzing cost efficiency and predicted click-through rates (CTR) across various ad categories, types, and formats. The goal is to derive actionable insights that can guide strategic ad placement and budgeting decisions.

---

## 📁 Dataset Overview

- **Source**: Simulated Ad Analytics dataset from an online ad platform
- **Records**: 12,000 rows × 8 columns
- **Attributes**:
  - `uniqueId`: Unique ad identifier
  - `date`: Date of ad activity
  - `tag`: Ad placement type (Banner, InApp, Interstitial)
  - `sub_type`: Ad category (e.g., Finance, Games, E-commerce)
  - `type`: Format (Native, non-Native)
  - `rating`: Content rating (PG-13, PG-17, R)
  - `cost`: Ad cost in USD
  - `predicted_ctr`: Predicted click-through rate

---

## 🔧 Data Preprocessing

- **Loaded using**: `read.csv()` in R
- **Missing values handled**:
  - `cost` & `predicted_ctr`: Filled using **median**
  - `rating`: Filled using **mode**
  - `date`: Imputed with placeholder value `"2024-01-01"`
- **Type conversions**: Dates converted to proper `Date` format

---

## 📊 Visualizations & Key Insights

### 🔹 Bar Plot – Average Ad Cost by Subcategory
- High-cost categories likely offer better ROI; Social Media and Travel are cost-effective for awareness campaigns.

### 🔹 Boxplot – CTR Distribution by Rating
- PG-13 and PG-17 ratings show consistent performance; R-rated ads are highly variable. Safer campaigns may prefer PG-13/PG-17 ads; R-rated ads are riskier but could be high-reward.

### 🔹 Line Plot – Ad Price vs Ad Volume
- Ad frequency drops as cost increases, suggesting rare but expensive premium placements.

### 🔹 Pie Chart – Ad Category Share
- Finance and Games dominate ad volume, indicating strong advertiser interest.

### 🔹 Scatter Plot – CTR vs Cost by Ad Type
- Non-Native ads outperform Native ads at similar costs in terms of CTR.

### 🔹 Histogram – Cost Distribution by Ad Type
- Non-Native ads are concentrated in the lower cost range ($3–$8), offering cost-efficiency.

### 🔹 Heatmap – CTR by Rating and Type
- Non-Native ads consistently show higher average CTRs across all content ratings.

---

## 📚 Tech Stack

- **Language**: R
- **Libraries**: `ggplot2`, `dplyr`, `lubridate`
- **Visualization**: Boxplots, Bar charts, Pie charts, Heatmaps, Scatter plots
