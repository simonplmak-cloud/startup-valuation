# Chapter 4: Advanced Techniques

## Advanced Techniques


### Learning Objectives

By the end of this chapter, readers will be able to:

Derive the Black-Scholes formula for valuing startups as real options and explain the economic intuition behind each
parameter

Construct binomial trees to value American-style options and prove convergence to Black-Scholes as time steps increase

Implement Monte Carlo simulations in Python to generate probability distributions of startup valuations under
uncertainty

Apply scenario analysis with probability weighting to value companies with discrete outcome possibilities

Compare the strengths and limitations of Real Options, Monte Carlo, and Scenario Analysis for different company types

Evaluate when advanced quantitative techniques are appropriate versus simpler qualitative methods

Assess the regulatory acceptability and litigation defensibility of advanced valuation techniques


This chapter introduces more sophisticated valuation techniques that are particularly well-suited for handling the high
levels of uncertainty and flexibility inherent in early-stage companies. These methods, including real options
valuation, Monte Carlo simulation, and scenario analysis, provide a more dynamic and nuanced approach to valuation than
the core models discussed in the previous chapter.

### 4.1: Real Options Valuation

Real options analysis (ROA) is a valuation technique that applies option pricing theory to the valuation of
non-financial assets, such as real estate, infrastructure projects, and, most relevant to this book, startup companies.
A real option is the right, but not the obligation, to take a particular business action, such as deferring, abandoning,
expanding, or contracting a project. These options have value because they give managers the flexibility to respond to
changing market conditions.

For a startup, the entire venture can be viewed as a call option on its future profits. The initial investment is the
price of the option, and the exercise price is the future investment required to scale the business. If the business is
successful, the option is exercised, and the investors reap the rewards. If the business is not successful, the option
expires worthless, and the investors lose only their initial investment.

#### Option Pricing Theory

The two most common models for pricing options are the Black-Scholes model and the binomial tree model.

The Black-Scholes Model

The Black-Scholes model is a mathematical model for pricing European-style options, which can only be exercised at a
specific date. The formula for the price of a call option is:

$$C(S,t)=N(d_{1})S-N(d_{2})Ke^{-r(T-t)}$$

where: * is the price of the call option * is the price of the underlying asset * is the strike price * is the risk-free
interest rate * is the time to maturity * and are the cumulative distribution functions of the standard normal
distribution, where:

$$C(S,t)$$

$$S$$

$$K$$

$$r$$

$$T-t$$

$$N(d_{1})$$

$$N(d_{2})$$

$$d_{1}=\frac{ln(\frac{S}{K})+(r+\frac{σ^{2}}{2})(T-t)}{σ\sqrt{T-t}}$$

$$d_{2}=d_{1}-σ\sqrt{T-t}$$

- is the volatility of the underlying asset

When applying the Black-Scholes model to a startup, the price of the underlying asset () is the present value of the
expected future cash flows of the business, and the strike price () is the investment required to scale the business.

$$S$$

$$K$$

Properties of the Black-Scholes Model:

The Black-Scholes model has several important properties. First, the option value increases with the volatility of the
underlying asset. This is because higher volatility increases the potential upside while limiting the downside (since
the option holder can choose not to exercise). Second, the option value increases with the time to maturity. More time
gives the option holder more opportunities to benefit from favorable market movements. Third, the option value increases
with the risk-free rate, as a higher rate reduces the present value of the strike price.

The Binomial Tree Model

The binomial tree model is a discrete-time model that breaks down the time to expiration into a number of time steps. At
each step, the price of the underlying asset can move up or down by a certain amount. The model then works backward from
the expiration date to determine the value of the option at the present time.

Theorem 4.1 (Convergence of the Binomial Tree Model): As the number of time steps in the binomial tree model approaches
infinity, the value of the option converges to the value given by the Black-Scholes model.

Proof: The proof of this theorem relies on the central limit theorem. As the number of steps increases, the binomial
distribution of the asset price approaches a log-normal distribution, which is the distribution assumed by the
Black-Scholes model. The detailed proof involves showing that the discrete-time binomial process converges to a
continuous-time geometric Brownian motion, which is the stochastic process underlying the Black-Scholes model. This
convergence has been rigorously proven in the financial mathematics literature.

