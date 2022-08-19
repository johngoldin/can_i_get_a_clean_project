---
title: Intra-Day Measures
author: John Goldin
date: '2022-08-13'
slug: 2022-08-another-test-post
categories:
  - Apple-Health-Export
tags: []
subtitle: 'Multiple Measures Per Hour'
excerpt: 'These measures are taken frequently during the day, sometimes multiple times a minute during workoiuts.'
draft: yes
images:
  - ~
  - ~
weight: 6
# layout: single
execute:
  freeze: auto  # re-render only when source changes
  echo: false
format: hugo
---



In this post we'll look at some low level measures in the Apple Health Export.

<div id="egxblwaxbk" style="overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#egxblwaxbk .gt_table {
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

#egxblwaxbk .gt_heading {
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

#egxblwaxbk .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#egxblwaxbk .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 0;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#egxblwaxbk .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#egxblwaxbk .gt_col_headings {
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

#egxblwaxbk .gt_col_heading {
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

#egxblwaxbk .gt_column_spanner_outer {
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

#egxblwaxbk .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#egxblwaxbk .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#egxblwaxbk .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#egxblwaxbk .gt_group_heading {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
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

#egxblwaxbk .gt_empty_group_heading {
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

#egxblwaxbk .gt_from_md > :first-child {
  margin-top: 0;
}

#egxblwaxbk .gt_from_md > :last-child {
  margin-bottom: 0;
}

#egxblwaxbk .gt_row {
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

#egxblwaxbk .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
}

#egxblwaxbk .gt_stub_row_group {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
  vertical-align: top;
}

#egxblwaxbk .gt_row_group_first td {
  border-top-width: 2px;
}

#egxblwaxbk .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#egxblwaxbk .gt_first_summary_row {
  border-top-style: solid;
  border-top-color: #D3D3D3;
}

#egxblwaxbk .gt_first_summary_row.thick {
  border-top-width: 2px;
}

#egxblwaxbk .gt_last_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#egxblwaxbk .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#egxblwaxbk .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#egxblwaxbk .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#egxblwaxbk .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#egxblwaxbk .gt_footnotes {
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

#egxblwaxbk .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding-left: 4px;
  padding-right: 4px;
  padding-left: 5px;
  padding-right: 5px;
}

#egxblwaxbk .gt_sourcenotes {
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

#egxblwaxbk .gt_sourcenote {
  font-size: 90%;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
}

#egxblwaxbk .gt_left {
  text-align: left;
}

#egxblwaxbk .gt_center {
  text-align: center;
}

#egxblwaxbk .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#egxblwaxbk .gt_font_normal {
  font-weight: normal;
}

#egxblwaxbk .gt_font_bold {
  font-weight: bold;
}

#egxblwaxbk .gt_font_italic {
  font-style: italic;
}

#egxblwaxbk .gt_super {
  font-size: 65%;
}

#egxblwaxbk .gt_two_val_uncert {
  display: inline-block;
  line-height: 1em;
  text-align: right;
  font-size: 60%;
  vertical-align: -0.25em;
  margin-left: 0.1em;
}

#egxblwaxbk .gt_footnote_marks {
  font-style: italic;
  font-weight: normal;
  font-size: 75%;
  vertical-align: 0.4em;
}

#egxblwaxbk .gt_asterisk {
  font-size: 100%;
  vertical-align: 0;
}

#egxblwaxbk .gt_slash_mark {
  font-size: 0.7em;
  line-height: 0.7em;
  vertical-align: 0.15em;
}

#egxblwaxbk .gt_fraction_numerator {
  font-size: 0.6em;
  line-height: 0.6em;
  vertical-align: 0.45em;
}

#egxblwaxbk .gt_fraction_denominator {
  font-size: 0.6em;
  line-height: 0.6em;
  vertical-align: -0.05em;
}
</style>
<table class="gt_table">
  <thead class="gt_header">
    <tr>
      <th colspan="2" class="gt_heading gt_title gt_font_normal" style>Frequency of Apple Health Measurements</th>
    </tr>
    <tr>
      <th colspan="2" class="gt_heading gt_subtitle gt_font_normal gt_bottom_border" style>The 15 Most Frequent Measurements</th>
    </tr>
  </thead>
  <thead class="gt_col_headings">
    <tr>
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1">Measurement Type</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1">Values per Day</th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td class="gt_row gt_left">Active Energy Burned</td>
<td class="gt_row gt_right">813</td></tr>
    <tr><td class="gt_row gt_left">Basal Energy Burned</td>
<td class="gt_row gt_right">767</td></tr>
    <tr><td class="gt_row gt_left">Heart Rate</td>
<td class="gt_row gt_right">664</td></tr>
    <tr><td class="gt_row gt_left">Distance Walking Running</td>
<td class="gt_row gt_right">548</td></tr>
    <tr><td class="gt_row gt_left">Step Count</td>
<td class="gt_row gt_right">127</td></tr>
    <tr><td class="gt_row gt_left">Apple Exercise Time</td>
<td class="gt_row gt_right">83</td></tr>
    <tr><td class="gt_row gt_left">Apple Stand Time</td>
<td class="gt_row gt_right">52</td></tr>
    <tr><td class="gt_row gt_left">Respiratory Rate</td>
<td class="gt_row gt_right">49</td></tr>
    <tr><td class="gt_row gt_left">Environmental Audio Exposure</td>
<td class="gt_row gt_right">46</td></tr>
    <tr><td class="gt_row gt_left">Walking Speed</td>
<td class="gt_row gt_right">40</td></tr>
    <tr><td class="gt_row gt_left">Walking Step Length</td>
<td class="gt_row gt_right">40</td></tr>
    <tr><td class="gt_row gt_left">Walking Double Support Percentage</td>
<td class="gt_row gt_right">27</td></tr>
    <tr><td class="gt_row gt_left">Apple Stand Hour</td>
<td class="gt_row gt_right">23</td></tr>
    <tr><td class="gt_row gt_left">Flights Climbed</td>
<td class="gt_row gt_right">21</td></tr>
    <tr><td class="gt_row gt_left">Oxygen Saturation</td>
<td class="gt_row gt_right">19</td></tr>
  </tbody>
  <tfoot class="gt_sourcenotes">
    <tr>
      <td class="gt_sourcenote" colspan="2">Source: From my Apple Health Export in the ast year.</td>
    </tr>
  </tfoot>
  
</table>
</div>
