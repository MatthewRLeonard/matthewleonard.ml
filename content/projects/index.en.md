---
aliases:
- projects
- portfolio
author: Matthew Leonard
date: '2021-07-01'
description: My projects
title: Projects
---

### NFL Index Ratings
![NFL Index Ratings](NFL-Index-Ratings.png#project-img)

[matthewleonard.shinyapps.io/NFL-Index-Ratings](https://matthewleonard.shinyapps.io/NFL-Index-Ratings/)

Using the R package, nflfastR, I developed an NFL team index ratings system. Using the tidyverse, I analysed nflfastR play-by-play data and created team offensive and defensive statistics, such as Success Rate, Available Yards % and Expected Points Added per play. Taking the offensive and defensive statistics, I then created net statistics and scaled them. Adding up these scaled scores, I created a rating for every team with a range from 0 - 100, hence the term "index rating".

Using R packages such as shiny, shinyWidgets, reactable and reactablefmtr, I developed a web application as a dynamic tool to display the index ratings and many other statistics, including the net ratings that were scaled to create the overall ratings. The web application can be filtered for NFL seasons 2014-2020, conference, division, overall, offensive and defensive ratings. All columns are sortable and it looks cool!