# Chapter 9: Common Pitfalls

## Common Pitfalls


### Learning Objectives

By the end of this chapter, readers will be able to:

Identify common valuation errors including TAM overestimation, dilution miscalculation, and discount rate
misspecification

Recognize cognitive biases that distort valuation including anchoring, confirmation bias, and overconfidence

Avoid circular reasoning in valuation (e.g., using valuation to justify valuation)

Perform sanity checks to detect unrealistic assumptions (e.g., implied market share >100%, impossible growth rates)

Adjust for survivorship bias when using historical VC return data

Account for dilution properly in multi-round financing scenarios

Critique third-party valuations by identifying red flags such as missing sensitivity analysis, cherry-picked
comparables, or unrealistic projections



Valuing pre-revenue and pre-profit companies is an inherently difficult task, and there are many pitfalls that can lead
to inaccurate and unreliable valuations. This chapter discusses some of the most common pitfalls and provides guidance
on how to avoid them.

### 9.1: Overestimating the Total Addressable Market (TAM)

One of the most common errors in startup valuation is overestimating the Total Addressable Market (TAM). The TAM is the
total market demand for a product or service, and it is a key input into many valuation models. An inflated TAM will
lead to an inflated valuation.

Theorem 9.1 (Valuation Bias from TAM Overestimation): Overestimating the TAM leads to a positive bias in the valuation.

Proof: Let the true TAM be and the estimated TAM be , where . Let the valuation be a function of the TAM, . If the
valuation is an increasing function of the TAM, which is typically the case (i.e., ), then . The bias in the valuation
is . This proves that overestimating the TAM leads to a positive bias in the valuation.

$$T$$

$$T$$

$$T>T$$

$$V(T)$$

$$\frac{∂V}{∂T}>0$$

$$V(T)>V(T)$$

$$V(T)-V(T)>0$$

How to Avoid This Pitfall

To avoid this pitfall, it is important to be realistic and conservative when estimating the TAM. Use a bottom-up
approach, starting with the number of potential customers and the average revenue per customer, rather than a top-down
approach, which starts with a large market and then tries to estimate the company’s share of that market. The bottom-up
approach is more grounded in reality and less prone to overestimation.

Worked Example 9.1:

A startup claims that the TAM for its product is $10 billion, based on a top-down estimate of the entire industry.
However, a bottom-up analysis reveals that there are only 100,000 potential customers, each willing to pay an average of
$500 per year. The realistic TAM is:

$$TAM=100,000×$500=$50,000,000=$50 million$$

The top-down estimate overstates the TAM by a factor of 200.

### 9.2: Other Common Pitfalls

Ignoring the Competitive Landscape

It is important to consider the strength and number of competitors when valuing a company. A company in a highly
competitive market will have a lower valuation than a company in a market with few competitors. Failing to account for
competition can lead to overvaluation.

Underestimating the Time and Cost of Execution

Building a successful company takes time and money. It is important to be realistic about the time and cost of executing
the business plan. Underestimating these factors can lead to a valuation that does not account for the need for
additional financing or the risk of delays.

Using Inappropriate Valuation Multiples

When using market comparables, it is important to use multiples from companies that are truly comparable to the target
company. Using multiples from companies in different industries, at different stages of development, or with different
growth prospects can lead to inaccurate valuations.

Failing to Account for Dilution

The valuation of a company should be performed on a fully diluted basis, taking into account the potential dilutive
effect of stock options, warrants, SAFEs, convertible notes, and other convertible securities. Failing to account for
dilution can lead to an overstatement of the value per share.

Over-reliance on Management Projections

Management projections are inherently optimistic and may not reflect the true range of possible outcomes. It is
important to critically evaluate management projections and to perform sensitivity analyses to understand the impact of
different assumptions.

Worked Example 9.2:

A company has 1 million shares outstanding and a valuation of $10 million, giving a value per share of $10. However,
there are also 200,000 stock options outstanding. On a fully diluted basis, there are 1.2 million shares, and the value
per share is:

$$Value per Share=\frac{$10,000,000}{1,200,000}=$8.33$$

