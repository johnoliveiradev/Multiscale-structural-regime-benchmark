# Multiscale Structural Regime Benchmark

This repository documents an empirical phenomenon observed in coupled dynamical systems.

## Problem
When two systems appear to overlap, it is unclear whether the overlap reflects
true structural coupling or coincidental effects such as density, marginals,
or shared support.

## Benchmark Question
Is there a parameter regime in which the intersection between two systems
exhibits multiscale structural persistence that cannot be explained by
strong null models?

## Data
We provide:
- A baseline system (Φ⁺)
- A scenario system (Φ⁻)
- Two null models:
  - Marginal-preserving (Y-permutation)
  - Support-preserving (occupancy-preserving)

All datasets are synthetic and fully reproducible.

## Observation
Across a sweep of the control parameter r, a critical regime is observed
(r ≳ 0.45) where the real system separates consistently from both nulls
under multiscale analysis.

This separation persists across resolutions and bootstrap trials.

## What This Is Not
- This is not a model.
- This is not a classifier.
- This repository does not propose a method.

It documents a regime-level structural phenomenon.

## Status
The mechanism detecting this regime is intentionally not included.
The benchmark exists to characterize the phenomenon itself.
