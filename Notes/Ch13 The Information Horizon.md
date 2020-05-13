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

**Ch13 The Information Horizon 347 - 374**  

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

## 11.1 Introduction

1. Highlights:
   1. Information analysis is a two-step process
   2. Step 1 is to turn information into portfolio
   3. Step 2 is to analyze the performance of those portfolios
   4. Event studies provide analysis when information arrives episodically

## 11.2 Information and Active Management

1. _alpha_, or residual return: beta-adjusted return relative to a benchmark.
2. Information classification
   1. Primary or processed
      1. most basic form information
   2. Judgmental or importial
      1. significant human input, irreproducible
   3. Ordinal or cardinal
      1. classify assets into groups
   4. historical, contemporary, or forecast

## 11.3 Information Analysis

1. Two steps
   1. Turn predictions into portfolios
   2. Evaluate the performance of those portfolios

## 11.4 Step1: Information into Portfolios

1. Six possible ways
   1. With buy and sell recommendations, we could equal-( or value-) weight the buy group and the sell group
   2. With scores, we can build a portfolio for each score by equal- (or value-) weight within each score category
   3. Elaboration of procedure 1: weight the stocks in each group by how far their alpha exceeds the average
   4. Elaboration of procedure 2: weight the stocks in each group by how far their alpha exceeds the average
   5.  With any numerical score, we can build a factor portfolio that bets on the prediction and does not make a market bet. The factor portfolio consists of a long portfolio and a short portfolio with equal value and equal beta. However, the long portfolio will have a unit bet on the prediction, relative to the short portfolio, also, it will track the short portfolio as closely as possible.
   6. Elaboration of procedure 5: we can control the portfolios to match a set of prespecified control variables, like industry, sector, or small-capitalization stock exposures. 
2. Based on the controlled experiment, procedure 5 and 6 are usually the best approach for analyzing the information contained in any numerical scores.

## 11.5 Step 2 : Performance Evaluation

1. Cumulative return and some basic mean and std statistics

### 11.5.1 t statistics, information ratios, and information coefficients

1. regression analysis on the portfolio returns, regressing the excess portfolio returns against the excess benchmark returns, to separate the porfolio return into two components, one benchmark-relateed and the other non-benchmark-related:

   $r(t)=\alpha+\beta \cdot r_{B}(t)+\epsilon(t)$    (12.1)

   1. t-statistic for alpha is : $t-$ stat $=\frac{\alpha}{\operatorname{SE}(\alpha)}$

2. Information ratio is the ratio of annual alpha to its annual risk. It captures the risk-reward trade-off of the strategy and the manager’s value added.

3. $\mathrm{IR} \approx \frac{t-\mathrm{stat}}{\sqrt{T}}$

   1. if we observe returns over a period of T years. The relationship becomes more exact as the number of obervations increases

4. The distinction between the t statistic and the information ratio arises because we define value added based on risk over a particular horizon, in this case 1 year.

5. Information coefficient: correlation between our data and realized alphas.

   1. IC = 0  if data item is all noise and no signal

6. $\mathrm{IR} \approx \mathrm{IC} \cdot \sqrt{\mathrm{BR}}$

### 11.5.2 Advanced Topics in Performance Analysis

1. Portfolio Turnover
2. more detailed aspects related strategies

## 11.6 Event Studies

1. Three types of variables play a role in event studies:
   1. description of the event
   2. asset returns after the event
      1. must avoid confounding calendar time with the time measured relative to the event
      2. usually use asset residual returns after the event
   3. conditioning variables from before the event
      1. eg. surprise in the previous quarter, predecessor’s fate : retired, fired or departed?, company leverage

### 11.6.1 How to do an event study

1. $n = 1,\cdots, N$ events, residual returns cumulated from period 1 to period j following each event, $\theta_{n}(1,j)$, the residual risk estimate over the period $w_n(1,j)$; and conditioning variables $X_{nk}$, where $k = 1\cdots K$ indexes the different conditioning variables for each event n.

2. Regression

   $\frac{\theta_{n}(1, j)}{\omega_{n}(1, j)}=b_{0}(1, j)+\sum_{k} X_{n k} \cdot b_{k}(1, j)+\epsilon_{n}(1, j)$  (12.5)

   We can also analyze performance in the second week

   $\frac{\theta_{n}(6,10)}{\omega_{n}(6,10)}=b_{0}(6,10)+\sum X_{n k} \cdot b_{k}(6,10)+\epsilon_{n}(6,10)$   (12.6)

   The dependent variable has ex ante mean 0 and std 1, and the in-sample estimate of the IC of the signal is $\sqrt{R^2}$ from the regression

### 11.6.2 From Event Study to Alpha

1. The forecast alpha over the next $j$ periods is

   $\alpha_{n}(1, j)=\omega_{n}(1, j) \cdot\left[b_{0}(1, j)+\sum_{k} X_{n k} \cdot b_{k}(1, j)\right]$   (12.7)

   If the event occurred $j_1$ periods earlier, the forecast alpha is 

   $\alpha_{n}(1, j)=\omega_{n}(1, j) \cdot\left[b_{0}\left(j_{1}, j+j_{1}\right)+\sum_{k} X_{n k} \cdot b_{k}\left(j_{1}, j+j_{1}\right)\right]$   (12.8)

   1. it is consistent with volatility * IC * Score

### 11.6.3 Relationship to CS studies

## 11.7 The Pitfalls of information analysis

### 11.7.1 Data Mining is Easy

1. it turns out to be surprisingly easy to search through historical data and find patterns that don’t really exist

### 11.7.2 Investment Research

1. Four guidelines can help keep information analysis from turing into data mining:
   1. Intuition
      1. Intuition must guide the search for information before the backtest begins.
   2. Restraint
      1. After 20 tests of worthless information, 1 should look significant at the 95 percent confidence level.
   3. Sensibleness
      1. The information that deserves most scrutiny is that which appears to perform too well. 
      2. Only about 10 percent of observed realized information ratios lie above 1
   4. Out-of-sample testing

























