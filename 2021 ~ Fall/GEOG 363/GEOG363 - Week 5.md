# GEOG363 - Week 5: Coordinate Systems
- **Outline:**
    - Introduction to coordinate systems
    - Geoids, Ellipsoids, and Datums
    - Geographic coordinate systems
    - Projected coordinate systems

# Coordinate Systems
- **Coordinate system** = a system that uses **numeric coordinates** to uniquely identify location on a surface

- **Elements of coordinate systems:**
    - An origin/starting point
        - Ex: 0, 0
    - A number of dimensions (2D or 3D)
        - Defines the number of axes
    - Axis
        - Sequence of axes (which comes first when referencing?)
        - Direction in which coordinates increment along axis
        - Units of measurement (degrees, meters, feet)

- **Why are coordinate systems important for GIS?**
    - Required to locate geographic features on the surface of the earth
    - Each GIS layer has its own projection/coordinate system
    - Each GIS project is made of several layers
    - **For Spatial Analysis:** all layers should be in the same coordinate system

- Two major types of coordinate systems:
    - **Geographic coordinate system** = The mathematical or physical representation of the earth’s surface
        - Geoid (physical)
        - Spheroid (mathematical)
        - Ellipsoid/datum (mathematical)
    - **Projected coordinate system** = The mathematical transformation to convert a 3-D mathematical/geometric shape (Spheroid, Ellipsoid) into a 2-D shape (map)
        - Convert a 3D (spherical) coordinate system into a 2D (planar) coordinate system

# Geoids, Ellipsoids, and Datums
- Geoid = a close representation or physical model of the figure of the Earth
    - The shape of the geoid is irregular
    - Geoids are mostly used in Geodesy science (more accurate for elevation but cannot be modeled mathematically)

# Geographic Coordinate Systems
- A Geographic coordinate system is a non-projected coordinate system
- It is based on the datum
- Coordinate are given in **latitude** and **longitude** (Lat/Long)
    - Lat/Lon correspond to angles at the center of earth based on a defined origin

- **Graticule** = spherical grid of co-ordinate lines over the planetary surface; graphical grid on a map or globe

- **Latitude:**
    - **Parallels** = lines of latitude
    - is a measure of the angle between the point and the equator along the meridian
    - has a range of -90 degrees (S pole) to +90 degrees (N pole)

- **Longitude:**
    - **Meridians** = lines of longitude
    - Measures the angle on the equatorial plane between the meridian of the point and the central meridian (through Greenwich, England)
    - has a range of -180 degrees (westward) to +180 degrees (eastward)

# Projected Coordinate Systems
