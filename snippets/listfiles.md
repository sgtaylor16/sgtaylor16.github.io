---
permalink: /snippets/listfiles/
title: ' '
---
## List Files in a Directory

```python
from os import listdir
from os.path import isfile,join
onlyfiles = [f for f in listdir(mypath) if isfile(join(mypath,f))]
```

[from stackoverflow](https://stackoverflow.com/questions/3207219/how-do-i-list-all-files-of-a-directory)