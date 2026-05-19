# Chapter 2: Mathematical Foundations

## Mathematical Foundations


### Learning Objectives

By the end of this chapter, readers will be able to:

Define and apply fundamental concepts from probability theory including probability spaces, random variables, and
expected values to model valuation uncertainty

Calculate present values and net present values for various cash flow streams using appropriate discount rates

Prove the Law of One Price and explain its implications for arbitrage-free valuation

Derive and apply the Capital Asset Pricing Model (CAPM) to estimate risk-adjusted discount rates for startup investments

Compute portfolio betas using the weighted average formula and interpret the results

Analyze the limitations of CAPM when applied to pre-revenue companies and identify appropriate adjustments

Evaluate the appropriateness of different probability distributions for modeling startup outcomes


A rigorous approach to valuation requires a solid understanding of the underlying mathematical principles. This chapter
lays the groundwork by introducing key concepts from probability theory, the time value of money, and asset pricing
models. These mathematical tools are essential for modeling the uncertainty and risk inherent in valuing pre-revenue and
pre-profit companies.

### 2.1: Probability Theory for Uncertainty Modeling

Probability theory provides the mathematical framework for quantifying and analyzing uncertainty. In the context of
startup valuation, uncertainty is a defining characteristic. The future cash flows, market size, and even the survival
of the firm are all uncertain. By using probability distributions, we can model these uncertainties and make more
informed valuation decisions.

Definition 2.1 (Probability Space): A probability space is a mathematical construct that models a real-world experiment
consisting of three parts:

A sample space, , which is the set of all possible outcomes.

$$Ω$$

A set of events, , where each event is a set containing zero or more outcomes.

$$F$$

An assignment of probabilities to the events; that is, a function  from events to probabilities.

$$P$$

The probability function must satisfy three axioms: (1) for all events , (2) , and (3) for any countable sequence of
mutually exclusive events , we have .

$$P$$

$$P(E)≥0$$

$$E$$

$$P(Ω)=1$$

$$E_{1},E_{2},...$$

$$P(E_{1}∪E_{2}∪...)=P(E_{1})+P(E_{2})+...$$

Definition 2.2 (Random Variable): A random variable, usually denoted by , is a variable whose value is a numerical
outcome of a random phenomenon. Formally, a random variable is a function that maps the sample space to the set of real
numbers .

$$X$$

$$Ω$$

$$R$$

Random variables can be discrete or continuous. A discrete random variable takes on a countable number of values, while
a continuous random variable can take on any value in a range. The probability distribution of a random variable
describes the probabilities of different outcomes.

Definition 2.3 (Expected Value): The expected value of a random variable , denoted , is the weighted average of all
possible values, where the weights are the probabilities. For a discrete random variable:

$$X$$

$$E[X]$$

$$E[X]=\sum_{i}^{​} x_{i}P(X=x_{i})$$

For a continuous random variable:

$$E[X]=\int_{-∞}^{∞} xf(x)dx$$

where  is the probability density function.

$$f(x)$$

Example 2.1: Consider a startup that is developing a new drug. The outcome of the clinical trial can be either a success
or a failure. The sample space is . We can define a random variable such that and . If the probability of success is
0.3, then and . The expected value is .

$$Ω={Success,Failure}$$

$$X$$

$$X(Success)=1$$

$$X(Failure)=0$$

$$P(X=1)=0.3$$

$$P(X=0)=0.7$$

$$E[X]=1×0.3+0×0.7=0.3$$

Example 2.2: A startup’s revenue in the first year is modeled as a normal distribution with mean and standard deviation
. The probability that the revenue will be between $400,000 and $600,000 is approximately 68%, as this range is within
one standard deviation of the mean.

$$μ=$500,000$$

$$σ=$100,000$$

📊 Real World Example: Moderna’s COVID-19 Vaccine Valuation (2020)

