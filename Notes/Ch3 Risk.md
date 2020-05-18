# Ch3 Risk

### Learning Plan

April 30 - May 30, 31 days

__Part 1 Foundations__

Ch2 Consensus Expected Returns: The CAMP   11- 40  3.5h

**Ch3 Risk  41 - 85** 

Ch4 Exceptional Return, Benchmarks, and Value Added  87 - 108

Ch5 Residual Risk and Return: The Information Ratio 109 - 145

Ch6 The Fundamental Law of Active Management 147 - 169

__Part 2 Expected Returns and Valuation__

Ch7 Expected Returns and the Arbitrage Pricing Theory 173 - 198

Ch8 Valuation in Theory 199 - 224

Ch9 Valuation in Practice 225 - 257

__Part 3 Information Processing__

Ch10 Forecasting Basics  261 - 293

Ch11 Advanced Forecasting 295 - 314

Ch12 Information Analysis 315 - 345

Ch13 The Information Horizon 347 - 374

__Part 4 Implementation__

Ch14 Portfolio Construction 377 - 418

Ch15 Long/Short Investing 419 - 443

Ch16 Transaction Costs, Turnover, and Trading 445 - 475

Ch17 Performance Analysis 477 - 515

Ch18 Asset Allocation 517 - 539

Ch19 Benchmark Timing  541 - 558

Ch20 The Historical Record for Active Management 559 - 571

Ch21 Open Questions 573 - 576

Ch22 Summary 577 - 580

__Appendix C: Return and Statistics Basics__

## 3.1 Introduction

1. Expected Return is the protagonist in the drama of active management. Risk is the antagonist
2. Important lessons:
   1. Risk is the standard deviation of return
   2. Risk don’t add
   3. Many Institutional investors care more about active and residual risk than about total risk
   4. active risk depends primarily on the size of the active position, not the size of the benchmark position
   5. the cost of risk is proportional to variance
   6. risk models identify the important sources of risk and separate risk into components

## 3.2 Defining Risk

1. a symmetric view of risk
   1. Institutional money managers are judged relative to a benchmark or relative to their peers
2. A flexible definition of risk
   1. we should apply both definition of risk to individual stocks and to portfolios
   2. time horizon flexibility
3. limit ourselves to a measure of risk that we can accurately forecast
   1. we want a measure of risk that we can build up from assets to portfolios 
4. The distribution of returns describes the probabilities of all possible outcomes
5. The _standard deviation_ (volatility) measures the spread of the distribution about its mean. it measures the uncertainty of the returns
6. Critics of the std:
   1. it measures the possibility of returns both above and below the mean, but most investors would define risk as involving small or negative returns. This has generated an alternative risk measure: _semivariance_, or _downside risk_ 
      1. Semivariance is defined in analogy to variance, but using only returns below the mean. If the returns are symmetric, then semivariance is $\frac{1}{2}$ variance.
         1. _target semivariance_: focuses on returns below a target, instead of just below the mean
      2. downside risk is the square root of the semivariance
         1. statistical properties are not well known
         2. it is computationally challenging for large portfolio construction problems
         3. **Aggregating semivariance from assets to portfolios** is extremely difficult to do well
         4. when the investment returns are reasonably symmetric, the downside risk are simply proportional to std or variance and so contain no additional information.
         5. When the return is not symmetric, it is hard to forecast downside risk. Return asymmetries are not stable over time and difficult to predict. Realzied downside risk may not be a good forecast of future downside risk.
         6. **we estimate it only half of the data, so we lose statistical accuracy.** This problem is accentuated for target semivariance,
7. _Shortfall probability_: closely related to an intuitive conception of what risk is. It is the probability that the return will lie below some target amount.
   1. Pros: intuitive
   2. Cons: 
      1. ambiguity, poor statistical understanding, difficulty of forecasting, and dependence on individual investor preferences.
      2. the difficulty of forecasting becomes higher when the shortfall target becomes lower.
