# IOHdata

This repository contains several data sets of 12 reference algorithms tested on the 23 Pseudo-Boolean Optimization (PBO) problems. PBO is ones of the benchmark suite compiled under the framework of __IOHexperimenter__. The 12 reference algorithms are:

* (1+(λ,λ)) GA
* (1+1) EA_>0
* (1+1) fGA
* (1+10) EA_>0
* (1+10) EA_logNormal
* (1+10) EA_normalized
* (1+10) EA_var_ctrl
* (1+10) EA_{r/2,2r}
* (30,30) vGA
* RLS
* EDA (previously called UMDA)
* gHC

The detailed description of those algorithms can be found [here](https://github.com/IOHprofiler/IOHalgorithm).

When performing independent runs of those algorithms, one could decide whether to use exactly the same problem instance from all the runs, or to use different problem instances for every run. Hence, two data sets are produced:

* `2019gecco-ins1-11run.rds`: one one problem instance (`ins1`) is used for all 11 repetitions, and
* `2019gecco-ins11-1run.rds`: 11 problems instances are created and each algorithm is executed only once (`1run`) on each instance.

The prefix `2019gecco-` says these data sets are used for the following GECCO '19 papers published by the authors (and collaborators):

* Carola Doerr, Furong Ye, Naama Horesh, Hao Wang, Ofer M. Shir, and Thomas Bäck. _Benchmarking Discrete Optimization Heuristics with IOHprofiler_. GECCO ‘19
* Borja Calvo, Ofer M. Shir, Josu Ceberio, Carola Doerr, Hao Wang, Thomas Bäck, and Jose A. Lozano. _Bayesian Performance Analysis for Black-Box Optimization Benchmarking_. GECCO ‘19

For the complete and up-to-date list of papers that use IOHprofiler, please look [here](https://iohprofiler.github.io/citation).

Data sets are stored as the `.rds` files (one of the compressed data type in `R`). Internally, the data are organized in a `S3` structure `DataSetList` which is implemented in __IOHnanalyzer__. To load the data set into you `R` session, please use the following commands:

```R
library(IOHanalyzer)
dsl <- readRDS('path/to/the/downloaded/rds/file')
dsl
```
