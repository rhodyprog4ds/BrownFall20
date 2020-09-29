# Assignment 4:

__Due: 2020-10-04__

## Objective & Evaluation

You can earn prepare level 2 and by completing the `cs_degrees.ipynb` and `travel_time.ipynb` analyses.

To earn access level 2 you must also do `airlines.ipynb` or `safi_full.ipynb` note that this is the SAFI dataset we've been working with in class, but a messier version of it. You know what some of the fixes are because they're in the notes and some of what it will look like when it's done.  

To earn python level 2, you must complete `safi_full.ipynb`, if you successfully use list or dictionary comprehensions and conditional statements, beyond those provided as hints.

To earn level 2 for summarize and visualize, include additional analyses after cleaning the datasets. You'll need at least two types of plots and two different ways of using summary statistics and to interpret the results.


## Instructions

For this assignment, your assignment is to clean datasets in notebooks and include narrative description of how you're making decisions about the data cleaning. At the end of each cleaning, save the cleaned dataset to the data folder with an informative file name.

````{margin}
```{tip}
You can download any of the files and open them with another program if you need to by pasting the url in your browser. You'll need to display relevant parts in a notebook for grading, but if looking another way helps, you can try that.  
```
````

When you [accept the assignment](https://classroom.github.com/a/y723c6qi), there will be template notebooks in the repository. These have significant hints to guide your efforts.

There is an issue type with a todo list, try that out to plan and track questions you have.


You can work with this assignment in 2 ways:



### Git Workflow

1. Click the green code button and copy the url.
1. clone the repository as below where th eurl is the one you copied from GitHub. In your terminal on Linux or Mac or on the GitBash on Windows ([install instructions on tools section of syllabus](prorgrammin-env) )

  ```
  cd path/where/you/want/a/new/folder/for/this/assignment
  git clone http://github.com/rhodyprog4ds/04-prepare-username
  ```

1. then launch your notebook from the newly created folder.

  on Linux or Mac, in the same terminal (remember you can use tab complete)
  ```
  cd 04-prepare-username
  jupyter notebook
  ```
  or on windows, in your anaconda prompt
  ```
  cd path/where/you/want/a/new/folder/for/this/assignment/04-prepare-username
  jupyter notebook
  ```

1. work on your assignment, by opening the notebooks there and editing them.
1. commit your changes when you want to save a point in your progress. Either you have part workign and want to save that, or you want feedback, or you're done. On whichever terminal you used for the `git clone` command above

  ```
  git add .
  git commit -m 'description of current status of project'
  ```

1. push your changes when you want to share them on GitHub, (eg need help, want feedback or complete)

  ```
  git push
  ```

1. if you will keep working after pushing, first pull down the .md conversion that was added by github actions.  If you don't you'll have to merge, it should be fine, but ask if you're not sure.

  ```
  git pull
  ```



### Download and upload workflow
1. Click the green code button
1. choose the download via zip option
1. unzip
1. launch a notebook in the folder where you unzipped
1. Upload only the files you changed into the repository to replace their previous versions with the add file via upload button on GitHub.  Put the notebooks at the top level and the data files in the data folder.


## Tips and hints

- Pandas can [convert string to dates](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.to_datetime.html) to be able to work with them more flexibly
- With python [date](https://docs.python.org/3/library/datetime.html#datetime.date.fromisoformat) objects you can get the [day of the week](https://docs.python.org/3/library/datetime.html#datetime.date.weekday) from a date
- Pandas [`read_excel`](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.read_excel.html) has:
  - a `header` parameter can take a list as its value
  - two parameters that allow you to skip rows when you read in the data
- `list(range(7))` check out what this line does
-

The goal of the plot for the CS degrees dataset is:
![plots of degrees by level from 1971-11 by gender](../img/cs_degree_target.png)
