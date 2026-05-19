# Chapter 11: Industry-Specific Valuation Frameworks

## Industry-Specific Valuation Frameworks

### Opening Vignette: Snowflake’s $33 Billion IPO

When Snowflake went public in September 2020, the cloud data warehouse company commanded a market capitalization of $33
billion on its first day of trading, despite being unprofitable and generating only $592 million in annual revenue. This
translated to a staggering 56x revenue multiple—nearly double the median for comparable SaaS companies. How did
investors justify such a valuation?

The answer lies in industry-specific metrics that traditional valuation models ignore. Snowflake’s 121% year-over-year
revenue growth, 158% net revenue retention rate, and consumption-based pricing model created a unique value proposition
that required specialized valuation frameworks. Generic valuation approaches would have missed the key drivers of value
in this cloud-native, usage-based business model.

This chapter explores how different industries require tailored valuation approaches that account for sector-specific
economics, metrics, risks, and growth drivers.

### Learning Objectives

By the end of this chapter, readers will be able to:

Apply SaaS-specific metrics including ARR, CAC, LTV, NRR, and Magic Number to value subscription businesses

Calculate risk-adjusted NPV (rNPV) for biotech companies incorporating clinical trial probabilities and regulatory
milestones

Evaluate fintech companies using regulatory capital requirements, network effects, and unit economics

Analyze marketplace platforms using GMV, take rates, liquidity metrics, and network density

Assess hardware and deep tech companies using Technology Readiness Levels (TRL), unit economics, and manufacturing
scalability

Value consumer and e-commerce businesses using cohort analysis, customer lifetime value, and brand equity

Compare valuation multiples and methodologies across different industries to select appropriate approaches



### 11.1 SaaS and Subscription Businesses

Software-as-a-Service companies represent one of the most mature categories of pre-revenue and early-stage valuation,
with well-established metrics and frameworks. The recurring revenue model, high gross margins, and predictable cash
flows (once profitable) make SaaS businesses particularly attractive to investors, but also require specialized
valuation approaches.

#### Key SaaS Metrics

Annual Recurring Revenue (ARR) and Monthly Recurring Revenue (MRR)

ARR represents the annualized value of all active subscriptions, providing a normalized measure of revenue run rate. For
pre-revenue or early-revenue SaaS companies, ARR growth rate is often the single most important valuation driver.

$$ARR=\sum_{i=1}^{n} Annual Subscription Value_{i}$$

$$MRR=\frac{ARR}{12}$$

Customer Acquisition Cost (CAC)

CAC measures the total sales and marketing expense required to acquire one new customer. For early-stage SaaS companies,
high CAC is acceptable if offset by high lifetime value, but the CAC payback period must be reasonable.

$$CAC=\frac{Sales &Marketing Expenses}{Number of New Customers Acquired}$$

Lifetime Value (LTV)

LTV estimates the total gross profit a company will earn from a customer over the entire relationship. The LTV:CAC ratio
is a critical metric for SaaS viability.

$$LTV=\frac{ARPU×Gross Margin}{Churn Rate}$$

where ARPU is Average Revenue Per User.

Rule of Thumb: LTV:CAC ratio should be at least 3:1, and ideally 5:1 or higher for venture-scale businesses.

Net Revenue Retention (NRR)

NRR measures the percentage of revenue retained from existing customers, including expansions, upsells, and cross-sells,
minus downgrades and churn. NRR >100% indicates that existing customers are expanding their usage, a powerful indicator
of product-market fit.

$$NRR=\frac{Revenue from Cohort_{t=1}-Churn+Expansion}{Revenue from Cohort_{t=0}}$$

Best-in-class SaaS companies achieve NRR of 120-150%, meaning existing customers grow revenue 20-50% annually even with
zero new customer acquisition.

CAC Payback Period

The number of months required to recover the cost of acquiring a customer through gross profit.

$$CAC Payback=\frac{CAC}{MRR per Customer×Gross Margin}$$

Target: <12 months for efficient SaaS businesses, <18 months acceptable for high-growth companies.

Magic Number

A metric measuring sales efficiency: how much ARR is generated for each dollar of sales and marketing spend.

$$Magic Number=\frac{Net New ARR_{quarter}}{Sales &Marketing Expense_{prior quarter}}$$

Interpretation: - Magic Number >1.0: Highly efficient, ready to scale - Magic Number 0.75-1.0: Good efficiency, can
scale with capital - Magic Number <0.75: Inefficient, need to improve before scaling

#### SaaS Valuation Framework

Revenue Multiple Approach

For SaaS companies with established revenue, the primary valuation method is EV/Revenue multiples, adjusted for growth
rate and profitability.

$$Valuation=ARR×Multiple$$

where the multiple depends on:

Rule of 40

A heuristic stating that a SaaS company’s growth rate plus profit margin should exceed 40%.

$$Growth Rate+Profit Margin≥40%$$