8. _Value at Risk (VaR)_: similar to shortfall probability. But it converts the probability to an associated return. it shares the same pros and cons with _Shortfall probability_ 
9. How to define risk is different from how to report risk
   1. any method relying on the normal distribution would strongly motivate us to focus on std at the asset level, which we can aggregate to the portfolio lvel

## 3.3 Standard Deviation

1. it is universal, symmetric, flexible, and accurately forecastable.
2. the std is quote on a percent per year basis
3. it does _not_ have the portfolio property, i.e. it is not the weighted average of the standard deviation of the constituents. Instead, we need to consider the correlation between the returns
4. The whole is less than the sum of its parts
   1. The risk of an equally weighted portfolio with all pairs of stocks correlation $\rho$ is $\sigma_{P}=\sigma \cdot \sqrt{\frac{1+\rho \cdot(N-1)}{N}}$, if $N \rightarrow \infty$, then $\sigma_{P} \rightarrow \sigma \cdot \sqrt{\rho}$
5. Risks don’t add across stocks, and don’t add across time.
   1. variance will add across time if the returns in one interval of time are uncorrelated with the returns in other intervals of time.
      1. The correlation of returns across time (autocorrelation) is close to zero for most asset classes
6. Relative risk is important
   1. $\psi_{P}=\operatorname{Std}\left\{r_{P A}\right\}=\operatorname{Std}\left\{r_{p}-r_{B}\right\}$
      1. active risk $\psi_P$, it is also called the _tracking error_
7. active risk is proportional to the capitalization of the asset
8. residual risk: the risk of the return orthogonal to the systematic return
   1. $\omega_{P}=\sqrt{\sigma_{P}^{2}-\beta_{P}^{2} \cdot \sigma_{B}^{2}}$
      1. Where $\beta_{P}=\frac{\operatorname{Cov}\left\{r_{p}, r_{B}\right\}}{\operatorname{Var}\left\{r_{B}\right\}}$
9. Typical numbers:
   1. total risk : 25 ~ 40 %
   2. residual risk : 20 ~ 35 %
   3. beta: 0.8 ~ 1.35

## 3.4 Elementary Risk Models

1. $\mathbf{V}=\left[\begin{array}{cccc}\sigma_{1}^{2} & \sigma_{12} & \dots & \sigma_{1 N} \\ \sigma_{12} & \sigma_{2}^{2} \\ \vdots & & \ddots \\ \sigma_{1 N} & & & \sigma_{N}^{2}\end{array}\right]$

2. The goal of a risk model is to accurately and efficiently forecast the covariance matrix

3. Single-factor Diagonal model

   1. intellectual precursor to the CAPM  $r_{n}=\beta_{n} \cdot r_{M}+\theta_{n}$

      1. where $\beta_{n}$ is stock $n^{\prime}$ s beta and $\theta_{n}$ is stock $n$ 's residual return.

   2. it assumes the residual returns  $\theta_n$ are uncorrelated, so

      $\operatorname{Cov}\left\{r_{n}, r_{m}\right\}=\beta_{n} \cdot \beta_{m} \cdot \sigma_{M}^{2}$

      and

      $\sigma_{n}^{2}=\beta_{n}^{2} \cdot \sigma_{M}^{2}+\omega_{n}^{2}$

   3. However, residual returns are correlated. The market-weighted average of the residual returns is exactly 0:

      $\sum_{n} h_{M}(n) \cdot \theta_{n}=0$

      1. which means most residual correlation must be in general negative

4. all pairs of stocks have the same correlation model

   1. $\operatorname{Cov}\left\{r_{n}, r_{m}\right\}=\sigma_{n} \cdot \sigma_{m} \cdot \rho$
   2. it ignores the subtle linkage between stocks in similar industries and firms with common attributes

