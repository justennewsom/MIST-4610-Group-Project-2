# MIST 4610 Group 7 Project Two Submission

# Team Number and Members
- **Team Number:** Group 7
- **Members:**
  - Wilson Nguyen [@dakarie](https://github.com/dakarie/MIST-4610-Group-Project-2/tree/main)
  - Akshaya Ezhil [@githubhandle2](https://github.com/githubhandle2)
  - Justen Newsom [@justennewsom](https://github.com/justennewsom)
  - Shahil Patel [@githubhandle4](https://github.com/githubhandle4)
  - Josh Gershon [@githubhandle4](https://github.com/githubhandle4)


# Dataset Description

- **Dataset Source:** [kaggle.com](https://www.kaggle.com/datasets/sumitrodatta/nba-aba-baa-stats?resource=download&select=Player+Play+By+Play.csv)
- **Dataset Title:** _We used the `Team Stats Per Game` file from the full dataset available on Kaggle._
- **Dimensions:** _1876 rows × 28 columns_

The dataset used for this project was sourced from Kaggle and is titled NBA/ABA/BAA Stats. Specifically, we utilized the “Team Stats Per Game” CSV file, which contains season-level performance metrics for professional basketball teams across the NBA, ABA, and BAA leagues.This dataset provides a comprehensive view of how basketball teams have performed on a per-game basis from the league’s early days through the 2023 season. It captures a wide range of statistics across multiple categories including shooting, scoring, rebounding, and playmaking.

**Key Columns and Data Types:**
- `season` – Integer (Year of the season)
- `lg` – String (League name, e.g., NBA)
- `team` – String (Full team name)
- `abbreviation` – String (Team abbreviation)
- `playoffs` – Boolean (True if team made playoffs)
- `g` – Float (Games played)
- `mp_per_game` – Float (Minutes per game)
- `fg_per_game` – Float (Field goals per game)
- `x3pa_per_game` – Float (3-point attempts per game)
- `x3p_per_game` – Float (3-point makes per game)
- `x3p_percent` – Float (3-point shooting percentage)
- `pts_per_game` – Float (Points per game)
*(Add more as needed)*




# Research Questions

1. **Question 1** _Is there a relationship between 3-point shooting volume and playoff qualification in the 2024 NBA season?_

   - _This question is important because 3-point shooting has become a central part of modern NBA strategy, but it’s unclear whether simply attempting more 3-pointers directly contributes to playoff success. By investigating this link, we can better understand whether volume-based shooting translates to results or if other factors (like efficiency or defense) play a larger role. This insight can inform how teams evaluate performance, make roster decisions, and approach game strategy._

   - _This question ties directly to our dataset, which includes `x3pa_per_game` (3-point attempts per game) and `playoffs` (playoff status) for each team. By isolating the 2024 season and comparing average 3PT attempts between playoff and non-playoff teams, we can evaluate whether there’s any real correlation between 3PT volume and making the postseason._


2. **Question 2:** _Did Stephen Curry's arrival to the league effect the amount of scoring and 3-pointers attempted in the NBA?​_  
   - _This question matters because Stephen Curry is widely credited with revolutionizing the NBA’s offensive style through his unprecedented 3-point shooting volume and accuracy. His influence is believed to have reshaped team strategies, player development, and even how fans engage with the game. By analyzing league-wide trends in scoring and 3-point attempts before and after his arrival (2009), we can objectively measure the impact of this shift. This question connects directly to our dataset, which includes per-game statistics such as x3pa_per_game (3-point attempts) and pts_per_game (points per game) for every NBA team across multiple seasons. By comparing team averages between the pre-Curry era (1992–2008) and the post-Curry era (2009–2025), we can assess how much the league has changed and how much of that change aligns with Curry’s influence._






# Analysis and Results

We used Tableau for visual analysis. The visualizations included:
- Bar charts

### Question 1: Is There a Relationship Between 3-Point Shooting Volume and Playoff Qualification in the 2024 NBA Season?

![Image](https://github.com/user-attachments/assets/78d94e1c-4bee-4dcc-97d8-482fab2b1955)

**Visualization:**  
_This bar chart compares the average number of 3-point attempts per game by each NBA team in the 2024 season. Bars are color-coded by playoff status — green for teams that made the playoffs, red for those that did not. It provides a visual comparison of how 3-point volume may relate to postseason qualification._

**Key Insights:**
- Most of the top 3-point shooting teams did not make the playoffs, suggesting that high volume alone does not guarantee success.
- Playoff teams tend to fall in the middle range of 3PT attempts, hinting that balance, efficiency, or other factors (like defense or shooting %) may be more important than just volume.
- There is no clear linear correlation between average 3-point attempts and playoff qualification — teams with both high and low 3PT volumes are seen in both playoff and non-playoff groups.



### Question 2: Did Stephen Curry’s Arrival to the League Affect the Amount of Scoring and 3-Pointers Attempted in the NBA?

![Image](https://github.com/user-attachments/assets/1d2f3f77-4ec1-4cda-8db9-9551ae8f7f2d)

**Visualization:**  
_Two bar charts comparing average team 3PT attempts and points per game across two time periods:_
- 1992–2008 (pre-Curry era)
- 2009–2025 (post-Curry era)

**Key Insights:**
- From 1992 to 2008, most teams averaged under 20 3PT attempts per game. Post-2009, nearly every team consistently averaged 25–35 attempts.
- Average scoring also increased, but the bigger shift was *how* teams scored — with a much greater reliance on 3-point shots across all franchises.





# Data Manipulations


### Question 1: Is there a relationship between 3-point shooting volume and playoff qualification in the 2024 NBA season?

- Filtered the dataset to include only the 2024 NBA season
- Used the `playoffs` column to separate teams into playoff vs. non-playoff groups
- Used `x3pa_per_game` (3-point attempts per game) as the primary metric
- Aggregated data by team to calculate average 3PT attempts
- Applied color coding in Tableau to visually distinguish playoff teams from non-playoff teams in the bar chart


### Question 2: Did Stephen Curry’s Arrival to the League Affect the Amount of Scoring and 3-Pointers Attempted in the NBA?

- Removed rows with missing values in key columns (`pts_per_game`, `x3pa_per_game`)
- Filtered dataset by two time periods:
  - 1992–2008 (pre-Curry era)
  - 2009–2025 (post-Curry era)
- Created calculated fields in Tableau to:
  - Compute average team 3PT attempts and points per game per era
- Aggregated data by team and season to create league-wide comparisons

# Conclusion 
Our analysis shows that while 3-point shooting volume has significantly increased since the late 2000s — especially after the emergence of Stephen Curry — success in the modern NBA is not solely based on 3-point attempts. In the 2024 season, teams with both high and low 3-point volumes made the playoffs, suggesting that efficiency and overall balance matter more than raw shooting volume. These findings reinforce the complexity of modern basketball strategy and how trends influence, but do not guarantee, competitive success.


# Deliverables
 
 - ✅ `README.md` – Full project explanation
 - ✅ `Project 2.twbx` – Tableau visualization file
 - ✅ `Team Stats Per Game.csv` – Dataset used for analysis


