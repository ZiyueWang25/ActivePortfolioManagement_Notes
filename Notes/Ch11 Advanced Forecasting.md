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

Ch8 Valuation in Theory 199 - 224 

Ch9 Valuation in Practice 225 - 257

__Part 3 Information Processing__

Ch10 Forecasting Basics  261 - 293  1.5h

**Ch11 Advanced Forecasting** 295 - 314  1.5h

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

## 11.1 Introduction

1. Highlights:
   1. single-asset methodology also applies to multiple assets
   2. A complication occurs when we have cross-sectional and not time series scores. In many cases, we need not multiply cross-sectional scores by volatility
   3. If you have information and you forecast some factor returns, do not set other factor forecasts to 0
   4. Uncertainty in the IC will lead to shrinkage in the alpha

## 11.2 Multiple Assets

1. $E\{\mathbf{r} | \mathbf{g}\}=E\{\mathbf{r}\}+\operatorname{Cov}\{\mathbf{r} \mathbf{g}\} \cdot \operatorname{Var}^{-1}\{\mathbf{g}\} \cdot(\mathbf{g}-E\{\mathbf{g}\})$   (11.1)
   1. $\mathbf{r}$ is a length N vector and $\mathbf{g}$ is length K. K/N measures the number of signals per asset
2. $\phi_{n}=\omega_{n} \cdot I C \cdot z_{\mathrm{T} S, n} $  (11.2)
   1. assuming the signal has the same IC across all assets
   2. “TS” to explicitly label the score as a time series score. $Z_{TS,n}$ has mean 0 and std 1. 
3. However, we do not have N time series scores; rather, we can calculate one set of cross-sectional scores. It has mean 0 and std 1 across N stocks at one time. $Z_{CS,n}$

## 11.3 Cross-sectional scores

1. Time series score $z_{\mathrm{TS}, n}(t)=\frac{g_{n}(t)-E_{\mathrm{TS}}\left\{g_{n}\right\}}{\operatorname{Std}_{\mathrm{TS}}\left\{g_{n}\right\}}$
2. cross-sectional score $z_{\mathrm{CS}, n}(t)=\frac{g_{n}(t)-E_{\mathrm{CS}}\left\{g_{n}(t)\right\}}{\operatorname{Std}_{\mathrm{CS}}\left\{g_{n}(t)\right\}}$
3. How to move from CS score to TS score ?

### 11.3.1 Case 1: Identical Time Series Signal Volatilities

1. assume $\operatorname{Std}_{\mathrm{TS}}\left\{g_{n}\right\}=c_{1}$, all TS means are 0.
   1. Where $c_1$ is independent of $n$
2. $z_{\mathrm{TS}, n}=\frac{g_{n}}{\mathrm{Std}_{\mathrm{TS}}\left\{g_{n}\right\}}=\frac{g_{n}}{c_{1}}=\frac{g_{n}}{\operatorname{Std}_{\mathrm{CS}}\left\{g_{n}\right\}}$
   $\alpha_{n}=\omega_{n} \cdot \mathrm{IC} \cdot z_{\mathrm{CS}, n}$

### 11.3.2 Case 2: Time Series Signal Volatilities Proportional to Asset Volatilities

1. assume TS std depend on asset volatilities:

   1. $\operatorname{Std}_{\mathrm{TS}}\left\{g_{n}\right\}=c_{2} \cdot \omega_{n}$

2. estimate $c_2$ by  $c_{2}=\operatorname{Std}_{\mathrm{TS}}\left\{\frac{g_{n}}{\omega_{n}}\right\}$

3. assume forecasts are uncorrelated across assets:

   1. $c_{2}=\operatorname{Std}_{\mathrm{CS}}\left\{\frac{g_{n}}{\omega_{n}}\right\}$

4. So the _refined_ forecast is 

   $\phi_{n}=\omega_{n} \cdot \mathrm{IC} \cdot\left(\frac{g_{n}}{c_{2} \cdot \omega_{n}}\right)$
   $\phi_{n}=\mathrm{IC} \cdot\left(\frac{g_{n}}{\operatorname{Std}_{\mathrm{CS}}\left\{\frac{g_{n}}{\omega_{n}}\right\}}\right)$

5. To write this explicitly in terms of CS scores

   $\phi_{n}=\mathrm{IC} \cdot\left(\frac{\operatorname{Std}_{\mathrm{CS}}\left\{g_{n}\right\}}{\operatorname{Std}_{\mathrm{CS}}\left\{\frac{g_{n}}{\omega_{n}}\right\}}\right) \cdot\left(\frac{g_{n}}{\operatorname{Std}_{\mathrm{CS}}\left\{g_{n}\right\}}\right)$

   1. The second term is just a number, independent of n, we will call it $c_g$, so

      $\phi_{n}=\mathrm{IC} \cdot c_{g} \cdot z_{\mathrm{CS}, n}$  **(11.14)**

   2. forecasts still equal volatility * IC * score, but this is proportional to IC * cross-sectional score. The constant of proportionality $c_g$ can vary by signal

### 11.3.3 Empirical Evidence

Do not understand the table 11.2

## 11.4 Why not forecast CS alphas direcly?

