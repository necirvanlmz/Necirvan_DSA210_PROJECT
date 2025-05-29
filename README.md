# ⚽ Football Data Analytics — DSA210 Final Project

## 🧠 Overview

This project investigates the relationship between offensive football statistics and expected goals (xG) by analyzing Euro 2024 match data and full-season Süper Lig team stats. 

Using tools and techniques from the DSA210 course, we tested football-specific hypotheses and applied machine learning to uncover insights into modern football tactics.

---

## 🎯 Objectives

- Explore the correlation between **touches in the opponent’s box** and **xG**.
- Analyze whether **pass accuracy** affects reliance on **open play vs set piece** xG.
- Apply **linear regression**, **decision trees**, and **random forests** to model xG.
- Use **K-means clustering** to identify team profiles based on key features.

---

## 📦 Datasets

- **Euro 2024 Match Statistics**: Game-by-game performance data for both home and away teams.
- **Süper Lig 2023–24 Season Statistics**: Aggregated per-match data for each team.

After cleaning and merging, home and away teams were combined into a single structure (`combined_df`) for Euro 2024. The Süper Lig data was used as-is (`superlig_df`).

---

## 🎯 Hypothesis Testing Summary

### ⚽ 1. Box Touches vs. xG
- **H₀:** There is no correlation between touches in the opponent’s box and xG.  
- **H₁:** There is a positive correlation between touches in the opponent’s box and xG.

✅ **Result:** A moderate positive correlation was found.  
📈 **Implication:** Teams entering the opponent’s box more frequently tend to generate more xG.

---

### 🎯 2. Pass Accuracy vs. Open Play xG
- **H₀:** There is a positive correlation between pass accuracy and open play xG.  
- **H₁:** There is no correlation between pass accuracy and open play xG.

❌ **Result:** No statistically significant correlation found.  
📉 **Implication:** High pass accuracy alone does not lead to better scoring opportunities unless it results in high-quality offensive actions.

---

### 🔁 3. Possession vs. Box Entries
- **H₀:** Possession percentage has no correlation with box entries.  
- **H₁:** Higher possession percentages are correlated with increased box entries.

✅ **Result:** Strong, statistically significant correlation found in Süper Lig data.  
🔎 **Implication:** Dominating possession increases the likelihood of entering the opponent's penalty area.

---

### 🧩 4. Pass Accuracy vs. xG Source Ratio
- **H₀:** Pass accuracy does not affect the ratio of open play xG to set piece xG.  
- **H₁:** Lower pass accuracy leads to a higher share of xG from open play compared to set pieces.

⚠️ **Result:** A weak negative trend was observed, but it was not statistically significant.  
🤔 **Implication:** There may be a tendency for teams with lower pass accuracy to rely more on open play, though more data is needed to support this claim.

---

## 🛠️ Tools & Libraries

- `Python`, `Pandas`, `Seaborn`, `Matplotlib`, `SciPy`, `Scikit-learn`
- Jupyter Notebook (data manipulation, ML, and visualizations)

---

## 🔍 Exploratory Analysis & Correlations

### 📈 Core Relationship

- **Box Touches vs xG** (Euro 2024):  
  **Pearson r = 0.67**, **p < 0.001** → Strong positive relationship ✅

### 📊 Extended Results

| Relationship                              | Pearson r | p-value | Conclusion                                        |
|-------------------------------------------|-----------|---------|---------------------------------------------------|
| Accurate Passes vs xG                     | -0.17     | 0.088   | Not statistically significant ❌                  |
| Pass Accuracy % vs Open Play xG           | -0.14     | 0.156   | Not statistically significant ❌                  |
| Possession % vs Box Entries (Süper Lig)   | 0.76      | 0.0001  | Strong, significant positive correlation ✅        |
| Pass Accuracy % vs Open/Set xG Ratio      | -0.18     | 0.0741  | Weak negative trend, not significant 🤏            |

---

## 💡 Summary of Insights

- ✅ **Box touches** are a reliable predictor of xG.
- ❌ High **pass accuracy** doesn’t directly translate into more goals.
- ⚽ **Possession** helps create access to danger zones (box entries).
- 🔄 Teams with **lower pass accuracy** may depend more on open play xG than set pieces.

---

### 🧠 Prediction Approach

In the final phase of the project, both **Linear Regression** and **Random Forest Regression** models were implemented to predict teams’ **expected goals (xG)** based on selected match statistics.

📌 **Features Used**:
- Possession Percentage (`possession_percentage`)
- Touches in Opposition Box (`encounters_in_opponent_box`)
- Accurate Passes Per Match (`accurate_passes_per_match`)
- Big Chances Created (`big_chances_created`)

These features were selected after performing correlation analyses, which indicated a strong positive relationship between **possession percentage and box touches** (Pearson r ≈ 0.76). This suggests that ball control and penetration are reliable indicators of attacking efficiency.

🧪 **Models Trained**:
- **Linear Regression**: Provided a baseline performance with R² scores indicating moderate predictive power.
- **Random Forest Regression**: Improved prediction accuracy by capturing non-linear relationships between features and xG.

🎯 **Goal**: To assess whether these match statistics can meaningfully estimate a team's attacking output in terms of xG, and to explore the predictive potential of football data.

While the models had room for improvement, this phase demonstrated that predictive modeling is a feasible and valuable direction for future work.


## 🤖 Machine Learning Models

### 📌 Süper Lig: Predicting xG
**Features**: possession %, box touches, accurate passes, big chances  
**Models Used**:
- Linear Regression → `R² = 0.85`
- Decision Tree Regressor → captured non-linear patterns
- Random Forest → improved accuracy with `R² ≈ 0.92`


## 🔍 Clustering Analysis (K-Means)

Teams were grouped based on `accurate_passes`, `box_touches`, and `xG`.  
K-Means with 5 clusters showed tactical diversity — from possession-heavy to counter-attacking styles.

🟡 Yellow cluster centers highlighted different play styles in visualizations.

---

## 📸 Visualizations

- Correlation heatmaps
- Regression plots with confidence intervals
- Clustering scatterplots (with K-means centers)
- Barplots of predicted vs actual xG

---

## ✅ Conclusion

This project confirms that **spatial metrics** such as **box entries** are more indicative of performance than basic passing stats.  
Data-driven football analysis should prioritize **zone penetration**, not just **possession volume**.

---

## 🔮 Future Work

- 🧱 Add **tactical features** (e.g., key passes, zone 14 entries).
- 🌍 Compare across **leagues** and **tournaments**.
- 🔄 Include **defensive metrics** (xGA, blocked shots).
- 📈 Train **predictive models** for match outcomes using engineered features.
- 🧠 Apply **clustering** on multi-league data for team profiling.

---

> — Project by Neçirvan Yılmaz | Sabancı University Industrial Engineering