In early 2020, Moderna was developing an mRNA vaccine for COVID-19. The company’s valuation hinged entirely on the
probability of clinical trial success--a perfect application of probability theory to real-world valuation.

$$
Probability Model: - Phase 1 success: P = 0.90 (safety trial) - Phase 2 success: P = 0.70 (efficacy in small group) -
Phase 3 success: P = 0.60 (efficacy in large trial) - FDA approval: P = 0.85 (given Phase 3 success) - Overall success
probability: 0.90 \times 0.70 \times 0.60 \times 0.85 = 0.32 (32%)
$$

Valuation Scenarios: - Success scenario: $50B+ market value (vaccine sales + platform validation) - Failure scenario:
$5B market value (platform technology only) - Expected value: 0.32 × $50B + 0.68 × $5B = $16B + $3.4B = $19.4B

Actual Outcome: Moderna’s market cap in January 2020 was approximately $7 billion. After successful Phase 3 results in
November 2020, the market cap surged to $50+ billion. The probability-weighted approach provided a reasonable framework,
though the actual probabilities and outcomes differed from initial estimates.

Key Insight: For biotech and other binary-outcome businesses, explicit probability modeling is essential. The expected
value framework allows investors to rationally value highly uncertain ventures.

Source: Moderna SEC filings, clinical trial data from clinicaltrials.gov


Example 2.3: A venture capital firm is evaluating a portfolio of 10 early-stage investments. Historical data suggests
that 20% of startups achieve a 10x return, 30% achieve a 2x return, 20% break even (1x), and 30% fail completely (0x).
The expected return per investment is:

$$E[R]=0.20(10)+0.30(2)+0.20(1)+0.30(0)=2.0+0.6+0.2+0=2.8x$$

This means that on average, each dollar invested returns $2.80, despite a 30% failure rate.


Figure 2.1: Probability Distribution of Startup Outcomes


Example 2.4: A fintech startup’s customer acquisition follows a Poisson distribution with an average of 500 new
customers per month. The probability of acquiring exactly 450 customers in a given month is:

$$P(X=450)=\frac{e^{-500}⋅500^{450}}{450!}≈0.011$$

The probability of acquiring at least 550 customers (exceeding expectations by 10%) can be calculated using the
cumulative distribution function.

### 2.2: Time Value of Money

The principle of the time value of money states that a sum of money today is worth more than the same sum of money in
the future. This is because money can be invested and earn a return. The time value of money is a fundamental concept in
finance and is the basis for all discounted cash flow valuation models.

Definition 2.4 (Present Value): The present value (PV) of a future cash flow is the amount of money that would have to
be invested today to generate that future cash flow. The formula for the present value of a single cash flow is:

$$PV=\frac{C}{(1+r)^{t}}$$

where  is the future cash flow,  is the discount rate, and  is the number of periods.

$$C$$

$$r$$

$$t$$

Definition 2.5 (Net Present Value): The net present value (NPV) of a series of cash flows is the sum of the present
values of all the cash flows:

$$NPV=\sum_{t=0}^{T} \frac{C_{t}}{(1+r)^{t}}$$

| Risk Factor | Value | Rationale |
| :--- | :---: | :--- |
| Sound Idea | $500,000 | On-demand car service solving real pain point |
| Prototype | $400,000 | Working iOS app, but limited functionality |
| Quality Management Team | $500,000 | Travis Kalanick (serial entrepreneur), Garrett Camp (StumbleUpon founder) |
| Strategic Relationships | $300,000 | Partnership with black car services, but limited |
| Product Rollout/Sales | $0 | Pre-revenue, very early traction |
| Total Valuation | $1,700,000 |  |

where  is the cash flow at time .

$$C_{t}$$

$$t$$

Theorem 2.1 (The Law of One Price): Two assets with the same cash flows must have the same price.

