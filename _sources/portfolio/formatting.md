# Formatting Tips

Your portfolio is a [jupyter book](https://jupyterbook.org/intro.html). This means a few things:
- it uses [myst markdown](https://jupyterbook.org/reference/cheatsheet.html)
- it will run and compile Jupyter notebooks

This page will cover a few basic tips.

## Organization

The summary of for the `part` or whole submission, should match the skills to the chapters.  Which prompt you're addressing is not important, the  prompts are a *starting point* not the end goal of your portfolio.


## Structure of plain markdown

Use a heading like this:

```
# Heading of page
```

in the file and it will appear in the sidebar.


## File Naming

It is best practice to name files without spaces.
Each `chapter` or file should have a descriptive file name (`with_no_spaces`) and descriptive title for it.


## Syncing markdown and ipynb files

To sync feedback received to your runnable notebook files, change the related GitHub Actions file: `.github/workflows/`
In the step named convert that looks like:
```
- name: convert
  run: |
      jupytext */*.ipynb --to myst
```

change it to:

```
- name: convert
  run: |
      jupytext --set-formats ipynb,md */*.ipynb  # Turn .ipynb into a paired ipynb/py notebook
      jupytext --sync */*.ipynb                  # Update whichever of .ipynb/notebook.md is outdated
```

This means if you accept suggestion commits from the the `.md` file, the action will upate your `.ipynb` file. If you update your `.ipynb file` the action will update the .md file.


## Adding annotations with formatting or margin notes

You can either install [jupytext](https://jupytext.readthedocs.io/en/latest/install.html) and convert locally or upload /push a notebook to your repository and let GitHub convert.  
Then edit the .md file with a [text editor](texteditor) of your choice. You can run by uploading if you don't have jupytext installed, or locally if you have installed jupytext or jupyterbook.

In your .md file use backticks to mark [special content blocks](https://jupyterbook.org/content/content-blocks.html)


````md
```{note}
Here is a note!
```
````

````md
```{warning}
Here is a warning!
```
````

````md
```{tip}
Here is a tip!
```
````


````md
```{margin}
Here is a margin note!
```
````


For a complete list of options, see [the `sphinx-book-theme` documentation](https://sphinx-book-theme.readthedocs.io/en/latest/reference/demo.html#admonitions).

## Links

Markdown syntax for links

```
[text to show](path/or/url)
```



## Configurations

Things like the menus and links at the top are controlled as [settings](https://jupyterbook.org/customize/config.html), in `_config.yml`. The following are some things that you might change in your configuration file.

(keeperrors)=
### Show errors and continue

To show errors and continue running the rest, add the following to your configuration file:

```
# Execution settings
execute:
  allow_errors              : true
```
