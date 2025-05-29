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

## 🧪 Hypotheses

- **H₀**: There is no relationship between box touches and xG.
- **H₁**: More touches in the opponent's box → higher expected goals.

Additionally:

- As **pass accuracy decreases**, do teams rely more on **open play xG**?
- Does **possession** lead to more **box entries**?

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

