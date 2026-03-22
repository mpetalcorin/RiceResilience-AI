# Datasheet for Dataset

## Dataset name

**Synthetic multi-stage rice resilience dataset under combined abiotic stress**

## Motivation

This dataset was created to support a computational proof of concept for analyzing rice resilience at two major developmental stages:

- seed-stage establishment
- reproductive-stage performance

The goal was to generate a structured, biologically plausible dataset that captures how rice genotypes may respond to:

- heat
- drought
- salinity
- oxidative stress
- and stress combinations

The dataset was built to enable integrated statistical, multivariate, and machine-learning analyses in support of climate-smart breeding concepts.

## Dataset composition

The dataset consists of three main components:

1. **Seed-stage dataset**
2. **Reproductive-stage dataset**
3. **Integrated multi-stage genotype-level dataset**

### Genotypes

The simulation includes **40 rice genotypes** partitioned into five subpopulation classes:

- Salt-tolerant
- Drought-tolerant
- Heat-tolerant
- Combined-tolerant
- Susceptible

### Environments

The dataset includes nine environments:

- Control
- Heat
- Drought
- Salinity
- Oxidative
- Heat+Drought
- Heat+Salinity
- Drought+Salinity
- Combined_All

### Replication

Each genotype x environment x stage combination includes biological replicates in the simulation design.

## Data generation process

The dataset was generated programmatically from a literature-guided simulation framework. Each genotype was assigned latent resilience capacities across:

- heat resilience
- drought resilience
- salinity resilience
- oxidative or redox resilience

Nominal stress vectors were defined for each environment, then converted to genotype-specific effective stress loads using resilience buffering. Stage-specific plant-level and molecular-style traits were then simulated as functions of:

- baseline biology
- genotype resilience
- effective stress
- compound-stress synergy
- stochastic variation

This design allows biologically structured covariance between traits, rather than random independent sampling.

## Variables included

### Seed-stage variables

- genotype
- subpopulation
- treatment
- replicate
- germination
- root_length
- vigor_index
- Na_K_ratio
- H₂O₂
- MDA
- proline
- SOD
- CAT
- APX
- relative expression features
- resilience-related latent features

### Reproductive-stage variables

- genotype
- subpopulation
- treatment
- replicate
- pollen_viability
- spikelet_fertility
- yield_per_plant
- grain_weight
- photosynthesis
- Na_K_ratio
- H₂O₂
- MDA
- proline
- SOD
- CAT
- APX
- relative expression features
- resilience-related latent features

### Derived outputs

- treatment means
- summary statistics
- ANOVA results
- correlation matrices
- PCA scores
- cluster assignments
- feature-importance tables
- resilience indices
- breeder-priority rankings

## Recommended units

The dataset contains a mixture of unit-bearing and relative variables.

### Typical units

- Germination: %
- Root length: cm
- Pollen viability: %
- Spikelet fertility: %
- Yield per plant: g plant⁻¹
- Grain weight: mg grain⁻¹
- Na⁺/K⁺ ratio: ratio
- H₂O₂: relative units or concentration-style units
- MDA: relative units or concentration-style units
- Proline: relative units or concentration-style units
- SOD, CAT, APX: relative activity units
- Expression variables: normalized relative expression

Because this is a synthetic dataset, some variables are intentionally represented in normalized or relative form rather than as direct laboratory units.

## Uses

### Suitable uses

- Testing computational workflows
- Demonstrating multi-stage stress analysis
- Teaching machine learning in crop science
- Exploring trait integration across developmental stages
- Prototyping breeder-facing ranking frameworks
- Building visualizations for abiotic stress biology

### Unsuitable uses

- Estimating real cultivar performance
- Publishing empirical trait values as measured observations
- Making field recommendations
- Claiming validated genotype superiority
- Replacing wet-lab or field phenotyping

## Distributional characteristics

The data were simulated to satisfy several biological expectations:

- beneficial performance traits are highest under control conditions
- injury-associated biochemical traits rise under stress
- combined stress is generally more damaging than single stress
- heat-containing environments strongly affect reproductive traits
- salinity-containing environments strongly affect ionic balance
- tolerant classes outperform susceptible classes, but not perfectly

The dataset therefore preserves structured overlap rather than trivial class separation.

## Preprocessing

The following preprocessing steps may be required depending on the downstream analysis:

- one-hot encoding of treatment and subpopulation
- standardization of numeric features
- aggregation across replicates when genotype-level summaries are needed
- transformation of ranking scores or resilience indices for visualization

## Missing data

The synthetic dataset was generated as a complete dataset with no missing values by default.

If users adapt the workflow to empirical data, missingness handling will need to be implemented explicitly.

## Relationships to other data

This dataset is not derived from a single empirical experiment. Instead, it is a **synthetic, literature-informed representation** of rice stress-response biology inspired by recurring findings in published rice physiology and stress-response studies.

It should therefore be treated as a computational scaffold rather than a benchmark field dataset.

## Data quality considerations

### Strengths

- structured multivariate biological relationships
- explicit developmental staging
- stress interaction modeling
- compatibility with statistical and AI workflows
- breeder-oriented composite outputs

### Limitations

- no empirical measurements
- no true field heterogeneity
- no genotype marker matrix
- no direct transcriptomics or metabolomics
- no management effects
- no season-to-season weather variation
- not suitable for direct biological inference without validation

## Sensitivity and bias

The dataset reflects modeling assumptions chosen by the author, including:

- the importance of oxidative stress as a central convergence layer
- the dominant role of pollen viability and spikelet fertility in reproductive yield
- the use of latent resilience classes
- positive adaptive interpretation of antioxidant and osmolyte responses

These assumptions are scientifically motivated but can shape the apparent importance of some variables.

## Maintenance and updates

This datasheet should be updated when:

- additional stress conditions are included,
- empirical data replace simulated data,
- genomic marker data are added,
- new derived indices are introduced,
- or the simulation framework is re-parameterized.

## Version

Version: 1.0  
Status: Synthetic proof-of-concept dataset