Companies exceeding the Rule of 40 command premium valuations. For example: - Company A: 80% growth, -45% margin = 35%
(below Rule of 40) → lower multiple - Company B: 50% growth, -5% margin = 45% (above Rule of 40) → higher multiple


Figure 11.1: SaaS Metrics Dashboard


Unit Economics-Based Valuation

For pre-revenue or early-revenue SaaS companies, valuation can be built from unit economics:

$$Valuation=Customer Count×LTV×Discount Factor$$

The discount factor accounts for execution risk, competitive dynamics, and time to scale.


📊 Real World Example: Zoom’s Pre-Pandemic Valuation (2019)

Background: Zoom Video Communications went public in April 2019 at a $9.2 billion valuation (first-day close). The
company was profitable, growing rapidly, and had best-in-class SaaS metrics.

Key Metrics (FY2019): - Revenue: $330M (growing 118% YoY) - ARR: ~$400M - Net Revenue Retention: 140% - Gross Margin:
80% - Operating Margin: 1% (profitable!) - CAC Payback: <5 months - Magic Number: >1.5

Valuation Analysis:

Using revenue multiples: - IPO valuation: $9.2B - ARR: $400M - Implied multiple: 23x ARR

$$
Justification: - Triple-digit growth (118% YoY) - Exceptional NRR (140%) - Profitable (rare for high-growth SaaS) -
Best-in-class unit economics - Rule of 40: 118% + 1% = 119% (far exceeds threshold)
$$

Comparable Company Analysis (2019):

Zoom’s 23x multiple was justified by superior growth and profitability combination.

Outcome: - Peak (Oct 2020): $160B market cap (pandemic surge) - 2024: $20-25B market cap (normalized post-pandemic) -
IPO investors: 2-3x return despite correction

| Growth Rate | Profitability | Typical Multiple Range |
| :---: | :--- | :---: |
| >100% YoY | Negative | 20-40x ARR |
| 50-100% YoY | Negative | 10-20x ARR |
| 30-50% YoY | Breakeven | 8-15x ARR |
| <30% YoY | Profitable | 5-10x ARR |

Lesson: SaaS companies with exceptional unit economics (NRR >130%, profitable growth, CAC payback <6 months) command
premium multiples. Zoom’s valuation wasn’t based on speculation but on demonstrated, sustainable metrics.

Source: Zoom S-1 filing, SaaS Capital Index, public filings



### 11.2 Biotech and Pharmaceuticals

Biotechnology companies present unique valuation challenges due to binary outcomes (drug approval or failure), long
development timelines (10-15 years), high capital requirements ($1-2 billion to bring a drug to market), and regulatory
uncertainty. Traditional DCF analysis is inadequate because it cannot properly model the probability-weighted outcomes
of clinical trials.

#### Risk-Adjusted Net Present Value (rNPV)

The standard approach for biotech valuation is rNPV, which applies probability weights to each development stage and
discounts expected cash flows.

$$rNPV=\sum_{t=1}^{T} \frac{P_{success}×CF_{t}}{(1+r)^{t}}-Development Costs$$

where: - = Probability of reaching market - = Cash flow in year if successful - = Risk-adjusted discount rate (typically
10-15%)

$$P_{success}$$

$$CF_{t}$$

$$t$$

$$r$$

Clinical Trial Success Probabilities (Industry Averages):

Overall probability of preclinical drug reaching market: ~7%

These probabilities vary significantly by therapeutic area: - Oncology: 5-6% overall success rate - Vaccines: 15-20%
overall success rate - Rare diseases: 10-12% overall success rate

#### Decision Tree Valuation

For biotech companies with multiple programs or indications, a decision tree approach models different paths and
outcomes.

Example Structure:

```python
Phase II Trial
├─ Success (35%) → Phase III
│   ├─ Success (60%) → FDA Review
│   │   ├─ Approval (90%) → Market ($500M NPV)
│   │   └─ Rejection (10%) → $0
│   └─ Failure (40%) → $0
└─ Failure (65%) → $0
```

Expected Value:

$$EV=0.35×0.60×0.90×$500M=$94.5M$$

Subtract development costs (~$200M for Phase II + Phase III) to get net value.

#### Peak Sales and Market Potential

For approved drugs or late-stage candidates, valuation focuses on peak sales potential and market share.

Peak Sales Estimation:

$$Peak Sales=Patient Population×Penetration Rate×Price×Compliance$$

Example: - Rare disease affecting 50,000 patients in U.S. - Penetration rate: 40% (20,000 treated patients) - Annual
price: $150,000 per patient - Compliance: 90% - Peak Sales: 20,000 × $150,000 × 0.90 = $2.7B annually

Valuation: Apply 3-5x peak sales multiple (depending on patent life, competition, manufacturing costs): - Conservative:
$2.7B × 3 = $8.1B - Optimistic: $2.7B × 5 = $13.5B