Worked Example 4.1:

A startup is developing a new software product. The company has the option to invest $5 million in one year to launch
the product. The present value of the expected cash flows from the product is $20 million, with a volatility of 40%. The
risk-free rate is 5%. Using the Black-Scholes model, the value of this real option is:

First, we calculate  and :

$$d_{1}$$

$$d_{2}$$

$$d_{1}=\frac{ln(\frac{20}{5})+(0.05+\frac{0.4^{2}}{2})(1)}{0.4\sqrt{1}}=\frac{ln(4)+0.05+0.08}{0.4}=\frac{1.3863+0.13}{0.4}=\frac{1.5163}{0.4}=3.79$$

$$d_{2}=3.79-0.4\sqrt{1}=3.79-0.4=3.39$$

Next, we find  and  from a standard normal distribution table or calculator:

$$N(d_{1})$$

$$N(d_{2})$$

$$N(d_{1})≈0.9999$$

$$N(d_{2})≈0.9997$$

Finally, we calculate the value of the call option:

$$C=(0.9999×20)-(0.9997×5×e^{-0.05(1)})=19.998-(0.9997×5×0.9512)=19.998-4.754=$15.24 million$$

The value of the option to launch the product is $15.24 million. This is the value of the flexibility that the company
has to wait and see how the market develops before committing to the investment.

Worked Example 4.2:

A biotech company has the option to invest $30 million in 3 years to commercialize a drug. The present value of the
expected cash flows is $100 million, with a volatility of 60%. The risk-free rate is 4%. Calculate the value of this
real option.

$$d_{1}=\frac{ln(\frac{100}{30})+(0.04+\frac{0.6^{2}}{2})(3)}{0.6\sqrt{3}}=\frac{ln(3.333)+0.04×3+0.18×3}{0.6×1.732}=\frac{1.204+0.12+0.54}{1.039}=\frac{1.864}{1.039}=1.79$$

$$d_{2}=1.79-0.6\sqrt{3}=1.79-1.039=0.75$$

$$N(d_{1})≈0.9633, N(d_{2})≈0.7734$$

$$C=(0.9633×100)-(0.7734×30×e^{-0.04×3})=96.33-(0.7734×30×0.8869)=96.33-20.57=$75.76 million$$

The value of the real option is $75.76 million.


Figure 4.1: Binomial Tree Valuation

### 4.2: Monte Carlo Simulation

Monte Carlo simulation is a powerful computational technique that allows us to model the uncertainty of a system by
running a large number of simulations. In the context of startup valuation, Monte Carlo simulation can be used to
generate a probability distribution of the company’s future cash flows, and therefore, its valuation.

Stochastic Modeling

The core of a Monte Carlo simulation is a stochastic model, which is a model that incorporates randomness. Instead of
using single-point estimates for the key drivers of the valuation (e.g., market size, market share, and profit margin),
we use probability distributions. For example, we might model the market size as a normal distribution with a mean of $1
billion and a standard deviation of $200 million.

The Monte Carlo method involves the following steps:

Define the model: Specify the relationships between the input variables and the output (valuation).

| Scenario | Probability | 2025 Revenue | Multiple | Value per Share |
| :--- | :---: | :---: | :---: | :---: |
| Bear (Gov’t only) | 20% | $2B | 8x | $5.00 |
| Base (Slow commercial) | 40% | $4B | 12x | $15.00 |
| Bull (Commercial success) | 30% | $8B | 15x | $35.00 |
| Super Bull (Platform) | 10% | $15B | 20x | $80.00 |

Specify probability distributions: For each uncertain input variable, specify a probability distribution (e.g., normal,
uniform, triangular).

Generate random samples: Draw random samples from the probability distributions for each input variable.

Calculate the output: For each set of random samples, calculate the valuation.

Repeat: Repeat steps 3 and 4 many times (e.g., 10,000 times).

Analyze the results: Calculate summary statistics (mean, standard deviation, percentiles) and create histograms or other
visualizations of the probability distribution of the valuation.

Python Pseudo-code

The following Python pseudo-code illustrates how a Monte Carlo simulation can be used to value a startup:

