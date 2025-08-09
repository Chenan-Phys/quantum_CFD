# Hybrid Quantum Solver for the 1D Burgers' Equation

This repository contains the code and documentation for a hybrid quantum-classical algorithm designed to solve the one-dimensional viscous Burgers' equation, a key model in computational fluid dynamics (CFD).

---

## Repository Contents

* `quantum_CFD.ipynb`: A Jupyter Notebook containing the complete Python implementation of the hybrid solver, a classical spectral solver for benchmarking, and the analysis code.
* `quantum_cfd_brief.pdf`: The final Algorithm Design Brief in PDF format, detailing the theoretical framework, implementation, and results.
* `README.md`: This file.

---

## About the Algorithm

The solver employs a hybrid **Quantum Tensor Network (QTN) - Hamiltonian Simulation Engine (HSE)** framework.

1.  **Classical Processor (QTN-inspired)**: Encodes the classical fluid velocity field into a quantum state and decodes it back after evolution. It also includes methods for state compression into a Matrix Product State (MPS).
2.  **Quantum Core (HSE)**: The time evolution of the quantum state is performed on a quantum simulator using a Hamiltonian derived from the Burgers' equation.

This approach leverages a quantum backend for the computationally intensive time-evolution step while using a classical computer to manage the simulation loop and state transformations.

---

## How to Run

1.  Ensure you have the required dependencies installed (see below).
2.  Open and run the `quantum_CFD.ipynb` notebook in a Jupyter environment.
3.  The notebook will execute the benchmark comparison between the classical and quantum solvers and generate the analysis plots.

---

## Dependencies

The simulation code requires the following Python libraries:

* `numpy`
* `matplotlib`
* `pennylane`