Discount for probability of approval and time to peak sales.


📊 Real World Example: Moderna’s Pre-COVID Valuation (2018)

Background: Moderna went public in December 2018 at a $7.5 billion valuation, making it the largest biotech IPO ever at
the time. The company had zero approved products, zero revenue, and had never successfully brought a drug to market. How
was this valuation justified?

The Valuation Challenge: - No revenue (pure R&D stage) - No approved products - Novel mRNA technology (unproven in
humans) - 21 programs in development (diversified pipeline) - Cumulative losses: $1.5 billion

rNPV Approach:

Moderna’s valuation was based on the probability-weighted value of its pipeline:

Total Pipeline Value (2018 estimate): ~$1.5-2B

Platform Value: The $7.5B valuation implied significant “platform value” beyond the pipeline: - mRNA technology platform
could address hundreds of diseases - Manufacturing capabilities and know-how - IP portfolio (>400 patents) - Partnership
potential (Merck, AstraZeneca deals)

Implied Platform Premium: $7.5B - $2B = $5.5B

Outcome: - 2020: COVID-19 vaccine (mRNA-1273) became one of the most successful drug launches in history - Peak market
cap (2021): $200B (27x IPO valuation) - 2024: Market cap $30-40B (still 4-5x IPO valuation) - Actual peak sales (COVID
vaccine): $18B in 2022

Lesson: For platform biotechnology companies, traditional rNPV of current pipeline significantly undervalues the
optionality and future applications of the technology. Moderna’s $7.5B valuation seemed high based on pipeline alone,
but the platform value proved real when COVID-19 emerged. However, the $200B peak was clearly excessive, driven by
pandemic-specific demand.

Source: Moderna S-1 filing, company presentations, analyst reports



### 11.3 Fintech and Digital Payments

Fintech companies combine technology business models (high growth, scalability) with financial services economics
(regulatory capital, credit risk, compliance costs). This hybrid nature requires specialized valuation approaches that
account for both dimensions.

#### Key Fintech Metrics

Transaction Volume and Take Rate

For payment processors and transaction-based fintechs:

$$Revenue=Transaction Volume×Take Rate$$

Example: - Square (2015): $6.5B transaction volume, 2.75% take rate = $179M revenue - Stripe (2020): $200B+ transaction
volume, ~2.5% take rate = $5B+ revenue

Unit Economics

$$Gross Profit per Transaction=Take Rate-Processing Costs-Fraud Losses$$

Regulatory Capital Requirements

For lending fintechs, regulatory capital requirements constrain growth and returns:

$$Max Loan Portfolio=\frac{Equity Capital}{Risk-Weighted Capital Ratio}$$

Example: - Fintech lender with $100M equity capital - 8% capital requirement (Basel III) - Maximum loan portfolio: $100M
/ 0.08 = $1.25B

This capital constraint affects valuation because growth requires continuous equity raises or debt financing.

Network Effects

Many fintechs benefit from network effects where value increases with user base:

$$Value per User∝Total Users^{α}$$

where  indicates positive network effects.

$$α>1$$

Metcalfe’s Law suggests  (value proportional to users squared), though empirical evidence suggests  is more realistic.

$$α=2$$

$$α=1.2-1.5$$

#### Fintech Valuation Framework

For Payment Processors:

$$Valuation=Transaction Volume×Take Rate×Multiple$$

Multiples typically range from 5-15x revenue depending on: - Growth rate (faster growth = higher multiple) - Take rate
sustainability (competitive moat) - International expansion potential - Regulatory risk

For Lending Fintechs:

$$Valuation=Loan Book×ROE×P/E Multiple-NPL Reserves$$

where: - ROE = Return on Equity (10-20% for successful lenders) - P/E Multiple = 10-20x for high-growth fintechs - NPL =
Non-Performing Loans

For Neobanks:

| Company | EV/Revenue | Growth | NRR | Rule of 40 |
| :--- | :---: | :---: | :---: | :---: |
| Zoom | 23x | 118% | 140% | 119% |
| Slack | 18x | 82% | 143% | 52% |
| Dropbox | 6x | 18% | 115% | 41% |
| Okta | 16x | 49% | 118% | 38% |

$$Valuation=Customer Count×LTV per Customer×Discount Factor$$

Similar to SaaS valuation but with lower LTV due to commoditized banking services.


📊 Real World Example: Stripe’s $95 Billion Valuation (2021)

Background: Stripe, the online payment processor, reached a $95 billion valuation in March 2021, making it one of the
most valuable private companies in the world. With estimated revenue of $7.4 billion, this implied a 13x revenue
multiple.

Key Metrics (2021 estimates): - Transaction volume: $640 billion - Revenue: $7.4 billion - Implied take rate: 1.16% -
Growth rate: 70% YoY - Customers: Millions of businesses - Geographic presence: 45+ countries

