---
layout: page
title: AI-Assisted Materials Research Platform — N-ERGY
description: Building automation infrastructure for AI-driven scientific discovery at N-ERGY AI Solutions
img: assets/img/nergy_platform.png
importance: 4
category: work
---

## Overview
Contributed to the development of an **AI-powered R&D automation platform** at [N-ERGY AI Solutions](https://www.nergyai.com/), designed to compress the materials discovery timeline from 5–10 years down to months. The platform integrates automated literature retrieval, AI-driven research gap identification, and simulation agents into a unified research workflow.

## Platform

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/nergy_platform.png" title="N-ERGY Platform" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    N-ERGY AI Platform — Query interface showing Deep Research, Quick Search, and Design Workspace modes for AI-driven materials discovery.
</div>

The platform consists of two core agents:
- **MatGeek** — a RAG (Retrieval-Augmented Generation) agent for automated scientific literature ingestion, search, and analysis
- **Axiom** — a simulation agent for automated materials property prediction

## My Journey
Joined N-ERGY as an **Experimental Materials Associate**, contributing to RF sputtering and thin-film synthesis work. When the company pivoted to building the AI platform, transitioned to the computational team — bridging domain expertise in materials science with platform development.

## My Contributions

### Literature Ingestion Pipeline (MatGeek)
- Building an automated paper ingestion pipeline using the **OpenAlex API** to search and retrieve open-access scientific publications
- Papers are processed and stored in a vector database, enabling semantic search and retrieval for the RAG agent
- Designed the pipeline to run autonomously — from API query → paper retrieval → processing → database ingestion

### Uncertainty Quantification (UQ) Module
- Developed Python classes for **uncertainty quantification (UQ)** of complex materials datasets
- Standardized automated analysis workflows for electrochemical and materials characterization data
- Built reusable, modular pipeline applicable across different experimental datasets

### Data Visualization & Results Interface
- Built interactive data visualizations using **Plotly** for displaying simulation and experimental results within the platform
- Designed result collection workflows to present materials property outputs in a researcher-friendly format
- Contributed to **Streamlit-based UI** components for platform interaction

## Tech Stack
Python · OpenAlex API · RAG Architecture · Vector Databases · Plotly · Streamlit · PyMongo · Git/GitHub · LLMs · Scientific Data Processing

## Proof of Work
- Active collaborator across private platform repositories (UI, backend, MatGeek, Axiom)
- Sole owner of the UQ module repository
- Transitioned from experimental to computational role based on platform needs — demonstrating adaptability across both domains

## Why This Matters for Materials Research
Traditional materials discovery relies on manual literature review, trial-and-error experimentation, and siloed workflows. This platform automates the full research cycle — from literature to simulation to results — directly addressing one of the biggest bottlenecks in materials science and energy research.

## Skills Demonstrated
RAG Systems · Literature Ingestion Pipelines · API Integration · Uncertainty Quantification · Python · Plotly · Streamlit · Scientific Data Processing · AI Platform Development · Materials Informatics

## Open Source

As part of this work I built and open-sourced an adaptive UQ engine for materials datasets:

**[materials-uq-engine](https://github.com/annegracia/materials-uq-engine)** — Python engine implementing GUM, Monte Carlo, and QRNN for automatic uncertainty quantification. Demonstrated on real anodization and corrosion datasets.
