# PINN Simulation: 2D Heat Transfer in Food Engineering

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Peter-X-Zhou/PINNs-Heat-Transfer/blob/main/PINNs_2D_Heat%20transfer_Nov%2023%2C%202025.ipynb)

This repository contains the source code and simulation files for Chapter [Digital Twins and Physics-Informed Neural Networks in Food Processing] of the book [AI for Food Science]

It implements a Physics-Informed Neural Network (PINN) to model transient heat transfer in a 2D food product during heating

## 📂 Project Overview

The goal of this simulation is to solve the **2D Heat Diffusion Equation** without using traditional mesh-based methods (like Finite Element Method). Instead, we use a neural network to approximate the temperature distribution T(x,y,t) by minimizing a loss function derived from the governing physical laws.

### The Physics Model
* **Governing Equation:** 2D Transient Heat Equation
* **Domain:** 10 cm * 10 cm cross-section.
* **Thermal properties: k   = 0.45        # thermal conductivity [W / (m·K)]
                        rho = 1050.0      # density [kg / m^3]
                        cp  = 3300.0      # specific heat [J / (kg·K)]
* **Initial Condition (IC):** Uniform temperature of 25C at t=0.
* **Boundary Conditions (BC):** 180C (Oven temperature) on all edges.

## 🚀 How to Run the Code

### Option 1: Google Colab (Recommended)
You can run the simulation immediately in your browser without installing anything. Click the "Open in Colab" badge at the top of this page.

### Option 2: Local Installation
If you prefer to run this locally, ensure you have Python installed.

1.  Clone this repository:
    ```bash
    git clone [https://github.com/Peter-X-Zhou/PINNs-Heat-Transfer.git](https://github.com/Peter-X-Zhou/PINNs-Heat-Transfer.git)
    cd PINNs-Heat-Transfer
    ```

2.  Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```

3.  Launch Jupyter:
    ```bash
    jupyter notebook
    ```

## 📊 Results

The PINN successfully reconstructs the temperature profile over 60 minutes of heating. The code produces:
* **Loss Convergence Plots:** Demonstrating the minimization of PDE, IC, and BC residuals.
* **Temperature Heatmaps:** Visualizing thermal penetration from the edges to the center.
* **Center Point History:** A time-temperature profile of the geometric center (the "coldest point").


---
*Author: [Xu Zhou]*
*Contact: [pxzhou@ucdavis.edu]*
