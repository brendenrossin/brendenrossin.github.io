---
layout: post
title: Predicting Baseball Player Salaries
---

## Introduction

Upon finishing my third week at Metis, I was tasked with a project in which the objective was to create a model solely using linear regression. Therefore, I knew the optimal result of my project would be to predict some numerical value, and my mind immediately jumped to a regression involving baseball statistics, because of the volume of both features to select from and my interest in the sport. As a fan, there seems to be an almost inexhaustible resource of potential complaints about specific players, teams, and the league as a whole, but one divisive subject that has always been hard to substantiate is whether or not a player is being overpaid or underpaid.

Therefore, I set out to create a model to predict players' salaries based on their previous statistics, and then determine a player's value in order to verify whether a player's current salary is commensurate to their play on the field, and in addition to predict what a player's future contracts should look like!

### Analysis

In order to create my model, I first had to gather the necessary data involved, most importantly the current MLB players' prior batting statistics and current salaries. In order to do so, I scraped baseball-reference.com with BeautifulSoup and Selenium to first get to each team's roster page, and subsequently scraped over the 40-man roster table to find the 40 players on the active roster for each of the 30 MLB teams, and compile a list of the Baseball-Reference URLs for the 1200 players actively in the MLB.

Having obtained the web addresses for each player, I then scraped each player's page to find their batting statistics in the 'Standard Batting' table, their overall defensive Wins Above Replacement fromt the 'Player Value--Batting' table, and their salary information in the 'Salary' table. In addition, I pulled their full name from the Player Information header on the page in an attempt to distinguish individual players with similar names.

![Image Missing]({{"/assets/Giancarlo Stanton.png"|https://github.com/brendenrossin/brendenrossin.github.io/blob/master/assets/Screen%20Shot%202018-07-25%20at%205.33.35%20PM.png}})

The next order of business was to find the correct players to create the model from, so that our algorithm wasn't influenced by players who's salaries didn't reflect their batting statistics for specific and intentional reasons. The first and most obvious cut was to remove pitchers from the analysis, as their salaries aren't a reflection of their batting statistics, but rather their pitching statistics, which is obviously a better representation of their worth to an organization. The next cut wasn't immediately obvious to me, but as I performed more EDA and even delved into modeling, it became clear that my models were influenced by the batting statistics of players on their rookie contracts.

Rookie contracts are generally pretty cookie cutter, with salaries less than $1,000,000, and usually sitting right above $500,000 for 2018 rookies. Their salaries aren't a reflection of their MLB batting statistics because they don't have a robust enough background in the MLB to make an indication of what their salaries should be. Therefore they're getting paid as entry-level players in the league until their actual worth is proven with experience in the league. Therefore, players on rookie contracts with wildly varying statistics are going to paid due to their entrance into the league, rather than their past performance.

For the purposes of this project, this makes a lot of logical sense, as we're attempting to analyze the new contracts that players get, so removing players on standard rookie contracts to model off of players who have gotten "real" contracts makes sense.

In doing further exploratory analysis, I ended up removing all players whose batting average was below 0.200, or the Mendoza line. The Mendoza line is typically a measure of competency for batters in the MLB. I removed batters below the Mendoza line as I didn't want my model to be influenced by "incompetent" batters.

Lastly, we wanted to only include 2018 current salaries, and only look at batting statistics from 2011-2017 in order to get a robust look at how players have been batting and what information could have gone into generating their current salaries.

I then created dummy variables for the 9 remaining positions (including Designated Hitter) and the 30 MLB teams, to see if they would make an impact on my model. There were some interesting trends to note with respect to how position impacts salary, but no distinguishable trends with respect to how teams impact salary, which surprised me as some teams (i.e. NY Yankees) tend to have much larger pockets.

![Image Missing]({{"/assets/Position_vs_Salary.png"|https://github.com/brendenrossin/brendenrossin.github.io/blob/master/assets/Screen%20Shot%202018-07-19%20at%208.33.24%20PM.png}})

![Image Missing]({{"/assets/Team_vs_Salary.png"|https://github.com/brendenrossin/brendenrossin.github.io/blob/master/assets/Screen%20Shot%202018-07-19%20at%208.35.44%20PM.png}})

### Results


Going forward, it would be helpful to look at player's salaries right after their contracts were negotiated in case a decline in performance over the course of a long contract influenced my model. In addition, it would be helpful to have a dataset with more data points, with all the cuts made to the dataset decreasing my total observations down to approximately 240 players.
