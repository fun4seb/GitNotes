# GEOG260 - Week 2: What is a Map, Critical Cartography, Scale, Coordinates & Projections

# What is a Map?
- **Maps can be many things**; no one single definition or use of maps
    - A spatial representation of the environment
    - A graphic statement that locates facts
    - A symbolized image of geographical reality...

> "The map is nothing but an assertion of the state of the world by its maker..." "A map is not an objective depiction of reality. It is a symbolic interpretation of place and highlights the relationship between elements in space, either perceived or actual. It reflects choices, biases, and agendas of the mapmaker"

- **Maps as Engines**
    - Energy > engine > work
    - Social energy > map > social space, social order, knowledge

# Critical Cartography
- process of pulling apart and analyzing maps to determine why they were made and why certain decisions were made
- Challenges the traditional practices of maps and links geographic knowledge with political power and understanding this relationship is key in understanding maps
- Relevant to this course through the idea of **mapping vs. making maps**
    - One is a mental process (mapping) and one is a physical process (making maps)

## Whats on a Map?
- **Data**
    - Qualitative
    - Quantitative
- **How is this data communicated?**
    - Words
    - Lines
    - Shapes (polygons)
    - Grids
    - Points
- **Design tools are used to manipulate those representations of data**
    - Colors
    - Fonts
    - Size
    - Thickness
    - Shade

## Multiple Cartographic Functions
- Maps are a **symbolic form of communication**; a symbolic language
- Maps have many functions...
    - Location
    - Traveling
    - Displacement
    - Measuring
    - Evaluation
    - Territorial claim
    - Control
    - Spatial analysis
    - Communication
    - Commerce
    - Politics
    - Planning
    - Etc.

## Map Types
- **3 types of maps:**
    - Mental maps
    - Tangible maps
    - Virtual maps
- **These maps fall into 2 categories:**
    - Reference maps
    - Thematic maps
- All maps are comprised of **qualitative and quantitative data** that is made of **single and multi variables**

### Common Reference Maps
- **Planimetric maps**
    - Refers to "common" reference maps (road maps, photo maps, planning maps, cadastral survey, etc)
    - Planimetric maps are **flat**; only working in two dimensions
        - No height indications + map used for reference = planimetric map
- **Topographic maps**
    - Topographic maps = Reference maps concerned with **elevation**; added the z-axis
    - Done through using lines that distinguish between changes in elevation over space

### Common Thematic Maps
- **Choropleth maps**
    - Understanding how data relates to space
    - Overlays a "quality" onto a physical map (Ex: Temperatures over an area plotted visually)
- **Dot maps**
    - Locate different types of phenemenon in space with dots
    - Common for uses such as plotting population density
- **Isoline maps**
    - "Weather maps"
    - Link points of data that are constant, such as a line along spots where the weather is the same
- **Flow maps**
    - Trace the flows of quantities of objects from one place to another (peoples, products, etc.)
- **Cartograms**
    - "Inflation maps"
    - Distort the map spatially according to the relavent data (Ex: size countries according to their GDP)

# Scale
> Map scale = distance on the map (Dm) / distance on the ground (Dg)

- **Expressed as a fraction where the distance on the map (Dm) is reduced to 1**
    - Ex: a scale of 1:1000 means that 1 unit on the map is equal to 1000 units on the ground
    - Can also be expressed **verballed** ("1 km = 100 km"), or **visually** in the form of a bar scale or variable scale

- **Large vs. small scale maps**
    - Large scale = "zoomed in" map, meaning scale ratio number is small; **large scale lots of detail**
    - Small scale = "zoomed out" map, meaning scale ratio number is small; **small scale less detail**

# Projections & Coordinates
- **There are two types of coordinate systems:**
    - Non-projected
    - Projected

- Different coordinate/projection systems = different results

## Non-projected Geographic Coordinate System
- Each location is determined by a grid structure:
    - **Parallels (Latitude):** N/S position (equator is the starting point)
        - Arctic Circle = 66°33'48.4" N
        - Tropic of Cancer = 23.43657° N
        - Equator = 0°
        - Tropic of Capricorn = 23.43657° S
        - Antarctic Circle = 66°33'48.4" S
    - **Meridians (Longitude):** W/E position (prime meridian is used)

- This network of parallels and meridians is called the **graticule**, and locations can be expressed as...
    - **DMS (degree, minutes, seconds)**
        - 15° = 1 hour or 60 minutes worth of rotation
    - **DD (decimal degrees)**
    - **Rad (Radians)**

- This system works well for precisely locating things and for 2D and 3D representations of Earth
    - Represent a 3D sphere (Earth) as a 2D map
    - **Equirectangular grid** (360° E/W and 180° N/S)

- **Null Island** = center of equirectangular grid; where the equator and prime meridian meet (0° lat, 0° long)

## Projected Coordinate Systems
- **Understanding projections summary:**
    - Distortion increases near the edges
    - Compromise projections spread the distortion around evenly (do nothing perfect but most things well enough)
    - Choose a projection method based on what properties the map is designed to communicate and also account for:
        - Area
        - Form
        - Distance
        - Direction
    - **There is never a single right answer when choosing a map projection**

## Datums
- Conversion of the Earth from a blob into a clean mathematic **ellipsoid** (3D sphere) that can be used to project coordinates onto and create maps
- A "regional surface model" of the Earth; different countries use different ellipsoids that best approximate their portion of the Earth

- The Earth is **not a perfect sphere**; it is an ellipsoid/spheroid also known as a **geoid**

- **Geoid vs. ellipsoid vs. map**
    - Reality: Earth is a 3D geoid
    - Mathematical approximation: 3D ellipsoid
    - Projection: 2D map

- **3 primary projection surfaces:**
    - Cylindrical
    - Conic
    - Azimuthal/Zenithal (flat plane)

- **Focal point** (location of light source used to make the projection)
    - Polar (center on a pole)
    - Equatorial (center on the equator)
    - Oblique (center on a non-specific point/line)
    - Transverse (center to a line 90° to the polar axis; parallel to equator)

## Distortion
- Whenever a projection is created due to conversion from 3D (Earth) to 2D (map) there is always **distortion**; every projection distorts the world and all projections are based on **compromise**
    - **Tissot's index** = index of distortion measured mathematically by observing the distortion of circles that are placed at the intersections of lat & long points

- **Projections can preserve either:**
    - Shape (conformal)
    - Area (Equivalent)
    - Distance (Equidistant)

- **Ways to project maps to solve for distortion:**
    - **Conformal projection** = projection that preserves shape/angle = 
        - Commonly used for topography, navigation, civil engineering, military maps
    - **Equivalent projection** = projection that preserves area
        - Commonly used for accurate spatial extent (land use maps), and quantitative attributes by area (Ex: GDP by country)
    - **Equidistant projection** = projections that preserves distance/direction
        - Commonly used for navigation, geological measurements, calculating distance costs, range depiction, meteorology
        - Ex: Gnomic projection (top down view of glob, extreme distortion), and Azimuthal Equidistant (preserves the distance between all points while compromising projection
    - **Interrupted projections** = projections made onto irregular surfaces (Ex: Fuller projection projects landmasses like a chain onto an unfolded dodecahedron)
    - **Compromise projections** = projections do not try to perfectly preserve any property and instead tries to balance distortion between many properties