Proof: Assume two assets, A and B, have the same cash flows at times . If the price of A, denoted , is less than the
price of B, denoted , an investor could execute the following arbitrage strategy: buy asset A at price and sell asset B
at price . The net cash flow at time 0 is . At all future times , the cash flows from A and B are identical, so they
cancel out. The investor has made a risk-free profit of at time 0 with no future obligations. This arbitrage opportunity
would drive the price of A up and the price of B down until . Therefore, two assets with the same cash flows must have
the same price. ∎

$$C_{1},C_{2},...,C_{T}$$

$$1,2,...,T$$

$$P_{A}$$

$$P_{B}$$

$$P_{A}$$

$$P_{B}$$

$$P_{B}-P_{A}>0$$

$$t=1,2,...,T$$

$$P_{B}-P_{A}$$

$$P_{A}=P_{B}$$

Example 2.5: An investor is offered a choice between receiving $10,000 today or $11,000 in one year. If the discount
rate is 8%, the present value of $11,000 in one year is . Since this is greater than $10,000, the investor should choose
to receive $11,000 in one year.

$$PV=\frac{$11,000}{(1+0.08)^{1}}=$10,185.19$$

Example 2.6: A project requires an initial investment of $100,000 and is expected to generate cash flows of $30,000,
$40,000, and $50,000 in years 1, 2, and 3, respectively. If the discount rate is 10%, the NPV is:

$$NPV=-$100,000+\frac{$30,000}{(1.10)^{1}}+\frac{$40,000}{(1.10)^{2}}+\frac{$50,000}{(1.10)^{3}}=-$100,000+$27,273+$33,058+$37,566=-$2,103$$

Since the NPV is negative, the project should be rejected.

📊 Real World Example: Spotify’s Negative Cash Flow Valuation (2018 IPO)

When Spotify went public via direct listing in April 2018, the company was still burning cash despite $5 billion in
annual revenue. Traditional NPV analysis would suggest the company was worthless (negative cash flows extending into the
future). Yet the market valued Spotify at $26.5 billion.

The Valuation Challenge: - 2017 Financial Performance: - Revenue: $5.0 billion - Operating loss: $461 million - Free
cash flow: -$350 million - Cumulative losses since founding: $3+ billion

Why Traditional NPV Failed: - Near-term cash flows were negative (would yield negative NPV) - Path to profitability was
uncertain (licensing costs = 70% of revenue) - Growth vs. profitability tradeoff (could be profitable if growth slowed)

Alternative Valuation Approach: - Scenario Analysis with Probability Weights: - Success scenario (40% probability):
Company reaches 500M subscribers, achieves 10% operating margin, valued at $60B - Base case (40% probability): Company
reaches 300M subscribers, achieves 5% margin, valued at $25B - Failure scenario (20% probability): Company plateaus at
150M subscribers, never profitable, valued at $5B - Expected value: 0.40($60B) + 0.40($25B) + 0.20($5B) = $24B + $10B +
$1B = $35B

Actual Outcome: Spotify’s market cap fluctuated between $15B and $60B over the next 4 years, reaching profitability in
2023. The scenario-based approach captured the range of outcomes better than simple NPV.

Lesson: For high-growth companies with negative cash flows, traditional NPV is misleading. Scenario analysis with
probability weights provides a more realistic framework, explicitly modeling the uncertainty in future profitability.

Source: Spotify SEC Form F-1, Bloomberg


### 2.3: Risk-Adjusted Discount Rates

The discount rate used to calculate the present value of future cash flows must reflect the risk of those cash flows.
The higher the risk, the higher the discount rate. The Capital Asset Pricing Model (CAPM) is a widely used model for
calculating the risk-adjusted discount rate.

Definition 2.6 (Capital Asset Pricing Model - CAPM): The CAPM describes the relationship between systematic risk and
expected return for assets, particularly stocks. The formula for the CAPM is:

$$E(R_{i})=R_{f}+β_{i}(E(R_{m})-R_{f})$$

where is the expected return on the asset, is the risk-free rate, is the beta of the asset (which measures its
systematic risk), and is the expected return on the market.

