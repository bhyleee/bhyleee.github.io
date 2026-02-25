---
title: "Radar-Based Bat Monitoring"
subtitle: "Using NEXRAD weather radar to detect free-tailed bats at landscape scale and quantify their pest-control value to agriculture."
hero_image: "/images/research/bat-radar/hero.jpg"
sidebar_image: "/images/research/bat-radar/thumb.jpg"
order: 1
tags: [radar, bats, ecosystem-services, pest-control, agriculture]
paper_url: "https://doi.org/10.1111/2041-210X.14445"
github_url: "https://github.com/bhyleee/BATS"
excerpt: "Free-tailed bats consume billions of insects annually. We built BATS—a Python toolkit using NEXRAD weather radar—to monitor roost emergence behavior at landscape scale and link it to insecticide reductions on farms."
---

## Overview
{: .no-rule}

<p class="story-lead">Free-tailed bats provide one of nature's most underappreciated services: they eat billions of insects every night, including crop pests. Yet measuring their activity at the scales relevant to farms and landscapes has remained a persistent challenge—until weather radar changed that.</p>

<div class="story-stats">
  <div class="story-stat">
    <span class="stat-number">~1B</span>
    <span class="stat-label">insects consumed per colony per night</span>
  </div>
  <div class="story-stat">
    <span class="stat-number">$1B+</span>
    <span class="stat-label">estimated annual pest-control value in TX alone</span>
  </div>
  <div class="story-stat">
    <span class="stat-number">~100</span>
    <span class="stat-label">NEXRAD radar stations across the US</span>
  </div>
</div>

![NEXRAD radar imagery showing bat emergence from Bracken Cave](/images/research/bat-radar/nexrad_emergence.jpg)
{: .story-animate}

## The Problem

Bats are cryptic. Ground-based acoustic detectors capture activity only near a sensor, and acoustic surveys are labor-intensive to scale across thousands of farms. Meanwhile, existing estimates of bat pest-control value rely on assumptions that have never been tested with real behavioral data at landscape scale.

<div class="story-callout">
"We needed a way to watch millions of bats move across the landscape every night—without being there."
</div>

NEXRAD weather radar—the same network that tracks thunderstorms—also detects large aggregations of birds, insects, and bats as they move through the atmosphere. Free-tailed bat colonies emerging from caves like Bracken Cave in Texas produce distinctive radar signatures that can be detected nightly across the entire NEXRAD network.

![Map of study region overlaid on NEXRAD coverage](/images/research/bat-radar/study_region.jpg){: .img-right .story-animate}

## The BATS Toolkit

We built **BATS (Bat-Aggregated Time Series)**, an open-source Python package that automates the extraction of bat emergence signatures from NEXRAD Level II data. BATS:

- Downloads and processes raw radar volumes from NOAA's archive
- Identifies and quantifies bat emergence pulses using a custom detection algorithm
- Produces landscape-level time series of bat activity at nightly resolution
- Links bat activity to environmental covariates (temperature, wind, moon phase)

The toolkit is freely available and works across any NEXRAD-covered colony in the US.

## Key Findings

Using BATS to monitor multiple free-tailed bat colonies across the Texas Coastal Bend, we found that:

- **Bats show targeted foraging behavior**: colonies shift their flight direction seasonally to track pest populations across agricultural landscapes
- **Agricultural context predicts foraging direction**: colonies near cotton farms shift toward those fields during moth flight season
- **Pest pressure modulates bat behavior**: nightly variation in bat emergence timing correlates with crop pest activity

![Seasonal foraging direction plots by colony](/images/research/bat-radar/foraging_direction.jpg){: .story-animate}

{: .story-callout}
A companion paper (currently in review at *Nature Sustainability*) links these radar-derived bat activity measures to reductions in insecticide applications on nearby farms—providing the first landscape-scale causal evidence for bat-driven pest control.

## Publications

**Lee, B.** (co-first author), **Sambado, S.** (co-first author), Farrant, D.N., Boser, A., Ring, K., Hyon, D., Larsen, A.E.
**Novel Bat-Monitoring Dataset Reveals Targeted Foraging With Agricultural and Pest Control Implications.**
*Ecology and Evolution*, 15(1). [DOI: 10.1002/ece3.70819](https://doi.org/10.1002/ece3.70819)

**Lee, B.**, Rich, A., Diehl, R.H., & Larsen, A.E.
**BATS: Bat-Aggregated Time Series—A Python-based toolkit for landscape-level monitoring of free-tailed bats via weather radar.**
*Methods in Ecology and Evolution*, 15(12), 2209–2215. [DOI: 10.1111/2041-210X.14317](https://doi.org/10.1111/2041-210X.14445)

**Lee, B.**, Heilmayr, R., Baylis, K., Noack, F., & Larsen, A.E.
Radar-based monitoring reveals bat-driven insecticide reductions.
*Nature Sustainability* (under review).
