# GxAge evaluation

This ecf script allows to evaluate genome-wide GxAge summary stats using the R package Easy2 (accesible at www.genepi-regenburg.de/easy2)

## Features
Workflow: 
1) Removes MAF<0.1% and imputation quality<0.8 variants
2) Extracts P values from log P values
3) Removes MHC region
4) Performs GC correction using lambdas obtained from non-marginally associated regions
5) Performs genome-wide and 2-step GxAge screen (using PCA to derive number of independent tests of marginally associated variants)
6) Clumps significant variants using distance<500kb and r2>0.1
7) Creates GxAge QQ and manhattan plot

## Prerequisites

Install R package Easy2 from www.genepi-regenburg.de/easy2 : install.packages("Easy2_version.tar.gz")

## Usage in R

library(Easy2)

Easy2("easy2_gxage.ecf")

