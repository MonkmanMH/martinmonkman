---
title: Continuous Learning in a Time of Continuous Change
author: Martin Monkman
date: "2022-05-30"
publishDate: "2022-05-30"
draft: true
diagram: true
featured: yes
image:
  caption: '_Stephen Leacock_'
  placement: 3
markup: mmark
math: true
tags:
- data science
- using R
- teaching
- learning
- career
- professional development
output:
  html_document
---



<!--
Copyright 2022 Martin Monkman

This work is licensed under the Creative Commons Attribution 4.0 International License.
To view a copy of this license, visit http://creativecommons.org/licenses/by/4.0/.
-->


>_This blog post is a long-form version of the talk I gave at the Statistical Society of Canada conference._



***

## Abstract


**Continuous Learning in Times of Continuous Change**

It’s a universally accepted truism that we live in a time of unprecedented change, both in terms of the magnitude and the pace of those changes. In the world of statistics, there have been enormous changes at the intersection of tools, methodologies and techniques, and transparency. New software packages, new ways to analyze data, and new open data arrive every day, each of which have implications for how we approach our professional development. In this talk, I will present observations drawn from applied statistical practice and teaching mid-career professionals that suggest possible responses that will allow us to keep pace with a perpetually shifting ecosystem.


**L'apprentissage continu en période de changement permanent**

C'est un truisme universellement accepté que de dire que nous vivons une époque de changements sans précédent, tant en termes d'ampleur que de rythme de ces changements. Dans le monde des statistiques, les outils, les méthodologies, les techniques et la transparence ont connu d'énormes changements. De nouveaux logiciels, de nouvelles méthodes d'analyse des données et de nouvelles données ouvertes arrivent chaque jour, chacun ayant des implications sur la manière dont nous abordons notre développement professionnel. Dans cet exposé, je présenterai des observations tirées de la pratique de la statistique appliquée et de l'enseignement à des professionnels en milieu de carrière qui suggèrent des réponses possibles qui nous permettront de suivre le rythme d'un écosystème en perpétuelle évolution.


Traduit avec www.DeepL.com/Translator (version gratuite)



***


Stephen Leacock, on getting his Doctor of Philosophy:

>The meaning of this degree is that the
recipient of instruction is examined for the last time in his life, and
is pronounced completely full. After this, no new ideas can be imparted
to him. ^[Preface, [_Sunshine Sketches of a Little Town_](https://onlinebooks.library.upenn.edu/webbin/gutbook/lookup?num=3533), 1912] 



## Career

Punch cards

Data stored on tape

Word processors before WYSIWYG

Spreadsheets before GUI

Methods constrained by the limitations of the tools

* Markov chain Monte Carlo (MCMC): as Christian Robert and George Casella have written, the paradigm shift of MCMC methods trace back to 1953, but it wasn't until 1990 that the theory and the necessary computing power converged^[Christian Robert and George Casella, "A Short History of Markov Chain Monte Carlo: Subjective Recollections from Incomplete Data", _Statistical Science_, 2011, Vol. 26, No. 1, 102-115. [DOI: 10.1214/10-STS351](https://projecteuclid.org/journals/statistical-science/volume-26/issue-1/A-Short-History-of-Markov-Chain-Monte-Carlo--Subjective/10.1214/10-STS351.full)]


I present these as examples as what has changed over the span of my career. We have adapted to typing our instructions into script files, pointing and clicking our way around our spreadsheets, and happily adding new methods to our approach to data analysis.

## A paradigm shift

But there has been—or perhaps, more accurately, we are in the midst of—a paradigm shift. And it's not so much in the fact that the tools have changed, it's that they _continuously_ change.

Open source software is in a constant state of development. In the R ecosystem, one I am familiar with, the core of R changes slowly. Updates come every six months or so, and the team of developers are mindful that they should not introduce breaking changes.

The packages around the core of R are a different story. There are, as of 2022-03-14, 18996 packages available on CRAN (the Comprehensive R Archive Network). These are packages that have passed rigorous scrutiny, and are maintained to ensure currency. There are many other packages that are available for download from sites such as GitHub.

We can look at the development history of a widely-used data wrangling package, {dplyr}^[Wickham H, François R, Henry L, Müller K (2022). [_dplyr: A Grammar of Data Manipulation_](https://dplyr.tidyverse.org).]. Version 1.0.0 was released on May 29, 2020. In the space of a little over a year (386 days, to be precise) seven updates were released. 


## The craft of data science

This shift in how our toolkit changes means that we need to adapt our approach to how we learn.




## Are our brains full?

I opened with a quote from Stephen Leacock, suggesting that our brains have a finite capacity, and one that is filled fairly early in life (if we consider that someone might finish their PhD in their late 20s or early 30s). 

But in truth, Leacock held a very different view:

>what I want to advocate is not to make education shorter, but to make it much longer—indeed to make it last as long as life itself.

>What I find wrong is the stark division now existing between the years of formal education and entry into the work of life. Education has become to a great extent a mere acquirement of a legal qualification to enter a closed profession, in place of being a process undertaken for its own sake. **All that is best in education can only be acquired by spontaneous interest; thus gained it lasts and goes on.**^[Preface, [_Too Much College, or, Education Eating Up Life_](https://gutenberg.ca/ebooks/leacock-toomuchcollege/leacock-toomuchcollege-00-h.html), 1939. Emphasis added.]

See also _Leacock on Life_ https://www.jstor.org/stable/10.3138/9781442676619




-30-
