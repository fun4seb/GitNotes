# GEOG363 - Week 10: Data Sources & Statistical Surfaces
- Outline:
    - **Data collection**
        - Data sources
        - Data input methods
        - Data integration
    - **Statistical surfaces**
        - Elevation
        - Slope
        - Aspect

# Data Collection
- **Data collection**
    - Data sources:
        - Primary data (direct measurements)
        - Secondary data (derived from other sources)
    - Data input methods:
        - Data encoding (scanning, digitizing)
        - Data transfer (transfer of digital data)
        - Keyboard input (tabular data)
    - Data integration:
        - Data validation
        - Data transformation

## Data Sources
- Primary vs. secondary sources
    - **Primary data sources** = direct measurements collected in digital format, specifically for use in a GIS project
        - Primary **raster** data: remote sensing data
        - Primary **vector** data: GPS measurements, survey
        - Primary **attribute** data: observations, interviews
    - **Secondary data sources** = data that is collected by others; needs to be converted into a digital format
        - Existing spatial data: aerial photographs, maps, images
        - Attribute data

### Primary Raster Data Source: Remote Sensing Data
- **Remote sensing** = the science and art of obtaining information about an object without touching it
    - Ex: our eyes, camera, etc.

- **Raster data:**
    - Aerial photography
    - Optical remote sensing: MODIS, Landsat, SPOT, IKONOS, RapidEye
    - Unmanned aerial vehicle (UAV)
    - Radio detection and Ranging (RADAR)
    - Light detection and Ranging (LIDAR)
    - Sound navigation and Ranging (SONAR)

- **Resolution** is a key consideration
    - Spatial resolution refers to the size of an object that can be resolved and the most usual measure is the pixel size
    - Spectral resolution refers to the parts of the electromagnetic spectrum that are measured
    - Temporal resolution (repeat cycle) describes the frequency with which images are collected for the same area

### Primary Vector Data Source: GPS Measurements
- **GPS** = global positioning system

1. **The space segment**
    - The space segment of the GPS system consists of GPS satellites. These space vehicles send radio signals from space
    - There are **24 GPS satellites**; their orbits are designed so that at least six satellites are in view from everywhere at all times
        - Enough for accurate positioning
    - The information sent by satellites are:
        - Precise time information
        - Orbital parameters
        - Using these two sets of information, one can find the exact present, past, and future location of the satellites
2. **The control segment**
    - The control segment consists of a system of **tracking stations** location around the world. They monitor the information sent by satellites, and send correction to orbital and time information periodically
3. **The user segment**
    - The use segment consists of the **GPS receivers** and the user community. GPS receivers convert satellite signals into position, velocity, and time estimates. Four satellites are required to compute a location (X, Y, Z). Typically, 6 should be in view at all times, 8-9 being the average number
    - The GPS receivers can display the following information:
    - Position in latitude and longitude expressed in (deg., min.) or in (deg., min., sec.) convention. Both are used and easy to confuse!
    - Altitude from sea level (or sometimes from the surface of the Earth geoid) in meters or feet
    - Time in Universal Time Coordinates (UTC)

### Primary Vector Data Source: Survey
- Ground surveying is based on the principle that the 3-D location of any point can be determined by measuring angles and distances from other known points
- Traditional equipment like theodolites have been replaced by total stations that can measure both angles and distances to an accuracy of 1mm

### Secondary Data Source: Existing Spatial Data
- Existing spatial data may include:
    - Aerial photographs
    - Existing paper/digital maps
    - Images

## Data Input Methods
- Before data input, ask yourself...
    1. Does this data contain the information I need to answer my question?
    2. Is the data well documented, so that I understand what I am looking at?
    3. Is the data in a usable formation, if not can I convert it?
    4. Can I link it to GIS?
    5. If multiple versions or similar datasets exist, which one should i use?

### Encoding: Scanning & Digitizing
- In GIS, analog graphic data, such as paper maps and images, are **encoded** into computer formats by **scanning or digitizing**

- **Scanner** (paper to raster)
    - Pros:
        - Easy
        - Fast
        - Requires little skill
        - Good for **raster**
        - Vectorization: feature recognition
        - Paper maps: clean, stable
    - Cons:
        - High cost
        - File storage