$$E(R_{i})$$

$$R_{f}$$

$$β_{i}$$

$$E(R_{m})$$

The term is called the market risk premium, and it represents the additional return that investors demand for bearing
market risk. The beta coefficient measures how sensitive the asset’s returns are to market movements. A beta of 1 means
the asset moves in line with the market, a beta greater than 1 means the asset is more volatile than the market, and a
beta less than 1 means the asset is less volatile.

$$E(R_{m})-R_{f}$$

$$β_{i}$$

Lemma 2.1: The beta of a portfolio is the weighted average of the betas of the individual assets in the portfolio.

Proof: Let the portfolio consist of assets with weights and betas . The return of the portfolio is . The beta of the
portfolio is given by:

$$n$$

$$w_{1},w_{2},...,w_{n}$$

$$β_{1},β_{2},...,β_{n}$$

$$R_{p}=\sum_{i=1}^{n} w_{i}R_{i}$$

$$β_{p}=\frac{Cov(R_{p},R_{m})}{Var(R_{m})}=\frac{Cov(\sum_{i=1}^{n} w_{i}R_{i},R_{m})}{Var(R_{m})}$$

Using the linearity of covariance:

$$β_{p}=\frac{\sum_{i=1}^{n} w_{i}Cov(R_{i},R_{m})}{Var(R_{m})}=\sum_{i=1}^{n} w_{i}\frac{Cov(R_{i},R_{m})}{Var(R_{m})}=\sum_{i=1}^{n} w_{i}β_{i}$$

This proves that the beta of a portfolio is the weighted average of the betas of the individual assets. ∎

Example 2.7: A stock has a beta of 1.5, the risk-free rate is 3%, and the expected market return is 10%. The expected
return on the stock according to CAPM is:

$$E(R)=0.03+1.5(0.10-0.03)=0.03+1.5(0.07)=0.03+0.105=0.135=13.5%$$

Example 2.8: A portfolio consists of two stocks: Stock A with a beta of 0.8 and a weight of 60%, and Stock B with a beta
of 1.2 and a weight of 40%. The beta of the portfolio is:

$$β_{p}=0.60×0.8+0.40×1.2=0.48+0.48=0.96$$

While the CAPM is a powerful tool, it has limitations when applied to startups. The beta of a startup is difficult to
estimate because startups are not publicly traded. Additionally, the CAPM only accounts for systematic risk (market
risk) and ignores unsystematic risk (company-specific risk). For startups, unsystematic risk is often the dominant
source of risk. In the following chapters, we will explore extensions and alternatives to the CAPM that are more
suitable for valuing early-stage companies.

Example 2.9 (Startup-Adjusted CAPM): A venture capital firm is evaluating a Series A investment in a SaaS startup. They
estimate: - Risk-free rate: 4% - Market risk premium: 7% - Comparable public SaaS company beta: 1.3 - Size premium
(small cap): 3% - Startup-specific risk premium: 10%

The required return is:

$$E(R)=4%+1.3(7%)+3%+10%=4%+9.1%+3%+10%=26.1%$$

This 26% discount rate reflects both systematic risk (via beta) and startup-specific risks not captured by CAPM alone.


Figure 2.2: CAPM Security Market Line


### Key Takeaways


Probability theory provides the framework for modeling uncertainty in startup valuations, using random variables,
probability distributions, and expected values to quantify outcomes

The time value of money is fundamental: A dollar today is worth more than a dollar tomorrow due to investment
opportunities and risk

The Law of One Price prevents arbitrage: Assets with identical cash flows must have identical prices in efficient
markets

CAPM relates risk to expected return: Higher systematic risk (beta) requires higher expected returns

Portfolio beta is a weighted average: Diversification affects overall portfolio risk in predictable ways

CAPM has significant limitations for startups: Beta is unobservable, and unsystematic risk dominates for early-stage
companies

