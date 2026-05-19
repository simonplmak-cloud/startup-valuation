# Appendix A: Valuation Formulas Quick Reference

## Overview

### Core Valuation Methods

Scorecard Method:

$$Valuation=Average Regional Pre-Money×\prod_{i=1}^{7} (1+w_{i}×a_{i})$$

Berkus Method:

$$Valuation=\sum_{i=1}^{5} Value_{i}, where each Value_{i}≤$500K$$

Risk Factor Summation:

$$Valuation=Base Valuation×(1+\sum_{i=1}^{12} Risk Factor_{i}×0.025)$$

Venture Capital Method:

$$Post-Money Valuation=\frac{Terminal Value}{(1+Target Return)^{Years}}$$

### Advanced Techniques

Black-Scholes for Real Options:

$$C=S×N(d_{1})-K×e^{-rT}×N(d_{2})$$

$$d_{1}=\frac{ln(S/K)+(r+σ^{2}/2)T}{σ\sqrt{T}}, d_{2}=d_{1}-σ\sqrt{T}$$

Binomial Option Pricing:

$$u=e^{σ\sqrt{Δt}}, d=e^{-σ\sqrt{Δt}}, p=\frac{e^{rΔt}-d}{u-d}$$

### Market Comparables

EV/Revenue Multiple:

$$Valuation=Revenue×Multiple$$

Regression-Adjusted Multiple:

$$Multiple=α+β_{1}×Growth+β_{2}×Margin+ϵ$$

### International Valuation

Currency-Adjusted DCF:

$$PV=\sum_{t=1}^{T} \frac{CF_{t}^{local}/E_{t}}{(1+r_{USD})^{t}}$$

Country Risk Premium:

$$CRP=Default Spread×\frac{σ_{equity}}{σ_{bond}}$$

### Industry-Specific

SaaS LTV:

$$LTV=\frac{ARPU×Gross Margin}{Churn Rate}$$

Biotech rNPV:

$$rNPV=\sum_{t=1}^{T} \frac{P_{success}×CF_{t}}{(1+r)^{t}}-Development Costs$$

Marketplace GMV:

$$Revenue=GMV×Take Rate$$