- **Digitizer** (paper to vector)
    - Pros:
        - Low cost
        - Flexible
        - Easily mastered skill
        - Reliable
        - High quality of data produced
        - Good for **vector**
        - Rasterization
    - Cons:
        - Paper map stability (paper maps are unstable and may stretch or shrink while they are on the digitizing table)
        - Accuracy is dependent on the dedication and skill of the operator
        - Laborious and time consuming

### Keyboard Entry: Attribute Data
- Keyboard entry entails manually entering collected data into a digital file format (Ex: Excel, SQL, plaintext, etc.)

- When validating attribute errors look for...
    - **Impossible values:**
        - Most datasets contain values that are only within a certain range. Data values lying outside the normal range may need verifying
    - **Extreme values:**
        - These values may need to be checked against the source document
    - **Internal consistency:**
        - Does the data that are in summary tables or that may represent mean or median values correspond with those given in source documents?
    - **Trends:**
        - Data often exhibits a regional trend (Ex: air temperatures will decrease towards the poles) are there values that go against known trends?

### Data transfer
- **Data transfer** = digital file transfer (transferring spatial and attribute data via digital files)

- Digital attribute data:
    - Excel spreadsheets
    - Statistical spreadsheets (SPSS, Statistica, SAS, etc.)
    - Database systems (SQL)

- Digital spatial data:
    - Direct download from site (zipped format)
    - FTP (file transfer protocol)
    - CD, DVD

## Data Integration
- When integrating data from different sources:
    - Projections (all data should be in the same projection/coordinate system; different projection = different results!)
    - Georeference (satellite images, aerial photos)
    - Generalization (method to reduce detail in GIS data, simplification of GIS data, Ex: resampling, rescaling of vectors/rasters, etc.)
    - Data conversion (raster to vector, vector to raster)

# Statistical Surfaces
- **Statistical surfaces**
    - Elevation
    - Slopes
    - Aspect

- **Statistical surfaces** = surfaces as features containing height values (Z values) distributed throughout an area defined by sets of X and Y coordinate pairs
    - Z values (data) constitute a statistical representation of the magnitude of the feature
    - The Z value is often elevation but could be used to describe other qualities (Ex: soil fertility, population density, home value, etc.)

- **Values of surface datasets:**
    - X,Y = spatial coordinates (location)
    - Z = variable analyzed (thematic element being mapped)

- **Surface representation:**
    - Surfaces can be represented using contour or isolines, points, TINs (triangulated irregular network), and rasters (grids)
    - Most surface analysis in GIS is done on raster or TIN data

## Elevation
- **Digital elevation model (DEM) as a statistical surface**
    - Elevation information can be interpolated to calculate different forms of statistical surfaces:
        - Steepness of slopes
        - Azimuth or orientation (aspect)
        - Visibility and intervisibility
## Slope
- Slope is based on the relationship between the **horizontal distance and the vertical change in elevation**

- A common way of expressing slope is **rise/run** (%)
    - Rise: change in elevation
    - Run: horizontal distance

- Different approximation methods to calculate the slope:
    - **In raster data**, common methods use a 3x3 moving window (kernel)
    - The kernel passes over every pixel of the grid to calculate the **maximum rate of change** of value (slope) based on its neighboring cells
    - The surface created is called the **trend surface**

- **Calculating slope:**
    1. Compare the 4 cells adjacent to the central pixel to determine the rise and run values (2 axes)
    2. Keep the highest rise/run value
    3. **Calculate its slope in percentage (Percentage = rise/run x 100)**

- Applications of slope:
    - Engineering (Ex: road construction)
    - Hydrology (Ex: watershed)
    - Geomorphology (Ex: erosion and landslide)
    - Planning
    - Mapping

- Slope hill shading conventions:
    - Sun azimuth: 315 degrees (NW)
    - Sun altitude: 45 degrees
    - The shadow appears to fall toward the viewer

## Aspect
- Orientation (aspect) of a pixel is derived from the slope
- The aspect identifies the **down slope direction of the maximum rate of change** in value from each cell to its neighbors
- Aspect can be thought of as the **slope direction** (is the slope north vs. south facing?)
- The values of the output raster will be the compass direction of the aspect

- **Calculating aspect:**
    1. Compare the 4 rise values (4 axes)
    2. Keep the highest rise/run value
    3. Estimate the direct of the slope (aspect); expressed as compass directions

- Slope and aspect can vary based on:
    - The algorithm used
    - The local topography
    - The resolution of the original data