---
title: A New Look for This Web Site
author: John Goldin
date: '2021-05-03'
slug: a-new-look-may-2021
categories:
  - personal
tags: []
subtitle: Converting This Site To the Hugo Apéro Theme
excerpt: It's a new look! I have converted the site to Hugo Apéro theme. It includes some fun images, including some grotesques from the Sterling Library and Law School buildings at Yale.
images: ~
series: ~
layout: single
draft: no
---

I'm now generating this site using the [Hugo Apéro theme](https://hugo-apero.netlify.app). I chose to look for a new theme for this site for three reasons. 

1) My previous theme looked bland compared with the many interesting examples I've seen lately.
Of course my site actually is fairly bland, but I don't need to emphasize that!

2) A blog format doesn't always fit what I want to put on the site. Most notably, 
since last June I have been updating my post on Covid in Connecticut each week
night with the latest stats. That's a crazy way to use a dated blog post. 
Apéro gives me a way to have a separate section without the scrolling dates of
a blog format.

3) I feel like I have a lot of things I need to do this month, so of course I
was eager to take on an irrelevant new task as a way to procrastinate from
the things I was supposed to be doing.

I'm happy with the result. 

#### Finding Some Images to Dress Up the Site

The Apéro theme encourages me to add more images
associated with pages on the site. So I had a good time looking for images to use.
I have featured photos of gothic grotesques from the Sterling Library 
and Sterling Law Building at Yale. I have walked between these two buildings
thousands of times on Wall Street. There were a lot of gothic decorations
included during the explosion of academic gothic buildings at Yale during
the depression. The most fanciful are on Sterling Law. The scene of 
a professor in front of a class that is the heading for the blog
page is directly over the main entrance to the building. Actually there are
two images. One is the class active and eager at the start of the day and
the other is a bunch of tired and sleeping students at the end of the day.

![Sterling Law class](/img/for_site/sidebar-law-classes-joined.png)

For the landing page I have a grotesque from the gallery in the Library.
In true grotesque fashion it lampoons the negative image of a callow
Yale student with his mug of beer, cigar, and girlie picture. Perhaps
I'll reconsider whether this is the image I want to lead with.

The Library gallery has an array of students carved in stone. In the corner opposite there
is one of my favorites: a student with an open book where the page
says "U R A JOKE".

![Sterling Law class](/img/for_site/UR_a_joke.png)

