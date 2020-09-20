# Formatting Tips

Your portfolio is a [jupyter book](https://jupyterbook.org/intro.html). This means a few things:
- it uses [myst markdown](https://jupyterbook.org/reference/cheatsheet.html)
- it will run and compile Jupyter notebooks

This page will cover a few basic tips.

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

## File Naming

It is best practice to name files without spaces.


## Configurations

Things like the menus and links at the top are controlled as [settings](https://jupyterbook.org/customize/config.html), in `_config.yml`

## Links

Markdown syntax for links

```
[text to show](path/or/url)
```
