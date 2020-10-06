# Assignment 5: Constructing Datasets and Using Databases


__Due: 2020-10-11__

_there will be no tolerance of late submissions on this assignment because it will be graded Monday, so that you can use that feedback to finish up your portfolio.

## Instructions
_this will earn level 2 for construct_

Your goal is to build and prepare two ready to analyze datasets. You will submit a notebook that describes how you built and prepared each dataset.
- Each finished dataset must be produced from two or more tables.
- At least one must come from an sqlite database, either by merging results from multiple queries or multiple tables.
- You should use at least three different merges and one concatenate

Your completed datasets should have:
- column names that are well formatted (only lowercase letters, numbers and `_`)
- an added column that is derived from one or more other columns (string operation or calculation)


For each dataset, pose one question that could not be answered from the input data files as provided and demonstrate how to answer it with the dataset you built. This could be something that can be answered with using only `shape` of the merged data, but if you need summarize and visualize level 2 achievements, you should use more statistics and plots.


## Additional Achievements:

_if you already earned prior achievements you can ignore the following_

To earn level 2 for prepare, one of your analyses must use datasets with missing values and one must be provided as excel files with merged columns (for example from [NCES](https://nces.ed.gov/programs/digest/current_tables.asp)). You may use one dataset with both merged columns and missing data or one of each. You must also use datasets that have column names that need repair.  
For the merged column data, either before or after merging, you must additionally:
- create separate separate tables for original and aggregate values (eg percentages or sums that can be recovered from the other columns)
- unstack all levels of the data to create a single level index over the columns
- create a database with the tables



To earn level 2 for summarize and/or visualize, include additional analyses after building the datasets. You'll need at least two types of plots for visualize and/or two different ways of using summary statistics for summarize and to interpret the results for either.