Failing to account for the stock options overstates the value per share by 20%.

📊 Real World Example: Quibi’s $1.75 Billion Failure - TAM Overestimation (2020)

Quibi (short for “quick bites”) raised $1.75 billion from top-tier investors to launch a mobile-only streaming service
with 10-minute episodes. The company shut down after just 6 months, making it one of the most spectacular startup
failures in history. The core problem: massive TAM overestimation.

The Valuation Pitch (2018-2019): - TAM Claim: “Mobile video market is $100 billion+” - Logic: People spend 5+ hours/day
on phones, video is dominant format - Projected subscribers: 7.4 million in Year 1, 20+ million by Year 3 - Valuation:
$1.75 billion raised pre-launch - Investors: Disney, NBCUniversal, Alibaba, Goldman Sachs

The Fatal Flaws: 1. TAM Confusion: Conflated total mobile video viewing with addressable market for paid short-form
content - Total mobile video: $100B+ (mostly YouTube, TikTok, social media - all free) - Paid short-form streaming: $0
(market didn’t exist) - Actual TAM: ~$0-1B, not $100B

Market Misunderstanding:

Assumed people would pay $5-8/month for 10-minute shows

Ignored that mobile video users expect free content (YouTube, TikTok)

Ignored that premium video viewers want long-form (Netflix, HBO)

| Input | Value/Range | Source/Rationale |
| :---: | :--- | :--- |
| [Input 1] | [Value] | [Explanation] |
| [Input 2] | [Value] | [Explanation] |
| [Input 3] | [Value] | [Explanation] |

Created a product for a market that didn’t exist

Valuation Math That Didn’t Work:

At $1.75B valuation, needed ~20M subscribers at $6/month to justify

Actual result: 500,000 subscribers after 6 months (2.5% of target)

Burn rate: $100M+ per quarter on content and marketing

Shut down after 6 months with ~$350M cash remaining

The Valuation Errors: - TAM overestimation: Used total market size instead of addressable market - No customer
validation: Raised $1.75B without testing product-market fit - Ignored competition: YouTube and TikTok offered better
free alternatives - Anchoring bias: Founders’ Hollywood pedigree (Jeffrey Katzenberg, Meg Whitman) created halo effect

Outcome: - April 2020: Launched with 50+ shows, $470M content budget - October 2020: Shut down, sold content library for
~$100M - Total loss: ~$1.65 billion (94% of capital) - Investors: Nearly total loss

Lesson: TAM estimation is the most critical and most commonly overestimated input in startup valuation. Quibi’s failure
shows the danger of: (1) using total market size instead of addressable market, (2) assuming you can create a new market
without validation, (3) ignoring free alternatives, (4) letting founder pedigree override market analysis. A proper TAM
analysis would have revealed the market was <$1B, making a $1.75B valuation impossible to justify.

Source: Wall Street Journal, The Verge, “Billion Dollar Loser” podcast, Quibi press releases

📊 Real World Example: Magic Leap’s Technology Risk Underestimation (2018-2020)

Magic Leap raised $2.6 billion (including a $461M Series C at $6B valuation in 2018) to build augmented reality glasses
that would revolutionize computing. The company massively underestimated technology risk, leading to a product that
couldn’t deliver on promises and a down round at 80% lower valuation.

The Valuation Pitch (2016-2018): - Vision: AR glasses that overlay digital content on real world seamlessly - Technology
claims: “Cinematic reality,” “light field” technology superior to all competitors - Market potential: Replace
smartphones and computers ($500B+ TAM) - Investors: Google, Alibaba, Qualcomm, AT&T, Andreessen Horowitz - 2018
valuation: $6 billion

The Technology Reality: - Promised: Lightweight glasses, wide field of view, all-day battery - Delivered (2018): Bulky
headset, narrow 50° field of view, 3-hour battery - Weight: 316g (vs. 50g for normal glasses) - Price: $2,295 (vs.
$300-500 target) - Performance: Significantly worse than Microsoft HoloLens (launched 2016)

