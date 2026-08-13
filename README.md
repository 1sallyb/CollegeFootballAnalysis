# SEC Home-Field Advantage Analysis
## Overview
This project analyzes whether home-field advantage had a measurable effect on game outcomes during the **2024 SEC football season**.

This analysis examines whether SEC home teams:
  * Won games at a higher rate than away teams
  * Had a positive average point differential
  * Showed statistically significant evidence of home-field advantage
  * Experienced different levels of home-field advantage across teams

This project includes data collection, data cleaning, exploratory analysis, statistical testing, and interpretation of results.

## Research Questions
The analysis addresses three primary questions:
  1. **Did SEC home teams have a significantly higher win percentage during the 2024 season?**
  2. **Was the average point differential between home and away teams significantly greater than zero?**
  3. **How did home-field advantage vary among SEC teams?**

## Data
The original dataset was obtained from <CollegeFootballData.com> using its API and saved locally as a CSV file.
The dataset was then filtered to include only the variables needed for this analysis.

The final dataset consists of **53 SEC games** from the 2024 season and includes variables such as:
  * Home Team
  * Away Team
  * Game Date
  * Game Location
  * Home Team Score
  * Away Team Score
  * Home-Team Win Indicator
  * Point Differential

Two primary measures of home-field advantage are used throughout the analysis:
  * **Home Win**: Whether the home team won the game
  * **Point Differential**: Home team points - Away team points

## Methodology
The analysis follows several steps:
  1. **Data Cleaning**: The raw data was examined and prepared for analysis.
  2. **Exploratory Analysis**: Home and away performance was summarized and visualized to identify patterns in the data.
  3. **Statistical Testing**: Statistical tests were used to determine whether the observed differences in home-team performance were statistically significant.
  4. **Team-level analysis**: Home-field advantage was compared across SEC teams to identify differences between programs.

## Results
  1. **Home Win Percentage**: SEC home teams won **60.4%** of games during the 2024 season. A one-sample proportion test was used to evaluate whether the home-team win rate differed from 50%. The test produced a **p-value of 0.065**, which was above the 0.05 significance threshold. The 95% confidence interval was **0.491-1.000**. **Conclusion**: The result did not provide sufficient evidence at the 0.05 significance level to conclude that SEC home teams won more than 50% of their games. However, the result suggests a possible trend toward home-field advantage that could be investigated further with a larger sample.
  2. **Mean Point Differential**: Home teams had an average point differential of **+2.06 points**, meaning they scored slightly more points than their opponents on average. A one-sample t-test was used to determine whether the average point differential differed significantly from zero. The test produced a **t-statistic of 0.86** and a **p-value of 0.196**. **Conclusion**: Although home teams scored an average of 2.06 more points, the difference was not statistically significant. The analysis therefore does not provide sufficient evidence that SEC home teams systematically outscored away teams during the 2024 season.
  3. **Differences Across SEC Teams**: A one-way ANOVA was used to determine whether average home-team point differential differed among SEC teams. The analysis found a statistically significant overall difference: **F = 2.06, p = 0.039**. **Conclusion**: Average home-team point differential varied significantly across SEC teams, suggesting that home-field performance was not uniform throughout the conference.
  4. **Tukey HSD Post-Hoc Analysis**: Because the ANOVA identified an overall difference between groups, a Tukey HSD post-hoc test was performed to determine which teams differed from one another. No individual pairwise comparison was statistically significant after adjusting for multiple comparisons (**all adjusted p-values > 0.05**). **Conclusion**: Although the ANOVA provides evidence of overall variation among teams, the post-hoc analysis did not identify a specific pair of teams with statistically significant differences in home-field advantage. 

## Visualizations
### Home-Team Win Rate
The home team won 60.4% of SEC games during the 2024 season.

### Average Point Differential
Home teams had an average point differential of +2.06 points.

### Home-Field Advantage by Team
Average point differential varied across SEC teams, with the overall ANOVA indicating statistically significant differences between groups.

## Tools & Technologies
  * R
  * Data Visualization
  * Statistical Analysis
  * CollegeFootballData API
  * RStudio

## Project Structure
```text
CollegeFootballAnalysis/
├── README.md
├── data/
│   ├── games_2024.csv
│   └── sec_2024_clean.csv
├── analysis/
│   ├── final.qmd
│   ├── results.qmd
│   ├── sec_setup.Rmd
│   └── setup.Rmd
└── images/
    ├── home_win_rate.png
    ├── point_differential.png
    └── team_home_advantage.png

## Future Improvements
Potential improvements to this analysis include:
  * Expanding the analysis to multiple SEC seasons
  * Comparing the SEC with other conferences
  * Controlling for team strength and rankings
  * Examining home-field advantage by stadium
  * Incorporating factors such as attendance, travel distance, and weather
  * Using a larger dataset to improve statistical power

## Conclusion
This project demonstrates a data-analysis workflow using real-world sports data, including data collection, cleaning, exploratory analysis, statistical testing, visualization, and interpretation. The analysis provides a quantitative assessment of whether home-field advantage was evident during the 2024 SEC football season. 
