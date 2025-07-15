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
1. Which team has the most players?
2. Which team has the fewest players? 
3. Which team has the youngest average age?
4. Which team has the oldest average age?
5. Who is the most valuable player?  
6. Which players are underpaid relative to their value?
7. What’s the relationship between `overall_rating`, `potential`, `value`, and `wage`?  
8. Which nation has the most "best players" (rating ≥ 80)?  
9. Which position earns the lowest wages?
10. Which position earns the highest wages?
11. Which attributes have a high correlation with overall rating for the top players in each position?"

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


---
## Answers
1. Which team has the most players?
<img width="225" height="355" alt="Club with most players" src="https://github.com/user-attachments/assets/3e3e0494-9358-48bc-89fc-1244066876f9" />

2. Which tean has the fewest players?
<img width="77" height="181" alt="Club with fewest players" src="https://github.com/user-attachments/assets/86d389af-7784-45a2-ba9f-48ac98199b76" />

3. Which team has the youngest average age?
<img width="168" height="114" alt="youngest average age" src="https://github.com/user-attachments/assets/b1ed70c5-af1d-48ee-8ec5-b575790db786" />

4. Which team has the oldest average age?
<img width="101" height="46" alt="Oldest Average Age" src="https://github.com/user-attachments/assets/ef46b359-92e0-4f17-89a1-5c421eb86eeb" />

5. Who is the most valuable player?
<img width="132" height="49" alt="Most Valuable Player" src="https://github.com/user-attachments/assets/4fe331d3-4468-4d5c-ac20-64e7c2f2bfd0" />

6. Which players are underpaid relative to their value?
<img width="202" height="296" alt="Underpaid Players" src="https://github.com/user-attachments/assets/63846790-223e-4b72-91b7-f6c893ad0287" />

7. What’s the relationship between overall_rating, value, and wage?
<img width="242" height="98" alt="Relationship" src="https://github.com/user-attachments/assets/661f0f76-edda-4f6d-b277-a3c0fb968fdb" />

8. Which nation has the most "best players" (rating ≥ 80)?
<img width="127" height="44" alt="Best Players" src="https://github.com/user-attachments/assets/85a36d37-1707-441b-9740-0a7fc8723611" />

9. Which position earns the lowest wages?
<img width="160" height="46" alt="Least Paid" src="https://github.com/user-attachments/assets/3fac1433-da69-41c5-a413-52e5265b8c28" />

10. Which position earns the highest wages?  
<img width="167" height="50" alt="Most Paid" src="https://github.com/user-attachments/assets/c52a200b-cf21-4f43-9228-165947b2e49b" />

11. Which attributes have a high correlation with overall rating for the top players in each position?
 - ST- finishing, ball control, reactions, positioning, shooting, composure.
- CT- short_passing, dribbling, ball_control, reactions, vision, composure, reactions
- RW - finishing, short_passing, dribbling, ball_control, reactions, long_shots, positioning, vision, composure, shooting, passing
- LW - finishing, short_passing, dribbling, ball_control, acceleration, sprint_speed, agility, reactions, positioning, vision, composure, pace, shooting
- CAM - crossing, short_passing,	volleys, ball_control, reactions, positioning, vision, shooting, passing
- CM - short passing, long passing, vision, reactions
- LM- ball controling, positioning, vision, composure, shooting
- RM- positioning, reactions
- CDM - short passing, interceptions, marking
- LWB - dribbling, curve, long_passing, ball_control, agility, reactions, interceptions, positioning, passing
- RWB - dribbling, ball_control, acceleration, sprint_speed, agility, shot_power, long_shots, interceptions, total_defending, marking, standing_tackle, sliding_tackle, gk_reflexes, pace
- LB - crossing, short_passing, reactions, passing
- RB - short_passing, ball_control, interceptions,reactions, standing_tackle, passing
- CB - interceptions, total_defending, marking, reactions,standing_tackle	
- GK- There is strong correlation with diving, reactions, handling, gk positioning, gk reflexex, pace and shooting


## 🔍 Key Observation  
- **Most Valuable Player**: The most valuable player in this dataset is Mbappe.
- **Wage Disparity**: There are couple of players with relatively high value that earn really little compare to thier counterpat.  
- **Overall rating, value, wage**: The relationship between these variables is high.
- **Best Team**: The nation with the top players based on overall rating is Spain.
- **Highest-Paid Position**: Strikers (ST) earn most on average; goalkeepers (GK) earn the least.
- **Attribute relationship with positions**: Reactions is an important attribute across all position for a player. For Goalkeepers diving, positioning, relexes are important attribute. For attackers (ST, CF, LW, RW) finishing, positioning, ball control are important attributes for overall rating. For Midfielders(CAM, CM, CDM, LM, RM) vision, ball control, positioning and passing are important attributes while for Defenders(CB, RB, LB, LWB, RWB) we could say passing, interceptions, standing tackle are important attributes. 