```python
import numpy as np

def monte_carlo_valuation(num_simulations):
    valuations = []
    for _ in range(num_simulations):
        # Define probability distributions for key inputs
        market_size = np.random.normal(1e9, 2e8)
        market_share = np.random.uniform(0.01, 0.05)
        profit_margin = np.random.triangular(0.1, 0.2, 0.3)

        # Calculate the terminal value
        revenue = market_size * market_share
        profit = revenue * profit_margin
        terminal_value = profit * 5 # Assuming a 5x profit multiple

        # Discount the terminal value to the present
        discount_rate = np.random.normal(0.25, 0.05)
        present_value = terminal_value / (1 + discount_rate)**5

        valuations.append(present_value)

    return np.mean(valuations), np.std(valuations), np.percentile(valuations, [10, 50, 90])
```


Figure 4.2: Monte Carlo Simulation Paths


```python
mean_val, std_val, percentiles = monte_carlo_valuation(10000)
print(f"Mean Valuation: ${mean_val:,.2f}")
print(f"Standard Deviation: ${std_val:,.2f}")
print(f"10th Percentile: ${percentiles[0]:,.2f}")
print(f"50th Percentile (Median): ${percentiles[1]:,.2f}")
print(f"90th Percentile: ${percentiles[2]:,.2f}")
```

Worked Example 4.3:

Running the pseudo-code above with 10,000 simulations might produce the following results:

Mean Valuation: $3,500,000

Standard Deviation: $1,200,000

10th Percentile: $1,800,000

50th Percentile (Median): $3,400,000

90th Percentile: $5,400,000

The Monte Carlo simulation gives us not just a single-point estimate of the valuation, but a range of possible
valuations and the probability of each valuation. This provides a much richer and more realistic picture of the
company’s value than a deterministic model. The 10th and 90th percentiles give us a sense of the downside and upside
scenarios.

Worked Example 4.4:

A startup’s valuation depends on three uncertain variables: customer acquisition cost (CAC), lifetime value (LTV), and
market size. CAC is uniformly distributed between $50 and $150. LTV is normally distributed with mean $500 and standard
deviation $100. Market size is triangularly distributed with minimum 100,000, mode 200,000, and maximum 500,000. The
valuation is calculated as (LTV/CAC) × Market Size × 0.1. After running 10,000 simulations, the results might be:

Mean Valuation: $4,200,000

Standard Deviation: $1,800,000

Range: $800,000 to $12,000,000

### 4.3: Scenario Analysis

Scenario analysis is a simpler form of stochastic modeling that involves analyzing the valuation of a company under a
small number of discrete scenarios. Typically, three scenarios are considered: a best-case scenario, a worst-case
scenario, and a base-case scenario.

Formalization as Expected Value

Let be the valuation of the company under scenario , and let be the probability of that scenario occurring. The expected
value of the valuation, , is given by:

$$V_{i}$$

$$i$$

$$p_{i}$$

$$E[V]$$

$$E[V]=\sum_{i=1}^{n} p_{i}V_{i}$$

This formula is a direct application of the expected value concept from probability theory.

Worked Example 4.5:

A startup is valued under three scenarios:

The expected value of the valuation is:

$$E[V]=(0.20×$10,000,000)+(0.60×$5,000,000)+(0.20×$1,000,000)=$2,000,000+$3,000,000+$200,000=$5,200,000$$

Worked Example 4.6:

A company is valued under four scenarios based on different market conditions:

The expected value is:

$$E[V]=(0.15×$20,000,000)+(0.50×$8,000,000)+(0.25×$3,000,000)+(0.10×$500,000)$$

$$=$3,000,000+$4,000,000+$750,000+$50,000=$7,800,000$$



📊 Real World Example: Palantir’s Direct Listing Valuation (2020)

Palantir went public via direct listing in September 2020 with a complex revenue mix: ~60% government contracts (stable
but slow-growing) and ~40% commercial clients (high-growth but uncertain). Traditional valuation struggled with this
bifurcated business model.

The Valuation Challenge: - Government revenue: Predictable but capped by budget constraints - Commercial revenue:
Growing 40%+ but from small base - Negative cash flow: $580M loss in 2019 - No clear path to profitability - Reference
price: $7.25 per share (private market)

Scenario Analysis Approach: Investment banks used probability-weighted scenarios:

