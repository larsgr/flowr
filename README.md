[![Build Status](https://travis-ci.org/sahilseth/flowr.png)](https://travis-ci.org/sahilseth/flowr)
[![DOI](https://zenodo.org/badge/11075/sahilseth/flowr.svg)](http://dx.doi.org/10.5281/zenodo.16170)

flow
======

R pacakge to design (and deploy) complex workflows, in a effective and efficient manner on High Perfomance computing clusters.

Please visit [docs.flowr.space](http://docs.flowr.space) for more information and here is a slide deck providing a quick overview: [sahilseth.github.io/slides/flowrintro](http://sahilseth.github.io/slides/flowrintro)

Here is a shiny app, [flow_creator](https://sseth.shinyapps.io/flow_creator/) for you to start building your flow.
[`guest; guestpass`]

Here are some useful questions:
https://github.com/sahilseth/flowr/issues?q=label%3Aquestion


```
## From the official R repository (may be a few version behind)
install.packages('flowr')
## for a latest and greatest
install.packages('devtools')
devtools::install_github("sahilseth/flowr")
```

## Example:
```
library(flowr)
example(plot_flow)
```

As of now we have tested this on the following clusters:

|Platform|submission commnd|Works?|label*|
|:---|:---:|:---:|:---:|
|LSF 9.1|bsub|Yes|lsf
|Torque|qsub|Yes|torque
|SGE|qsub|should work|sge
|LSF HPC 7|bsub|should work|lsf

*label: This serves as the type argument for [queue](http://docs.flowr.space/en/latest/rd/topics/queue.html) function.

### Aknowledgements:
- Jianhua Zhang
- Samir Amin
- Kadir Akdemir
- Ethan Mao
- Henry Song
- An excellent resource for writing your own R packages: r-pkgs.had.co.nz
