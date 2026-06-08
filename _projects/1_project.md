---
layout: page
title: RF Sputtering of Aluminium Thin Films
description: Optimized Al thin-film deposition for Metal-Induced Layer Exchange in quantum computing applications
img: assets/img/12.jpg
importance: 1
category: work
---

## Overview
Deposited ~100 nm aluminium thin films on silicon wafers using RF sputtering, optimized for the **Metal-Induced Layer Exchange (MIL)** process with amorphous silicon. The target application is isotopically enriched Si-28 — a critical material for spin-based quantum computing architectures requiring nuclear spin-free environments.

This work was carried out at SSN College of Engineering using the RF sputtering facility at the institution's research centre.

## Problem Statement
The MIL process for producing high-purity Si-28 depends critically on the quality of the aluminium seed layer. Precise control over film thickness, grain size, and surface roughness is essential for uniform, defect-free silicon recrystallization. Existing literature had not fully optimized RF sputtering parameters specifically for MIL applications.

## My Role
- Systematic optimization of RF sputtering process parameters
- Substrate preparation using standard RCA cleaning protocol
- Design and execution of 8 experimental runs across varying power, pressure, temperature, and deposition time
- Film characterization using profilometry, FE-SEM, and AFM
- Data analysis using ImageJ for grain size quantification

## Methods

| Technique | Purpose |
|---|---|
| RCA Cleaning | Removal of organic, metallic, and oxide contaminants from Si wafers |
| RF Sputtering | Al thin film deposition (99.99% purity Al target) |
| Thickness Profilometry (Bruker Dektak XT) | Step-height measurement of deposited films |
| FE-SEM (Thermo Fisher Apreo 2) | Surface morphology and EDS elemental mapping |
| AFM (JPK NanoWizard XP) | Surface roughness quantification (Ra, Rq) |

## Characterization Images

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/sem_RT.png" title="SEM Sample A - Room Temperature" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/sem_150.png" title="SEM Sample B - 150°C" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 1 FE-SEM surface morphology — Sample A (room temperature, ~40 nm uniform grains) vs Sample B (150°C, ~500 nm coarse grains with voids)
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/afm_2d.png" title="AFM 2D Topography" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/afm_3d.png" title="AFM 3D Surface Map" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 2(a) 2D AFM height map and (b) 3D surface topography of optimized Al thin film
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/afm_profile.png" title="AFM Cross-sectional Profile" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 2(c) Cross-sectional roughness profile — Ra = 5.385 nm, Rq = 6.719 nm
</div>

## Key Results

**Optimized parameters:** 250 W RF power · Room temperature (28°C) · 0.001 mbar working pressure · 1 hour deposition

- ✅ Achieved target film thickness of **~100 nm**
- ✅ Fine, densely packed grains of **~40 nm** (confirmed via FE-SEM + ImageJ)
- ✅ Surface roughness: **Ra = 5.385 nm, Rq = 6.719 nm**
- ✅ Uniform Al distribution confirmed by EDS elemental mapping
- ❌ Films deposited at 150°C showed grain coarsening (~500 nm), clustering, and voids — unsuitable for MIL

Room-temperature deposition suppressed adatom mobility, preventing Volmer–Weber island growth and yielding a smooth, continuous film suitable for subsequent layer exchange processing.

## Skills Demonstrated
RF Sputtering · Thin Film Deposition · Semiconductor Processing · FE-SEM · AFM · Surface Profilometry · RCA Cleaning · ImageJ Analysis · Experimental Design · Materials Characterization
