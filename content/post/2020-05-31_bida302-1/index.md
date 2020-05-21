---
date: "2020-05-31"
#lastmod: "2016-01-25"
diagram: true
image:
  caption: 'Image credit: [**Carleton University, Archives & Special Collections**](https://arc.library.carleton.ca/exhibits/construction-u)'
  placement: 3
markup: mmark
math: true
tags:
- data science
- open source
- learning
title: Some thoughts on teaching data science
---


### Data Analytics Coding Fundamentals

In the summer of 2019, I received an offer from the University of Victoria to teach a new course in the Continuing Studies department, "Data Analytics Coding Fundamentals". The course ran for 6 consecutive Saturdays, starting on November 2, 2019. The course was repeated in the spring of 2020, starting on February 29.

The course content covers the basics of what I've been doing as part of my day job for, well, decades. And over the past few years I've learned and incorprated R into that work, so I was enthusiastic to introduce others to using R to tackle data analysis problems.


#### Getting ready

So where to start?

I had already decided, based on my own experience of learning R and observing how my colleagues had learned (or struggled to learn and incorporate) R, that the tidyverse was the best entry point. I had a clear idea that I was going to teach "data analysis with R", _not_ "programming R". As a consequence, I knew that _R for Data Science_ as to be the text book, and the examples and some homework assignments would be drawn directly from that.

This was my first time in front of a classroom in many years, so I embarked on a quick study of pedagogical methods. I also discovered andragogy—the methods and principles of adult education, which reinforced my prior belief that this was going to be different than teaching a room full of similarly aged and experienced undergraduates.

I had also had the benefit of participating in a [Software Carpentry lesson](https://software-carpentry.org/lessons/), and two different classes introducing the tidyverse, taught by Dr. Charlotte Wickham. Not only did I get better at using R as a consequence of these classes, but I also saw good androgogical practice.

It was clear that the approach of providing a clear learning objective for each section coupled with some theoretical or technical background, followed by hands-on exercises that applied those concepts, was an effective method. It seemed particularly effective when this approach is concluded with a quick test to reinforce those concepts.

### RStudio Cloud

I decided to employ RStudio Cloud offering as the platform for the participants to use. This provided a number of distinct advantages:

* No need to interface with the department's IT support, ensuring that 23 identical instances of R and packages are installed on the computers in the lab, including updates to packages. 

* Everyone in the class had the same version of R and associated packages both while in the lab _and_ at home. 

* Everyone had easy access to the same hands-on exercises and homework assignments, including the data files. No more messy "download this file, unzip into a folder named exactly this, etc".

* The participants could start coding on the morning of the first day. There is no need to spend time dealing with the permutations of installs on different operating systems, setting up package libraries, etc. on the first day—that could wait until later in the course.

* Adding a module of "data science with Python" was not an issue at all—I simply installed the {reticulate} package in an rstudio.cloud project, and we were off to the races.


### Additional materials

{learnr} -- tutormanor

I made some tutorials for the class I'm teaching when we went online mid-stream, and frankly I wish I'd used it before. I particularly appreciate the option to have some formative assessment (eg multiple choice questions) inside the tutorial. 

* publish to shinyapps.io 

flipbooks


### The sudden transition to online





### Notebooks

Yihui Xie, [The First Notebook War](https://yihui.name/en/2018/09/notebook-war/)


## References and other resources

[The GitHub repo for the course](https://github.com/MonkmanMH/UVic_BIDA302)

[tutormanner](https://github.com/MonkmanMH/tutormanner)

-30-