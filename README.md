# Kinematic Synthesis of Aircraft Flap Actuation Mechanism
![MATLAB](https://img.shields.io/badge/MATLAB-R2023b-orange)
![Institution](https://img.shields.io/badge/CSIR--NAL-Internship-blue)
![Domain](https://img.shields.io/badge/Aerospace-Kinematics-red)

## Overview
This repository contains the design and kinematic analysis of a **Fowler Flap Actuation Mechanism** developed during an internship at **CSIR-National Aerospace Laboratories (CSIR-NAL)**. 

The project focuses on the **kinematic synthesis** of a four-bar linkage system to achieve a specific aerodynamic deployment path, maximizing lift during takeoff and landing while minimizing mechanical complexity.

<h2 align="center">Mechanism Analysis & Simulation</h2>

<p align="center">
  <img src="assets/simulation.gif" width="600" title="4-Bar Mechanism Animation">
  <br>
  <em>Figure 1: Kinematic simulation of the flap deployment (0° to 40°)</em>
</p>

<div align="center">
  <table>
    <tr>
      <td align="center">
        <img src="assets/stick_model.png" width="400" alt="Vector Loop Model">
        <br>
        <strong>Derivation Model (Vector Loop)</strong>
      </td>
      <td align="center">
        <img src="assets/validation_plot.png" width="400" alt="Transmission Angle">
        <br>
        <strong>Validation (Transmission Angle)</strong>
      </td>
    </tr>
  </table>
</div>

## Key Objectives
* **Analytical Synthesis:** Designed a 4-bar linkage mechanism using **Freudenstein’s Equation** and three-position synthesis techniques.
* **Path Generation:** Optimized the coupler curve to match the desired flap deployment trajectory (0° to 40° deflection).
* **Mechanical Advantage:** Analyzed the transmission angles to ensure smooth operation without locking (singularity analysis).

## Methodology
The mechanism was designed using a **Three-Position Analytical Synthesis** approach:
1.  **Input:** Defined three critical positions of the flap (Stowed, Take-off, Landing).
2.  **Synthesis:** Solved the loop-closure equations using MATLAB to determine link lengths ($L_1, L_2, L_3, L_4$).
3.  **Validation:** Verified the transmission angles $\mu$ remained within the safe range ($40^\circ < \mu < 140^\circ$) throughout the entire range of motion.

## Repository Structure
```text
aircraft-flap-mechanism-synthesis/
│
├── src/                        # MATLAB source code
│   ├── MAIN_FlapSynthesis.m    # Main execution script
│   ├── freudenstein_solver.m   # Function for analytical synthesis
│   └── animate_mechanism.m     # Visualization and plotting logic
│
├── docs/                       # Project documentation
│   ├── Final_Project_Report.pdf
│   └── Mathematical_Formulation.pdf
│
├── assets/                     # Images and animations for the README
│   ├── simulation.gif
│   ├── stick_model.png
│   └── validation_plot.png
│
├── LICENSE                     # MIT License
└── README.md                   # Project overview and instructions
