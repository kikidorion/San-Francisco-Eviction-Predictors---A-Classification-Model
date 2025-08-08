# San-Francisco-Eviction-Predictors---A-Classification-Model

## 📌 Project Overview
This project analyzes San Francisco eviction notice data to predict which neighborhoods are most at risk of future eviction activity.  
By applying exploratory data analysis (EDA) and predictive modeling, the project aims to identify trends, highlight vulnerable areas, and provide actionable insights for housing policy and advocacy.

## 🎯 Objectives
- Explore eviction trends across time, neighborhoods, and causes.
- Identify key factors influencing eviction rates.
- Build a predictive model to forecast eviction risk by neighborhood.
- Provide data-driven recommendations for targeted policy interventions.

## 📂 Data Sources
- **Eviction Notices Dataset** (San Francisco Open Data Portal)  
  Contains detailed eviction records, including dates, locations, eviction reasons, and outcomes.
- **Geospatial Neighborhood Data**  
  Used to map eviction occurrences by neighborhood boundaries.

---

## 🧠 Project Workflow & Logic

### 1️⃣ Data Loading & Cleaning
- Imported **Eviction_Notices_20250305.csv**.
- Checked for missing values and removed invalid or incomplete records.
- Standardized column names for easier reference.
- Converted date columns to `datetime` format for time-based analysis.

**Why?**  
Clean and consistent data ensures accurate analysis and prevents errors in the predictive modeling phase.

---

### 2️⃣ Feature Engineering
- Extracted **year**, **month**, and **day** from eviction filing dates.
- Grouped eviction reasons into broader categories (e.g., "Owner Move-In", "Breach of Contract", "Nuisance").
- Aggregated eviction counts by **neighborhood** and **time period**.
- Calculated rolling averages to smooth short-term fluctuations.

**Why?**  
Feature engineering enhances the model’s ability to capture seasonality, trends, and underlying neighborhood patterns.

---

### 3️⃣ Exploratory Data Analysis (EDA)
- **Time Trends**: Identified eviction spikes during certain years and months.
- **Neighborhood Impact**: Ranked neighborhoods by historical eviction frequency.
- **Cause Analysis**: Found most common eviction reasons and their distribution over time.
- **Heatmaps**: Visualized correlations between features.

**Why?**  
EDA reveals patterns and relationships that guide both feature selection and policy insights.

---

### 4️⃣ Predictive Modeling
- **Model Used**: Random Forest Classifier (chosen for interpretability and handling of categorical data).
- **Target Variable**: Binary indicator of whether a neighborhood would see above-average eviction counts in a given time period.
- **Training/Test Split**: 80% training, 20% testing.
- **Evaluation Metrics**: Accuracy, Precision, Recall, F1 Score.
- Extracted **feature importance** scores to understand which variables drive predictions.

**Why?**  
Predictive modeling allows us to move beyond descriptive analytics into forward-looking insights.

---

### 5️⃣ Visualization & Interpretation
- **Top Predictors**:  
  - Neighborhood historical eviction rate  
  - Month/seasonality factors  
  - Specific eviction reason categories  
- **Risk Maps**: Displayed neighborhoods color-coded by predicted risk level.
- **Feature Importance Chart**: Ranked key drivers of eviction predictions.

**Why?**  
Clear visuals make findings actionable for policymakers and advocacy groups.

---

## 📊 Key Findings
1. Certain neighborhoods consistently show high eviction risk due to historical trends and seasonal patterns.
2. Month and seasonality play a notable role, with some months historically producing more eviction filings.
3. Specific causes, such as "Owner Move-In" and "Breach of Contract", are strong predictors of future activity.

---

## 💡 Policy Recommendations
- Target eviction prevention programs in **high-risk neighborhoods**.
- Increase tenant legal support during months with historically high eviction filings.
- Focus on eviction causes that drive the majority of predicted cases.

---

## 🚀 How to Run This Project
1. Clone the repository:
   ```bash
   git clone https://github.com/kikidorion/San-Francisco-Eviction-Predictors---A-Classification-Model.git
