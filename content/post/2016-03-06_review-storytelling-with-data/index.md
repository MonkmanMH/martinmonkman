---
date: "2016-03-06"
diagram: true
image:
  caption: '[Storytelling with Data](https://www.storytellingwithdata.com)'
  placement: 3
markup: mmark
math: true
tags:
- data science
- book review
title: Book review--Storytelling with Data
---



#### by Cole Nussbaumer Knaflic (2015, Wiley)


_Originally posted to [bayesball.blogspot.com](https://bayesball.blogspot.com/2016/03/book-review-storytelling-with-data.html), 2016-03-06_


One of the great strengths of R is that there are some robust (and always improving) packages that facilitate great data visualization and tabular summaries. Beyond the capabilities built into the base version of R, packages such as `ggplot2` (my favourite), `lattice`, and `vcd` and `vcdExtra` extend the possibilities for rendering charts and graphs, and a similar variety exist for reproducing tables. And accompanying these packages have been a variety of fine instruction manuals that delineate the code necessary to produce high-quality and reproducible outputs. (You can't go wrong by starting with Winston Chang's _R Graphics Cookbook_, and the [R Graph Catalog](http://shiny.stat.ubc.ca/r-graph-catalog/) based on Naomi Robbins's _Creating More Effective Graphs_, created and maintained by Joanna Zhao and Jennifer Bryan at the University of British Columbia.)

Let's call these the "how" resources; once you've determined you want a Cleveland plot (which are sometimes called "lollipop plots"---please, just stop it), these sources provide the code for that style of chart, including the myriad options available to you.

Elsewhere, there has been a similar explosion in the number of books that build on research and examples as to what makes a good graphic.  These are the "what" books; the authors include the aforementioned William Cleveland and Naomi Robbins, and also include  Stephen Few and Edward R. Tufte. Also making an appearance are books that codify the "why", written by the likes of Alberto Cairo and Nathan Yau.

The recently published _Storytelling with Data: A Data Visualization Guide for Business Professionals_ by Cole Nussbaumer Knaflic falls into the latter category, and it's one of the best I've seen to date. Although the subtitle indicates the intended audience, I believe that anyone involved in creating data-driven visualizations would benefit from reading and learning from it.

The book is relatively software agnostic, although Nussbaumer Knaflic recognizes the ubiquity of Excel and has used it to produce the charts in the book. She also provides some sidebar commentary and tools via her website [http://www.storytellingwithdata.com/](http://www.storytellingwithdata.com/) specifically using Excel. For R users, this shouldn't pose a particular challenge or barrier; the worst-case scenario is that it provides an opportunity to learn how to use R to replicate the book's examples. 

One of the strengths of the book is that Nussbaumer Knaflic takes the approach of starting with a chart (often a real-life example published elsewhere), and then iterates through one or more options before arriving at the finished product. One instance is the step-by-step decluttering of a line graph, which becomes substantially improved through a six step process. This example re-appears later, first in the chapter on the use of preattentive attributes and then again in the chapter titled "Think like a designer". This approach reinforces the second of Nussbaumer Knaflic's tips that close the book, "iterate and seek feedback".

Nussbaumer Knaflic also introduces the Gestalt Principles of Visual Perception, and provides vivid examples of how these principles play out in data visualizations.

All of the discussion of graphics is wrapped in the context of storytelling. That is to say, the data visualization is always in the service of making a point about what the data tell us. In the context of business, this then translates into influencing decisions. The chapter "Lessons in storytelling" falls almost exactly in the middle of the book; after we've been introduced to the principles of making good data visualizations, Nussbaumer Knaflic gives us a way to think about the purpose of the visualization. With all of the pieces in place, the remainder of the book is focussed on the applications of storytelling with data.

The book is supported with Nussbaumer Knaflic's site [storytellingwithdata.com](http://www.storytellingwithdata.com/), which includes her blog. Check out her blog entry/discussion with Steven Few (["Is there a single right answer?"](http://www.storytellingwithdata.com/blog/2016/1/12/is-there-a-single-right-answer)), and some [makeovers (in the Gallery)](http://www.storytellingwithdata.com/gallery/) where she redraws some problematic charts that have appeared in the public domain. 

All in all, Cole Nussbaumer Knaflic's _Storytelling with Data_ is a succinct and focussed book, one that clearly adopts and demonstrates the enormous value of the principles that it espouses. Highly recommended to anyone, of any skill level, who is interested in making effective data visualizations, and the effective use of those visualizations.  

Cole Nussbaumer Knaflic's  _Storytelling with Data: A Data Visualization Guide for Business Professionals_ was published in 2015 by Wiley.

_Cross-posted at [bayesball.blogspot.com](bayesball.blogspot.com)_

#### References

Note: the authors of the following books have all published additional books on these topics; I've simply selected the ones that most closely fit with the context of this review. All are recommended.

* Alberto Cairo, _The Functional Art: An Introduction to Information Graphics and Visualization_ (2013) New Riders.

* Winston Chang, _R Graphics Cookbook_ (2012) O'Reilly.

* William S. Cleveland, _Visualizing Data_ (1993) Hobart Press.

* Stephen Few, _Signal_ (2015) Analytics Press.

* Michael Friendly and David Meyer, _Discrete Data Analysis with R: Visualization and Modeling Techniques for Categorical and Count Data_ (2016) CRC Press.

* Naomi B. Robbins, _Creating More Effective Graphs_ (2004) Reprinted 2013 by Chart House.

* Edward R. Tufte, _The Visual Display of Quantitative Information_ (2nd edition, 2001) Graphics Press.

* Hadley Wickham, _ggplot2: Elegant Graphics for Data Analysis_ (2nd edition, 2016) Springer.

* Nathan Yau, _Visualize This: The FlowingData Guide to Design, Visualization, and Statistics_ (2011) Wiley.

-30-
