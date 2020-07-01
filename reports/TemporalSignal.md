Temporal signal from root-to-tip regression
================
Louis du Plessis
Last modified: 01 Jul 2020

-   [Summary](#summary)
-   [Root-to-tip regression](#root-to-tip-regression)
    -   [Dataset A (complete dataset)](#dataset-a-complete-dataset)
    -   [Dataset B](#dataset-b)
    -   [Dataset C](#dataset-c)
    -   [Dataset D](#dataset-d)
    -   [Dataset E](#dataset-e)
    -   [Dataset F](#dataset-f)
-   [Date shuffling analysis](#date-shuffling-analysis)
-   [Session info](#session-info)

Summary
=======

**Methodology** Test the temporal signal using regression between the root-to-tip genetic distance and the sampling date. For the root-to-tip genetic distance use midpoint-rooted ML trees built in RAxML. All trees were built using only variable sites, after removing all sites where more than 25% of genomes were unresolved, and correcting for ascertainment bias. The trees were midpoint rooted in FigTree and correlations and regression analyses were performed in R. Date shuffling analyses were performed to obtain the null distribution of the correlation coefficient on the ML trees.

**Results** The temporal signal is spuriously high when including Kampen, however, it is obviously an outlier because of the poor coverage. Including the excessively passaged Nichols genomes or the colonial Mexican syphilis genomes results in a poor temporal signal. Removing these genomes leads to a significant temporal signal, however it appears as if the yaws clade may be evolving at a slower rate than syphilis and bejel. Removing the bejel genome improves the temporal signal, but this improvement is probably artificial and stems from recentering the midpoint root such that the yaws and syphilis clades are equally distant from the root. Removing Fribourg-Blanc makes no noticeable difference.

Root-to-tip regression
======================

Dataset A (complete dataset)
----------------------------

| Name        | Accession      | Sampling location | Strain            | Sampling date |
|:------------|:---------------|:------------------|:------------------|:--------------|
| NIC2        | SRR3268713     | USA               | TPA (Nichols)     | 1912          |
| DAL-1       | NC\_016844.1   | USA               | TPA (Nichols)     | 1991          |
| Nichols     | NC\_021490.2   | USA               | TPA (Nichols)     | 1912          |
| BAL73       | SRR3268726     | USA               | TPA (Nichols)     | 1973          |
| Chicago     | NC\_017268.1   | USA               | TPA (Nichols)     | 1951          |
| BAL3        | SRR3268715     | USA               | TPA (Nichols)     | 1973          |
| SEA86       | SRR3268740     | USA               | TPA (Nichols)     | 1986          |
| NE20        | SRR3268710     | Netherlands       | TPA (Nichols)     | 2013          |
| SEA81-4     | 15169\_7\#74   | USA               | TPA (Nichols)     | 1981          |
| AU15        | SRR3268722     | Austria           | TPA (SS14)        | 2013          |
| NE14        | SRR3268703     | Netherlands       | TPA (SS14)        | 2013          |
| CZ33        | SRR3268690     | Czech Republic    | TPA (SS14)        | 2013          |
| NE17        | SRR3268707     | Netherlands       | TPA (SS14)        | 2013          |
| AR2         | SRR3268682     | Argentina         | TPA (SS14)        | 2013          |
| SW6         | SRR3268732     | Switzerland       | TPA (SS14)        | 2012          |
| P3          | SRR2996731     | China             | TPA (SS14)        | 2016          |
| PT\_SIF1002 | NZ\_CP016051.1 | Portugal          | TPA (SS14)        | 2011          |
| SS14        | NC\_021508.1   | USA               | TPA (SS14)        | 1977          |
| MexicoA     | NC\_018722.1   | Mexico            | TPA (SS14)        | 1953          |
| Fribourg    | NC\_021179.1   | Guinea            | TPP (Yaws)        | 1966          |
| IND1        | SRR3268698     | Indonesia         | TPP (Yaws)        | 1990          |
| Gauthier    | NC\_016843.1   | Ghana             | TPP (Yaws)        | 1960          |
| CDC2        | NC\_016848.1   | Ghana             | TPP (Yaws)        | 1980          |
| SamoaD      | NC\_016842.1   | Western Samoa     | TPP (Yaws)        | 1953          |
| GHA1        | Ghana-051      | Ghana             | TPP (Yaws)        | 1988          |
| BosniaA     | SRR3268694     | Bosnia            | TEN (Bejel)       | 1950          |
| 133         | PRJEB21276     | Mexico            | TPP (Yaws)        | 1600-1861     |
| 94A         | PRJEB21276     | Mexico            | TPA (Unknown)     | 1600-1861     |
| 94B         | PRJEB21276     | Mexico            | TPA (Unknown)     | 1600-1861     |
| PD28        | TU41           | Finland           | TPA (Unknown)     | 1666-1789     |
| SJ219       | TU579          | Estonia           | TPA (Unknown)     | 1429-1635     |
| CHS119      | TU590          | Finland           | TPP (Yaws)        | 1450-1630     |
| KM14-7      | TU391          | Netherlands       | Unknown (Unknown) | 1494-1631     |

![(A) Midpoint-rooted ML tree of **dataset A**. The sampling date or date range is given in parentheses after the sample name. Newly sequenced samples are highlighted. (B-D) Root-to-tip distance in the ML tree plotted against sampling date, respectively using the mean sampling date, lower limit of the date range and upper limit of the date range.](../results/temporal-signal/root-to-tip-A-1.png)

> **Figure 1:** (A) Midpoint-rooted ML tree of **dataset A**. The sampling date or date range is given in parentheses after the sample name. Newly sequenced samples are highlighted. (B-D) Root-to-tip distance in the ML tree plotted against sampling date, respectively using the mean sampling date, lower limit of the date range and upper limit of the date range.

Dataset B
---------

Remove genomes with insufficient coverage

![(A) Midpoint-rooted ML tree of **dataset B**. The sampling date or date range is given in parentheses after the sample name. Newly sequenced samples are highlighted. (B-D) Root-to-tip distance in the ML tree plotted against sampling date, respectively using the mean sampling date, lower limit of the date range and upper limit of the date range.](../results/temporal-signal/root-to-tip-B-1.png)

> **Figure 2:** (A) Midpoint-rooted ML tree of **dataset B**. The sampling date or date range is given in parentheses after the sample name. Newly sequenced samples are highlighted. (B-D) Root-to-tip distance in the ML tree plotted against sampling date, respectively using the mean sampling date, lower limit of the date range and upper limit of the date range.

Remove KM14-7

Dataset C
---------

Remove genomes that have been excessively passaged

![(A) Midpoint-rooted ML tree of **dataset C**. The sampling date or date range is given in parentheses after the sample name. Newly sequenced samples are highlighted. (B-D) Root-to-tip distance in the ML tree plotted against sampling date, respectively using the mean sampling date, lower limit of the date range and upper limit of the date range.](../results/temporal-signal/root-to-tip-C-1.png)

> **Figure 3:** (A) Midpoint-rooted ML tree of **dataset C**. The sampling date or date range is given in parentheses after the sample name. Newly sequenced samples are highlighted. (B-D) Root-to-tip distance in the ML tree plotted against sampling date, respectively using the mean sampling date, lower limit of the date range and upper limit of the date range.

Remove NIC2, Nichols, KM14-7

Dataset D
---------

Remove genomes with too many unique SNPs that may be damage/contamination artefacts

![(A) Midpoint-rooted ML tree of **dataset D**. The sampling date or date range is given in parentheses after the sample name. Newly sequenced samples are highlighted. (B-D) Root-to-tip distance in the ML tree plotted against sampling date, respectively using the mean sampling date, lower limit of the date range and upper limit of the date range.](../results/temporal-signal/root-to-tip-D-1.png)

> **Figure 4:** (A) Midpoint-rooted ML tree of **dataset D**. The sampling date or date range is given in parentheses after the sample name. Newly sequenced samples are highlighted. (B-D) Root-to-tip distance in the ML tree plotted against sampling date, respectively using the mean sampling date, lower limit of the date range and upper limit of the date range.

Remove NIC2, Nichols, 94A, 94B, KM14-7

Dataset E
---------

Remove bejel

![(A) Midpoint-rooted ML tree of **dataset E**. The sampling date or date range is given in parentheses after the sample name. Newly sequenced samples are highlighted. (B-D) Root-to-tip distance in the ML tree plotted against sampling date, respectively using the mean sampling date, lower limit of the date range and upper limit of the date range.](../results/temporal-signal/root-to-tip-E-1.png)

> **Figure 5:** (A) Midpoint-rooted ML tree of **dataset E**. The sampling date or date range is given in parentheses after the sample name. Newly sequenced samples are highlighted. (B-D) Root-to-tip distance in the ML tree plotted against sampling date, respectively using the mean sampling date, lower limit of the date range and upper limit of the date range.

Remove NIC2, Nichols, BosniaA, 94A, 94B, KM14-7

Dataset F
---------

Remove genome that may have been excessively passaged

![(A) Midpoint-rooted ML tree of **dataset F**. The sampling date or date range is given in parentheses after the sample name. Newly sequenced samples are highlighted. (B-D) Root-to-tip distance in the ML tree plotted against sampling date, respectively using the mean sampling date, lower limit of the date range and upper limit of the date range.](../results/temporal-signal/root-to-tip-F-1.png)

> **Figure 6:** (A) Midpoint-rooted ML tree of **dataset F**. The sampling date or date range is given in parentheses after the sample name. Newly sequenced samples are highlighted. (B-D) Root-to-tip distance in the ML tree plotted against sampling date, respectively using the mean sampling date, lower limit of the date range and upper limit of the date range.

Remove NIC2, Nichols, Fribourg, BosniaA, 94A, 94B, KM14-7

Date shuffling analysis
=======================

![Null distribution of the Pearson correlation coefficient between root-to-tip distance and sampling date (using mean sampling dates) for datasets A--F when shuffling dates across the whole phylogeny. The dashed lines indicate 2.5 and 97.5 quantiles of the distribution and the star indicates the correlation coefficient using the true (unshuffled) sampling dates. The p-value is the proportion of replicates with the test statistic (Pearson correlation coefficient) greater than or equal to the true value.](../results/temporal-signal/dateshuffling-1.png)

> **Figure 7:** Null distribution of the Pearson correlation coefficient between root-to-tip distance and sampling date (using mean sampling dates) for datasets A--F when shuffling dates across the whole phylogeny. The dashed lines indicate 2.5 and 97.5 quantiles of the distribution and the star indicates the correlation coefficient using the true (unshuffled) sampling dates. The p-value is the proportion of replicates with the test statistic (Pearson correlation coefficient) greater than or equal to the true value.

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
    ##  [1] treedater_0.5.0 limSolve_1.5.6  phangorn_2.5.5  phytools_0.6-99
    ##  [5] maps_3.3.0      ape_5.3         ggpubr_0.2.4    magrittr_1.5   
    ##  [9] beastio_0.2.5   ggsci_2.9       ggplot2_3.2.1   ggtree_2.1.1   
    ## [13] treeio_1.11.2   cowplot_1.0.0  
    ## 
    ## loaded via a namespace (and not attached):
    ##  [1] Rcpp_1.0.3              lattice_0.20-38         tidyr_1.0.0            
    ##  [4] gtools_3.8.1            assertthat_0.2.1        zeallot_0.1.0          
    ##  [7] digest_0.6.23           R6_2.4.1                backports_1.1.5        
    ## [10] evaluate_0.14           coda_0.19-3             highr_0.8              
    ## [13] pillar_1.4.2            rlang_0.4.2             lazyeval_0.2.2         
    ## [16] Matrix_1.2-18           combinat_0.0-8          rmarkdown_2.3          
    ## [19] labeling_0.3            stringr_1.4.0           igraph_1.2.4.2         
    ## [22] munsell_0.5.0           compiler_3.5.1          numDeriv_2016.8-1.1    
    ## [25] xfun_0.15               pkgconfig_2.0.3         mnormt_1.5-5           
    ## [28] htmltools_0.4.0         tidyselect_0.2.5        lpSolve_5.6.13.3       
    ## [31] tibble_2.1.3            expm_0.999-4            quadprog_1.5-8         
    ## [34] crayon_1.3.4            dplyr_0.8.3             withr_2.1.2            
    ## [37] MASS_7.3-51.4           grid_3.5.1              nlme_3.1-143           
    ## [40] jsonlite_1.6            gtable_0.3.0            lifecycle_0.1.0        
    ## [43] scales_1.1.0            tidytree_0.3.1          stringi_1.4.3          
    ## [46] farver_2.0.1            ggsignif_0.6.0          scatterplot3d_0.3-41   
    ## [49] rvcheck_0.1.7           vctrs_0.2.1             fastmatch_1.1-0        
    ## [52] tools_3.5.1             glue_1.3.1              purrr_0.3.3            
    ## [55] plotrix_3.7-7           parallel_3.5.1          yaml_2.2.0             
    ## [58] colorspace_1.4-1        BiocManager_1.30.10     animation_2.6          
    ## [61] clusterGeneration_1.3.4 knitr_1.29