Startup discount rates typically range from 25-60%: Far higher than public company rates due to extreme uncertainty and
company-specific risks


### Exercises for Chapter 2

#### ⭐ Basic Understanding

| Factor | Value |
| :--- | :---: |
| Sound Idea | $500,000 |
| Prototype | $500,000 |
| Quality Management Team | $500,000 |
| Strategic Relationships | $0 |
| Product Rollout or Sales | $0 |
| Total Valuation | $1,500,000 |

1. A random variable X takes the value 100 with probability 0.4 and the value 200 with probability 0.6. What is the
expected value of X?

2. What is the present value of $50,000 to be received in 5 years if the discount rate is 12%?

3. A project requires an initial investment of $200,000 and generates cash flows of $60,000, $80,000, and $100,000 in
years 1, 2, and 3. If the discount rate is 15%, what is the NPV?

4. A stock has a beta of 2.0, the risk-free rate is 4%, and the expected market return is 11%. What is the expected
return on the stock according to CAPM?

5. A portfolio consists of three stocks with betas of 0.9, 1.1, and 1.3, and weights of 30%, 40%, and 30%, respectively.
What is the beta of the portfolio?

#### ⭐⭐ Intermediate Application

6. Explain the Law of One Price and why it is important in valuation. Provide a specific example of an arbitrage
opportunity that would arise if the law were violated.

7. What is the difference between systematic risk and unsystematic risk? Why does CAPM only price systematic risk?

8. Why is the CAPM difficult to apply to startups? Identify at least four specific challenges and propose potential
solutions for each.

9. What is the market risk premium, and how is it estimated in practice? What has been the historical market risk
premium in the U.S. over the past 50 years?

10. Calculate the NPV of a project with an initial cost of $150,000 and cash flows of $50,000 per year for 4 years,
using a discount rate of 10%. Should the project be accepted?

#### ⭐⭐⭐ Advanced Analysis

11. A biotech startup has a 30% probability of FDA approval. If approved, the company will be worth $500M. If not
approved, it will be worth $20M. The risk-free rate is 4%, and the appropriate risk-adjusted discount rate is 35%. The
FDA decision will be made in 3 years. What is the present value of the company today?

12. Prove that for a portfolio of n assets, the variance of the portfolio return is: Var(R_p) = \Sigma\Sigma wi wj
Cov(R_i, R_j). Explain how this formula demonstrates the benefits of diversification.

13. A venture capital firm has a portfolio of 20 startups. Historical data shows that 10% achieve a 20x return, 20%
achieve a 5x return, 30% achieve a 1x return (break even), and 40% fail completely (0x return). Calculate: (a) The
expected return per investment, (b) The standard deviation of returns, (c) The probability that the portfolio as a whole
returns at least 3x, (d) How many investments would be needed to have a 95% probability of at least a 2x return?

14. Derive the CAPM formula starting from the assumption that investors hold the market portfolio and can borrow/lend at
the risk-free rate. Your derivation should use the Capital Market Line and the Security Market Line.

15. A startup has projected cash flows of -$1M (Year 1), -$500K (Year 2), $2M (Year 3), $5M (Year 4), and $8M (Year 5).
However, there is a 40% probability the company fails in Year 2, in which case all future cash flows are zero. Calculate
the probability-adjusted NPV using a 30% discount rate.

#### 💭 Discussion Questions

16. The CAPM assumes investors can diversify away unsystematic risk. Is this assumption reasonable for venture capital
investors? Why or why not?

17. Some practitioners argue that using probability-weighted scenarios is more appropriate than traditional NPV for
startups. Do you agree? What are the advantages and disadvantages of each approach?

18. The historical equity risk premium in the U.S. has been approximately 7-8%. However, many VCs use discount rates of
40-60% for early-stage investments. How can this discrepancy be justified theoretically?

#### 🔬 Research Projects

19. Research the historical returns of venture capital funds over the past 20 years. How do these returns compare to
public equity markets? What does this tell us about the appropriate discount rates for startup investments?

