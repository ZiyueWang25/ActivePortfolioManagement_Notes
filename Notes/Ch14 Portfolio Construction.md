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

Ch13 The Information Horizon 347 - 374  Mon

__Part 4 Implementation__

**Ch14 Portfolio Construction 377 - 418 0519**  Tue

Ch15 Long/Short Investing 419 - 443 0520 Wed

Ch16 Transaction Costs, Turnover, and Trading 445 - 475 0521 Thur

Ch17 Performance Analysis 477 - 515 0522 Fri

Ch18 Asset Allocation 517 - 539 0523 Sat

Ch19 Benchmark Timing  541 - 558  0524 Sun

Ch20 The Historical Record for Active Management 559 - 571 0525 Mon

Ch21 Open Questions 573 - 576

Ch22 Summary 577 - 580

__Appendix C: Return and Statistics Basics__

## 14.1 Introduction

1. inputs: 
   1. the current portfolio, alphas, covariance estimates, transactions cost estimates, and an active risk aversion
2. Key ideas:
   1. Implementation schemes are, in part , safeguards against poor research
   2. with alpha analysis, the alphas can be adjusted so that they are in line with the manager’s desires for risk control and anticipated sources of value added
   3. portfolio construction techniques include screening, stratified sampling, linear programming, and quadratic programming. Given sufficiently accurate risk estimates, the quadratic programming technique most consistently achieves high value added.
   4. For most active institutional portfolio mangers, building portfolios using alternative risk measure greatly increase the effort without greatly affecting the result.
   5. managers running separate accounts for multiple clients can control dispersion, but cannot eliminate it.

## 14.2 Alphas and portfolio construction

1. We can always replace a very complicated portfolio construction procedure that leads to active holdings $\boldsymbol{h}^*_{PA}$, active risk $\psi_P^*$ and an ex ante information ratio IR with a direct unconstrained mean/variance optimization
   $$
   \alpha' = (\frac{IR}{\psi_P^*})Vh_{PA}^*
   \\
   \lambda_A' = \frac{IR}{2\psi_P^*}
   $$


## 14.3 Alpha Analysis

### 14.3.1 Scale the Alpha

1. $\alpha = \text{volatility} \times IC \times score$ 
2. The alphas should have mean 0 and standard deviation, or _scale_, of $\text{Std}\{\alpha\} \sim \text{volatility} \times \text{IC}$

### 14.3.2 Trim Alpha Outliers

1. some of the outliers may depend upon questionable data and should be ignored, while others may appear genuine
2. force them into a normal distribution with benchmark alpha equal to 0 and the required scale factor

### 14.3.3 Neutralization

1. Benchmark neutralization means that the benchmark has 0 alpha

### 14.3.4 Benchmark - and Cash-Neutral Alphas

1. Cash-Neutral: the alphas will not lead to any active cash position

### 14.3.5 Risk-Factor-Neutral Alphas

1. The multiple-factor approach to portfolio analysis separates return
   along several dimensions: A manager can identify each of those dimensions as either a source of risk or a source of value added.
2. By this definition, the manager does not have any ability to forecast the risk factors. Therefore, he or she should neutralize the alphas against the risk factors. The neutralized alphas will include only information on the factors the manager can forecast, along with specific asset information. Once neutralized, the alphas of the risk factors will be 0.
3. example: making alphas industry-neutral: calculate the capitalization-weighted alpha for each industry, then subtract the industry average alpha from each alpha in that industry

## 14.4 Transaction Costs

1. The annualized transactions cost is the round-trip cost divided by the holdings period in years

## 14.5 Practical Details

1. choose a risk aversion parameter: $\lambda_A = \frac{IR}{2\times \psi_P}$

## 14.6 Portfolio Revisions

1. If a manager knows how to make the correct trade-off between expected active return, active risk, and transactions costs, frequent revision will not present a problem.
2. But if not, then the manager may resort to less frequent revision as a safeguard

## 14.7 Techniques for portfolio construction

1. Applications:
   1. Screens
   2. Stratification
   3. Linear Programming
   4. Quadractic Programming
2. Criteria: high alpha, low active risk, and low transactions costs
   1. maximize $\alpha_p - \lambda_A \times \psi^2 - TC$ 

### 14.7.1 Screens

1. recipe:
   1. Rank the stock by alpha
   2. choose the first 50 stocks
   3. equal-weight the stocks
2. pros: simplicity
3. cons:
   1.  ignore all information in the alphas apart from the rankings. 
   2. Risk control is fragmentary at best

### 14.7.2 Stratification

1. splitting the list of followed stocks into categories
2. mimic the screening exercise within each category
3. It ensures the portfolio matches the benchmark along these important dimensions
4. pros: simple and robust
5. cons: ignores some information, risk control is rudimentary

### 14.7.3 Linear Programming

1. space-age stratification
2. it characterizes stocks along dimensions of risk, e.g. industry, size, volatility and beta
3. pros: takes all the information about alpha into account and controls risk by keeping the characteristics of the portfolio close to the characteristics of the benchmark
4. cons: 
   1. has difficulty produing portfolios with a prespecified number of stocks
   2. the risk-control characteristics should not work at cross purposes with the alphas. eg.  if the alphas tell you to shade the portfolio toward smaller stocks at some times and toward larger stocks at other times, you should not control risk on the size dimension.

## 14.7.4 Quadratic Programming

1. Quadratic programming (QP) is the ultimate10 in portfolio construction. The quadratic program explicitly considers each of the three elements in our figure of merit: alpha, risk, and transactions costs.
2. Two lessons:
   1. errors in the estimates of covariance lead to inefficient implementation.
   2. it is vital to have good estimates of covariance.

## 14.8 Tests of portfolio construction methods

1. QP approach clearly lead to consistently the highest ex post information ratios

## 14.9 Alternative to Mean/Variance Optimization

## 14.10 Dispersion

1. dispersion as the difference between the maximum return and minimum return for these separate account portfolios.























