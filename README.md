# Quantum Adiabatic Computing – Practice 1

## QUBO Optimization with Constraints

This project implements the first practice of Adiabatic Quantum Computing, focused on solving constrained combinatorial optimization problems using QUBO models (Quadratic Unconstrained Binary Optimization). The implementation uses Python and the D-Wave Ocean SDK to build and solve QUBO models through simulated annealing and exhaustive search.

## Overview

The goal is to solve a constrained Max-Cut problem on a weighted graph. The QUBO formulation includes the following elements:

* Weighted Max-Cut objective
* Balance constraint to ensure similar partition sizes
* Must-Link constraints for nodes required to be in the same partition
* Cannot-Link constraints for nodes required to be in different partitions

The project generates random graphs, constructs the corresponding QUBO, solves it, and visualizes the resulting partitions.

## Features

* Random weighted graph generation
* Automatic creation of Must-Link and Cannot-Link constraints
* QUBO construction using objective and penalty terms
* Two solving strategies:

  * Exhaustive brute-force search
  * SimulatedAnnealingSampler from the D-Wave Ocean SDK
* Graph visualization before and after optimization
* Reporting of metrics such as:

  * Minimum energy
  * Cut weight
  * Partition sizes
  * Constraint violations

## Requirements

* Python 3.8 or higher
* D-Wave Ocean SDK
* NumPy
* NetworkX
* Matplotlib

## How to Run

Open the Jupyter notebook and execute all cells:

```bash
jupyter notebook Practica1Adiabatica.ipynb
```

## Learning Goals

* Understand QUBO formulation for combinatorial optimization
* Explore the impact of penalty parameters A, B, and C
* Compare heuristic (simulated annealing) and exact (brute-force) solvers
* Analyze performance and scalability as the graph size increases
