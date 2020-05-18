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

## 13.1 Introduction

1. Time dimension to information
2. highlights
   1. information horizon should be defined as the half-life of the information's forecasting ability
   2. A strategy's horizon is an intrinsic property. Time averages or time differences can change performance, but they will not change the horizon
   3. Lagged signals or scores and past returns can improve investment performance

# 13.2 MacroAnalysis of The Information Horizon

1. Half-life is robust characteristic but have little or no effect on the strategy's half-life
2. The ability to add value is proportional to the square of the information ratio
3. given a decay rate $\tau$ and a correlation $\rho$, the optimal weight is
   1. $w_{\mathrm{Now}}^{*}=\frac{\gamma+x}{\gamma+1}$  where $x \equiv \frac{1-\gamma}{1-\rho}$
4. Combing the old and new strategy can improve the IR

# 13.3 MicroAnalysis of the Information Horizon

1. $\alpha(\Delta t)=(\sigma \cdot \sqrt{\Delta t}) \cdot \operatorname{IC}(\Delta t) \cdot s(0)$
   1. Where $IC(\Delta t)$ is the correlation of the score with the return over the period $\{ 0,\Delta t\}$. Given a score $s(0)$,  $\alpha(\Delta t) = E(r(0,\Delta t)|s(0))$
2. Information ratio here:
   1. $\mathrm{IR}^{2}=[\mathrm{IC}(\Delta t)]^{2} \cdot\left(\frac{1}{\Delta t}\right)$
      1. We measure the breadth BR as simply the inverse of the period $1/\Delta t$
      2. Here is the tradeoff between arrival rate, captured by $\Delta t$ and the accuracy, captured by $IC(\Delta t)$

## 13.4 Two-Period Shelf Life















