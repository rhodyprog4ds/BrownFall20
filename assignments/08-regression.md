# Assignment 8

__Due: 2020-11-03__


## Linear Regression

Find a dataset suitable for regression. We recommend a dataset from the UCI repository (see bottom)

Fit a regression model, measure the fit with two metrics, and make a plot that helps visualize the result.  

Examine the [coefficients](https://rhodyprog4ds.github.io/BrownFall20/notes/2020-10-28.html#digging-in-deeper-to-the-linear-regression-model) or the [residuals](2020-10-30) to try to interpret the results and explain what this regression model is doing.

Try fitting the model only on one feature. Justify your choice of feature based on the results above.  Plot this result.

[Accept the assignment](https://classroom.github.com/a/RHbMBUNd) to create your submission repository



__Part 2: Test Train Splits__

_if you successfully completed this experiment in assignment 7, you don't need to repeat it, but it might be interesting to try_

Do an experiment to compare test set size vs performance:
1. Train a the linear regression model on 20%, 30%, ... , 80% of the data.
1. Save the results of both test and train accuracy for each size training data in a DataFrame with columns ['train_pct','n_train_samples','n_test_samples','train_acc','test_acc']
1. Plot the accuracies vs training percentage.  
1. Explain these results. What is the best test/train split. Why?


__Part 3: Other models__

Try fitting LASSO and explaining what it does. Does LASSO make better predictions on your data?

Do you think a model more complex than linear would be better? How could you tell?  

## Grading

For regression level 2, complete part 1.

For evaluate level 2, complete part 2.

If you're curious, try a more complex regression model as in part 3.  This will get you an early start on level 3 for regression.  


If you don't successfully complete the whole assignment, pseudocode or partial answers to the questions could earn you level 1 for either skill.



## FAQ

### How do I find a good dataset?

Look for a dataset with numerical features and a categorical target variable.

If you look at the [UCI website](https://archive.ics.uci.edu/ml/datasets.php?format=&task=reg&att=&area=&numAtt=&numIns=&type=&sort=nameUp&view=table ) you can search for datasets for Classification and numerical and look through what those search filters give you some options.  You might want to choose a dataset with less than about 20 attributes.  To make the training fast, try to find a dataset with 1000 samples or less, or use read functions to use only a small chunk of the data.  Remember to read about the dataset and note what you're predicting.   
