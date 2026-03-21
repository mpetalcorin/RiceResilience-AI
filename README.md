# RiceResilience-AI
AI-enabled multi-stage proof-of-concept for modeling rice seed-stage and reproductive-stage resilience under combined heat, drought, salinity, and oxidative stress.
<img width="1495" height="983" alt="Screenshot 2026-03-21 at 09 14 01" src="https://github.com/user-attachments/assets/bda1bbd6-a83e-4749-b151-65012b86fc95" />
## Overview

This repository contains a computational proof of concept for studying **rice resilience under climate-linked abiotic stress**. The project integrates **seed-stage establishment** and **reproductive-stage performance** into one unified framework and uses simulated, literature-benchmarked datasets to test whether molecular-style and plant-level features can be combined with machine learning to support **climate-smart breeding decisions**.

The workflow was designed around biologically plausible rice stress responses, especially the well-established roles of **ionic imbalance**, **oxidative stress**, **osmotic adjustment**, **antioxidant defense**, **pollen viability**, and **spikelet fertility** under abiotic stress. The project treats resilience as a **developmentally staged systems phenotype**, not a single-trait property.

## Project aims

This repository was built to answer five core questions:

1. Can a synthetic but biologically structured dataset recover plausible rice stress-response patterns across two developmental stages?
2. Do combined stresses produce stronger penalties than single stresses at both seed and reproductive stages?
3. Which plant-level and molecular-style features best predict germination and yield under stress?
4. Can multivariate and machine-learning methods distinguish tolerant and susceptible phenotypes?
5. Can stage-specific outputs be integrated into a breeder-facing ranking framework?

## Biological scope

The model focuses on the following stress types:

- Heat
- Drought
- Salinity
- Oxidative stress
- Stress combinations, including:
  - Heat + Drought
  - Heat + Salinity
  - Drought + Salinity
  - Combined_All

The two developmental stages modeled are:

- **Seed stage**, emphasizing germination, root growth, vigor, ion balance, oxidative injury, osmotic response, and antioxidant activity
- **Reproductive stage**, emphasizing pollen viability, spikelet fertility, grain weight, yield, photosynthesis, oxidative injury, and biochemical stress response

## Simulated trait layers

### Seed-stage variables

- Germination percentage
- Root length
- Vigor index
- Na⁺/K⁺ ratio
- H₂O₂
- MDA
- Proline
- SOD
- CAT
- APX
- Relative expression features for stress-associated genes

### Reproductive-stage variables

- Pollen viability
- Spikelet fertility
- Yield per plant
- Grain weight
- Photosynthesis
- Na⁺/K⁺ ratio
- H₂O₂
- MDA
- Proline
- SOD
- CAT
- APX
- Relative expression features for stress-associated genes

## Analytical workflow

The repository includes a full proof-of-concept workflow:

1. Generation of genotype classes and latent resilience structure
2. Simulation of stress environments and effective stress load
3. Generation of seed-stage and reproductive-stage datasets
4. Construction of stage-specific resilience indices
5. Statistical analysis
6. Multivariate analysis
7. Machine-learning and AI-based prediction
8. Permutation feature importance
9. Integrated breeding-priority ranking
10. Export of publishable figures and tables

## Main analyses included

- Descriptive statistics
- Treatment-wise summaries
- ANOVA-style linear models
- Pearson correlation analysis
- Principal component analysis
- K-means clustering
- Random forest regression
- Gradient boosting regression
- Multilayer perceptron regression
- Permutation feature importance
- Composite resilience scoring
- Genotype breeding-priority ranking

## Repository structure

```
RiceResilience-AI/
├── rice_resilience_proof_of_concept.ipynb
├── outputs/
│   ├── figures/
│   ├── tables/
│   └── rankings/
├── README.md
├── ModelCard.md
└── DataSheet.md
```
## Key outputs

The workflow produces:
	•	Seed-stage response profiles
	•	Reproductive-stage response profiles
	•	Correlation heatmaps
	•	PCA plots
	•	Cluster assignments
	•	Feature-importance plots
	•	Regression model performance summaries
	•	Stage-specific resilience indices
	•	Integrated breeding-priority ranking of genotypes

## Interpretation

This project is a simulation-based proof of concept. Its purpose is to test whether a biologically informed computational framework can recover known stress logic in rice and convert that logic into interpretable, breeder-facing outputs.

The results should therefore be interpreted as hypothesis-generating and workflow-validating, not as definitive agronomic conclusions.

## Intended use cases

This repository may be useful for:
	•	Rice stress biology concept development
	•	Climate-smart breeding workflow design
	•	Computational phenotyping demonstrations
	•	AI and machine-learning method prototyping in crop science
	•	Training and teaching in plant systems biology
	•	Planning empirical multi-stage stress experiments

## Limitations
	•	All observations are simulated
	•	Trait ranges are literature-guided but not meta-analytic estimates
	•	Gene-expression features are stylized relative-response variables
	•	Stress values are encoded on a relative scale
	•	The framework emphasizes interpretability over mechanistic biochemical detail
	•	Field heterogeneity, genotype-by-management interaction, and soil-microbiome effects are not explicitly modeled

## Future directions

Potential next steps include:
	•	Replacing synthetic data with real greenhouse or field measurements
	•	Integrating transcriptomics, metabolomics, or ionomics
	•	Adding genomic marker data
	•	Expanding to direct-seeded versus transplanted systems
	•	Including methane, water-use, or nutrient-efficiency traits
	•	Building multi-environment genomic prediction models
	•	Deploying breeder-facing dashboards for line prioritization

## Reproducibility

The notebook is fully reproducible under the specified Python environment, using a fixed random seed for simulation and deterministic export of figures and tables.

## Citation

**Petalcorin, M.I.R.** (2026). A multi-stage AI-enabled proof of concept for dissecting seed-stage and reproductive-stage resilience in rice under combined heat, drought, salinity, and oxidative stress. https://github.com/mpetalcorin/RiceResilience-AI

