---
layout: page
title: Code Snippets
permalink: /snippets/
---
## Python

### Open (and close) a file with the _with_ statement.

```python
with open(filename,'r') as fh
    all_lines = fh.readlines
```

More [here](https://cmdlinetips.com/2016/01/opening-a-file-in-python-using-with-statement/)

### List comprehension with a conditional statement.

```python
[ expression for item in list if conditional ]
```

## Pandas



## Matplotlib

### Add text to a plot with relative position.

```python
ax.text(x,y,text,transform = ax.transAxes)
```

## Bokeh

### Put bokeh plot in Jupyter Notebook.

```python
from bokeh.plotting import figure, show
from bokeh.io import output_notebook
```

```python
p = figure()
show(p)
```

## Javascript

## D3

