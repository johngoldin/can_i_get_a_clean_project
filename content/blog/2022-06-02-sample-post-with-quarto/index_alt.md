---
title: "Sample Post With Quarto"
format: hugo
editor: visual
author: John Goldin
date: '2022-05-11'
slug: sample-post-with-quarto
categories: []
tags: []
subtitle: ''
excerpt: 'National county-level data shows a correlation between COVID vaccinatioin rates and 2020 Trump vote share. This post will do something similar at the level of Connecticut towns.'
draft: yes
images:
  - ~
  - ~
series: ~
layout: single
execute:
  echo: false
  warning: false
cache: true
toc: true
freeze: auto
fig-width: 7
out-width: 100%
fig-align: "center"
fig-asp: 0.618  
---



-   <a href="#connecticut-2020-presidential-vote-and-vaccination-by-town" id="toc-connecticut-2020-presidential-vote-and-vaccination-by-town">Connecticut 2020 Presidential Vote and Vaccination by Town</a>
    -   <a href="#work-by-charles-gaba-on-trump-vote-and-covid-vaccination-and-death" id="toc-work-by-charles-gaba-on-trump-vote-and-covid-vaccination-and-death">Work by <span>Charles Gaba</span> on Trump Vote and COVID vaccination and death</a>
    -   <a href="#polling-on-partisanship-and-vaccination" id="toc-polling-on-partisanship-and-vaccination">Polling on Partisanship and Vaccination</a>
    -   <a href="#some-quick-reactions" id="toc-some-quick-reactions">Some Quick Reactions</a>
    -   <a href="#the-issue-of-the-population-denominator-and-its-effects-on-vaccination-rates" id="toc-the-issue-of-the-population-denominator-and-its-effects-on-vaccination-rates">The Issue of the Population Denominator and Its Effects on Vaccination Rates</a>

<div id="fig-anonymous-1">

<img src="index_alt_files/figure-gfm/setup_date-1.png" width="672" />

</div>

## Connecticut 2020 Presidential Vote and Vaccination by Town

The plot below shows the relationship between vaccination rates and percentage of the vote for Trump in the 2020 election.

<div id="fig-anonymous-2">

<img src="index_alt_files/figure-gfm/vote_repub-1.png" width="672" />

</div>

Note that for the trend lines in the plot I have eliminated Mansfield and Simsbury as outliers. Manfield is the location of University of Connecticut. Some students may be counted in census population, but getting their vaccinations elsewhere. I don't know what's going on with Simsbury.

