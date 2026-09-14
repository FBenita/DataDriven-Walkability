# DataDriven-Walkability

An open-source computational framework for large-scale, micro-spatial walkability assessment. 

Traditional walkability indices often lack the scalability to evaluate urban environments objectively at a micro-level across vast geographic areas. By integrating open geospatial datasets, network analysis, and hexagonal spatial indexing, this repository bypasses the processing bottlenecks associated with traditional metropolitan-scale isochrone mapping.

## Project Roadmap & Capabilities

### Current Release: v1.0 (Southeast Asia Walkability Engine)
The core Python scripts in the `/notebooks` directory power the spatial analysis of highly fragmented, data-scarce urban fabrics. 
* **Capabilities:** Computes 13 multi-scale walkability indicators (Accessibility, Built Environment, Topography, Network) across 400m, 800m, and 1200m spatial boundaries.
* **Deployment:** Executed across Jakarta, Manila, Ho Chi Minh City, and Phnom Penh to evaluate the scale sensitivity of walkability metrics and the Modifiable Areal Unit Problem (MAUP).
* **Reference:** Benita, F. (2026). Scale sensitivity of walkability indicators in Southeast Asian megacities: an open-source computational framework. *Spatial Information Research*, 34(5), 52.

### In Active Development: v2.0 (North America & HPC Scalability)
We are currently scaling this pipeline using High-Performance Computing (HPC) to process massive origin-destination matrices for over 400 metropolitan areas in Mexico and the USA.
* **Innovation:** Replaces manual indicator weighting with unsupervised Machine Learning (PCA and K-Means clustering) to objectively extract and categorize urban morphologies without human bias.
* **Status:** The HPC Python scripts and city datasets are currently under peer review. 
* **Preview:** A fully processed GPKG sample for Monterrey, Mexico, alongside interactive Tableau dashboards for prescriptive livability interventions, is available in this repository.

## Repository Structure
* `/notebooks/` - Jupyter notebooks containing the v1.0 spatial grid generation and isochrone computation engine.
* `/data/` - Links to the published Southeast Asian datasets and the Monterrey v2.0 GPKG sample.
* `/dashboards/` - URLs to interactive Tableau Public visual analytics and the Walkable Southeast Asia web portal.

## Project Impact & Educational Outreach

This repository serves as the computational backbone for several open-source urban mobility initiatives and educational collaborations:

*   **Applied Urban Research:** The codebase generated the spatial metrics (including intersection density, building density, and elevation ranges across 800-meter isochrones on a $250 \times 250$ meter grid) for the 2024 IEEE publication, *Walkable Southeast Asia: A Comparative Study Between Phnom Penh and Ho Chi Minh City*.
*   **Interactive Visualizations:** The raw outputs from these analyses power the public-facing [Walkable Southeast Asia web portal](https://ddum-sutd.github.io/walkable-southeastasia-main), demonstrating the real-world utility of the data.
*   **Youth & Undergraduate Mentorship:** We actively bridge open-source data science with education. The 2024 IEEE study was a direct collaboration with junior college students from Temasek Junior College in Singapore. We continually work with undergraduate researchers to test, refine, and expand these geospatial frameworks.

## Contact & Citation
**Primary Maintainer:** Francisco Benita
**Affiliations:** Tecnológico de Monterrey
