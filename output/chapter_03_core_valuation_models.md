# Chapter 3: Core Valuation Models

## Core Valuation Models


### Learning Objectives

By the end of this chapter, readers will be able to:

Apply the Scorecard Method to value a pre-revenue startup by selecting appropriate factors, weights, and scores

Calculate valuations using the Berkus Method by assessing which risk factors have been mitigated

Implement the Risk Factor Summation Method by rating 12 key risk factors and computing adjustments

Derive post-money and pre-money valuations using the Venture Capital Method with terminal value projections

Prove key mathematical properties of each method including linearity, normalization, and sensitivity

Compare the strengths and weaknesses of qualitative versus market-based valuation approaches

Evaluate the appropriateness of each method for different company stages, industries, and stakeholder perspectives


This chapter delves into the core valuation models specifically designed for pre-revenue and pre-profit companies. These
models move away from traditional discounted cash flow analysis and instead focus on qualitative and market-based
factors. We will formalize these models mathematically, provide proofs of their key properties, and illustrate their
application with worked examples.

### 3.1: The Scorecard Method

The Scorecard Method, developed by Bill Payne in 2001, is a popular technique among angel investors for valuing
pre-revenue startups. It works by comparing the target company to a baseline of similar startups and adjusting the
valuation based on a set of key criteria.

Formalization as a Weighted Sum Model

Let be the average pre-money valuation of pre-revenue companies in the same region and industry as the target company.
The Scorecard Method adjusts this average valuation based on a set of factors. We can formalize this as a weighted sum
model.

$$V_{avg}$$

Let the set of factors be , and let the corresponding weights be , such that . For each factor , we assign a score that
represents how the target company compares to the average company in that category. The score is typically a multiplier,
where a score of 1.0 means the company is average, a score greater than 1.0 means the company is above average, and a
score less than 1.0 means the company is below average.

$$F={f_{1},f_{2},...,f_{n}}$$

$$W={w_{1},w_{2},...,w_{n}}$$

$$\sum_{i=1}^{n} w_{i}=1$$

$$f_{i}$$

$$s_{i}$$

The valuation of the target company, , is then calculated as:

$$V_{target}$$

$$V_{target}=V_{avg}×\sum_{i=1}^{n} w_{i}s_{i}$$

Theorem 3.1 (Linearity of the Scorecard Method): The Scorecard Method is a linear function of the factor scores.

Proof: The valuation formula is a linear combination of the scores , with coefficients . Therefore, the model is linear.
This property means that if we double all the scores, the valuation will also double (assuming the average valuation
remains constant). ∎

$$V_{target}=V_{avg}×\sum_{i=1}^{n} w_{i}s_{i}$$

$$s_{i}$$

$$V_{avg}×w_{i}$$

Theorem 3.2 (Normalization): If all factor scores are equal to 1 (i.e., the company is perfectly average), the valuation
is equal to the average valuation.

Proof: If  for all , then the valuation formula becomes:

$$s_{i}=1$$

$$i$$

$$V_{target}=V_{avg}×\sum_{i=1}^{n} w_{i}(1)=V_{avg}×\sum_{i=1}^{n} w_{i}$$

Since the weights sum to 1, . Therefore:

$$\sum_{i=1}^{n} w_{i}=1$$

$$V_{target}=V_{avg}×1=V_{avg}$$

This normalization property ensures that the Scorecard Method is properly calibrated to the market. ∎

Properties and Special Cases:

The Scorecard Method has several important properties. First, it is sensitive to the choice of weights. Different
investors may assign different weights to the same factors based on their investment philosophy. Second, the method
requires a reliable estimate of the average valuation for comparable companies. This can be obtained from industry
databases, angel investor networks, or recent financing rounds. Third, the scores are subjective and require judgment.
It is important to document the rationale for each score to ensure transparency and consistency.

📊 Real World Example: Dropbox Seed Round Valuation (2007)

When Dropbox raised its seed round in 2007, the company was pre-revenue with just a demo video and waiting list. Y
Combinator and Sequoia Capital valued the company at approximately $4 million post-money for a $1.2 million investment.

Scorecard Method Analysis (Reconstructed):

Average pre-revenue cloud storage startup valuation (2007): ~$2 million

Calculated Valuation: $2M × 1.50 = $3M (close to actual $4M post-money)

