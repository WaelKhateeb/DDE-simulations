# DDE Simulations

This repository contains MATLAB code for the symbolic setup and bifurcation analysis of delay differential equation models using DDE-Biftool.

## Congestion-control DDE model

The current project studies a two-variable delayed congestion-control model with state variables `w` and `q`, delayed variables `wtau` and `qtau`, and parameters `k`, `tau`, and `delay`.

The workflow is:

1. Define the delayed system symbolically.
2. Generate the DDE-Biftool-compatible model function.
3. Initialize and correct a steady state.
4. Compute stability eigenvalues.
5. Continue the steady-state branch with respect to the delay parameter.
6. Detect Hopf bifurcation points.
7. Branch from Hopf points into periodic orbits.
8. Compute Floquet multiplier magnitudes along the periodic-orbit branch.

## Files

- `congestion-control-ddebiftool/Function_def6.m`: Symbolic definition of the delayed model and automatic generation of the DDE-Biftool function file.
- `congestion-control-ddebiftool/Main_code6.m`: Main continuation and bifurcation-analysis script.
- `sym_congestionControlModel.m`: Generated locally by running `Function_def6.m` in MATLAB with DDE-Biftool symbolic tools.

## Requirements

- MATLAB
- Symbolic Math Toolbox
- DDE-Biftool

## Reproducibility notes

The generated file `sym_congestionControlModel.m` is intentionally not stored as a primary source file. It should be regenerated from `Function_def6.m` so that the repository contains only the project-specific model definition and analysis script. To reproduce the workflow, run `Function_def6.m` first, then run `Main_code6.m`.

## References and attribution

This repository uses DDE-Biftool for numerical bifurcation analysis of delay differential equations. Please cite the DDE-Biftool project and manual when using or adapting this code:

- K. Engelborghs, T. Luzyanina, and D. Roose, ``Numerical bifurcation analysis of delay differential equations using DDE-BIFTOOL,'' ACM Transactions on Mathematical Software, 28(1), 1--21, 2002.
- J. Sieber, K. Engelborghs, T. Luzyanina, G. Samaey, and D. Roose, ``DDE-BIFTOOL Manual: Bifurcation analysis of delay differential equations,'' arXiv:1406.7144, 2014.

The MATLAB scripts in this repository are project-specific code written for the congestion-control delay model. DDE-Biftool itself is not included in this repository and should be downloaded from its official source.