The Valuation Errors: 1. Technology risk underestimation: - Assumed “light field” technology would work at consumer
scale - No working prototype shown to investors before $2B+ raised - Physics and engineering challenges dismissed as
solvable

Comparison to software startups:

Valued like a software company (high multiples)

Actually a hardware company (capital intensive, long development cycles)

Hardware requires working prototypes; software can iterate quickly

Ignoring competitive benchmarks:

Microsoft HoloLens proved AR was possible but with severe limitations

Magic Leap claimed 10x better performance without evidence

Investors didn’t demand proof before deploying billions

Outcome: - 2018: Product launch disappointed, sales <10,000 units - 2019: Layoffs, CEO resigned - 2020: Down round at
$1.2B valuation (80% decline) - 2021: Pivot to enterprise, consumer product abandoned - 2024: Company still not
profitable, total raised >$3.5B

Lesson: Technology risk is often underestimated in deep tech startups. Magic Leap’s failure shows: (1) demand working
prototypes before billion-dollar valuations, (2) hardware is fundamentally different from software—can’t iterate
quickly, (3) extraordinary claims require extraordinary evidence, (4) competitive benchmarks (HoloLens) should inform
risk assessment. A proper technology risk analysis would have assigned <30% probability of success, reducing the $6B
valuation to <$2B.

Source: The Information, Bloomberg, Magic Leap SEC filings, “The Untold Story of Magic Leap” (The Verge)

### Key Takeaways


TAM overestimation is the #1 valuation error: Use bottom-up analysis (# customers \times price) rather than top-down
(total market size), and distinguish between total market and addressable market

Dilution is often miscalculated: Each funding round dilutes existing shareholders; a company raising $10M at $40M
post-money gives up 25%, not 20%

Cognitive biases distort valuation: Anchoring (fixating on first number heard), confirmation bias (seeking supporting
evidence only), and overconfidence (underestimating uncertainty)

Technology risk is systematically underestimated: Deep tech companies (AR, biotech, fusion) often assume technical
problems are solvable when they’re not

Survivorship bias inflates VC returns: Historical data shows successful funds; failed funds disappear from databases,
making VC returns appear higher than reality

Circular reasoning is common: Using valuation to justify valuation (e.g., “we’re worth $50M because we raised at $50M”)
rather than fundamental analysis

Red flags include: Missing sensitivity analysis, cherry-picked comparables, hockey-stick projections, no customer
validation, and extraordinary claims without evidence


### Exercises for Chapter 9

#### ⭐ Basic Understanding

1. A startup is valued at $10 million based on a TAM of $1 billion. If the true TAM is only $500 million, what is the
valuation bias, assuming a linear relationship between valuation and TAM?

2. An analyst is valuing a startup using the P/S multiples of publicly traded companies. What are some of the potential
problems with this approach?

3. A company has 500,000 shares outstanding and 100,000 stock options. What is the fully diluted share count?

4. Why is a bottom-up approach to estimating TAM more reliable than a top-down approach?

5. What is the consequence of underestimating the time and cost of execution?

#### ⭐⭐ Intermediate Application

6. A company is valued at $20 million with 2 million shares outstanding. If there are 400,000 convertible securities,
what is the fully diluted value per share?

7. What is the risk of over-relying on management projections?

| Input | Change | Impact on Fair Value |
| :---: | :---: | :--- |
| [Input 1] | +10% | [Increase/Decrease] by [Amount] |
| [Input 1] | -10% | [Increase/Decrease] by [Amount] |
| [Input 2] | +10% | [Increase/Decrease] by [Amount] |
| [Input 2] | -10% | [Increase/Decrease] by [Amount] |

8. How does ignoring the competitive landscape affect valuation?

9. A startup estimates its TAM using a top-down approach and arrives at $5 billion. A bottom-up analysis shows only
50,000 potential customers at $1,000 each. What is the realistic TAM?

10. What is the valuation bias if the estimated TAM is twice the true TAM and valuation is proportional to TAM?

#### ⭐⭐⭐ Advanced Analysis

