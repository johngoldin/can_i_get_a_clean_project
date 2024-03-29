---
title: Tracking Covid-19 in Connecticut
author: John Goldin
date: '2020-06-22'
categories:
  - COVID19
tags:
  - COVID19
subtitle: "Summary of Daily Connecticut Report"
slug: covid-19-in-Connecticut-2
excerpt: "Summary of Connecticut Covid-19 based on Department of Public Health Data with some comparisons to national data. This has been updated each weekday during 2020 and most of 2021. There are also notes on sources of data for Covid-19 in Connecticut."
draft: no
output: 
  blogdown::html_page:
    # figure parameters based on recommendation in Hadley's book 
    toc: yes
    number_sections: false
    fig_width: 7
    out.width: "100%" 
    fig.align: "center"
    fig.asp: 0.618  
editor_options:
  markdown: 
    wrap: 72
---

<script src="{{< blogdown/postref >}}index.en_files/htmlwidgets/htmlwidgets.js"></script>
<script src="{{< blogdown/postref >}}index.en_files/jquery/jquery.min.js"></script>
<link href="{{< blogdown/postref >}}index.en_files/jquery-sparkline/jquery.sparkline.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index.en_files/jquery-sparkline/jquery.sparkline.js"></script>
<script src="{{< blogdown/postref >}}index.en_files/sparkline-binding/sparkline.js"></script>

## Latest Connecticut Data from the Department of Public Health

<style>html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#vprynqcgbh .gt_table {
  display: table;
  border-collapse: collapse;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 16px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#vprynqcgbh .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#vprynqcgbh .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#vprynqcgbh .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 0;
  padding-bottom: 4px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#vprynqcgbh .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#vprynqcgbh .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#vprynqcgbh .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#vprynqcgbh .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#vprynqcgbh .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#vprynqcgbh .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#vprynqcgbh .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#vprynqcgbh .gt_group_heading {
  padding: 8px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
}

#vprynqcgbh .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#vprynqcgbh .gt_from_md > :first-child {
  margin-top: 0;
}

#vprynqcgbh .gt_from_md > :last-child {
  margin-bottom: 0;
}

#vprynqcgbh .gt_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#vprynqcgbh .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 12px;
}

#vprynqcgbh .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#vprynqcgbh .gt_first_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
}

#vprynqcgbh .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#vprynqcgbh .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#vprynqcgbh .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#vprynqcgbh .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#vprynqcgbh .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#vprynqcgbh .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding: 4px;
}

#vprynqcgbh .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#vprynqcgbh .gt_sourcenote {
  font-size: 90%;
  padding: 4px;
}

#vprynqcgbh .gt_left {
  text-align: left;
}

#vprynqcgbh .gt_center {
  text-align: center;
}

#vprynqcgbh .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#vprynqcgbh .gt_font_normal {
  font-weight: normal;
}

#vprynqcgbh .gt_font_bold {
  font-weight: bold;
}

#vprynqcgbh .gt_font_italic {
  font-style: italic;
}

#vprynqcgbh .gt_super {
  font-size: 65%;
}

#vprynqcgbh .gt_footnote_marks {
  font-style: italic;
  font-size: 65%;
}
</style>
<div id="vprynqcgbh" style="overflow-x:auto;overflow-y:auto;width:auto;height:auto;"><table class="gt_table">
  <thead class="gt_header">
    <tr>
      <th colspan="4" class="gt_heading gt_title gt_font_normal" style>Latest Data on Covid-19 in Connecticut</th>
    </tr>
    <tr>
      <th colspan="4" class="gt_heading gt_subtitle gt_font_normal gt_bottom_border" style>Data as of  May 14, 2021</th>
    </tr>
  </thead>
  <thead class="gt_col_headings">
    <tr>
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1"></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1">total<br>to date</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1">since<br>yesterday</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1">since a<br>week ago</th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr>
      <td class="gt_row gt_left">Cases</td>
      <td class="gt_row gt_right">344,977</td>
      <td class="gt_row gt_right">+365</td>
      <td class="gt_row gt_right"> </td>
    </tr>
    <tr>
      <td class="gt_row gt_left">Deaths</td>
      <td class="gt_row gt_right">8,173</td>
      <td class="gt_row gt_right">+5</td>
      <td class="gt_row gt_right"> </td>
    </tr>
    <tr>
      <td class="gt_row gt_left">Currently in Hospital</td>
      <td class="gt_row gt_right">198</td>
      <td class="gt_row gt_right">-24</td>
      <td class="gt_row gt_right"> </td>
    </tr>
    <tr>
      <td class="gt_row gt_left">Tests</td>
      <td class="gt_row gt_right">8,991,905</td>
      <td class="gt_row gt_right">+32,583</td>
      <td class="gt_row gt_right"> </td>
    </tr>
    <tr>
      <td class="gt_row gt_left">Rate of positive tests</td>
      <td class="gt_row gt_right"></td>
      <td class="gt_row gt_right">0.9%</td>
      <td class="gt_row gt_right">NA%</td>
    </tr>
    <tr>
      <td class="gt_row gt_left"> </td>
      <td class="gt_row gt_right"></td>
      <td class="gt_row gt_right"> </td>
      <td class="gt_row gt_right"> </td>
    </tr>
    <tr>
      <td class="gt_row gt_left">Nursing home cases<sup class="gt_footnote_marks">1</sup></td>
      <td class="gt_row gt_right">8,672</td>
      <td class="gt_row gt_right"> </td>
      <td class="gt_row gt_right">+3</td>
    </tr>
    <tr>
      <td class="gt_row gt_left">Nursing home deaths</td>
      <td class="gt_row gt_right">2,719</td>
      <td class="gt_row gt_right"> </td>
      <td class="gt_row gt_right">+72</td>
    </tr>
  </tbody>
  <tfoot class="gt_sourcenotes">
    <tr>
      <td class="gt_sourcenote" colspan="4">Source: Multiple tables from <a href="https://data.ct.gov/stories/s/COVID-19-data/wa3g-tfvc/">Connecticut Open Data</a></td>
    </tr>
  </tfoot>
  <tfoot>
    <tr class="gt_footnotes">
      <td colspan="4">
        <p class="gt_footnote">
          <sup class="gt_footnote_marks">
            <em>1</em>
          </sup>
           
          Nursing home data are reported only weekly so the dates for "today" and a "week ago" are 06/19/2020 and 06/11/2020.
          <br />
        </p>
      </td>
    </tr>
  </tfoot>