Valuation Analysis:

Comparable Company Multiples (2021):

Justification for $95B Valuation:

Exceptional Growth: 70% YoY revenue growth at $7B+ scale is rare

Global Platform: Operating in 45+ countries with room for expansion

Developer-First: Strong technical moat and ecosystem

Product Expansion: Beyond payments (Stripe Capital, Stripe Treasury, Stripe Tax)

Enterprise Adoption: Moving upmarket to large enterprises

Network Effects: More merchants → better fraud detection → more merchants

Revenue Multiple Regression:

Using regression on growth rate:

$$Multiple=3+0.15×Growth Rate$$

$$Multiple=3+0.15×70=13.5x$$

Actual 13x multiple was consistent with regression model.

Outcome: - 2023: Down round at $50B valuation (47% decline) - Reason: Market correction, slower growth (40% vs. 70%),
rising interest rates - 2024: Valuation recovering as IPO approaches

Lesson: Fintech valuations are highly sensitive to growth rates and interest rate environment. Stripe’s $95B valuation
was defensible at 70% growth, but when growth slowed to 40% and rates rose, the valuation compressed significantly. The
13x multiple was appropriate for the growth rate, but the growth rate itself proved unsustainable.

Source: Bloomberg, The Information, analyst estimates


### 11.4 Marketplaces and Platforms

Marketplace businesses (connecting buyers and sellers) have unique economics driven by network effects, liquidity, and
take rates. Valuation must account for the two-sided nature of the business and the critical importance of achieving
liquidity.

#### Key Marketplace Metrics

Gross Merchandise Value (GMV)

Total value of all transactions on the platform, regardless of take rate.

$$GMV=\sum_{i=1}^{n} Transaction Value_{i}$$

Take Rate

Percentage of GMV captured as revenue.

$$Take Rate=\frac{Revenue}{GMV}$$

Typical take rates by marketplace type: - Ride-sharing (Uber, Lyft): 20-30% - Food delivery (DoorDash, Uber Eats):
15-30% - E-commerce (eBay, Etsy): 5-15% - Freelance (Upwork, Fiverr): 15-20% - Real estate (Airbnb): 10-15%

Liquidity

The probability that a buyer finds what they want and a seller finds a buyer.

$$Liquidity=\frac{Successful Transactions}{Total Attempts}$$

High liquidity (>80%) indicates a healthy marketplace. Low liquidity (<50%) suggests the marketplace hasn’t reached
critical mass.

Network Density

$$Network Density=\frac{Actual Connections}{Possible Connections}$$

Higher density indicates stronger network effects.

Cohort Retention

For marketplaces, both buyer and seller retention matter:

$$Buyer Retention_{t}=\frac{Active Buyers in Month t}{New Buyers in Month 0}$$

Best-in-class marketplaces achieve 60-80% buyer retention after 12 months.

#### Marketplace Valuation Framework

GMV Multiple Approach

$$Valuation=GMV×Multiple$$

Typical GMV multiples: - Early-stage (pre-liquidity): 0.1-0.3x GMV - Growth stage (achieving liquidity): 0.5-1.5x GMV -
Mature (strong network effects): 2-5x GMV

Revenue Multiple Approach

$$Valuation=Revenue×Multiple$$

More common for mature marketplaces with established take rates.

Multiples typically range 5-15x revenue depending on: - Growth rate - Unit economics - Competitive moat - International
expansion potential

Network Value Approach

For marketplaces with strong network effects:

$$Valuation=k×Active Users^{α}$$

where  (empirically observed network effect exponent).

$$α=1.2-1.5$$


📊 Real World Example: DoorDash’s IPO Valuation (2020)

Background: DoorDash went public in December 2020 at a $60 billion valuation, capitalizing on pandemic-driven demand for
food delivery. The company was unprofitable and faced intense competition from Uber Eats and Grubhub.

Key Metrics (2020): - GMV: $24.7 billion - Revenue: $2.9 billion - Take rate: 11.7% - Orders: 816 million - Active
consumers: 20 million - Merchant partners: 390,000 - Gross margin: 29% - Operating margin: -23% (unprofitable)

Valuation Analysis:

GMV Multiple: - Valuation: $60B - GMV: $24.7B - Implied multiple: 2.4x GMV

Revenue Multiple: - Valuation: $60B - Revenue: $2.9B - Implied multiple: 21x revenue

Comparable Company Analysis (Dec 2020):

Justification for Premium Valuation:

| Stage | Probability of Advancing | Cumulative Probability |
| :--- | :---: | :---: |
| Preclinical | 65% | 65% |
| Phase I | 60% | 39% |
| Phase II | 35% | 14% |
| Phase III | 60% | 8% |
| FDA Approval | 90% | 7% |

Market Leadership: 50% U.S. market share (vs. Uber Eats 25%, Grubhub 15%)

Network Effects: Largest driver network → fastest delivery → more consumers

