---
date: "2021-12-31"
#lastmod: "2016-01-25"
draft: TRUE
diagram: true
image:
  caption: 'Image credit: [**Horia Varlan**](https://www.flickr.com/photos/horiavarlan/4777129318/in/photolist-8h937A-8hBXso-f859U7-7yuQFL-u8ZMFH-6UtSFp-J5b5po-cqx11j-CcQMzs-pChH96-8qdyhE-ebLAEx-D2U5Yx-b5fE7T-dx24Uo-ebcAhs-fJU9RB-7GVhDa-o3dpv5-daJ1Qc-FgAUzQ-8FFXKw-mTXza-KWTYYy-jzbfAp-nfvigS-fQrAn5-dBGY6t-eb79oF-DysEbS-dAcszP-uCUByj-8uPhwp-7LBEDa-vL1T52-c9o1tQ-o4XEFq-7Duwmv-MQTK7-7SRthr-9gYvR8-6ZqQcg-bW7fP-8KbVbG-huCWgF-ckzYHd-9ieN3t-hAqaWs-8NB82B-24vANH)'
  placement: 3
markup: mmark
math: true
tags:
- data science
- learning
- teaching
- open source
- rstats
- rstudio
- rstudio.cloud
title: Teaching data science with rstudio.cloud
---


### Data Analytics Coding Fundamentals

In the summer of 2019, I received an offer from the University of Victoria to teach a new course in the Continuing Studies department, "Data Analytics Coding Fundamentals". The course ran for six consecutive Saturdays, starting on November 2, 2019. The course was repeated in the spring of 2020, starting on February 29.

The course content—using software to automate data analytics tasks—covers a substantial chunk of what I've learned as part of my day job for, truth be told, three decades. And over the past few years I've learned and incorprated R into that work, so I was understandably enthusiastic to be able to introduce others to the marvel of using R to tackle data analysis problems.


#### Getting ready

So where to start?

I had already decided, based on my own experience of learning R and observing how my colleagues had learned (or struggled to learn and incorporate) R, that the tidyverse was the best entry point. I had a clear idea that I was going to teach "data analysis with R", _not_ "R programming". As a consequence, I knew that [_R for Data Science_](https://r4ds.had.co.nz/) was to be the text book, and some of the examples and homework assignments would be drawn directly from it.

This was my first time in front of a classroom in many years, so I embarked on a quick study of pedagogical methods. I also discovered andragogy—the methods and principles of adult education—which reinforced my prior belief that this was going to be different than teaching a room full of undergraduates, who come (by and large) with a similar set of experiences and knowledge.

I had also had the benefit of participating in a [Software Carpentry lesson](https://software-carpentry.org/lessons/), as well as serving as a tutor in two different day-and-a-half classes taught by [Dr. Charlotte Wickham](https://www.cwick.co.nz/), introducing the tidyverse to people new to R. Not only did I get better at using R as a consequence of these classes, but I also saw good androgogical practice. A substantial part of that is hands-on coding in the classroom.

It was clear that the approach of providing a clear learning objective for each section coupled with some theoretical or technical background, followed by hands-on exercises that applied those concepts, was an effective method. It seemed particularly effective when this approach is concluded with a quick test to reinforce those concepts.

### RStudio Cloud

I decided to employ RStudio Cloud offering as the platform for the participants to use. This provided a number of distinct advantages:

* No need to interface with the department's IT support, ensuring that 23 identical instances of R and packages are installed on the computers in the lab, including updates to packages. 

* Everyone in the class had the same version of R and associated packages both while in the lab _and_ at home. 

* Everyone had easy access to the same hands-on exercises and homework assignments, including the data files. No more messy "download this file, unzip into a folder named exactly this, etc".

* The participants could start coding on the morning of the first day. There is no need to spend time dealing with the permutations of installs on different operating systems, setting up package libraries, etc. on the first day—that could wait until later in the course.

* Adding a module of "data science with Python" was not an issue at all—I simply installed the {reticulate} package in an rstudio.cloud project, and we were off to the races. For this module, we recreated an analysis that had been done earlier in the course using R—this gave first-hand exposure to the fact that one can solve data analysis problems using either language.


### Additional materials

{learnr} -- tutormanor

I made some tutorials for the class I'm teaching when we went online mid-stream, and frankly I wish I'd used it before as a supplement to classroom instruction. I particularly appreciate the option to have some formative assessment (eg multiple choice questions) inside the tutorial. 

* publish to shinyapps.io 

flipbooks


### The sudden transition to online





### Notebooks

Yihui Xie, [The First Notebook War](https://yihui.name/en/2018/09/notebook-war/)


## References and other resources

[The GitHub repo for the course](https://github.com/MonkmanMH/UVic_BIDA302)

[tutormanner](https://github.com/MonkmanMH/tutormanner)

-30-