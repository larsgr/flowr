---
title: "flowr building a pipeline"
date: "2015-05-19"
output: rmarkdown::html_vignette
vignette: >
  %\VignetteIndexEntry{flowr simple example}
  %\VignetteEngine{knitr::rmarkdown}
  \usepackage[utf8]{inputenc}
---

## Building pipelines



### A working example


```r
## 6 jobs with 10 each
cmds = sprintf("sleep %s", round(rchisq(6*10, df = 1), 1))
nms = sprintf("myjob%s", rep(1:6, each = 10))
mat = data.frame(cbind(jobname = nms, cmd = cmds), stringsAsFactors = FALSE)
head(mat)
```

```
#>   jobname       cmd
#> 1  myjob1 sleep 1.5
#> 2  myjob1 sleep 1.2
#> 3  myjob1 sleep 2.6
#> 4  myjob1 sleep 1.9
#> 5  myjob1 sleep 3.8
#> 6  myjob1 sleep 0.3
```
