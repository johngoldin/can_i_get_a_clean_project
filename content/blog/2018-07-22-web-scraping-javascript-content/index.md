---
title: Web Scraping Javascript Content
author: John Goldin
date: '2018-07-22'
slug: scraping-javascript
aliases:
    - /2018/07/scraping_javascript/
categories: 
  - R
tags: 
  - R
excerpt: 'An example of using a "headless browser" to scrape web content produced by javascript. The data is about compensation of university CEOs and was published by the Chronicle of Higher Education.'
keywords: []
---
Web scraping with [rvest](https://github.com/hadley/rvest) and [SelectorGadget](https://selectorgadget.com) can be powerful and fun. Recently I have experimented
with trying to scrape a table from the [Chronicle of Higher Education](https://www.chronicle.com/interactives/executive-compensation?cid=at&utm_source=at&utm_medium=en&elqTrackId=96983a9eb49d4f7fb200919f8f825d48&elq=44975a24d16b4d13bc145c3dd45cf40a&elqaid=19745&elqat=1&elqCampaignId=9127#id=table_public_2017) 
that showed compensation for
university CEO's. With a certain amount of trial and error I used [SelectorGadget](https://selectorgadget.com)
to find the fields I wanted to scrape: name, university, and compensation.

But when I went through the steps in `rvest` to scrape those fields, I got nothing (in the form of a zero length vector of results). 
I know next to nothing about how javascript is used to populate a web page so my understanding
of what is happening is almost non-existant. I see the results on the screen, but when I use
the browser to look at the page source, I don't see the individual compensation data.
Here's a Stack Overflow [response](https://stackoverflow.com/questions/8598836/jquery-dom-changes-not-appearing-in-view-source) that explains a little bit of what is going on:

> The "View Source" only shows the source the server sent at the time the browser requested the particular webpage from the server. Therefore, since these changes were made on the client side, they don't show up on the "View Source" because they've been made after the original page has been delivered.

In my case, javascript processed by my browser is adding html after the original page was sent. (Or at least I think that is what is going on.)

The solution is a "headless browser." This is a program that functions like a web browser,
but it's purpose is to produce HTML rather than to put something on the screen (hence, headless, if
one thinks of the screen as the head).
[This article](http://www.rladiesnyc.org/post/scraping-javascript-websites-in-r/) by Brooke Watson
goes over the steps you need to follow to scrape web data created via javascript (and also 
discusses other considerations related to web scraping). Another good source is [this post](https://www.r-bloggers.com/web-scraping-javascript-rendered-sites/) by Florian Teschner. I also found a comprehensive list of [headless browsers](https://github.com/dhamaniasad/HeadlessBrowsers), although I haven't looked beyond PhantomJS.

### An Example

In this post I will work through scraping the Chronicle page as an example. 
First we have to get the HTML containing the CEO compensation table.
To do that I will use [PhantomJS](http://phantomjs.org) as a headless browser.
I installed it on my Windows computer at work via a [PhantomJS install page](http://phantomjs.org/download.html). I also installed it on my Mac at home
using [HomeBrew](https://brew.sh). I did a little bit of googling first to assure
myself that PhantomJS was was reputable and safe to install. The [source code](https://github.com/ariya/phantomjs) is available on GitHub. Note that the
author has suspended development of PhantomJS as of March, 2018, for reasons that
are discussed at the GitHub README. 

To use PhantomJS, I'll use the R system()
function to run PhantomJS so that it processes a javascript file called
`public_fetch.js`. This is based on example code cited above with
the URL reference changed to point to the Chronicle of Higher Ed page
and an output file for the resulting HTML called `public_ceo_export.html`.
Here's the javascript that PhantomJS will process:

```
var webPage = require('webpage');
var page = webPage.create();

var fs = require('fs');
var path = 'public_ceo_export.html';

page.open('https://www.chronicle.com/interactives/executive-compensation?cid=wsinglestory#id=table_public_2017', function (status) {
  var content = page.content;
  fs.write(path,content,'w');
  phantom.exit();
});
```

We can call PhantomJS from within R:

```
# a macos version of running phantomjs
system("phantomjs public_fetch.js")
```

After this runs, `public_ceo_export.html` contains the HTML that contains the
data table. Here's what the beginning of the data table looks like in raw HTML:

```
<table id="interactive_table" class="interactive_table"><tbody><tr id="table-13623_157289_2017_public" class="result odd"><td class="col_0"><div class="ect_name"><div class="ect_head"><img class="fl headshot" src="//chronicle.s3.amazonaws.com/DI/exec-comp/james-r-ramsey.jpg" alt="James R. Ramsey"></div><span class="name">James R. Ramsey *</span><span class="college">University of Louisville</span></div><div class="ec_baractual" data-val="4290232" style="width: 100%;"><div class="ecba_notbase" style="width:98.70163198633547%;"></div></div><span class="ec_barlabel">$4,290,232</span><div class="ec_rowHover"><span class="ech_label">James R. Ramsey <em>University of Louisville, 2017</em></span><span class="ech_detail"><em>Total Compensation: </em>$4,290,232</span><span class="ech_detail ech_base"><em>Base Pay: </em>$55,703</span><span class="ech_detail ech_bonus"><em>Bonus Pay: </em>$0</span><span class="ech_detail ech_other"><em>Other Pay: </em>$4,233,739</span></div></td></tr><tr id="table-13790_100858_2017_public" class="result even"><td class="col_0"><div class="ect_name">
```
Yuck. The data is in there, but HTML is not easy for mere humans to decipher. 
Our next task is to use rvest to pull out the data elements
we are looking for. In the HTML there are a lot of "class" labels which (I think) are
there so that CSS can be used to produce a snazzy looking data table delivered to the user's screen.
Those names are confusing to read, but revest is going to make good use of them.

What class names are we looking for? I used [SelectorGadget](https://selectorgadget.com) to tease out
which elements I wanted to pull out of the HTML. Here is a [video](https://www.youtube.com/watch?v=4IYfYx4yoAI) that demonstrates how to use both rvest and SelectorGadget.
I won't try to explain how to use SelectorGadget here. 

Next we'll look at some basic rvest code.

```{r revest_example, message=FALSE}
library(rvest)
library(tidyverse)
library(stringr)

# read the page that was written by the headless browser
public_page <- read_html("public_ceo_export.html")

# look for HTML bit with the ".name" and produce them as text
name <- public_page %>% html_nodes(".name") %>% html_text()
# look for HTML bit with the ".college" and produce list of universities
college <- public_page %>% html_nodes(".college") %>% html_text()
print(college[1:3])  # show we have something reasonable

base <- public_page %>% 
  html_nodes(".ech_base") %>% 
  html_text() %>% 
  str_replace_all("[[:alpha:]]|:| |\\$|,", "") %>% 
  as.numeric()
bonus <- public_page %>% 
  html_nodes(".ech_bonus") %>% 
  html_text() %>% 
  str_replace_all("[[:alpha:]]|:| |\\$|,", "") %>% 
  as.numeric()
other <- public_page %>% 
  html_nodes(".ech_other") %>% 
  html_text() %>% 
  str_replace_all("[[:alpha:]]|:| |\\$|,", "") %>% 
  as.numeric()
# .ech_detail retrieves all four elements so length is 200 rther than 50
# (I figured out .ech_detail by trial and error.)
# we need to pull out every fourth element to get the total
total <- public_page %>% 
  html_nodes(".ech_detail") %>% 
  html_text()
total <- total[seq(1, 200, 4)] 
# Identify cases where adding up the bits is different than the "total"
if (!all(str_detect(total, "Total Compensation"))) print("something is wrong with total")
total <- total %>% 
  str_replace_all("[[:alpha:]]|:| |\\$|,", "") %>% 
  as.numeric()
```
The general pattern is that we get the HTML (loaded here into `pubic_page`),
use `html_nodes` to pick out the items we want, and then convert the resulting
items into text via `html_text`. For the numeric fields, we also need strip out
commas and dollar signs and covert to numeric.

(`str_replace` uses [regular expressions](https://en.wikipedia.org/wiki/Regular_expression), which
is a whole topic in and of itself. There is a giga-ton of info on the web about regular expressions.
For an R user, I would suggest focusing on using it via the [stringr](https://stringr.tidyverse.org/index.html) package, so
[this page](https://stringr.tidyverse.org/articles/regular-expressions.html) might
be a good place to start.)

### The Punch Line?

At this point, you are probably looking for the punchline: some insight about university
CEO compensation. No such luck. What to do with the information after you 
have scraped it is a different topic. In this post I am just trying to find an illustration
of where scrpaing might be used and lay down enough information so that if I actually
want to do something like this again I'll be able to recreate it.

### When Is Scraping OK?

Just because you *can* do something doesn't mean you *may*. You should
check the terms of service of the web site you are going to scrape. Sometimes
it is made clear that web scraping is off limits. For example, this
bit from the FlightAware [terms of service](https://flightaware.com/about/termsofuse) is admirably clear:

> you will only access the FlightAware web site with a human-operated interactive web browser and not with any program, collection agent, or "robot" for the purpose of automated retrieval or display of content.

Okey dokey, no web scraping the FlightAware web site. 

The "User Agreement" for the Chronicle web
site seems to be more what one expects in the way of long and ambiguous (to the layperson at least) legalese.
There is a [restrictions on use](https://www.chronicle.com/page/User-Agreement/619/?cid=cheftr#restrictionsOnUse) section
that seems to be restrictive indeed.

> You may not modify, decompile, create derivative work(s) of, disassemble, retransmit, resell, distribute, compile, broadcast, sublicense, mirror, frame, rent, or otherwise use in any manner not expressly permitted herein, the Site or any of its content; use robots or spiders or other automated devices or manual processes to monitor or gather any data from the Site or its users; create course books or educational materials using any of the Site content; use the Site to “stalk” or harass; place a link to the internal pages of any password-protected portions of the Site on any Web site, intranet, or extranet without the prior written permission of The Chronicle....

Under the section on permitted uses, 

>We would like your access to the Site to be useful and convenient.  Subject to the terms and conditions of this Agreement, you may download items of content on the Site for personal use during the term of this Agreement, except in any instance where we have expressly restricted the access to or copying of such materials.

So can I use web scraping to download data from this *Chronicle* article for my own use? I don't really know. As a practical
matter I assume that if I don't republish the information I'm on fairly safe ground. 
An earlier version of this post had a screenshot to illustrate using SelectorGadget on
the Chronicle CEO table. I decided that was not something they would regard as a fair
use of their copyrighted and restricted material, so I deleted it before this post was
published.

#### robots.txt

Another way to check on whether web scraping is welcomed or frowned upon is to check
for a file called `robots.txt` at the top level of the site. This [Wikipedia article](https://en.wikipedia.org/wiki/Robots_exclusion_standard) describes the 
history of this tool. You can ask your browser to see robots text by just
adding `/robots.txt` to the top level domain name for a site. For example,
`chronicle.com/robots.txt` is fairly thin:

>User-agent: yandex

>User-agent: bingbot  
>User-agent: msnbot  
>Disallow:  
>Sitemap: https://www.chronicle.com/public/sitemap/chronicle-sitemap-index.xml  
>Crawl-delay: 20  
>
>User-agent: *  
>Disallow:  
>Sitemap: https://www.chronicle.com/public/sitemap/chronicle-sitemap-index.xml  

There's nothing after `Disallow:`. The robots.txt standard is aimed primarily at things
like search engines crawling the internet looking for the information
to add to their search algorithms. FlightAware has a long, elaborate
robots.txt file. Yale's robots.txt is even more elaborate.

There's a semi-official site that describes [robots.txt](http://www.robotstxt.org/robotstxt.html). 
I don't know much more about how to interpret robots.txt, but it's one
more thing you can check if you are concerned about whether your web
scraping is legit.

That wraps it up. Web sraping can be fun and useful. 
But keep an eye on whether scraping a particular site is legit and legal.
