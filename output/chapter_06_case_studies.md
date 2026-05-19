# Chapter 6: Case Studies

## Case Studies


### Learning Objectives

By the end of this chapter, readers will be able to:

Apply multiple valuation methods (Scorecard, VC Method, Real Options, Comparables) to the same company and reconcile the
results

Select the most appropriate valuation method(s) based on company stage, data availability, and stakeholder requirements

Document all assumptions, data sources, and methodologies in a format suitable for regulatory compliance and audit

Perform sensitivity analysis to identify key value drivers and assess the impact of assumption changes

Reconcile different valuation approaches by understanding the economic drivers behind each method

Present valuation findings professionally with appropriate caveats, ranges, and risk disclosures

Critique existing valuations by identifying methodological flaws, unrealistic assumptions, and missing risk factors



This chapter applies the valuation models discussed in the previous chapters to three hypothetical case studies: a
technology startup, a biotechnology company, and a Software-as-a-Service (SaaS) business. These case studies provide a
practical demonstration of how to value pre-revenue and pre-profit companies in different industries.

### 6.1: Case Study 1: Tech Startup - “InnovateAI”

InnovateAI is a pre-revenue startup that has developed a proprietary artificial intelligence algorithm for image
recognition. The company is seeking $1 million in seed funding. The management team consists of experienced AI
researchers and entrepreneurs. The company has filed for patent protection and has a working prototype. The market for
image recognition is large and growing, but there are several established competitors.

Valuation using the Scorecard Method

Average Pre-Money Valuation: $2 million (based on comparable seed-stage AI startups in the region)

Factors and Scores:

Valuation:

$$$2,000,000×1.350=$2,700,000$$

Compliance Notes:

This valuation is a Level 3 fair value measurement under IFRS 13 and ASC 820. The key unobservable inputs are the
average pre-money valuation and the subjective scores. The valuation report should document the source of the average
valuation (e.g., industry databases, recent financing rounds) and the rationale for each score. A sensitivity analysis
should show how the valuation changes if the scores are adjusted.

### 6.2: Case Study 2: Biotechnology Company - “BioCure”

BioCure is a pre-revenue biotechnology company that is developing a new drug for a rare genetic disease. The company has
completed pre-clinical trials and is seeking funding for Phase I clinical trials. The drug, if successful, could
generate substantial revenue, but the probability of success is uncertain. The company has a strong scientific team and
has established partnerships with leading research institutions.

Valuation using Real Options Analysis

Underlying Asset: The expected future cash flows from the drug if it is successfully commercialized. Based on market
analysis, the present value of these cash flows is estimated to be $500 million.

Strike Price: The cost of completing the clinical trials and obtaining regulatory approval, which is estimated to be
$100 million.

Time to Maturity: The time it will take to complete the clinical trials, which is estimated to be 5 years.

Volatility: The volatility of the stock prices of publicly traded biotechnology companies with similar drug candidates,
which is estimated to be 60%.

Risk-Free Rate: 4%

Using the Black-Scholes model:

$$d_{1}=\frac{ln(\frac{500}{100})+(0.04+\frac{0.6^{2}}{2})(5)}{0.6\sqrt{5}}=\frac{ln(5)+0.04×5+0.18×5}{0.6×2.236}=\frac{1.609+0.2+0.9}{1.342}=\frac{2.709}{1.342}=2.02$$

$$d_{2}=2.02-0.6\sqrt{5}=2.02-1.342=0.68$$

$$N(d_{1})≈0.9783, N(d_{2})≈0.7517$$

$$C=(0.9783×500)-(0.7517×100×e^{-0.04×5})=489.15-(75.17×0.8187)=489.15-61.53=$427.62 million$$

The value of the real option to develop the drug is approximately $428 million. This is the valuation of the company
today, reflecting the value of the flexibility to proceed with or abandon the drug development based on the results of
the clinical trials.

Compliance Notes:

This valuation is also a Level 3 measurement. The key unobservable inputs are the present value of future cash flows
($500 million), the cost to complete development ($100 million), and the volatility (60%). The valuation report should
explain how these inputs were estimated and should include a sensitivity analysis showing the impact of different
assumptions.

### 6.3: Case Study 3: SaaS Company - “CloudFlow”

CloudFlow is a pre-revenue SaaS company that has developed a project management tool for remote teams. The company has a
working product and a small number of beta users. The company is seeking $1.5 million in Series A funding. The market
for project management tools is competitive, but CloudFlow has a unique feature set that differentiates it from
competitors.

Valuation using the Venture Capital Method

Terminal Value: The company is projected to have $20 million in revenue in 5 years. The average P/S multiple for
publicly traded SaaS companies is 8x. The terminal value is:

$$Terminal Value=$20,000,000×8=$160,000,000$$

Expected ROI: The venture capitalist requires a 20x return on investment.

Post-Money Valuation:

$$Post-money Valuation=\frac{$160,000,000}{20}=$8,000,000$$

Investment Amount: $1,500,000

Pre-Money Valuation:

$$Pre-money Valuation=$8,000,000-$1,500,000=$6,500,000$$

Compliance Notes:

This valuation is a Level 3 measurement. The key unobservable inputs are the projected revenue ($20 million), the P/S
multiple (8x), and the expected ROI (20x). The valuation report should document the basis for the revenue projection
(e.g., market analysis, customer acquisition model) and the source of the P/S multiple (e.g., publicly traded
comparables). A sensitivity analysis should show how the valuation changes with different assumptions about revenue,
multiples, and ROI.