Outcome: - 2008: $6M Series A at $30M valuation - 2011: $250M Series B at $4B valuation - 2018: IPO at $9.2B valuation -
Peak market cap: $12B+

Lesson: The Scorecard Method captured the key value drivers (team, market, viral traction) that justified a premium to
average valuations. The 1.5x multiplier proved conservative--the actual outcome was 2,000x the seed valuation.

Source: TechCrunch, Dropbox S-1 filing


Figure 3.1: Scorecard Method Factors

.

Worked Example 3.1:

An angel investor is valuing a pre-revenue SaaS startup in Silicon Valley. The average pre-money valuation for similar
startups is $1.5 million. The investor uses the following factors and weights:

The valuation of the startup is:

$$V_{target}=$1,500,000×1.200=$1,800,000$$

Worked Example 3.2:

A European fintech startup is being valued using the Scorecard Method. The average valuation for comparable companies is
\text{€}2 million. The scores are: Management (40%, score 1.3), Market (30%, score 1.1), Technology (20%, score 1.4),
Competition (10%, score 0.9). The weighted score is:

$$S=0.40×1.3+0.30×1.1+0.20×1.4+0.10×0.9=0.52+0.33+0.28+0.09=1.22$$

| Scenario | Probability | Valuation |
| :--- | :---: | :---: |
| Best Case | 20% | $10,000,000 |
| Base Case | 60% | $5,000,000 |
| Worst Case | 20% | $1,000,000 |

The valuation is:

$$V=€2,000,000×1.22=€2,440,000$$

Regulatory Notes (IFRS/GAAP):

The Scorecard Method is a Level 3 valuation technique under the IFRS 13 and ASC 820 fair value hierarchy. This is
because it relies on unobservable inputs, such as the subjective scores assigned to each factor. When using the
Scorecard Method for financial reporting, it is crucial to document the rationale for the chosen factors, weights, and
scores, as well as the source of the average valuation. A sensitivity analysis should also be performed to show how the
valuation changes with different assumptions.

### 3.2: The Berkus Method

The Berkus Method, created by venture capitalist Dave Berkus in the 1990s, is a simple and intuitive valuation tool for
pre-revenue startups. It assigns a monetary value to the key risk factors that have been mitigated by the startup.

Mathematical Definition

The Berkus Method assigns a value of up to $500,000 for each of the following five key success factors:

Sound Idea (Basic Value): The business idea is sound and has a clear value proposition.

Prototype (Reduces Technology Risk): The company has a working prototype of its product.

Quality Management Team (Reduces Execution Risk): The management team has the skills and experience to execute the
business plan.

Strategic Relationships (Reduces Market Risk): The company has established key partnerships that will help it reach its
target market.

Product Rollout or Sales (Reduces Financial Risk): The company has started to generate revenue or has a clear path to
generating revenue.

The valuation of the company is the sum of the values assigned to each of these factors. The maximum valuation under the
Berkus Method is $2.5 million.

Let  be the value assigned to factor , where . The valuation of the company, , is given by:

$$v_{i}$$

$$i$$

$$0≤v_{i}≤500,000$$

$$V$$

$$V=\sum_{i=1}^{5} v_{i}$$

Properties and Bounds:

The Berkus Method has a clear lower bound of $0 (if the company has mitigated none of the risk factors) and an upper
bound of $2.5 million (if the company has fully mitigated all five risk factors). The method is additive, meaning that
each risk factor contributes independently to the valuation. This simplicity is both a strength and a limitation. It
makes the method easy to apply, but it does not account for interactions between the risk factors.

📊 Real World Example: Uber’s Angel Round Valuation (2009)

When Uber (then “UberCab”) raised its angel round in 2009, it was pre-revenue with just a prototype app and a handful of
black car drivers in San Francisco. The company raised $200K at approximately $1.5-2M valuation.

Berkus Method Analysis (Reconstructed):

Outcome: - 2010: Series A at $60M valuation - 2011: Series B at $330M valuation - 2014: Series D at $17B valuation -
2019: IPO at $82B valuation - Peak market cap: $120B+

Lesson: The Berkus Method appropriately identified that Uber had mitigated technology, execution, and idea risk, but not
yet market or financial risk. The $1.7M valuation proved extremely conservative—actual outcome was 70,000x. This
demonstrates both the method’s utility for early-stage assessment and the extreme uncertainty in startup outcomes.