For more on the Library gallery, read [If These Walls Could Talk](http://www.thenewjournalatyale.com/2009/12/if-these-stone-walls-could-talk/) or
see this video:

{{< youtube 2RgrlQbZkYE >}}

I plan to use some more photos of these details at Yale. I should point
out that usually the only time I noticed these things was when I 
had out of town visitors who wanted a tour of the campus. Only
then would I actually look at the details rather than dashing by
on the way to somewhere else.

It has been fun looking through my photos for images to use of Yale,
or walking in England, or anything else that might fit in.

#### More To Do

Converting to a new Hugo theme has forced me to actually look at the site. 
I need to fix up some old posts. I have two draft posts related to the Apple
Health Kit that I should just go ahead and finish and publish. I'm hoping
that the way Apéro separates the blog from Projects or more ephemeral products will
inspire me to use the blog more frequently.

#### Why Did I Choose Apéro?

I didn't do an exhaustive search. From time to time I have checked out the
[gallery of Hugo themes](https://themes.gohugo.io). Switching to a new theme
is an investment in time, and I wasn't confident it would be worth the effort.
I have been seeing lots of examples of people in the R crowd using the Academic
theme so I was considering that. Then I saw an announcement of a [coming
talk](https://www.meetup.com/rladies-tunis/events/277518271/) by Alison Hill
that  mentioned Apéro. I had recently given a talk to our staff group at
work on creating a web presence and based that mostly on a talk by [Alison Hill
and Desirée De Leon](https://www.youtube.com/watch?v=QcE4RBH2auQ). I've been
getting most of my tips on Blogdown from reading [Alison's posts](https://alison.rbind.io/post/) so I felt
like diving into Apéro wouldn't be too risky. I think the talk at the end
of May seems like it's the coming out of Apéro so there are not yet a lot of instructions
on how to use the theme. I was jumping the gun a bit and appropriately
paid a wee price of additional time and frustration. But adapting to the
theme has mostly been entertaining and the pain and frustration has encouraged me to
develop my weak GitHub skills. I had to dust off [Happy Git](https://happygitwithr.com)
and try again to learn some basic skills. I even took Jenny Bryan's advice
and started using [GitKracken](https://www.gitkraken.com).

As discussed above, I was particularly attracted to the place Apéro would
provide for non-blog content. I have more to learn about how to take 
advantage of those features. What I have done so far with the Project and
Collections menus is just a first attempt at exploring what's possible.

#### What Have I Learned While Updating

1) The `magick` package (based on the ImageMagick library)
is more useful than I realized. I used it to resize a photo
as raw material to make an iconset. I also used it to concatenate
the two law school photos displayed above and resize them so that they
were both exactky the same width:

```r
#  Using magick package to append two photos: 
image1 <- magick::image_read("IMG_6832.PNG")     
    image1_width <- magick::image_info(image1)$width    
    image2 <- magick::image_read("IMG_6833.PNG")    
    image2_width <- magick::image_info(image2)$width    
    if (image2_width > image1_width){    
      image1 <- magick::image_scale(image1, paste0(image2_width, "x"))    
    } else if (image2_width < image1_width) {    
      image2 <- magick::image_scale(image2, paste0(image1_width, "x"))    
    }     
xx <- magick::image_append(c(image2, image1), stack = TRUE)  
# and then use magick::image_write to export xx 
```

2) I should think about PNG images a bit more. To use them as
featured images for my posts here, I need to size them correctly.
Using the Preview app on MacOS, I ended up sizing them as
400 pixels high at 144 pixels per inch (after initially
doing 200 pixels high at 72 pixels per inch). I kept an eye
on the resulting file sizes trying to avoid too much clutter.
I'll have to see how well this does. Maybe I should use higher
pixel density, which might make a difference on fancy screens.
Maybe in the future I'll use magick to resize images rather than Preview.

3) My life will be easier if I buckle down and learn how to use Git. I made
some progress working on this, but I've got a ways to go. 
And at the end of this project I've got bits and bytes lying 
around on the floor so I need to go back and do a bit of clean up.

4) Maybe I need to break down and learn a bit more about CSS.
As someone who pre-dates the internet, let alone pre-dates CSS,
I've been reluctant to expose myself to the details of CSS. I did
a tiny amount to adjust some Xarigan slides I did last month,
but maybe I should do a bit more to help with my web site. I'm
always feel like the font sizes of default markdown headers are
too large. Maybe I could come up with some CSS that I could use
repeatedly here and elsewhere.

5) I should give some more thought to markdown versus RMarkdown
for blog posts, or rather .md versus .Rmd versus .Rmarkdown. The
advantage of using .Rmd and RMarkdown to create my content is
that I can dive right in with less housekeeping. The 
disadvantage is that an .Rmd post is more fragile. If
something changes, there may be a problem if it has to
be re-knitted. I had to re-knit all my posts and there was
only one that gave me trouble. In a census post, I was
using a list of census variable names downloaded from the
census by `tidycensus`. I had used the fixed position of
variables in that list, and it turned out the number of
variables had changed slightly. So I had to go back to 
figure out exactly which variables I needed. It wasn't
too difficult to fix the code and re-knit, but one can easily imagine a situation where
the file I'm depending on no longer exists. Then I would be
stuck. All the issues that come up when people
worry about reproduceable code apply, such as
changes in package versions or change in any
resource that the code relies on.
The solution is to use RMarkdown to create a
markdown product and then use that markdown file
as the blog post. If I had a blog with a larger audience
and greater visibility the pressure to have posts that
will endure over time would probably push me to 
use markdown rather than Rmd. Given my situation where I can be
a bit more casual, relying on .Rmd seems like the easy
way to go. But I should think about this more for the future.