Growth: 226% revenue growth YoY (pandemic surge)

Unit Economics Improving: Contribution margin improving from 3% to 10%

Expansion Potential: DashMart (grocery), DoorDash Drive (white-label logistics)

Outcome: - First day close: $72B market cap (20% pop) - Peak (Nov 2021): $72B - 2024: $45-55B market cap - Company
achieved profitability in 2023

Lesson: Marketplace valuations depend critically on market share and network effects. DoorDash’s 2.4x GMV multiple (2-3x
higher than competitors) was justified by its dominant market position, which creates self-reinforcing network effects.
However, the premium valuation required the company to prove it could achieve profitability, which it eventually did.

Source: DoorDash S-1 filing, public filings, industry reports



### 11.5 Hardware and Deep Tech

Hardware and deep technology companies (semiconductors, robotics, advanced materials, quantum computing, fusion energy)
face unique valuation challenges due to capital intensity, long development cycles, manufacturing complexity, and
technology risk.

#### Technology Readiness Levels (TRL)

The U.S. Department of Defense developed a 9-level framework for assessing technology maturity:

Valuation Framework:

$$Valuation=Market Size×Market Share×Margin×Multiple×(1-TRL Discount)$$

#### Unit Economics for Hardware

Unlike software (near-zero marginal cost), hardware has significant per-unit costs:

$$Gross Margin=\frac{ASP-COGS}{ASP}$$

where: - ASP = Average Selling Price - COGS = Cost of Goods Sold (materials, labor, manufacturing overhead)

Target gross margins: - Consumer hardware: 30-50% - Enterprise hardware: 50-70% - Semiconductors: 60-80%

Manufacturing Scalability

A critical question for hardware startups: Can you manufacture at scale profitably?

$$Break-Even Volume=\frac{Fixed Costs}{ASP-Variable Cost per Unit}$$

Many hardware startups fail because they can’t reach break-even volume before running out of capital.


📊 Real World Example: Rivian’s Pre-Production Valuation (2019-2021)

Background: Rivian, the electric vehicle startup, raised $2.5 billion in July 2019 at a $5.5 billion valuation despite
having delivered zero vehicles. By November 2021, the company IPO’d at a $66.5 billion valuation with only 156 vehicles
delivered.

The Valuation Challenge: - Zero revenue (pre-production) - Capital intensive ($8B+ required to reach scale) - Unproven
manufacturing capabilities - Intense competition (Tesla, traditional OEMs, other EV startups) - Technology risk
(battery, software, autonomous driving)

Valuation Approach (2019 - $5.5B):

Comparable Company Analysis:

DCF with Probability Weighting:

Scenarios for 2025 (5 years out):

$$
Expected Value: 0.30($60B) + 0.40($10B) + 0.30($0) = $22B
$$

Discounted to 2019: $22B / (1.30)^5 = $5.9B

The $5.5B valuation was slightly below the probability-weighted DCF, reflecting execution risk.

2021 IPO Valuation ($66.5B):

By IPO, Rivian had: - Delivered 156 vehicles (proof of manufacturing capability) - Secured Amazon order for 100,000
delivery vans - Built manufacturing facility in Illinois - Raised $10.5B total capital

Valuation jumped 12x due to: 1. De-risked manufacturing: Vehicles actually rolling off line 2. Amazon partnership:
Guaranteed demand for 100,000 units 3. EV market euphoria: All EV stocks trading at peak multiples 4. Competitive
positioning: Differentiated (trucks/SUVs vs. Tesla sedans)

Outcome: - Peak market cap (Nov 2021): $150B (briefly exceeded Ford and GM) - 2022-2024: Declined to $10-20B (85-90%
drop) - Reasons: Production delays, cash burn, competition, market correction

Lesson: Hardware company valuations are extremely sensitive to manufacturing risk. Rivian’s $5.5B pre-production
valuation was defensible based on probability-weighted scenarios, but the $66.5B IPO valuation (and $150B peak)
reflected euphoria rather than fundamentals. The subsequent 85-90% decline brought valuation back to reality as
production challenges emerged.

Source: Rivian S-1 filing, public filings, industry analysis



### 11.6 Consumer and E-Commerce

Consumer and e-commerce companies are valued based on customer acquisition costs, lifetime value, brand equity, and
repeat purchase rates. Unlike B2B businesses, consumer companies face higher churn and more competition but can scale
faster with viral growth.

#### Key Consumer Metrics

Customer Lifetime Value (LTV)

$$LTV=Average Order Value×Purchase Frequency×Customer Lifespan×Gross Margin$$

$$
Example: - AOV: $100 - Frequency: 4 purchases per year - Lifespan: 3 years - Gross Margin: 50% - LTV: $100 \times 4
\times 3 \times 0.50 = $600
$$

Customer Acquisition Cost (CAC)

