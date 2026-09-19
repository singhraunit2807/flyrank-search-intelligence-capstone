# Final Capstone Setup

The repository is built and the analysis workflow has been verified successfully on the public starter slice.

For the strongest final submission matching the Week 8 brief, complete these two account-level settings:

## 1. Add the FlyRank Hugging Face read token

The full FlyRank warehouse is gated. Do not commit the token.

GitHub:
Settings → Secrets and variables → Actions → New repository secret

Name:
HF_TOKEN

Value:
Your Hugging Face read token.

After saving it, open:
Actions → Execute and publish capstone → Run workflow

The notebook will then prefer the full warehouse automatically. It uses DuckDB to query the hosted Parquet data without downloading the entire warehouse.

## 2. Enable GitHub Pages

GitHub:
Settings → Pages

Under Build and deployment:
- Source: Deploy from a branch
- Branch: gh-pages
- Folder: / (root)
- Save

The paper is already published to the gh-pages branch by CI.

Expected paper URL:
https://singhraunit2807.github.io/flyrank-search-intelligence-capstone/

## Current verified state

- Capstone notebook executes successfully.
- Leakage check passes.
- Client-grouped holdout passes with zero group overlap.
- Model and baseline use the same holdout.
- Research paper is generated automatically.
- gh-pages branch is populated.
- Current CI run uses the public starter slice because HF_TOKEN is not configured.
