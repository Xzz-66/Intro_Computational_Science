# Assignment 1: Deterministic Epidemic Models

This project studies epidemic dynamics using deterministic compartmental models for the course **Introduction to Computational Science**.

## Overview

The notebook starts with the classical **SIR model** and then extends it to more complex settings.

Topics covered include:

- basic SIR simulation
- epidemic threshold and phase-space plots
- fitting the model to influenza outbreak data
- comparison of vaccination strategies
- SIR with birth and death
- infection-induced mortality
- SEIR model
- seasonal forcing

## Methods

Main methods used in this notebook:

- numerical ODE solving
- parameter fitting
- phase-space analysis
- Fourier analysis
- simulation comparison across parameter settings

## Tools

The project mainly uses:

- `numpy`
- `scipy`
- `matplotlib`
- `pandas`

## How to run

Open the notebook in Jupyter and run all cells:

```bash
pip install numpy scipy matplotlib pandas jupyter
jupyter notebook
