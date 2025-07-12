# FIFA 21 Player Data Analysis with Python  

**Description**: A comprehensive data analysis project cleaning and exploring EA Sports' FIFA 21 player dataset to uncover insights about player attributes, wages, and performance metrics.  

---

##  Table of Contents  
- [Dataset Overview](#-dataset-overview)  
- [Key Questions](#-key-questions)  
- [Process](#-process)  
  - [Data Cleaning](#data-cleaning)  
  - [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)  
- [Key Findings](#-key-findings)  
---

## 📁 Dataset Overview  
- **Source**: [Kaggle](https://www.kaggle.com/)  
- **Size**: 18,979 players × 77 attributes  
- **Features**: Player positions, wages, market value, release clauses, overall_rating, potential, height, weight.

---

## Key Questions  
1. Which club has the most players?
2. Which club has the fewest players? 
3. Which club has the youngest average age?
4. Which club has the oldest average age?
5. Who is the most valuable player?  
6. Which players are underpaid relative to their value?  
7. Do physical attributes (height/strength) correlate with `overall_rating`?  
8. Does wage correlate with age?  
9. What’s the relationship between `overall_rating`, `potential`, `value`, and `wage`?  
10. Which nation has the most "best players" (rating ≥ 80)?  
11. Which position earns the lowest wages?
12. Which position earns the lowest wages?  

---

##  Process  

### **Data Cleaning**  
- **Split Columns**: Separated `Team` and `Contract` into  `club` and `contract_type`.  
- **Standardized Units**:  
  - Converted `height` from feet/inches to inches.  
  - Removed "lbs" from `weight` for numerical analysis.  
- **Normalized Monetary Values**:  
  - Replaced "K" and "M" in `wage`, `value`, and `release_clause` with numerics(e.g., "€5K" → 5000).  
- **Cleaned Ratings**: Removed stars (★) from `W/F`, `SM`, and `IR` columns.  
- **Renamed columns**: Renamed a few columns for easier undertstanding of what it represents
- **Standardize Column names** - Lowercases all column names  
- **Removed Columns**: Dropped irrelevant columns (`photo_url`, `player_url`) and duplicates.
- **Removed Duplicates** - Dropped duplicated rows from dataset  

### **Exploratory Data Analysis (EDA)**  
- Used visualizations (histograms, scatter plots, heatmaps) to explore:  
  - Distributions of wages, ages, and ratings.  
  - Correlations between attributes (e.g., `height` vs. `strength`).  
  - Club/nationality-based trends.  

---

## 🔍 Key Findings  
*(Summarize your most interesting insights here. Example:)*  
- **Top Club**: "Manchester City" has the most players (X), while "XYZ" has the fewest (Y).  
- **Wage Disparity**: Player XYZ is underpaid (wage = €A, rating = B).  
- **Physical Traits**: Taller players show a weak/moderate correlation (R² = X) with `overall_rating`.  
- **Highest-Paid Position**: Strikers (ST) earn ~€X on average; goalkeepers (GK) earn the least.  

*(Add screenshots of key charts if possible!)*  

---

## 📦 Dependencies  
- Python 3.8+  
- Libraries:  
  ```bash
  pandas numpy matplotlib seaborn
  ```
  Install with:  
  ```bash
  pip install -r requirements.txt
  ```

---

## 🚀 How to Run  
1. Clone the repository:  
   ```bash
   git clone [your-repo-url]
   ```
2. Run the Jupyter notebook:  
   ```bash
   jupyter notebook fifa21_analysis.ipynb
   ```

---

## 🤝 Contributing  
Pull requests welcome! For major changes, open an issue first.  

---

### **Improvements Over Original**  
✅ **Added Structure**: Clear sections with emojis for readability.  
✅ **Reproducibility**: Added "Dependencies" and "How to Run" for users to replicate your analysis.  
✅ **Findings Section**: Highlights impact (original lacked summary).  
✅ **Removed Redundancy**: Merged repetitive "Questions" and "Process" sections.  
❌ **Removed**: Unnecessary bullet points (e.g., "DATA CLEANING AND ANALYSIS" preamble).
