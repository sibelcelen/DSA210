# Retail Therapy & Stress: Does Stress Encourage Shopping?

## Project Overview
This project explores the relationship between stress levels and spending habits to determine if people tend to **spend more money when they are stressed**. The study analyzes *personal shopping behavior* and *external stress indicators* to uncover any correlations between emotional state and consumer behavior.

## Motivation
Retail therapy is often seen as a way to cope with stress, but does stress actually lead to increased spending? This study aims to provide data-driven insights into:
- Whether stress levels influence overall spending behavior
- Which product categories (fashion, beauty, food, etc.) are most impacted
- How external stress indicators (e.g., market volatility) correlate with spending patterns

---
##  Research Questions & Hypotheses

1. **Does an increase in self-reported stress levels correspond to a significant increase in total daily spending?**
   - **H₀ (Null Hypothesis):** Stress levels have no significant effect on daily spending.
   - **H₁ (Alternative Hypothesis):** Higher stress levels are associated with increased daily spending.

2. **Which product categories are most influenced by stress?**

3. **Do external financial stress indicators align with personal spending behavior during stressful periods?**

---

## Data Sources

### 1. Personal Data (Primary Data Collection)
- **Date of Purchase**  
- **Purchase Amount**  
- **Product Category**: `Fashion`, `Beauty`, `Food`, `Entertainment`, `Essentials`  
- **Impulse vs. Planned**: Binary label (`Impulse`, `Planned`)  
- **Shopping Motivation**: `Need-based`, `Stress-based`, `Reward`, `Boredom`, etc.  
- **Stress Level**: Self-reported on a `1–10` scale  
- **Sleep Quality**: Self-rated (optional)  
- **Social Media Use**: Hours per day (optional)  
- **Weather Conditions**: Enriched via API if possible  
- **Day of Week & Time of Day**: Captured automatically  
- **Notes (Optional)**: Extra note if necessary  

### 2. Public Data (For Enrichment)
To supplement personal data, external datasets will provide broader context:

- **Retail Therapy Scale Development Studies**
  - Insights from *Retail Therapy: Scale Development* (Kang & Johnson, 2011) on shopping as a mood-alleviating behavior.  
    📄 [Read the study](https://www.researchgate.net/publication/254085102_Retail_Therapy_Scale_Development)
  - Validated survey data distinguishing retail therapy from impulse and compulsive buying.

---

###  Machine Learning Models & Evaluation Plan

I plan to use the following models to predict daily spending based on stress levels and contextual features:

- **Linear Regression**
- **Random Forest Regressor**

Model training will include **cross-validation** to avoid overfitting.

####  Evaluation Metrics

- **R² (Coefficient of Determination)**: Measures how well the model explains the variance in spending  
- **Mean Absolute Error (MAE)**: Shows the average magnitude of prediction errors  
- **Root Mean Squared Error (RMSE)**: Penalizes larger errors more heavily, giving insight into prediction accuracy

Additionally, **feature importance** from tree-based models (like Random Forest) will be analyzed to understand which variables most strongly influence stress-related spending behavior.

---

## Data Collection Plan
- Tracking personal data daily to capture spending habits and stress levels.  
- Categorizing purchases into **fashion, beauty, entertainment, food, and essentials**.  
- Enriching data with economic trends & external financial stress indicators.  
- Performing **Exploratory Data Analysis (EDA)** to identify spending trends during high and low stress periods.  
- Applying **Machine Learning Models** to predict high-stress spending behavior.  

---

## Planned Analysis & Techniques
- **Correlation Analysis:** Checking if higher stress scores correspond with higher spending.  
- **Time-Series Analysis:** Observing trends in spending patterns across different stress levels.  
- **Clustering:** Identifying spending categories most affected by stress.  
- **Hypothesis Testing:** Testing if spending significantly increases on high-stress days.  
- **Predictive Modeling:** Using regression models to predict spending behavior based on stress levels.  

---

## Expected Outcomes
- Identify whether stress leads to impulse purchases or increased spending.  
- Discover which product categories (**beauty, fashion, food**) are most affected by stress-driven shopping.  
- Determine if external stress factors (**economy, stock market**) influence retail therapy trends.  

---

# Phase 2 Insights
##  Hypothesis Testing

The dataset includes variables such as stress level, sleep quality, shopping behavior, impulse/planned purchase type, social media usage, and weather.

---

### 🔹 H1: People are more likely to shop when they are under higher stress.

**Test Used**: Independent t-test  
**Variables**:  
- Group 1: Stress Level on shopping days (`Shopping? = YES`)  
- Group 2: Stress Level on non-shopping days (`Shopping? = NO`)

**Result**:  
`t = 2.31`, `p = 0.027` ✅

**Interpretation**:  
Since *p < 0.05*, we reject the null hypothesis. People tend to experience **higher stress on shopping days**, suggesting that shopping is used as a **coping mechanism for stress**.

---

### 🔹 H2: Impulse shopping is more common on high-stress days compared to planned shopping.

**Test Used**: Independent t-test  
**Variables**:  
- Group 1: Stress Level on `IMPULSE` shopping days  
- Group 2: Stress Level on `PLANNED` shopping days

**Result**:  
`t = 2.75`, `p = 0.011` ✅

**Interpretation**:  
Since *p < 0.05*, the result is statistically significant. Stress levels are **significantly higher** on impulse shopping days, supporting the idea that **unplanned purchases are emotionally driven**.

---

### 🔹 H3: Weather conditions influence shopping behavior.

**Test Used**: Chi-square test of independence  
**Variables**:  
- `Weather` (e.g., Sunny, Rainy, Cloudy)  
- `Shopping?` (YES/NO)

**Result**:  
`p = 0.218` ❌

**Interpretation**:  
Since *p > 0.05*, there is **no statistically significant relationship** between weather and shopping frequency. While cloudy or rainy days might feel like triggers, the data does **not support this assumption** statistically.

---

### 🔹 H4: Social media usage negatively impacts sleep quality.

**Test Used**: Pearson correlation  
**Variables**:  
- `Social Media Use (h)`  
- `Sleep Quality`

**Result**:  
`r = -0.38`, `p = 0.042` ✅

**Interpretation**:  
There is a **moderate negative correlation**, meaning **more social media use is linked to lower sleep quality**. This may contribute indirectly to stress and emotional shopping patterns.

---

### ✅ Summary Table

| Hypothesis                               | Test       | p-value | Result           | Interpretation                              |
|------------------------------------------|------------|---------|------------------|----------------------------------------------|
| H1: Stress ↑ → Shopping ↑                | t-test     | 0.027   | ✅ Significant    | Shopping is linked to high stress            |
| H2: Stress ↑ → Impulse > Planned         | t-test     | 0.011   | ✅ Significant    | Impulse purchases are stress-driven          |
| H3: Weather ↔ Shopping                   | Chi-square | 0.218   | ❌ Not Significant| Weather doesn't significantly affect shopping|
| H4: Social Media ↑ → Sleep ↓             | Pearson r  | 0.042   | ✅ Significant    | More social = worse sleep quality            |

