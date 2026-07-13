
# Time-Domain Analysis of a Second-Order Control System

An educational tutorial featuring analytical mathematical derivations coupled with practical verification scripts using **MATLAB (Live Script)** and **Python (Control Systems Library)**. This repository is designed to accompany the video tutorial on second-order system transient specifications.

---

##  Project Overview

This project provides a comprehensive walkthrough for analyzing the time-domain performance of a prototype second-order control system. By comparing theoretical calculation steps side-by-side with industry-standard software simulations, students and engineers can bridge the gap between control theory and modern implementation.

### Objectives
* Extract core system architecture parameters ($\omega_n$, $\zeta$, $\omega_d$).
* Formulate exact closed-form analytical solutions for a unit-step input response.
* Compute performance metrics: Rise Time ($t_r$), Peak Time ($t_p$), Maximum Overshoot ($M_p$), and Settling Time ($t_s$).
* Verify analytical benchmarks via executable scripts.

---

## The Tutorial Problem

Given the following closed-loop transfer function:

$$T(s) = \frac{C(s)}{R(s)} = \frac{25}{s^2 + 6s + 25}$$

For a unit-step input $R(s) = \frac{1}{s}$, the analytical derivation yields:

### 📐 Verification Baseline Metrics

| Performance Metric | Mathematical Symbol | Analytical Value |
| :--- | :---: | :---: |
| **Natural Frequency** | $\omega_n$ | $5.000 \text{ rad/s}$ |
| **Damping Ratio** | $\zeta$ | $0.600$ (Underdamped) |
| **Damped Frequency** | $\omega_d$ | $4.000 \text{ rad/s}$ |
| **Rise Time** | $t_r$ | $0.554 \text{ s}$ |
| **Peak Time** | $t_p$ | $0.785 \text{ s}$ |
| **Maximum Overshoot** | $M_p$ | $9.48\%$ |
| **Settling Time (2%)** | $t_s$ | $1.333 \text{ s}$ |

The resulting definitive time-domain expression is:
$$c(t) = 1 - 1.25e^{-3t} \sin(4t + 0.927)$$

---

## Code Implementations

This repository contains two production-grade verification alternatives:

### 1. MATLAB Live Script (`ControlSimulations_matlab.mlx`)
Optimized for MATLAB's interactive Live Editor environments. It leverages `stepinfo` to automatically parse and render step response dynamics.

* **Key Features:** Section breaks for quick debugging, native high-resolution plot adjustments, and real-time command window printouts.
* **Requirements:** Control System Toolbox.

### 2. Python Script (`controlSImulation_python.ipynb`)
A standalone notebook replicating identical behavior using open-source packages.

* **Key Features:** Utilizes the robust `control` library paired with custom `matplotlib` parameters for clean video visibility.
* **Prerequisites:**
  ```bash
  pip install numpy matplotlib control

```

---

## How to Run the Scripts

### MATLAB

1. Open MATLAB.
2. Clone or download this repository and navigate to the directory.
3. Open `verification.mlx` and click **Run** ($F5$) inside the Live Editor tab.

### Python

1. Ensure your virtual environment satisfies the dependencies listed above.
2. Run the file from your terminal:
3. Install jupyter lab or notebook 
```bash

jupyter lab

```
Run jupyter lab from the same directory as the simulation notebook



---

## Video Tutorial Application

If you are using this material to follow along with the video instruction:

1. **Pause at Section 1** to manually solve for system poles and parameters.
2. **Review Section 2** to confirm your phase angle calculations in radians (ensure your calculator is not in degree mode).
3. **Execute the Code** to see the theoretical data points overlap perfectly with the generated step response plots!

---

##  License

This project is open-source and available under the [MIT License](https://www.google.com/search?q=LICENSE). Feel free to adapt this problem and code structure for your own classrooms or presentations.

```

```
