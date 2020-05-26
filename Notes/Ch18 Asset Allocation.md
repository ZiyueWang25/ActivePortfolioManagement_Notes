# Study Notes

### Learning Plan

April 30 - May 30, 31 days

__Part 1 Foundations__

Ch2 Consensus Expected Returns: The CAMP   11- 40  3.5h

Ch3 Risk  41 - 85  3h

Ch4 Exceptional Return, Benchmarks, and Value Added  87 - 108 2.5h

Ch5 Residual Risk and Return: The Information Ratio 109 - 145  2h

Ch6 The Fundamental Law of Active Management 147 - 169 1.5h

__Part 2 Expected Returns and Valuation__

Ch7 Expected Returns and the Arbitrage Pricing Theory 173 - 198 1.5h

Ch8 Valuation in Theory 199 - 224  1h

Ch9 Valuation in Practice 225 - 257

__Part 3 Information Processing__

Ch10 Forecasting Basics  261 - 293  1.5h

Ch11 Advanced Forecasting 295 - 314  1.5h

Ch12 Information Analysis 315 - 345  1.5h

Ch13 The Information Horizon 347 - 374  Mon  3h

__Part 4 Implementation__

Ch14 Portfolio Construction 377 - 418 0519  Tue  3h

Ch15 Long/Short Investing 419 - 443 0520 Sun 1h

Ch16 Transaction Costs, Turnover, and Trading 445 - 475 0521 Sun 1h

Ch17 Performance Analysis 477 - 515 0522 Mon  2h

**Ch18 Asset Allocation 517 - 539 0523 Tue**  40min

Ch19 Benchmark Timing  541 - 558  0524 Wed

Ch20 The Historical Record for Active Management 559 - 571 0525 Thur

Ch21 Open Questions 573 - 576 Fri

Ch22 Summary 577 - 580

__Appendix C: Return and Statistics Basics__

## 18.1 Introduction

1. it is a field lies somewhere between asset selection and benchmark timing
2. _Strategic asset allocation_ : The process of selecting a _target asset allocation_
3. _tactic asset allocation_: variation in asset allocation around that target
4. major points
   1.  Researching asset allocation strategies is a three-step process: 
      1. forecasting returns
      2. building portfolios, and
      3. analyzing out-of-sample performance.
   2. The procedure for forecasting returns for asset allocation differs from that for asset selection in its focus on time series instead of cross-sectional analysis. In spite of this, asset allocation, like asset selection, adds value through identifying relative performance.
   3. Traditional asset allocation ignores any explicit benchmark, simply trading off expected excess return against total risk. This causes substantial problems. We
      will implicitly include a benchmark in the expected returns, a procedure complicated by the presence of currencies.

## 18.2 The Three-Step Process

1. There are two related reasons to focus on separate time series models rather than a cross-sectional model
   1.  to the extent that these asset classes exhibit low correlations as compared to asset returns (which usually include a strong market factor), a time series approach makes better sense
   2. the typical explanatory variables for asset-class returns focus on the individual time series rather than on cross-sectional comparisons, and aren’t always comparable across countries and asset classes

### 18.2.1 Forecasting returns

1. $r(t)=\sum_{j} x_{j}(t) \cdot b_{j}+\epsilon(t)$
2.  In fact, our initial regression will use the first 30 months of data to forecast returns over the 31st month. Our next regression will use the first 31 months of data to forecast returns over the 32nd month. We will expand our regression
   window until we reach 60 months of data, after which we will always use the past 60 months of data to forecast returns over the next month.
3. Our simple model constrained the explanatory variables to be the same in each market. An obvious extension would be to allow different variables in different markets based on how well they forecast returns in those markets (and accounting for colinearities in some markets). 

### 18.2.2 Building Optimal Portfolios

1. Whereas active or residual asset returns exhibit relatively low correlations, asset-class excess returns exhibit high correlations.

2. We could handle this problem by using expected active or residual returns relative to an asset allocation benchmark

3.  refining these “raw” expected returns $\hat{r}$.

   $E\{r | \hat{r}\}=E\{r\}+\operatorname{Cov}\{r, \hat{r}\} \cdot \operatorname{Var}^{-1}\{\hat{r}\} \cdot(\hat{r}-E\{\hat{r}\})$

   1. Where $E\{r | \hat{r}\}$ is the refined expected return conditional on the forecast $\hat{r}$
   2. This can be simplified to  $E\{r | \hat{r}\}=E\{r\}+\mathrm{IC} \cdot \mathrm{STD}\{r\} \cdot$ Score

4. Where do we find the consensus expected excess returns?

   1. $E\{r\}=\beta \cdot f_{B}$

      Where $\beta$ is the beta of the asset class relative to the benchmark and $f_B$ is the consensus expected return to the benchmark

## 18.3 International Consensus Expected Returns

### 18.3.1 An Aside: Currency Semantics

1. Currency has a double meaning: It can be either a numeraire of perspective or an asset. It is this double nature that gives a theological aspect to that old conundrum: “Is currency an asset?” We will maintain that short-term, default-free, interest-bearing bills held in foreign countries are indeed assets.

### 18.2.3 Analyzing OOS Portfolio Performance

1. A more detailed performance analysis would also look at turnover, performance in up markets versus down markets (defined by the benchmark or the numeraire market), the number of up and down months, and which particular markets contributed the most to the outperformance. Performance dominated by one
   particular market would be a worrisome sign.
2. 





