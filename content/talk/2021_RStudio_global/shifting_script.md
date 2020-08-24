<!--
Copyright 2020 Martin Monkman

This work is licensed under the Creative Commons Attribution 4.0 International License.
To view a copy of this license, visit http://creativecommons.org/licenses/by/4.0/.
-->

---
title: "Shifting data analysis mental models"
subtitle: "Intro script"
author: "Martin Monkman"
date: "2020/12/31"
output: html_document
---



# 



author: Martin Monkman

date of most recent revision: 2020-08-24


**rstudio::global(2021)**



## script

Talk theme:

* techniques for teaching R to help it reach new domains and new audiences


Abstract: 

People who have experience in data analysis and statistical practice have established mental models of their workflow. These mental models are often influenced by the GUI tools that are ubiquitous in business and academic settings. As a consequence, their introduction to R and data science practice needs to be different than the approach taken with someone (say, a student in a typical undergraduate statistics class) who is simultaneously learning both the underlying methods and how to use R to implement those methods. Experienced data analysts arrive in class knowing what their outcome (the artifact of their workflow) will be—perhaps a short analytic report that combines text, summary tables, and plots—and are seeking a different workflow to produce that artifact.  (And as we know, you can't do data science in a GUI.) 

In this talk I will explore how as an instructor in university continuing studies courses I have used RStudio, RStudio Cloud, and the tidyverse to guide experienced data analysts in shifting their mental models.

* A typical mental model of an experienced GUI data analyst, including the steps and terminology common in those tools.

* The concept of Einstellung: "the development of a mechanized state of mind", and the often bad habits that we develop

* How the verbs of the tidyverse, the access to visualizations of the data, and the reduced friction of RStudio, RStudio Cloud, and the tidyverse family of packages help overcome Einstellung and ease the introduction to R and a robust data science workflow.


Key words: teaching, adult learners, mental models, EIKIFJB


Call for talks
https://blog.rstudio.com/2020/07/17/rstudio-global-call-for-talks/



***

## Script

Hello!

I am Martin Monkman, and this is my video abstract for my proposed talk at rstudio::global(2021)

I have been doing data science (although I didn't know it was called that until rather recently) for years

And have been encouraging my colleagues to start adopting R into their workflow

As well, I have started teaching introductory data science courses through the local university's continuing studies department

In both of these contexts, I am introducing R to people who already have an established workflow practice. They know their analytic methods, and have build a workflow using available tools

These tools are often GUI--and we know you can't do data science in a GUI

Teaching these people R is different than, say, a typical undergraduate class where the students are learning both the methods AND the tools

I've come across the term "Einstellung" that is used to describe "the development of a mechanized state of mind". 

EIKIFJB

