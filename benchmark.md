# Multiscale Structural Regime Benchmark

## Purpose

This benchmark formalizes an empirical test for the **existence of multiscale structural persistence**
in the intersection of two systems.

It is designed to answer a single question:

> Does there exist a parameter regime in which the joint structure between two systems
> cannot be explained by marginal distributions, density, or coarse spatial support alone?

The benchmark does not assume any specific detection method.

---

## Systems

Let:

- Φ⁺ denote a baseline system.
- Φ⁻(r) denote a parameterized system depending on a control parameter r.

The nature of the systems is intentionally unrestricted.
They may arise from dynamical systems, embeddings, or other constructions.

---

## Intersection

Define the empirical intersection Ψ(r) as the joint support occupied by Φ⁺ and Φ⁻(r)
under a multiscale discretization.

No assumptions are made about metric, probability, causality, or learning.

---

## Null Models

Two null models are used to control for trivial explanations:

### Null A — Marginal-Preserving (Y-Permutation)

- Preserves marginal distributions.
- Preserves point density.
- Destroys correlation and geometric alignment.

This null tests whether observed structure can be explained by marginals alone.

---

### Null B — Support-Preserving (Occupancy-Preserving)

- Preserves coarse spatial support.
- Preserves occupancy of discretized cells.
- Destroys micro-geometry and fine-scale organization.

This null tests whether observed structure is an artifact of shared support.

---

## Success Criteria

A method or observation is considered successful on this benchmark if it satisfies **all** of the following:

1. **Separation**  
   The real system exhibits a positive gap relative to both null models.

2. **Multiscale Consistency**  
   Separation persists across multiple discretization scales.

3. **Statistical Robustness**  
   Separation remains within 95% confidence bounds under resampling.

4. **Regime Localization**  
   Separation emerges within a contiguous interval of the control parameter r.

---

## Outputs

The benchmark reports:

- Aggregate gap statistics between REAL and NULL systems.
- Confidence intervals for observed separation.
- Diagnostics of scale consistency and stability.
- Parameter sweeps identifying regime boundaries.

The benchmark does not prescribe how these quantities are computed.

---

## Non-Goals

This benchmark does **not** attempt to:

- Prove Hausdorff or Minkowski dimension formally.
- Establish global monotonicity across all r.
- Attribute causality or directionality.
- Provide a predictive or generative model.

It documents an empirical structural regime.

---

## Reproducibility Scope

This repository documents observed results under the above benchmark definition.

The benchmark is agnostic to:
- implementation details,
- choice of metric,
- choice of detection algorithm.

Independent implementations are encouraged to test whether they observe
the same regime-level behavior.

---

## Interpretation

If no method can reproduce the observed separation under these null controls,
the phenomenon remains unexplained.

If multiple methods reproduce it, the benchmark has identified
a structural property that exists independently of any specific approach.

In both cases, the benchmark remains valid.

---

## Status

This benchmark defines a **regime-level question**, not a solution.

It exists to anchor discussion, replication attempts, and theoretical explanation
around a concrete empirical phenomenon.
