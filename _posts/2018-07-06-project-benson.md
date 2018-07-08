---
layout: post
title: Analysis of MTA data
---

#### Introduction

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

### Conclusion

Stuff.

### Recommendation

Do things.
