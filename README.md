
# Football Data Analysis — DSA210 Project

## Project Overview

Over the course of this project, I explored how various offensive football statistics relate to expected goals (xG). Specifically, I analyzed whether the number of touches inside the opponent's box, passing accuracy, and possession metrics could predict xG performance.

The main goal was to test a football-based hypothesis using real match data from Euro 2024 and the 2023–24 Süper Lig season, applying data science techniques learned in the DSA 210 course. Through data cleaning, visualization, and statistical analysis, I aimed to discover actionable insights into modern football tactics.

## Objectives

- Test whether touches in the opponent’s penalty box correlate with expected goals.
- Understand the efficiency of attacking presence.
- Apply data science techniques to real-world football data.
- Support findings with statistical analysis and visualizations.

## Motivation

Modern football is increasingly shaped by advanced metrics like expected goals (xG) and positional play. However, traditional statistics like total possession often lack context. This project attempts to go deeper by asking:

- Does entering the opponent's penalty area lead to higher-quality chances?
- Can box touches serve as a predictor of xG?
- What tactical insight does this offer?

## Dataset

The project utilized two main datasets:

**Euro 2024 Match Statistics**
Including detailed match stats such as touches in opposition box, xG (open play and set piece), passes, and passing accuracy.

**2023–24 Süper Lig Season Statistics**
Covering full-season team statistics: points per match, possession percentage, box entries, and more.

Each dataset was cleaned and merged to allow home and away teams to be treated uniformly.
### Key features used:

- Expected goals (xG)
- Touches in opposition box
- Shots inside and outside the box
- Big chances
- Goals scored
- Pass accuracy and total passes
- Dribbles and defensive actions

Missing values were handled through filtering, and home/away team stats were combined into a unified structure for comparison.

## Hypothesis

- H₀ (Null Hypothesis): There is no significant relationship between touches in the opponent's penalty box and expected goals (xG).
- H₁ (Alternative Hypothesis): Teams with more touches in the opponent's penalty box generate significantly higher expected goals (xG).

## Tools and Technologies

- Python
- Pandas
- Matplotlib and Seaborn
- SciPy (Pearson correlation)
- Jupyter Notebook

## Analysis Steps

1. **Data Cleaning:** Removed missing values and standardized relevant columns.
2. **Feature Engineering:** Combined home and away stats into a single DataFrame.
3. **Visualization:** Created scatter plots with regression lines and correlation heatmaps.
4. **Statistical Testing:** Applied Pearson correlation test.

## Key Results and Findings
**Core Analysis**
- Opponent Box Touches vs xG

-  Pearson r = 0.67, p < 0.001
-  Strong positive and statistically significant relationship.
-  Conclusion: More touches inside the box reliably predict higher xG.

## Extended Analyses

| Relationship                               | Pearson r | p-value | Conclusion                                    |
|--------------------------------------------|-----------|---------|-----------------------------------------------|
| Accurate Passes vs xG                      | -0.17     | 0.088   | No significant relationship                   |
| Pass Accuracy % vs Open Play xG           | -0.14     | 0.156   | No significant relationship                   |
| Possession % vs Box Entries (Süper Lig)   | 0.76      | 0.0001  | Strong, significant positive relationship     |
| Pass Accuracy % vs Open/Set xG Ratio      | -0.18     | 0.0741  | Weak negative trend (not statistically significant) |


### Summary of Insights

- ✅ **Touches in the opponent's box** are the most reliable indicator of xG generation.
- ❌ **High passing accuracy alone** does not necessarily lead to better scoring chances.
- ⚽ **Higher possession percentages** help teams gain more access to dangerous zones (box entries).
- 🔄 **Teams with lower pass accuracy** may lean slightly more on open play chances rather than set pieces, but more data is needed to confirm this trend.

  

## 📊 Results

The analysis focused on exploring the statistical relationships between key football performance metrics and expected goals (xG). The primary hypothesis was confirmed with strong support, and additional metrics were evaluated for their impact on xG.

## ✅ Conclusion

This project confirmed that touches inside the opponent’s penalty area are a strong predictor of a team’s expected goals (xG). While commonly referenced metrics like accurate passes and pass accuracy did not correlate significantly with xG, spatial dominance — reflected in metrics like box entries — proved to be far more meaningful.

The findings suggest that modern football analytics should shift the emphasis from possession volume and passing percentages toward positional context and offensive penetration. Teams that are able to enter dangerous zones are consistently more likely to generate high-quality chances, regardless of how clean their passing game appears.

---

## 🔮 Future Work

- **Include more tactical variables** such as progressive passes, key passes, and pressing intensity.
- **Incorporate zone-based data** (e.g., final third passes, zone 14 entries) for deeper spatial analysis.
- **Compare across leagues and tournaments** to evaluate whether these trends are universal or context-dependent.
- **Build predictive models** using features like box touches and possession zones to estimate xG or match outcomes.
- **Investigate defensive metrics** such as xGA and blocked shots to understand xG suppression strategies.
