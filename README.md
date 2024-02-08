# Comparative Analysis of K-Means and DBSCAN on Synthetic Datasets

## Overview
This repository presents a thorough comparison between two fundamental clustering algorithms: K-Means and DBSCAN. Implemented from scratch, these algorithms are evaluated across four synthetic datasets designed to simulate various real-world data conditions, from simple blobs to complex cyclic patterns.

## Datasets
- **Dataset1 (Blobs)**: Simulates normal, minor, and major fault conditions in equipment.
- **Dataset2 (Anisotropic)**: Represents different operating conditions through anisotropically distributed data.
- **Dataset3 (Noisy Moons)**: Mimics cyclic patterns in equipment behavior with noise.
- **Dataset4 (Noisy Circles)**: Depicts complex cyclic patterns in larger equipment with noise.

## Algorithms
- **K-Means**: A centroid-based algorithm known for its simplicity and efficiency in clustering spherical data groups.
- **DBSCAN**: A density-based algorithm that excels in identifying clusters of arbitrary shapes and sizes, robust against noise.

## Methodology
The analysis involves generating the datasets, applying both algorithms, and evaluating their performance using metrics such as F-measure, Normalized Mutual Information (NMI), and Rand Statistic.

## Results
### Dataset1 - Blobs
- **K-Means** showed excellent performance with high scores across all metrics (F-measure: 0.343, NMI: 0.959, Rand Statistic: 0.970), indicating its effectiveness in handling well-separated, spherical clusters.
- **DBSCAN** struggled with this dataset, as reflected in its lower scores (F-measure: 0.007, NMI: 0.864, Rand Statistic: 0.905), likely due to its sensitivity to density variations in such uniform distributions.

### Dataset2 - Anisotropic
- Both algorithms faced challenges with the anisotropic dataset. **K-Means** (F-measure: 0.114, NMI: 0.429, Rand Statistic: 0.447) had difficulty due to its assumption of isotropic clusters.
- **DBSCAN** performed slightly better (F-measure: 0.011, NMI: 0.614, Rand Statistic: 0.496), showing some resilience to the dataset's stretched clusters.

### Dataset3 - Noisy Moons
- **K-Means**'s performance dropped (F-measure: 0.260, NMI: 0.173, Rand Statistic: 0.228) due to the non-linear separation of the clusters.
- **DBSCAN** excelled in this scenario (F-measure: 0.992, NMI: 0.934, Rand Statistic: 0.967), demonstrating its strength in clustering non-linearly separable data.

### Dataset4 - Noisy Circles
- **K-Means** failed to identify the intricate structure of the clusters (F-measure: 0.493, NMI: 0.000, Rand Statistic: -0.003).
- **DBSCAN** achieved perfect scores (F-measure: 1.000, NMI: 1.000, Rand Statistic: 1.000), showcasing its exceptional ability to handle complex patterns and noise.

## Conclusion
The comparative analysis underscores the importance of choosing the right clustering algorithm based on the dataset's characteristics. K-Means is suitable for simple, well-separated clusters, while DBSCAN is more adaptable to complex shapes and noise. This study highlights the trade-offs between simplicity and flexibility in clustering algorithms.

## Getting Started
To run the project:
1. Ensure Python is installed along with the libraries: NumPy, Matplotlib, Scikit-learn, and Seaborn.
2. Clone this repository.
3. Run the Jupyter Notebook `ML-Edited5.ipynb` to replicate the analysis.
