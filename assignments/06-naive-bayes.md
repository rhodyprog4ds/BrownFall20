# Assignment 6


__Due: 2020-10-20__


Remember, even if you aren't sure how to do every part of the assignment, submitting pseudocode, a list of your questions indicating where you got stuck, or a partial solution will get you personalized feedback. You might even earn level 1 achievements for the partial effort.

## For Classification Level 2:

[Acccept the Assignment](https://classroom.github.com/a/fojgz8Cc)



Create one notebook where you load examine each of the provided datasets for for suitability to use with Gaussian Naive Bayes. Label the sections `Dataset #`. Use exploratory data analysis (visualisation and statistics) in pandas and Gaussian Naive Bayes from scikit learn to answer the following for each dataset:


1. Do you expect Gaussian Naive Bayes to work well on this dataset, why or why not? (think about the assumptions of naive bayes and classification in general) _explanation is essential here, because you can actually use the classifier to check_
1. How well does a Gaussian Naive Bayes classifier work on this dataset? Do you think a different classifier might work better or do you think this data cannot be predicted any better than this?
1. How does the actual performance compare to your prediction?  If it performs much better or much worse than you expected, what might you use to figure out why? (_you do not have to figure out why your predictions were not correct, just list tools you've learned in class that might help you figure that out_)


This assignment will be easiest if you take advantage of the template via git: 

### Git Workflow

1. Click the green code button and copy the url.
1. clone the repository as below where th eurl is the one you copied from GitHub. In your terminal on Linux or Mac or on the GitBash on Windows ([install instructions on tools section of syllabus](prorgrammin-env) )

  ```
  cd path/where/you/want/a/new/folder/for/this/assignment
  git clone http://github.com/rhodyprog4ds/06-classification-username
  ```

1. then launch your notebook from the newly created folder.

  on Linux or Mac, in the same terminal (remember you can use tab complete)
  ```
  cd 06-classification
  jupyter notebook
  ```
  or on windows, in your Anaconda prompt
  ```
  cd path/where/you/want/a/new/folder/for/this/assignment/06-classification-username
  jupyter notebook
  ```

1. work on your assignment, by opening the notebooks there and editing them.
1. commit your changes when you want to save a point in your progress. Either you have part workign and want to save that, or you want feedback, or you're done. On whichever terminal you used for the `git clone` command above

  ```
  git add .
  git commit -m 'description of your changes since las commit'
  ```

1. push your changes when you want to share them on GitHub, (eg need help, want feedback or complete)

  ```
  git push
  ```

1. if you will keep working after pushing, first pull down the .md conversion that was added by GitHub actions.  If you don't you'll have to merge, it should be fine, but ask if you're not sure.

  ```
  git pull
  ```



## For construct level 2

Build your own dataset for classification by merging data from separate sources that you're interested in.


## Summarize and Viz level 2

Show some extra summary stats and plots
