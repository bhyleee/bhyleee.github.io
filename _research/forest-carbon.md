---
title: "Forest Carbon Remote Sensing"
subtitle: "Quantifying changes in forest carbon stocks using multi-sensor remote sensing and machine learning across tropical and temperate landscapes."
hero_image: "/images/research/forest-carbon/hero.jpg"
sidebar_image: "/images/research/forest-carbon/thumb.jpg"
order: 2
tags: [remote-sensing, LiDAR, SAR, forest, carbon, machine-learning]
excerpt: "Forests store vast amounts of carbon, but tracking how those stocks change over time is difficult at scale. We fuse LiDAR, SAR, and optical imagery with machine learning to produce reliable landscape-level estimates of forest biomass and carbon flux."
---

## Overview
{: .no-rule}

<p class="story-lead">Forests are among Earth's most important carbon sinks, but accurately tracking how that carbon changes—due to disturbance, regrowth, or degradation—requires measuring tree structure at scales far beyond what ground surveys alone can provide.</p>

<div class="story-stats">
  <div class="story-stat">
    <span class="stat-number">~45%</span>
    <span class="stat-label">of terrestrial carbon stored in forest biomass</span>
  </div>
  <div class="story-stat">
    <span class="stat-number">2.6B</span>
    <span class="stat-label">hectares of forest globally</span>
  </div>
  <div class="story-stat">
    <span class="stat-number">3</span>
    <span class="stat-label">sensor types fused in our approach</span>
  </div>
</div>

![Forest canopy height map derived from multi-sensor fusion](/images/research/forest-carbon/canopy_height.jpg)
{: .story-animate}

## The Challenge

Ground-based forest inventories are accurate but expensive and sparse. Optical satellite imagery captures forest extent and greenness but cannot see through canopies to measure structure. This gap between what satellites observe and what managers need to know—tree height, basal area, biomass—has long been the central challenge in forest carbon science.

<div class="story-callout">
"Measuring carbon where it matters most—in the canopy and belowground—requires sensors that can pierce the forest, not just photograph its surface."
</div>

## Multi-Sensor Fusion Approach

![SAR backscatter sensitivity to forest structure](/images/research/forest-carbon/sar_sensitivity.jpg){: .img-right .story-animate}

Our approach combines three complementary data streams:

**LiDAR** (airborne and spaceborne) provides direct measurements of canopy height and vertical structure—the gold standard for biomass estimation. We use ICESat-2 and GEDI as spaceborne LiDAR references.

**SAR (Synthetic Aperture Radar)** penetrates cloud cover and is sensitive to woody biomass. L-band SAR (ALOS PALSAR) saturates in high-biomass forests, but we model saturation explicitly and combine with C-band Sentinel-1 to extend the dynamic range.

**Optical imagery** (Landsat, Sentinel-2) captures spectral variation in canopy chemistry and phenology, providing dense temporal coverage that links LiDAR and SAR snapshots to continuous time series.

## Machine Learning for Landscape Extrapolation

We train gradient boosting and deep learning models to extrapolate LiDAR-derived biomass estimates across entire landscapes using SAR and optical covariates as predictors. Key modeling choices include:

- Spatial cross-validation to avoid overfitting to local conditions
- Uncertainty quantification (prediction intervals) so users know where estimates are reliable
- Transfer learning to adapt models trained in one region to new forest types

![Model performance across forest types](/images/research/forest-carbon/model_performance.jpg){: .story-animate}

## Study Regions

Current work focuses on:

- **Central American dry forests**: tracking forest recovery after agricultural abandonment
- **Pacific Northwest**: monitoring carbon flux following wildfire and harvest
- **Atlantic Forest, Brazil** (in collaboration with NASA Goddard): mapping degradation not captured by deforestation metrics

## Why It Matters

Accurate, spatially explicit carbon maps enable:

- Credible forest carbon offsets and REDD+ monitoring
- Identifying forests at highest risk of carbon loss
- Detecting degradation (not just clearing) that optical sensors miss

## Publications

**Lee, B.**, Rich, A., Fatoyinbo, L., Thomas, N., Stovall, A., Olmedo, G.F., Ramirez, P.I., & Heilmayr, R.
Tree-mendous changes: Quantifying changes in forest carbon using remote sensing and machine learning.
*In preparation* (targeting *Remote Sensing of the Environment*).

Thomas, N., **Lee, B.**, Coutts, O., Bunting, P., Lagomasino, D., & Fatoyinbo, L.
**A purely spaceborne open-source approach for regional bathymetry mapping.**
*IEEE Transactions on Geoscience and Remote Sensing*, 60, 1–9. [DOI: 10.1109/TGRS.2022.3152674](https://doi.org/10.1109/TGRS.2022.3192825)
