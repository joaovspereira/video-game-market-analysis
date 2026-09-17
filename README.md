![Video Game Market Analysis](assets/banner.svg)

**English** · [Português](README.pt-BR.md) · [Notebook](notebooks/video_game_market_analysis.ipynb) · [Portfolio](https://github.com/joaovspereira)

# Video Game Market Analysis

## Business question

Use historical game sales and review scores to support a 2017 campaign-planning case for the online store Ice.

## Results and evidence

| Hypothesis comparison | Saved Welch p-value | At α = 0.05 |
|---|---:|---|
| Xbox One vs PC user scores | **0.54895** | Do not reject equal means |
| Action vs Sports user scores | **4.24 × 10⁻²⁰** | Reject equal means |

The 2012–2016 analysis distinguishes North American and European preferences from Japan’s. Historical recommendations prioritize PS4/Xbox One in Western markets and emphasize 3DS in Japan. These are recommendations for the original 2017 scenario.

## Methodology

1. Standardize columns, handle missing records and convert the `tbd` score marker to missing values.
2. Aggregate regional sales into global unit sales.
3. Examine platform life cycles and choose the historical 2012–2016 analysis window.
4. Compare platform, genre, review-score and regional patterns.
5. Use Welch t-tests for user-score comparisons and translate findings into campaign priorities.

## Technologies

Python · pandas · NumPy · SciPy · Matplotlib

## Explore the repository

- [Notebook](notebooks/video_game_market_analysis.ipynb) — analysis, code and saved evidence
- [Data requirements](data/README.md) — expected source files
- [Validation notes](VALIDATION.md) — provenance, corrections and checks
- [Dependencies](requirements.txt)

## Run locally

```bash
git clone https://github.com/joaovspereira/video-game-market-analysis.git
cd video-game-market-analysis
python -m venv .venv
```

Activate the environment with `source .venv/bin/activate` on macOS/Linux or `.\.venv\Scripts\Activate.ps1` in Windows PowerShell. Then run:

```bash
python -m pip install -r requirements.txt
python -m notebook notebooks/video_game_market_analysis.ipynb
```

Add the datasets listed in [data/README.md](data/README.md) before executing the notebook. The analysis is in Portuguese, with this English guide for navigation. Dependencies are an installation list, not a lockfile for the original environment.

## Key learning

Segmenting a market changes the recommendation: a globally popular platform or genre is not necessarily the best regional choice. Non-rejection of a null hypothesis is not proof of equivalence.

## Limitations

Sales are measured in millions of units, not USD; mislabeled chart source was corrected and affected stale chart outputs were cleared. Remaining results are from the saved original execution. The 2016 period may be incomplete. Missing review scores and ESRB ratings can bias comparisons. Correlation does not establish a causal effect on sales, and recommendations are historical rather than current market advice.

## Next improvements

Add effect sizes and uncertainty, sensitivity to the selected time window and explicit treatment of missing ESRB ratings.

## Context

Educational project developed during the TripleTen Data Science Bootcamp and prepared for this public portfolio. No production deployment or realized business impact is claimed.

[João Vitor Pereira](https://github.com/joaovspereira) · [LinkedIn](https://www.linkedin.com/in/joao-vitor-de-souza-pereira) · [Email](mailto:joaovitorsouza20pereira@gmail.com)