</table></div>

There is a new [data tracker
map](https://portal.ct.gov/Coronavirus/COVID-19-Data-Tracker) that
displays the rate of cases in the last two weeks by town. It is
color-coded to indicate where cases are most prevalent.

[My post on Covid-19 back in
March](https://www.johngoldin.com/2020/03/covid-19-cases-in-connecticut/)
tracked the growth of the epidemic as it hit Connecticut. Back at the
end of March I did not realize that the greater New York area (including
Connecticut) would be the center of the first wave in the US. At that
time what I was reading focused on the nature of exponential growth of
an epidemic. We were urged to “flatten the curve” and that shaped the
way I presented the data in that post. I have been updating the figures
in that post each evening. During that time the [Connecticut data
portal](https://data.ct.gov/stories/s/COVID-19-data/wa3g-tfvc/) has
expanded considerably, and I’ve built [some R
code](https://github.com/johngoldin/ctcorona/blob/master/R/daily_ct_stats.R)
that let’s me easily update that post. I’ll use the same data
infrastructure for this post as well. This post is more oriented toward
tracking the current status of the epidemic in Connecticut.

## Tracking the Virus in Connecticut

This post focuses on what is happening currently. The aim is to use the
recent trend to get some idea of the near future. The first plot will
show the average number of new cases reported each day along with a line
that displays the rolling seven-day average. Typically there are
day-of-the-week effects in the reporting so it’s best to focus on the
seven-day average.

### New Covid-19 Cases in Connecticut

The plot shows the history of new cases and also shows the actions
required by some of Governor Lamont’s executive orders. <br/><br/><br/>

<div class="figure">

<img src="{{< blogdown/postref >}}index.en_files/figure-html/p-new-cases-1.png" alt="New Cases" width="672" />
<p class="caption">
Figure 1: New Cases
</p>

</div>

<br/><br/><br/>

<div class="figure">

<img src="{{< blogdown/postref >}}index.en_files/figure-html/p-rt-live-1.png" alt="Estimated R&lt;sub&gt;t&lt;/sub&gt;" width="672" />
<p class="caption">
Figure 2: Estimated R<sub>t</sub>
</p>

</div>

<br/>

### Covid-19 Deaths in Connecticut

<div class="figure">

<img src="{{< blogdown/postref >}}index.en_files/figure-html/p-daily-deaths-1.png" alt="Daily Deaths" width="672" />
<p class="caption">
Figure 3: Daily Deaths
</p>

</div>

<br/>

### Connecticut Covid-19 Patients in Hospital

<div class="figure">

<img src="{{< blogdown/postref >}}index.en_files/figure-html/p-hospitalizations-1.png" alt="Covid-19 Patients in Hospital" width="672" />
<p class="caption">
Figure 4: Covid-19 Patients in Hospital
</p>

</div>

<br/> The number of new cases peaked in mid April and then began to
decrease rapidly, although not as rapidly as it increased. A key issue
is how fast epidemic is expanding or contracting. One indicator of that
is to estimate the parameter R<sub>t</sub>, the average number of people
who become infected by an infectious person. When R<sub>t</sub> is
greater than 1 the number of daily new cases is increasing, If
R<sub>t</sub> is less than 1, it is decreasing. See the site
[covidestim · COVID-19 nowcasting](https://covidestim.org) for an estimate by state of the effective
value for R<sub>t</sub>. The site is described in [this
article](https://www.vox.com/recode/2020/4/21/21227855/coronavirus-spreading-by-state-instagram-effective-reproduction-rate)
at Vox.com. I don’t claim to have the expertise to evaluate the quality
of the calculation of R at the [covidestim](https://covidestim.org) site, but it
seems to jive with other information about the pattern of the epidemic
among states.

As of June (and a month previous), Connecticut, New York, and New Jersey
have among the lowest values for R<sub>t</sub> in the country. This is
good news for us in Connecticut. I have included R<sub>t</sub> for
Arizona as well as Connecticut to provide a contrast with a state that
has lately shown [signs of a growing
outbreak](https://www.fox10phoenix.com/news/arizona-medical-experts-alarmed-over-surge-in-covid-19-cases).
The goal in Connecticut and in the entire New York City area is to keep
R<sub>t</sub> well under 1. As of
05/16/2021 R<sub>t</sub> is
0.77.
On the other hand, in Arizona R<sub>t</sub> is about
0.91.

## Comparisons with Other States

### Estimate of R<sub>t</sub> by State (from [covidestim · COVID-19 nowcasting](https://covidestim.org))

The next display shows the trend of R<sub>t</sub> in each state arranged
according to geographic position in the US. Remember that R<sub>t</sub>
is a measure of the rate of increase. When R<sub>t</sub> is greater than
1 the number of daily new cases is increasing, If R<sub>t</sub> is less
than 1, it is decreasing. The color of the R line shows whether the most
recent estimate of R for a state is <span style="color: #af8dc3">above 1 (purple
line)</span> or <span style="color: #7fbf7b">equal or below 1 (green
line)</span>. <br/><br/>

<div class="figure">

<img src="{{< blogdown/postref >}}index.en_files/figure-html/p-rt-map-1.png" alt="Estimate of R&lt;sub&gt;t&lt;/sub&gt; by State" width="95%" />
<p class="caption">
Figure 5: Estimate of R<sub>t</sub> by State
</p>

</div>

<br/> R is estimated from the state data and the gray area around the
line indicates the statistical uncertainty of the estimate showing an
95% confidence interval. Note that this map shows only whether
transmission seems to be growing or shrinking. How concerned one should
be about the epidemic in a particular state also depends on the
prevalence of cases.

### Trends in New Cases by State

The next map shows the history of new cases in each state per 100K of
population. The lines are color coded the same as in the previous map to
indicate whether the most recent estimate of R for a state is <span style="color: #af8dc3">above 1
(purple line)</span> or <span style="color: #7fbf7b">equal or below 1 (green
line)</span>. <br/><br/>

<div class="figure">

<img src="{{< blogdown/postref >}}index.en_files/figure-html/p-states-map-1.png" alt="New Cases per 100K by State" width="95%" />
<p class="caption">
Figure 6: New Cases per 100K by State
</p>

</div>

<br/> The tallest graphs of new cases per 100K of population are New
York and Arizona.. From the point of view of someone living in
Connecticut, the striking thing is how thoroughly Connecticut (and New
York, New Jersey, Rhode Island, and Massachusetts) have recovered from
the peak. New cases are low and the low value of the estimate of R
confirms that they are likely to decrease even more. The great contrast
is with the increase of cases in some of the southern states.
<br/><br/><br/>

## Connecticut Covid-19 Deaths and Cases by Age

<div style="float: left; width: 50%; padding: 5PX;">

<div class="figure">

<img src="{{< blogdown/postref >}}index.en_files/figure-html/deaths-by-age2-1.png" alt="Covid-19 Deaths by Age" width="672" />
<p class="caption">
Figure 7: Covid-19 Deaths by Age
</p>

</div>

</div>

<div style="float: right; width: 50%; padding: 5PX;">

<div class="figure">

<img src="{{< blogdown/postref >}}index.en_files/figure-html/deaths-per-100k2-1.png" alt="Covid-19 Cases by Age" width="672" />
<p class="caption">
Figure 8: Covid-19 Cases by Age
</p>

</div>

</div>

<br/>

Deaths increase with age, as has been well known since the beginning of
the epidemic. For cases, the number of cases per population stays
relatively flat from 20 to 79 and rises very rapidly for the oldest
category. I haven’t examined this data closely, but I assume this
pattern is related to the high rates of mortality in nursing homes. For
the age range from 60 to 79 there probably are a lot of seniors who are
going to a great deal of trouble avoiding places and situations where
there is risk of catching the virus. But individuals in nursing homes
don’t have that much control over their own lives. I would guess that
the older population outside of nursing homes has a lower rate of
catching the virus and the population inside nursing homes has a higher
rate. The two trends may average out to a rate that is the same as
middle aged adults. This is just speculation. I haven’t dug into the
data to say anything firm about this

## Nursing Homes

Nursing homes have been hard hit by the epidemic. It’s hard to control
coronavirus outbreak in a group living situation, which includes prisons
and cruises ship. On top of that, Covid-19 is especially serious for the
elderly. The combination in nursing homes has been deadly. There have
been 2,719 deaths in Connecticut
Nursing Homes which makes
33.3%
of the total of
8,173
deaths from Covid-19.

## Prisons

Prisons even more than nursing homes create a situation where it is hard
to limit exposure among individuals living together. We have less
information about prisons than about nursing homes. The Department of
Corrections (DOC) posts some statistics on [total Covid19 rates among
prisoners and
staff](https://data.ct.gov/Public-Safety/COVID-19-in-Correctional-Facilities/6t8i-du3u)
via the state open data site and some limited information of [rates by
individual
facility](https://portal.ct.gov/DOC/Common-Elements/Common-Elements/Health-Information-and-Advisories)
on their web site, but the data are not as detailed or as accessible as
the data on nursing homes.

As of 05/14/2021,
4,469 inmates
have tested positive for Covid-19. At the peak of the epidemic,
158 inmates
were isolated at the Northern Correctional Institution medical facility.
The most recent report is that
19
died, and currently
NA
Covid-19 inmates remain in that medical facility.

Unlike nursing homes, the number of deaths from Covid-19 in prisons is
relatively low. Presumably that is because the prison population has
many fewer elderly people who are especially vulnerable to the effects
of Covid-19.

In addition to prisoners, the Department of Corrections reports that
1,670 staff
have tested positive for Covid-19, of whom
1,649 have been
cleared to return to work.

One cannot easily relate the number of cases reported by the Department
of Corrections to the town by town counts reported by the Department of
Public Health. It’s clear that for small rural towns the prison cases
may swamp the community counts in those towns. For example, in the town
of Brooklyn in Windham County (population about 8,200) the DPH town
stats between June 17 and June 18 showed the number of cases jumped from
24 to 116. That’s the home of the Brooklyn Correctional Institution and
I have to believe that site dominated those numbers and that the process
by which the Department of Corrections reported test results to the
Department of Public Health affected the magnitude of the one-day jump.

In effect there is a separate epidemic occurring inside the prison
system and the pace of that epidemic does not necessarily correspond to
trends in the wider community. For the purposes of tracking Covid-19 in
the population of Connecticut generally, in some cases I will exclude
some of the small rural towns with prisons such as Somers, Montville,
and Brooklyn. But it’s not practical for me to segregate the effect of
prisons on counts for larger towns such as New Haven, Cheshire,
Hartford, and others. As of 6/16/2020, the DOC reported a cumulative
total of 117 cases among prisoners in Bridgeport, 125 in New Haven, 94
in Hartford, and 21 in Cheshire. Enfield is a tricky case. There are two
DOC facilities in Enfield and as of 6/16/2020 DOC reported 265 cases
there. Enfield has a population of about 44,000, but the prison cases
may have a significant effect on the picture of Covid-19 in Enfield.
Similar to Brooklyn, one can see likely effects in the reports. On
6/10/20 DPH reported a total of 447 Covid-19 cases in Enfield and the
next day on 6/11/2020 they reported 546, and increase of 22% in one day.
That’s highly likely to be an effect of how cases were reported from the
DOC facilities in Enfield and how those reports reached the Department
of Public Health.

## Variations by County in Connecticut

Next I’ll look at variations within Connecticut. Below are two maps
showing the eight counties in Connecticut[^1]. The first map in Figure
<a href="#fig:county-maps">9</a> shows the cumulative total of cases since the
start of the epidemic. The second map shows only new cases reporting
during the last two weeks. On both maps, cases are adjusted to show
cases per 100K of population. So the first map relates more to the total
impact of the disease over the full course of the epidemic to date, and
the second map is an indication of the recent prevalence of the virus.

Connecticut is part of the epidemic’s surge in the New York area and the
magnitude of the epidemic has been greater in the counties closer to New
York City. Back in March cases first appeared in Fairfield County and
then spread to Litchfield, New Haven, and Hartford. More recently
Hartford has been the area that we have to watch.

<br/><br/><br/>

<div class="figure">

<img src="{{< blogdown/postref >}}index.en_files/figure-html/county-maps-1.png" alt="County Maps of New and of Cumulative Cases" width="50%" /><img src="{{< blogdown/postref >}}index.en_files/figure-html/county-maps-2.png" alt="County Maps of New and of Cumulative Cases" width="50%" />
<p class="caption">
Figure 9: County Maps of New and of Cumulative Cases
</p>

</div>

### By County and Type of Town

There are 169 towns in Connecticut, which makes it hard to examine
variations by town. To help examine variations within counties, I’ll use
a typology of towns called [The Five
Connecticuts](https://ctdatahaven.org/sites/ctdatahaven/files/UConnCPR%20Changing%20Demographics-5%20CTs%202004.pdf)
that divides towns into five categories based on census variables: Urban
Core, Urban Periphery, Suburban, Rural, and a fifth category for Wealthy
Suburbs used for some towns in Fairfield County. Adjusting for
population, the number of cases has been greater in the counties closer
to New York City. In the figure below I’ll fold the wealthy towns into
the Suburban category. I have excluded Montville and Somers because the
prisons in those towns complicates interpretation of the town
statistics.

Counties are laid out from top to bottom and the counties closer to New
York are toward the top. The columns show the four categories. Urban
towns have been hit harder than suburban and rural towns. While density
may have some effect on case rates, the report [Towards Health Equity in
Connecticut: The Role of Social Inequality and the Impact of
COVID-19](https://ctdatahaven.org/reports/towards-health-equity-connecticut)
by DataHaven documents how the epidemic interacts with existing social
inequality in Connecticut. <br/>

<div class="figure">

<img src="{{< blogdown/postref >}}index.en_files/figure-html/county-by-category-1.png" alt="Cases by County" width="672" />
<p class="caption">
Figure 10: Cases by County
</p>

</div>

### Details by Town

The links below take you to a separate HTML page for each Connecticut
county. That page contains a table with one row for each town in the
county.

For each town it shows the category, the population, the total number of
cases to date, the number of recent cases per 100K of population (total
new cases in the last two weeks), total deaths, and the percentage of
total deaths in that town attributed to nursing home residents.

Next there are two [sparklines](https://en.wikipedia.org/wiki/Sparkline)
that show the trend in daily new cases and daily deaths (based on 14 day
moving average). Cases and deaths are shown as a ratio to population in
the town.

The purpose of these tables is to make it easier to quickly scan for
trends in local towns. Here is sample (based on my home of Guilford)
showing what is available for each town.

For each county there is also a map showing the towns in that county and
the relative number of total cases in the town and a second map that
shows the percentage of individuals who are below the poverty line.

The town sparklines at the right show the trends over time. The vertical
scale is different for new cases and for deaths. For new cases, the
maximum height shown on the scale is 100 while
for deaths, the maximum value shown is 23.7.
For both new cases and deaths, the sparkline shows the rolling seven day
average of new cases or deaths.

<div><table class="table table-condensed">
 <thead>
  <tr>
   <th style="text-align:left;"> town </th>
   <th style="text-align:left;"> category </th>
   <th style="text-align:right;"> total population </th>
   <th style="text-align:right;"> total cases </th>
   <th style="text-align:right;"> recent cases per 100K </th>
   <th style="text-align:right;"> total deaths </th>
   <th style="text-align:right;"> % deaths from nursing homes </th>
   <th style="text-align:center;"> town cases </th>
   <th style="text-align:center;"> town deaths </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> Guilford </td>
   <td style="text-align:left;"> Suburban </td>
   <td style="text-align:right;"> 22,285 </td>
   <td style="text-align:right;"> 1,433 </td>
   <td style="text-align:right;"> NA </td>
   <td style="text-align:right;"> 35 </td>
   <td style="text-align:right;"> 82% </td>
   <td style="text-align:center;"> <span id="htmlwidget-1" class="sparkline html-widget"></span>
<script type="application/json" data-for="htmlwidget-1">{"x":{"values":[0.747887218607434,1.9231385621334,1.9231385621334,1.9231385621334,3.8462771242668,5.1283694990224,7.69255424853361,10.8977851854226,11.5388313728004,12.820923747556,14.7440623096894,12.820923747556,14.1030161223116,11.5388313728004,11.5388313728004,11.5388313728004,10.2567389980448,10.2567389980448,13.4619699349338,11.5388313728004,11.5388313728004,13.4619699349338,11.5388313728004,12.820923747556,12.1798775601782,8.33360043591141,7.69255424853361,13.4619699349338,8.33360043591141,8.97464662328921,8.33360043591141,8.97464662328921,9.61569281066701,10.2567389980448,4.4873233116446,5.1283694990224,5.76941568640021,5.1283694990224,3.205230936889,3.8462771242668,2.5641847495112,2.5641847495112,2.5641847495112,2.5641847495112,3.8462771242668,4.4873233116446,3.205230936889,4.4873233116446,5.76941568640021,5.76941568640021,4.4873233116446,3.205230936889,3.205230936889,2.5641847495112,2.5641847495112,1.2820923747556,0.641046187377801,0.641046187377801,0.641046187377801,0,0.641046187377801,0,0.641046187377801,1.9231385621334,1.9231385621334,1.9231385621334,2.5641847495112,3.205230936889,2.5641847495112,1.9231385621334,0.641046187377801,1.9231385621334,1.2820923747556,0.641046187377801,0.641046187377801,0.641046187377801,1.2820923747556,0.641046187377801,-0.641046187377801,0,0.641046187377801,0,0.641046187377801,0,1.2820923747556,1.2820923747556,1.9231385621334,1.2820923747556,1.2820923747556,1.2820923747556,0.641046187377801,0.641046187377801,0.641046187377801,0,0,0,0,1.79492932465784,0.897464662328921,0.897464662328921,0.897464662328921,0.897464662328921,0.897464662328921,0.897464662328921,0,0.897464662328921,1.79492932465784,1.79492932465784,2.69239398698676,2.69239398698676,2.69239398698676,2.69239398698676,1.79492932465784,0.897464662328921,0,-0.897464662328921,-0.897464662328921,-0.897464662328921,0,3.58985864931568,3.58985864931568,5.38478797397353,5.38478797397353,5.38478797397353,5.38478797397353,4.4873233116446,0.897464662328921,0,-0.897464662328921,-0.897464662328921,-0.897464662328921,-0.897464662328921,-0.897464662328921,-0.897464662328921,0,0.897464662328921,0.897464662328921,0.897464662328921,0.897464662328921,0.897464662328921,0.897464662328921,0.897464662328921,0,0,0,0,0,0,0,0.897464662328921,0.897464662328921,0.897464662328921,0.897464662328921,3.58985864931568,5.38478797397353,7.17971729863137,7.17971729863137,8.97464662328921,8.97464662328921,8.97464662328921,7.85281579537806,10.0964774512004,8.97464662328921,8.97464662328921,10.0964774512004,10.0964774512004,10.0964774512004,14.3594345972627,10.7695759479471,9.87211128561813,8.97464662328921,7.17971729863137,7.17971729863137,7.17971729863137,0.897464662328921,0.897464662328921,1.79492932465784,2.69239398698676,1.79492932465784,1.79492932465784,1.79492932465784,1.79492932465784,2.69239398698676,0.897464662328921,0,0.897464662328921,0.897464662328921,0.897464662328921,1.79492932465784,0.897464662328921,2.69239398698676,1.79492932465784,1.79492932465784,1.79492932465784,1.79492932465784,1.79492932465784,0.897464662328921,1.79492932465784,3.58985864931568,4.4873233116446,4.4873233116446,4.4873233116446,8.07718196096029,9.87211128561813,8.07718196096029,8.07718196096029,6.28225263630245,6.28225263630245,6.28225263630245,8.97464662328921,10.7695759479471,12.5645052726049,21.5391518958941,23.3340812205519,23.3340812205519,23.3340812205519,21.5391518958941,19.7442225712363,17.9492932465784,11.667040610276,12.5645052726049,12.5645052726049,12.5645052726049,12.5645052726049,13.4619699349338,21.5391518958941,20.6416872335652,31.4112631815122,31.4112631815122,31.4112631815122,30.5137985191833,32.3087278438411,25.1290105452098,25.1290105452098,15.2568992595917,15.2568992595917,15.2568992595917,15.2568992595917,12.5645052726049,17.9492932465784,19.0711240744896,25.8021090419565,25.8021090419565,25.8021090419565,45.9950639443572,61.7006955351133,62.8225263630245,75.3870316356294,73.5921023109715,73.5921023109715,73.5921023109715,70.0022436616558,68.207314336998,62.8225263630245,48.4630917657617,74.4895669733004,74.4895669733004,74.4895669733004,83.4642135965896,78.0794256226161,86.1566075835764,78.0794256226161,49.3605564280906,49.3605564280906,49.3605564280906,46.6681624411039,50.2580210904196,47.5656271034328,50.2580210904196,57.2133722234687,57.2133722234687,57.2133722234687,78.5281579537806,74.040834642136,75.1626654700471,75.1626654700471,75.1626654700471,75.3870316356294,75.3870316356294,61.9250617006955,66.4123850123401,70.0022436616558,83.4642135965896,85.2591429212475,87.0540722459053,87.0540722459053,80.7718196096029,82.5667489342607,81.6692842719318,71.7971729863137,64.6174556876823,64.6174556876823,64.6174556876823,74.4895669733004,70.0022436616558,66.4123850123401,67.3098496746691,64.6174556876823,64.6174556876823,64.6174556876823,52.9504150774063,48.4630917657617,51.1554857527485,44.873233116446,41.2833744671304,41.2833744671304,41.2833744671304,34.103657168499,43.9757684541171,37.6935158178147,33.2061925061701,35.0011218308279,35.0011218308279,35.0011218308279,39.4884451424725,26.0264752075387,24.2315458828809,30.5137985191833,25.1290105452098,25.1290105452098,25.1290105452098,35.8985864931568,40.3859098048014,43.0783037917882,40.3859098048014,43.9757684541171,43.9757684541171,43.9757684541171,28.7188691945255,28.7188691945255,32.3087278438411,32.3087278438411,36.7960511554857,36.7960511554857,36.7960511554857,40.3859098048014,39.4884451424725,37.6935158178147,40.3859098048014,39.4884451424725,39.4884451424725,39.4884451424725,33.2061925061701,35.0011218308279,35.0011218308279,32.3087278438411,35.0011218308279,35.0011218308279,35.0011218308279,35.0011218308279,34.103657168499,33.2061925061701,34.103657168499,36.7960511554857,36.7960511554857,36.7960511554857,46.6681624411039,55.6428090643931,54.7453444020642,63.7199910253534,62.8225263630245,62.8225263630245,62.8225263630245,55.6428090643931,51.1554857527485,45.770697778775,38.5909804801436,31.4112631815122,31.4112631815122,31.4112631815122,28.7188691945255,23.3340812205519,33.2061925061701,32.3087278438411,32.3087278438411,32.3087278438411,32.3087278438411,30.5137985191833,44.873233116446,39.4884451424725,36.7960511554857,33.2061925061701,33.2061925061701,33.2061925061701,41.2833744671304,26.9239398698676,26.9239398698676,26.0264752075387,25.1290105452098,25.1290105452098,25.1290105452098,24.2315458828809,20.6416872335652,17.9492932465784,17.0518285842495,17.9492932465784,17.9492932465784,17.9492932465784,6.28225263630245,4.4873233116446,6.28225263630245,8.07718196096029,5.38478797397353,5.38478797397353,5.38478797397353,3.36549248373345,8.97464662328921,7.85281579537806,4.4873233116446,5.60915413955576,6.28225263630245],"options":{"chartRangeMin":0,"chartRangeMax":100,"height":20,"width":60},"width":60,"height":20},"evals":[],"jsHooks":[]}</script> </td>
   <td style="text-align:center;"> <span id="htmlwidget-2" class="sparkline html-widget"></span>
<script type="application/json" data-for="htmlwidget-2">{"x":{"values":[0,0,0,0,0,0,0,0,0,0,0,0.641046187377801,0.641046187377801,0.641046187377801,0.641046187377801,0.641046187377801,0.641046187377801,0.641046187377801,0,0,0,0,0,0,0,0,0,0,0,0.641046187377801,0.641046187377801,0.641046187377801,0.641046187377801,1.2820923747556,2.5641847495112,3.205230936889,3.205230936889,3.8462771242668,3.8462771242668,3.8462771242668,2.5641847495112,1.2820923747556,0.641046187377801,0,0,0,0,1.2820923747556,1.2820923747556,1.2820923747556,1.9231385621334,1.2820923747556,1.2820923747556,1.2820923747556,0.641046187377801,1.2820923747556,1.2820923747556,0.641046187377801,0.641046187377801,0.641046187377801,0.641046187377801,0.641046187377801,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0.897464662328921,0.897464662328921,0.897464662328921,0.897464662328921,0.897464662328921,0.897464662328921,0.897464662328921,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0.897464662328921,0.897464662328921,0.897464662328921,0.897464662328921,0.897464662328921,0.897464662328921,0.897464662328921,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0.897464662328921,0.897464662328921,0.897464662328921,1.79492932465784,1.79492932465784,1.79492932465784,1.79492932465784,0.897464662328921,0.897464662328921,4.4873233116446,4.4873233116446,4.4873233116446,4.4873233116446,5.60915413955576,6.73098496746691,6.73098496746691,2.2436616558223,2.2436616558223,2.69239398698676,2.69239398698676,2.69239398698676,2.69239398698676,2.69239398698676,2.69239398698676,2.2436616558223,1.79492932465784,1.79492932465784,0.897464662328921,0.897464662328921,2.69239398698676,3.58985864931568,4.4873233116446,4.4873233116446,4.4873233116446,4.4873233116446,3.58985864931568,1.79492932465784,0.897464662328921,0,0,0,0,0,0,0,0,0,0,0.897464662328921,0.897464662328921,0.897464662328921,0.897464662328921,0.897464662328921,0.897464662328921,0.897464662328921,0,0,0,0,0.897464662328921,0.897464662328921,0.897464662328921,0.897464662328921,0.897464662328921,0.897464662328921,0.897464662328921,0,0,0,0,0,0,0.897464662328921,0,0,0,0,0,0,-0.897464662328921,0,0,0,0,0,0,0,0,0,0,0.897464662328921,0.897464662328921,0.897464662328921,0.897464662328921,1.79492932465784,1.79492932465784,1.79492932465784,0.897464662328921,0.897464662328921,0.897464662328921,0.897464662328921,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0.897464662328921,0.897464662328921,0.897464662328921,0.897464662328921,0.897464662328921,0.897464662328921,0.897464662328921,0,0,0,0,0,0.897464662328921],"options":{"chartRangeMin":0,"chartRangeMax":23.7201027871121,"height":20,"width":60},"width":60,"height":20},"evals":[],"jsHooks":[]}</script> </td>
  </tr>
</tbody>
</table></div>

### Links to Summary Page for Each Connecticut County

Below are links to a separate web page by for each of the eight counties
in Connecticut. Click on the county name for detail about individual
towns within that county.

|                                                                                                               |                                                                                                             |                                                                                                             |                                                                                                               |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [Litchfield County](/post/2020-06-22-tracking-covid-19-in-connecticut/index.en_files/litchfield_summary.html) | [Hartford County](/post/2020-06-22-tracking-covid-19-in-connecticut/index.en_files/hartford_summary.html)   | [Tolland County](/post/2020-06-22-tracking-covid-19-in-connecticut/index.en_files/tolland_summary.html)     | [Windham County](/post/2020-06-22-tracking-covid-19-in-connecticut/index.en_files/windham_summary.html)       |
| [Fairfield County](/post/2020-06-22-tracking-covid-19-in-connecticut/index.en_files/fairfield_summary.html)   | [New Haven County](/post/2020-06-22-tracking-covid-19-in-connecticut/index.en_files/new_haven_summary.html) | [Middlesex County](/post/2020-06-22-tracking-covid-19-in-connecticut/index.en_files/middlesex_summary.html) | [New London County](/post/2020-06-22-tracking-covid-19-in-connecticut/index.en_files/new_london_summary.html) |

<br/>

------------------------------------------------------------------------

<br/>

## Where Do Things Stand Today?

As I write this on July 4, Connecticut seems to be in relatively good
shape. [Covid ActNow](https://covidactnow.org/?s=61890) shows it as one
of only three states “on track to contain COVID” along with
Massachusetts and Vermont.  
It won’t be easy to sustain that situation. Some of our fellow
northeastern states have also done well but are struggling to maintain
their success.

I started burrowing into the Covid-19 data back in March in part because
I’m a 70 year old male who therefore is at high risk (and because I love
to work in R and I’m always looking for an excuse). The situation in
Connecticut looks and feels very different than it did in March-April.
One amazing feature of this epidemic is how differently it affects
subsets of the population. As a financially comfortable semi-retiree, it
was quite easy for me to hide from the virus by hiding from people in
general. Many, many people were not so fortunate. If you can get out of
the way of the virus, you do it. But if economic circumstances force you
to work face to face or if you are confined to a group living situation
or if where you live forces you to mingle with multiple generations and
multiple networks of interactions, it is much harder to avoid the virus.
I’m equally shocked by how the economic effects hit individuals in
dramatically different ways. For someone in my circumstances there is
almost no effect. Meanwhile many people face economic ruin that will
affect them for the rest of their lives. The virus and its effects
cannot be contained by uncoordinated individual efforts. It takes
collective will and collective action. Many individuals are coping, but
collectively we are failing.

It is tragic watching the virus explode in the south and southwest. New
York and others showed that you can get it back under control, but it
took a maximum concerted effort. There is no sign that going to happen
in many parts of the country. <br/>

## Links to Sources

-   State of Connecticut Department of Public Health

    -   Daily Covid-19 Update in the form of a PDF. A [list of the
        reports](https://data.ct.gov/Health-and-Human-Services/COVID-19-Daily-DPH-Reports-Library/bqve-e8um)
        is available via Connecticut Open Data.
    -   [Connecticut Covid-19 Data
        Tracker](https://portal.ct.gov/Coronavirus/COVID-19-Data-Tracker)
    -   Links to [all Covid-19 items available via Connecticut Open
        Data](https://data.ct.gov/stories/s/COVID-19-data/wa3g-tfvc/#data-library)

    The [Connecticut Open Data](https://data.ct.gov) site is a
    tremendous resource and I expect to use it for other projects in the
    future. The RSocrata package made it very easy to download this
    data. It’s run by Connecticut’s [Chief Data
    Officer](https://portal.ct.gov/OPM/Secr-General/Data-and-Analytics-Policy/Chief-Data-Officer)
    under the auspices of the Office of Policy and Management. They have
    produced a high-quality data portal.

-   [Yale community Covid-19
    Statistics](https://covid19.yale.edu/yale-covid-19-statistics)

-   [Mapping and Covid-19 at the Yale Medical
    School](https://covid.yale.edu/innovation/mapping/) I have had an
    opportunity to observe some of these efforts for me it has been a
    great source of information and inspiration.

-   [DataHaven](https://ctdatahaven.org/reports/covid-19-connecticut-data-analysis)
    provides some Connecticut-focused information on Covid-19. They also
    published a
    [report](https://ctdatahaven.org/reports/towards-health-equity-connecticut)
    on how Covid-19 relates to existing inequalities in Connecticut.

-   [CTData Collaborative](https://www.ctdata.org/covid19) also provides
    data on Covid-19 and its impact in Connecticut.

-   [New Haven Covid Site](https://covid19.newhavenct.gov)

-   [Connecticut COVID-19 Wastewater
    Project](https://covidtrackerct.com/wastewater-report/) Report on
    test results on New Haven area sewage.

-   [Yale SARS-CoV-2 Genomic Surveillance
    Initiative](https://covidtrackerct.com/portfolio/current/) Genomic
    sequencing of some cases in Connecticut.

-   [COVID Tracking Project](https://covidtracking.com) The data for
    Figure <a href="#fig:p-states-map">6</a> is from [COVID Tracking
    Project](https://covidtracking.com/data) and is used under a
    Creative Commons CC BY-NC-4.0 license.

-   [New York Times Tracking the
    Coronavirus](https://www.nytimes.com/interactive/2020/world/coronavirus-maps.html)

-   For Rt I am [using covidestim · COVID-19 nowcasting](https://covidestim.org). I previously used [rt.live](https://rt.live), but they stopped doing estimates and
    referred me to Covid-19 nowcasting.

-   [Covid ActNow](https://covidactnow.org/?s=61890) I only learned
    about this project today, but it seems quite interesting.

-   [CovidTrackCT](https://covidtrackerct.com/portfolio/current/) uses
    genetic sequence mapping to trace what strains have they have seen
    in Connecticut. This shows connection to New York and continued
    local transmission within Connectiut.

## Methodology and Notes

### Code Used to Produce This Post

The R code used to download and process the data from Connecticut and
elsewhere is in the file
[daily\_ct\_stats](https://github.com/johngoldin/ctcorona/blob/master/R/daily_ct_stats.R).
This post was created using RMarkdown so the code to create most of the
figures is in the [.Rmd file for this
post](https://github.com/johngoldin/can_i_blog_too/blob/master/content/post/2020-06-22-tracking-covid-19-in-connecticut/index.en.Rmd).

The separate HTML files for each Connecticut county were created using
the [rmarkdown::render
function](https://github.com/johngoldin/ctcorona/blob/master/R/render_town_summary_html.R).
The RMarkdown document that actually formatted the town details
(including sparklines and county maps) is
[here](https://github.com/johngoldin/ctcorona/blob/master/code/county_summary.Rmd).

Some noteworthy packages used here:

-   [geofacet](https://hafen.github.io/geofacet/) used to create the map
    of US states in Figures <a href="#fig:p-rt-map">5</a> and
    <a href="#fig:p-states-map">6</a>.

-   [tidycensus](https://walker-data.com/tidycensus/) used to create the
    Connecticut maps and retrieve Census data (most of which I didn’t
    use).

-   [sparkline](https://github.com/htmlwidgets/sparkline)

-   [formattable](https://www.displayr.com/formattable/) – Used to
    create the town-by-town detail tables primarily because this was the
    only tool I found that would readily add a sparkline to a table.

### Some Notes on the Data Available From the Department of Public Health

Sometimes there is a lag before cases and deaths end up in the daily
reports. As a result, there tends to be a “day of the week” effect. For
that reason, observers of the Covid-19 statistics generally focus on a
7-day rolling average of the daily counts. Some of the unusually large
peaks and valleys in these charts are due to reporting process. The DPH
has also begun producing reports based on the [date a sample was taken
for a
test](https://data.ct.gov/Health-and-Human-Services/Number-of-COVID-19-Cases-by-Date-of-Specimen-Colle/xz44-6swc)
and [by the date of
death](https://data.ct.gov/Health-and-Human-Services/COVID-19-associated-deaths-by-date-of-death/abag-bjkj).
That’s a more accurate way to look at the change over time, but it means
the data for the most recent days are hard to interpret because some
data may be “in process” and not yet reported. In these charts I have
used “date of report” rather than “date of sample taken” or “date of
death” because that gives me all of the recent data that is available
and because that is what most other data projects (such as the COVID
Tracking Project or the New York Times) have been using.

The DPH reports always include a comment that “all data are preliminary
and subject to change.” But when they make and adjustment to correct
errors, as far as I can tell they do not go back and adjust the earlier
reports. That can lead to a misleading report of recent changes. For
example, in one note below they removed 70 cases because of errors on a
day in which there were 81 new cases. In the data series that I
download, that shows up as having been 11 new cases that day, not 81,
because 70 were removed. Earlier days are not corrected.

[Note as of June
1](https://portal.ct.gov/-/media/Coronavirus/CTDPHCOVID19summary6012020.pdf?la=en)

> \*In Connecticut during the early months of this pandemic, it became
> increasingly clear that it would be necessary to track probable
> COVID-19 cases and deaths, in addition to laboratory-confirmed (RT-
> PCR) cases and deaths. This was needed to better measure the burden
> and impact of this disease in our communities and is now part of the
> national surveillance case definition for COVID-19. Today for the
> first time, DPH is reporting cases and deaths as “confirmed” or
> “probable.” Previous reports reported these as a combined number. The
> only change today is that they are being separated to conform with CDC
> reporting guidance. Probable cases of COVID-19 involve persons who
> have not had confirmatory laboratory testing (RT-PCR) performed for
> COVID-19, but whose symptoms indicate they are very likely to have a
> COVID-19 infection. In Connecticut, most of the probable COVID-19
> cases involve persons whose death certificates list COVID-19 disease
> or SARS-CoV-2 as a cause of death or a significant condition
> contributing to death.

[Note as of May
27](https://portal.ct.gov/-/media/Coronavirus/CTDPHCOVID19summary5272020.pdf?la=en)

> The staff at the Department of Public Health have removed 356 cases
> and 808 tests in the past 24 hours, which were identified as
> duplicates in the system, affecting both test and overall case
> numbers. Since yesterday, there have been 341 new positive cases, and
> 5,215 new tests were reported.

[Note as of June
18](https://portal.ct.gov/-/media/Coronavirus/CTDPHCOVID19summary6182020.pdf)

> Please note that 81 new cases were reported in the past 24-hours; 70
> previously reported cases were removed from the total counts due to
> correction of data errors.

In the data portal, the number of cases reported for Montville was 381
on June 17. As of June 18 it reports 293 cases, a reduction of 88 cases.
That’s more than the 70 cases removed. Perhaps the case counts for
Montville were affected by inmates being moved within the Connecticut
prison system.

[Note as of June 24,
2020](https://portal.ct.gov/-/media/Coronavirus/CTDPHCOVID19summary6242020.pdf)

> 1175 new test results were reported since the last report and 2770
> previously reported PCR tests were removed due to correction of data
> errors.

[Note as of July 23,
2020](https://portal.ct.gov/-/media/Coronavirus/CTDPHCOVID19summary7232020.pdf)

> \*Please note 83 new cases were reported to DPH since yesterday. In
> addition, 74 previously reported cases were removed due to updated
> laboratory findings of false positive results.

*July 24, 2020*: [Governor’s press
release](https://portal.ct.gov/Office-of-the-Governor/News/Press-Releases/2020/07-2020/Governor-Lamont-Coronavirus-Update-July-24)

> \*NOTE: Today’s update includes a large set of data provided by an
> out-of-state lab on tests that were conducted on Connecticut residents
> between May 23 and July 20 and not reported to the State of
> Connecticut until today. This data set provided by the out-of-state
> lab includes approximately 12,000 tests, 440 of which were positive.
> The remaining 104 positive cases in today’s report are newly reported
> cases in the day-to-day update, giving a 0.79% positivity rate for the
> day.

See also [Hartford Courant, July 24,
2020](https://www.courant.com/coronavirus/hc-news-coronavirus-daily-numbers-0724-20200724-cqtkcw4zzraenoz5kbw5wxckmy-story.html)
I don’t see any explanation of this in the Department of Public Health
PDF, but it was clear that an increase of 544 cases in one day would be
remarkable.

> On Friday, the state also announced a backlog of unreported test
> results for Connecticut residents dating back to mid-May. Among these
> approximately 12,000 tests, 440 were positive. On Thursday, the state
> reported an additional 13,000 tests. With the 544 new cases, the state
> has now recorded 48,776 coronavirus cases.

[July 29, 2020 press
release](https://portal.ct.gov/Office-of-the-Governor/News/Press-Releases/2020/07-2020/Governor-Lamont-Coronavirus-Update-July-29)

> \*In addition to the 79 recently diagnosed cases and 12,367 tests, 384
> cases and 750 tests performed between April and June were newly
> reported to the Department of Public Health in connection with a
> transition to electronic reporting by an out-of-state regional
> laboratory. For surveillance purposes, that data has been added to the
> total case and total test counts.

[Note as of August 18, 2020 DPH daily
update:](https://portal.ct.gov/-/media/Coronavirus/CTDPHCOVID19summary8182020.pdf)

> \*Forty new cases were reported to CT DPH since yesterday; in
> addition, DPH removed 52 previously reported cases because of newly
> identified data errors.

[Note as of October 12,
2020:](https://www.fox61.com/article/news/health/coronavirus/governor-lamont-covid-19-update-connecticut/520-57baa88a-fbe8-47f3-9d06-600b2222d96a)

> As of Monday, there were additional 1,066 positive cases from Friday.
> That included over 270 positive cases out of 23,130 tests conducted
> between September 26 and October 8 that are newly reported as part of
> catch-up reporting.

[^1]: The data displayed on these maps excludes the towns of Somers,
    Brooklyn, and Montville because they are small rural towns with
    prisons, and the cases reported in the prisons may dominate the
    total in the town and even affect the reporting for the county
    overall. Covid-19 in prisons is a significant issue, but it’s
    helpful to try to evaluate it separately from data from the
    non-prison community.