$$CAC=\frac{Marketing Spend}{New Customers Acquired}$$

LTV:CAC Ratio

Target: 3:1 or higher for sustainable consumer businesses.

Cohort Analysis

Track revenue and retention by customer cohort (month/quarter of acquisition):

$$Cohort Revenue_{t}=Customers_{t=0}×Retention_{t}×Revenue per Active Customer_{t}$$

Best-in-class consumer companies show increasing revenue per cohort over time (indicating repeat purchases and
expansion).

Brand Value

For consumer companies, brand equity is a significant intangible asset. Proxy metrics: - Organic vs. paid customer
acquisition ratio - Net Promoter Score (NPS) - Social media engagement - Brand awareness surveys

#### Consumer Valuation Framework

For E-Commerce:

$$Valuation=Revenue×Multiple$$

Typical multiples: - Commodity e-commerce: 0.5-1.5x revenue - Branded e-commerce: 2-5x revenue - Subscription
e-commerce: 3-8x revenue

For Consumer Apps:

$$Valuation=Active Users×LTV per User×Discount Factor$$

Discount factors: - Proven monetization: 0.5-0.8 - Emerging monetization: 0.2-0.4 - No monetization: 0.05-0.15


### Key Takeaways


| Program | Indication | Stage | Peak Sales | P(Success) | NPV | Risk-Adjusted Value |
| :---: | :--- | :--- | :---: | :---: | :---: | :---: |
| mRNA-1273 | COVID vaccine | Preclinical | N/A | N/A | N/A | $0 (not yet started) |
| mRNA-1647 | CMV vaccine | Phase II | $2B | 14% | $4B | $560M |
| mRNA-1345 | RSV vaccine | Phase I | $1.5B | 8% | $3B | $240M |
| mRNA-3927 | Rare disease | Phase I | $500M | 8% | $1B | $80M |
| + 17 more programs | Various | Preclinical-Phase I | Various | 5-10% | Various | $500M |

Industry-specific metrics are essential: Generic valuation approaches miss the key drivers of value in specialized
sectors (ARR for SaaS, rNPV for biotech, GMV for marketplaces)

SaaS companies are valued on ARR multiples adjusted for growth rate and unit economics, with NRR >120% and Magic Number
>0.75 indicating strong businesses worthy of premium valuations

Biotech valuations require probability-weighted analysis using rNPV methodology, with overall success rates of only 7%
from preclinical to approval requiring significant risk discounts

Fintech valuations combine technology multiples with financial services constraints, particularly regulatory capital
requirements that limit growth and returns

Marketplace valuations depend critically on network effects and liquidity, with market leaders commanding 2-3x higher
multiples than competitors due to self-reinforcing advantages

Hardware and deep tech require TRL-based discounting to account for technology risk, with 70-95% discounts for
early-stage technology (TRL 1-5)

Consumer businesses are valued on LTV:CAC ratios and cohort economics, with sustainable businesses requiring 3:1 LTV:CAC
and improving cohort performance over time


### Exercises for Chapter 11

#### ⭐ Basic Understanding

1. A SaaS company has $10M ARR growing at 80% YoY, with a Net Revenue Retention of 125%. Using the Rule of 40 and
assuming -30% operating margin, calculate whether this company meets the threshold and estimate an appropriate revenue
multiple.

2. A biotech company has a drug candidate in Phase II clinical trials for a rare disease. Using industry-average success
probabilities (35% Phase II, 60% Phase III, 90% FDA approval), calculate the overall probability of reaching market.

3. A payment processing fintech has $50B in annual transaction volume and charges a 2.5% take rate. Calculate annual
revenue and estimate valuation using a 10x revenue multiple.

4. A marketplace has $500M in GMV and a 15% take rate. Calculate revenue and estimate valuation using both 2x GMV and
12x revenue multiples. Which gives a higher valuation?

5. A hardware startup is at TRL 5 (laboratory prototype validated). If the target market is $10B and the company could
capture 5% share at 40% margin with a 15x multiple, calculate the risk-adjusted valuation using an 80% TRL discount.

#### ⭐⭐ Intermediate Application

6. Compare two SaaS companies:
   Company A: $20M ARR, 100% growth, 130% NRR, -40% margin, Magic Number 0.9
   Company B: $20M ARR, 50% growth, 115% NRR, -10% margin, Magic Number 0.6
   Which deserves a higher valuation multiple and why? Estimate appropriate multiples for each.

7. A biotech company has three drug candidates:
   Drug A: Phase III, $2B peak sales, 60% probability of approval
   Drug B: Phase II, $1B peak sales, 14% probability of reaching market
   Drug C: Phase I, $500M peak sales, 8% probability of reaching market
Using a 5x peak sales multiple and 12% discount rate, calculate the risk-adjusted NPV of the pipeline assuming drugs
reach peak sales in years 2, 4, and 6 respectively.

