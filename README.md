# Glacier Mass Balance Modeling
## Numerical ODE Analysis of Glacial Tipping Points

**GP 145/245, Computational Earth System Analysis**  
**Milo Skapinsky, Stanford University, Spring 2026**

---

## Overview

This project implements and analyzes the Oerlemans (2012) glacier length ODE model 
to investigate critical warming thresholds and bifurcation behavior in glacier dynamics. 
We implement Euler and RK4 solvers from scratch, extend the model with a nonlinear term, 
and use Numba JIT compilation and parallelism to accelerate parameter sweeps.

**Question:** At what critical warming threshold ΔT* does glacier retreat 
become irreversible, and how does this depend on model parameters and initial conditions?

---

## Key Results

- **Analytical T*:** ΔT* = -1/(4ατkβ) = **1.333°C** above pre-industrial baseline
- **Numerical convergence:** T* recovered to within 0.002°C at t=10,000 years
- **Computational speedup:** A 335x total speedup using Numba JIT (84x) + parallelism (4x) over pure Python serial code

---

## Repository Structure

```
Final_Project/
├── glacier_model.ipynb     # Main notebook, all the code and analysis
└── README.md               # This file
```

---

## Requirements

```
numpy
matplotlib
numba
```

Install with:
```bash
pip install numpy matplotlib numba
```

---

## How to Run

1. Clone the repository:
```bash
git clone https://github.com/biondiettore/GP145_245_Spring2026.git
cd GP145_245_Spring2026/Final_Project
```

2. Install dependencies:
```bash
pip install numpy matplotlib numba
```

3. Open the notebook:
```bash
jupyter notebook glacier_model.ipynb
```

4. Run all cells in order: **Kernel → Restart & Run All**

---

## Reference

Oerlemans, J. (2012). Linear modelling of glacier length fluctuations. 
*Geografiska Annaler: Series A, Physical Geography*, 94(2), 183-194.