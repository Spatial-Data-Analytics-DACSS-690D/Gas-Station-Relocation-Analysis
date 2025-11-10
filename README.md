# Gas-Station-Relocation-Analysis

### Objective
Identify and suggest relocation for all gas stations located within 200 meters of any school in Boston using geospatial analysis and visualization.

### Overview
This project analyzes the spatial proximity between schools and fuel stations across Boston to assess potential safety and zoning conflicts.
Using geospatial data (GeoPackage layers) and R (ggplot2 + sf), the study identifies gas stations that are too close to educational institutions and visualizes suitable relocation zones.

The project is visualized through an interactive Flexdashboard, integrating multiple geospatial layers and statistical insights.

### Key Steps in the Analysis

#### Data Import:

Imported multiple .gpkg layers such as boston, schoolBoston, fuelBoston, secured_schoolBoston, gas_relocate, suitable_roads, etc.

#### Spatial Joins & Buffering:

Created 200-meter buffers around all school locations.

Identified all fuel stations within these buffer zones using spatial intersection (st_intersects).

#### Relocation Identification:

Filtered out fuel stations violating proximity rules.

Suggested new potential locations based on secured and suitable road networks.

#### Visualization:

Built multiple ggplot2 visualizations integrated into a Flexdashboard.

Each plot highlights different spatial relationships and insights.

| Plot       | Title                                     | Description                                                                 |
| ---------- | ----------------------------------------- | --------------------------------------------------------------------------- |
| **Plot 1** | *Distribution of Fuel Stations in Boston* | Displays all existing fuel stations across the city.                        |
| **Plot 2** | *Distribution of Schools in Boston*       | Visualizes the location of all schools to identify dense educational areas. |
| **Plot 3** | *Fuel Stations Within 200m of Schools*    | Highlights stations located within restricted proximity zones.              |
| **Plot 4** | *Regional Distribution of Fuel Stations*  | Bar chart summarizing station counts across regions/districts.              |


### Tools & Libraries Used

R Libraries:

sf – spatial data handling

ggplot2 – visualization

dplyr – data manipulation

tmap / leaflet (optional for comparison)

flexdashboard – interactive dashboard creation

GIS Data Format: GeoPackage (.gpkg)

### Links
[Dashboard] (https://spatial-data-analytics-dacss-690d.github.io/Gas-Station-Relocation-Analysis/)
[Repo] (https://github.com/Spatial-Data-Analytics-DACSS-690D/Gas-Station-Relocation-Analysis/)
