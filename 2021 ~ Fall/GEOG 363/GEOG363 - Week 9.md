# GEOG363 - Week 9: Raster Analysis I-III
- Outline:
    - **Raster analysis I**
        - Measuring cells 
        - Measuring distances
        - Cost distance
        - Convert Raster to Vector, Vector to Raster
    - **Raster analysis II**
        - Raster selection & reclassification
        - Raster overlay
        - Raster mask
    - **Raster analysis III**
        - Operators and functions
            - Local functions
            - Focal functions
            - Zonal functions
            - Global functions; proximity functions
            - Application functions
            - Cartographic model

# Measuring Cells
- Calculating **perimeter**
    - Perimeter is estimated more than calculated
    - **Perimeter** = number of cells of the perimeter * resolution
    - **The problem:** The more complex the polygon, the more grid cells will be at diagonal to their neighbors and the less accurate your results will be
    - Diagonal distance > lateral distance

- Calculating **area**
    - **Area** = number of cells * area of a cell
    - 
# Measuring Distances
- There are two ways of measuring distances in a **raster** dataset:
    - **Euclidean distance** = For each cell, the distance is calculated to the source cell (origin) by calculating the **hypotenuse** of the square triangle
        - Euclidean distance is used when calculating **buffer zones** around a feature of interest; two step process:
            1. Creating a Euclidean distance grid originating on the source pixel and the distance of each surrounding pixel to the source pixel
            2. Reclassifying the result to select the pixels within a specific distance (e.g. 20 m)
    - **Cell distance** = Calculate the distance from the origin through the center of neighboring cells
        - Useful to calculate the path from different points of the grid (shortest path); cost distance

# Cost Distance
- **Cost distance** = the least costly path (path with least obstruction) to reach a source for each cell location in the analysis

- While measuring Euclidean distance is essential, the chance of encountering a totally isotropic surface (where no obstructions or frictional changes exist) in reality is practically non-existent
    - In reality the shortest path between two locations is almost always obstructed, in this case Non Euclidean distance **(cell distance)** may be more meaningful
    - Ex: shortest path **following roads** between two houses; different from the distance between two houses as the crow flies

- Movement across non-identical surfaces incurs a **cost** (cost distance)

- **Functional cost distance** views distance in **cost units**, not geographical units
    - - **Objective:** determine the least costly path to reach a source (destination) for each cell location
    - 2 basic concepts in calculating functional cost distance:
        - **Friction Surfaces**
        - **Barriers**

## Friction Surfaces
- **Friction surfaces** = surfaces that involve some form of impedance (measured in friction value)
    - Topography may impose a friction value based on both surface roughness and the variable cost of moving up or down hill
    - 
- Ex: The least costly path between a forest stand and the nearest sawmill, based on slope, elevation and forest density.

## Barriers
- **Barriers** = discrete obstacles that interfere with movement across a surface

- Barriers can be:
    - **Absolute** (Ex: cliffs, fenced areas, lakes)
        - Absolutely permeable (Ex: bridge over stream);
        - Absolutely impermeable (Ex: ocean, mountain, cliff)
    - **Relative:** restrict but not prevent the movement (Ex: a patch of forest restrict but not prevent the movement of animal herd)

## Cost Distance Method
- Cost distance calculates the cost distance from the source cell to every other cells using the cost values

- **Example:**
    1. Create a cost grid. For example, if you want the find the best path between a forest stand and a sawmill, you would prefer the road to pass through areas of low slopes. Reclass your slope layer with low values (low cost) for low areas and high values (high cost) for mountain areas
    2. Calculate the cost distance for each link (2 first rows)
    3. From the cost distance derive the accumulative cost path, then the **least accumulative cost path**

- **Least accumulative cost path** = sum all the accumulative costs between a destination and the source and Keep the path with the lowest value
    - Requires: a source raster, a cost raster, derived distance cost, a destination and an algorithm for calculating the **least cost path**
    - Iterative process (derived after each possible path has been evaluated)

# Converting Raster to Vector, Vector to Raster
- **Converting raster to vector**
    - Transforms a raster file into a vector file (features)
    - All neighboring cells are connected to each other to determine line or polygon limits
    - Points are draw according to the **center of each raster cell**

- **Converting vector to raster**
    - The value of each cell is based on the values of ONE selected field
    - Errors are common in the converting process

