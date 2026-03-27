# Assignment 2: Stochastic and Network Epidemic Models

This project studies epidemic spread using stochastic simulation and network-based models for the course **Introduction to Computational Science**.

## Overview

This notebook has two main parts:

1. **Stochastic SIR simulation** with Gillespie's algorithm  
2. **Epidemic spreading on networks**

Topics covered include:

- Gillespie simulation of SIR dynamics
- comparison between stochastic and deterministic models
- extinction and critical community size
- epidemic spread on ER, WS, and BA networks
- network statistics and comparison
- vaccination strategy on a Sociopatterns contact network

## Methods

Main methods used in this notebook:

- Gillespie algorithm
- repeated stochastic simulation
- deterministic comparison
- network generation with `networkx`
- SIR simulation with `ndlib`

## Tools

The project mainly uses:

- `numpy`
- `scipy`
- `matplotlib`
- `pandas`
- `networkx`
- `ndlib`

## How to run

Open the notebook in Jupyter and run all cells:

```bash
pip install numpy scipy matplotlib pandas networkx ndlib jupyter
jupyter notebook
