---
title: A data science workflow example
subtitle: School enrollment in southern Vancouver Island
author: Martin Monkman
date: "2022-10-31"
publishDate: "2022-10-31"
draft: true
diagram: true
featured: yes
image:
  caption: '_Mickey slips on soap_'
  placement: 3
markup: mmark
math: true
tags:
- data science
- using R
- teaching
- learning
- school enrollment
output:
  html_document
---



<!--
Copyright 2022 Martin Monkman

This work is licensed under the Creative Commons Attribution 4.0 International License.
To view a copy of this license, visit http://creativecommons.org/licenses/by/4.0/.
-->


>_This blog post is an expanded version of an on-the-fly project walkthrough I presented during the last class of BIDA405, 2022-10-20"._



***


## Research question

How is elementary school enrollment changing in the three school districts in the Victoria, British Columbia area?


```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)

```

First up, we will load the various data wrangling packages we need. Note that although {readxl} is part of the broader tidyverse, it doesn't load with the `library(tidyverse)` function.

```{r packages}
# packages
library(tidyverse)
library(readxl)

# utilities
library(here)
library(janitor)


```


## background

Ministry of Education
https://www2.gov.bc.ca/gov/content/education-training/post-secondary-education/data-research/enrolment-data

School district maps
https://www2.gov.bc.ca/gov/content/data/geographic-data-services/land-use/administrative-boundaries/school-district


BC Data Catalogue
https://catalogue.data.gov.bc.ca/dataset/bc-schools-student-enrolment-and-fte-by-grade

BC Schools - Student Enrolment and FTE by Grade 
PUBLISHED
Published By
Education Analytics
Description
Student enrolment and FTE by Grade to 2021/2022, including facility type and counts by indigeneity. Due to size, the data have been separated into three documents in each format (Excel and CSV): 1991/91 to 2003/04; 2004/05 to 2019/20; 2020/21 to 2021/22

Licence
Open Government Licence - British Columbia



## read data

use {bcdata} package
* https://cran.r-project.org/web/packages/bcdata/vignettes/bcdata.html

```{r}
# read data from the BC Data Catalogue
library(bcdata)

```

Search the data catalogue

```{r}
bcdc_search("Enrolment and FTE")

```

Our search turns up three different 

```{r}
bcdc_get_record("2c53729a-2453-4633-92f3-6876a45f8bc4")
```

**DON'T CHOSE THE EXCEL FILE!!!!"

```{r}
# if you run this - need to pick option 
#df_enrol <- bcdc_get_data("2c53729a-2453-4633-92f3-6876a45f8bc4")

# read data
df_enrol <- bcdc_get_data('2c53729a-2453-4633-92f3-6876a45f8bc4', resource = 'e2debe69-0d03-492f-b2dc-656fbe01cd38')
```

## data wrangling

because of characters in numeric column, change to numeric

* should I choose "integer" type?

```{r}

df_enrol <- df_enrol %>% 
  mutate(
    TOTAL_ENROLMENT = as.numeric(TOTAL_ENROLMENT)
    )

```

explore data--what are the variables?


```{r}
ls.str(df_enrol)

df_enrol %>% 
  distinct(PUBLIC_OR_INDEPENDENT)
df_enrol %>% 
  distinct(GRADE)
df_enrol %>% 
  distinct(DATA_LEVEL)

unique(df_enrol$FACILITY_TYPE)

```


## Victoria public schools

```{r}
# define list of districts in the region
yyj_districts <- c("Greater Victoria", "Sooke", "Saanich")
  
```

```{r}
# create subset table
df_enrol_victoria <- df_enrol %>% 
  filter(
    DISTRICT_NAME %in% yyj_districts
    )

head(df_enrol_victoria)
tail(df_enrol_victoria)

```

