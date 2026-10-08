# Data and Code Availability

To support reproducibility and transparency, this study releases the processed analytical resources, temporal features, baseline implementations, and standardized temporal-GNN evaluation pipeline used in the manuscript.

## Released packages

- `CoreData.zip`: processed event-level and media–viewpoint temporal records used to reconstruct first-adoption sequences and derive analytical samples.
- `TimeFeatures.zip`: time-indexed features used by TOAM, including historical propensity, short-term diffusion state, local node position, system-level network state, and cross-platform context.
- `CanonicalGNNAdapter.zip`: common adapters mapping the canonical first-adoption event stream to the input formats required by TGAT, TGN, GraphMixer, and DyGFormer.
- `GNNRunCode.zip`: training and evaluation code for the standardized temporal-GNN baselines, including repeated-seed evaluation and manuscript metrics.

## Repository

https://github.com/annieeeeeeeee/TOAM-temporal-media-networks

## Recommended manuscript statement

**Code and Data Availability.** To support reproducibility, the processed analytical data, temporal features, temporal-GNN adapters, and baseline implementation code used in this study are publicly available at https://github.com/annieeeeeeeee/TOAM-temporal-media-networks. The repository provides four modular packages—`CoreData.zip`, `TimeFeatures.zip`, `CanonicalGNNAdapter.zip`, and `GNNRunCode.zip`—covering canonical data construction, TOAM time-indexed features, standardized temporal-GNN input conversion, and baseline training/evaluation. Data derived from third-party sources remain subject to the applicable source terms and redistribution conditions.
