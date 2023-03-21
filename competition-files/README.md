Predicting Inventory Needs
================

In this repository/directory you should see the following items:

- `README.md` - this document.
- `mini-competition.Rmd` - an empty RMarkdown file for you to keep track
  of your explorations and provide detailed notes.
- `data` - a subfolder containing the dataset.

## The “rules”

You and your team have been “hired” by Mr. Greg Sperlbaum - purchasing
manager at a local supply chain company. You are tasked with predicting
future inventory needs based on past monthly sales.

By **4:00 pm on Tuesday, March 28** you need to create a Google slide
deck that only contains four-slides. At least one member from each team
will provide a 5-minute maximum presentation of these slides.

Instead of asking questions after each presentation, we will hopefully
have time at the end to have a closing conversation. Also, to help
create slides quickly (so you can focus on the modeling task), we will
use Google Slides instead of creating [slides in
RMarkdown](https://rmarkdown.rstudio.com/lesson-11.html).

Upload your slides to this Google folder by the deadline:
<https://drive.google.com/drive/folders/1oVFzj9wA7FdMazi-fORrz5Y6B8qRjF6e?usp=share_link>

Presentation order will be randomly determined around 4:01 pm and edits
to your slides will not be allowed.

While this is a friendly competition, the main purpose is to share your
ideas/process and learn from your peers and their ideas/process. I
(Bradford) will determine the “best” group based *only* on your
presentation by assessing each of the following categories on a
“missing/attempted/sufficient”-scale (or 0/0.5/1 point-scale; I will be
very [stingy](https://www.merriam-webster.com/dictionary/stingy) with
awarding “1”s except for the last category):

- Clarity of your presentation for a non-data scientist (i.e., Greg),
- Soundness of your approach,
- Aesthetically pleasing presentation, and
- Maximum of 5-minutes and four slides (only 0 or 1 possible).

The best group based on these categories will receive a prize.

### Your task

You want to be able to predict future inventory needs for as many unique
products as possible. This should include efficient code that **fits a
model for each product** you decide to model. If you are not including
certain products, explain why.

While we have not explored assessing generalized linear models for count
data in class, it is part of your task to research and implement
assessing the “goodness” of your predictions.

### Data

These are real sales data from a real company. Please do not distribute
this data beyond our class and do not push this to GitHub. Reach out to
me if you need assistance to avoid doing this.

You have an `inventory.csv` datafile posted on Blackboard directly under
the link you used to access this GitHub repository. You will need to
download this file, then upload to your RStudio Workbench session
(deleting the file from your personal machine once this competition is
over).

To focus your analysis and avoid some pitfalls, this is a subset of all
products sold by this company. Specifically, this file only contains
products that had more than 500 items sold in the past 53 weeks. If you
choose to further subset this datafile, be sure to explain your
decisions. For example, sparsity is a perfectly valid reason. However,
you should be prepared to explain (and show) why any products were
removed.

Greg has provided you with the following variables:

| Variable  | Description                                                                                |
|:----------|:-------------------------------------------------------------------------------------------|
| `item_no` | The company’s product number for each item                                                 |
| `week`    | Week of the year with 0 representing a year and one week ago and 53 representing last week |
| `sold`    | The number/count of an item sold during a week - this is your response variable            |

### Suggestions to get started

- Make appropriate exploratory graphs and numerical summary tables.
- What methods would be appropriate for this type of data? In
  [Additional resources](#additional-resources) below, I provide some
  helpful-to-me resources. These are not exhaustive.
- What products are you fitting a model for and why are you excluding
  some products?
- How will you measure the “goodness” of your predictions?

## Additional resources

We have not directly practiced methods for handling this type of
response variable. However, you were encouraged to read Sections 4.6 and
4.7 from *ISL* that show similar methods.

- I have shared Emil Hvitfeldt’s *ISLR tidymodels labs* which uses
  `{tidymodels}` to cover topics that *ISL* does in base R. This will
  take you to his chapter corresponding to the [Classficiation
  labs](https://emilhvitfeldt.github.io/ISLR-tidymodels-labs/04-classification.html).
- UCLA’s Advanced Research Computing team provides great examples for
  various [statistical learning
  problems](https://stats.oarc.ucla.edu/other/dae/).
- The University of Wisconsin - Madison’s Social Science Computing
  Cooperative provides a good overview of [Generalized Linear Models in
  R](https://sscc.wisc.edu/sscc/pubs/glm-r/index.html).
- *Tidy Modeling with R* by Max Kuhn and Julia Silge has great
  examples/discussion on working with [generalized linear
  models](https://www.tmwr.org/inferential.html).

## What is next?

Next week will explore computationally heavy methods for assessing
models and selecting model features beginning with resampling methods
(Chapter 5).
