---
permalink: /snippets/uniqued3/
title: ''
---

Often times when working in D3, I want to get a list of unique values from a column of data. There is no specific function for this, but the below works:

```
d3.map(object,d => d.column).keys()
```

[Source](https://stackoverflow.com/questions/28572015/how-to-select-unique-values-in-d3-js-from-data) from Stack-Overflow