20. Investigate alternative asset pricing models beyond CAPM (such as the Fama-French three-factor model or the
arbitrage pricing theory). How might these models be applied to startup valuation?

### Solutions for Chapter 2

#### ⭐ Basic Understanding

$$
1. Expected value = (100 \times 0.4) + (200 \times 0.6) = 40 + 120 = 160.
$$

$$
2. PV = 50,000 / (1 + 0.12)^5 \approx 50,000 / 1.7623 \approx 28,379.
$$

$$
3. NPV = -200,000 + (60,000 / 1.15) + (80,000 / 1.15^2) + (100,000 / 1.15^3) \approx -200,000 + 52,174 + 60,465 + 65,432
\approx -21,929 (reject project).
$$

$$
4. Expected return = 4% + 2.0 \times (11% - 4%) = 4% + 14% = 18%.
$$

$$
5. Portfolio beta = (0.3 \times 0.9) + (0.4 \times 1.1) + (0.3 \times 1.3) = 0.27 + 0.44 + 0.39 = 1.10.
$$

#### ⭐⭐ Intermediate Application

6. Law of One Price: Two assets with identical cash flows must have the same price; otherwise, arbitrage opportunities
exist. Example: If two bonds pay identical coupons but trade at different prices, investors can buy the cheaper and
short the expensive bond for risk-free profit.

7. Systematic risk affects all assets and cannot be diversified away; unsystematic risk is company-specific and can be
eliminated through diversification. CAPM prices only systematic risk because rational investors do not require
compensation for diversifiable risk.

8. CAPM challenges for startups: (a) No observable beta (solution: use industry comparables), (b) High unsystematic risk
(solution: add specific risk premium), (c) Illiquidity (solution: add illiquidity premium), (d) Rapidly changing risk
profile (solution: stage-specific discount rates).

9. Market risk premium = Expected market return - risk-free rate. Estimated using historical averages (~7% in U.S.),
forward-looking models, or surveys. Historically ~7-8% arithmetic mean over 50 years.

$$
10. NPV = -150,000 + 50,000 \times [(1 - (1 + 0.10)^-4) / 0.10] \approx -150,000 + 50,000 \times 3.1699 \approx -150,000
+ 158,495 = 8,495 (accept project).
$$

#### ⭐⭐⭐ Advanced Analysis

$$
11. Expected value in 3 years = (0.3 \times 500M) + (0.7 \times 20M) = 150M + 14M = 164M. PV = 164M / (1 + 0.35)^3
\approx 164M / 2.459 \approx 66.7M.
$$

12. Var(R_p) = \Sigma\Sigma wi wj Cov(R_i, R_j). Diversification reduces variance because covariance terms are less than
variance terms when assets are imperfectly correlated.

$$
13. Expected return = (0.10 \times 20) + (0.20 \times 5) + (0.30 \times 1) + (0.40 \times 0) = 2 + 1 + 0.3 = 3.3x.
Standard deviation and probabilities require detailed computation using variance formula and binomial distribution.
$$

14. CAPM derivation: Start from Capital Market Line (E(R_p) = R_f + (E(R_m) - R_f) \times \sigmap/\sigmam) and Security
Market Line assumptions; derive E(R_i) = R_f + \betai(E(R_m) - R_f).

15. Compute probability-adjusted NPV by weighting cash flows by survival probability and discounting at 30%. Year 1:
-1M; Year 2: -500K \times 0.6; Years 3-5: apply 0.6 survival probability and discount factors.

#### 💭 Discussion Questions

16-18. These are open-ended questions intended for discussion. Suggested points: diversification limits for VCs, pros
and cons of scenario analysis vs. NPV, justification for high discount rates due to extreme uncertainty and illiquidity.

#### 🔬 Research Projects

19-20. Research projects require external data collection and analysis. Evaluation should focus on methodology, data
quality, and insightfulness rather than specific numeric answers.

