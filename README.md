# DSA210-Project
**Single-player vs Multiplayer Games: Data Science Project**

 **Motivation**
In recent years, the gaming industry has increasingly shifted toward multiplayer experiences.  
However, many players still value story-driven single-player games.  
Through this project, I aim to explore whether players actually prefer multiplayer or single-player games — based on measurable data such as sales numbers and review scores.

 **Data Sources**
I will use publicly available datasets to collect and combine relevant information:
- **VGChartz dataset** – Provides global video game sales by title and platform.  
  (https://www.vgchartz.com/)
- **Metacritic dataset (Kaggle)** – Includes critic and user review scores for video games.  
  (https://www.kaggle.com/datasets/)
  
By merging these datasets using game titles, I plan to enrich the data and label games as either single-player or multiplayer.

 **Planned Analysis**
1. **Data Collection & Cleaning**  
   - Gather data from VGChartz and Metacritic.  
   - Remove duplicates and normalize game titles.  
   - Add a “Game Type” label (Single-player / Multiplayer).

2. **Exploratory Data Analysis (EDA)**  
   - Compare sales and review averages between categories.  
   - Create visualizations for yearly sales trends.  
   - Check correlations between ratings and sales.

3. **Statistical & Machine Learning Methods**  
   - Perform hypothesis testing (e.g., t-test between sales averages).  
   - Build a simple regression model to predict sales based on ratings and game type.

4. **Visualization & Reporting**  
   - Create charts comparing single vs. multiplayer game success.  
   - Summarize insights in the final report.

**Project Timeline**
| Date | Task |
|------|------|
| **Oct 31** | Submit project proposal on GitHub |
| **Nov 28** | Complete data collection and exploratory analysis |
| **Jan 2** | Apply ML techniques and finalize analysis |
| **Jan 9** | Submit final report |

 **Tools & Libraries**
- Python  
- pandas, numpy  
- matplotlib, seaborn  
- scikit-learn  

**Expected Outcome**
I expect to find whether multiplayer games actually dominate in terms of player engagement and sales, or if single-player titles still hold strong in terms of player satisfaction and critical success.

**Ethical Considerations**
All datasets used will be public and properly cited.  
No personal or private data will be included in this project.
