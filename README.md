# Physics-Informed Neural Network (PINN) for Nonlinear Reaction-Diffusion BVPs

This repository contains the results of my Math Research at Weber State University. The implementation of a Physics-Informed Neural Network (PINN) designed to solve nonlinear steady-state reaction-diffusion boundary value problems (BVPs). The network respects analytically derived **sub- and super-solutions** to ensure physically valid solutions and employs a custom Cosine activation function to capture higher-order derivatives accurately.

---

## Features

- **Bounded PINN Output:** Network outputs are constrained using **sub- and super-solutions** for physical validity.
- **Custom Cosine Activation:** Smooth, periodic activation function improves convergence and derivative approximation.
- **Flexible Architecture:** Supports multiple hidden layer configurations for exploring depth/width effects.
- **CPU and GPU Support:** Environment files for both CPU-only and NVIDIA GPU setups.
- **Benchmarking:** Solutions can be compared against high-precision quadrature methods.

---

## Optimization Notebook

A short Jupyter notebook, `Optimization.ipynb`, is included to provide a brief overview of the experiments and architecture selection process.  

### Features:

- Demonstrates how different network depths and widths were tested.
- Shows the impact of custom Cosine activation and sigmoid output scaling on convergence.
- Summarizes average errors and training times for various architectures.
- Provides visualizations of training loss and solution benchmarking for selected parameter sets.

This notebook is intended for quick experimentation and to guide users in selecting architectures for their own PINN experiments.


---

## Requirements

### Using Conda

Two environment files are provided:  

- `environment-cpu.yml` – for CPU-only usage  
- `environment-gpu.yml` – for NVIDIA GPU usage  

### Setup Instructions

1. **Clone the repository:**

```bash
git clone https://github.com/yourusername/pinn-reaction-diffusion.git
cd pinn-reaction-diffusion
