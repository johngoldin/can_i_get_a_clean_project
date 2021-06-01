---
title: My Apple Watch Visits the ER -- Twice
author: John Goldin
date: '2021-06-07'
weight: 5
slug: apple-watch-visits-the-er
categories:
  - Apple-Health-Export
  - Quantified-Self
  - R
tags:
  - Apple-Health-Export
  - Quantified-Self
  - R
subtitle: ~
excerpt: |
  Using the Apple Health Export data to show the context of a visit to the ER. 
  The same principles apply to using heart rate data to provide a context for
  an ECG recording.
images: ~
series: ~
layout: single
draft: yes
---

**A disclaimer: Not only am I not a cardiologist, but if you asked me to point
to the location of the heart in my chest, I wonder whether I would
point to the correct spot. Perhaps the information presented here may
have some clinical value, but I don't have the expertise to say one
way or the other.**

Here I will tell the tale of two visits to a local ER. 
At the end of the post I will include a note about
why I am not concerned about diminishing my privacy
and why I would advise most people to think twice before
publishing something like this. 

### At the ER in February 2019

I feel a tinge of embarrassment about this visit because
one can argue it was not necessary. But in part by accident
it had favorable health consequences.

About 1:30 AM early in a day in February I had
a brief but intense period of digestive upset.
I won't go into the details except to say that
it probably was related to GERD and that I 
have had episodes somewhat like this since I
was in my late 30's, although much
diminished as I got older and my life style changed.
About 5:30 AM after a brief visit to the bathroom
I got back into bed and felt strange, looked at
my Apple Watch, and saw that my pulse was up to 150.
I felt my pulse at my throat and realized the reading
was not a fluke. Now comes the embarrassing part.
I freaked out. I don't claim my alarm was
reasonable. I had no chest pain or any other symptom
except rapid pulse. I was half asleep and not thinking
clearly. I had had an episode of atrial fibrillation
about five years previously and was returned
to normal rhythm during a visit to an emergency room.
Anyway, I immediately jumped out of bed thinking I 
needed to go to the ER and told my partner. If the
same thing happened today I would not feel I needed
to rush off like that, but I didn't know any better then.

The ER was only 10 minutes away. During the drive I felt
like my heart rate had dropped somewhat. We arrived at the
ER at a time when it wasn't very busy and after a quick
stop at triage I was in a bed getting an ECG, which was
normal. I told them that I felt my heart rate had
been sustained at a fast rate until part way during the
trip to the ER. That's what I thought, but part of the
point of this post is that we'll see my perception 
(and what I reported to the ER doc) was not accurate.
I reported my digestive episode from earlier in the
night and a blood test showed that my lipase (a pancreatic enzyme)
was abnormal. Eventually I realized they were unconcerned about
my heart and instead poking my abdomen. They were considering
whether I had pancreatitis, which I had never heard of.
(Not only am I not a cardiologist, I also am not a 
gastroenterologist.) 

Apparently the lipase level was abnormally
high, but not as high as one would expect with 
pancreatitis. It turned out I didn't have pancreatitis.
In fact, I redid the blood work the next
day and it was completely normal. Let's ignore
the digestive story because that is a dull story that has nothing to
do with my Apple Watch; instead let's focus on
heart [palpitations](https://en.wikipedia.org/wiki/Palpitations), 
the symptom that I presented with at the ER. (I haven't had
a significant repeat of the digestive episode since then so it doesn't seem to be 
an issue I need to worry about.)

I am not 100% clear about the meaning of the word "palpitations." Generally it
seems to imply a sensation of irregular heart beat, but the Wikipedia
discussion allows as well just abnormally rapid heart beat, which is the
most I can muster in this case. 

So what was actually going on with my heart rate during this incident?
That takes us to the Apple Health Export. After getting home from the ER
I was a bit unsettled by the whole experience and my typical reaction 
was to gather data. It was this episode that sent me to the web looking
for information about the Apple heart rate data that led me to learn
about the Health Export. I found a [post by Ryan Praskievicz](https://www.ryanpraski.com/apple-health-data-how-to-export-analyze-visualize-guide/)
that showed me how to get the Health Export and load it into R.
I had a an appointment with my primary care physician early in the next
week, and before that visit I had prepared a plot showing my heart rate
throughout the incident, as recorded on my Apple Watch.[^1]

[^1]:The actual ER incident was not a major health event. But it resulted
in a significant improvement in my health via a route which also
has an RStudio connection. When I left the ER, the
doctor suggested that I might want to go on a liquid diet for a day or two.
I didn't know what a doctor means by a "liquid diet," and I still don't.
But for a couple of days I subsisted on juice and broth. I wanted to avoid
fatty food so I started using the LoseIt! app to track fat in what I was eating.
I noted that I immediately lost a noticeable amount of weight without much
difficulty. So for the next year and a half I faithfully used LoseIt! to
track calories and ended up losing about 25 pounds. One of the creators
of LoseIt! was J.J. Allaire, the co-founder of RStudio. I am confident
that losing that weight has lowered my blood pressure and improved my
health in general and discovering RStudio has improved my intellectual health as well.