5. full covariance model based on historical returns

   1. is not robust nor reasonable
      1. merge/ spinoff 
   2. it requires $T \gt N$
      1. T period, N stocks
      2. TN observations, N(N+1)/2 independent estimates
      3. 2 observations for 1 estimate
      4. T has to be no smaller than N+1
   3. problems:
      1. Circumventing the $T>N$ restriction requires short time periods, one day or one week, while the forecast horizon of the manager is generally one quarter or one year.
      2. Historical risk cannot deal with the changing nature of a company. Mergers and spinoffs cause problems.
      3. There is selection bias, as takeovers, LBOs, and failed companies are omitted.
      4. **Sample bias will lead to some gross misestimates of covariance.** A 500-asset covariance matrix contains 125,250 independent numbers. If 5 percent of these are poor estimates, we have 6262 poor estimates.

## 3.5 Structural Risk Models

1. The multiple-factor risk factor model is based on the notion that the return of a stock can be explained by a collection of common factors + an idiosyncratic element that pertains to that particular stock
2. Four components: stock’s excess returns, the stock’s exposure to the factors, the attributed factor returns, and the specific returns
3. $r_{n}(t)=\sum_{k} X_{n, k}(t) \cdot b_{k}(t)+u_{n}(t)$   **(3.16)**
   1. $r_n(t)$ : excess return on stock n during the period from time t to time t+1
   2. $X_{n,k}(t)$ : exposure of asset n to factor k, estimated at time t. also called _factor loadings_. For industry factors, the exposure are either 0 or 1. For other common factors, the exposures are standardized so that the average exposure over all stocks is 0, and the standard deviation across stocks is 1
   3. $b_k(t)$: _factor return_ to factor k during t to t+1
   4. $u_n(t)$: _specific, or idiosyncratic return_ of stock n during t to t+1
4. Careful Parts:
   1. exposures are known at time t.
   2. asset return, factor return, and specific returns span the period from t to t+1
   3. the factors may or may not be the basic driving forces for security returns. In our view, they are merely dimensions along which to analyze risk.
5. Assumption: the specific returns are not correlated with the factor returns and are not correlated with each other. 
6. Risk Structure: $V_{n, m}=\sum_{k_{1},k_{2}=1}^{K} X_{n k_{1}} \cdot F_{k_{1} k_{2}} \cdot X_{m, k_{2}}+\Delta_{n, m}$  **(3.17)**
   1. $V_{n,m}$ : covariance of asset n with asset m.
   2. $X_{n,k_1}$: exposure of asset n to factor $k_1$
   3. $F_{k1,k2}$: covariance of factor $k_1$ with factor $k_2$
   4. $\Delta_{n,m}$ : specific covariance of asset n with m. Under the given assumption, it is 0 when n != m.

## 3.6 Choosing the factors

1. only one key constraint: **all factors must be a priori factors**, i.e. it must be known at the beginning of the period.
2. factors categories: response to external influences, cross-sectional comparisons of asset attributes, and purely internal or statistical factors.

### 3.6.1 Responses to External Influences

1. demonstrable link between outside economic forces and the equity markets
2. Factors include responses to return in the bond market (bond beta), unexpected changes in inflation (inflation surprise), changes in oil prices, changes in exchange rates, changes in industrial production, and so on.
3. It is sometimes called _macrofactors_
4. 3 defects:
   1. we must estimate the response coefficient through regression analysis or some similar technique. This leads to errors in the estimates, commonly called an _error in variables_ problem
   2. we base the estimate on behavior over a past period of generally 5 years and **it may not be an accurate description of the current situation**. These response coefficients can be nonstationary.
   3. Several of the macroeconomic data items are of poor quality, gathered by the government rather than observed in the market. This leads to inaccurate, delayed, and relatively infrequent observations

### 3.6.2 Cross-Sectional Comparisons

1. Fundamental
   1. dividend yield, earnings yield + analysts’ forecasts of future earnings per share
