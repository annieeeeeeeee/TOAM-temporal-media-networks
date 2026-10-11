# TOAM: Temporal Opportunity-Aware Amplification in Temporal Media Networks

This repository provides the reproducibility materials for the study:

**Who Matters, and When? Explainable Prediction of Excess Amplification in Temporal Media Networks**

The study develops the **Temporal Opportunity-Aware Amplification Model (TOAM)** for predicting whether a media–viewpoint entry is followed by **excess amplification (EA)** beyond the diffusion level expected from the pre-entry trajectory.

## Repository contents

| Package | Purpose |
|---|---|
| `CoreData.zip` | Processed event-level and media–viewpoint temporal records used to reconstruct first-adoption sequences and analytical samples. |
| `TimeFeatures.zip` | Time-indexed TOAM features, including historical propensity, short-term diffusion state, local node position, system-level network state, and cross-platform context. |
| `CanonicalGNNAdapter.zip` | Common adapters mapping the canonical first-adoption event stream to the temporal-graph baseline input formats. |
| `GNNRunCode.zip` | Training and evaluation code for TGAT, TGN, GraphMixer, and DyGFormer under the common chronological evaluation protocol. |
| `TOAM_TGFormer.zip` | TGFormer (2026) adaptation and five-seed evaluation materials for the canonical EA prediction task. |

## Reproducibility workflow

1. `CoreData.zip` — inspect the canonical event and first-adoption records.
2. `TimeFeatures.zip` — load or reconstruct the time-indexed features used by TOAM.
3. `CanonicalGNNAdapter.zip` — convert the canonical first-adoption stream into temporal-graph model inputs.
4. `GNNRunCode.zip` — train and evaluate TGAT, TGN, GraphMixer, and DyGFormer.
5. `TOAM_TGFormer.zip` — reproduce the TGFormer (2026) comparison and its five-seed evaluation outputs.

## Main evaluation design

- Events: 6,021
- Canonical first-adoption interactions: 994,890
- Model-ready situations: 645,154
- Training period: 2016–2017 (345,430 situations)
- Holdout test period: 2018–2019 (299,724 situations)
- Positive test cases under the main specification: 41,371 (13.803%)
- Main specification: 3-hour horizon, EA ≥ 2

The prediction target is:

`EA(i,v,e,t; h) = observed future diffusion - expected future diffusion`

Expected diffusion is estimated from the trajectory available before the focal entry time. Predictors and graph neighborhoods use only information available before the prediction time. Interactions sharing the same timestamp are predicted from a common pre-update graph state and incorporated only after prediction.

## Temporal-GNN comparison

The standardized temporal-graph comparison includes **TGAT, TGN, GraphMixer, DyGFormer, and TGFormer (2026)**. All models are evaluated on the same canonical EA task, chronological train/test split, and strict historical-information protocol. Stochastic temporal-GNN results are reported over five random seeds.

## Data-use notice

The code and documentation in this repository are released under the MIT License unless otherwise stated. Data files may contain processed records derived from third-party sources and remain subject to the applicable source terms and redistribution conditions. The MIT License does not automatically grant rights to third-party source data.

## Repository

https://github.com/annieeeeeeeee/TOAM-temporal-media-networks
