# Multiscale Structural Regime Benchmark

This repository documents an empirical phenomenon observed in coupled dynamical systems:  
the emergence of a **multiscale structural regime** that persists under strong null models.

No method or model is proposed here.

---

## Problem

When two systems appear to overlap, it is unclear whether the overlap reflects:

- genuine structural coupling, or
- coincidental effects such as shared marginals, density, or spatial support.

Existing tools typically analyze individual systems, signals, or causal influence,  
but do not directly address **whether a joint structure truly exists across scales**.

---

## Benchmark Question

> Is there a parameter regime in which the intersection between two systems
> exhibits multiscale structural persistence that cannot be explained by
> strong null models?

This benchmark exists to document that regime empirically.

---

## What Is Included

This repository contains **aggregated empirical results only**, organized under `results/`:

- **Gap analysis** between the real system and null controls
- **Robustness checks** across:
  - multiple random seeds
  - multiple spatial resolutions
  - bootstrap confidence intervals
- **Parameter sweep** identifying the regime where separation emerges

The key outputs are:

- `copitolo_prego.png` / `copitolo_prego.json`  
  Empirical separation between REAL and NULL systems across a parameter sweep.

- `copitolo_report.json`  
  Summary statistics including confidence intervals and robustness metrics.

- `copitolo_runs.csv`  
  Per-run diagnostics (index estimates, fit quality, proxies).

- `copitolo_sweep.json`  
  Regime-level behavior as the control parameter varies.

---

## Null Models Used

Two strong null models are used to rule out trivial explanations:

1. **Marginal-preserving null (Y-permutation)**  
   Preserves marginal distributions while destroying correlation.

2. **Support-preserving null (occupancy-preserving)**  
   Preserves coarse spatial support while destroying micro-geometry.

The observed regime separates from both nulls consistently.

---

## Interpretation Guide

- Values above zero in the reported gap plots indicate that the real system
  exhibits stronger multiscale structure than the corresponding null model.

- Persistence across scales, seeds, and confidence intervals indicates
  a regime-level phenomenon rather than noise or artifact.

This repository intentionally avoids proposing a specific metric or algorithm.
It documents the phenomenon itself.

---

## What This Is Not

- This is **not** a classifier.
- This is **not** a predictive model.
- This is **not** a learning-based system.
- This repository does **not** include the mechanism used to detect the regime.

The focus is on **existence and robustness**, not implementation.

---

## Data Availability

Raw point clouds (Φ⁺, Φ⁻) and internal detection mechanisms are not included at this stage.

The reported results are aggregated, regime-level, and do not depend on any specific
realization of the underlying systems.

Future releases may include reference datasets.

---

## Status

This benchmark is intended to:
- establish the existence of a multiscale structural regime,
- provide a neutral testbed for independent interpretation,
- and invite alternative explanations or detection approaches.

The phenomenon documented here remains regardless of the method used to analyze it.