2. Market:
   1. volatility over a past period, return over a past period, option implied volatility, share turnover, etc.

### 3.6.3 Statistical Factors

1. _factor ex machina_
2. PCA, maximum likelihood analysis, expectations maximization analysis\
3. we usually avoid statistical factors, because
   1. hard to interpret
   2. is prone to discovering spurious correlations
   3. cannot capture factors whose exposures change over time



3. Choose the factor following the **3 criteria**
   1. incisive: distinguish returns
   2. intuitive: interpretable and recognizable dimensions of the market
   3.  interesting: explain some part of the performacne
4. Typical factors to choose: _industry factors_ and _risk indices_

## 3.7 Industry Factors

1. Industry groupings criteria:
   1. a reasonable number of companies in each industry
   2. a reasonable fraction of capitalization in each industry
   3. a reasonable accord with the conventions and mindset of investors in that market
2. The market itself has unit exposure in total to the industries.
3. Since large corporations can do business in several industries, we can extend the industry factors to account for membership in multiple industries.

## 3.8 Risk Indices

1. it measures the movements of stocks exposed to common investment themes
2. Risk indices fall into these broad categories:
   1. Volatility
   2. Momentum
   3. Size
   4. Liquidity
   5. Growth
   6. Value
   7. Earnings Volatility
   8. Financial Leverage
3. Each broad category can typically contain several specific measurements of the category. We call them _descriptors_
4. risk index exposures is a weighted exposures f the descriptors within the risk index
   1. choose weights that maximize the explanatory and predictive power of the model
   2. It can also improve the model robustness
5. how to quantify the exposures?
   1. rescale first $x_{\text {normalized }}=\frac{x_{\text {raw }}-\left\langle x_{\text {raw }}\right\rangle}{\operatorname{Std}\left[x_{\text {raw }}\right]}$
      1. Where $\lang x_{raw}\rang$ is the raw exposure value mean
      2. each risk index exposure has mean 0 and standard deviation 1. 
      3. facilitates the handling of outliers
6. Usage of Risk Models
   1. Portfolio risk analysis
   2. Forecast Total Risk/ Active Risk/ Residual Risk, beta, etc.

## 3.9 Structural Risk Model Covariance

## 3.10 The Uses of a risk model

1. present, future, and past

### 3.10.1 The Present: Current Portfolio Risk Analysis

1. Divide the risk
   1. market and residual components
   2. benchmark and active risk
   3. model risk and the specific risk
2. Marginal analysis: what assets are most and least diversifying in the portfolio, at the margin?
3. Passive managers want minimum tracking error
4. Active managers want to take on risk only long those dimensions where they believe they can outperform
5. Risk analysis can classify active bets into inherent bets, intentional bets, and incidental bets:
   1. _Inherent_: an active manager who is trying to outperform a benhmark must bear the benchmark risk, i.e. the volatility of the benchmark itself
      1. Beta
   2. _Intentional_: the stocks with the highest expected returns should provide the highest marginal contributions to risk
   3. _Incidental_: unintentional side effects of the manager’s active position.
6. Risk model will let us know the marginal impact on total, residual, or active risk of changes in portfolio exposures to factors or changes in stock holdings

### 3.10.2 The Future

Ch14 Portfolio Construction 

### 3.10.3 The Past

Ch 17 Performance Analysis

## 3.11 How well do risk models work?

1. we can forecast only std from historical data, and that portfolio-based forecasts of std surpass those historical estimates
2. Accurate risk forecasts should lead to few surprises, not zero surprises.

# Problems

How to answer question 4?

# Technical Appendix

Risk Model Details

- Basic Model
- Model Assumption
  - specific return is uncorrelated with factor return
  - specific return is uncorrelated with each other
- Stock Covariance Matrix
  - V = X F X^T + Delta
- Estimation of Factor Return
- Factor Covariance Matrix & Specific Risk
- Portfolio Risk
- Risk Attribution









