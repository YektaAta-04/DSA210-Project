#  DSA210 Project
#  Single-player vs Multiplayer Games: What Do Players Really Prefer?

##  Motivation
In recent years, the gaming industry has increasingly shifted toward multiplayer-focused titles. However, single-player games continue to receive strong critical and fan appreciation. This project aims to explore whether players actually prefer multiplayer or single-player games — based on measurable data such as global sales and review scores.

---

##  Research Question & Hypotheses

### **Research Question**
> *Do multiplayer games outperform single-player games in terms of global sales and review scores?*

### **Hypotheses**
- **H1:** Multiplayer games have significantly higher global sales compared to single-player games.  
- **H2:** Single-player games receive significantly higher critic and user review scores compared to multiplayer games.  
- **H3:** Review scores (critic/user) positively correlate with sales irrespective of game type.  

These hypotheses justify the need for:
- detailed statistical tests (t-test, correlation analysis),
- exploratory data analysis,
- regression modeling.

---

##  Data Sources

### **1. VGChartz (Sales Data)**
- URL: https://www.vgchartz.com
- Includes: game titles, platforms, release years, global sales.

### **2. Metacritic Video Games Dataset (Kaggle)**
- URL: https://www.kaggle.com/datasets
- Includes: critic scores, user scores, genre, release year.

---

##  Data Collection Plan

### **VGChartz**
VGChartz does **not** provide an API.  
Therefore, I will collect data using:

- **Web scraping**  
  Tools:
  - `requests`
  - `BeautifulSoup4`
  
Scraping will target:
- Top-selling games pages
- Platform lists
- Sales tables

The extracted data will be saved as CSV.

---

### **Kaggle Dataset**
Kaggle provides a ready dataset, so the collection method is:

- Download Kaggle dataset manually
- Load via pandas (`pd.read_csv()`)

---

##  Data Merging Strategy

To combine VGChartz and Metacritic data:

- Primary key: **normalized game title**
- Secondary key: **release year**
  
If titles differ slightly, matching will be done using:
- fuzzy matching (`fuzzywuzzy library`, or `rapidfuzz`)
- manual inspection for unmatched cases

---

##  Data Cleaning & Normalization

### **1. Game Title Normalization**
Game titles often appear differently across datasets (e.g., varying punctuation, platform tags).

Normalization steps:
- Convert titles to lowercase  
- Remove punctuation  
- Remove platform info in parentheses (regex)  
  Example:  
  - “Halo 3 (Xbox 360)” → “halo 3”
- Remove edition labels:  
  (“Definitive Edition”, “Remastered”, “GOTY Edition”)
- Trim whitespace

This ensures clean, merge-ready uniform titles.

---

### **2. Remove Duplicates**
If a game appears multiple times:
- Keep the most complete/accurate record based on filled fields.

---

### **3. Missing Values Handling**
- If sales or review scores are missing, rows will be:
  - removed if few,
  - imputed if many (mean score, median score).

---

### **4. Labeling Game Type**
Games will be categorized using:
- Kaggle “genre” or “game type”
- Keyword detection (e.g., “online”, “multiplayer”, “co-op”)

Resulting in:
- `singleplayer`
- `multiplayer`

---

##  Planned Analysis

### **Exploratory Data Analysis (EDA)**
- Average sales for both game types
- Average critic/user score comparisons
- Trend charts by year
- Sales distribution (histograms)
- Correlation heatmap

---

### **Statistical Tests**
- **t-test** (single vs multiplayer sales comparison)
- **t-test** (single vs multiplayer review score comparison)
- **Pearson/Spearman correlation** between scores and sales  

---

### **Machine Learning Application**
A regression model to predict sales using:
- critic score  
- user score  
- game type  
- release year  

Models considered:
- Linear Regression  
- Random Forest  

---

##  Timeline
| Date | Task |
|------|------|
| **Oct 31** | Submit proposal |
| **Nov 28** | Data collection, cleaning, normalization, EDA, hypothesis testing |
| **Jan 2** | ML models and deeper analysis |
| **Jan 9** | Final report and presentation |

---

##  Tools & Libraries
- Python  
- pandas, numpy  
- matplotlib, seaborn  
- BeautifulSoup4 (scraping)  
- scikit-learn  
- rapidfuzz / fuzzywuzzy (matching titles)

---

##  Expected Outcome
The analysis will evaluate whether the industry's shift toward multiplayer reflects measurable player preferences, and how ratings influence sales effectiveness for both categories.

---

##  Ethical Considerations
All datasets are public, non-personal, and ethically sourced.  
Web scraping will comply with robots.txt rules and reasonable request frequency.

