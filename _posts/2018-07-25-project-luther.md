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

##### Tables used to extract relevant information
![Image Missing]({{"/assets/Giancarlo Stanton.png"|https://github.com/brendenrossin/brendenrossin.github.io/blob/master/assets/Screen%20Shot%202018-07-25%20at%205.33.35%20PM.png}})


### Results
