---
layout: page
title: Adaptive UQ Engine for Materials Datasets
description: Open-source Python engine implementing GUM, Monte Carlo, and QRNN for automatic uncertainty quantification
img: assets/img/nergy_platform.png
importance: 5
category: work
---

## Overview

An open-source Python engine that automatically selects and executes the right uncertainty quantification method for experimental materials data — outputting five interactive HTML reports per run.

Built from real research experience in anodization process optimization, corrosion science, and thin-film deposition. The engine is demonstrated on oxide layer thickness (TOL) data from industrial anodization experiments at Brakes India Pvt. Ltd.

**GitHub:** [annegracia/materials-uq-engine](https://github.com/annegracia/materials-uq-engine)

---

## The Problem

In materials science, every measurement carries uncertainty. A reported oxide layer thickness of 12.15 μm is not a precise value — it is the center of a distribution shaped by instrument noise, environmental variation, sample preparation inconsistency, and measurement technique limitations.

Most researchers either skip UQ entirely or apply GUM blindly to nonlinear data where it systematically underestimates uncertainty. This engine solves that by automatically diagnosing your data and routing it to the right method.

---

## Adaptive Method Selection

The engine computes the **coefficient of variation (CV)** of the target data and selects:

| CV Range | Method Selected | Why |
|---|---|---|
| CV < 0.05 | GUM | Near-linear, low variance — analytical propagation sufficient |
| CV < 0.20 | Monte Carlo | Moderate nonlinearity — sampling captures asymmetry |
| CV ≥ 0.20 | QRNN | High variance, skewed — neural network quantile regression |

---

## Methods

**GUM (ISO/IEC 98-3)** — Type A uncertainty propagation. Computes mean, standard uncertainty u_mean = σ/√n, and expanded uncertainty U95 = k·u_mean where k is the t-distribution coverage factor.

**Monte Carlo** — Fits Normal(μ, σ) to data, draws 50,000 samples, returns 2.5th–97.5th percentile confidence interval. Captures nonlinearity GUM misses.

**QRNN (Quantile Regression Neural Network)** — PyTorch network (Linear→ReLU→Linear→ReLU→Linear(3)) trained with pinball loss to simultaneously predict 2.5%, 50%, and 97.5% quantile bounds. No distribution assumptions. Best for noisy, skewed, or high-variance datasets.

---

## Results on Anodization Data

Dataset: 20 experimental runs on aluminium automotive plungers varying temperature, electrolyte concentration, current density, and exposure time. Target: TOL (μm).

**CV = 0.36 → QRNN selected automatically**

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/1_uq_TOL_um_qrnn.png" title="UQ Result" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/2_summary_table.png" title="Summary Table" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left: QRNN quantile bounds on raw TOL measurements. Right: GUM vs Monte Carlo vs QRNN summary table.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3_comparison.png" title="Method Comparison" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/4_distribution.png" title="Distribution" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left: GUM vs Monte Carlo vs QRNN CI comparison. Right: TOL data distribution showing right skew (skewness = 1.09).
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5_correlation.png" title="Correlation Heatmap" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Correlation heatmap — exposure time and temperature are the dominant drivers of TOL variability.
</div>

---

## Key Findings

- GUM underestimates the upper CI bound because TOL data is right-skewed — a known failure mode of linear analytical propagation
- QRNN correctly captures the asymmetric uncertainty envelope without any distribution assumptions
- Correlation heatmap identifies **exposure time** and **temperature** as the dominant process variables driving TOL variability
- All 3 methods agree on the mean (~12.5 μm) but diverge significantly on upper bounds — highlighting why method selection matters

---

## Skills Demonstrated
Python · PyTorch · Plotly · Uncertainty Quantification · GUM · Monte Carlo · Neural Networks · Materials Characterization · Electrochemistry · Data Analysis
