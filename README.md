# Retail Therapy & Stress: Does Stress Encourage Shopping?

## Project Overview
This project explores the relationship between stress levels and spending habits to determine if people tend to spend more money when they are stressed. The study analyzes personal shopping behavior and external stress indicators to uncover any correlations between emotional state and consumer behavior.

## Motivation
Retail therapy is often seen as a way to cope with stress, but does stress actually lead to increased spending? This study aims to provide data-driven insights into:
- Whether stress levels influence overall spending behavior
- Which product categories (fashion, beauty, food, etc.) are most impacted
- How external stress indicators (e.g., market volatility) correlate with spending patterns

---
## ❓ Research Questions & Hypotheses

1. **Does an increase in self-reported stress levels correspond to a significant increase in total daily spending?**
   - **H₀ (Null Hypothesis):** Stress levels have no significant effect on daily spending.
   - **H₁ (Alternative Hypothesis):** Higher stress levels are associated with increased daily spending.

2. **Which product categories are most influenced by stress?**

3. **Do external financial stress indicators align with personal spending behavior during stressful periods?**

---

## Data Sources

### 1. Personal Data (Primary Data Collection)
- **Date & Time of Purchase**  
- **Purchase Amount**  
- **Product Category**: `Fashion`, `Beauty`, `Food`, `Entertainment`, `Essentials`  
- **Impulse vs. Planned**: Binary label (`Impulse`, `Planned`)  
- **Shopping Motivation**: `Need-based`, `Stress-based`, `Reward`, `Boredom`, etc.  
- **Stress Level**: Self-reported on a `1–10` scale  
- **Sleep Quality**: Self-rated (optional)  
- **Social Media Use**: Hours per day (optional)  
- **Weather Conditions**: Enriched via API if possible  
- **Day of Week & Time of Day**: Captured automatically  
- **Mood Notes (Optional)**: Brief daily log for qualitative insights  

### 2. Public Data (For Enrichment)
To supplement personal data, external datasets will provide broader context:

- **Retail Therapy Scale Development Studies**
  - Insights from *Retail Therapy: Scale Development* (Kang & Johnson, 2011) on shopping as a mood-alleviating behavior.  
    📄 [Read the study](https://www.researchgate.net/publication/254085102_Retail_Therapy_Scale_Development)
  - Validated survey data distinguishing retail therapy from impulse and compulsive buying.

- **Economic & Consumer Spending Trends**
  - *CES, FRED, World Bank, Statista:* Consumer spending patterns, inflation, and economic indicators.

- **Psychological Studies on Retail Therapy & Stress**
  - Research on shopping as a coping mechanism and its psychological drivers.

- **Stock Market Volatility (Stress Indicator)**
  - *VIX Index, financial reports:* Economic uncertainty’s impact on spending behavior.

---

### 🤖 Machine Learning Models & Evaluation Plan

I plan to use the following models to predict daily spending based on stress levels and contextual features:

- **Linear Regression**
- **Random Forest Regressor**

Model training will include **cross-validation** to avoid overfitting.

#### 📏 Evaluation Metrics

- **R² (Coefficient of Determination)**: Measures how well the model explains the variance in spending  
- **Mean Absolute Error (MAE)**: Shows the average magnitude of prediction errors  
- **Root Mean Squared Error (RMSE)**: Penalizes larger errors more heavily, giving insight into prediction accuracy

Additionally, **feature importance** from tree-based models (like Random Forest) will be analyzed to understand which variables most strongly influence stress-related spending behavior.

---

## Data Collection Plan
✔️ Tracking personal data daily to capture spending habits and stress levels.  
✔️ Categorizing purchases into **fashion, beauty, entertainment, food, and essentials**.  
✔️ Enriching data with economic trends & external financial stress indicators.  
✔️ Performing **Exploratory Data Analysis (EDA)** to identify spending trends during high and low stress periods.  
✔️ Applying **Machine Learning Models** to predict high-stress spending behavior.  

---

## Planned Analysis & Techniques
🔹 **Correlation Analysis:** Checking if higher stress scores correspond with higher spending.  
🔹 **Time-Series Analysis:** Observing trends in spending patterns across different stress levels.  
🔹 **Clustering:** Identifying spending categories most affected by stress.  
🔹 **Hypothesis Testing:** Testing if spending significantly increases on high-stress days.  
🔹 **Predictive Modeling:** Using regression models to predict spending behavior based on stress levels.  

---

## Expected Outcomes
✅ Identify whether stress leads to impulse purchases or increased spending.  
✅ Discover which product categories (**beauty, fashion, food**) are most affected by stress-driven shopping.  
✅ Determine if external stress factors (**economy, stock market**) influence retail therapy trends.  

---

