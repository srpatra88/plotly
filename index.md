---
title: "R Markdown Presentation & Plotly"
author: "Soumya Patra, 07 march 2017"
output:
  ioslides_presentation: default
  beamer_presentation: default
---
## Summary

- Showing a basic plot using plotly
- Presenting in the form of a web presentation
- Plot Diamond carets vs price colour-coded on different values for carets

## Interactive Plotly plot

```{r echo=FALSE, message=FALSE}
library(plotly)
set.seed(100)
d <- diamonds[sample(nrow(diamonds), 1000), ]
plot_ly(d, x = ~carat, y = ~price, color = ~carat,
        size = ~carat, text = ~paste("Clarity: ", clarity))
```