$$
Expected value: 0.20($5) + 0.40($15) + 0.30($35) + 0.10($80) = $1 + $6 + $10.50 + $8 = $25.50 per share
$$

Outcome: - First day close: $9.50 per share (31% above reference) - 2021 peak: $45 per share (commercial growth
accelerating) - 2024: $20-25 per share range (market recalibration)

Lesson: Scenario analysis with explicit probability weights provided a framework for valuing a company with two distinct
business models. The wide range of outcomes ($5-$80) reflected genuine uncertainty, and the probability-weighted
approach avoided the false precision of single-point DCF estimates.

Source: Palantir S-1 filing, direct listing prospectus, financial press


### Key Takeaways

Real Options valuation treats startups as call options on future value, capturing the asymmetric payoff structure
(limited downside, unlimited upside) that traditional DCF misses

Black-Scholes requires five inputs: current value, exercise price, time to expiration, risk-free rate, and
volatility--with volatility being the most critical and difficult to estimate for startups

Monte Carlo simulation generates probability distributions by running thousands of scenarios with random inputs,
providing a full range of outcomes rather than a single point estimate

Scenario analysis is simpler but less comprehensive: typically uses 3-5 discrete scenarios with explicit probability
weights, making it more transparent and easier to explain

Advanced techniques are computationally intensive and require specialized expertise, making them less suitable for
early-stage valuations where data is scarce

Regulatory acceptance varies: Courts and auditors are often skeptical of complex models, preferring simpler market-based
evidence (as seen in Hyde Park case)

Real-world examples (Tesla, Palantir) show extreme outcomes: Initial valuations of $1.7B and $16B grew to $1.2T and $45B
peaks, demonstrating both the methods’ utility and the irreducible uncertainty in startup valuation


| Company | EV/Revenue | Revenue Growth | NRR | Gross Margin |
| :--- | :---: | :---: | :---: | :---: |
| Snowflake | 56x | 121% | 158% | 62% |
| ——— | ———— | —————- | —– | ————– |
| Datadog | 45x | 68% | 130% | 77% |
| Zoom | 42x | 326% | 130% | 68% |
| Crowdstrike | 40x | 86% | 124% | 72% |
| Okta | 28x | 43% | 118% | 73% |
| Median | 40x | 77% | 127% | 72% |

### Exercises for Chapter 4

#### ⭐ Basic Understanding (Conceptual & Computational)

1. Define a real option in the context of startup valuation. How does it differ from a financial option?

2. A biotech startup has the option to abandon a drug development program after Phase I trials. The cost to reach Phase
I is $5M, and the probability of success is 30%. If successful, the Phase II investment would be $20M. Should this be
valued as a real option? Explain.

3. Calculate the value of a call option using Black-Scholes with the following parameters: S=$50M, K=$30M, r=5%, σ=60%,
T=3 years.

4. Explain why volatility (\sigma) increases the value of a real option. Use a numerical example.

5. A startup has the option to expand into a new market in 2 years. The expansion would cost $10M. Current market value
is $8M, with 50% annual volatility. Risk-free rate is 4%. Calculate the option value using Black-Scholes.

6. What is the difference between American and European options in the context of startup real options?

7. Draw a binomial tree for a 2-period model with u=1.3, d=0.8, starting value $100M. Calculate the risk-neutral
probabilities if r=5%.

#### ⭐⭐ Intermediate Application

8. A SaaS startup can invest $15M now to launch a new product line, or wait 1 year. Current PV of cash flows is $12M
with 70% volatility. Risk-free rate is 4%. Should they invest now or wait? Use Black-Scholes.

9. Build a 3-period binomial tree to value an expansion option for a fintech startup. Current value $50M, expansion cost
$40M, u=1.4, d=0.7, r=6%. The option can be exercised at any time.

10. A hardware startup has sequential options: (1) Prototype development ($2M), (2) Manufacturing setup ($10M), (3)
Market launch ($20M). Each stage has 40% success probability. Value this compound option.

11. Compare the valuation of a biotech company using traditional DCF vs. real options approach. The company has 3
pipeline drugs at different clinical stages. Show calculations.

12. A marketplace platform can expand to 5 new countries. Each expansion costs $5M and has independent 35% success
probability. Value this portfolio of options.

