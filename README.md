# Extrapolation Is an Assumption: Sharp Limits for Pass@k Forecasting

## Abstract

Repeated sampling can reveal capabilities and risks that are invisible in one language-model attempt, motivating forecasts of pass@$k$ from much smaller response banks. We ask what such data support without a parametric law for task difficulty. With $b$ attempts per task, the count distribution identifies exactly the first $b$ moments of the latent success-probability distribution. We prove that the worst-case diameter of pass@$k$'s identified set is exactly twice the best degree-$b$ uniform approximation error for $x^k$. A theorem of Newman and Rivlin then yields explicit binomial-tail bounds and a sharp extrapolation transition at $k\asymp b^2$. We extend the limit to finite task sets through a Hellinger modulus and to adaptive policies with a per-task cap. We also give two finite-sample confidence intervals: a global polynomial interval that attains the limiting worst-case diameter and a data-adaptive projection interval. At 128 tasks and 78 attempts per task, any honest 95% interval for population pass has expected-length lower bounds $0.276$ and $0.686$ for pass@1000 and pass@10000. In synthetic audits, narrow taskwise Beta intervals have zero coverage under seven nonparametric alternatives. Across 22 public response banks, model-free intervals include every 10,000-response reference but are necessarily wide at distant horizons. Pass@$k$ extrapolation can be useful, but its uncertainty must disclose the structural assumptions that make it possible.

## Main results

**Proposition.** The count law $\pi(F)$ identifies exactly $\int q(p)dF(p)$ for every $q\in\mathcal{P}_b$, equivalently the first $b$ moments of $F$. Hence $\theta_k$ is identified for $k\leq b$, with the usual combinatorial pass@$k$ estimator, but not generally for $k>b$.

**Theorem.** Let 

$$
 E_{b,k}=\inf_{q\in\mathcal{P}_b}\\|x^k-q(x)\\|_{\infty,[0,1]}. 
$$

 Then 

$$
 \sup_{\mu}\\{U_k(\mu)-L_k(\mu)\\}=D_{b,k}=2E_{b,k}. 
$$

 Moreover, there are two probability laws attaining this gap while inducing the same complete count distribution.

**Corollary.** For $H\sim\mathrm{Binomial}(2k,1/2)$, let $T_{b,k}=\Pr(|H-k|>b)$. Then 

$$
 \frac{T_{b,k}}{2e}\leq D_{b,k}\leq 2T_{b,k}. 
$$

 In particular, the worst-case identification transition is $b\asymp\sqrt{k}$, or $k\asymp b^2$.

**Corollary.** Restrict both task populations to $P\in[p_0,1]$, for a declared $p_0\in[0,1]$. The sharp worst-case diameter becomes 

$$
 D_{b,k}(p_0)=(1-p_0)^kD_{b,k}. 
$$

## Keywords

pass@k, forecasting, moment problem, polynomial approximation, language model evaluation, extrapolation, identified set

## Files

- `aistats2027.sty`
- `code.zip`
- `fancyhdr.sty`
- `finite_interval_limits.pdf`
- `interval_audit.pdf`
- `main.bbl`
- `main.pdf`
- `main.tex`
- `matched_pair_curves.pdf`
- `real_forecast_audit.pdf`
- `references.bib`
- `supplement.bbl`
- `supplement.pdf`
- `supplement.tex`
