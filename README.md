# Convection-Diffusion Case Study using Custom OpenFOAM Solver Implementation

## Project Overview

This project implements a custom scalarFoam solver in OpenFOAM to analyze convection-diffusion phenomena in a 1D shocktube case. The solver is designed to evaluate 
the impact of different numerical discretization schemes on temperature transport and diffusion behavior.

## Features

✔ Custom implementation of scalarFoam solver for passive scalar transport.

✔️ Supports 6 numerical schemes (Upwind, Linear Upwind, Quadratic, Cubic, vanLeer, QUICK).

✔️ Simulates temperature diffusion and convection in a 1D shocktube case.

✔️ Configurable boundary conditions and transport properties.

✔️ Post-processing support using ParaView for result visualization.

## Setup & Compilation

```bash
# Clone the repository
git clone https://github.com/yourusername/OpenFOAM-scalarFoam.git
cd OpenFOAM-scalarFoam/solver

# Compile the solver
wmake
```

## Running the Simulation

```bash
cd ../case
blockMesh       # Generate mesh
checkMesh       # Validate mesh
setFields       # Initialize temperature field
scalarFoam      # Run the solver
```

## Post-Processing Results

```bash
paraFoam
```

## Results & Observations

- Diffusion Study: Simulated different diffusion coefficients (DT = 0, 0.0001, 0.01, 1) and analyzed temperature spread.
- Convection Study: Compared 6 numerical schemes for convection-dominated cases.
- Key Findings: Higher-order schemes improved accuracy but introduced oscillations; lower-order schemes added numerical diffusion.