8. A fintech lender has $100M in equity capital and is subject to an 8% risk-weighted capital requirement. If the
company can generate 15% ROE on its loan book and trades at a 12x P/E multiple, calculate the maximum valuation.

9. A marketplace has the following metrics:
   GMV: $1B
   Take rate: 12%
   Growth rate: 150% YoY
   Gross margin: 35%
   Operating margin: -25%
Calculate valuation using (a) 3x GMV, (b) 15x revenue, and (c) a regression model where Multiple = 5 + 0.05 × Growth
Rate. Which method gives the highest valuation?

10. A consumer e-commerce company has:
    500,000 customers
    Average order value: $80
    Purchase frequency: 3x per year
    Customer lifespan: 2.5 years
    Gross margin: 45%
    CAC: $50
    Calculate LTV, LTV:CAC ratio, and estimate valuation using 4x revenue multiple.

#### ⭐⭐⭐ Advanced Analysis

11. Perform a complete SaaS valuation for a company with the following metrics:
    Current ARR: $15M
    Growth rate: 120% YoY (declining 20% per year)
    NRR: 135%
    Gross margin: 75%
    Operating margin: -45% (improving 10% per year)
    CAC payback: 14 months
    Magic Number: 1.2
Project 5-year financials, calculate terminal value using 25x ARR multiple, and discount at 15% to get present value.
Compare to a simple revenue multiple approach.

12. A biotech company is developing a gene therapy for a rare genetic disorder. Build a complete rNPV model with the
following assumptions:
    Patient population: 10,000 in U.S., 25,000 globally
    Current stage: Phase I (just completed)
    Phase II cost: $50M, duration 2 years, success probability 40%
    Phase III cost: $150M, duration 3 years, success probability 65%
    FDA review: $20M, duration 1 year, approval probability 85%
    Pricing: $1M per patient (one-time treatment)
    Penetration: 30% of patients
    Patent life: 15 years from approval
    Discount rate: 12%
    Calculate rNPV and determine the minimum success probability required to justify current development costs.

13. A two-sided marketplace is trying to achieve liquidity. Currently:
    Supply side: 10,000 sellers, adding 500/month
    Demand side: 50,000 buyers, adding 2,000/month
    Transaction success rate: 45% (below 80% liquidity threshold)
    GMV: $20M/month
    Take rate: 18%
Model the path to liquidity assuming transaction success rate increases by 2% for every 10% increase in seller base. How
many months until the marketplace reaches 80% liquidity? What will GMV and valuation (at 2.5x GMV) be at that point?

14. A hardware startup has developed a revolutionary battery technology. Perform a TRL-adjusted valuation:
    Current TRL: 6 (prototype in relevant environment)
    Target market: $50B (EV batteries)
    Potential market share: 8%
    Gross margin: 65%
    Development costs to TRL 9: $500M
    Time to market: 4 years
    Probability of technical success: 60%
    Probability of commercial success (given technical success): 70%
    Calculate risk-adjusted valuation using both TRL discount method and probability-weighted DCF. Compare results.

```python
15. Perform a cohort analysis for a subscription e-commerce company:
    Month 0: 10,000 new customers acquired at $40 CAC
    Monthly retention: 85% (consistent across cohorts)
    Average order value: $60
    Purchase frequency: 1.2x per month for active customers
    Gross margin: 50%
    Calculate LTV using cohort analysis over 24 months. Compare to the simplified LTV formula. If the company has 12 cohorts (one per month for a year), calculate total company valuation using 5x revenue multiple.
```

#### 💭 Discussion Questions

16. SaaS companies with >100% NRR can theoretically grow revenue without acquiring any new customers. Why then do they
still invest heavily in customer acquisition? Under what circumstances would it make sense to stop acquiring new
customers and focus entirely on expanding existing accounts?

17. The average biotech drug has only a 7% probability of reaching market from preclinical stage, yet biotech companies
regularly achieve multi-billion dollar valuations. Is this rational, or does it represent a systematic overvaluation of
biotech companies by investors?

18. Marketplace businesses often operate at a loss for years to achieve network effects and liquidity. At what point
should investors lose patience with unprofitable marketplaces? What metrics indicate whether losses are 'good'
(investing in growth) versus 'bad' (fundamental unit economics problems)?

19. Hardware startups require 10-100x more capital than software startups to reach the same revenue scale. Given this
capital intensity, should hardware startups be valued at significant discounts to software companies, or do they deserve
premium valuations due to defensibility and barriers to entry?

#### 🔬 Research Projects

20. Research three recent SaaS IPOs (2022-2024) and analyze their valuation multiples relative to growth rate, NRR, and
profitability. Has the relationship between these metrics and multiples changed compared to the 2020-2021 period? What
explains any changes?

21. Analyze the rNPV methodology by studying five biotech companies that had drug candidates in Phase III trials five
years ago. How many succeeded? How did actual outcomes compare to the 60% Phase III success probability? Were initial
valuations justified by outcomes?

