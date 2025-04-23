# Optimism Retro Funding Algorithm

The Goldilocks algorithm is a key component of Optimism’s Retro-Funding Evaluation, designed to reward onchain builders (projects) that demonstrate steady and balanced contributions across multiple metrics, with a strong focus on retention. However, as Optimism Season 7 shifts its priority to driving Total Value Locked (TVL), the current weight configuration reveals a significant limitation: it favors established projects while overlooking "rising stars"—emerging projects with shorter track records but substantial growth potential and impact. This exclusion risks undervaluing innovative contributors critical to achieving Season 7’s TVL objectives. This report examines these shortcomings, proposes refined metric and variant weights, and demonstrates how these adjustments better align with Optimism’s goal of rewarding impact while preserving the algorithm’s foundational strengths.

### Shortcomings of the Current Weight Configuration
1. Equal Metric Weights Undermine TVL Focus and Exclude Rising Stars:
All metrics are weighted equally at 0.25, despite total value locked (TVL) being Season 7’s primary target. Metrics like trace_count and monthly_active_farcaster_users, while informative, do not directly contribute to TVL and dilute the focus on value-centric projects. Furthermore, this equal weighting overlooks the unique strengths of rising stars, which often demonstrate strong growth metrics rather than established performance.

2. Vulnerability to Artificial Activity:
The lack of bot-filtered metrics (e.g., transaction_count_bot_filtered) allows unverified or artificial activity to influence scores.
Projects with inflated metrics due to bot activity could receive undeserved rewards, compromising fairness and the recognition of genuine value creation.

3. Platform Bias Towards Farcaster:
Relying exclusively on monthly_active_farcaster_users restricts community assessment to a single platform.
Projects with robust engagement on alternative platforms (e.g., X, Discord) are undervalued, reducing inclusivity and potentially excluding rising stars that thrive on diverse channels.

### Proposed Adjustments to the Goldilocks Algorithm
The proposed changes recalibrate the algorithm by structuring the metric weights into three key categories—TVL Drivers, Transactions, and User Metrics—following a 50-30-20 weighting approach. This framework reflects Retro-Funding’s methodology of evaluating onchain impact through financial commitment (TVL), transaction activity, and user adoption, while emphasizing growth to spotlight rising stars.

Using the 50-30-20 Metric Weight Methodology

TVL Drivers (50%):
- monthly_average_tvl: 0.30
- amortized_gas_fee: 0.20
  
Transaction Drivers (30%):
- trace_count: 0.20
- transaction_count_bot_filtered: 0.10
  
User Metrics (20%):
- monthly_active_farcaster_users: 0.10
- monthly_active_addresses: 0.10
This 50-30-20 split prioritizes financial commitment (TVL) as the primary driver, supported by transaction activity and user adoption metrics. The increased growth weight of 0.30 in the variant weights ensures that rising stars—projects demonstrating strong upward momentum—are adequately recognized.


### Conclusion
The proposed adjustments to the Goldilocks algorithm offer a strategic overhaul that directly addresses its existing limitations while aligning with the core objectives of Optimism Season 7. These refinements ensure the algorithm not only drives Total Value Locked (TVL) but also fosters a fair, inclusive, and resilient Superchain ecosystem.


