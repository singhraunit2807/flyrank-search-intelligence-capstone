# FlyRank Search Intelligence Capstone

## Search Decline Signals and a Transparent Content Review Queue

This repository contains the Week 8 Machine Learning Capstone for the FlyRank internship.

### Research question

**Which observable search-performance signals are associated with future content decline, and can those signals support a transparent ranking system for deciding what to review first?**

### What is included

- `work/notebooks/capstone_analysis.ipynb` — complete, reproducible analysis
- `work/outputs/` — generated ranked recommendations
- `paper/index.html` — deployed research paper
- `paper/results.json` — machine-readable run summary
- `submission/paper_url.txt` — public paper URL

### Method

The capstone compares:

1. A transparent hand-written baseline.
2. A Random Forest model.
3. Both evaluated on the same client-grouped holdout.

The preferred run uses the gated FlyRank warehouse through DuckDB. If a Hugging Face read token is not available in CI, the notebook safely falls back to the public starter slice and records that mode explicitly.

### Leakage control

The target is never used as a feature. The validation split is grouped by client, so clients do not appear in both training and holdout sets.

### Honest framing

The output is a review-prioritization system, not a claim about Google's ranking algorithm and not a causal estimate of the effect of refreshing content.

## Paper

The intended GitHub Pages URL is:

https://singhraunit2807.github.io/flyrank-search-intelligence-capstone/