13. Calculate the implied volatility from a recent acquisition: Company valued at $80M, acquired for $120M after 18
months. Risk-free rate was 3%.

14. A startup has the option to pivot its business model in 6 months. Current trajectory has $20M PV, pivot would cost
$8M with $25M expected PV but 60% uncertainty. Value the pivot option.

#### ⭐⭐⭐ Advanced Analysis

15. A deep tech startup has a patent portfolio with 5 different technology applications. Each can be commercialized
independently with different costs, timings, and success probabilities. Model this as a rainbow option and estimate
value.

16. Critique the use of Black-Scholes for startup valuation. What assumptions are violated? Propose adjustments for: (1)
non-tradeable assets, (2) changing volatility, (3) competitive threats.

17. A biotech company has a drug in Phase II trials. Success probability is 45%. If successful, they can either: (A)
Complete Phase III themselves ($50M cost, $200M NPV), or (B) License to Big Pharma ($80M upfront). Model as a switching
option.

18. Design a Monte Carlo simulation (10,000 paths) to value a startup with the following uncertainties: revenue growth
(\mu=30%, \sigma=50%), margin expansion (15% to 35% over 5 years), and binary regulatory approval (60% probability in
year 3). Provide pseudo-code.

#### 💭 Discussion Questions

19. When is real options valuation most appropriate for startups? When might it overstate value?

20. How should boards and investors think about the ‘option to abandon’ when making follow-on investment decisions?

21. Discuss the ethical implications of valuing a biotech startup’s option to abandon a drug program that could help
patients.

#### 🔬 Research Projects

22. Collect data on 20 biotech IPOs. Estimate the implied volatility from their valuations. Compare to actual stock
price volatility post-IPO. What explains the differences?

23. Interview 5 VCs about how they think about optionality in their investment decisions. Do they explicitly value real
options? If not, how do they account for flexibility?

24. Build a complete real options valuation model for a specific startup (with permission). Compare to their most recent
409A valuation. Present findings.


### Solutions for Chapter 4

#### ⭐ Basic Understanding

1. A real option in startup valuation is the right, but not the obligation, to undertake certain business actions (e.g.,
expand, delay, abandon) in the future. It differs from a financial option because the underlying asset is a real
investment project, not a traded security.

2. Yes, this should be valued as a real option because the startup has flexibility to abandon after Phase I, limiting
downside risk while preserving upside potential.

3. Use Black-Scholes formula: C = S*N(d1) - K*e^(-rT)*N(d2), where d1 and d2 are calculated based on given parameters.

4. Higher volatility increases option value because it raises the probability of extreme favorable outcomes while
limiting downside (option holder can choose not to exercise).

5. Apply Black-Scholes with given inputs to compute option value.

6. American options can be exercised anytime before expiration; European options only at maturity. Real options often
resemble American options due to managerial flexibility.

$$
7. Risk-neutral probability p = (e^(r\Deltat) - d) / (u - d). For u=1.3, d=0.8, r=5%, compute p and draw tree.
$$

#### ⭐⭐ Intermediate Application

8. Calculate option value using Black-Scholes; compare to immediate investment NPV to decide.

9. Build binomial tree, compute option value by backward induction.

10. Value compound option by multiplying probabilities and discounting expected payoffs.

11. Real options approach typically yields higher value than DCF because it accounts for flexibility and uncertainty.

12. Portfolio option value = sum of individual option values (assuming independence).

13. Implied volatility can be derived from observed price using Black-Scholes inversion.

14. Compute pivot option value using scenario analysis or Black-Scholes approximation.

#### ⭐⭐⭐ Advanced Analysis

15. Model as rainbow option using multi-dimensional binomial or Monte Carlo simulation.

16. Black-Scholes assumptions violated: constant volatility, continuous trading, lognormal distribution, no dividends.
Adjust by using binomial trees, stochastic volatility models, or scenario analysis.

17. Use decision tree or switching option model to compare strategies and compute expected value.

18. Monte Carlo pseudo-code provided in chapter; simulate thousands of paths for revenue, margin, and regulatory
outcomes.

#### 💭 Discussion Questions & 🔬 Research Projects

19-24. These are open-ended questions and projects requiring qualitative analysis and external research. Solutions
should focus on reasoning, evidence, and methodology rather than numeric answers.

