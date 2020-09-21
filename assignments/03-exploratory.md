# Assignment 3: Exploratory Data Analysis

__Due: 2020-09-27__

## Objective & Evaluation

This assignment is an opportunity to earn level 1 or 2 achievements in `summarize`, `visualize`, or `access`. You can earn level 2 in `python`.


Accept the assignment on [GitHub Classroom](). It contains a notebook with some template structure (and will set you up for grading). The template will also convert notebooks that are added to markdown, which makes reading on GitHub for easier grading. If you want to incorporate feedback you receive back into a notebook file, [Jupytext](https://jupytext.readthedocs.io/en/latest/using-cli.html) can do that.  

This week I encourage you to try working with git, but if you're not comfortable with that you can work via upload again.  



## Exploratory Data Analysis



This week your goal is to do a small exploratory data analysis for two datasets of your choice. One dataset must include at least two continuous valued variables and at least one categorical variable(d1). One dataset must include at least two categorical variables and at least one continuous valued variable(d2).


Use a separate notebook for each dataset, name them `dataset_01.ipynb` and `dataset_02.ipynb`.


For each dataset:
1. Load the data to a notebook as a `DataFrame` from url.
1. Explore the dataset in a notebook enough to describe its structure
  - shape
  - columns
  - variable types
1. Write a short description of what the data contains and what it could be used for
1. complete one of the analyses below
1. Describe what, if anything might need to be done to clean or prepare this data for analysis

For d1:
1. Display overall summary statistics
1. Display overall summary statistics grouped by a categorical variable
1. For two continuous variables make a scatter plot and color the points by a categorical variable
1. Pose one question for this dataset that can be answered with summary statistics, compute a statistic and plot that help answer that exploratory question.


For d2:
1. Display two individual summary statistics for one variable
1. Group the data by two categorical variables and display a table of one summary statistic
1. Use a `FacetGrid` to make a plot that shows something informative about this data, using both categorical variables and at least one numerical value. Describe what this tells you about the data.
1. Produce one additional plot of a different plot type that shows something about this data.