1. $\phi_{n}=\mathrm{IC} \cdot \mathrm{Std}_{\mathrm{CS}}\left\{\theta_{n}\right\} \cdot z_{\mathrm{CS}, n} $  (11.16)
   1. for practical purposes, it is equivalent to **(11.14)**
2. We need to know what we can consistently forecast over time.

## 11.5 Multiple forecasts for each of N stocks

1. each information source j has an information coefficient vector $\mathbf{IC}_j$. The elements of $\mathbf{IC}_j$ describe the information coefficient asset by asset. For each information source, a correlation matrix $\mathbf{\rho}_j$ describes the signal correlations across assets

   $\mathrm{IC}_{j}(n)=\mathrm{IC}_{j}$
   $\boldsymbol{\rho}_{j}=\boldsymbol{\rho}$

   1. Information source j exhibit the same information coefficient for all assets
   2. The correlation of its signal across assets matches the correlation of every other information source’s signal across assets

## 11.6 Factor forecasts

1. Using the APT

   $E\{\mathbf{r}\}=\mathbf{X} \cdot \mathbf{m}$

   Where $\mathbf{r}=\mathbf{X} \cdot \mathbf{b}+\mathbf{u}$ and $\mathbf{m}=E\{\mathbf{b}\}$

2. some factor generate consistent returns but some require timing, i.e. their returns vary from pos to neg

3. Suppose we have a signal $g_1$ to forecast $b_1$, what should expect it for other factors? Use the basic forecasting formula

   $E\left\{b_{j} | g_{1}\right\}=E\left\{b_{j}\right\}+\operatorname{Cov}\left\{b_{j}, g_{1}\right\} \cdot \operatorname{Var}^{-1}\left\{g_{1}\right\} \cdot\left(g_{1}-E\left\{g_{1}\right\}\right)$

   1. Assuming the $g_1$ contains some information about $b_1$, plus noise:

      $g_{1}=\mathrm{IC}^{2} \cdot b_{1}+\mathrm{IC} \cdot \sqrt{1-\mathrm{IC}^{2}} \cdot \omega_{1} \cdot \mathrm{Z}$

   2. In this case, $\begin{aligned} \operatorname{Cov}\left\{b_{j ; g}\right\} &=\mathrm{IC}^{2} \cdot \operatorname{Cov}\left\{b_{j}, b_{1}\right\} \\ &=\mathrm{IC}^{2} \cdot \rho_{1 j} \cdot \omega_{j} \cdot \omega_{1} \end{aligned}$

   3. Substituting it back to equation and assume that $E[b_j] = 0$, then

      $\begin{aligned} E\left\{b_{j} | g_{1}\right\} &=\mathrm{IC} \cdot \rho_{1 j} \cdot \omega_{j} \cdot\left(\frac{g_{1}-E\left\{g_{1}\right\}}{\mathrm{Std}\left\{g_{1}\right\}}\right) \\ &=\mathrm{IC} \cdot \rho_{1 j} \cdot \omega_{j} \cdot z_{1} \end{aligned}$

   4. So we should not set $E\left\{b_{j} | g_{1}\right\}=0$ if we forecast $E\left\{b_{1} | g_{1}\right\} \neq 0$

## 11.7 Uncertain Information Coefficients

1. OLS method

   1. $\theta(t)=a+b \cdot g(t)+\epsilon_{\theta}(t) $  **(11.26)**

      1. assume $\theta(t)$ and $g(t)$ both have mean 0
      2. So $a=0$
         $b=\frac{\operatorname{Cov}\{\theta, g\}}{\operatorname{Var}\{g\}}=\frac{\sum_{t=1}^{T} \theta(t) \cdot g(t)}{\sum_{t=1}^{T} g^{2}(t)}$

   2. We can handle uncertainty in the estimated IC by adding a prior, $\hat b$ to the regression (11.26). We now have

      $\left[\begin{array}{c}\theta(1) \\ \vdots \\ \theta(T) \\ \hat{b}\end{array}\right]=\left[\begin{array}{c}g(1) \\ \vdots \\ g(T) \\ 1\end{array}\right] \cdot b^{\prime}+\left[\begin{array}{c}\epsilon_{\theta}(1) \\ \vdots \\ \epsilon_{\theta}(T) \\ \epsilon_{b}\end{array}\right]$     (11.29)

      1. We weight the observations of $\theta(t)$ by $\frac{1}{\omega_\theta^2}$ and the prior by $\frac{1}{\omega_b^2}$, where $\omega_\theta$ and $\omega_b$ is the std

   3. Then it corresponds to a maximum likelihood analysis, solving the regression for adjusted $b'$ leads to

      $b^{\prime}=\frac{\left(1 / \omega_{\theta}^{2}\right) \cdot \sum_{t=1}^{T} \theta(t) \cdot g(t)+\left(\hat{b} / \omega_{b}^{2}\right)}{\left(1 / \omega_{\theta}^{2}\right) \cdot \sum_{t=1}^{T} g^{2}(t)+\left(1 / \omega_{b}^{2}\right)}$

      

2. we can simplify it to $b^{\prime} \approx\left(\frac{1}{1+\left[\frac{1}{\left(T \cdot \mathrm{IC}^{2}\right)}\right]}\right) \cdot b$

   1. large number of T or high IC can lead the prior to naive estimate b. 

# Problems





