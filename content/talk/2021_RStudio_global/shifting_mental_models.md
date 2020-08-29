<!--
Copyright 2020 Martin Monkman

This work is licensed under the Creative Commons Attribution 4.0 International License.
To view a copy of this license, visit http://creativecommons.org/licenses/by/4.0/.
-->

---
title: "Shifting data analysis mental models"
author: "Martin Monkman"
date: "2020/12/31"
output: html_document
---



# 



author: Martin Monkman

date of most recent revision: 2020-08-24


**rstudio::global(2021)**



## Abstract

Talk theme:

* techniques for teaching R to help it reach new domains and new audiences


Abstract: 

Part of the challenge 

People who have experience in data analysis and statistical practice have established mental models of their workflow. These mental models are often influenced by the GUI tools that are ubiquitous in business and academic settings. As a consequence, their introduction to R and data science practice needs to be different than the approach taken with someone (say, a student in a typical undergraduate statistics class) who is simultaneously learning both the underlying methods and how to use R to implement those methods. Experienced data analysts arrive in class knowing what their outcome (the artifact of their workflow) will be—perhaps a short analytic report that combines text, summary tables, and plots—and are seeking a different workflow to produce that artifact.  (And as we know, you can't do data science in a GUI.) 

In this talk I will explore how as a colleague in a data science organization and as an instructor in university continuing studies courses I have used RStudio, RStudio Cloud, and the tidyverse to guide experienced data analysts in shifting their workflows into R, and along with that, shifted their mental models of their workflow.

* A typical mental model of an experienced GUI data analyst, including the steps and terminology common in those tools.

* The concept of Einstellung: "the development of a mechanized state of mind", and the often bad habits that we develop

* How the verbs of the tidyverse, the access to visualizations of the data, and the reduced friction of RStudio, RStudio Cloud, and the tidyverse family of packages help overcome Einstellung and ease the introduction to R and a robust data science workflow.



Key words: teaching, adult learners, mental models, EIKIFJB


Call for talks
https://blog.rstudio.com/2020/07/17/rstudio-global-call-for-talks/






***

## Einstellung

>A temporary attitude, expectation, or state of readiness, especially in relation to a stimulus that is about to be experienced.
> _A Dictionary of Psychology_, 3rd ed., Andrew M. Colman (ed.), Oxford University Press, 2008

When we learn how to do something, we learn both a combination of the method or technique _and_ the tools. The way I learned handwriting was different than my grandfather—my ballpoint pen required a different approach than his ink well fountain pen.

We sometimes hear the expression "To a person with a hammer, the whole world looks like a nail." ^[Image: Ryan Adams, homedust.com, https://www.flickr.com/photos/159630537@N08/28918563378/. Creative Commons CC BY 2.0 https://creativecommons.org/licenses/by/2.0/]



<img src="images/28918563378_77bc6997cb_k.jpg" alt="hammer and nail" width="300"/>

But more accurately, if you’ve been taught that the way to join two pieces of wood is to hammer in a nail, that’s how you’ll approach the problem.

And the "hammer and nail" mental model of the workflow might get in the way of your ability to see that using a screwdriver and screw could do the same job—arguably better. ^[Image: Ed Munoz https://www.flickr.com/photos/basementden/3536895965/. Creative Commons CC BY-NC-ND 2.0 https://creativecommons.org/licenses/by-nc-nd/2.0/]

<img src="images/3536895965_59217f40d0_k.jpg" alt="wood screw" width="300"/>



And having a "hammer and nail" mindset is almost certainly going to make it a challenge to learn that there are ways to join wood that don't involve using bits of metal or any other fasteners at all. The innovation of a dovetail joint is going to challenge your Einstellung. ^[Image: Caroline Jones, https://www.flickr.com/photos/cjwoodworkingdesign/8310710895/. Creative Commons CC BY-NC-ND 2.0 https://creativecommons.org/licenses/by-nc-nd/2.0/]

<img src="images/8310710895_5a6d440eb0_k.jpg" alt="dovetail joint" width="300"/>















The same is true for data science. People who are new to both data science and R learn the data wrangling and modeling methods (say, what a linear regression _is_: what the regression line depicts, what the residuals are measuring, etc.) as well as the tool.

`lm(y ~ x)`

But what about the situation where someone has established experience doing data science using other tools, and we want to introduce them to the wonders of R?


### At work

Workflow images

* old

* new

Some of my colleagues have embraced R and moved to create some great things using R.

But some of my colleagues haven't jumped on the bandwagon. I have used these images to try to pursuade people that the simplification shown is enough, minimizing the number of tools and therefore the switching back and forth, the copy-and-pasting, and extending the functionality.

But they continue to use R.

I've also heard some variations of

* If it ain't broke, don't fix it

* I know what I'm doing with my combination of tools, and I can produce the reports my clients need—why should I invest the time in learning a new way to do the same thing?

And more troublingly from people who have demonstrated some interest. They have installed R and RStudio on their machines, taken some workshops from some renowned instructors, but there it sits: "I think I can see the benefit of R programming but I am still struggling with it. I can't commit the time to learn this new thing because I have deadlines so I'll just stick with what I know."

Einstellung.


Einstellung also shows up in the habits we develop—including the bad habits, such as how we name things or how we use spreadsheets. (#EIKIFJB)


### Teaching a course

Data Analytics Coding Fundamentals

Teaching 

<img src="images/BIDA302_hex_300.jpg" alt="BIDA302 hex" width="300"/>

The course is the second in a series; the first is an introduction to data analytics.

For simplicity's sake, consider the two axes as having three bins, with a "none" or "a little", or "a lot". There is no students who are high on both "data analytics" and "coding" dimensions—the people who have those skills can jump into the course series in the higher level classes.

Some people were new to both "data analytics" and "coding" when participating in the series. As well, some people were well along the "coding" (X) axis. I have had course participants who were familiar with SQL, Python, and COBOL. For these two student personas, moving into data science meant learning the "data analytics" portion. For these people, this meant the creation of summary statistics such as grouped means, an introduction to linear models, and plotting, and using R to create those.

The third group are, in some ways, similar to those work colleagues I mentioned earlier. They have a lot of data analytics experience, and are in the second or third bin on the Y axis. They can mentally visualize what a summary table or plot is going to look like based on the structure of the source data, because they have done it before. They've created analytic outputs with workflows that look like Figure 1. And these people have signed up for a six-week course that is a significant commitment of time and money, so they are motivated to learn the data analytics component.

But in some ways they have the most friction. For the newcomers, this is all new, so while it's a lot of content to take in all at once, the creation of summary tables and the R code to make it happen are inextricably linked. For the programmers, R has its quirks but they have had to deal with the quirks of all the other languages they know, and they embrace the syntax once they see that it streamlines working with vector and tabular data structures. For them, the focus of the learning is the "data analytics"—what am I trying to accomplish programatically? 

The data analysts know what they want to do, but have become used to working in a GUI environment where the data is central in how the tool is accessed.

























***

### Footnotes

[^1]: Kenneth M. Miller, ["Einstellung rigidity, intelligence and teaching methods"](https://onlinelibrary.wiley.com/doi/abs/10.1111/j.2044-8279.1957.tb01400.x), _British Journal of Educational Psychology_, Vol. 27 Issue 2, June 1957, pp.127-134, DOI 10.1111/j.2044-8279.1957.tb01400.x

