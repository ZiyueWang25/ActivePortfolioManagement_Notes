# Study Notes

### Learning Plan

April 30 - May 30, 31 days

__Part 1 Foundations__

Ch2 Consensus Expected Returns: The CAMP   11- 40  3.5h

Ch3 Risk  41 - 85  3h

**Ch4 Exceptional Return, Benchmarks, and Value Added  87 - 108** 2.5h

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

## 4.1 Introduction

1. Consensus forecasts + risk control + accurate forecasts of expected return
2. Key results:
   1. the components of expected return are defined. Exceptional expected return is the difference between our forecasts and the consensus
   2. Benchmark portfolios are a standard for the active manager
   3. Active Management value-added is expected exceptional return less a penalty for active variance.
   4. management of total risk and return  is distinct from management of active risk and return
   5. Benchmark timing decisions are distinct from stock selection decisions.

## 4.2 Benchmarks

1. _market_ -> _benchmark_, also known as _bogey_ and _normal_ portfolio
2. pros:
   1. allows investment managers to specialize and concentrate their expertise on a smaller collection of assets
   2. focuses the manager’s attention on performance relative to the benchmark

### 4.2.1 New Terminology

1. redefine beta: $\mathbf{\beta}_{n}=\frac{\operatorname{Cov}\left\{r_{n} r_{B}\right\}}{\operatorname{Var}\left\{r_{B}\right\}}$

   1. not w.r.t. _the market_ but to _benchmark_

2. _active position_: $\mathbf{h}_{P A}=\mathbf{h}_{P}-\mathbf{h}_{B}$

3. active cash holding: Active cash $=\mathbf{h}_{P}(0)-\mathbf{h}_{B}(0)=-\mathbf{e} \cdot \mathbf{h}_{P A}$

4. _active variance_: variance of the active position

   $\begin{aligned} \psi_{P}^{2} &=\mathbf{h}_{P A}^{T} \cdot \mathbf{V} \cdot \mathbf{h}_{P A} \\ &=\sigma_{P}^{2}+\sigma_{B}^{2}-2 \cdot \sigma_{P, B} \end{aligned}$

   1. use beta, we can rewrite it as 

      $\psi_{P}^{2}=\beta_{P A}^{2} \cdot \sigma_{B}^{2}+\omega_{P}^{2}$

      Where $\beta_{PA} = \beta_P -1$ and $\omega_P$ is the residual risk $\operatorname{Var}\left\{\theta_{P}\right\} \equiv \omega_{P}^{2}$

## 4.3 Components of expected return

1. components:
   1. risk free component (the time premium)
   2. benchmark component (the risk premium)
   3. benchmark timing component (exceptional benchmark return)
   4. alpha (expected residual return)
2. $E\left\{R_{n}\right\}=1+i_{F}+\beta_{n} \cdot \mu_{B}+\beta_{n} \cdot \Delta f_{B}+\alpha_{n}$
   1. $R_n$ is the total return on asset n

### 4.3.1 The Time Premium $i_F$

- compensation for time

### 4.3.2 Time Risk Premium $\beta_n \cdot \mu_B $

1. From CAPM
2. expected excess return on the benchmark $\mu_B$ is usually estimated by analysts as a very long run average
3. A number between 3 and 7 % per annum is reasonable for most equity markets
4. low-beta -> low risk premiums

###  4.3.3 Exceptional Benchmark Return $\beta_n \cdot \Delta f_B$

1. The $\mu_B$ is based on very long run considerations, while $\Delta f_B$ is based on next year (quarter, or month)

### 4.3.4 Alpha $\alpha_n$

1. It is the expected residual return $\alpha_{n}=E\left\{\theta_{n}\right\}$



3. Combination of these components:
   1. _Consensus Expected Excess Return_: $\beta_n \cdot \mu_B$
   2. _Expected Excess Return_: $f_{n}=\beta_{n} \cdot \mu_{B}+\beta_{n} \cdot \Delta f_{B}+\alpha_{n}$
   3. _Exceptional Expected Return_: $\beta_{n} \cdot \Delta f_{B}+\alpha_{n}$
      1. key to active management
      2. $\beta_{n} \cdot \Delta f_{B},$ measures benchmark timing
      3. $\alpha_{n},$ measures stock selection.
4. Portfolio Level:
   1. Expected Excess Return: $f_{B}=\sum h_{B}(n) \cdot E\left\{R_{n}-\left(1+i_{F}\right)\right\}$
   2. Exceptional benchmark return : $\Delta f_{B}=f_{B}-\mu_{B}$

## 4.4 Management of total risk and return

1.  expected excess return $f_{n}=\beta_{n} \cdot f_{B}+\alpha_{n}$
   1. $f_B$ is the forecast expected excess return for the benchmark
   2. $\beta_n$ is stock n’s beta, and $\alpha_n$ is stock n’s forecast alpha
2. Differ with the consensus estimate $\mu_B$ and $\alpha_n$ differs from 0

### 4.4.1 The Total Return / Total Risk Trade-Off

1. _expected utility_ $U[P]=f_{P}-\lambda_{T} \cdot \sigma_{P}^{2}$

   1. where $f_P$ is the expected excess return, $\lambda_T \cdot \sigma_P^2$ is a penalty for risk, $\lambda_T$ measures _aversion to total risk_, where total risk includes systematic risk and residual risk (from asset selection)
   2. Some people choose $\tau = \frac{1}{\lambda}$ or $\frac{\lambda}{2}$ for convenience

2. a scientific way to get a reasonable value for $\lambda_T$

   1. $\lambda_{T}=\frac{\mu_{B}}{2 \cdot \sigma_{B}^{2}}$

