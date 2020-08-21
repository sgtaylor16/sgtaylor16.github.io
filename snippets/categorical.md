---
permalink: /snippets/categorical/
title: ' '
---
## Create Catagorical data types in Pandas

* Create a categorical data type within a series.

```python
s = pd.Series(["a","b","c","a", dtype = "category")
```

* By converting an existing series or column to a category dtype.

```python
df = pd.DataFrame({"A":["a", "b", "c", "a"]})

df["B"] = df["A"].astype('category')
```

* Create a specific Categorical data type

```python
raw_cat = pd.Categorical(["a", "b", "c", "a"], categories =["b", "c", "d"], ordered=False)

s = pd.Series(raw_cat)
```

For more information go to:
[This pandas link](https://pandas.pydata.org/pandas-docs/stable/user_guide/categorical.html#:~:text=Categoricals%20are%20a%20pandas%20data%20type%20corresponding%20to,affiliation%2C%20observation%20time%20or%20rating%20via%20Likert%20scales.)