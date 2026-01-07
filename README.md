# Battery-Size-Optimization-for-Battery-Electric-Buses-in-urban-Public-Transport
This repository presents a reproducible framework for optimal battery sizing of battery electric buses. The framework integrates route-level profiling, clustering, and optimization using real-world urban public transport data. The provided code supports reproduction and independent verification of the main results reported in the study.
Datasets

## 1. Datasets

This repository provides two datasets used to support the methodology and reproduce the results of the study:

1. **`Clustering-Dataset.xlsx`**  
   This dataset contains integrated route-level integrated profiles for all routes in the study. It is used to apply various clustering techniques to group routes with similar operational characteristics.

2. **`Kmeans-Clustered-Dataset.xlsx`**  
   This dataset contains the route clusters obtained by applying the K-Means clustering technique to the `Clustering-Dataset.xlsx`. These clusters are subsequently used for battery sizing optimization and validation steps.
## 2. Code Implementation

The computational framework is implemented in Python and is organized into
clustering and optimization modules.

### 2.1 Clustering Techniques

The following Python scripts implement different clustering techniques to group
routes based on similarities in their integrated route-level profiles:

- **`Agglomerative-Clustering.py`** – Hierarchical agglomerative clustering  
- **`DBSCAN-Clustering.py`** – Density-based spatial clustering of applications with noise (DBSCAN)  
- **`GMM-Clustering.py`** – Gaussian Mixture Model (GMM)–based clustering  
- **`K-Means-Clustering.py`** – K-Means clustering used to generate the route clusters reported in the study  
- **`Spectral-Clustering.py`** – Spectral clustering based on graph partitioning  

### 2.2 Battery Size Optimization

Battery size optimization is performed using the following Python scripts:

- **`Battery-Size-Optimization-LP-100-150-Power-levels.py`**  
  Implements a linear programming (LP)–based optimization model to determine the
  optimal battery size under specified charging power levels.

- **`Battery-Size-Optimization-SP-100-150-Power-levels.py`**  
  Implements a stochastic programming (SP)–based optimization model to account for
  uncertainty in operational conditions while optimizing battery size.


