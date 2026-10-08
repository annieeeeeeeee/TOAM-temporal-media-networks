# TOAM: Temporal Opportunity-Aware Amplification in Temporal Media Networks

This repository provides the reproducibility materials for the study:

**Who Matters, and When? Explainable Prediction of Excess Amplification in Temporal Media Networks**

The study introduces the **Temporal Opportunity-Aware Amplification Model (TOAM)** for predicting whether a media–viewpoint entry is followed by **excess amplification (EA)** beyond the diffusion level expected from the pre-entry trajectory.

## Repository contents

| Package | Purpose |
|---|---|
| `CoreData.zip` | Processed event-level and media–viewpoint temporal records used to reconstruct first-adoption sequences and analytical samples. |
| `TimeFeatures.zip` | Time-indexed TOAM features, including historical propensity, short-term diffusion state, local node position, system-level network state, and cross-platform context. |
| `CanonicalGNNAdapter.zip` | Common adapters mapping the canonical first-adoption event stream to TGAT, TGN, GraphMixer, and DyGFormer input formats. |
| `GNNRunCode.zip` | Training and evaluation code for the four standardized temporal-GNN baselines. |

## Reproducibility workflow

1. `CoreData.zip` — inspect the canonical event and first-adoption records.
2. `TimeFeatures.zip` — load or reconstruct the time-indexed features used by TOAM.
3. `CanonicalGNNAdapter.zip` — convert the canonical event stream into model-specific temporal-GNN inputs.
4. `GNNRunCode.zip` — train and evaluate TGAT, TGN, GraphMixer, and DyGFormer under the same chronological protocol.

## Main evaluation design

- Training: 2016–2017
- Holdout testing: 2018–2019
- Main test size: 299,724 media–viewpoint–event–time situations
- Main positive class: 41,371 cases (13.803%)

The main prediction target is Excess Amplification (EA):

`EA(i,v,e,t; h) = observed future diffusion - expected future diffusion`

where expected diffusion is estimated using only information available before the focal entry time.

## Data-use notice

The code and documentation in this repository are released under the MIT License unless otherwise stated. Data files may contain processed records derived from third-party sources and remain subject to the applicable source terms and redistribution conditions. The MIT License does not automatically grant rights to third-party source data.

## Repository

https://github.com/annieeeeeeeee/TOAM-temporal-media-networks
