# DSA210 Project
## Single-player vs Multiplayer Games: A Data-Driven Comparative Analysis
## 1. Motivation

The gaming industry has increasingly shifted toward multiplayer-focused titles, with live-service and online competitive games dominating market trends. Despite this, single-player games continue to receive critical acclaim and maintain a loyal audience.
The goal of this project is to investigate whether multiplayer games truly outperform single-player titles in terms of global sales, using publicly available data and statistical analysis.

## 2. Research Question

Do multiplayer games achieve significantly higher global sales compared to single-player games?

## 3. Hypothesis

Null Hypothesis (H₀):
There is no significant difference in mean global sales between multiplayer and single-player games.

Alternative Hypothesis (H₁):
Multiplayer games have significantly higher global sales than single-player games.

This hypothesis is tested using descriptive statistics, visual exploration, and statistical hypothesis testing.

## 4. Dataset Description

This project uses a single publicly available dataset, enriched through additional feature engineering:

VGChartz Video Game Sales Dataset (Kaggle)

URL: https://www.kaggle.com/datasets/gregorut/videogamesales

### Contains:

Game titles

Platform

Release year

Genre

Publisher

Regional and global sales

Why a Single Dataset?

Project guidelines state that publicly available datasets must be enriched if used alone.
To satisfy this requirement, extensive feature engineering was performed.

## 5. Feature Engineering (Enrichment)

The original dataset includes basic attributes, mainly sales and platform information.
To enhance its analytical value, the following new variables were created:

## 1. Sales Category (sales_cat)

Categorized global sales into:

low (<1M)

mid (1–5M)

high (>5M)

## 2. Decade (decade)

Extracted from release year:
e.g., 1980s, 1990s, 2000s.

## 3. Platform Family (platform_family)

Mapped each platform into broader families:

PlayStation

Nintendo

Xbox

PC

Other

## 4. Game Type (game_type)

Estimated whether a game is primarily multiplayer or single-player based on its genre category:

sports, racing, shooter, fighting → multiplayer

other genres → single-player

## 5. Simplified Genre (genre_simple)

Reduced detailed genres into:

Action

Combat

Competitive

Strategy

Story Driven

These engineered features allowed richer analysis and supported valid statistical testing.

## 6. Exploratory Data Analysis (EDA)

EDA was conducted through visualizations such as:

Genre distribution

Global sales by platform family

Sales comparison between single-player and multiplayer games

Global sales trend across decades

These plots provided initial insight into overall market dynamics and differences across game categories.

## 7. Hypothesis Testing

A Welch two-sample t-test was performed to compare mean global sales between multiplayer and single-player games.

Results

t-statistic: 3.27

p-value: 0.0010

Interpretation

Since p < 0.05, the null hypothesis is rejected.
There is significant statistical evidence that:

Multiplayer games sell more, on average, than single-player games.

This supports the idea that the industry shift toward multiplayer-oriented games aligns with consumer purchasing behavior.

## 8. Tools and Libraries

Python

pandas, numpy

seaborn, matplotlib

scipy (statistical tests)

Jupyter Notebook

GitHub for version control

## 9. Project Structure
DSA210-Project/
 data/vgsales.csv
 notebooks/02_analysis.ipynb
 scripts/
 README.md
 requirements.txt

## 10. Conclusion

The analysis demonstrates that multiplayer games achieve significantly higher global sales compared to single-player games. Although single-player titles remain influential and critically acclaimed, market data suggests that multiplayer experiences are currently more commercially successful.

The findings provide a data-driven perspective on evolving player preferences and modern industry trends.

## 11. Ethical Considerations

All data used in this project is publicly available and does not include personal or sensitive information.
No scraping was performed, and all guidelines regarding ethical data usage were followed.
