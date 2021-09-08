# GEOG260 - Week 10: UTM, Cross Sections, Slope Interpolation

# National Topographic System Maps (NTS)
- Topographic maps produced by Natural Resources Canada
- Regionally defined
- Common standard scales: 1:50,000 and 1:250,000
    - The 1:250,000 scaled maps are identified by a combination of numbers and letters (A-P); Ex: 13C
    - The 1:250,000 blocks are divided into 16 segments (1 to 16), forming blocks used for 1:50,000 scale mapping

- Canadian topographic maps can be found at: "geogratis.gc.ca"

- All maps are labeled so they can be stitched together with adjacent maps with larger maps

# Universal Transverse Mercator (UTM)
- Plane-coordinate grid system
    - Consists of 60 zones that are ~6 degrees wide
    - Start at prime meridian (zone 30), and counts up towards 60 east of it, and down towards 0 west of it

- UTM is primarily used for land navigation
- **"Transverse"** Mercator refers to the projection being tilted on its side to create an incredibly accurate map along the prime meridian rather than the equator

# Interpolation
- **Interpolation** = the process of estimating unknown values that fall between known scales
    - **Linear interpolation** refers to looking at **two points** and inferring the value of a point between them
    - **Polynomial interpolation** refers to looking at **all data points** as a whole to predict where the data points are moving; better for complex data
    - **Piecewise polynomial interpolation** is a combination of linear and polynomial