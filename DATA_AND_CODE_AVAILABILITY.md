# Data and Code Availability

To support reproducibility and transparency, this repository releases the processed analytical resources, temporal features, baseline implementations, and standardized temporal-graph evaluation materials used in the manuscript.

## Released packages

- `CoreData.zip`: processed event-level and media–viewpoint temporal records used to reconstruct first-adoption sequences and derive analytical samples.
- `TimeFeatures.zip`: time-indexed features used by TOAM, including historical propensity, short-term diffusion state, local node position, system-level network state, and cross-platform context.
- `CanonicalGNNAdapter.zip`: common adapters mapping the canonical first-adoption stream to the temporal-graph baseline input formats.
- `GNNRunCode.zip`: training and evaluation code for TGAT, TGN, GraphMixer, and DyGFormer under the common chronological evaluation protocol.
- `TOAM_TGFormer.zip`: TGFormer (2026) adaptation and five-seed evaluation materials for the canonical EA prediction task.

## Evaluation protocol

The main prediction task uses a 3-hour horizon with EA ≥ 2. The chronological split is 2016–2017 for training and 2018–2019 for holdout testing. Predictors and graph neighborhoods use only information available before the focal prediction time. Interactions sharing the same timestamp are predicted from a common pre-update graph state and incorporated only after prediction.

The standardized temporal-graph comparison includes TGAT, TGN, GraphMixer, DyGFormer, and TGFormer (2026), evaluated on the same canonical first-adoption stream and held-out test set. Stochastic temporal-GNN results are reported over five random seeds.

## Repository

https://github.com/annieeeeeeeee/TOAM-temporal-media-networks

## Recommended manuscript statement

**Data and Code Availability.** Processed analytical data and code supporting this study are publicly available at https://github.com/annieeeeeeeee/TOAM-temporal-media-networks. The repository provides reproducibility packages for canonical data construction, TOAM time-indexed features, standardized temporal-GNN input conversion and evaluation, and the TGFormer (2026) comparison. Data derived from third-party sources remain subject to the applicable source terms and redistribution conditions.
