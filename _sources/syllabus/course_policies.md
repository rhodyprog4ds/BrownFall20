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

## Grading

This course will be graded on a basis of a set of *skills* (described in detail the next section of the syllabus). This is in contrast to more common grading on a basis of points earned through assignments. This section of the syllabus describes the principles and mechanics of the grading for the course.

+++

### Principles of Grading

Learning happens through practice and feedback. My goal as a teacher is for you to learn. The grading in this course is based on your learning of the material, rather than your completion of the activities that are assigned.

Earning a C in this class is intended to be easier than typical grading. I expect everyone to get at least a C.
Earning a B in this class is intended to be very accessible, you can make a lot of mistakes along the way as you learn, but if you learn by the end.
Earning an A in this class will be challenging, but is possible even with making mistakes while you learn.


This course is designed to encourage you to work steadily at learning the material and demonstrating your new knowledge. There are no single points of failure, where you lose points that cannot be recovered. Also, you cannot cram anything one time and then forget it. The material will build and you have to demonstrate that you retained things

Grading this way also is more ammenable to the fact that there are correct and incorrect ways to do things, but there is not always a single correct answer to a realistic data science problem. Your work will be assessed on whether or not it demonstrates your learning of the targeted skills. You will also receive feedback on how to improve.

+++

### How it works

There are 15 skills that you will be graded on in this course.
While learning these skills, you will work through a progression of learning.
Your grade will be based on earning 45 achievements that are organized into 15 skill groups with 3 levels for each.
That is,
If you achieve level 1 in all of the skills, you will earn at least a C in the course. To earn level 1 achievements, you will need to demonstrate basic awareness of the required concepts and know approximately what to do, but you may need specific instructions of which things to do or to look up examples to modify every step of the way. You can earn level 1 achievements in class, assignments, or portfolio submissions.
To earn a B, you must earn all of the level 1 and level 2 achievements. To earn level 2 achievements you will need to demonstrate understanding of the concepts and the ability to apply them with minimal instruction after earning the level 1 achievement for that skill. You can earn level 2 achievements in assignments or portfolio submissions.
To get an A, you must earn all of the achievements. To do that you will be required to consistently execute each skill and demonstrate deep understanding of the course material, after achieving level 2 in that skill. You can earn level 3 achievements only through your portfolio submissions.



You will have at least three opportunities to earn every level 2 achievement.
You will have at least two opportunities to earn every level 3 achievement.

You will have three *types* of opportunities to demonstrate your current skill level.

#### Participation

While attending synchronous class sessions, there will be understanding checks and in class exercises.
Completing in class exercises and correctly answering questions in class can earn level 1 achievements.
In class questions will be administered through the classroom chat platform Prismia.chat; these records will be used to update your skill progression.

#### Assignments

For your learning to progress and earn level 2 achievements, you must practice with the skills outside of class time.

Assignments will each evaluate certain skills. After your assignment is reviewed, you will get qualitative feedback on your work, and an assessment of your demonstration of the targeted skills.

#### Portfolio Checks

To earn level 3 achievements, you will build a portfolio consisting of reflections, challenge problems, and longer analyses over the course of the semester.
You will submit your portfolio for review 4 times.
The first two will cover the skills taught up until 1 week before the submission deadline.
<!-- The first portfolio check will cover skills FIXME.
The second portfolio check will cover skills FIXME. -->
The third and fourth portfolio checks will cover all of the skills.
The fourth will be due during finals. This means that, if you have achieved mastery of all of the skills by the 3rd portfolio check, you do not need to submit the fourth one.

Portfolio prompts will be given throughout the class, some will be strucutred questions, others may be questions that arise in class, for which there is not time to answer.

#### TLDR

You *could* earn a C through in class participation alone, if you make nearly zero mistakes. To earn a B, you must complete assignments and participate in class. To earn an A you must participate, complete assignments, and build a portfolio.

+++

### Detailed mechanics

On Brightspace there are 45 Grade items that you will get a 0 or a 1 grade for. These will be revealed, so that you can view them as you have an opportunity to demonstrate each one.
The table below shows the minimum number of skills at each level to earn each letter grade.  

```{code-cell} ipython3
:tags: [remove-input]

import pandas as pd
import numpy as np
N = 15
Nmaj = 10
Nmin = 5

grades = np.asarray(['A', 'A-','B+', 'B','B-', 'C+', 'C', 'C-', 'D+', 'D' ])
skill_levels_cum = [[N, N,N],[Nmaj,N,N], [Nmin,N, N],
                [0,N, N],[0,Nmaj,N], [ 0,Nmin,N]
               , [0, 0,N],[0,0,Nmaj], [ 0, 0,Nmin],
               [0,0,3]]

grade_df = pd.DataFrame(data = skill_levels_cum,
                        columns = ['Level 3','Level 2', 'Level 1'] )


grade_df['letter grade'] = grades
grade_df.set_index('letter grade')
```

For example, if you achieve level 2 on all of the skills and level 3 on 7 skills, that will be a B+.
````{margin}
```{note}
In this example, you will have also achieved level 1 on all of the skills, because it is a prerequisite to level 2.
```
````

If you achieve level 3 on 14 of the skills, but only level 1 on one of the skills, that will be a B-, because the minimum number of level 2 achievements for a B is 15.


+++

### Late work

No late work will be graded.
Every skill will be assessed through more than one assignment, so missing assignments occasionally *may* not hurt your grade. If you do not submit any assignments that cover a given skill, you may earn the level 2 achievement in that skill through a portfolio check, but you will not be able to earn the level 3 achievement in that skill.

````{margin}
```{note}
You may visit office hours to discuss assignments that you did not complete on time to get feedback and check your own understanding, but they will not count toward skill demonstration.
```
````
