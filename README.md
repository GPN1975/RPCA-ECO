# **RPCA-Eco: Regularized PCA for Ecological Data with Missing Values**  
*Version 0.1.0*  

---

## **Table of Contents**  
1. [Installation](#installation)  
2. [Overview](#overview)  
3. [Function Reference](#functions)  
   - `generate_data()`  
   - `introduce_missing()`  
   - `rpca_eco()`  
   - `plot_reconstruction_error()`  
4. [Tutorial](#tutorial)  
5. [Simulation Study](#simulation)  
6. [References](#references)  

---

## **1. Installation** <a name="installation"></a>  
Install the development version from GitHub:  
```r
if (!require("devtools")) install.packages("devtools")
devtools::install_github("ecostats/RPCA-Eco")
```

---

## **2. Overview** <a name="overview"></a>  
**RPCA-Eco** is an R package designed to recover low-rank structure from ecological datasets that may contain missing values and sparse noise (outliers). It implements:

- Regularized Principal Component Analysis (RPCA) using nuclear norm (for low-rank component) and L1 norm (for sparse component) penalties.
- An Alternating Direction Method of Multipliers (ADMM) algorithm for efficient optimization.
- Tools for simulating ecological data and evaluating recovery performance.

**Use Cases:**  
- Impute missing species abundance or environmental sensor data.
- Decompose ecological matrices into interpretable low-rank (e.g., latent environmental gradients) and sparse (e.g., outliers) components.
