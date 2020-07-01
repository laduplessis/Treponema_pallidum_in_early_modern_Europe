BEAST2 molecular clock dating (Dataset D)
================
Louis du Plessis
Last modified: 01 Jul 2020

-   [Summary](#summary)
    -   [Dataset](#dataset)
    -   [Models](#models)
    -   [Analyses](#analyses)
    -   [Figures and tables](#figures-and-tables)
-   [Clade TMRCA and sampling date estimates](#clade-tmrca-and-sampling-date-estimates)
    -   [Constant population size](#constant-population-size)
    -   [Exponential growth](#exponential-growth)
    -   [Bayesian Skyline Plot](#bayesian-skyline-plot)
-   [Posterior distributions compared between models](#posterior-distributions-compared-between-models)
-   [MCC trees](#mcc-trees)
-   [Session info](#session-info)

Summary
=======

Dataset
-------

Dataset D. That is, the complete dataset with Kampen, Nichols, NIC-2, 94A and 94B removed.

Models
------

### Site model

Use an HKY model with *Γ*-distributed rate heterogeneity and default priors. Nucleotide frequencies were also inferred from the data \[Hasegawa et al. JME (1985) and Yang, JME (1994)\].

### Clock models

Analyses were performed under a strict clock or an uncorrelated lognormally distributed relaxed clock model. In both cases an exponentially distributed prior with mean 5 × 10<sup>−7</sup> s/s/y was placed on the (mean) clock rate \[Drummond et al. PLoS Biology (2006)\].

### Tree priors

Three different tree priors were used:

-   Constant population size coalescent
-   Exponential growth coalescent
-   Bayesian skyline plot with 10 groups \[Drummond et al. MBE (2005)\]

In all cases default priors were used.

### Tip date priors

> **Table 1:** Radiocarbon date ranges used.

|     | Name   | Accession  | Sampling location | Strain            | Sampling date |
|:----|:-------|:-----------|:------------------|:------------------|:--------------|
| 27  | 133    | PRJEB21276 | Mexico            | TPE (Yaws)        | 1600-1861     |
| 28  | 94A    | PRJEB21276 | Mexico            | TPA (Unknown)     | 1600-1861     |
| 29  | 94B    | PRJEB21276 | Mexico            | TPA (Unknown)     | 1600-1861     |
| 30  | PD28   | TU41       | Finland           | TPA (Unknown)     | 1666-1789     |
| 31  | SJ219  | TU579      | Estonia           | TPA (Unknown)     | 1429-1635     |
| 32  | CHS119 | TU590      | Finland           | TPE (Yaws)        | 1450-1630     |
| 33  | KM14-7 | TU391      | Netherlands       | Unknown (Unknown) | 1494-1631     |

Two types of priors were placed on the sampling dates of ancient sequences:

-   **Narrow uniform:** Uniform prior between the limits inferred from radiocarbon dating
-   **Wide uniform:** Uniform prior between 1000 and 2016 on all sampling dates (not informed by radiocarbon dating).

Analyses
--------

All analyses were performed in BEAST v2.6.0 \[Bouckaert et al. PLoS Comp Biol (2019)\]. MCMC chains were run for 50 million steps and parameters and trees sampled every 5,000 steps. 30% of samples were discarded as burn-in. Convergence was assessed in Tracer \[Rambaut et al. Sys. Biol. (2018)\]. Treeannotator was used to compute MCC trees of the resulting posterior tree distributions.

Figures and tables
------------------

-   Fig. 1-6 show the posterior estimates for the sampling dates of ancient sequences and TMRCAs of clades in the tree under different combinations of clock model, tree prior and tip date priors. In all figures the shaded regions indicate the date limits inferred from radiocarbon dating (narrow uniform prior distributions).
    -   Fig. 1-2: constant population size
    -   Fig. 3-4: Exponential growth
    -   Fig 5-6: Bayesian skyline plot).
-   Table 2 and 3 summarise the HPD estimates in Fig. 1-6, with the addition of the posterior probability that a sample dates from pre-Columbian times (sampling date &lt; 1493) and that a clade is monophyletic.
-   Fig. 7-9 show the posterior TMRCA of Treponema pallidum and TPE/TEN as well as substitution rate estimates under different combinations of clock model, tree prior and tip date priors.
-   Fig. 10-12 show the posterior sampling date estimates for the three new sequences under different combinations of clock model, tree prior and tip date priors.
-   Fig. 13-14 show the MCC trees inferred under a relaxed clock model, Bayesian skyline tree prior and different tip date priors. MCC trees for all other models are available, but not shown (the differences are minor).

Clade TMRCA and sampling date estimates
=======================================

Constant population size
------------------------

![Posterior distributions for the sampling dates of ancient samples (left) and the TMRCAs of clades (right) inferred under a relaxed (orange) and strict (blue) clock model. The distributions are truncated at the upper and lower limits of the 95% HPD interval and the red lines indicate the median estimates. All analyses used a **constant population** size coalescent tree prior and **narrow uniform** priors on sampling dates.](../results/beast/D/figures/Const.narrow-1.png)

> **Figure 1:** Posterior distributions for the sampling dates of ancient samples (left) and the TMRCAs of clades (right) inferred under a relaxed (orange) and strict (blue) clock model. The distributions are truncated at the upper and lower limits of the 95% HPD interval and the red lines indicate the median estimates. All analyses used a **constant population** size coalescent tree prior and **narrow uniform** priors on sampling dates.

![Posterior distributions for the sampling dates of ancient samples (left) and the TMRCAs of clades (right) inferred under a relaxed (orange) and strict (blue) clock model. The distributions are truncated at the upper and lower limits of the 95% HPD interval and the red lines indicate the median estimates. All analyses used a **constant population** size coalescent tree prior and **wide uniform** priors on sampling dates.](../results/beast/D/figures/Const.wide-1.png)

> **Figure 2:** Posterior distributions for the sampling dates of ancient samples (left) and the TMRCAs of clades (right) inferred under a relaxed (orange) and strict (blue) clock model. The distributions are truncated at the upper and lower limits of the 95% HPD interval and the red lines indicate the median estimates. All analyses used a **constant population** size coalescent tree prior and **wide uniform** priors on sampling dates.

Exponential growth
------------------

![Posterior distributions for the sampling dates of ancient samples (left) and the TMRCAs of clades (right) inferred under a relaxed (orange) and strict (blue) clock model. The distributions are truncated at the upper and lower limits of the 95% HPD interval and the red lines indicate the median estimates. All analyses used an **exponential growth** coalescent tree prior and **narrow uniform** priors on sampling dates.](../results/beast/D/figures/Exp.narrow-1.png)

> **Figure 3:** Posterior distributions for the sampling dates of ancient samples (left) and the TMRCAs of clades (right) inferred under a relaxed (orange) and strict (blue) clock model. The distributions are truncated at the upper and lower limits of the 95% HPD interval and the red lines indicate the median estimates. All analyses used an **exponential growth** coalescent tree prior and **narrow uniform** priors on sampling dates.

![Posterior distributions for the sampling dates of ancient samples (left) and the TMRCAs of clades (right) inferred under a relaxed (orange) and strict (blue) clock model. The distributions are truncated at the upper and lower limits of the 95% HPD interval and the red lines indicate the median estimates. All analyses used an **exponential growth** coalescent tree prior and **wide uniform** priors on sampling dates.](../results/beast/D/figures/Exp.wide-1.png)

> **Figure 4:** Posterior distributions for the sampling dates of ancient samples (left) and the TMRCAs of clades (right) inferred under a relaxed (orange) and strict (blue) clock model. The distributions are truncated at the upper and lower limits of the 95% HPD interval and the red lines indicate the median estimates. All analyses used an **exponential growth** coalescent tree prior and **wide uniform** priors on sampling dates.

Bayesian Skyline Plot
---------------------

![Posterior distributions for the sampling dates of ancient samples (left) and the TMRCAs of clades (right) inferred under a relaxed (orange) and strict (blue) clock model. The distributions are truncated at the upper and lower limits of the 95% HPD interval and the red lines indicate the median estimates. All analyses used a **Bayesian skyline plot** coalescent tree prior and **narrow uniform** priors on sampling dates.](../results/beast/D/figures/BSP10.narrow-1.png)

> **Figure 5:** Posterior distributions for the sampling dates of ancient samples (left) and the TMRCAs of clades (right) inferred under a relaxed (orange) and strict (blue) clock model. The distributions are truncated at the upper and lower limits of the 95% HPD interval and the red lines indicate the median estimates. All analyses used a **Bayesian skyline plot** coalescent tree prior and **narrow uniform** priors on sampling dates.

![Posterior distributions for the sampling dates of ancient samples (left) and the TMRCAs of clades (right) inferred under a relaxed (orange) and strict (blue) clock model. The distributions are truncated at the upper and lower limits of the 95% HPD interval and the red lines indicate the median estimates. All analyses used a **Bayesian skyline plot** coalescent tree prior and **wide uniform** priors on sampling dates.](../results/beast/D/figures/BSP10.wide-1.png)

> **Figure 6:** Posterior distributions for the sampling dates of ancient samples (left) and the TMRCAs of clades (right) inferred under a relaxed (orange) and strict (blue) clock model. The distributions are truncated at the upper and lower limits of the 95% HPD interval and the red lines indicate the median estimates. All analyses used a **Bayesian skyline plot** coalescent tree prior and **wide uniform** priors on sampling dates.

> **Table 2:**

<table>
<caption>Sampling time estimates for ancient sequences under different models. The posterior probability that a sample is pre-Columbian is calculated as the proportion of posterior samples with a date &lt; 1493.</caption>
<colgroup>
<col width="8%" />
<col width="16%" />
<col width="15%" />
<col width="13%" />
<col width="9%" />
<col width="11%" />
<col width="11%" />
<col width="15%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sample</th>
<th align="left">Tip date prior</th>
<th align="left">Clock model</th>
<th align="left">Tree prior</th>
<th align="right">Median</th>
<th align="right">HPD lower</th>
<th align="right">HPD upper</th>
<th align="right">Pre-Columbian</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left">133</td>
<td align="left">Narrow</td>
<td align="left">Relaxed clock</td>
<td align="left">Constant</td>
<td align="right">1663.40</td>
<td align="right">1600.06</td>
<td align="right">1775.12</td>
<td align="right">0.00</td>
</tr>
<tr class="even">
<td align="left">133</td>
<td align="left">Narrow</td>
<td align="left">Relaxed clock</td>
<td align="left">Exponential</td>
<td align="right">1663.70</td>
<td align="right">1600.13</td>
<td align="right">1771.70</td>
<td align="right">0.00</td>
</tr>
<tr class="odd">
<td align="left">133</td>
<td align="left">Narrow</td>
<td align="left">Relaxed clock</td>
<td align="left">BSP</td>
<td align="right">1663.72</td>
<td align="right">1600.00</td>
<td align="right">1780.22</td>
<td align="right">0.00</td>
</tr>
<tr class="even">
<td align="left">133</td>
<td align="left">Narrow</td>
<td align="left">Strict clock</td>
<td align="left">Constant</td>
<td align="right">1658.42</td>
<td align="right">1600.14</td>
<td align="right">1722.64</td>
<td align="right">0.00</td>
</tr>
<tr class="odd">
<td align="left">133</td>
<td align="left">Narrow</td>
<td align="left">Strict clock</td>
<td align="left">Exponential</td>
<td align="right">1659.45</td>
<td align="right">1600.21</td>
<td align="right">1720.76</td>
<td align="right">0.00</td>
</tr>
<tr class="even">
<td align="left">133</td>
<td align="left">Narrow</td>
<td align="left">Strict clock</td>
<td align="left">BSP</td>
<td align="right">1662.85</td>
<td align="right">1600.03</td>
<td align="right">1725.75</td>
<td align="right">0.00</td>
</tr>
<tr class="odd">
<td align="left">133</td>
<td align="left">Wide</td>
<td align="left">Relaxed clock</td>
<td align="left">Constant</td>
<td align="right">1843.82</td>
<td align="right">1685.38</td>
<td align="right">1984.38</td>
<td align="right">0.00</td>
</tr>
<tr class="even">
<td align="left">133</td>
<td align="left">Wide</td>
<td align="left">Relaxed clock</td>
<td align="left">Exponential</td>
<td align="right">1856.14</td>
<td align="right">1715.03</td>
<td align="right">1978.69</td>
<td align="right">0.00</td>
</tr>
<tr class="odd">
<td align="left">133</td>
<td align="left">Wide</td>
<td align="left">Relaxed clock</td>
<td align="left">BSP</td>
<td align="right">1846.24</td>
<td align="right">1709.33</td>
<td align="right">1962.53</td>
<td align="right">0.00</td>
</tr>
<tr class="even">
<td align="left">133</td>
<td align="left">Wide</td>
<td align="left">Strict clock</td>
<td align="left">Constant</td>
<td align="right">1783.36</td>
<td align="right">1623.57</td>
<td align="right">1882.66</td>
<td align="right">0.00</td>
</tr>
<tr class="odd">
<td align="left">133</td>
<td align="left">Wide</td>
<td align="left">Strict clock</td>
<td align="left">Exponential</td>
<td align="right">1800.27</td>
<td align="right">1674.82</td>
<td align="right">1889.61</td>
<td align="right">0.00</td>
</tr>
<tr class="even">
<td align="left">133</td>
<td align="left">Wide</td>
<td align="left">Strict clock</td>
<td align="left">BSP</td>
<td align="right">1798.17</td>
<td align="right">1687.60</td>
<td align="right">1883.06</td>
<td align="right">0.00</td>
</tr>
<tr class="odd">
<td align="left">CHS119</td>
<td align="left">Narrow</td>
<td align="left">Relaxed clock</td>
<td align="left">Constant</td>
<td align="right">1607.88</td>
<td align="right">1542.20</td>
<td align="right">1629.99</td>
<td align="right">0.01</td>
</tr>
<tr class="even">
<td align="left">CHS119</td>
<td align="left">Narrow</td>
<td align="left">Relaxed clock</td>
<td align="left">Exponential</td>
<td align="right">1609.38</td>
<td align="right">1544.29</td>
<td align="right">1629.99</td>
<td align="right">0.01</td>
</tr>
<tr class="odd">
<td align="left">CHS119</td>
<td align="left">Narrow</td>
<td align="left">Relaxed clock</td>
<td align="left">BSP</td>
<td align="right">1609.09</td>
<td align="right">1547.07</td>
<td align="right">1629.99</td>
<td align="right">0.01</td>
</tr>
<tr class="even">
<td align="left">CHS119</td>
<td align="left">Narrow</td>
<td align="left">Strict clock</td>
<td align="left">Constant</td>
<td align="right">1614.50</td>
<td align="right">1569.21</td>
<td align="right">1629.99</td>
<td align="right">0.00</td>
</tr>
<tr class="odd">
<td align="left">CHS119</td>
<td align="left">Narrow</td>
<td align="left">Strict clock</td>
<td align="left">Exponential</td>
<td align="right">1615.47</td>
<td align="right">1572.89</td>
<td align="right">1630.00</td>
<td align="right">0.00</td>
</tr>
<tr class="even">
<td align="left">CHS119</td>
<td align="left">Narrow</td>
<td align="left">Strict clock</td>
<td align="left">BSP</td>
<td align="right">1615.61</td>
<td align="right">1572.22</td>
<td align="right">1630.00</td>
<td align="right">0.00</td>
</tr>
<tr class="odd">
<td align="left">CHS119</td>
<td align="left">Wide</td>
<td align="left">Relaxed clock</td>
<td align="left">Constant</td>
<td align="right">1825.17</td>
<td align="right">1655.66</td>
<td align="right">1965.52</td>
<td align="right">0.00</td>
</tr>
<tr class="even">
<td align="left">CHS119</td>
<td align="left">Wide</td>
<td align="left">Relaxed clock</td>
<td align="left">Exponential</td>
<td align="right">1839.71</td>
<td align="right">1694.42</td>
<td align="right">1969.59</td>
<td align="right">0.00</td>
</tr>
<tr class="odd">
<td align="left">CHS119</td>
<td align="left">Wide</td>
<td align="left">Relaxed clock</td>
<td align="left">BSP</td>
<td align="right">1827.36</td>
<td align="right">1681.68</td>
<td align="right">1941.44</td>
<td align="right">0.00</td>
</tr>
<tr class="even">
<td align="left">CHS119</td>
<td align="left">Wide</td>
<td align="left">Strict clock</td>
<td align="left">Constant</td>
<td align="right">1763.42</td>
<td align="right">1601.84</td>
<td align="right">1870.47</td>
<td align="right">0.01</td>
</tr>
<tr class="odd">
<td align="left">CHS119</td>
<td align="left">Wide</td>
<td align="left">Strict clock</td>
<td align="left">Exponential</td>
<td align="right">1781.45</td>
<td align="right">1651.53</td>
<td align="right">1871.92</td>
<td align="right">0.00</td>
</tr>
<tr class="even">
<td align="left">CHS119</td>
<td align="left">Wide</td>
<td align="left">Strict clock</td>
<td align="left">BSP</td>
<td align="right">1777.93</td>
<td align="right">1661.81</td>
<td align="right">1862.61</td>
<td align="right">0.00</td>
</tr>
<tr class="odd">
<td align="left">PD28</td>
<td align="left">Narrow</td>
<td align="left">Relaxed clock</td>
<td align="left">Constant</td>
<td align="right">1707.83</td>
<td align="right">1666.00</td>
<td align="right">1775.47</td>
<td align="right">0.00</td>
</tr>
<tr class="even">
<td align="left">PD28</td>
<td align="left">Narrow</td>
<td align="left">Relaxed clock</td>
<td align="left">Exponential</td>
<td align="right">1707.85</td>
<td align="right">1666.00</td>
<td align="right">1774.85</td>
<td align="right">0.00</td>
</tr>
<tr class="odd">
<td align="left">PD28</td>
<td align="left">Narrow</td>
<td align="left">Relaxed clock</td>
<td align="left">BSP</td>
<td align="right">1713.01</td>
<td align="right">1666.07</td>
<td align="right">1777.66</td>
<td align="right">0.00</td>
</tr>
<tr class="even">
<td align="left">PD28</td>
<td align="left">Narrow</td>
<td align="left">Strict clock</td>
<td align="left">Constant</td>
<td align="right">1691.66</td>
<td align="right">1666.00</td>
<td align="right">1753.80</td>
<td align="right">0.00</td>
</tr>
<tr class="odd">
<td align="left">PD28</td>
<td align="left">Narrow</td>
<td align="left">Strict clock</td>
<td align="left">Exponential</td>
<td align="right">1691.46</td>
<td align="right">1666.00</td>
<td align="right">1754.53</td>
<td align="right">0.00</td>
</tr>
<tr class="even">
<td align="left">PD28</td>
<td align="left">Narrow</td>
<td align="left">Strict clock</td>
<td align="left">BSP</td>
<td align="right">1694.17</td>
<td align="right">1666.00</td>
<td align="right">1760.70</td>
<td align="right">0.00</td>
</tr>
<tr class="odd">
<td align="left">PD28</td>
<td align="left">Wide</td>
<td align="left">Relaxed clock</td>
<td align="left">Constant</td>
<td align="right">1631.33</td>
<td align="right">1270.91</td>
<td align="right">1860.57</td>
<td align="right">0.22</td>
</tr>
<tr class="even">
<td align="left">PD28</td>
<td align="left">Wide</td>
<td align="left">Relaxed clock</td>
<td align="left">Exponential</td>
<td align="right">1680.30</td>
<td align="right">1355.34</td>
<td align="right">1891.03</td>
<td align="right">0.12</td>
</tr>
<tr class="odd">
<td align="left">PD28</td>
<td align="left">Wide</td>
<td align="left">Relaxed clock</td>
<td align="left">BSP</td>
<td align="right">1651.99</td>
<td align="right">1353.11</td>
<td align="right">1864.60</td>
<td align="right">0.13</td>
</tr>
<tr class="even">
<td align="left">PD28</td>
<td align="left">Wide</td>
<td align="left">Strict clock</td>
<td align="left">Constant</td>
<td align="right">1662.19</td>
<td align="right">1413.41</td>
<td align="right">1822.40</td>
<td align="right">0.10</td>
</tr>
<tr class="odd">
<td align="left">PD28</td>
<td align="left">Wide</td>
<td align="left">Strict clock</td>
<td align="left">Exponential</td>
<td align="right">1691.93</td>
<td align="right">1500.14</td>
<td align="right">1835.24</td>
<td align="right">0.04</td>
</tr>
<tr class="even">
<td align="left">PD28</td>
<td align="left">Wide</td>
<td align="left">Strict clock</td>
<td align="left">BSP</td>
<td align="right">1680.56</td>
<td align="right">1498.64</td>
<td align="right">1823.66</td>
<td align="right">0.04</td>
</tr>
<tr class="odd">
<td align="left">SJ219</td>
<td align="left">Narrow</td>
<td align="left">Relaxed clock</td>
<td align="left">Constant</td>
<td align="right">1518.24</td>
<td align="right">1429.00</td>
<td align="right">1617.06</td>
<td align="right">0.36</td>
</tr>
<tr class="even">
<td align="left">SJ219</td>
<td align="left">Narrow</td>
<td align="left">Relaxed clock</td>
<td align="left">Exponential</td>
<td align="right">1522.26</td>
<td align="right">1429.03</td>
<td align="right">1618.89</td>
<td align="right">0.33</td>
</tr>
<tr class="odd">
<td align="left">SJ219</td>
<td align="left">Narrow</td>
<td align="left">Relaxed clock</td>
<td align="left">BSP</td>
<td align="right">1535.41</td>
<td align="right">1440.72</td>
<td align="right">1632.46</td>
<td align="right">0.28</td>
</tr>
<tr class="even">
<td align="left">SJ219</td>
<td align="left">Narrow</td>
<td align="left">Strict clock</td>
<td align="left">Constant</td>
<td align="right">1516.80</td>
<td align="right">1430.03</td>
<td align="right">1606.44</td>
<td align="right">0.35</td>
</tr>
<tr class="odd">
<td align="left">SJ219</td>
<td align="left">Narrow</td>
<td align="left">Strict clock</td>
<td align="left">Exponential</td>
<td align="right">1517.68</td>
<td align="right">1429.07</td>
<td align="right">1606.11</td>
<td align="right">0.34</td>
</tr>
<tr class="even">
<td align="left">SJ219</td>
<td align="left">Narrow</td>
<td align="left">Strict clock</td>
<td align="left">BSP</td>
<td align="right">1520.38</td>
<td align="right">1430.39</td>
<td align="right">1609.72</td>
<td align="right">0.32</td>
</tr>
<tr class="odd">
<td align="left">SJ219</td>
<td align="left">Wide</td>
<td align="left">Relaxed clock</td>
<td align="left">Constant</td>
<td align="right">1526.77</td>
<td align="right">1101.48</td>
<td align="right">1747.22</td>
<td align="right">0.42</td>
</tr>
<tr class="even">
<td align="left">SJ219</td>
<td align="left">Wide</td>
<td align="left">Relaxed clock</td>
<td align="left">Exponential</td>
<td align="right">1587.43</td>
<td align="right">1208.37</td>
<td align="right">1812.82</td>
<td align="right">0.27</td>
</tr>
<tr class="odd">
<td align="left">SJ219</td>
<td align="left">Wide</td>
<td align="left">Relaxed clock</td>
<td align="left">BSP</td>
<td align="right">1560.33</td>
<td align="right">1246.60</td>
<td align="right">1783.41</td>
<td align="right">0.32</td>
</tr>
<tr class="even">
<td align="left">SJ219</td>
<td align="left">Wide</td>
<td align="left">Strict clock</td>
<td align="left">Constant</td>
<td align="right">1562.07</td>
<td align="right">1257.82</td>
<td align="right">1758.29</td>
<td align="right">0.31</td>
</tr>
<tr class="odd">
<td align="left">SJ219</td>
<td align="left">Wide</td>
<td align="left">Strict clock</td>
<td align="left">Exponential</td>
<td align="right">1599.41</td>
<td align="right">1364.49</td>
<td align="right">1763.35</td>
<td align="right">0.18</td>
</tr>
<tr class="even">
<td align="left">SJ219</td>
<td align="left">Wide</td>
<td align="left">Strict clock</td>
<td align="left">BSP</td>
<td align="right">1587.08</td>
<td align="right">1370.20</td>
<td align="right">1748.22</td>
<td align="right">0.18</td>
</tr>
</tbody>
</table>

> **Table 3:**

<table>
<caption>TMRCA estimates for clades under different models. The posterior probability that a clade is monophyletic is calculated as the proportion of posterior trees where the clade is monophyletic.</caption>
<colgroup>
<col width="9%" />
<col width="16%" />
<col width="15%" />
<col width="13%" />
<col width="9%" />
<col width="11%" />
<col width="11%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Clade</th>
<th align="left">Tip date prior</th>
<th align="left">Clock model</th>
<th align="left">Tree prior</th>
<th align="right">Median</th>
<th align="right">HPD lower</th>
<th align="right">HPD upper</th>
<th align="right">Monophyletic</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left">Nichols</td>
<td align="left">Narrow</td>
<td align="left">Relaxed clock</td>
<td align="left">Constant</td>
<td align="right">1610.65</td>
<td align="right">1393.73</td>
<td align="right">1755.22</td>
<td align="right">0.97</td>
</tr>
<tr class="even">
<td align="left">Nichols</td>
<td align="left">Narrow</td>
<td align="left">Relaxed clock</td>
<td align="left">Exponential</td>
<td align="right">1621.26</td>
<td align="right">1432.24</td>
<td align="right">1769.14</td>
<td align="right">0.97</td>
</tr>
<tr class="odd">
<td align="left">Nichols</td>
<td align="left">Narrow</td>
<td align="left">Relaxed clock</td>
<td align="left">BSP</td>
<td align="right">1625.48</td>
<td align="right">1485.25</td>
<td align="right">1757.74</td>
<td align="right">0.97</td>
</tr>
<tr class="even">
<td align="left">Nichols</td>
<td align="left">Narrow</td>
<td align="left">Strict clock</td>
<td align="left">Constant</td>
<td align="right">1612.83</td>
<td align="right">1517.87</td>
<td align="right">1695.03</td>
<td align="right">0.97</td>
</tr>
<tr class="odd">
<td align="left">Nichols</td>
<td align="left">Narrow</td>
<td align="left">Strict clock</td>
<td align="left">Exponential</td>
<td align="right">1616.11</td>
<td align="right">1517.32</td>
<td align="right">1694.03</td>
<td align="right">0.97</td>
</tr>
<tr class="even">
<td align="left">Nichols</td>
<td align="left">Narrow</td>
<td align="left">Strict clock</td>
<td align="left">BSP</td>
<td align="right">1613.62</td>
<td align="right">1519.24</td>
<td align="right">1694.63</td>
<td align="right">0.97</td>
</tr>
<tr class="odd">
<td align="left">Nichols</td>
<td align="left">Wide</td>
<td align="left">Relaxed clock</td>
<td align="left">Constant</td>
<td align="right">1697.21</td>
<td align="right">1447.96</td>
<td align="right">1835.91</td>
<td align="right">0.97</td>
</tr>
<tr class="even">
<td align="left">Nichols</td>
<td align="left">Wide</td>
<td align="left">Relaxed clock</td>
<td align="left">Exponential</td>
<td align="right">1729.43</td>
<td align="right">1510.09</td>
<td align="right">1863.76</td>
<td align="right">0.97</td>
</tr>
<tr class="odd">
<td align="left">Nichols</td>
<td align="left">Wide</td>
<td align="left">Relaxed clock</td>
<td align="left">BSP</td>
<td align="right">1711.98</td>
<td align="right">1540.55</td>
<td align="right">1833.51</td>
<td align="right">0.97</td>
</tr>
<tr class="even">
<td align="left">Nichols</td>
<td align="left">Wide</td>
<td align="left">Strict clock</td>
<td align="left">Constant</td>
<td align="right">1694.25</td>
<td align="right">1492.72</td>
<td align="right">1812.34</td>
<td align="right">0.97</td>
</tr>
<tr class="odd">
<td align="left">Nichols</td>
<td align="left">Wide</td>
<td align="left">Strict clock</td>
<td align="left">Exponential</td>
<td align="right">1717.82</td>
<td align="right">1567.55</td>
<td align="right">1822.98</td>
<td align="right">0.97</td>
</tr>
<tr class="even">
<td align="left">Nichols</td>
<td align="left">Wide</td>
<td align="left">Strict clock</td>
<td align="left">BSP</td>
<td align="right">1713.93</td>
<td align="right">1583.77</td>
<td align="right">1810.75</td>
<td align="right">0.97</td>
</tr>
<tr class="odd">
<td align="left">SS14</td>
<td align="left">Narrow</td>
<td align="left">Relaxed clock</td>
<td align="left">Constant</td>
<td align="right">1815.96</td>
<td align="right">1689.98</td>
<td align="right">1902.60</td>
<td align="right">0.98</td>
</tr>
<tr class="even">
<td align="left">SS14</td>
<td align="left">Narrow</td>
<td align="left">Relaxed clock</td>
<td align="left">Exponential</td>
<td align="right">1822.16</td>
<td align="right">1701.09</td>
<td align="right">1899.91</td>
<td align="right">0.98</td>
</tr>
<tr class="odd">
<td align="left">SS14</td>
<td align="left">Narrow</td>
<td align="left">Relaxed clock</td>
<td align="left">BSP</td>
<td align="right">1834.92</td>
<td align="right">1729.45</td>
<td align="right">1912.34</td>
<td align="right">0.98</td>
</tr>
<tr class="even">
<td align="left">SS14</td>
<td align="left">Narrow</td>
<td align="left">Strict clock</td>
<td align="left">Constant</td>
<td align="right">1824.79</td>
<td align="right">1764.18</td>
<td align="right">1874.40</td>
<td align="right">0.98</td>
</tr>
<tr class="odd">
<td align="left">SS14</td>
<td align="left">Narrow</td>
<td align="left">Strict clock</td>
<td align="left">Exponential</td>
<td align="right">1827.11</td>
<td align="right">1767.02</td>
<td align="right">1875.85</td>
<td align="right">0.98</td>
</tr>
<tr class="even">
<td align="left">SS14</td>
<td align="left">Narrow</td>
<td align="left">Strict clock</td>
<td align="left">BSP</td>
<td align="right">1829.56</td>
<td align="right">1773.19</td>
<td align="right">1882.19</td>
<td align="right">0.98</td>
</tr>
<tr class="odd">
<td align="left">SS14</td>
<td align="left">Wide</td>
<td align="left">Relaxed clock</td>
<td align="left">Constant</td>
<td align="right">1865.74</td>
<td align="right">1743.88</td>
<td align="right">1930.24</td>
<td align="right">0.98</td>
</tr>
<tr class="even">
<td align="left">SS14</td>
<td align="left">Wide</td>
<td align="left">Relaxed clock</td>
<td align="left">Exponential</td>
<td align="right">1877.66</td>
<td align="right">1773.12</td>
<td align="right">1933.19</td>
<td align="right">0.98</td>
</tr>
<tr class="odd">
<td align="left">SS14</td>
<td align="left">Wide</td>
<td align="left">Relaxed clock</td>
<td align="left">BSP</td>
<td align="right">1869.30</td>
<td align="right">1770.51</td>
<td align="right">1930.23</td>
<td align="right">0.99</td>
</tr>
<tr class="even">
<td align="left">SS14</td>
<td align="left">Wide</td>
<td align="left">Strict clock</td>
<td align="left">Constant</td>
<td align="right">1860.95</td>
<td align="right">1771.36</td>
<td align="right">1913.15</td>
<td align="right">0.98</td>
</tr>
<tr class="odd">
<td align="left">SS14</td>
<td align="left">Wide</td>
<td align="left">Strict clock</td>
<td align="left">Exponential</td>
<td align="right">1871.46</td>
<td align="right">1798.78</td>
<td align="right">1916.73</td>
<td align="right">0.98</td>
</tr>
<tr class="even">
<td align="left">SS14</td>
<td align="left">Wide</td>
<td align="left">Strict clock</td>
<td align="left">BSP</td>
<td align="right">1868.66</td>
<td align="right">1806.86</td>
<td align="right">1915.26</td>
<td align="right">0.98</td>
</tr>
<tr class="odd">
<td align="left">SS14-w</td>
<td align="left">Narrow</td>
<td align="left">Relaxed clock</td>
<td align="left">Constant</td>
<td align="right">1935.43</td>
<td align="right">1886.91</td>
<td align="right">1966.68</td>
<td align="right">0.98</td>
</tr>
<tr class="even">
<td align="left">SS14-w</td>
<td align="left">Narrow</td>
<td align="left">Relaxed clock</td>
<td align="left">Exponential</td>
<td align="right">1937.76</td>
<td align="right">1895.73</td>
<td align="right">1967.67</td>
<td align="right">0.97</td>
</tr>
<tr class="odd">
<td align="left">SS14-w</td>
<td align="left">Narrow</td>
<td align="left">Relaxed clock</td>
<td align="left">BSP</td>
<td align="right">1954.58</td>
<td align="right">1927.80</td>
<td align="right">1973.75</td>
<td align="right">0.98</td>
</tr>
<tr class="even">
<td align="left">SS14-w</td>
<td align="left">Narrow</td>
<td align="left">Strict clock</td>
<td align="left">Constant</td>
<td align="right">1944.16</td>
<td align="right">1919.57</td>
<td align="right">1964.65</td>
<td align="right">0.98</td>
</tr>
<tr class="odd">
<td align="left">SS14-w</td>
<td align="left">Narrow</td>
<td align="left">Strict clock</td>
<td align="left">Exponential</td>
<td align="right">1944.68</td>
<td align="right">1921.23</td>
<td align="right">1964.44</td>
<td align="right">0.98</td>
</tr>
<tr class="even">
<td align="left">SS14-w</td>
<td align="left">Narrow</td>
<td align="left">Strict clock</td>
<td align="left">BSP</td>
<td align="right">1953.58</td>
<td align="right">1932.33</td>
<td align="right">1970.91</td>
<td align="right">0.98</td>
</tr>
<tr class="odd">
<td align="left">SS14-w</td>
<td align="left">Wide</td>
<td align="left">Relaxed clock</td>
<td align="left">Constant</td>
<td align="right">1953.89</td>
<td align="right">1913.85</td>
<td align="right">1973.97</td>
<td align="right">0.98</td>
</tr>
<tr class="even">
<td align="left">SS14-w</td>
<td align="left">Wide</td>
<td align="left">Relaxed clock</td>
<td align="left">Exponential</td>
<td align="right">1957.57</td>
<td align="right">1924.53</td>
<td align="right">1973.98</td>
<td align="right">0.98</td>
</tr>
<tr class="odd">
<td align="left">SS14-w</td>
<td align="left">Wide</td>
<td align="left">Relaxed clock</td>
<td align="left">BSP</td>
<td align="right">1962.95</td>
<td align="right">1942.10</td>
<td align="right">1975.15</td>
<td align="right">0.98</td>
</tr>
<tr class="even">
<td align="left">SS14-w</td>
<td align="left">Wide</td>
<td align="left">Strict clock</td>
<td align="left">Constant</td>
<td align="right">1956.03</td>
<td align="right">1925.64</td>
<td align="right">1972.81</td>
<td align="right">0.98</td>
</tr>
<tr class="odd">
<td align="left">SS14-w</td>
<td align="left">Wide</td>
<td align="left">Strict clock</td>
<td align="left">Exponential</td>
<td align="right">1959.17</td>
<td align="right">1934.29</td>
<td align="right">1973.12</td>
<td align="right">0.98</td>
</tr>
<tr class="even">
<td align="left">SS14-w</td>
<td align="left">Wide</td>
<td align="left">Strict clock</td>
<td align="left">BSP</td>
<td align="right">1963.22</td>
<td align="right">1945.72</td>
<td align="right">1974.71</td>
<td align="right">0.98</td>
</tr>
<tr class="odd">
<td align="left">TPA</td>
<td align="left">Narrow</td>
<td align="left">Relaxed clock</td>
<td align="left">Constant</td>
<td align="right">1275.65</td>
<td align="right">914.40</td>
<td align="right">1489.14</td>
<td align="right">0.98</td>
</tr>
<tr class="even">
<td align="left">TPA</td>
<td align="left">Narrow</td>
<td align="left">Relaxed clock</td>
<td align="left">Exponential</td>
<td align="right">1293.51</td>
<td align="right">990.62</td>
<td align="right">1503.46</td>
<td align="right">0.98</td>
</tr>
<tr class="odd">
<td align="left">TPA</td>
<td align="left">Narrow</td>
<td align="left">Relaxed clock</td>
<td align="left">BSP</td>
<td align="right">1339.12</td>
<td align="right">1117.16</td>
<td align="right">1515.99</td>
<td align="right">0.98</td>
</tr>
<tr class="even">
<td align="left">TPA</td>
<td align="left">Narrow</td>
<td align="left">Strict clock</td>
<td align="left">Constant</td>
<td align="right">1328.03</td>
<td align="right">1187.52</td>
<td align="right">1453.53</td>
<td align="right">0.98</td>
</tr>
<tr class="odd">
<td align="left">TPA</td>
<td align="left">Narrow</td>
<td align="left">Strict clock</td>
<td align="left">Exponential</td>
<td align="right">1330.36</td>
<td align="right">1193.78</td>
<td align="right">1452.22</td>
<td align="right">0.98</td>
</tr>
<tr class="even">
<td align="left">TPA</td>
<td align="left">Narrow</td>
<td align="left">Strict clock</td>
<td align="left">BSP</td>
<td align="right">1336.73</td>
<td align="right">1201.99</td>
<td align="right">1466.62</td>
<td align="right">0.98</td>
</tr>
<tr class="odd">
<td align="left">TPA</td>
<td align="left">Wide</td>
<td align="left">Relaxed clock</td>
<td align="left">Constant</td>
<td align="right">1388.06</td>
<td align="right">889.91</td>
<td align="right">1667.76</td>
<td align="right">0.98</td>
</tr>
<tr class="even">
<td align="left">TPA</td>
<td align="left">Wide</td>
<td align="left">Relaxed clock</td>
<td align="left">Exponential</td>
<td align="right">1463.10</td>
<td align="right">1002.81</td>
<td align="right">1706.48</td>
<td align="right">0.98</td>
</tr>
<tr class="odd">
<td align="left">TPA</td>
<td align="left">Wide</td>
<td align="left">Relaxed clock</td>
<td align="left">BSP</td>
<td align="right">1438.72</td>
<td align="right">1082.41</td>
<td align="right">1684.51</td>
<td align="right">0.98</td>
</tr>
<tr class="even">
<td align="left">TPA</td>
<td align="left">Wide</td>
<td align="left">Strict clock</td>
<td align="left">Constant</td>
<td align="right">1443.54</td>
<td align="right">1071.37</td>
<td align="right">1660.39</td>
<td align="right">0.97</td>
</tr>
<tr class="odd">
<td align="left">TPA</td>
<td align="left">Wide</td>
<td align="left">Strict clock</td>
<td align="left">Exponential</td>
<td align="right">1489.59</td>
<td align="right">1205.78</td>
<td align="right">1675.66</td>
<td align="right">0.98</td>
</tr>
<tr class="even">
<td align="left">TPA</td>
<td align="left">Wide</td>
<td align="left">Strict clock</td>
<td align="left">BSP</td>
<td align="right">1477.76</td>
<td align="right">1232.29</td>
<td align="right">1669.17</td>
<td align="right">0.98</td>
</tr>
<tr class="odd">
<td align="left">TPE</td>
<td align="left">Narrow</td>
<td align="left">Relaxed clock</td>
<td align="left">Constant</td>
<td align="right">1475.63</td>
<td align="right">1319.60</td>
<td align="right">1571.78</td>
<td align="right">0.96</td>
</tr>
<tr class="even">
<td align="left">TPE</td>
<td align="left">Narrow</td>
<td align="left">Relaxed clock</td>
<td align="left">Exponential</td>
<td align="right">1482.09</td>
<td align="right">1343.32</td>
<td align="right">1572.03</td>
<td align="right">0.97</td>
</tr>
<tr class="odd">
<td align="left">TPE</td>
<td align="left">Narrow</td>
<td align="left">Relaxed clock</td>
<td align="left">BSP</td>
<td align="right">1488.78</td>
<td align="right">1376.73</td>
<td align="right">1570.28</td>
<td align="right">0.97</td>
</tr>
<tr class="even">
<td align="left">TPE</td>
<td align="left">Narrow</td>
<td align="left">Strict clock</td>
<td align="left">Constant</td>
<td align="right">1498.12</td>
<td align="right">1411.28</td>
<td align="right">1566.40</td>
<td align="right">0.97</td>
</tr>
<tr class="odd">
<td align="left">TPE</td>
<td align="left">Narrow</td>
<td align="left">Strict clock</td>
<td align="left">Exponential</td>
<td align="right">1500.33</td>
<td align="right">1415.59</td>
<td align="right">1566.27</td>
<td align="right">0.97</td>
</tr>
<tr class="even">
<td align="left">TPE</td>
<td align="left">Narrow</td>
<td align="left">Strict clock</td>
<td align="left">BSP</td>
<td align="right">1502.21</td>
<td align="right">1415.59</td>
<td align="right">1566.10</td>
<td align="right">0.97</td>
</tr>
<tr class="odd">
<td align="left">TPE</td>
<td align="left">Wide</td>
<td align="left">Relaxed clock</td>
<td align="left">Constant</td>
<td align="right">1702.90</td>
<td align="right">1470.97</td>
<td align="right">1861.21</td>
<td align="right">0.97</td>
</tr>
<tr class="even">
<td align="left">TPE</td>
<td align="left">Wide</td>
<td align="left">Relaxed clock</td>
<td align="left">Exponential</td>
<td align="right">1730.03</td>
<td align="right">1534.38</td>
<td align="right">1859.04</td>
<td align="right">0.97</td>
</tr>
<tr class="odd">
<td align="left">TPE</td>
<td align="left">Wide</td>
<td align="left">Relaxed clock</td>
<td align="left">BSP</td>
<td align="right">1714.41</td>
<td align="right">1556.91</td>
<td align="right">1840.16</td>
<td align="right">0.97</td>
</tr>
<tr class="even">
<td align="left">TPE</td>
<td align="left">Wide</td>
<td align="left">Strict clock</td>
<td align="left">Constant</td>
<td align="right">1650.12</td>
<td align="right">1424.34</td>
<td align="right">1787.37</td>
<td align="right">0.97</td>
</tr>
<tr class="odd">
<td align="left">TPE</td>
<td align="left">Wide</td>
<td align="left">Strict clock</td>
<td align="left">Exponential</td>
<td align="right">1677.11</td>
<td align="right">1499.42</td>
<td align="right">1784.64</td>
<td align="right">0.97</td>
</tr>
<tr class="even">
<td align="left">TPE</td>
<td align="left">Wide</td>
<td align="left">Strict clock</td>
<td align="left">BSP</td>
<td align="right">1673.07</td>
<td align="right">1527.91</td>
<td align="right">1787.88</td>
<td align="right">0.97</td>
</tr>
<tr class="odd">
<td align="left">TPE/TEN</td>
<td align="left">Narrow</td>
<td align="left">Relaxed clock</td>
<td align="left">Constant</td>
<td align="right">374.67</td>
<td align="right">-640.44</td>
<td align="right">1106.99</td>
<td align="right">0.96</td>
</tr>
<tr class="even">
<td align="left">TPE/TEN</td>
<td align="left">Narrow</td>
<td align="left">Relaxed clock</td>
<td align="left">Exponential</td>
<td align="right">393.26</td>
<td align="right">-652.88</td>
<td align="right">1154.64</td>
<td align="right">0.96</td>
</tr>
<tr class="odd">
<td align="left">TPE/TEN</td>
<td align="left">Narrow</td>
<td align="left">Relaxed clock</td>
<td align="left">BSP</td>
<td align="right">472.19</td>
<td align="right">-371.68</td>
<td align="right">1110.10</td>
<td align="right">0.96</td>
</tr>
<tr class="even">
<td align="left">TPE/TEN</td>
<td align="left">Narrow</td>
<td align="left">Strict clock</td>
<td align="left">Constant</td>
<td align="right">335.55</td>
<td align="right">-66.31</td>
<td align="right">651.19</td>
<td align="right">0.97</td>
</tr>
<tr class="odd">
<td align="left">TPE/TEN</td>
<td align="left">Narrow</td>
<td align="left">Strict clock</td>
<td align="left">Exponential</td>
<td align="right">347.87</td>
<td align="right">-23.75</td>
<td align="right">679.04</td>
<td align="right">0.97</td>
</tr>
<tr class="even">
<td align="left">TPE/TEN</td>
<td align="left">Narrow</td>
<td align="left">Strict clock</td>
<td align="left">BSP</td>
<td align="right">352.23</td>
<td align="right">-34.05</td>
<td align="right">678.49</td>
<td align="right">0.97</td>
</tr>
<tr class="odd">
<td align="left">TPE/TEN</td>
<td align="left">Wide</td>
<td align="left">Relaxed clock</td>
<td align="left">Constant</td>
<td align="right">930.26</td>
<td align="right">-66.42</td>
<td align="right">1590.92</td>
<td align="right">0.97</td>
</tr>
<tr class="even">
<td align="left">TPE/TEN</td>
<td align="left">Wide</td>
<td align="left">Relaxed clock</td>
<td align="left">Exponential</td>
<td align="right">1019.28</td>
<td align="right">164.72</td>
<td align="right">1566.68</td>
<td align="right">0.97</td>
</tr>
<tr class="odd">
<td align="left">TPE/TEN</td>
<td align="left">Wide</td>
<td align="left">Relaxed clock</td>
<td align="left">BSP</td>
<td align="right">969.16</td>
<td align="right">282.00</td>
<td align="right">1520.45</td>
<td align="right">0.97</td>
</tr>
<tr class="even">
<td align="left">TPE/TEN</td>
<td align="left">Wide</td>
<td align="left">Strict clock</td>
<td align="left">Constant</td>
<td align="right">775.48</td>
<td align="right">-21.33</td>
<td align="right">1269.66</td>
<td align="right">0.96</td>
</tr>
<tr class="odd">
<td align="left">TPE/TEN</td>
<td align="left">Wide</td>
<td align="left">Strict clock</td>
<td align="left">Exponential</td>
<td align="right">871.77</td>
<td align="right">250.65</td>
<td align="right">1269.51</td>
<td align="right">0.97</td>
</tr>
<tr class="even">
<td align="left">TPE/TEN</td>
<td align="left">Wide</td>
<td align="left">Strict clock</td>
<td align="left">BSP</td>
<td align="right">846.71</td>
<td align="right">295.28</td>
<td align="right">1242.05</td>
<td align="right">0.97</td>
</tr>
</tbody>
</table>

Posterior distributions compared between models
===============================================

![Posterior distributions for the Treponema TMRCA inferred under a relaxed (orange) and strict (blue) clock model with various tree priors and priors on the sampling dates of ancient sequences. The distributions are truncated at the upper and lower limits of the 95% HPD interval and the red lines indicate the median estimates.](../results/beast/D/figures/treeheight-1.png)

> **Figure 7:** Posterior distributions for the Treponema TMRCA inferred under a relaxed (orange) and strict (blue) clock model with various tree priors and priors on the sampling dates of ancient sequences. The distributions are truncated at the upper and lower limits of the 95% HPD interval and the red lines indicate the median estimates.

![Posterior distributions for the TPP/TPE TMRCA inferred under a relaxed (orange) and strict (blue) clock model with various tree priors and priors on the sampling dates of ancient sequences. The distributions are truncated at the upper and lower limits of the 95% HPD interval and the red lines indicate the median estimates.](../results/beast/D/figures/TPP.TPE-1.png)

> **Figure 8:** Posterior distributions for the TPP/TPE TMRCA inferred under a relaxed (orange) and strict (blue) clock model with various tree priors and priors on the sampling dates of ancient sequences. The distributions are truncated at the upper and lower limits of the 95% HPD interval and the red lines indicate the median estimates.

![Posterior distributions for the substitution rate inferred under a relaxed (orange) and strict (blue) clock model with various tree priors and priors on the sampling dates of ancient sequences. The distributions are truncated at the upper and lower limits of the 95% HPD interval and the red lines indicate the median estimates. The relaxed clock estimates show the mean rate across the tree. The shaded boxes represent the substitution rate estimates reported in Beale et al. (2019) for the TPA clade.](../results/beast/D/figures/clockrate-1.png)

> **Figure 9:** Posterior distributions for the substitution rate inferred under a relaxed (orange) and strict (blue) clock model with various tree priors and priors on the sampling dates of ancient sequences. The distributions are truncated at the upper and lower limits of the 95% HPD interval and the red lines indicate the median estimates. The relaxed clock estimates show the mean rate across the tree. The shaded boxes represent the substitution rate estimates reported in Beale et al. (2019) for the TPA clade.

![Posterior distributions of the sampling date of SJ219 inferred under a relaxed (orange) and strict (blue) clock model with various tree priors and priors on the sampling dates of ancient sequences. The distributions are truncated at the upper and lower limits of the 95% HPD interval and the red lines indicate the median estimates. The shaded boxes represent the sampling date range inferred from radiocarbon dating.](../results/beast/D/figures/SJ219-1.png)

> **Figure 10:** Posterior distributions of the sampling date of SJ219 inferred under a relaxed (orange) and strict (blue) clock model with various tree priors and priors on the sampling dates of ancient sequences. The distributions are truncated at the upper and lower limits of the 95% HPD interval and the red lines indicate the median estimates. The shaded boxes represent the sampling date range inferred from radiocarbon dating.

![Posterior distributions of the sampling date of PD28 inferred under a relaxed (orange) and strict (blue) clock model with various tree priors and priors on the sampling dates of ancient sequences. The distributions are truncated at the upper and lower limits of the 95% HPD interval and the red lines indicate the median estimates. The shaded boxes represent the sampling date range inferred from radiocarbon dating.](../results/beast/D/figures/PD28-1.png)

> **Figure 11:** Posterior distributions of the sampling date of PD28 inferred under a relaxed (orange) and strict (blue) clock model with various tree priors and priors on the sampling dates of ancient sequences. The distributions are truncated at the upper and lower limits of the 95% HPD interval and the red lines indicate the median estimates. The shaded boxes represent the sampling date range inferred from radiocarbon dating.

![Posterior distributions of the sampling date of CHS119 inferred under a relaxed (orange) and strict (blue) clock model with various tree priors and priors on the sampling dates of ancient sequences. The distributions are truncated at the upper and lower limits of the 95% HPD interval and the red lines indicate the median estimates. The shaded boxes represent the sampling date range inferred from radiocarbon dating.](../results/beast/D/figures/CHS119-1.png)

> **Figure 12:** Posterior distributions of the sampling date of CHS119 inferred under a relaxed (orange) and strict (blue) clock model with various tree priors and priors on the sampling dates of ancient sequences. The distributions are truncated at the upper and lower limits of the 95% HPD interval and the red lines indicate the median estimates. The shaded boxes represent the sampling date range inferred from radiocarbon dating.

MCC trees
=========

![Maximum clade credibility tree inferred under a **relaxed clock** model, **Bayesian skyline plot** coalescent tree prior and **narrow uniform** priors on sampling dates. Sequences with estimated sampling dates are highlighted and the HPD interval of the sampling date is shown in parentheses. Nodes with posterior support of at least 90% are highlighted.](../results/beast/D/figures/BSP10.relaxed.narrow.MCC-1.png)

> **Figure 13:** Maximum clade credibility tree inferred under a **relaxed clock** model, **Bayesian skyline plot** coalescent tree prior and **narrow uniform** priors on sampling dates. Sequences with estimated sampling dates are highlighted and the HPD interval of the sampling date is shown in parentheses. Nodes with posterior support of at least 90% are highlighted.

![Maximum clade credibility tree inferred under a **relaxed clock** model, **Bayesian skyline plot** coalescent tree prior and **wide uniform** priors on sampling dates. Sequences with estimated sampling dates are highlighted and the HPD interval of the sampling date is shown in parentheses. Nodes with posterior support of at least 90% are highlighted.](../results/beast/D/figures/BSP10.relaxed.wide.MCC-1.png)

> **Figure 14:** Maximum clade credibility tree inferred under a **relaxed clock** model, **Bayesian skyline plot** coalescent tree prior and **wide uniform** priors on sampling dates. Sequences with estimated sampling dates are highlighted and the HPD interval of the sampling date is shown in parentheses. Nodes with posterior support of at least 90% are highlighted.

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
    ##  [9] ggsci_2.9       ggplot2_3.2.1   ggtree_2.1.1    treeio_1.11.2  
    ## [13] beastio_0.2.5   coda_0.19-3     cowplot_1.0.0  
    ## 
    ## loaded via a namespace (and not attached):
    ##  [1] Rcpp_1.0.3              lattice_0.20-38         tidyr_1.0.0            
    ##  [4] gtools_3.8.1            assertthat_0.2.1        zeallot_0.1.0          
    ##  [7] digest_0.6.23           R6_2.4.1                backports_1.1.5        
    ## [10] evaluate_0.14           highr_0.8               pillar_1.4.2           
    ## [13] rlang_0.4.2             lazyeval_0.2.2          Matrix_1.2-18          
    ## [16] combinat_0.0-8          rmarkdown_2.3           stringr_1.4.0          
    ## [19] igraph_1.2.4.2          munsell_0.5.0           compiler_3.5.1         
    ## [22] numDeriv_2016.8-1.1     xfun_0.15               pkgconfig_2.0.3        
    ## [25] mnormt_1.5-5            htmltools_0.4.0         tidyselect_0.2.5       
    ## [28] lpSolve_5.6.13.3        tibble_2.1.3            expm_0.999-4           
    ## [31] quadprog_1.5-8          crayon_1.3.4            dplyr_0.8.3            
    ## [34] withr_2.1.2             MASS_7.3-51.4           grid_3.5.1             
    ## [37] nlme_3.1-143            jsonlite_1.6            gtable_0.3.0           
    ## [40] lifecycle_0.1.0         scales_1.1.0            tidytree_0.3.1         
    ## [43] stringi_1.4.3           farver_2.0.1            ggsignif_0.6.0         
    ## [46] scatterplot3d_0.3-41    rvcheck_0.1.7           vctrs_0.2.1            
    ## [49] fastmatch_1.1-0         RColorBrewer_1.1-2      tools_3.5.1            
    ## [52] glue_1.3.1              purrr_0.3.3             plotrix_3.7-7          
    ## [55] parallel_3.5.1          yaml_2.2.0              colorspace_1.4-1       
    ## [58] BiocManager_1.30.10     animation_2.6           clusterGeneration_1.3.4
    ## [61] knitr_1.29
