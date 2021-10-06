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

- **Two major types of coordinate systems in GIS:**
    - **Geographic coordinate system** = The mathematical or physical representation of the earth’s surface into **3D coordinates**
        - Geoid (physical)
        - Spheroid (mathematical)
        - Ellipsoid/datum (mathematical)
    - **Projected coordinate system** = The mathematical transformation to convert a 3-D mathematical/geometric shape (Spheroid, Ellipsoid) into a **2-D plane (map)**
        - Convert a 3D (spherical) coordinate system into a 2D (planar) coordinate system

# Geoids, Ellipsoids, and Datums
- **Geoid** = a close representation or physical model of the figure of the Earth
    - **Physical model** for representing the Earth in 3D; accurate way of representing the Earth and its irregular topography however not useful for math or GIS applications
    - The shape of the geoid is **irregular**; looks lumpy
    - Geoids are mostly used in Geodesy science (more accurate for elevation but cannot be modeled mathematically)

- **Ellipsoid/spheroid** = simplified geometric representation of earth in the form of a perfect sphere or ellipse, it may not correspond perfectly to every place on earth (e.g high mountains)
    - **Geometric model** for representing the Earth in 3D

- **Datum** = "a mathematical model of the earth, which serves as the reference or base for calculating the geographic coordinates of a location”
    - A datum is a reference ellipsoid together with an offset from the center of the Earth; By specifying different offsets, we can use the same standard ellipsoids in many different regions of the Earth
    - Different countries will often use the same ellipsoid but with different offsets/datums
    - A datum roughly approximates the surface of the earth at some mean sea level value

# Geographic Coordinate Systems
- **Geographic coordinate system** = The mathematical or physical representation of the earth’s surface into **3D coordinates**
        - Geoid (physical)
        - Spheroid (mathematical)
        - Ellipsoid/datum (mathematical)

- A Geographic coordinate system is a non-projected coordinate system
- It is based on the datum
- Coordinate are given in **latitude** and **longitude** (Lat/Long)
    - Lat/Lon correspond to angles at the center of earth based on a defined origin

- **Graticule** = spherical grid of coordinate lines over the planetary surface; graphical grid on a map or globe

- **Latitude:**
    - **Parallels** = lines of latitude
    - is a measure of the angle between the point and the equator along the meridian
    - has a range of -90 degrees (S pole) to +90 degrees (N pole)

- **Longitude:**
    - **Meridians** = lines of longitude
    - Measures the angle on the equatorial plane between the meridian of the point and the central meridian (through Greenwich, England)
    - has a range of -180 degrees (westward) to +180 degrees (eastward)

# Projected Coordinate Systems
- **Projected coordinate system** = The mathematical transformation to convert a 3-D mathematical/geometric shape (Spheroid, Ellipsoid) into a **2-D plane (map)**
        - Convert a 3D (spherical) coordinate system into a 2D (planar) coordinate system

- **Map projection procedure:**
    1. Start with physical model of the earth **(geoid)**
    2. Turn into **ellipsoid**
    3. Localize the ellipsoid to create a **datum**
    4. From this datum, produce **projections**

- Serve to transform geographic coordinates into plane coordinates

- Different classes of map projections based on:
    - Distortion
    - Projection surface:
        - Geometric shape: cylinder, cone, plane
        - Point of contact: tangent, secant
        - Orientation of surface (aspect): normal (i.e. equatorial), transverse, oblique

## Distortion
- Projecting Earth’s surface always involves **distortion**

- **Four spatial properties are subject to distortion:**
    - Shape
    - Area
    - Distance
    - Direction
 
- Each map is attempting to **preserve** one of the following spatial properties:   
    - Shape (Conformal)
    - Area (Equivalent or Equal Area)
    - Distance (Equidistant)
    - Direction (Azimuthal)
    - Most of everything (i.e. generalist)

- **No flat map can be both equal area and conformal**

- **Tissot indicatrix** = method of visualizing the distortion of a map by placing equal size circles across the map in a grid > after the projection method is applied you can observe how the circles in different parts of the map are distorted differently
    - Ex: circles at poles of the map will be stretched while the equator will stay unchanged

## Projection Surface: Shape
- Classification is based on the type of projection surface onto which the globe is conceptually projected:
    - **Azimuthal (planar)** = result from projecting a spherical surface onto a plane
    - **Cylindrical** = result from projecting a spherical surface onto a cylinder.
    - **Conic** = result from projecting a spherical surface onto a cone.
    - Within each family there is a tangent and secant case