Source: TechCrunch, Uber S-1 filing, “Super Pumped” by Mike Isaac


Worked Example 3.3:

A pre-revenue startup has a strong management team, a working prototype, and a sound business idea. However, it has not
yet established any strategic relationships or started its product rollout. The valuation using the Berkus Method would
be:

Worked Example 3.4:

A biotech startup has a sound idea ($500,000), a prototype ($400,000), a quality management team ($500,000), strategic
relationships with two major pharmaceutical companies ($500,000), but no product rollout yet ($0). The valuation is:

$$V=$500,000+$400,000+$500,000+$500,000+$0=$1,900,000$$

Regulatory Notes (IFRS/GAAP):

Like the Scorecard Method, the Berkus Method is a Level 3 valuation technique. The values assigned to each factor are
subjective and based on unobservable inputs. It is important to document the reasoning behind the assigned values to
support the valuation for financial reporting purposes. The method is most appropriate for early-stage, pre-revenue
companies and may not be suitable for companies that have already started generating significant revenue.


### Key Takeaways


The Scorecard Method is a weighted comparison approach that adjusts average market valuations based on company-specific
factors, with mathematical properties of linearity and normalization

The Berkus Method values risk mitigation by assigning up to $500K per factor (max $2.5M total), making it simple but not
accounting for factor interactions

Both methods are Level 3 valuations under IFRS 13/ASC 820, requiring extensive documentation of subjective inputs and
sensitivity analysis

Real examples (Dropbox, Uber) show extreme outcomes: Initial valuations of $1.5-4M grew to $9-120B, demonstrating both
the methods’ utility and the inherent uncertainty

Weight selection is critical in Scorecard Method: Different investors prioritize different factors (team vs. market vs.
product) based on investment philosophy

Berkus Method works best for very early stage: Pre-revenue companies where risk mitigation is the primary value driver

Documentation and transparency are essential: Both for regulatory compliance and for updating valuations as companies
progress


### Exercises for Chapter 3

#### ⭐ Basic Understanding

1. Using the Scorecard Method, calculate the valuation of a startup if the average valuation is $2M and the weighted
score is 1.35.

2. A company using the Berkus Method has mitigated all five risk factors at $500K each. What is the valuation?

3. In the Scorecard Method, what does a score of 0.8 for a factor mean?

| Scenario | Probability | Valuation |
| :--- | :---: | :---: |
| Rapid Growth | 15% | $20,000,000 |
| Moderate Growth | 50% | $8,000,000 |
| Slow Growth | 25% | $3,000,000 |
| Market Decline | 10% | $500,000 |

4. What is the maximum valuation possible under the Berkus Method?

5. Prove that if all Scorecard factors are scored at 1.0, the valuation equals the average valuation.

#### ⭐⭐ Intermediate Application

6. A SaaS startup is being valued using the Scorecard Method. The average valuation is $3M. Scores are: Team (30%, 1.4),
Market (25%, 1.6), Product (20%, 1.2), Competition (15%, 0.9), Sales (10%, 1.1). Calculate the valuation.

7. Compare the Scorecard and Berkus methods. When would you use each? Provide specific scenarios.

8. A biotech company has: Sound Idea ($500K), Prototype ($300K), Team ($450K), Relationships ($400K), Sales ($0). What
is the Berkus valuation? What does this tell you about the company’s stage?

9. In the Scorecard Method, an investor weights Management at 40% (score 1.5) and Market at 30% (score 1.2). If the
average valuation is $2.5M and other factors are neutral (score 1.0, weight 30%), what is the valuation?

10. Explain why both methods are classified as Level 3 under IFRS 13. What documentation would be required?

#### ⭐⭐⭐ Advanced Analysis

11. A startup receives two valuations: Scorecard Method yields $4M, Berkus Method yields $1.8M. Analyze why these might
differ and which you would trust more. What does the discrepancy tell you?

12. Derive the sensitivity of Scorecard valuation to a single factor. If Management weight is 30%, average valuation is
$2M, and the Management score increases from 1.2 to 1.5, what is the change in valuation?

13. Design a modified Berkus Method for a late-stage pre-revenue company (e.g., biotech in Phase 3 trials). What factors
would you change and why? What should the maximum valuation be?

14. A company is valued at $3M using Scorecard Method with these factors: Team (35%, 1.6), Market (30%, 1.4), Product
(20%, 1.1), Competition (15%, 0.8). What was the average valuation used? Show your work.

