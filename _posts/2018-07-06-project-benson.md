---
layout: post
title: Analysis of MTA data
---

## Introduction

Our team at  Super Awesome Data Scientist, Inc. set out to form a partnership with the well known women's tech organization: Women Tech, Women Yes. In order to do so, we set out to implement a strategy to increase awareness, attendance, and ultimately, donations at their annual Summer Gala.

We know that Women Tech, Women Yes increases awareness for their events by placing volunteer staff at subway stations around New York City. With that in mind, we wanted to figure out the best subway stations to place their staff at, and the best times. In order to do so, we analyzed subway turnstile data to find the most trafficked stations, and then incorporated that information with data from yelp to try and hone in on a wealthier demographic to maximize donations.

In doing so, we were able to find the best subway stations for Women Tech, Women Yes to place their volunteer staff in order to maximize donations at their Summer Gala! 

### Analysis

Our first order of business was to find the median number of people entering a specific subway station, and not only that, but to find the busiest time of the week to place our staffers at those locations. Unsuprisingly, the busiest time of week was Friday evening, as people tend to be leaving work for the weekend and most likely going out to dinner. The resulting list is of the median traffickers per 4 hour period at the top 10 busiest subway stations at that time period.

| Subway Station | Foot Traffic (people) |
| ---------------|-----------------------|
| 34 St - Herald Square | 75462 |
| 34 St - Penn Station | 71010 |
| Times Square - 42 St | 62494 |
| Grand Central Station - 42 St | 44397 |
| 23 St | 42064 |
| 47-50 Streets Rock | 41853 |
| 59 St Columbus | 38911 |
| 59 St | 37528 |
| 86 St | 34716 |
| Chambers St | 34674 |

Next, we fed every station's geographical coordinates, not only the top 10 list, through Yelp find the density of high priced restaurants within 3 blocks of that station, to help target the high priced demographic we were searching for. 

According to our research, high priced restaurants such as NYC Michelin rated restaurants need at least 250 customers on busy night to turn a profit. We made the assumption that 50% of restaurant goers in New York City arrived by subway station. We also generated the assumptions that only 2% of the population are likely to speak with a flyer distributor, and of that 2%, only 20% will ultimately result in the Summer Gala attendance and donation.

This allowed us to generate a list of expected donors from each subway station location, and in addition, the number of staff required to obtain those donations!

### Results

Below is the list of optimal subway stations to place volunteer staff to hand out flyers and gather email addresses for attendance at the Summer Gala. However, depending on the number of resources available, it's up to Women Tech, Women Yes to determine how to allocate their staff as they see fit.

| Subway Station | Foot Traffic (people) | Number of High Priced Restaurants | Sales Reps Required | Donors |
| ---------------|:---------------------:|:------------------------------:|:----------------:|:------:|
| 3rd Avenue - 149 St | 6436 | 37 | 3 | 19 |
| Brighton Beachn | 5762 | 38 | 2 | 19 |
| 167 St | 7851 | 36 | 3 | 18 |
| 161 St/Yankee Stadium | 7522 | 36 | 3 | 18 |
| 149 St/Grand Conc | 4911 | 37 | 2 | 18 |
| Flushing-Main | 29208 | 34 | 12 | 17 |
| Kings Highway | 10528 | 33 | 4 | 17 |
| 5th Avenue | 9099 | 34 | 4 | 17 |
| 103 St - Corona | 8268 | 35 | 3 | 17 |
| Fordham Rd | 7623 | 34 | 3 | 17 |

### Recommendation

Given our analysis, we highly recommend Women Tech, Women Yes to allocate their staff at the above locations in order to maximize their attendance and donation quantity at their Summer Gala 2019. We know that our guidance will lead towards greater awareness for this wonderful event!

