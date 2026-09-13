# DataDriven-Walkability

An open-source computational framework for large-scale, micro-spatial walkability assessment. 

Traditional walkability indices frequently lack the computational scalability to objectively evaluate environments at a micro-scale across massive geographic extents. By integrating open geospatial datasets, network analysis, and hexagonal spatial indexing, this repository bypasses the severe computational bottlenecks associated with traditional isochrone mapping at a metropolitan scale.

## Project Roadmap & Capabilities

### Current Release: v1.0 (Southeast Asia Walkability Engine)
The core Python scripts provided in the `/notebooks` directory power the spatial analysis of highly fragmented, data-scarce urban fabrics. 
* **Capabilities:** Computes 13 multi-scale walkability indicators (Accessibility, Built Environment, Topography, Network) across 400m, 800m, and 1200m spatial boundaries.
* **Deployment:** Successfully executed across Jakarta, Manila, Ho Chi Minh City, and Phnom Penh to evaluate the scale sensitivity of walkability metrics and the Modifiable Areal Unit Problem (MAUP).
* **Reference:** Benita, F. (2026). Scale sensitivity of walkability indicators in Southeast Asian megacities: an open-source computational framework. *Spatial Information Research*, 34(5), 52.

### In Active Development: v2.0 (North America & HPC Scalability)
We are currently scaling this pipeline using High-Performance Computing (HPC) vito process massive origin-destination matrices for 400+ metropolitan areas in Mexico and the USA.
* **Innovation:** Replaces manual indicator weighting with unsupervised Machine Learning (PCA and K-Means clustering) to objectively extract and categorize urban morphologies without human bias.
* **Status:** The HPC Python scripts and  city datasets are currently under peer review. 
* **Preview:** A fully processed GPKG sample for Monterrey, Mexico, alongside interactive Tableau dashboards for prescriptive livability interventions, is available in this repository.

## Repository Structure
* `/notebooks/` - Jupyter notebooks containing the v1.0 spatial grid generation and isochrone computation engine.
* `/data/` - Links to the published Southeast Asian datasets and the Monterrey v2.0 GPKG sample.
* `/dashboards/` - URLs to interactive Tableau Public visual analytics and the Walkable Southeast Asia web portal.

## Contact & Citation
**Primary Maintainer:** Francisco Benita
**Affiliation:** Tecnológico de Monterrey 
