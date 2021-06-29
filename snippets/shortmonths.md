To shorten the months on a d3 axis use the following method chained to the axis method.

```JavaScript
var xAxis = d3.axisBottom(xScale)
  .tickFormat(d3.timeFormat("%b"));
  ```
from [this](https://stackoverflow.com/questions/40173533/customize-the-d3-month-or-year-tick-format) StackOverflow post