# Corporate Hedged Total Return Rate-of-Change Analyzer

A quantitative workbook for analyzing the **rate of change of hedged corporate bond total return versus the rate of change of its underlying rating index.**

Unlike traditional relative value models that compare yields, spreads, or even absolute hedged total return, this project studies the **first derivative of institutional carry**.

The objective is to identify when an individual corporate bond begins accelerating or decelerating relative to its rating cohort before the divergence becomes obvious in price.

---

# Motivation

Most credit analysis focuses on questions like:

- Is this bond yielding more than the index?
- Is the spread rich or cheap?
- Is hedged carry attractive?

Those are useful questions.

This project instead asks:

> **Is the change in hedged total return outperforming or underperforming the change in the rating index?**

Institutional portfolios continuously rebalance financing conditions.

Acceleration often contains more information than the absolute level.

---

# Hedged Total Return

For each observation:

```text
TR =
Yield
− Bid/Ask Cost
− Duration Hedge Cost
− Credit Hedge Cost
− Special Repo Cost
```

All components are measured in basis points.

This approximates the economic carry available to an institution after financing and hedging costs rather than simply observing coupon yield.

---

# The Core Idea

Instead of comparing

```text
Corporate Hedged TR
vs
Rating Index Hedged TR
```

the workbook computes

```text
ROC(Corporate Hedged TR)
vs
ROC(Rating Index Hedged TR)
```

where ROC represents the rate of change through time.

Each ROC series is then normalized into an index:

```text
Index = 100 + ROC
```

creating two directly comparable acceleration indices.

The question becomes:

> **Which financing regime is improving faster?**

rather than

> **Which financing regime currently has higher carry?**

---

# Why This Matters

Institutional markets often respond to *changes* in financing conditions before they respond to the absolute level.

A corporate bond may still exhibit lower total return than its benchmark while simultaneously experiencing improving financing dynamics.

Likewise, a bond with attractive current carry may already be deteriorating beneath the surface.

Monitoring acceleration rather than level can reveal:

- Improving funding conditions
- Worsening funding conditions
- Relative financing momentum
- Early balance-sheet regime changes

---

# Methodology

1. Calculate Hedged Total Return.

2. Build a historical time series.

3. Compute the Rate of Change (ROC) for every observation.

4. Normalize each ROC series into an index beginning at 100.

5. Compare

```text
Corporate Hedged TR ROC Index
```

against

```text
Rating Index Hedged TR ROC Index
```

Persistent divergence suggests the corporate financing regime is evolving differently from its credit cohort.

---

# Interpretation

## Corporate ROC > Rating ROC

- Financing conditions improving faster than the rating index.
- Relative institutional carry strengthening.
- Potential balance-sheet improvement.

## Corporate ROC < Rating ROC

- Financing conditions deteriorating relative to the rating index.
- Institutional carry weakening.
- Potential funding stress.

---

# What This Is

This project measures the **momentum of institutional financing economics** rather than the financing level itself.

It is designed to analyze:

- Relative financing momentum
- Institutional carry acceleration
- Funding regime transitions
- Corporate balance-sheet dynamics

---

# What This Is Not

This is **not** a model of:

- Yield
- Credit spreads
- Price momentum
- Absolute Total Return

Instead, it studies the **first derivative of hedged total return**, treating changes in financing conditions as the primary informational signal.

---

# Applications

- Relative Value Credit Analysis
- Earnings Research
- Funding Regime Monitoring
- Corporate Balance Sheet Analysis
- Institutional Carry Surveillance
- Credit Market Diagnostics
- Quantitative Fixed Income Research

---

# Future Development

Potential additions include:

- Multi-rating acceleration models (AAA through High Yield)
- Rolling z-score divergence analysis
- Statistical significance testing
- Forward ROC forecasting
- Cross-sectional acceleration ranking
- Integration with equity volatility models
- Repo regime classification
- Machine learning classification of financing regimes

---

# Author

**Robert Daniel**

Independent Quantitative Research in:

- U.S. Rates
- Repo Markets
- Fixed Income Derivatives
- Market Microstructure
- Relative Value Trading
- Institutional Funding Dynamics

## Links

GitHub: https://github.com/RobertNikolasDaniel

Substack: https://robertdaniel.substack.com

YouTube: https://www.youtube.com/@BondsAreHard
