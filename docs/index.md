--- 
title: "使用 BookDown 制作在线电子书"
author: "杨志宏"
date: "2019-12-09"
output: pdf_document
bibliography:
- book.bib
- packages.bib
description: 介绍Bookdown的使用，记录遇到的问题及解决办法。
documentclass: ctexbook
geometry:
- a4paper
- tmargin=2.5cm
- bmargin=2.5cm
- lmargin=3.5cm
- rmargin=2.5cm
github-repo: yangjh-xbmu/bookdown
link-citations: yes
lof: yes
lot: yes
colorlinks: yes
site: bookdown::bookdown_site
biblio-style: "GBT7714-2005"
---



# 前言 {-}

在这本小书中，我将介绍 bookdown 的用法，并记录在使用过程中遇到的各种问题和解决方案，尽量节约后来的同好上手的时间。

以下是我的 R 进程信息：


```r
sessionInfo()
```

```
## R version 3.6.1 (2019-07-05)
## Platform: x86_64-apple-darwin15.6.0 (64-bit)
## Running under: macOS Catalina 10.15.1
## 
## Matrix products: default
## BLAS:   /Library/Frameworks/R.framework/Versions/3.6/Resources/lib/libRblas.0.dylib
## LAPACK: /Library/Frameworks/R.framework/Versions/3.6/Resources/lib/libRlapack.dylib
## 
## locale:
## [1] en_US.UTF-8/en_US.UTF-8/en_US.UTF-8/C/en_US.UTF-8/en_US.UTF-8
## 
## attached base packages:
## [1] stats     graphics  grDevices utils     datasets 
## [6] methods   base     
## 
## loaded via a namespace (and not attached):
##  [1] compiler_3.6.1  magrittr_1.5    bookdown_0.16  
##  [4] tools_3.6.1     htmltools_0.4.0 yaml_2.2.0     
##  [7] Rcpp_1.0.3      stringi_1.4.3   rmarkdown_1.18 
## [10] knitr_1.26      stringr_1.4.0   xfun_0.11      
## [13] digest_0.6.23   rlang_0.4.2     evaluate_0.14
```


\BeginKnitrBlock{flushright}<p class="flushright">杨志宏  
于 世界之最温暖处</p>\EndKnitrBlock{flushright}

