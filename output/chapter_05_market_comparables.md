# Chapter 5: Market Comparables

## Market Comparables


### Learning Objectives

By the end of this chapter, readers will be able to:

Calculate key valuation multiples including EV/Revenue, P/S, EV/EBITDA, and P/E for comparable companies

Identify appropriate comparable companies based on industry, size, growth rate, and business model similarity

Apply regression analysis to adjust multiples for differences in growth rates, profitability, and risk between target
and comparables

Implement the guideline public company method and guideline transaction method under IFRS 13 and ASC 820

Evaluate the reliability of different multiples for pre-revenue companies (revenue multiples vs. user-based metrics)

Adjust comparable company multiples for differences in capital structure, growth stage, and market conditions

Document the comparable company selection process and adjustments to satisfy regulatory and audit requirements



The market comparables approach, also known as the method of multiples, is a valuation technique that uses the valuation
of publicly traded companies or the acquisition prices of similar private companies to estimate the value of a target
company. This chapter will define valuation multiples mathematically, discuss how to adjust them for various factors,
and review the relevant IFRS and U.S. GAAP disclosure requirements.

### 5.1: Defining Valuation Multiples Mathematically

A valuation multiple is a ratio of a company’s value to a key financial metric. The most common multiples are:

Price-to-Earnings (P/E) Ratio:

$$P/E=\frac{Market Cap}{Net Income}$$

Price-to-Sales (P/S) Ratio:

$$P/S=\frac{Market Cap}{Revenue}$$

Enterprise Value-to-EBITDA (EV/EBITDA) Ratio:

$$EV/EBITDA=\frac{Enterprise Value}{EBITDA}$$

Enterprise Value-to-Revenue (EV/Revenue) Ratio:

$$EV/Revenue=\frac{Enterprise Value}{Revenue}$$

For pre-revenue and pre-profit companies, the P/S ratio or EV/Revenue ratio is the most relevant, as they do not have
earnings or EBITDA. The valuation of the target company is then calculated as:

$$Valuation=Multiple_{comparable}×Metric_{target}$$

For example:

$$Valuation=(P/S)_{comparable}×Revenue_{target}$$

Properties of Valuation Multiples:

Valuation multiples are market-based and reflect the collective judgment of investors. They are relatively simple to
calculate and understand. However, they have several limitations. First, they assume that the target company is
comparable to the companies used to derive the multiples. Second, they do not explicitly account for differences in
growth rates, risk, or profitability. Third, they can be distorted by market bubbles or temporary market conditions.

Worked Example 5.1:

A publicly traded SaaS company has a market capitalization of $500 million and annual revenue of $100 million. Its P/S
ratio is:

$$P/S=\frac{$500,000,000}{$100,000,000}=5.0x$$

If a pre-revenue SaaS startup is projected to have revenue of $10 million next year, and we assume the same P/S
multiple, the valuation would be:

$$Valuation=5.0×$10,000,000=$50,000,000$$

However, this valuation should be adjusted downward to account for the higher risk and uncertainty of the startup.

Worked Example 5.2:

Three comparable companies have P/S ratios of 4.5x, 5.5x, and 6.0x. The median P/S ratio is 5.5x. If the target company
has projected revenue of $8 million, the valuation is:

$$Valuation=5.5×$8,000,000=$44,000,000$$

### 5.2: Scaling Adjustments for Stage and Geography

A key challenge in using market comparables is that no two companies are exactly alike. Adjustments need to be made for
differences in growth prospects, risk, stage of development, and geographic location. Regression analysis can be used to
quantify these adjustments.

Regression Model

We can model the valuation multiple as a function of several variables:

$$Multiple=β_{0}+β_{1}g+β_{2}M+β_{3}S+β_{4}G+ϵ$$

where: * is the expected revenue growth rate * is a dummy variable for the market maturity (e.g., 1 for a developed
market, 0 for an emerging market) * is a dummy variable for the stage of the company (e.g., 1 for a late-stage company,
0 for an early-stage company) * is a dummy variable for geography (e.g., 1 for North America, 0 for Europe) * is the
error term

$$g$$

$$M$$

$$S$$

$$G$$

$$ϵ$$

By running a regression on a sample of comparable companies, we can estimate the coefficients . We can then use these
coefficients to calculate the appropriate multiple for the target company.

$$β_{0},β_{1},β_{2},β_{3},β_{4}$$

