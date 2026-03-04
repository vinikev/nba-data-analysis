# NBA Data Analysis Project

## Project Overview

This project performs an exploratory data analysis on historical NBA player statistics (2000-2017) to understand patterns, correlations, and tactical insights about basketball performance. The analysis focuses on understanding how different positions contribute to key statistical categories and identifying relationships between physical attributes and on-court performance.

## Problem Description

The **NBA Players stats since 1950** dataset contains historical NBA data (1950-2017), including:

- Player information (position, height, weight, age)
- Per-season statistics (points, assists, rebounds, 3-point field goals)
- Among many others that will not be used in this analysis

## Analysis Hypotheses

The following hypotheses were formulated for investigation:

**1. Position Influence on Statistics**
To verify whether the on-court position significantly determines players' statistical performance.

**2. Relationship Between Height and Performance**
To identify which metrics show a positive correlation with athletes' height.

**3. Data Adherence to Tactical Patterns**
To evaluate whether the observed statistics correspond to tactical expectations for each position.

**4. Talent Distribution by Position**
To investigate the existence of concentration or balance in performance across different positions.

**5. Frequency of Performance Outliers**
To quantify the occurrence of exceptional values ("star players") in relation to the overall average.

## Dataset Attributes

The dataset contains 24,691 samples, where each record represents a player in a season. The following attributes were used:

- **_Player_** (Player's full name)
- **_Height_** (Player's height in cm)
- **_Pos_** (Player's position)
- **_PTS_** (Number of points in the season)
- **_AST_** (Number of assists in the season)
- **_TRB_** (Number of rebounds in the season)
- **_3P_** (Number of 3-point field goals made in the season)
- **_3PA_** (Number of 3-point field goal attempts in the season)
- **_G_** (Number of games played in the season)
- **_Year_** (Season year)

## Data Filtering & Preparation

The following selection criteria were applied:

**Time period:** Only records after the year 2000 were selected, aiming to analyze the contemporary NBA period.

**Analyzed positions:** Only the five most frequent positions were kept, discarding hybrid or marginally occurring variations:

- PG (Point Guard)
- SG (Shooting Guard)
- SF (Small Forward)
- PF (Power Forward)
- C (Center)

**Relevant variables:** Only columns with direct correlation to the investigated hypotheses were considered.

**Data standardization:** Observations with missing or zero values in points (PTS), assists (AST), rebounds (TRB), and games played (G) were eliminated.

## Analysis Performed

### 1. Player Distribution by Position

Analysis of the balance and concentration of unique players across different positions since 2000.

**Technical Position Legend:**

- **PG (Point Guard):** Responsible for offensive organization and play creation
- **SG (Shooting Guard):** Specializes in mid-range and long-distance shots
- **PF (Power Forward):** Operates in the paint, standing out in physical strength plays and rebounding
- **C (Center):** Usually the tallest player, with predominant role in defense and rebounds
- **SF (Small Forward):** Versatile player with balanced participation in offensive and defensive actions

### 2. Per-Game Statistics Distribution

Histogram analysis of three key per-game metrics:

- Points per Game (PTS/G)
- Assists per Game (AST/G)
- Rebounds per Game (TRB/G)

### 3. Performance Analysis by Position

Boxplot visualization comparing statistical distributions across different positions, revealing tactical patterns and positional specialization.

### 4. Correlation Analysis

Heatmap correlation matrix examining relationships between:

- Per-game statistics (PTS/G, AST/G, TRB/G)
- 3-point statistics (3P, 3PA)
- Player height

## Key Findings

### Player Distribution by Position

The distribution of players by position throughout the analyzed period shows relative balance, with a slight predominance of positions with greater offensive protagonism.

### Histogram Analysis

**Points per Game (PTS/G)**

- Shows positive asymmetric distribution
- Main concentration: 5-15 points per game
- Indicates that most players have moderate scoring contribution

**Assists per Game (AST/G)**

- Distribution concentrated in the 0-5 assists range
- Values above 8 assists/game have low frequency

**Rebounds per Game (TRB/G)**

- Peak frequency between 0-5 rebounds
- Few cases exceed 10 rebounds/game

### Boxplot Analysis by Position

**Points per Game (PTS/G)**

- Highest medians in SG (Shooting Guard) and PG (Point Guard), corroborating the offensive nature of these positions
- C (Center) presents the lowest average, consistent with its predominantly defensive role

**Assists per Game (AST/G)**

- Clear dominance of the PG (Point Guard) position, as expected in its tactical function

**Rebounds per Game (TRB/G)**

- Highest values concentrated in C (Center) and PF (Power Forward)
- PG (Point Guard) presents marginal contribution, characteristic of shorter players with greater mobility

### Correlation Matrix Insights

**Key correlations identified:**

1. **3-Point Attempts vs. Made:** Almost perfect correlation (r ≈ 1.0) - expected relationship

2. **Rebounds vs. Outside Game:** Near-zero correlation between rebounds and 3-point statistics - tactical explanation: rebound specialists (centers/power forwards) operate primarily in the paint

3. **Assists vs. Offensive Statistics:** Significant positive correlations - consistent with point guards' role in play creation

4. **Height vs. Rebounds:** Moderate positive correlation (0.41) - taller players tend to have more rebounds

5. **Height vs. Points per Game:** Insignificant correlation (-0.04) - height is not a determining factor for scoring

6. **Height vs. 3-Point Shots:** Weak negative correlation (-0.25 to -0.26) - shorter players (PGs/SGs) are primary 3-point shooters

7. **Height vs. Assists:** Moderate negative correlation (-0.40) - shorter players lead in assists, reinforcing the point guard's role as primary offensive organizer

### Outliers Observation

Even considering multiple seasons of exceptional athletes (LeBron James, Shaquille O'Neal, Kobe Bryant), extreme values remain statistically rare, which explains the differentiated recognition of these athletes in the sports context.

## Technologies Used

- **Python** (Pandas, NumPy)
- **Data Visualization:** Matplotlib, Seaborn
- **Data Processing:** Jupyter Notebook / Google Colab