3. beta of P is $\beta_{P}=\frac{f_{B}}{2 \cdot \lambda_{T} \cdot \sigma_{B}^{2}}$

   1. Using $\lambda_T $ and $\Delta f_{B} \equiv f_{B}-\mu_{B}$ to be the forecast of _exceptional_ benchmark return, the beta of portfolio P becomes

      $\beta_{p}=1+\frac{\Delta f_{B}}{\mu_{B}}$

4. The active beta $\beta_{PA} = \beta_P - 1$, is the ratio of our forecast for benchmark exceptional return to the consensus expected excess return of the benchmark $\mu_B $ 

5. Problem: This expected utility criterion will typically lead to portfolios that are too aggressive for institutional investment managers

   1. This is not due to the extravagant nature of the expected returns. The problem is not the total portfolio risk $\sigma_{p}$, it is the residual risk $\omega_{p}$
   2. **In total risk/return analysis, small levels of information lead to very high levels of residual risk**

6. We need to focus on the __active component of return__ and look at __active risk/return trade-offs__

## 4.5 Focus on Value-added

1. investment managers and pension plan sponsors are much more averse to the risk of deviation from the benchmark than they are averse to the risk of the benchmark

### 4.5.1 Business Risk and Investment Risk

1. pension funds bears the benchmark component of the risk; while the active manager bears the responsibility for the residual risk
   1. The active manager is, in fact, responsible for active risk. In the typical case of $\beta_{p}=1$ residual risk equals active risk. If $\beta_{p} \neq 1,$ the manager is responsible for both residual risk and active systematic risk.
2. Split risk and return into three parts
   1. _Intrinsic_, $f_B - \lambda_T \cdot \sigma_B^2$ : risk and return of the benchmark. it is not under the manager’s control. $\lambda_T$ is aversion to total risk
   2. _cross effect_, net to zero $\beta_{PA}(\mu_B - 2\lambda_T\sigma_B^2)$
   3. _Benchmark Timing_, $\beta_{PA} \cdot \Delta f_B - \lambda_{BT} \cdot \beta_{PA}^2 \cdot \sigma^2_B$. contribution from timing the benchmark. It is governed by __the manager’s active beta__. $\lambda_{BT}$ is aversion to benchmark timing
   4. _Residual. Stock Selection_, $\alpha_P - \lambda_R \cdot \omega_P^2$. due to the manager’s residual position. $\lambda_R$ is aversion to residual risk.
3. _Value added_:  Timing + Residual (4.15)
   1. $\mathrm{VA}=\left\{\beta_{P A} \cdot \Delta f_{B}-\lambda_{B T} \cdot \beta_{P A}^{2} \cdot \sigma_{B}^{2}\right\}+\left\{\alpha_{P}-\lambda_{R} \cdot \omega_{P}^{2}\right\}$

## 4.6 Benchmark Timing

1. Benchmark timing is the choice of an appropriate active beta,  period by period

2. The optimal level of _active_ beta is 

   $\beta_{P A}=\frac{\Delta f_{B}}{2 \cdot \lambda_{B T} \cdot \sigma_{B}^{2}}$

## 4.7 Active vs. Residual Return

1. Residual Return and Risk

   $\theta_{P}=r_{P}-\beta_{P} \cdot r_{B}$
   $\omega_{P}=\operatorname{Std}\left\{\theta_{P}\right\}$

2. active return and risk

   $\begin{aligned} r_{P A} &=r_{P}-r_{B}=\theta_{P}+\beta_{P A} \cdot r_{B} \\ \psi_{P}=& \operatorname{Std}\left\{r_{P A}\right\}=\sqrt{\omega_{P}^{2}+\beta_{P A}^{2} \cdot \sigma_{B}^{2}} \end{aligned}$

3. As long as the manager avoids benchmark timing and sets $\beta_P = 1$, active and residual returns (and risks) are identical

4. If $\beta_P \ne 1$, the active return is the sum of the residual return and the benchmark timing return

# Problems

1. $i_F = 0.06, \mu_B = 0.06, \Delta f_B = 0.065, R_n = 0.15, \beta_n = 1.07$

   1. Time premium: $i_F$
   2. Risk premium: $\beta_n \cdot \mu_B$
   3. Exceptional benchmark return: $\beta_n \cdot \Delta f_B$
   4. Alpha: $\alpha_n = R_n - i_F - \beta_n \mu_B - \beta_n \cdot \Delta f_B $
   5. Consensus expected return: $\beta_n \cdot \mu_B $
   6. Expected Excess Return: $f_{n}=\beta_{n} \cdot \mu_{B}+\beta_{n} \cdot \Delta f_{B}+\alpha_{n}$
   7. Exceptional expected return:  $\beta_{n} \cdot \Delta f_{B}+\alpha_{n}$
   8. Consensus Expected Return = Expected Excess Return + Exceptional Expected return

2. ?

3. residual risk = $\sqrt{0.21^2 - 0.2^2} = 0.064$

   1. same active risk
   2. ?

4. $\alpha_1 = f_1 - \beta_1f_B = 0.04$, $\alpha_2 = f_2 - \beta_2 f_B = 0.1$

   $\omega_1^2 = \sigma_1^2 - \sigma_B^2 = 0.000885$,  $\omega_2^2 = \sigma_2^2 - \sigma_B^2 = 0.0225$

   $f_1 - \lambda_T \sigma_1^2 = 0.09848 <  0.1581= f_2 - \lambda_T \sigma_2^2$, so A will choose 2

   using the same method , B will choose 1

5. ?