Theorem 5.1 (Unbiased Estimator): If the assumptions of the linear regression model hold (linearity, random sampling, no
perfect collinearity, zero conditional mean of the error term, and homoscedasticity), the ordinary least squares (OLS)
estimators of the coefficients are unbiased.

Proof: The proof of the unbiasedness of OLS estimators is a standard result in econometrics. The key insight is that the
expected value of the OLS estimator equals the true parameter value. Formally, let be the OLS estimator of . We need to
show that . The OLS estimator is given by , where is the matrix of independent variables and is the vector of dependent
variables. Substituting and taking expectations, we get . Under the assumption that , we have , and therefore .

$$β$$

$$β$$

$$E[β]=β$$

$$β=(X'X)^{-1}X'Y$$

$$X$$

$$Y$$

$$Y=Xβ+ϵ$$

$$E[β]=E[(X'X)^{-1}X'(Xβ+ϵ)]=β+E[(X'X)^{-1}X'ϵ]$$

$$E[ϵ|X]=0$$

$$E[(X'X)^{-1}X'ϵ]=0$$

$$E[β]=β$$

Worked Example 5.3:

An analyst is valuing a pre-revenue startup in the European fintech sector. The analyst has collected data on a sample
of publicly traded fintech companies and has run a regression to estimate the P/S ratio. The regression equation is:

$$P/S=2.5+10g+0.5M-1.5S-0.2G$$

The target company has an expected revenue growth rate of 30% (g = 0.30), is in a developed market (M = 1), is an
early-stage company (S = 0), and is located in Europe (G = 0). The appropriate P/S ratio is:

$$P/S=2.5+10(0.30)+0.5(1)-1.5(0)-0.2(0)=2.5+3.0+0.5-0-0=6.0x$$

If the target company is projected to have revenue of $10 million in five years, the terminal value is:

| Factor | Weight | Score | Weighted Score |
| :--- | :---: | :---: | :---: |
| Management Team | 30% | 1.5 | 0.450 |
| Technology | 25% | 1.8 | 0.450 |
| Market Size | 20% | 1.2 | 0.240 |
| Competition | 15% | 0.8 | 0.120 |
| Sales & Marketing | 10% | 0.9 | 0.090 |
| Total | 100% |  | 1.350 |

$$Terminal Value=6.0×$10,000,000=$60,000,000$$

This can then be discounted back to the present to arrive at the current valuation. For example, if the discount rate is
25%, the present value is:

$$PV=\frac{$60,000,000}{(1.25)^{5}}=\frac{$60,000,000}{3.05}=$19,672,000$$

Worked Example 5.4:

A late-stage company (S = 1) in North America (G = 1) with a growth rate of 20% (g = 0.20) in a developed market (M = 1)
has a P/S ratio calculated as:

$$P/S=2.5+10(0.20)+0.5(1)-1.5(1)-0.2(1)=2.5+2.0+0.5-1.5-0.2=3.3x$$

### 5.3: IFRS/GAAP Disclosure Requirements

When using market comparables for financial reporting, IFRS 13 and ASC 820 require the following disclosures:

The valuation technique(s) used.

The inputs used in the valuation, including the multiples and any adjustments made.

The source of the comparable data.

A reconciliation of the fair value measurement to the company’s financial statements.

For Level 3 measurements, a description of the sensitivity of the fair value to changes in unobservable inputs.

The market comparables approach is typically classified as a Level 2 or Level 3 measurement, depending on the
observability of the inputs. If the multiples are derived from publicly traded companies with active markets, the
measurement may be Level 2. However, if significant adjustments are made for differences in stage, geography, or other
factors, the measurement is likely Level 3.


📊 Real World Example: Snowflake’s IPO Valuation (2020)

Snowflake’s September 2020 IPO became the largest software IPO in history, with the company valued at $33 billion on
first-day close despite being pre-profit. The valuation was driven entirely by comparable company analysis using SaaS
multiples.

The Valuation Challenge: - 2020 Revenue: $592M (growing 121% YoY) - Net loss: $539M (negative 91% margin) - No path to
profitability in near term - IPO price: $120 per share ($33B market cap) - How to justify 56x revenue multiple?

Comparable Company Analysis:

$$
Regression Adjustment: Using regression: Multiple = 10 + 0.25(Growth%) + 0.15(NRR%)
$$

$$
For Snowflake: Multiple = 10 + 0.25(121) + 0.15(158) = 10 + 30.25 + 23.7 = 64x
$$

Actual 56x multiple was slightly below regression-predicted value, suggesting reasonable pricing.

Outcome: - First day: Stock surged 112% to $245 ($70B market cap) - Peak (2021): $106B market cap (106x revenue) - 2024:
$45B market cap (~15x revenue) as growth slowed

Lesson: For high-growth SaaS companies, revenue multiples adjusted for growth rates and net revenue retention provide a
market-based framework. The 56x multiple seemed extreme but was justified by 121% growth and 158% NRR--metrics that
predicted future revenue scale.

Source: Snowflake S-1 filing, Capital IQ, SaaS Capital Index


📊 Real World Example: Rivian’s IPO Valuation (2021)

Rivian’s November 2021 IPO valued the electric vehicle startup at $66.5 billion despite having delivered only 156
vehicles and generating just $1 million in revenue. Finding appropriate comparables for a pre-revenue EV manufacturer
proved extremely challenging.

The Valuation Challenge: - 2021 Revenue: $1M (essentially zero) - Vehicles delivered: 156 (vs. target of 1,000) -
Production just beginning - IPO valuation: $66.5B ($78 per share) - Traditional automaker multiples: 0.3-0.8x revenue -
How to justify valuation higher than Ford ($50B) or GM ($80B)?

Comparable Company Analysis:

Traditional Automakers (Rejected as Comparables): | Company | Market Cap | Revenue | EV/Revenue | P/E |
|———|————|———|————|—–| | Ford | $50B | $136B | 0.4x | 35x | | GM | $80B | $127B | 0.6x | 6x | | Not applicable to
pre-revenue company ||||

EV Pure-Plays (Used as Comparables): | Company | Market Cap | Revenue | EV/Revenue | Stage | |———|————|———|————|——-| |
Tesla | $1,100B | $54B | 20x | Profitable, scaling | | Lucid | $40B | $0 | N/A | Pre-revenue | | Rivian | $66.5B | $1M |
66,500x | Pre-revenue |

Alternative Metric: Pre-Orders - Rivian pre-orders: ~55,000 vehicles - Average price: $75,000 - Potential revenue: $4.1B
- Valuation/pre-order revenue: 16x (comparable to Tesla’s 20x)

Outcome: - Peak (Nov 2021): $172 per share ($150B market cap) - 2022-2023: Declined to $10-20 per share ($10-20B market
cap) - Production challenges and cash burn concerns

Lesson: For pre-revenue companies in emerging industries, traditional comparables may not exist. Rivian’s valuation
relied on (1) Tesla as aspirational comparable, (2) pre-order book as proxy for future revenue, and (3) venture
capital-style growth assumptions. The subsequent 85% decline showed the danger of extrapolating from limited comparables
in euphoric markets.

Source: Rivian S-1 filing, Bloomberg, automotive industry data



### Key Takeaways


Revenue multiples are the primary metric for pre-profit companies since EBITDA and earnings are negative, with
EV/Revenue being preferred over P/S to account for capital structure differences

Growth rate is the most important adjustment factor: High-growth companies (>50% YoY) command 2-5x higher multiples than
slow-growth peers in the same industry

Net Revenue Retention (NRR) is critical for SaaS valuations: NRR >120% indicates strong unit economics and justifies
premium multiples (as seen in Snowflake’s 158% NRR)

Comparable selection requires multiple criteria: Industry, business model, size, growth stage, and market conditions
must all be considered—no single factor is sufficient

Regression analysis provides objectivity: Rather than subjective adjustments, regression on growth, margins, and other
metrics yields defensible multiple predictions

Market conditions matter enormously: Snowflake’s 56x and Rivian’s 66,500x multiples reflected 2020-2021 euphoria; both
declined 60-85% as markets normalized

Pre-order books can proxy for revenue: When actual revenue is zero, committed customer demand (Rivian’s 55,000
pre-orders) provides a market-based anchor for valuation


### Exercises for Chapter 5

#### ⭐ Basic Understanding

1. A company has a market cap of $500 million and revenue of $100 million. What is its P/S ratio?

2. Using the regression equation from Worked Example 5.3, what is the P/S ratio for a late-stage company (S=1) in North
America (G=1) with a growth rate of 20% in a developed market (M=1)?

| Item | Description | Completed |
| :---: | :---: | :--- |
| 1 | Valuation date clearly stated | ☐ |
| 2 | Purpose of the valuation specified (e.g., financial reporting, tax compliance, transaction pricing) | ☐ |
| 3 | Valuation standard identified (e.g., fair value, fair market value) | ☐ |
| 4 | Detailed description of the company, its industry, and competitive landscape | ☐ |
| 5 | Valuation methodology described, including specific techniques and rationale | ☐ |
| 6 | All key inputs and assumptions disclosed | ☐ |
| 7 | Source of market data documented | ☐ |
| 8 | Management projections included and explained | ☐ |
| 9 | Valuation conclusion stated clearly | ☐ |
| 10 | Reconciliation to financial statements provided (if applicable) | ☐ |
| 11 | Sensitivity analysis included | ☐ |
| 12 | Qualifications and experience of the valuer described | ☐ |
| 13 | Statement of independence (if applicable) | ☐ |
| 14 | Compliance with IFRS 13 or ASC 820 confirmed | ☐ |
| 15 | Compliance with IRS 409A confirmed (if applicable) | ☐ |

3. Three comparable companies have EV/Revenue multiples of 3.5x, 4.0x, and 4.5x. What is the average multiple?

4. If a company has projected revenue of $15 million and the average P/S multiple of comparables is 5.5x, what is the
estimated valuation?

5. What is the main limitation of using valuation multiples from publicly traded companies to value startups?

#### ⭐⭐ Intermediate Application

6. A company has an enterprise value of $200 million and EBITDA of $40 million. What is its EV/EBITDA multiple?

7. In the regression model for P/S ratios, what does a positive coefficient for the growth rate indicate?

8. If the P/S ratio is 4.0x and the projected revenue is $20 million, what is the valuation?

9. What is the difference between a Level 2 and Level 3 fair value measurement?

10. Calculate the P/S ratio for a company with market cap of $750 million and revenue of $125 million.

#### ⭐⭐⭐ Advanced Analysis

11. Using the regression equation, calculate the P/S ratio for g=0.25, M=0, S=0, G=1.

12. If five comparable companies have P/S ratios of 3.0x, 4.0x, 5.0x, 6.0x, and 7.0x, what is the median?

13. What type of companies are most suitable as comparables for a pre-revenue SaaS startup?

14. A company is valued at $40 million using a P/S multiple of 5.0x. What is its projected revenue?

15. Why might an early-stage company have a lower valuation multiple than a late-stage company?

#### 💭 Discussion Questions

16. Discuss the reliability of market comparables in volatile market conditions.

17. Should adjustments for growth and profitability always be applied when using multiples? Why or why not?

18. How do geographic and regulatory differences affect the comparability of companies?

#### 🔬 Research Projects

19. Research 10 recent IPOs and compare their valuation multiples to those of private startups in the same industry.

20. Analyze the impact of regression-adjusted multiples on valuations in high-growth sectors.


### Solutions for Chapter 5

#### ⭐ Basic Understanding

1. P/S ratio = Market Cap / Revenue = $500M / $100M = 5.0x.

$$
2. Apply regression equation: Multiple = 10 + 0.25(0.20) + 0.15(1) + adjustments (details per example).
$$

$$
3. Average multiple = (3.5 + 4.0 + 4.5) / 3 = 4.0x.
$$

$$
4. Valuation = Projected Revenue \times Multiple = $15M \times 5.5 = $82.5M.
$$

5. Limitation: Public companies are larger, more mature, and less risky than startups, leading to potential
overvaluation if multiples are applied without adjustment.

#### ⭐⭐ Intermediate Application

$$
6. EV/EBITDA = $200M / $40M = 5.0x.
$$

7. A positive coefficient indicates that higher growth rates are associated with higher P/S ratios.

$$
8. Valuation = $20M \times 4.0 = $80M.
$$

9. Level 2 uses observable inputs other than quoted prices; Level 3 uses unobservable inputs based on assumptions.

$$
10. P/S ratio = $750M / $125M = 6.0x.
$$

#### ⭐⭐⭐ Advanced Analysis

11. Substitute values into regression equation (details depend on coefficients provided in text).

12. Median = 5.0x.

13. Suitable comparables: Other pre-revenue or early-stage SaaS companies with similar growth prospects and business
models.

$$
14. Projected revenue = Valuation / Multiple = $40M / 5.0 = $8M.
$$

15. Early-stage companies have higher risk and uncertainty, justifying lower multiples.

#### 💭 Discussion Questions

16-18. Open-ended questions; answers should discuss market volatility, adjustment rationale, and geographic/regulatory
impacts.

#### 🔬 Research Projects

19-20. Research-based tasks; solutions involve data collection, analysis, and interpretation.

