# Assignment 1: Portfolio Setup, Data Science, and Python

## Objective & Evaluation

This assignment is an opportunity to earn level 2 achievements for the `process` and `python` and confirm that you have all of your tools setup, including your portfolio.

## To Do

````{margin}
```{note}
If you get stuck on any of this after accepting the assignment and creating a repository, you can create an issue on your repository, describing what you're stuck on and tag us with `@rhodyprog4ds/fall20instructors`.

To do this click Issues at the top, the green "New Issue" button and then type away.
```
````

Your task is to:
1. Install required software
1. Setup your portfolio, by [accepting the assignment](https://classroom.github.com/a/m-WYYP0Q) and following the instructions in the README file on your repository.
1. Add your own definition of data science to the introduction of your portfolio, in `about/index.md`
1. Add a Jupyter notebook called `grading.ipynb` to the `about` folder and write a function that computes a grade for this course, with the following docstring. Include:
-  a Markdown cell with a heading
- your function called `compute_grade`
- three calls to your function that verify it returns the correct value for different number of badges that produce at three different letter grades.
1. Uncomment the line `#     - file: about/grading` in your `_toc.yml` file.

```
    '''
    Computes a grade for CSC/DSP310 from numbers of achievements at each level

    Parameters:
    ------------
    num_level1 : int
      number of level 1 achievements earned
    num_level2 : int
      number of level 2 achievements earned
    num_level3 : int
      number of level 3 achievements earned

    Returns:
    --------
    letter_grade : string
      letter grade with possible modifier (+/-)
    '''
```

Here are some sample tests you could run to confirm that your function works correctly:
````{margin}
```{warning}
your function can have a different name than `compute_grade`, but make sure it's your function name, with those parameter values in your tests.
```

```{note}
when the value of the expression after `assert` is `True`, it will look like nothing happened. `assert` is used for testing
```
````

```
assert compute_grade(15,15,15) == 'A'

assert compute_grade(15,15,13) == 'A-'

assert compute_grade(15,14,14) == 'B-'

assert compute_grade(14,14,14) == 'C-'

assert compute_grade(4,3,1) == 'D'

assert compute_grade(15,15,6) =='B+'
```


## Submission Instructions

Create a Jupyter Notebook with your function and
Add the notebook to your portfolio by uploading it to your repository, or adding to the folder off line and committing and pushing the changes.

View the `gh-pages` branch to see your compiled submission, as `portfolio.pdf` or by viewing your website.

There will be a pull request on your repository that is made by GitHub classroom, [request a review](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/requesting-a-pull-request-review) from the team `rhodyprog4ds/Fall20instructors`.

## Solutions

One solution is added to the [Detailed Mechanics](grade:calculation) part of the Grading section of the syllabus.
