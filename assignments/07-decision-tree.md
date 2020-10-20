# Assignment 7

__Due: 2020-10-27__

## For Classification and Evaluation Level 2

Choose a datasets that is well suited for classification and that has all numerical features. (eg the Wisconsin Breast Cancer data from UCI)

__Part 1: DT Basics__
1. Include a basic description of the data(what the features are)
1. Write  your own description of what the classification task is and why a decision tree is a reasonable model to try for this data.
1. Include one summary visualization fo the data.
1. Fit a decision tree with the default parameters on 50% of the data
1. Test it on 50% held out data and generate a classification report
1. Inspect the model by visualizing and interpretting the results
  - Does this model make sense?
  - Are there any leaves that are vey small?
  - Is this an interpretable number of levels?
1. Repeat with the entropy criterion. Does using the entropy criterion make a big difference or small difference in the overall classifier?

__Part 2: DT parameters__


Do an experiment to see how `max_depth`, `min_values_split`, or `min_values_leaf` impacts the model.
1. Choose one of these and say explain why and how you hypothesize it will impact the performance
1. Use the model you fit above and EDA to choose minimum and maximum values for your parameter.
1. Retrain the model for each value of the parameter
1. Test and use at least 3 metrics to describe the performance, compiling your results into a dataframe
1. Plot and interpret your results

_you should use a loop for this part_


__Part 3:__

Do an experiment to compare test set size vs performance:
1. Train a decision tree on 20%, 30%, ... , 80% of the data, using one of the training parameter combinations you tried above and explain why you chose the one you chose.
1. Save the results of both test and train accuracy for each size training data in a DataFrame with columns ['train_pct','n_train_samples','n_test_samples','train_acc','test_acc']
1. Plot the accuracies vs training percentage.  
1. Explain these results. What is the best test/train split. Why?

_you should use a loop for this part_
