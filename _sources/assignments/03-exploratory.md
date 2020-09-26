# Assignment 3: Exploratory Data Analysis

__Due: 2020-09-27__

## Objective & Evaluation

This assignment is an opportunity to earn level 1 or 2 achievements in `summarize`, `visualize`, or `access`. You can earn level 2 in `python`.


Accept the assignment on [GitHub Classroom](https://classroom.github.com/a/t2NWi3KU).  The template will convert notebooks that are added to markdown, which makes reading on GitHub for easier grading. It will sync between .ipynb and .md style notebooks stored in your repository.  

This week I encourage you to try working with git, but if you're not comfortable with that you can work via upload again.  



## Exploratory Data Analysis

````{margin}
```{tip}
A continuous valued variable is one that can take on infinitely many values.
Examples include temperatue, length, age, etc.
A categorical value is one that can only take on one of a subset of specific values.
These require a bit more context to define often.
For example color could be recorded in a basically continuous way as RGB values in HEX, but color of the stoplight will only be red, green, or yellow.
Town of birth in a dataset of celebrities would not be a good categorical variable, there might not be many duplicates to do analysis with, but metro area of current residence for celebrities would be because we'd see mostly major cities and could do analyses.
```
````

This week your goal is to do a small exploratory data analysis for two datasets of your choice. One dataset must include at least two continuous valued variables and at least one categorical variable(d1). One dataset must include at least two categorical variables and at least one continuous valued variable(d2).


Use a separate notebook for each dataset, name them `dataset_01.ipynb` and `dataset_02.ipynb`.


For each dataset:
````{margin}
```{tip}
if you use a local copy of the dataset you can load from a [relative path](https://en.wikipedia.org/wiki/Path_(computing)#Absolute_and_relative_paths) instead of a url. Please include the data in a data folder that's in the folder where your notebook is so that the path is something like: `data/best-dataset-ever.csv` and upload the data to your assignment repository as well. 
```
````

1. Include a markdown header with a title for your analysis
1. Load the data to a notebook as a `DataFrame` from url.
1. Explore the dataset in a notebook enough to describe its structure
  - shape
  - columns
  - variable types
1. Write a short description of what the data contains and what it could be used for
1. Complete an exploratory analysis with statistics and plots. Your analysis should include markdown cells  describing the results you see, not only what you did.  Your analysis should be structured to follow the steps below, for the corresponding dataset.

```{margin}
```{tip}
Recall how we used a single function to see many statistics in class, use that for dataset 1.
For dataset 2, you can make your own combination of summary statistics with [`pandas.DataFrame.agg`](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.aggregate.html)
```
````

For d1:
1. Display all of the summary statistics for a subset of 5 of your choice or all variables if there are fewer than 5 numerical values
1. Display all of summary statistics grouped by a categorical variable
1. For two continuous variables make a scatter plot and color the points by a categorical variable
1. Pose one question for this dataset that can be answered with summary statistics, compute a statistic and plot that help answer that exploratory question.


For d2:
1. Display two individual summary statistics for one variable
1. Group the data by two categorical variables and display a table of one summary statistic
1. Use a seaborn plotting function with the `col` parameter or a `FacetGrid` to make a plot that shows something informative about this data, using both categorical variables and at least one numerical value. Describe what this tells you about the data.
1. Produce one additional plot of a different plot type that shows something about this data.


In total, in each of your notebooks you will have:
- a loaded dataset
- a basic description
- at least two summary statistic calculations
- at least two plots