15. Critically evaluate the assumption in Berkus Method that each risk factor contributes independently. Provide an
example where factors interact and explain how this affects valuation.

#### 💭 Discussion Questions

16. Both Dropbox and Uber were initially valued at $1.5-4M and grew to $9-120B. Does this mean the initial valuations
were “wrong”? What does this tell us about the nature of startup valuation?

17. Should different industries use different weights in the Scorecard Method? For example, should biotech weight “Team”
higher than SaaS companies? Defend your position.

18. The Berkus Method caps valuation at $2.5M. Is this still appropriate in 2024, or should it be updated for inflation
and market changes?

#### 🔬 Research Projects

19. Research 10 actual seed-stage investments from the past 5 years. Estimate what their Scorecard valuations would have
been and compare to actual deal prices. What patterns emerge?

20. Interview 3-5 angel investors or VCs about which valuation methods they actually use in practice. Do they use
Scorecard or Berkus? How do they modify these methods?


### Solutions for Chapter 3

#### ⭐ Basic Understanding

1. Valuation = Average valuation × Weighted score = $2M × 1.35 = $2.7M.

$$
2. Valuation = 5 factors \times $500K each = $2.5M (maximum possible).
$$

3. A score of 0.8 means the company is 20% below average for that factor (80% of average performance).

4. The maximum valuation is $2.5M (5 factors × $500K each).

5. Proof: Valuation = Average valuation \times \Sigma(weight \times score). If score = 1.0 for all factors,
\Sigmaweights = 1, so Valuation = Average valuation.

#### ⭐⭐ Intermediate Application

$$
6. Weighted score = (0.30\times1.4)+(0.25\times1.6)+(0.20\times1.2)+(0.15\times0.9)+(0.10\times1.1) =
0.42+0.40+0.24+0.135+0.11 = 1.305. Valuation = $3M \times 1.305 = $3.915M.
$$

7. Scorecard: Use when comparable market data exists and you want to benchmark against similar companies. Best for
Series A/B with some traction. Berkus: Use for very early stage (pre-revenue, pre-product) when risk mitigation is the
primary value. Best for seed/angel rounds.

8. Berkus valuation = $500K+$300K+$450K+$400K+$0 = $1.65M. Interpretation: Company is in late development stage (has
prototype and relationships) but hasn’t launched product yet.

$$
9. Weighted score = (0.40\times1.5)+(0.30\times1.2)+(0.30\times1.0) = 0.6+0.36+0.3 = 1.26. Valuation = $2.5M \times 1.26
= $3.15M.
$$

10. Both are Level 3 because they rely on unobservable inputs: subjective scores/values assigned by the valuer, not
market prices. Required documentation: rationale for each score/value, source of average valuation, comparable company
data, sensitivity analysis, valuer qualifications, date of valuation.

#### ⭐⭐⭐ Advanced Analysis

11. Differences arise because Scorecard uses market comparables and qualitative factors, while Berkus uses fixed dollar
amounts for risk mitigation. Trust depends on stage: Scorecard better for later seed/Series A, Berkus better for very
early stage. Discrepancy shows subjectivity and stage-dependence.

$$
12. Change in valuation = Average valuation \times weight \times (new score - old score) = $2M \times 0.30 \times (1.5 -
1.2) = $2M \times 0.30 \times 0.3 = $180K.
$$

13. Modified Berkus for late-stage: Increase cap to $10M, add factors like regulatory approval, manufacturing readiness,
strategic partnerships. Maximum valuation should reflect reduced risk at late stage.

$$
14. Weighted score = (0.35\times1.6)+(0.30\times1.4)+(0.20\times1.1)+(0.15\times0.8) = 0.56+0.42+0.22+0.12 = 1.32.
Average valuation = $3M / 1.32 \approx $2.27M.
$$

15. Factors often interact (e.g., strong team accelerates product development). Independent assumption may overstate
combined effect. Example: Team and Technology both scored high may not double impact if one drives the other.

#### 💭 Discussion Questions

16-18. These are open-ended discussion questions with no single correct answer. Instructors should facilitate debate and
encourage students to support positions with evidence and reasoning.

#### 🔬 Research Projects

19-20. These research projects require students to gather and analyze external information. Grading should focus on
research quality, analytical rigor, and clarity of presentation rather than specific conclusions.

