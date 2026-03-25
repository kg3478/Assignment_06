# Data Generation using Cantera for Machine Learning

## Objective

The aim of this assignment is to generate synthetic data using a simulation-based approach and then apply different machine learning models to analyze the generated data.

---

## Overview

In this project, I have used the Cantera library to simulate a simple combustion process. By changing initial conditions such as temperature, pressure, and fuel-air ratio, multiple simulation runs were performed to generate a dataset. This dataset was then used to train and compare different machine learning models.

---

## Methodology

### 1. Simulation Setup

* The Cantera library was used with the `gri30.yaml` mechanism.
* A reactor model was created using `IdealGasReactor`.
* Initial conditions were randomly generated for each simulation:

  * Temperature: 900 K to 1800 K
  * Pressure: 1 atm to 5 atm
  * Equivalence ratio (phi): 0.5 to 1.5

### 2. Data Generation

* A total of around 1000 simulation runs were performed.
* For each run, the reactor was allowed to evolve over time.
* The final temperature after simulation was recorded.
* Based on the final temperature, the outcome was defined:

  * Stable combustion (1) → if temperature > 1400 K
  * Unstable combustion (0) → otherwise

### 3. Dataset Features

The generated dataset contains the following features:

* Initial Temperature
* Pressure
* Equivalence Ratio (phi)
* Final Temperature
* Output (Stable / Unstable)

---


## Results

The performance of each model was evaluated using accuracy. A comparison table and a bar graph were generated to visualize the results.

In most cases, Random Forest performed better compared to other models, likely due to its ability to handle non-linear relationships in the data.

<img width="263" height="133" alt="Screenshot 2026-03-25 at 12 08 29 PM" src="https://github.com/user-attachments/assets/75890509-2f8e-433c-8c19-b88ae73c1c9e" />

<img width="598" height="475" alt="Screenshot 2026-03-25 at 12 08 14 PM" src="https://github.com/user-attachments/assets/5a73e5a7-f9f9-4df0-9057-5b6c60bda272" />

---

