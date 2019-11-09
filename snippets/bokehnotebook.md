---
permalink: /snippets/bokehnotebook/
title: ' '
---
## Put bokeh plot in Jupyter Notebook.

```python
from bokeh.plotting import figure, show
from bokeh.io import output_notebook
```

```python
p = figure()
show(p)
```