11. Why is it important to use comparable companies when applying valuation multiples?

12. A company has a valuation of $15 million and 1.5 million shares outstanding. What is the value per share?

13. If there are 300,000 stock options in the previous question, what is the fully diluted value per share?

14. What is the main problem with using a top-down approach to estimate TAM?

15. How can sensitivity analysis help avoid over-reliance on management projections?

#### 💭 Discussion Questions

16. Discuss why cognitive biases such as anchoring and confirmation bias can distort startup valuations.

17. Should valuation reports always include sensitivity analysis? Why or why not?

18. How can survivorship bias affect the interpretation of historical venture capital returns?

19. Debate whether technology risk is systematically underestimated in deep tech valuations.

#### 🔬 Research Projects

20. Research three recent startup failures and identify which valuation pitfalls contributed most to their collapse.

21. Analyze five venture capital term sheets and identify how valuation assumptions are reflected in deal structures.

22. Compare TAM estimates for three companies using both top-down and bottom-up approaches. Which method proved more
accurate post-launch?

23. Investigate how dilution was handled in five multi-round financing scenarios and its impact on founder ownership.

24. Study the role of competitive landscape analysis in valuations of ten startups across different industries.


### Solutions for Chapter 9

#### ⭐ Basic Understanding

1. If the valuation is linearly proportional to the TAM, then the valuation based on the true TAM would be $10M × (500M
/ 1B) = $5M. The valuation bias is $10M - $5M = $5M.

2. Publicly traded companies are typically much larger, more mature, and less risky than startups. They may have
different growth prospects, risk profiles, and operating margins. Using their P/S multiples to value a startup can lead
to a significant overvaluation.

$$
3. Fully diluted share count = 500,000 + 100,000 = 600,000 shares.
$$

4. A bottom-up approach starts with specific, observable data (number of customers, revenue per customer) and builds up
to the TAM, making it more grounded in reality. A top-down approach starts with a large, often speculative market
estimate and is more prone to overestimation.

5. Underestimating the time and cost of execution can lead to a valuation that does not account for the need for
additional financing, the risk of delays, or the possibility of running out of cash before achieving profitability.

#### ⭐⭐ Intermediate Application

$$
6. Fully diluted share count = 2,000,000 + 400,000 = 2,400,000 shares. Fully diluted value per share = $20,000,000 \div
2,400,000 = $8.33.
$$

7. Over-relying on management projections can lead to an overly optimistic valuation that does not reflect the true
range of possible outcomes or the risks facing the company.

8. Ignoring the competitive landscape can lead to overvaluation because a company in a highly competitive market will
have lower profit margins, slower growth, and higher risk than a company in a market with few competitors.

$$
9. Realistic TAM = 50,000 \times $1,000 = $50,000,000 ($50M).
$$

10. If the estimated TAM is twice the true TAM and valuation is proportional to TAM, the valuation bias is 100% (the
valuation is twice what it should be).

#### ⭐⭐⭐ Advanced Analysis

11. Using comparable companies ensures that the multiples reflect the characteristics of similar businesses (industry,
stage, growth, risk), making the valuation more accurate and defensible.

$$
12. Value per share = $15,000,000 \div 1,500,000 = $10.
$$

$$
13. Fully diluted share count = 1,500,000 + 300,000 = 1,800,000 shares. Fully diluted value per share = $15,000,000 \div
1,800,000 = $8.33.
$$

14. The main problem with a top-down approach is that it often relies on broad, speculative market estimates that may
not reflect the realistic addressable market for the specific product or service.

15. Sensitivity analysis shows how the valuation changes with different assumptions, helping to identify the key drivers
of value and the range of possible outcomes, reducing over-reliance on any single set of projections.

#### 💭 Discussion Questions

16-19. These are open-ended discussion questions designed to stimulate critical thinking. Sample discussion points would
be provided in the instructor’s manual.

#### 🔬 Research Projects

20-24. These research projects require external data gathering and analysis. Grading rubrics would focus on research
methodology, data quality, analytical rigor, and clarity of presentation.


