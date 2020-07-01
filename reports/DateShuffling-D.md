BEAST2 Bayesian DRT (Dataset D)
================
Louis du Plessis
Last modified: 01 Jul 2020

-   [Summary](#summary)
    -   [Dataset](#dataset)
    -   [Models](#models)
    -   [Analyses](#analyses)
-   [Constant population size](#constant-population-size)
-   [Exponential growth](#exponential-growth)
-   [Bayesian Skyline Plot](#bayesian-skyline-plot)
-   [Session info](#session-info)

Summary
=======

Dataset
-------

-   Dataset D. That is, the complete dataset with Kampen, Nichols, NIC-2, 94A and 94B removed.
-   Sampling dates of ancient samples were fixed to the middle of the radiocarbon date range.

> **Table 1:** Dates used in date shuffling analyses (before shuffling).

| Name        | Accession      | Sampling location | Strain        |  Sampling date|
|:------------|:---------------|:------------------|:--------------|--------------:|
| NIC2        | SRR3268713     | USA               | TPA (Nichols) |         1912.0|
| DAL-1       | NC\_016844.1   | USA               | TPA (Nichols) |         1991.0|
| Nichols     | NC\_021490.2   | USA               | TPA (Nichols) |         1912.0|
| BAL73       | SRR3268726     | USA               | TPA (Nichols) |         1973.0|
| Chicago     | NC\_017268.1   | USA               | TPA (Nichols) |         1951.0|
| BAL3        | SRR3268715     | USA               | TPA (Nichols) |         1973.0|
| SEA86       | SRR3268740     | USA               | TPA (Nichols) |         1986.0|
| NE20        | SRR3268710     | Netherlands       | TPA (Nichols) |         2013.0|
| SEA81-4     | 15169\_7\#74   | USA               | TPA (Nichols) |         1981.0|
| AU15        | SRR3268722     | Austria           | TPA (SS14)    |         2013.0|
| NE14        | SRR3268703     | Netherlands       | TPA (SS14)    |         2013.0|
| CZ33        | SRR3268690     | Czech Republic    | TPA (SS14)    |         2013.0|
| NE17        | SRR3268707     | Netherlands       | TPA (SS14)    |         2013.0|
| AR2         | SRR3268682     | Argentina         | TPA (SS14)    |         2013.0|
| SW6         | SRR3268732     | Switzerland       | TPA (SS14)    |         2012.0|
| P3          | SRR2996731     | China             | TPA (SS14)    |         2016.0|
| PT\_SIF1002 | NZ\_CP016051.1 | Portugal          | TPA (SS14)    |         2011.0|
| SS14        | NC\_021508.1   | USA               | TPA (SS14)    |         1977.0|
| MexicoA     | NC\_018722.1   | Mexico            | TPA (SS14)    |         1953.0|
| Fribourg    | NC\_021179.1   | Guinea            | TPP (Yaws)    |         1966.0|
| IND1        | SRR3268698     | Indonesia         | TPP (Yaws)    |         1990.0|
| Gauthier    | NC\_016843.1   | Ghana             | TPP (Yaws)    |         1960.0|
| CDC2        | NC\_016848.1   | Ghana             | TPP (Yaws)    |         1980.0|
| SamoaD      | NC\_016842.1   | Western Samoa     | TPP (Yaws)    |         1953.0|
| GHA1        | Ghana-051      | Ghana             | TPP (Yaws)    |         1988.0|
| BosniaA     | SRR3268694     | Bosnia            | TEN (Bejel)   |         1950.0|
| 133         | PRJEB21276     | Mexico            | TPP (Yaws)    |         1730.5|
| 94A         | PRJEB21276     | Mexico            | TPA (Unknown) |         1730.5|
| 94B         | PRJEB21276     | Mexico            | TPA (Unknown) |         1730.5|
| PD28        | TU41           | Finland           | TPA (Unknown) |         1727.5|
| SJ219       | TU579          | Estonia           | TPA (Unknown) |         1534.5|
| CHS119      | TU590          | Finland           | TPP (Yaws)    |         1540.0|
| KM14-7      | TU391          | Netherlands       | NA (Unknown)  |         1562.5|

Models
------

### Site model

Use an HKY model with *Γ*-distributed rate heterogeneity and default priors. Nucleotide frequencies were also inferred from the data \[Hasegawa et al. JME (1985) and Yang, JME (1994)\].

### Clock models

Analyses were performed under a strict clock or an uncorrelated lognormally distributed relaxed clock model. In both cases an exponentially distributed prior with mean 5 × 10<sup>−7</sup> s/s/y was placed on the (mean) clock rate \[Drummond et al. PLoS Biology (2006)\]

### Tree priors

Three different tree priors were used:

-   Constant population size coalescent
-   Exponential growth coalescent
-   Bayesian skyline plot with 10 groups \[Drummond et al. MBE (2005)\]

In all cases default priors were used.

Analyses
--------

All analyses were performed in BEAST v2.6.0 \[Bouckaert et al. PLoS Comp Biol (2019)\]. MCMC chains were run for 50 million steps and parameters and trees sampled every 5,000 steps. 30% of samples were discarded as burn-in.

Constant population size
========================

![Date shuffling analyses performed under a **constant size** coalescent tree prior and **relaxed clock** (A) and **strict clock** (B) models. The plot shows the posterior distributions for the (mean) clock rate, truncated at the upper and lower limits of the 95% HPD interval. Horizontal red lines indicate the medians of the posterior distributions. The red dashed lines indicate the median and upper and lower limits of the 95% HPD interval of the clock rate inferred under the true sampling dates.](../results/beast/shuffleddates/figures/shuffleddates-Const-D-1.png)

> **Figure 1:** Date shuffling analyses performed under a **constant size** coalescent tree prior and **relaxed clock** (A) and **strict clock** (B) models. The plot shows the posterior distributions for the (mean) clock rate, truncated at the upper and lower limits of the 95% HPD interval. Horizontal red lines indicate the medians of the posterior distributions. The red dashed lines indicate the median and upper and lower limits of the 95% HPD interval of the clock rate inferred under the true sampling dates.

Exponential growth
==================

![Date shuffling analyses performed under an **exponential growth** coalescent tree prior and **relaxed clock** (A) and **strict clock** (B) models. The plot shows the posterior distributions for the (mean) clock rate, truncated at the upper and lower limits of the 95% HPD interval. Horizontal red lines indicate the medians of the posterior distributions. The red dashed lines indicate the median and upper and lower limits of the 95% HPD interval of the clock rate inferred under the true sampling dates.](../results/beast/shuffleddates/figures/shuffleddates-Exp-D-1.png)

> **Figure 2:** Date shuffling analyses performed under an **exponential growth** coalescent tree prior and **relaxed clock** (A) and **strict clock** (B) models. The plot shows the posterior distributions for the (mean) clock rate, truncated at the upper and lower limits of the 95% HPD interval. Horizontal red lines indicate the medians of the posterior distributions. The red dashed lines indicate the median and upper and lower limits of the 95% HPD interval of the clock rate inferred under the true sampling dates.

Bayesian Skyline Plot
=====================

![Date shuffling analyses performed under a **Bayesian skyline plot** coalescent tree prior and **relaxed clock** (A) and **strict clock** (B) models. The plot shows the posterior distributions for the (mean) clock rate, truncated at the upper and lower limits of the 95% HPD interval. Horizontal red lines indicate the medians of the posterior distributions. The red dashed lines indicate the median and upper and lower limits of the 95% HPD interval of the clock rate inferred under the true sampling dates.](../results/beast/shuffleddates/figures/shuffleddates-BSP10-D-1.png)

> **Figure 3:** Date shuffling analyses performed under a **Bayesian skyline plot** coalescent tree prior and **relaxed clock** (A) and **strict clock** (B) models. The plot shows the posterior distributions for the (mean) clock rate, truncated at the upper and lower limits of the 95% HPD interval. Horizontal red lines indicate the medians of the posterior distributions. The red dashed lines indicate the median and upper and lower limits of the 95% HPD interval of the clock rate inferred under the true sampling dates.

Session info
============

    ## R version 3.5.1 (2018-07-02)
    ## Platform: x86_64-apple-darwin15.6.0 (64-bit)
    ## Running under: macOS Sierra 10.12.6
    ## 
    ## Matrix products: default
    ## BLAS: /Library/Frameworks/R.framework/Versions/3.5/Resources/lib/libRblas.0.dylib
    ## LAPACK: /Library/Frameworks/R.framework/Versions/3.5/Resources/lib/libRlapack.dylib
    ## 
    ## locale:
    ## [1] en_GB.UTF-8/en_GB.UTF-8/en_GB.UTF-8/C/en_GB.UTF-8/en_GB.UTF-8
    ## 
    ## attached base packages:
    ## [1] stats     graphics  grDevices utils     datasets  methods   base     
    ## 
    ## other attached packages:
    ## [1] ggtree_2.1.1  ggsci_2.9     ggplot2_3.2.1 beastio_0.2.5 coda_0.19-3  
    ## [6] cowplot_1.0.0
    ## 
    ## loaded via a namespace (and not attached):
    ##  [1] Rcpp_1.0.3          highr_0.8           BiocManager_1.30.10
    ##  [4] pillar_1.4.2        compiler_3.5.1      RColorBrewer_1.1-2 
    ##  [7] tools_3.5.1         zeallot_0.1.0       digest_0.6.23      
    ## [10] jsonlite_1.6        tidytree_0.3.1      nlme_3.1-143       
    ## [13] evaluate_0.14       lifecycle_0.1.0     tibble_2.1.3       
    ## [16] gtable_0.3.0        lattice_0.20-38     pkgconfig_2.0.3    
    ## [19] rlang_0.4.2         rvcheck_0.1.7       parallel_3.5.1     
    ## [22] yaml_2.2.0          xfun_0.15           treeio_1.11.2      
    ## [25] withr_2.1.2         stringr_1.4.0       dplyr_0.8.3        
    ## [28] knitr_1.29          vctrs_0.2.1         grid_3.5.1         
    ## [31] tidyselect_0.2.5    glue_1.3.1          R6_2.4.1           
    ## [34] rmarkdown_2.3       tidyr_1.0.0         purrr_0.3.3        
    ## [37] magrittr_1.5        backports_1.1.5     scales_1.1.0       
    ## [40] htmltools_0.4.0     assertthat_0.2.1    ape_5.3            
    ## [43] colorspace_1.4-1    stringi_1.4.3       lazyeval_0.2.2     
    ## [46] munsell_0.5.0       crayon_1.3.4
