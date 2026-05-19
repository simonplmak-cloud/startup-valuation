# Chapter 10: Tools and Templates

## Tools and Templates

### Learning Objectives

By the end of this chapter, readers will be able to:

Understand the key formulas and frameworks for Scorecard Method, VC Method, and DCF analysis

Apply Monte Carlo simulation and scenario analysis concepts to valuation problems

Select appropriate valuation methodologies for different company stages (seed, Series A, Series B+)

Prepare IFRS 13 and ASC 820 compliant disclosure templates for Level 3 fair value measurements

Complete IRS 409A valuation reports with required documentation and safe harbor compliance

Apply valuation checklists to ensure all key factors are considered and documented

Customize templates for industry-specific requirements (SaaS, biotech, marketplace, hardware)



This final chapter provides a reference guide of key formulas, frameworks, and checklists to help you apply the concepts
and methodologies discussed in this book.

### 10.1: Formulas

Present Value:

$$PV=\frac{C}{(1+r)^{t}}$$

Net Present Value:

$$NPV=\sum_{t=0}^{T} \frac{C_{t}}{(1+r)^{t}}$$

Capital Asset Pricing Model (CAPM):

$$E(R_{i})=R_{f}+β_{i}(E(R_{m})-R_{f})$$

Scorecard Method:

$$V_{target}=V_{avg}×\sum_{i=1}^{n} w_{i}s_{i}$$

Berkus Method:

$$V=\sum_{i=1}^{5} v_{i}$$

Risk Factor Summation Method:

$$V=V_{base}+\sum_{i=1}^{12} (r_{i}×$250,000)$$

Venture Capital Method:

$$Post-money Valuation=\frac{Terminal Value}{Expected ROI}$$

$$Pre-money Valuation=Post-money Valuation-Investment Amount$$

Black-Scholes Model:

$$C(S,t)=N(d_{1})S-N(d_{2})Ke^{-r(T-t)}$$

$$d_{1}=\frac{ln(\frac{S}{K})+(r+\frac{σ^{2}}{2})(T-t)}{σ\sqrt{T-t}}$$

$$d_{2}=d_{1}-σ\sqrt{T-t}$$

Expected Value (Scenario Analysis):

$$E[V]=\sum_{i=1}^{n} p_{i}V_{i}$$

Valuation Multiples:

$$P/S=\frac{Market Cap}{Revenue}$$

$$EV/EBITDA=\frac{Enterprise Value}{EBITDA}$$

### 10.2: Valuation Frameworks

The following frameworks illustrate how valuation models can be structured:

Scorecard Method Template:

Average Pre-Money Valuation: $1,500,000
Weighted Score: 1.200
Target Company Valuation: $1,800,000

Venture Capital Method Template:

Berkus Method Template:

### 10.3: Python Snippets for Simulations

The following Python

| Item | Amount |
| :--- | :--- |
| Fair Value at Beginning of Period | [Amount] |
| Additions | [Amount] |
| Changes in Fair Value | [Amount] |
| Disposals | [Amount] |
| Fair Value at End of Period | [Amount] |

snippet can be used to run a Monte Carlo simulation for valuation, as discussed in [Chapter
4](./chapter_04_advanced_techniques.md).

```python
import numpy as np

def monte_carlo_valuation(num_simulations):
    """
    Monte Carlo simulation for startup valuation.
    
    Parameters:
    num_simulations: Number of simulation iterations to run
    
    Returns:
    Tuple of (mean, std_dev, percentiles)
    """
    valuations = []
    
    for _ in range(num_simulations):
        # Define probability distributions for key inputs
        market_size = np.random.normal(1e9, 2e8)  # Mean $1B, SD $200M
        market_share = np.random.uniform(0.01, 0.05)  # 1% to 5%
        profit_margin = np.random.triangular(0.1, 0.2, 0.3)  # Min 10%, Mode 20%, Max 30%

        # Calculate the terminal value
        revenue = market_size * market_share
        profit = revenue * profit_margin
        terminal_value = profit * 5  # Assuming a 5x profit multiple

        # Discount the terminal value to the present
        discount_rate = np.random.normal(0.25, 0.05)  # Mean 25%, SD 5%
        present_value = terminal_value / (1 + discount_rate)**5

        valuations.append(present_value)

    mean_val = np.mean(valuations)
    std_val = np.std(valuations)
    percentiles = np.percentile(valuations, [10, 50, 90])
    
    return mean_val, std_val, percentiles

# Run the simulation
mean_valuation, std_valuation, percentiles = monte_carlo_valuation(10000)

print(f"Mean Valuation: ${mean_valuation:,.2f}")
print(f"Standard Deviation: ${std_valuation:,.2f}")
print(f"10th Percentile: ${percentiles[0]:,.2f}")
print(f"50th Percentile (Median): ${percentiles[1]:,.2f}")
print(f"90th Percentile: ${percentiles[2]:,.2f}")
```

### 10.4: IFRS/GAAP-Compliant Disclosure Templates

When disclosing a Level 3 fair value measurement, the following template can be used as a guide:

Fair Value Measurement Disclosure Template

Company Name: [Insert Company Name]
Valuation Date: [Insert Date]
Reporting Period: [Insert Period]

1. Valuation Technique

The fair value of [Asset/Liability] was determined using the [Valuation Technique Name], which is a Level 3 fair value
measurement under IFRS 13 / ASC 820. This technique was selected because [Rationale for Selection].

2. Unobservable Inputs

The key unobservable inputs used in the valuation are:

3. Sensitivity Analysis

The fair value measurement is sensitive to changes in the unobservable inputs. The following table shows the impact of
changes in key inputs on the fair value:

4. Reconciliation

The fair value measurement is reconciled to the financial statements as follows:

5. Valuer Information

The valuation was performed by [Name of Valuer/Firm], who has [Qualifications and Experience]. [Statement of
Independence, if applicable].

### 10.5: IRS 409A Compliance Template

409A Valuation Report Summary

Company Name: [Insert Company Name]
Valuation Date: [Insert Date]
Purpose: Compliance with IRS Section 409A

1. Executive Summary

This report presents the fair market value (FMV) of the common stock of [Company Name] as of [Valuation Date] for the
purpose of complying with IRS Section 409A.

2. Company Overview

[Brief description of the company, its business, industry, and stage of development]

3. Valuation Methodology

The FMV was determined using [Valuation Method(s)], which is/are appropriate for a company at this stage of development.
The method(s) used include:

[Method 1]: [Brief description]

[Method 2]: [Brief description]

4. Key Assumptions

The valuation is based on the following key assumptions:

[Assumption 1]

[Assumption 2]

[Assumption 3]

5. Valuation Conclusion

Based on the analysis performed, the FMV of the common stock as of [Valuation Date] is $[Amount] per share.

6. Allocation of Value

The enterprise value was allocated among the various classes of equity as follows:

7. Discount for Lack of Marketability (DLOM)

A discount of [X]% was applied to account for the lack of marketability of the common stock.

8. Certification

This valuation was performed by [Name], [Title], who has [Qualifications]. The valuation is intended to comply with the
safe harbor provisions of IRS Section 409A.


### Key Takeaways


Structured frameworks provide consistency: Well-designed valuation models for Scorecard, Berkus, VC Method, and DCF
ensure no steps are missed and formulas are correct

Advanced analysis provides deeper insights: Monte Carlo simulation, sensitivity analysis, and scenario planning help
quantify uncertainty and risk

| Class of Equity | Shares Outstanding | Value per Share | Total Value |
| :--- | :--- | :--- | :--- |
| Preferred Stock | [Number] | $[Amount] | $[Amount] |
| Common Stock | [Number] | $[Amount] | $[Amount] |
| Total | [Number] |  | $[Amount] |

Documentation ensures compliance: IFRS 13, ASC 820, and 409A valuations require thorough documentation and disclosure of
assumptions and methodologies

Systematic processes prevent errors: Checklists for data gathering, assumption validation, and quality control help
ensure accuracy and completeness

Industry-specific approaches are essential: SaaS companies require ARR and NRR analysis, biotech needs clinical trial
probability modeling, marketplaces need GMV and take rate evaluation

Version control is critical: Track changes to assumptions, data, and methodology over time to show evolution of
valuation

Frameworks should enhance, not replace, judgment: Valuation models and methodologies are aids to analysis, not
substitutes for critical thinking and professional skepticism


### Exercises for Chapter 10

#### ⭐ Basic Understanding

1. What is the formula for the Scorecard Method?

2. What is the maximum valuation under the Berkus Method?

3. In the Venture Capital Method, how is the pre-money valuation calculated?

4. What is the purpose of a Monte Carlo simulation in valuation?

5. What is a Level 3 fair value measurement?

6. What is the purpose of a sensitivity analysis in a valuation report?

7. What is the safe harbor provision under IRS 409A?

8. What is a discount for lack of marketability (DLOM)?

9. In the Black-Scholes model, what does N(d1) represent?

10. What is the formula for the Risk Factor Summation Method?

11. What are the three main valuation approaches permitted by IFRS 13?

12. What is the purpose of a 409A valuation?

13. What is the formula for expected value in scenario analysis?

14. What is the P/S ratio?

15. What is the key difference between post-money and pre-money valuation?

#### ⭐⭐ Intermediate Application

#### ⭐⭐⭐ Advanced Analysis

#### 💭 Discussion Questions

#### 🔬 Research Projects


### Solutions for Chapter 10

#### ⭐ Basic Understanding

1. Scorecard Method formula: Valuation = Average Pre-Money Valuation \times Weighted Score.

2. Maximum valuation under Berkus Method: $2,500,000 (five factors × $500,000 each).

$$
3. Pre-money valuation = Post-money valuation - Investment amount.
$$

4. Monte Carlo simulation generates a probability distribution of valuations by running thousands of simulations with
random inputs, providing a range of possible outcomes rather than a single point estimate.

5. A Level 3 fair value measurement uses unobservable inputs based on the entity’s own assumptions and requires
extensive disclosure.

6. A sensitivity analysis shows how the valuation changes with different assumptions, helping users understand the key
drivers of value and the range of possible outcomes.

7. The safe harbor provision provides protection from IRS challenges if the valuation is performed by a qualified
independent appraiser and meets certain criteria.

8. A DLOM is a discount applied to the value of an asset to reflect the difficulty of selling it due to the lack of an
active market.

9. N(d1) represents the cumulative distribution function of the standard normal distribution evaluated at d1, which is
used to calculate the option delta and the option value.

10. Risk Factor Summation Method formula: Valuation = Base Value + (Sum of Risk Factor Adjustments).

11. Three main valuation approaches permitted by IFRS 13: Market approach, income approach, and cost approach.

12. A 409A valuation determines the fair market value of a company’s common stock for the purpose of complying with IRS
Section 409A, which governs the taxation of stock options and other deferred compensation.

13. Expected value formula in scenario analysis: EV = \Sigma (Probability of Scenario \times Valuation in Scenario).

14. P/S ratio = Price-to-Sales ratio, calculated as Market Capitalization \div Revenue.

15. Post-money valuation includes the new investment, while pre-money valuation is the value before the investment.
Pre-money = Post-money - Investment.