### Key Takeaways


Multiple methods should always be used: No single valuation approach is definitive for pre-revenue
companies--triangulation across 2-3 methods provides confidence bounds

Method selection depends on stage: Berkus/Scorecard for pre-product, VC Method for Series A/B, Comparables for later
stage, Real Options for binary outcomes

Documentation is as important as calculation: Regulatory compliance and litigation defense require extensive
documentation of assumptions, sources, and methodology

Sensitivity analysis reveals key drivers: Identifying which assumptions have the largest impact (e.g., exit multiple,
growth rate) focuses due diligence efforts

| Factor | Weight | Score | Weighted Score |
| :--- | :---: | :---: | :---: |
| Strength of Management Team | 30% | 1.25 | 0.375 |
| Size of Opportunity | 25% | 1.5 | 0.375 |
| Product/Technology | 15% | 1.2 | 0.180 |
| Competitive Environment | 10% | 0.75 | 0.075 |
| Marketing/Sales Channels | 10% | 1.0 | 0.100 |
| Need for Additional Funding | 5% | 0.9 | 0.045 |
| Other | 5% | 1.0 | 0.050 |
| Total | 100% |  | 1.200 |

Valuation ranges are more honest than point estimates: Given the uncertainty, presenting a range (e.g., $15-25M) is more
credible than false precision ($19.7M)

Industry-specific factors dominate: SaaS companies are valued on ARR and NRR, biotech on clinical trial probabilities,
marketplaces on GMV and take rates

Real case studies show extreme variance: Tech startup valued at $2M → $50M (25x), biotech at $15M → $0 (failure), SaaS
at $8M → $200M (25x)—outcomes vary wildly


### Exercises for Chapter 6

#### ⭐ Basic Understanding

1. Recalculate the valuation of InnovateAI if the competition score is 1.0 and the sales & marketing score is 1.2.

2. What is the pre-money valuation of CloudFlow if the venture capitalist requires a 25x return on investment?

3. If the volatility in the BioCure case increases to 70%, how does this affect the real option value?

4. What is the ownership percentage of the investor in CloudFlow after the $1.5 million investment?

5. If InnovateAI’s average pre-money valuation changes to $2.5 million, what is the new valuation?

#### ⭐⭐ Intermediate Application

6. Calculate the post-money valuation for CloudFlow if the terminal value is $200 million and the required ROI is 15x.

7. In the BioCure case, what happens to the option value if the time to maturity increases to 7 years?

8. What is the weighted score for InnovateAI in Exercise 1?

9. If the P/S multiple for CloudFlow increases to 10x, what is the new terminal value?

10. What is the strike price in the BioCure real options analysis?

#### ⭐⭐⭐ Advanced Analysis

11. Calculate the pre-money valuation for CloudFlow if the post-money valuation is $10 million and the investment is $2
million.

12. In the InnovateAI case, which factor has the highest weight?

13. What is the present value of the underlying asset in the BioCure case?

14. If CloudFlow’s projected revenue increases to $25 million, what is the new terminal value (assuming P/S = 8x)?

15. What valuation method is most appropriate for a company with high uncertainty and valuable managerial flexibility?

#### 💭 Discussion Questions

16. Discuss why multiple valuation methods should be used for startups rather than relying on a single method.

17. How do qualitative factors such as team quality and strategic partnerships influence valuation compared to
quantitative metrics?

18. Should real options valuation be applied to all startups or only those in certain industries? Explain your
reasoning.

#### 🔬 Research Projects

19. Research a recent startup acquisition and analyze which valuation methods were likely used. Compare to methods
discussed in this chapter.

20. Investigate how sensitivity analysis is presented in actual valuation reports for early-stage companies. Summarize
best practices.

### Solutions for Chapter 6

#### ⭐ Basic Understanding

1. Weighted Score recalculation: Adjust competition score to 1.0 and sales & marketing to 1.2; compute new weighted
score and multiply by average valuation.

2. Pre-money valuation = (Terminal Value / ROI) - Investment. With ROI = 25x, compute accordingly.

3. Higher volatility increases real option value because option value grows with uncertainty; expect a noticeable
increase from original value.

4. Ownership percentage = Investment / Post-money valuation.

5. New valuation = Weighted Score × $2.5 million.

#### ⭐⭐ Intermediate Application

6. Post-money valuation = Terminal Value / ROI; then compute pre-money if needed.

7. Longer time to maturity increases option value due to extended flexibility; calculate using Black-Scholes inputs.

8. Weighted score from Exercise 1 remains as recalculated in question 1.

9. Terminal value = Projected revenue \times P/S multiple; with P/S = 10x, compute accordingly.

10. Strike price in BioCure case = $100 million (cost to complete development).

#### ⭐⭐⭐ Advanced Analysis

$$
11. Pre-money valuation = Post-money valuation - Investment.
$$

12. Highest weight factor in InnovateAI case: Management Team (30%).

13. Present value of underlying asset in BioCure case = $500 million.

$$
14. Terminal value = $25 million \times 8 = $200 million.
$$

15. Real Options Valuation is most appropriate for companies with high uncertainty and valuable managerial flexibility.

#### 💭 Discussion Questions

16-18. These are open-ended questions; responses should include reasoning based on chapter concepts and examples.

#### 🔬 Research Projects

19-20. These projects require external research; evaluation should focus on methodology, data quality, and analytical
rigor.