22. Compare the unit economics of three marketplace businesses in different categories (e.g., ride-sharing, food
delivery, freelance services). Which has the best unit economics? What structural factors explain the differences in
take rates and margins?

23. Research the history of three hardware startups that failed despite raising significant capital. What were the
common factors? How could better valuation analysis have identified the risks earlier?

24. Investigate how consumer brand value is quantified and incorporated into valuations. Find examples of consumer
companies that traded at significant premiums or discounts based on brand strength. What metrics or methodologies were
used to justify the brand value?

### Solutions for Chapter 11

#### ⭐ Basic Understanding

1. Rule of 40 = Growth Rate + Operating Margin = 80% + (-30%) = 50%. Meets threshold (>40%). With 80% growth and 125%
NRR (excellent retention), appropriate multiple: 12-15x ARR. At $10M ARR: Valuation = $120M - $150M.

$$
2. Overall probability = 0.35 \times 0.60 \times 0.90 = 18.9%.
$$

$$
3. Annual revenue = $50B \times 2.5% = $1.25B. Valuation = $1.25B \times 10 = $12.5B.
$$

4. Revenue = $500M × 15% = $75M. GMV method: $500M × 2 = $1.0B. Revenue method: $75M × 12 = $900M. GMV multiple gives
higher valuation ($1.0B).

$$
5. Target value = $10B \times 5% \times 40% \times 15 = $3B. Risk-adjusted (TRL 5 = 80% discount): $3B \times (1 - 0.80)
= $600M.
$$

#### ⭐⭐ Intermediate Application

6. Company A: 100% growth, 130% NRR, Magic Number 0.9 → Suggested multiple: 12-14x ARR. Company B: 50% growth, 115% NRR,
Magic Number 0.6 → Suggested multiple: 8-10x ARR. Winner: Company A due to superior growth and retention.

$$
7. Drug A: $2B \times 5 \times 0.60 / (1.12)^2 = $4.78B. Drug B: $1B \times 5 \times 0.14 / (1.12)^4 = $0.44B. Drug C:
$500M \times 5 \times 0.08 / (1.12)^6 = $0.10B. Total pipeline value: $5.32B.
$$

$$
8. Maximum loan book = $100M / 8% = $1.25B. Annual earnings = $100M \times 15% = $15M. Valuation = $15M \times 12 =
$180M.
$$

$$
9. Revenue = $1B \times 12% = $120M. GMV: $1B \times 3 = $3.0B. Revenue: $120M \times 15 = $1.8B. Regression: Multiple =
5 + 0.05 \times 150 = 12.5; Valuation = $120M \times 12.5 = $1.5B. Highest valuation: GMV method at $3.0B.
$$

$$
10. Annual revenue per customer = $80 \times 3 = $240. Lifetime revenue = $240 \times 2.5 = $600. LTV = $600 \times 45%
= $270. LTV:CAC = $270 / $50 = 5.4 (excellent). Total revenue = 500,000 \times $240 = $120M. Valuation = $120M \times 4
= $480M.
$$

#### ⭐⭐⭐ Advanced Analysis

11. Projected ARR growth leads to terminal value of ~$2,100M discounted to ~$1,044M at 15%. Simple multiple approach:
$15M × 12 = $180M. DCF gives significantly higher valuation due to strong growth trajectory.

$$
12. Peak sales = 35,000 patients \times $1M \times 30% = $10.5B. Overall success probability = 0.40 \times 0.65 \times
0.85 = 22.1%. PV of revenues \approx $89.9B, PV of costs \approx $156M. rNPV = ($89.9B - $156M) \times 22.1% = $19.8B.
Minimum success probability to break even: $220M / $89.9B \approx 0.24%.
$$

13. [Solution would include growth projections, liquidity threshold analysis, and valuation impact - detailed
calculation provided in full version]

14. [Solution would include TRL advancement timeline, capital requirements, and risk-adjusted valuation at each stage -
detailed calculation provided in full version]

15. [Solution would include monthly cohort LTV calculations, retention curves, and comparison to simplified formula -
detailed calculation provided in full version]

#### 💭 Discussion Questions

16. Companies acquire new customers to expand TAM, create competitive moats, and diversify revenue. Stop acquiring only
if CAC payback >24 months, negative unit economics, or approaching market saturation.

17. Multi-billion valuations can be rational due to power law returns and platform optionality, but systematic
overvaluation occurs in bull markets.

18. Investors should evaluate unit economics and liquidity trends. Good losses: improving metrics; bad losses: flat or
worsening metrics.

19. Hardware may deserve discounts for capital intensity but premiums for defensibility and barriers to entry.
Case-by-case basis.

#### 🔬 Research Projects

20-24: These research projects require students to conduct independent analysis. Instructors should provide guidance on
data sources, frameworks, and evaluation rubrics.

