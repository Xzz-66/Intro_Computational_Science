# Assignment 1: Deterministic Epidemic Modeling with SIR and SEIR

This project was completed for the **Introduction to Computational Science** course at the **University of Amsterdam**. It studies infectious-disease dynamics using deterministic compartmental models, starting from the classical SIR model and extending it with vaccination, demography, infection-induced mortality, and seasonal forcing.

The main implementation is contained in:

- `Z_Xia_15984230_assignment1.ipynb`

---

## Overview

The notebook explores epidemic spread through a sequence of increasingly rich compartmental models.

The project begins with the classical **SIR model**,

\[
\frac{dS}{dt} = -\beta S I,\qquad
\frac{dI}{dt} = \beta S I - \gamma I,\qquad
\frac{dR}{dt} = \gamma I,
\]

and then extends it to:

- vaccination scenarios
- SIR with birth and natural death
- SIR with infection-induced mortality
- SEIR dynamics
- SEIR with seasonal forcing

The emphasis is on how changes in model assumptions affect epidemic thresholds, long-term behavior, oscillations, and intervention outcomes.

---

## This notebook includes:

### 1. Basic SIR dynamics and epidemic threshold

The first part numerically solves the SIR system under two parameter regimes:

- one that produces an epidemic
- one that does not

The notebook uses these simulations to illustrate the role of the epidemic threshold through \(R_0 = \beta / \gamma\), and includes **phase-space plots** to visualize the qualitative behavior of the system.

### 2. Parameter estimation from historical influenza data

The notebook fits an SIR model to the historical school influenza outbreak data provided in the assignment. The fitting step estimates model parameters by comparing simulated trajectories to the observed infected counts over time.

This section connects the theoretical SIR model to a concrete real-data example.

### 3. Vaccination strategy comparison

A major part of the notebook compares **four vaccination strategies**:

1. **Pediatric / pre-epidemic vaccination**
2. **Random mass vaccination**
3. **Targeted vaccination without risk grouping**
4. **Targeted vaccination with risk grouping**

These strategies are implemented and compared within the same simulation framework, allowing intervention effects to be studied systematically.

### 4. Demographic SIR model

The notebook then extends the SIR model by adding:

- **birth**
- **natural death**

This produces a demographic SIR model that can sustain endemic behavior. The simulations explore whether oscillations arise in the infected fraction and under what parameter choices.

### 5. Oscillation analysis with Fourier methods

To quantify oscillatory dynamics, the notebook applies **Fourier decomposition / Fourier analysis** to infection trajectories. This helps characterize the frequency structure of the oscillations rather than relying only on visual inspection.

### 6. Infection-induced mortality

A further extension introduces disease-induced mortality into the demographic model. This allows the total population size to vary and makes it possible to study how epidemic behavior changes as the mortality probability increases.

The notebook includes both time-series simulations and phase-space visualization for this case.

### 7. SEIR model

For the model-variant part of the assignment, the notebook implements an **SEIR model**, adding an exposed compartment between susceptible and infected states.

This section analyzes:

- the resulting epidemic dynamics
- phase-space structure
- oscillatory behavior through Fourier analysis

### 8. Seasonal forcing

The final section adds **seasonal forcing** to the SEIR model by using a time-varying transmission rate. This is used to study how stronger or weaker seasonal modulation changes epidemic trajectories and long-term patterns.

---

## Methods

This project uses standard scientific Python tools for numerical simulation and analysis:

- `numpy`
- `matplotlib`
- `scipy.integrate.odeint`
- `scipy.optimize.minimize`
- `scipy.fftpack`
- `pandas`

Main computational steps include:

- numerical ODE integration
- parameter fitting by optimization
- phase-space visualization
- intervention comparison
- Fourier-based oscillation analysis

---

## Notebook structure

The notebook is organized into the following sections:

- **Problem 1:** Numerical integration of the SIR model
  - epidemic vs non-epidemic regimes
  - phase-space plots
  - parameter estimation
  - vaccination strategies

- **Problem 2:** Demography
  - birth and natural death
  - oscillatory behavior
  - phase plots
  - Fourier quantification
  - infection-induced mortality

- **Problem 3:** Variant of the SIR model
  - SEIR model
  - phase plots
  - Fourier decomposition
  - seasonal forcing
  - seasonal phase plots

---

## Key ideas explored

This notebook focuses on several scientific questions:

- What determines whether an outbreak becomes an epidemic?
- How well can a simple SIR model fit outbreak data?
- How much can vaccination reduce outbreak size, and which strategy performs better?
- How do demographic processes change the long-term qualitative dynamics?
- When do oscillations emerge, and how can they be quantified?
- How do latent infection stages and seasonality alter epidemic behavior?

---

## How to run

Open the notebook in Jupyter Notebook or JupyterLab and run the cells in order.

A typical setup is:

```bash
python -m venv .venv
source .venv/bin/activate
pip install numpy matplotlib scipy pandas jupyter
jupyter notebook