- **Raster vs. Vector**
    - Data structure
        - Raster: simple
        - Vector: complex
    - Data volume
        - Raster: high
        - Vector: low(er)
    - Spatial resolution
        - Raster: limited
        - Vector: unlimited
    - Spatial analysis
        - Raster: powerful
        - Vector: restricted
    - Visualization/mapping
        - Raster: "pixely"
        - Vector: sharp

# Raster Selection & Reclassification
- Raster data can be **isolated (selected)** based on specific criteria:
    - Arithmetic, logical, and boolean operators can be used to select **(reclassify)**

- Raster layers can be **combined (overlay, mask)** in order to produce new information:
    - Arithmetic, logical, and boolean operators can be used to combine data layers and produce new data

## Selecting Raster Data

## Reclassifying Raster Data

# Raster Overlay
- **Raster overlay** = the combination of 2 or more raster datasets to create a new dataset
    - You may need to **reclassify** one or more of the files to create a useful overlay
    - You can use arithmetic, logical, and boolean operators

# Raster Mask
- **Raster mask** = the selection of pixels from one grid based on pixels from another grid (mask)
    - The mask grid must be binary (1 or 0); either masking or not masking
    - The mask can be used to "clip" other layers (like Photoshop clipping mask)

# Operators & Functions
- Operators and functions:
    - **Local functions**
        - Those that work on single cell locations
    - **Focal functions**
        - Those that work on cell locations within a neighborhood
    - **Zonal functions**
        - Those that work on cell locations within zones
    - **Global/proximity functions**
        - Those that work on all cells within a raster (global)
    - **Application functions**
        - Those that perform a specific application (Ex: hydrologic analysis functions)
    - **Cartographic model**

## Local Functions
- Operate on the value of each **single cell**
- Operations are independent of attribute values in neighboring cells
- New raster layer as function of input raster layers

- For a single dataset, examples of per-cell functions are mathematical functions (e.g. square root, sin, exponential log, etc), reclassification

## Focal Functions
- The value of a cell is determined by **neighboring cells**
- Explicitly make use of spatial associations to determine value of locations in output layer

- **Three elements of focal functions:**
    1. Target location
    2. Specification of neighborhood around target
    3. Determine function to perform calculation (Ex: mean, std, min, etc.)

### Filtering
- **Filtering using moving windows**
    - Involves moving a window of 3x3, 5x5, etc. an image 1 pixel at a time
    - Applies a mathematical calculation using pixel values under that window (e.g. mean, median, or mode)
    - Replace central pixel under window with new value

- **Low pass filter** = smooths an image
    - Emphasizes gradual trends at expense of local variability
    - Can be used to remove noise or artifacts in raster images

- **High pass filter** = sharpens an image (enhances edges)
    - Emphasizes abrupt changes in cell values
    - Brings out detail, high frequency information at expense of general trends

## Zonal Functions
- Operate on properties of **region (or zone)** to which a cell belongs
- These properties might be area, or shape
- Or attributes having a certain value on one grid with an area defined by a region on another grid

- **Applications of zonal functions:**
    - Urban planner may want to know average green space per planning zone or unit
    - Hydrologist may want to know average slope and height per watershed
    - Crop scientist may want to compute average soil nitrogen content per paddy field

## Global Functions
- **Proximity functions** = compute an attribute value for each cell according to length of shortest path between that cell and a target location/area

## Application Functions
- An application function performs an analysis that is specific to a discipline
    - Ex: hydrology functions create a stream network and delineate a watershed. You may find that a specific application function can manipulate cell-based data for an entirely different application from its category. For example, calculating slope is a surface analysis function that can be useful in hydrologic analysis as well

- **Application functions include the following:**
    - Density analysis
    - Surface generation
    - Surface analysis
    - Hydrologic analysis
    - Geometric transformation
    - Generalization
    - Resolution altering

## Cartographic Model
- **Cartographic model** = Set of interacting, ordered map operations that act on raw data, as well as derived and intermediate data, to simulate a spatial decision making process
    - Usually presented in graphic form
    - Implemented in the form of macros or a graphic modelling environment
    - An organizational tool; helps you think

- The functions associated with raster cartographic modeling can be divided into five types:
    1. Those that work on single cell locations **(local functions)**
    2. Those that work on cell locations within a neighborhood **(focal functions)**
    3. Those that work on cell locations within zones **(zonal functions)**
    4. Those that work on all cells within the raster **(global functions)**
    5. Those that perform a specific **application** (Ex: hydrologic analysis functions)