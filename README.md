<div align="center">
  <h1>bus-scheduling-optimization 🚌🔋</h1>
  <p><b>A Mixed-Integer Linear Programming (MILP) approach to minimizing fleet size and managing charging constraints.</b></p>
  
  <p>
    <img src="https://img.shields.io/badge/Julia-9558B2?style=for-the-badge&logo=julia&logoColor=white" alt="Julia">
    <img src="https://img.shields.io/badge/Gurobi-darkgreen?style=for-the-badge" alt="Gurobi">
    <img src="https://img.shields.io/badge/JuMP-blue?style=for-the-badge" alt="JuMP">
  </p>
</div>

<hr />

## 📌 Overview
This repository contains a Julia implementation for the **Electric Bus Scheduling Problem**. Using the **JuMP** modeling language and **Gurobi** (or Cbc) solvers, the script optimizes bus assignments to minimize the total number of vehicles required while ensuring every trip is covered and charging requirements are met.



## 🚀 Key Features
* **Fleet Minimization:** Optimizes the objective function to find the smallest number of buses needed.
* **Temporal Constraints:** Ensures sequential trip feasibility (a bus cannot be in two places at once).
* **Charging Integration:** Includes parameters for energy supply rates and battery SoC (State of Charge) thresholds.
* **Flexible Solver Support:** Compatible with commercial solvers (Gurobi) and open-source solvers (Cbc).

## 🛠 Prerequisites
Ensure you have [Julia](https://julialang.org/) installed, then install the required packages:
## Paper
https://www.sciencedirect.com/science/article/abs/pii/S0360544221010549
## Abstract
Highlights
•
We developed a MILP model for dynamic wireless charging planning.
•
We simultaneously optimize EB fleet size and DWC infrastructure planning.
•
We optimize EB fleet size, battery capacity, transmitter locations, inverters, and cables.
•
We conduct a sensitivity analysis to understand the system behavior.
•
Lifetime cost was build using fleet size, battery cost, cable cost, and bus purchase cost.

```julia
using Pkg
Pkg.add(["JuMP", "Gurobi", "DataFrames", "CSV"])