```{r}

df_enrol_elem <- df_enrol_victoria %>%
  filter(
    SCHOOL_YEAR == "2021/2022",
    FACILITY_TYPE == "Standard",
    DATA_LEVEL == "School Level",
    GRADE == "All Elementary"
    )

df_enrol_elem %>%
  group_by(DISTRICT_NAME) %>%
  summarise(n_enrol = sum(TOTAL_ENROLMENT, na.rm = TRUE)) %>%
  mutate(pct_enrol = n_enrol / sum(n_enrol))

```


Need both years in data...will have to re-do the filter

```{r}
df_ch_victoria <-
df_enrol_victoria %>%
  filter(
#    SCHOOL_YEAR == "2021/2022",
    FACILITY_TYPE == "All Facility Types",
    DATA_LEVEL == "District Level",
    GRADE == "All Elementary"
    ) %>% 
  select(
    SCHOOL_YEAR,
    DISTRICT_NAME,
    TOTAL_ENROLMENT
  )

```

## plot


```{r} 

ggplot(df_ch_victoria) +
  geom_point(aes(
    x = SCHOOL_YEAR, 
    y = TOTAL_ENROLMENT, 
    colour = DISTRICT_NAME)
    )

ggplot(df_ch_victoria, 
       aes(
    x = SCHOOL_YEAR, 
    y = TOTAL_ENROLMENT, 
    colour = DISTRICT_NAME)) +
  geom_point()




```

## dumbell plot

Dumbell plot:

* https://r-graph-gallery.com/web-extended-dumbbell-plot-ggplot2.html

* https://www.r-bloggers.com/2021/08/ggalt-make-a-dumbbell-plot-to-visualize-change-in-ggplot2/


This one with the gapminder data is promising--I am familiar with that data, so it will make understanding what's happening more straight-forward.

* using gapminder data https://datavizpyr.com/dumbbell-plot-in-r-with-ggplot2/

Hmm--there's some interesting code that I am not sure about. The `mutate(paired = rep())` function...the "paired" variable gets used in the plot, so maybe it's important.

I will stick it in my code chunk, and see what it does:

```{r}
## # from https://datavizpyr.com/dumbbell-plot-in-r-with-ggp## lot2/
## df_ch_victoria %>% 
##   arrange(DISTRICT_NAME) %>% 
## mutate(paired = rep(1:(n()/2),each=2),
##          year=factor(SCHOOL_YEAR))

```

The new "paired" variable corresponds with the district name--both of the Greater Victoria records are numbered "1", Saanich is "2" and Sooke is "3". So why can't I just used the district name as my grouping variable?

Let's test that.

The example uses a `geom_line()` function, with the group defining how the points are joined.

```{r}

ggplot(df_ch_victoria, 
       aes(
    x = SCHOOL_YEAR, 
    y = TOTAL_ENROLMENT, 
    colour = DISTRICT_NAME)) +
  geom_point() +
  geom_line(aes(group = DISTRICT_NAME))



```

From this point, we can add all manner of formatting to make this more visually appealing.

However, the differences in the district sizes obscures the rate of change. So I will create an index, setting the first year as 100 and then the 2nd year as a percentage of the first. This will show the growth rate more clearly.

## create index

```{r}
df_ch_victoria <-
df_ch_victoria %>% 
  group_by(DISTRICT_NAME) %>% 
  mutate(enrol_index = TOTAL_ENROLMENT / first(TOTAL_ENROLMENT) * 100)
```

## create plot of index

```{r}
ggplot(df_ch_victoria, 
       aes(
    x = SCHOOL_YEAR, 
    y = enrol_index, 
    colour = DISTRICT_NAME)) +
  geom_point() +
  geom_line(aes(group = DISTRICT_NAME))

```

This shows the rate of change more clearly. In particular, that Sooke is growing most rapidly, while Saanich is shrinking--something that wasn't immediately apparent in the previous chart.

From this point, we might want to see what the absolute change is--creating a new variable that shows the number of students added (or subtracted) in the 2nd year.

The resulting plot will be similar to the index, but will have 0 as the starting point.

-30-