The CDC uses someting they call the [social vulnerability index](https://www.atsdr.cdc.gov/placeandhealth/svi/index.html), and DPH has included that as well. DPH flags each town that has at least one census tract that has a social vulnerability index of 75% or greater. Towns showing the social vulnerability index flag tend to have a lower vaccination rate (and a lower Trump percentage), and that's especially true for the large cities.

### Work by [Charles Gaba](https://t.co/x3Vu568chv?amp=1) on Trump Vote and COVID vaccination and death

Charles Gaba has been doing analyses showing the [relationship between 2020 vote and vaccinations](https://acasignups.net/21/11/23/weekly%20to%20update%20to%20us%20to%20covid19%20to%20vaccination%20to%20levels%20to%20county%20to%20trump%20to%202020%20to%20vote) and deaths using county to level data for all states.

![From Charles Gaba](https://acasignups.net/sites/default/files/styles/inline_default/public/vaxxes_red_blue_every_county_112221_0.jpg?itok=JBx4OW9o) Which reminds me, why have I been putting Trump Vote on the y to axis? The x to axis makes much more sense given that the hypothesis is that Trump vote affects vaccination.

### Polling on Partisanship and Vaccination

See this summary of the MULawPoll.

<blockquote class="twitter-tweet">
<p lang="en" dir="ltr">
Here is vaccination status by age and party, suggested by <a href="https://twitter.com/AFilindra?ref_src=twsrc%5Etfw">@AFilindra</a> <br><br>This pools Sept & Nov 2021 <a href="https://twitter.com/MULawPoll?ref_src=twsrc%5Etfw">@MULawPoll</a> national surveys to maximize cases. Estimates are logit fits by party.<br><br>Partisan gap narrows with age, but obvious partisan difference even among old. <a href="https://t.co/klA11TY5YX">pic.twitter.com/klA11TY5YX</a>
</p>
--- Charles Franklin (@PollsAndVotes) <a href="https://twitter.com/PollsAndVotes/status/1465126616561029126?ref_src=twsrc%5Etfw">November 29, 2021</a>
</blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

### Some Quick Reactions

The first interesting thing is that the relationship between Trump vote and vaccination is so different for the over 65 crowd. It's only the under 65 population for whom a higher Trump vote is correlated with lower vaccination (and that relationship is probably even clear if one separate out the towns flagged with the social vulnerability index or the large cities).

I'll sleep on this and see what I think tomorrow.

#### Sources

Vote stats come from [The Secretary of State](https://ctemspublic.pcctg.net/#/reports).

Vaccination rates are from DPH via [data.ct.gov](https://data.ct.gov/Health%20to%20and%20to%20Human%20to%20Services/COVID%20to%2019%20to%20Vaccinations%20to%20by%20to%20Town%20to%20and%20to%20Age%20to%20Group/gngw%20to%20ukpw).

### The Issue of the Population Denominator and Its Effects on Vaccination Rates

The Department of Public Health (DPH) provides vaccination rates by age ranges by town. For this plot I have collapsed the age ranges into four groups. DPH also provides an estimated population for each range. Note that you see a lot of vaccination percentages above 100%. That's probably an issue with the estimated population. DPH includes their estimate of the population with all of their statistics. See \[this page\](<https://portal.ct.gov/dph/Health> to Information to Systems to to Reporting/Population/Population to Statistics for [this description of technical issues](https://authoring.ct.gov/%20to%20/media/Departments%20to%20and%20to%20Agencies/DPH/Population/PopulationStatisticsOverviewpdf.pdf). I am uncertain where that leaves things. It's possible they are using estimates based on the 2010 to 2014 surveys from Census. I am in my own town of Guilford the population is definitely aging. It became more of a bedroom community for New Haven in the 1970's and that original influx has benn growing old together. Something similar may be going on in other towns, and that might make the estimates of population for older ages come out too low. I'm not sure. (John Burn-Murdoch of the *Financial Times* has pointed that that one needs to watch out for [issues with the denominators](https://threadreaderapp.com/thread/1447617110910382081.html) while comparing vaccination rates.)

#### Vaccination Rate Depends Both on the Population Denominator and the Vax Doses

As near as I can tell (and I may be wrong), DPH is using the population figures from the Census ACS from 2010-2014 (a five year average). The most recent ACS data I could fetch was for 2015-2019. I used that data to estimate the population by age by town. The plot below compares the effect of using either the DPH population estimate or the latest ACS estimate as the denominator when calculating the vaccination rate. It makes a noticeable difference. The town names are show for cases where the difference in population estimates is greater than 5%.

    [1] "ACS 2000-2014"

    # A tibble: 5 × 3
      age      estimate  pct   
      <fct>    <chr>     <chr> 
    1 Under 18 795,085   22.1% 
    2 18-44    1,233,666 34.3% 
    3 45-64    1,032,223 28.7% 
    4 65+      531,079   14.8% 
    5 Total    3,592,053 100.0%

    [1] "ACS 2005-2019"

    # A tibble: 5 × 3
      age      estimate  pct   
      <fct>    <chr>     <chr> 
    1 Under 18 743,833   20.8% 
    2 18-44    1,214,627 34.0% 
    3 45-64    1,015,561 28.4% 
    4 65+      601,053   16.8% 
    5 Total    3,575,074 100.0%
