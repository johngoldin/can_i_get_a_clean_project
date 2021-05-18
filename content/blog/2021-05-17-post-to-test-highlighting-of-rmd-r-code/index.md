---
title: Post to Test Highlighting of Rmd R Code
author: John Goldin
date: '2021-05-17'
slug: []
categories:
  - other-R
tags: []
subtitle: ~
excerpt: ~
images: ~
series: ~
layout: single
draft: yes
output:
  blogdown::html_page:
    # figure parameters based on recommendation in Hadley's book
    highlight: pygments
  code_download: yes
---

### Post content

Typical location to start editing 



```r
library(tidyverse)
```

```
## ── Attaching packages ─────────────────────────────────────── tidyverse 1.3.1 ──
```

```
## ✓ ggplot2 3.3.3     ✓ purrr   0.3.4
## ✓ tibble  3.1.1     ✓ dplyr   1.0.6
## ✓ tidyr   1.1.3     ✓ stringr 1.4.0
## ✓ readr   1.4.0     ✓ forcats 0.5.1
```

```
## ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
## x dplyr::filter() masks stats::filter()
## x dplyr::lag()    masks stats::lag()
```

```r
library(lubridate)
```

```
## 
## Attaching package: 'lubridate'
```

```
## The following objects are masked from 'package:base':
## 
##     date, intersect, setdiff, union
```

```r
path_saved_export <- "~/Dropbox/Programming/R_Stuff/john_vitals/Apple-Health-Data/"
path_to_healthexport1 <- "~/Documents/R_local_repos/applehealth1/R/"

a <- 1 + 2
b <- "Text in quoted string"
# commented text
```

What does R text look like?
