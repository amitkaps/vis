---
title: Notes - Stacked Color
layout: visdown
permalink: notes-stacked-color
---

<section id="output"></section>

<textarea id="input" oninput="visdown()">

```vis
data:
  url: data/notes.csv
  format:
    type: csv

mark: area

encoding:
  x:
    timeUnit: year
    field: year
    type: temporal
    axis:
      format: %Y
      labelAngle: 0
      title: Year
      titleFontSize: 12
  y:
    field: money
    type: quantitative
    aggregate: sum
    axis:
      format: %
      title: Share of Notes (by Value)
      titleFontSize: 12

  color:
    field: denom
    type: nominal
    scale:
      range: ["#9087A8", "#BEA58A", "#819C74", "#AE8B80", "#E58275", "#958087", "#979B9B", "#AEA98E", "#EB8D8C"]

config:
  cell:
    width: 650
    height: 450
  mark:
    stacked: normalize
```


</textarea>
