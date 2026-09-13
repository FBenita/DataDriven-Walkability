# Walkability and Urban Mobility Analysis Notebooks

This directory contains the Jupyter Notebooks used to process city boundaries, extract urban amenities, generate hexagonal grids, and compute spatial walkability indicators for Southeast Asian cities (Jakarta, Manila, Ho Chi Minh City, and Phnom Penh). These notebooks process the raw geospatial data and produce the final `.gpkg` files shared via Zenodo.

## Notebooks Overview

### 1. OpenStreetMaps - Food & Urban Amenities Extraction
*   **Purpose**: Downloads city boundary GeoPackage files and extracts Point of Interest (POI) amenities.
*   **Process**: Uses `osmnx` to query and extract point geometries categorized into food, healthcare, education, and leisure.
*   **Output**: Saves the extracted amenities as city-specific `.gpkg` files (e.g., `Jakarta_food_amenities.gpkg`).

### 2. Generate Hexagonal Grids and Urban Indicators
*   **Grid Generation**: Reprojects city boundaries to a local UTM coordinate reference system (CRS) and generates hexagonal grids at 400m, 800m, and 1200m radii.
*   **Filtering**: Cleans the grid by verifying proximity to the pedestrian network (within 500 meters) and the presence of population.
*   **Indicator Computation**: Calculates four primary categories of urban indicators for each hexagonal cell:
    *   **Accessibility**: POI density (food, education, healthcare, leisure) and Shannon Diversity Index.
    *   **Built Environment**: Built-up ratio (derived from building footprints) and population density per square kilometer.
    *   **Topography**: Mean elevation and elevation range.
    *   **Network Structure**: Network length density, intersection density, cul-de-sac ratio, and average link length.
*   **Visualization**: Generates mapped figures of the computed indicators across the different radii using `matplotlib` and `matplotlib-scalebar`.

## Data Sources
The notebooks fetch input data via URLs, which include city boundaries, pedestrian networks, population counts, building footprints, and elevation data. If running locally or updating for the Zenodo release, ensure the URLs in the data dictionaries point to the official Zenodo repository links.

## Dependencies
To execute these notebooks, the following Python libraries are required:
*   `geopandas`
*   `osmnx`
*   `networkx`
*   `shapely`
*   `rtree`
*   `matplotlib`
*   `matplotlib-scalebar`
*   `mapclassify`
*   `pyogc` / `pyogrio`

## Execution Instructions
1. Install the required dependencies in your local environment or Google Colab.
2. Run the OSM Amenities notebook first to generate the necessary POI datasets for each city.
3. Run the Hexagonal Grids and Indicators notebook. Ensure the target output directory (`city_hex_grids/`) is writable, as it will store the final grid geometries and computed metrics.
