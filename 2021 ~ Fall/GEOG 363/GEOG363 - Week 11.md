# GEOG363 - Week 11: Visibility & Decision Analysis
- Outline:
    - Visibility and intervisibility (viewshed)
    - DEM analysis: exercise
    - Raster/vector: synthesis

# DEM as a Statistical Surface
- Elevation can be available in both:
    - Vector
    - Raster

- Elevation information can be interpolated to calculate different forms of surfaces
    - Steepness of slopes
    - Azimuth or orientation (aspect)
    - Visibility and intervisibility

# Visibility and Intervisiblity (Viewshed)
- **Viewshed** = refers to the portion of land that is visible from one or more viewpoints
    - Viewshed analysis: defining the regions that are visible from a particular point based on the terrain

## Viewshed Analysis
- A viewshed analysis requires two input datasets:
    - A point layer (viewpoint or viewpoints)
    - An elevation layer
        - The elevation layer can be in raster (DEM) or vector (TIN)

- **Line-of-sight/sight-line operation algorithm** (basis for viewshed analysis):
    1. Connects the viewpoint to the target point
    2. Interpolates the elevation of the intermediate cells
    3. Determines if the target is visible or not based on the elevation of the intermediate cells (is there a high elevation cell between two low elevation cells blocking the sight-line?)
    4. Expands this operation to every possible cell to determine which ones are visible or invisible to the view point

## Viewshed Applications
- Application of viewshed analysis include:
    - Site selection of facilities (e.g. wireless telephone based station)
    - Housing and resort area development (e.g. visual intrusion of new facilities)
    - Resource management (e.g. reducing the visual impact of clear-cuts)
    - Maximizing visibility of billboards & other advertising
    - Designing scenic paths with the best views
    - Reducing detection of troops (military)
    - Maximizing crowd surveillance (event security)