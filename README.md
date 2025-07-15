# FIFA 21 Player Data Analysis with Python  

**Description**: A comprehensive data analysis project cleaning and exploring EA Sports' FIFA 21 player dataset to uncover insights about player attributes, wages, and performance metrics. 

## *Table of Contents*  
- [Dataset Overview](#-dataset-overview)  
- [Key Questions](#-key-questions)  
- [Process](#-process)
- [Answers](#-answers)
- [Key Findings](#-key-findings)  
- [Recommendations](#-recommendations)

##  Dataset Overview  
- **Source**: [Kaggle](https://www.kaggle.com/)
- **Files**: Attach to this repository is the csv raw file of fifa21 and notebook of analysis.
- **Size**: 18,979 players × 77 attributes  
- **Features**: Player positions, wages, market value, release clauses, overall_rating, potential, height, weight.

---

##  Key Questions  
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


## Key Observation  
### 1. Most Valuable Player 
- The most valuable player in this dataset is Mbappe with valuation of 105,500,000.
### 2. Wage Disparity 
- There are a few players with relatively high market value who earn significantly less compared to their counterparts.
### 3. Overall rating, value, wage
- There is a strong positive correlation.
### 4. Nation with Top Players
- The Spain happens to have a lot of top players 
### 5. Highest-Paid Position
- Strikers (ST) earn the most on average (23,444.87), while goalkeepers (GK) earn the least (6,390.81)
### 6. Attribute relationship with positions
- Reactions is an important attribute across all position for a player.
- *Forwards (ST/LW/RW)*: Finishing, ball control, reactions.  
- *Midfielders (CAM/CDM)*: Vision, passing, interceptions, ball control.  
- *Defenders (CB/RB)*: Tackling, marking, positioning, interceptions.  
- *Goalkeepers (GK)*: Reflexes, diving, handling, gk positioning.

## *Recommendations*  
1. **Clubs should also target Underpaid Players**: Players with high value but low wage—these could be cost-effective signings.  
2. **Position-Specific Training**: Coaches should focus on key attributes for each role to maximize player performance.  
3. **Negotiate Better Contracts**: Players with high overall_rating but below-average wages should leverage their market value in contract talks.
4. **Clubs should invest in Young Talents**: Players with high potential but low wages can provide long-term value.  
