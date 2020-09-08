---
jupytext:
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.12
    jupytext_version: 1.6.0
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---

## Learning Objective, Schedule, and Rubric

```{code-cell} ipython3
:tags: [remove-input]


import yaml as yml
import pandas as pd
import os
pd.set_option('display.max_colwidth', None)


def yml_df(file):
    with open(file, 'r') as f:
        file_unparsed = f.read()

    file_dict = yml.safe_load(file_unparsed)
    return pd.DataFrame(file_dict)

outcomes_df = yml_df('../_data/learning_outcomes.yml')
outcomes_df.set_index('keyword',inplace=True)
schedule_df = yml_df('../_data/schedule.yml')
schedule_df.set_index('week', inplace=True)
# schedule_df = pd.merge(schedule_df,outcomes_df,right_on='keyword',  left_on= 'clo')
rubric_df = yml_df('../_data/rubric.yml')
rubric_df.set_index('keyword', inplace=True)
```


### Learning Outcomes

There are five learning outcomes for this course.


```{code-cell} ipython3
:tags: [remove-input]

#[print(o + ' ('+ k +')') for o,k in zip(outcomes_df['outcome'], outcomes_df['keyword'])];
outcomes_df['outcome']
```

We will build your skill in the `process` and `communicate` outcomes over the whole semester. The middle three skills will correspond roughly to the content taught for each of the first three portfolio checks.  

### Schedule

````{margin}
```{note}
On the [BrightSpace calendar](https://brightspace.uri.edu/d2l/le/calendar/101136) page you can get a feed link to add to the calendar of your choice by clicking on the subscribe (star) button on the top right of the page. Class is for 1 hour there because of Brightspace/zoom integration limitations, but that calendar includes the zoom link.
```
````

The course will meet MWF 1-1:50pm on Zoom. Every class will include participatory live coding (instructor types, students follow along)) instruction and small exercises for you to progress toward level 1 achievements of the new skills introduced in class that day.

Programming assignments that will be due each week Sunday by 11:59pm.


```{code-cell} ipython3
:tags: [remove-input]


schedule_df.replace({None:'TBD'})
schedule_df[['topics','skills']]
```

(skill-rubric)=
### Skill Rubric


The skill rubric describes how your participation, assignments, and portfolios will be assessed to earn each achievement. The keyword for each skill is a short name that will be used to refer to skills throughout the course materials; the full description of the skill is in this table.

```{code-cell} ipython3
:tags: [remove-input]


rubric_df.replace({None:'TBD'},inplace=True)
rubric_df.rename(columns={'mastery':'Level 3',
              'compentent':'Level 2',
              'aware':'Level 1'}, inplace=True)

rubric_df[['skill','Level 1','Level 2','Level 3']]
```


```{code-cell} ipython3
:tags: [remove-input]


assignment_dummies  = pd.get_dummies(rubric_df['assignments'].apply(pd.Series).stack()).sum(level=0)
assignment_dummies['# Assignments'] = assignment_dummies.sum(axis=1)
col_rename = {float(i):'A' + str(i) for i in range(1,14)}
assignment_dummies.rename(columns =col_rename,inplace=True)

portfolio_dummies  = pd.get_dummies(rubric_df['portfolios'].apply(pd.Series).stack()).sum(level=0)
col_rename = {float(i):'P' + str(i) for i in range(1,5)}
portfolio_dummies.rename(columns =col_rename,inplace=True)


rubric_df = pd.concat([rubric_df,assignment_dummies, portfolio_dummies],axis=1)

assignment_cols =  ['A'+ str(i) for i in range(1,14)] + ['# Assignments']

portfolio_cols = [ 'Level 3'] + ['P' + str(i) for i in range(1,5)]
```

(assignment-skills)=
### Assignments and Skills

Using the keywords from the table above, this table shows which assignments you will be able to demonstrate which skills and the total number of assignments that assess each skill. This is the number of opportunities you have to earn Level 2 and still preserve 2 chances to earn Level 3 for each skill.

```{code-cell} ipython3
:tags: [remove-input]

rubric_df[assignment_cols]
```

### Portfolios and Skills

The objective of your portfolio submissions is to earn level 3 achievements. The following table shows what Level 3 looks like for each skill and identifies which portfolio submissions you can earn that Level 3 in that skill.


```{code-cell} ipython3
:tags: [remove-input]

rubric_df[portfolio_cols]
```
