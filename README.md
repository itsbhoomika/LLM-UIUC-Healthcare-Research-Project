# Predictive Modeling for Clinical Trials Using LLM Feature Extraction

> Transforming unstructured clinical trial descriptions into structured ML features using a **supervised learning feedback loop with LLMs** — Statistics Dept, UIUC.

[![Python](https://img.shields.io/badge/Python-3.9+-blue?logo=python)](https://python.org)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)](https://jupyter.org)

> **Interactive notebook (with outputs):** [Colab](https://colab.research.google.com/drive/1wijB5DZEg8d_zAywuaVC-Wf2pvXdIS4v#scrollTo=owBsntoEwMUD)

## Problem

Clinical trial datasets contain large amounts of unstructured text — study design, interventions, eligibility criteria, outcomes. Key success predictors are buried in narrative descriptions and invisible to traditional ML models that only consume structured columns.

**Goal:** Build a scalable pipeline that uses an LLM to automatically extract structured attributes from trial descriptions and convert them into predictive features.

## Dataset

- Source: [ClinicalTrials.gov](https://clinicaltrials.gov) — 115,480 cancer trials, 33 columns
- After filtering ambiguous statuses: **79% completed** (success) · **21% terminated/withdrawn** (failure)
- Task: predict trial completion from description + metadata

## File Guide

| File | What it does |
|------|--------------|
| `Bhoomika_project_with_markdowns (2).ipynb` | **Full pipeline** — LLM feature extraction, prompt iteration, ML model training and evaluation on ClinicalTrials.gov data |
| `Bhoomika_project_with_markdowns.html` | Static HTML export for offline viewing |
| `Predictive Modeling-Bhoomika-Ravishankar.pdf` | Research report: methodology, results, and analysis |

## Pipeline

```
Raw Clinical Trial Text
        │
        ▼
LLM Feature Extraction (structured attributes from free text)
        │
        ├── Study design characteristics
        ├── Intervention mechanisms
        ├── Patient eligibility constraints
        └── Operational logistics
        │
        ▼
Structured Feature Matrix → ML Model (classification)
        │
        ▼
Model Feedback → Refined LLM Prompt → Improved Features
```

The feedback loop is the key contribution: ML model performance guides iterative refinement of the LLM extraction prompt, improving feature quality without manual annotation.

## Key Findings

- LLM-extracted features improved predictive performance over structured metadata alone
- Prompt refinement guided by model feedback produced more consistent and informative features
- Demonstrates a generalizable pattern for text-heavy datasets where manual feature engineering is infeasible

## Tech Stack

`Python` · `OpenAI / Gemini API` · `Scikit-learn` · `Pandas` · `ClinicalTrials.gov API`

## Context

Research project at the **Statistics Department, University of Illinois Urbana-Champaign**.
