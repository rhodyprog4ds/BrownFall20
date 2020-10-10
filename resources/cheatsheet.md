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

# Cheatsheet

Patterns and examples of how to use common tips in class

## Axes

```{code-cell} ipython3
:tags:['remove-input']
import pandas as pd
```

First build a small dataset that's just enough to display

```{code-cell} ipython3
data = [[1,0],[5,4],[1,4]]
df = pd.DataFrame(data = data,
  columns = ['A','B'])
```

``````{list-table}
:header-rows: 1
:widths: 25 25

* - data = [[1,0],[5,4],[1,4]]
    df = pd.DataFrame(data = data,
                      columns = ['A','B'])
  - ```{code-cell} ipython3
    df
    ```

* - ```{code-cell} ipython3
    df.sum(axis=0)
    ```
  - ```{code-cell} ipython3
    df.sum(axis=1)
    ```

* - ```{code-cell} ipython3
    df.apply(sum,axis=0)
    ```
  - ```{code-cell} ipython3
    df.apply(sum,axis=1)
    ```

* - ```{code-cell} ipython3
    df['A'][1]
    ```

 - ```{code-cell} ipython3
    df.iloc[0][1]
    ```
``````
