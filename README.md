
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

To evaluate the core hypothesis — that touches in the opponent’s penalty box correlate with expected goals (xG) — several statistical tests were performed:

- A **strong and statistically significant** positive correlation was found between box touches and xG:  
  **Pearson r = 0.67**, **p < 0.01**

- Alternative variables were also tested for correlation with xG, but none showed statistical significance:
  - **Accurate passes** → r = -0.17, p = 0.088
  - **Pass accuracy percentage vs. open play xG** → r = -0.14, p = 0.156

These results suggest that general passing statistics do not meaningfully predict xG. A correlation heatmap further confirmed that **box touches** had the strongest relationship with xG among the tested variables.

---

## Conclusion

This project provides evidence that **deeper attacking metrics**, such as touches in the opposition penalty area, are stronger indicators of scoring potential (xG) than general possession or passing accuracy.

While traditional metrics like accurate passes or pass percentage may reflect a team’s control of the ball, they did not correlate with the quality of scoring opportunities. This highlights the importance of **positional context** in modern football analytics: it’s not about how much possession a team has, but **where** and **how** they use it.

The findings support a shift in focus from surface-level stats toward metrics that capture **attacking intent and territorial advantage**.

## Future Work

There are several directions in which this analysis could be expanded or refined:

- **Include additional contextual metrics:** Incorporating pressing data, zone 14 entries, or progressive passes could provide deeper insights into xG generation patterns.
- **Analyze temporal trends:** Comparing xG and box touches across match periods (first vs. second half) might reveal tactical or stamina-related effects.
- **Efficiency analysis:** Calculating metrics like xG per box touch or xG per possession could help evaluate how efficiently teams convert attacking presence into quality chances.
- **Team or match-up level modeling:** Exploring how different teams generate or concede xG based on their play styles could add a comparative dimension.
- **Expand the dataset:** Applying the same methodology to domestic leagues or other international tournaments could test the generalizability of the findings.

These extensions would not only validate the current insights but also help build more robust models for predicting scoring potential in football.


## Final Note

This project applies fundamental data science principles to a real-world problem: understanding football performance. It highlights how asking the right question—and choosing the right variable—can make all the difference.
