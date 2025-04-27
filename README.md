# The Evolution of the NBA 
- The source code for this analysis is available [here](https://github.com/leonemma/NBA-1996-2022-Stats-Analysis/blob/main/NBA-(1996-2022)-Analysis.ipynb)

## Contents 
- [Background](#Background)
- [Data Source](#Data-Source)
- [Goals](#Goals)
- [Key Questions](#Key-Questions)
- [FIndings](#Findings)

  
## Background
The NBA is one of the most popular sports in the world. Top basketball players from all over the globe dream of reaching the level required to earn a spot in this highly competitive league.
In this analysis, we will explore the NBA from the 1996 season to 2023. Our analysis will focus on differences in key basketball metrics each year, as well as the players who stood/stand out during different periods.  

## Data Source
The dataset is available on Kaggle (Justinas Cirtautas: [NBA Players](https://www.kaggle.com/datasets/justinas/nba-players-data/data)).   

## Goals 
- Explore and Analyze NBA players' performance data over the years.
- Answer Key Questions related to player origins, scoring trends, playmaking abilities, consistency, and impact.
- Identify Patterns in player performance such as the evolution of top scorers and dominant all-around players.
- Visualize Insights through clear graphs to make data easily understandable.
  
This dataset consists of  22 columns and 12844 observations and contains individual players multiple times due to the collection of their statistics every year.

That's why we will split our analysis into two parts:
1. Analyzing the NBA over the years
2. Transforming the dataset to represent NBA players average career stats

## Key-Questions
These questions will guide our exploration and uncover insights into the dynamics of NBA players's performance over the years. 

### NBA over the Years
#### 1. What's the total number of NBA players over the years ?
#### 2. How long do NBA players typically stay in the league?
#### 3. How many players are drafted each year ?
#### 4. How does the Maximum Points per Game change over the years ?
### NBA Players who Stood Out  
#### 5. How many NBA players performed at an All-Star level consistently ?
#### 6. Which NBA players had/have the best scoring seasons in the last 25 years ?
#### 7. Which NBA players were/are the most dominant in the last 25 years ?
#### 8. Which NBA players were/are the best guards in the last 25 years ?

## Findings

#### 1. Total Number of NBA players
The NBA has strategically expanded its player pool by creating more contract options, increasing global scouting, and using the G League as a talent pool. This trend has allowed for a larger number of players to participate in the league, improving overall competition and entertainment value.  
The following plot highlights the increase in the number of NBA players starting from 2010. It appears that teams have expanded their rosters, providing more opportunities for basketball players to secure a position in the league.

![Count_ofNBA_players](https://github.com/leonemma/NBA-1996-2022-Stats-Analysis/blob/main/plots/1.%23playersbyyears.png)

#### 2. Career Longevity of NBA Players (Seasons Played)
To better understand the dynamics of player careers, we engineered a new feature called SeasonsPlayed, representing the total number of seasons each player participated in the NBA.
We visualized the distribution of this variable to answer our second key question.

![SeasonsPlayed](https://github.com/leonemma/NBA-1996-2022-Stats-Analysis/blob/main/plots/2.1SeasonsPLayed.png)

#### 3. Count of Players in Yearly Draft
Let's see the NBA players drafted per year, by excluding those who didn't participate in the draft.

![Drafted_Players](https://github.com/leonemma/NBA-1996-2022-Stats-Analysis/blob/main/plots/2.2Drafted1.png)

#### 4. Changes in Maximum Points Per Game (PPG) 
The NBA has seen some of the greatest scorers in basketball history, with certain players dominating individual seasons by posting exceptionally high points-per-game (PPG) averages.
The following line plot visualizes the maximum PPG recorded in each NBA season, helping us understand how elite scoring has evolved over time.  

![MAXPPG](https://github.com/leonemma/NBA-1996-2022-Stats-Analysis/blob/main/plots/3.MAXppgBySeason.png)

#### 5. All Star Players
We create a new feature that categorizes if a player was/is in all star level during his career based on the following metrics:
- Top 10% Scoring Low
- Top 10% Rebounding Low
- Top 10% Passing Low
If an NBA player belongs to one of those subsets, it means that is better in the corresponding category from at least the 90% of the entire NBA.

![All_Star](https://github.com/leonemma/NBA-1996-2022-Stats-Analysis/blob/main/plots/4.All_star_distr.png)

#### 6. Top Scoring Seasons
Let's explore the top 10 seasons in scoring in the NBA in the last 25 years and see who are the players who stood out during this period.  

![Scoring_Seasons](https://github.com/leonemma/NBA-1996-2022-Stats-Analysis/blob/main/plots/5.Best_Scoring_Seasons2.png)  

#### 7. Most Dominant Players
We define a dominant player as one who consistently stands out in both scoring and rebounding throughout his career. Specifically, a player is considered dominant if he meets the following criteria:
- Averaged at least 20 points per game (PPG) across their career
- Averaged at least 10 rebounds per game (RPG) throughout their career
By applying this definition, we identify players who were both elite scorers and strong rebounders in the game. This allows us to highlight players who had a significant two-way impact, particularly in scoring and controlling the boards.

![DominantPlayers](https://github.com/leonemma/NBA-1996-2022-Stats-Analysis/blob/main/plots/6.Most_Dominant.png)  

#### 8. Top Playmakers in the Game
A playmaking scorer is a player who excels in both scoring efficiently and creating opportunities for teammates. Unlike traditional point guards who focus primarily on passing the ball or shooting guards who are primarily scorers, playmaking scorers effectively combine both skills, making them key offensive leaders for their teams.

For this analysis, we define a player as a playmaking scorer if they meet the following criteria:
- Averaged at least 20 points per game (PPG) throughout their career
- Averaged at least 5 assists per game (APG) throughout their career

![Playmakers](https://github.com/leonemma/NBA-1996-2022-Stats-Analysis/blob/main/plots/7.Best_Playmakers.png)

