
# Euro 2024 Football Data Analysis — DSA210 Project

## Project Overview

This project analyzes match data from UEFA Euro 2024 to explore the relationship between attacking actions and scoring potential. Specifically, it investigates whether the number of touches a team makes inside the opponent's penalty box can significantly predict their expected goals (xG). The goal is to identify whether deep attacking presence is more meaningful than conventional metrics like overall possession.

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

The dataset contains match-by-match statistics from the UEFA Euro 2024 tournament. Each row represents a match and includes data for both home and away teams.

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

## Results

- Pearson correlation coefficient (r): 0.67
- p-value: < 0.0001

The analysis shows a statistically significant, strong positive correlation between touches in the opponent's penalty box and expected goals (xG).

## Conclusion

This project provides evidence that deeper attacking metrics like touches in the opposition box are better indicators of scoring potential than general possession statistics. The results suggest that tactical analysis should prioritize where a team has possession, not just how much.

## Future Work

- Compare box touches to actual goals, not just xG.
- Analyze time-dependent box touches (first vs second half).
- Extend model with pressing data or zone 14 entries.
- Explore box touches per pass or per possession as efficiency metrics.

## Final Note

This project applies fundamental data science principles to a real-world problem: understanding football performance. It highlights how asking the right question—and choosing the right variable—can make all the difference.
