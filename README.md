# Andropogon gerardi Reciprocal Garden Analyses

## Project Overview

This repository contains analysis workflows associated with the manuscript:

**“Taking genomics outdoors: linking local adaptation, trait variation, and gene expression in grass ecotypes across a rainfall gradient”**

The study evaluates ecological, physiological, and transcriptomic responses of *Andropogon gerardi* ecotypes across reciprocal garden experiments spanning a natural rainfall gradient in the central United States. Analyses include plot-level cover and biomass responses, functional trait analyses, principal components analysis (PCA), RNA-seq processing, differential gene expression, and gene co-expression analyses.

Experimental Design

Reciprocal garden experiments were established across a rainfall gradient including:

Colby, Kansas, USA (driest site)
Hays, Kansas, USA (dry site)
Manhattan, Kansas, USA (mesic site)
Carbondale, Illinois, USA (wet site)

Experimental rainout shelters (~50% rainfall reduction) were installed at Hays, Manhattan, and Carbondale sites.

Ecotypes included:

Dry ecotype
Mesic ecotype
Wet ecotype
Analyses Included
1. Cover and Biomass Analyses

Script:

scripts/01_cover_biomass_trait_analysis.jsl

Analyses include:

Plot-level canopy cover
Aboveground biomass
Split-plot ANOVA models
Fixed effects:
Site
Ecotype
Treatment
Interactions
Random effects:
Block
Quadrat/plot repetition
Tukey HSD post hoc comparisons

Analyses were conducted using JMP Pro 17 (SAS Institute Inc., Cary, NC, USA).

2. Functional Trait Analyses

Traits analyzed include:

Photosynthetic rate
Stomatal conductance
Transpiration
Water-use efficiency
SPAD chlorophyll absorbance
Leaf thickness
Leaf width
Height
Canopy diameter
Total biomass
Seed biomass
Leaf carbon concentration
Leaf nitrogen concentration
Internal CO₂ concentration
Flowering and bolting phenology

Separate models were conducted by season and treatment.

3. Principal Components Analysis (PCA)

PCA analyses were conducted to evaluate multivariate trait coordination across:

Ecotypes
Sites
Homesites
Rainout treatments

Trait values were log-transformed prior to analysis.

4. RNA-seq Processing

Scripts include:

FASTQ quality control
Read trimming
HISAT2 genome alignment
SAM/BAM processing
featureCounts count matrix generation

Reference genome:
Andropogon gerardi Hap2 v1.1 (Joint Genome Institute)

5. Differential Gene Expression

Differential expression analyses were performed using:

DESeq2
Adjusted p-value threshold: padj < 0.05

Comparisons included:

Ecotype
Site
Homesite
Rainout treatment
6. Weighted Gene Co-expression Network Analysis (WGCNA)

WGCNA analyses identified:

Co-expressed gene modules
Gene–trait associations
Hub genes associated with adaptive traits
Software Requirements
Ecological and Trait Analyses
JMP Pro 17
RNA-seq Analyses
fastp
HISAT2
SAMtools
featureCounts
FastQC
R Packages
DESeq2
WGCNA
pheatmap
igraph
geneplotter
Data Availability

Processed trait, cover, biomass, and transcriptomic datasets are available in this repository upon publication.

Raw RNA-seq reads will be deposited in NCBI SRA upon manuscript acceptance.

Contact: Jack Sytsma, sytsmaj134@ksu.edu

Citation

If using these scripts or data, please cite:

Sytsma J., Galliart M., Fogarty K., Howe K., Olson B.J.S.C., Baer S.G., Gibson D.J., Maricle B., Hartung E., and Johnson L.C. Taking genomics outdoors: linking local adaptation, trait variation, and gene expression in grass ecotypes across a rainfall gradient. (2026). Molecular Ecology.
