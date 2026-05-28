# Numerical Methods from Scratch

A research-grade, **6-week** masterclass in classical **Numerical Analysis**, built entirely from first principles. No SciPy, no black-box solvers — just **pure NumPy and Matplotlib**. Every algorithm is implemented, analyzed for its order of convergence, and stress-tested against its failure modes.

This course is the *classical numerical analysis* companion to [`numerical_methods_for_ml`](https://github.com/HAYDARKILIC/numerical_methods_for_ml): where that repo rebuilds the ML numerical stack (autodiff, SVD, BFGS, GPs), this one covers the **foundational pillars** — floating-point reality, root-finding, linear systems, interpolation, quadrature, and differential equations.

Each week is a single, self-contained Jupyter notebook combining **theoretical derivations**, **from-scratch implementations**, **visualizations**, and **research-style exercises**.

---

## Philosophy

> *Algebraically equivalent expressions are not numerically equivalent.*

The unifying thread of the course is the distinction between the **conditioning of a problem** and the **stability of an algorithm**, tied together by the master rule of numerical analysis:

```
forward error  ≲  condition number  ×  backward error
```

Every method is judged through this lens — from the quadratic formula in Week 1 to stiff ODE solvers in Week 6.

---

## Curriculum

| Week | Topic | Key methods built from scratch |
|:---:|---|---|
| **1** | Floating-Point & Error Analysis | Machine epsilon, catastrophic cancellation, conditioning, backward error |
| **2** | Root-Finding | Bisection, fixed-point, Newton, secant, safeguarded hybrid; convergence-order estimation |
| **3** | Linear Systems | LU + partial pivoting, Cholesky, condition numbers, iterative refinement |
| **4** | Interpolation & Approximation | Lagrange/Newton forms, Runge phenomenon, Chebyshev nodes, cubic splines, least squares |
| **5** | Differentiation & Integration | Finite differences, Richardson extrapolation, Newton–Cotes, adaptive & Gaussian quadrature |
| **6** | ODEs & Finite Differences *(capstone)* | Euler, RK4, adaptive RK, stiffness & implicit methods, boundary-value problems |

The capstone deliberately re-uses the machinery of all five earlier weeks — root-finding inside implicit steps, linear solvers for boundary-value problems, quadrature behind time-stepping — to show numerical methods as **one coherent discipline**.

---

## Repository structure

```
numerical_methods/
├── notebooks/
│   ├── week1_floating_point_and_error_analysis.ipynb
│   ├── week2_root_finding.ipynb
│   ├── week3_linear_systems.ipynb
│   ├── week4_interpolation_approximation.ipynb
│   ├── week5_differentiation_integration.ipynb
│   └── week6_odes_and_finite_differences.ipynb
├── requirements.txt
├── LICENSE
└── README.md
```

---

## Getting started

```bash
git clone https://github.com/HAYDARKILIC/numerical_methods.git
cd numerical_methods
pip install -r requirements.txt
jupyter notebook notebooks/
```

The only dependencies are **NumPy**, **Matplotlib**, and **Jupyter**. Every notebook runs top-to-bottom with no external data.

---

## Prerequisites

- Calculus (Taylor series, derivatives, integrals)
- Linear algebra (matrices, eigenvalues — see [`linear_algebra_for_ml`](https://github.com/HAYDARKILIC/linear_algebra_for_ml))
- Comfortable Python + NumPy

---

## License

Released under the MIT License — see [`LICENSE`](LICENSE).