## Projection Surface: Aspect
- The aspect describes how the projection surface surface is placed relative to the globe, it may be:
    - **Normal or equatorial** (such that the surface's axis of symmetry coincides with the Earth's axis),
    - **Transverse** (at right angles to the Earth's axis) or
    - **Oblique** (any angle in between).
    
## Projection Surface: Contact Point
- The projection surface can be placed in relation to the Earth either so that there is only one point of contact, thus meaning there is no intersection between projection surface and Earth **(tangent)**, or with two points of contact, meaning that at some point the surface would have to "cut" through the Earth model conceptually **(secant)**
    - **Tangent** = cylinder, cone or plane are “tangent” to the ellipsoid (no intersection) making only one point of contact at high point of ellipsoid); useful for global maps
    - **Secant** = cylinder, cone or plane “cuts” through the ellipsoid (intersecting) making multiple points of contact; useful for regional maps
        - **Standard parallel** = line of intersection where the projection shape "cuts" through the ellipsoid; every point along this line is touching and thus is not distorted at all

- **Different map projections = different results (In GIS)**
    - Must make sure all features in a map are of the same projection method; can be a major problem for GIS

## Choosing Map Projections
- Most common projections:
    - **Albers Conic Equal-Area:** Good for Canada or individual provinces which span many UTM zones (e.g. BC, Yukon, Quebec) . Good default map. Thematic mapping.
    - **Lambert Conformal Conic:** Good for North America, Canada (when the area is across several UTM zones)
    - **Universal Transverse Mercator (UTM):** Good for small areas, small extents (1:250,000 or larger e.g. 1:10,000).

- **Rules of thumb:**
    1. Metadata containing projection and coordinate system information is necessary (if you get or release the data)
    2. Selecting the appropriate projection and correct parameters of projection is more critical when displaying large areas (Ex: global scale) then when displaying small areas (Ex: city map)

- **Issues to consider:**
    - Extent of area to map: city, province, country, world?
    - Location: polar, mid-latitude, equatorial?
    - Predominant extent of area to map: East-West, North-South, Oblique?

### Universal Transverse Mercator (UTM)
- Created by Johann Heinrich Lambert in 1772 by modifying the Mercator projection into its **transverse form**
- Became widely used in the US after World War II
- Minimizing distortion by dividing the earth into narrow strips running from pole to pole

- UTM divides the earth (between 84°N and 80°S) into **60 zones** (strips), each of which covers 6 degrees of longitude
    - Zone 1 begins at 180 ° W longitude.
    - Each zone is centered on a meridian (origin for longitude) with a value of 500,000 m
    - Secant: Minimizes distortion in a narrow strip from pole to pole
    
- **Properties:**
    - Shape - are preserved in small areas (Conformal)
    - Area - Minimal distortion of larger shapes occurs within the same zone.
    - Distance – Scale is constant along the central meridian
    - Direction - local angles are true
- **Limitation:**
    - Error and distortion increase for regions that span more than one UTM zone; UTM is not designed for areas that span more than a few zones. (not Equivalent)

- **Do not use UTM if your study area spans 2+ UTM zones**
    - Do not use UTM for maps with scales smaller (meaning covering a larger scope) than 1/250,000
    - Canada spans 16 UTM zones (zones 7 to 12) meaning you cannot use UTM to display all of Canada because it covers multiple zones

## Things to Remember for GIS
- When you download geographical data:
    - Check the datum (based on an ellipsoid)
    - Check the coordinate system (geographic or projected)
    - Check the unit (meters or feet)
    - **Must make sure everything is constant between features when performing any spatial analysis/calculations**

- Transform all your data into a unique coordinate system!

## Projecting in ArcGIS
- **Two different functions:**
    - Project
    - Define Projection
    - **Two different uses (DO NOT CONFUSE!)**

- Project vs. Define projection
    - **Project** = use when your dataset already has a coordinate system and you want to convert it to another projection
        - Changes coordinates in file
        - Changes definition also
        - Creates new data set
        - Use when changing a coordinate system permanently
    - **Define projection** = use when your dataset has NO coordinate system assigned to it and you obtain information regarding what it is, allowing you to then **define the projection system**
        - Does not change coordinates
        - Keeps original dataset
        - Essentially changing the metadata of the dataset to be in accordance with its correct coordinate system
        - Use only when you know the coordinate system

## Projected Coordinates Summary
- Projection: a two dimensional representation, using a plane coordinate system, of the earth’s three dimensional sphere/spheroid

- location on the 3-D earth is measured by **latitude** and **longitude**
- location on the 2-D map is measured by **x,y Cartesian coordinates**
    - (X,Y) coordinates change from one projection to another one for aspecific location.