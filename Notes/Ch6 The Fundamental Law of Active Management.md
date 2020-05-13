# Study Notes

### Learning Plan

April 30 - May 30, 31 days

__Part 1 Foundations__

Ch2 Consensus Expected Returns: The CAMP   11- 40  3.5h

Ch3 Risk  41 - 85  3h

Ch4 Exceptional Return, Benchmarks, and Value Added  87 - 108 2.5h

Ch5 Residual Risk and Return: The Information Ratio 109 - 145  2h

**Ch6 The Fundamental Law of Active Management 147 - 169** 1.5h

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

## 6.1 Introduction

1. Major points:
   1. A strategy’s breadth is the number of independent, active decisions available per year
   2. The manager’s skill, measured by the information coefficient, is the correlation between forecasts and results
   3. The fundamental law of active management explains the information ratio in terms of breadth and skill
   4. the additivity of the fundamental law allows for an attribution of value added to different components of a strategy

## 6.2 The Fundamental Law

1. _breadth, BR_: the number of independent forecasts of exceptional return we make per year
2. _Information coefficient, IC_: the correlation of each forecast with the actual outcomes.
3. $\mathrm{IR}=\mathrm{IC} \cdot \sqrt{\mathrm{BR}}$
   1. this ignores the benefits of reducing risk that our forecasts provide
4. $\omega^{*}=\frac{\mathrm{IR}}{2 \lambda_{R}}=\frac{\mathrm{IC} \cdot \sqrt{\mathrm{BR}}}{2 \lambda_{R}}$
5. $\mathrm{VA}^{*}=\frac{\mathrm{IR}^{2}}{4 \lambda_{R}}=\frac{\mathrm{IC}^{2} \cdot \mathrm{BR}}{4 \lambda_{R}}$

## 6.3 Additivity

1. $\mathrm{IR}^{2}=\mathrm{BR}_{1} \cdot \mathrm{IC}_{1}^{2}+\mathrm{BR}_{2} \cdot \mathrm{IC}_{2}^{2}$
2. The additivity can also work along other dimensions, like information ratio from stock selection and market timing.
   1. international portfolio: different region
   2. across managers

## 6.4 Assumptions

1. The skill involved in forecasting each component, IC, is the same.
2. The forecast should be independent
   1. Regression analysis gives us the opportunity both to uncover consistent patterns and to remove them if we choose
   2. the greater the dependence between the two information sources, the lower the value of the incremental information
      1. $\mathrm{IC}(\mathrm{com})=\mathrm{IC} \cdot \sqrt{\frac{2}{1+\gamma}}$
         1. Where $\gamma$ is the correlation, and we assume each of the BR active bets has the same level of skill
3. the manager will accurately gauge the value of information and build portfolios that use that information in an optimal way
   1. this requires insight and humility, a desirable combination that is not usually found in one individual.

## 6.5 Not the law of large numbers

1. more breadth at the same skill level let us diversify the residual risk

## 6.6 Tests

1. The fundamental law is a guideline, not an operational tool

## 6.7 Investment Style

1. The law encourages managers to have an eclectic style

# Problems

1. $IR_A = 0.02 * \sqrt{250*4}=0.2\sqrt{10}$
   1. $IR_B = IC_B *\sqrt{4*4} = 4*IC_B$
   2. $IC_B = 0.05\sqrt{10}$
   3. $IR =\sqrt{ 0.04*10 + 0.0064*16} \approx 0.7$
2. $BR_{ind} = (\frac{IR}{IC})^2 = (\frac{1}{0.05})^2= 400$
   1. $BR_{all} = 500*12 = 6000$
   2. Alpha is highly correlated
3. ?



