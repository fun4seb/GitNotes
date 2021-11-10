# GEOG363 - Week 2: Vector & Raster Data
- **Spatial features/entities on earth can be described by their:**
    - Location (Ex: latitude, longitude)
    - Characteristics (Ex: color red, width of 5m, population of 435); represented by **attribute data**

- **Types of spatial features:**
    - **Continuous** features occur everywhere on the surface of the earth
        - Represented by **raster data models**
    - **Discrete** features occur in selected places on the earth's surface; objects with defined boundaries
        - Represented by **vector data models**

- **Raster** = the world consists of smooth, **continuous** fields
    - Building blocks: cells
    - Usable for: **continuous data**
- **Vector** = The world consists of sets of **discrete** objects, their attributes and their relations
    - Building blocks: points, lines, polygons
    - Usable for: **discrete data**

# Vector Data
- With vector data, spatial features are identified individually and represented by **coordinates**
    - A **point** is the building block of **lines and polygons**
        - A line is a set of connected points
        - A polygon is a closed circuit of lines

## Simple Vector Data Model
- **Main features:**
    - Also called "spaghetti" data model
    - Features are independent of each others
- **Benefits:**
    - Easy to create and store
    - Can be retrieved and rendered on screen very quickly
    - Interoperable (can be used across different software packages)
- **Drawbacks:**
    - Inefficient for modeling relationships between geographic objects (Ex: road network)

## Topological Vector Data Model
- **Topology** = a set of rules that model the relationship between neighboring points, lines, and polygons and determines how they share geometry
    - **Concerned with connectivity vs. contiguity**
        - Connectivity = if two arcs are connected at nodes; is there a path between nodes?
        - Contiguity = if two polygons share an arc; are two polygons neighbors?
    - Topology **allows spatial operations** based on connectivity and neighboring (contiguity) relations

- **Building blocks:**
    - **Nodes (points):** locations where arcs intersect
        - Ex: Node c is shared by arcs c-a and d-c and c-e
    - **Arcs (lines):** directed lines
        - Ex: Arc a-b is shared by polygons A and B
    - **Polygons:** closed circuit of lines
        - Ex: Polygon A and B are neighbors

- **Purpose of topological vector data model:**
    - Validate the geometry of vector entities
        - Validate the geometry of features
        - Determine if two polygons share boundary lines (arcs)
    - Perform spatial operations based on connectivity and contiguity relations
        - Ex: Polygon adjacency, network analysis

- **Benefits of topological vector data model:**
    - Efficient way of storing data
        - Fewer coordinates than in a simple structure (Ex: an arc may serve for several adjacent polygons but the actual coordinate for each arc is stored only once)
        - More tables for each file
    - Key for applying the concept of **planar enforcement**
        - The space of a real map must be completely filled
        - Polygons must not overlap

# Raster Data
- **Review**
    - **Geographic information systems (GIS)**
        - Purpose:
            - Perform operations on spatial data from the real world such as collecting, storing, transforming, displaying, analyzing, and retrieving.
            - Spatial relationships between different data types
        - Users:
            - Managers
            - Researchers
            - Corporations
            - Population (Ex: websites)
    - **Spatial Data**
        - Spatial data fall in two categories:
            - Spatial (where?)
            - Attribute (what?)
    - **Data types and data models:**
        - Continuous data:
            - Compatible with **raster data model**
            - Building blocks: cells
            - Ex: air temperature, image
        - Discrete data:
            - Compatible with **vector data model**
            - Building blocks: points, lines, polygons
            - Ex: bike paths, buildings

- **Raster data model** = division of continuous space into **valued cells** across a grid; also known as a **tessellation** model

- **Cell** = type of building block unique to raster data; acts like pixels across a resolution
    - Location (Ex: x,y coordinates)
    - Size (Ex: 1m) and resolution (fine vs. coarse)
    - Value kind: short or long integer (no decimal), float or double (decimal)
    - Value type: absolute (measurable) and coded (categories)

- **Data structures (in summary)**
    - Raster building blocks = cells
    - Vector building blocks = points, lines, polygons

## Structure of Raster Data
- According to the raster data model: the world consists of **smooth continuous fields**
    - Building blocks = cells (squares across a resolution)
    - Suitability = **continuous data**

- **Principles of raster structure:**
    - Also known as a **tessellation** model
    - Quantizing: dividing space into regular or irregular 2-D polygons (in the case of raster data, space is divided into a **grid of squares**)
    - Each chunk is associated with one feature

- **Grid structure:**
    - A grid consists of rows and columns
    - The origin is the upper-left corner
    - Columns are x-coordinates
    - Rows are y-coordinates
    - Each cell is defined by its row and column position

## Cells
- A **Cell** is a geographic object that has:
    - A location
    - A size
    - A value

### Cell Location
- Each cell is explicitly defined by its row and column position
    - Ex: (3,2; column 3, row 2), (5,7; column 5, row 7), etc.

### Cell Size
- **Cell size:**
    - A 10m cell is 10m x 10m (area of 100m2)
    - A 30m cell is 30m x 30m (area of 900m2)

- **Resolution:**
    - Cell size determines resolution of the raster data model
    - A 10m cell has a greater resolution (or is finer) than a 30m cell; A resolution made up of smaller cells can represent data in finer detail
        - If a resolution is low, we can say that it is coarse (low detail)
        - If a resolution is high, we can say that it is fine (high detail)

- **Projection:**
    - A flat grid does not fit neatly on the curved Earth surface
    - Cells can never be perfectly equal in size on the ground

- **Large vs. small cells (low vs. high resolution)**
    - Disadvantages of large cells **(low resolution)**
        - Not very precise spatially
        - Not very accurate thematically (mixed cell problem)
    - Disadvantages of small cells **(high resolution)**
        - More storage requires much more computer power to be viewed and processed
        - For an equal number of pixels, a high resolution grid covers a smaller area

### Cell Value
- Each cell has a **value** (even if it is a special value to indicate that there is “no data” or that data is “missing” at that location)
- That value is a **number** (actual values vs. coded values)
- The number **may or may not** have a numeric meaning depending on the variable being represented:
    - **Coded values:** The values stored in each cell are used as substitutes for categorical data (Ex: land cover classes); **NOTE: coded values must have NO DECIMAL**
    - **Absolute values:** The value of the cell represents the value of the phenomenon of interest (Ex: the elevation at that cell location)

- Cells from a raster have a unique **type**
    - Without decimal point
        1. Short integer: -32,768 to +32,767
        2. Long integer: -2,147,483,648 to + 2,147,483,647
    - With decimal point
        3. Floating point: -3.4E38 to 1.2E38
        4. Double: -2.2E308 to 1.8E308

## Creating Raster Data: Converting Vector into Raster
- Converting **points into raster**
    - Best case:
        - One point corresponds to one cell
        - Point diameter is equal to cell size
    - Potential problems:
        - 2 points fall in a single cell
        - Point is on the boundary between 2 or more cells
- Converting **lines into raster**
    - Best case:
        - Horizontal lines, vertical lines, oblique lines through cell corners
        - Line thickness is equal to cell size
    - Potential problems:
        - Line is narrower than the cells can show
        - Loss in detail (Ex: curves smaller than the cell resolution being represented as straight lines
- Converting **polygons into raster**
    - Best case:
        - Features are made up of rectangles having the same size and location as the grid to convert to
    - Potential problems:
        - How to deal with an edge overflowing into a cell; include cell or not?
        - Loss in accuracy during area calculations

### Mixed Cell problem
- **Cell assignment problem**
    - Each cell only holds a **single value!**
    - Ex: If a large cell covers over both forest, pasture, and water, which category should be represented within the cell?
- **Assignment methods:**
    1. The category with the **largest share** of the cell area gets represented (most common)
    2. The category at the **central point** of each cell gets represented

- **If a small entity is located at the intersection between 4 cell, it is possible it will not be shown according to each assignment method** (doesn't take up the majority of any one cell and isn't at the center of any one cell)

## Summary: Which Data Model Should You Use
- **General rule:**
    - **Vector model:** for discrete data such as rivers, roads, buildings, and political boundaries
        - **Topological:** when concerned with analysis related to connectivity or contiguity
        - **Simple:** all other cases
    - **Raster model:** for continuous data such as elevation, temperature, etc.

# Reading Notes: Chapter 2 - Data Models (Perusall)
- **Reading questions:**
    - Which are the two common GIS models?
        - The two common GIS data models are the vector data model (which uses points, lines, and polygons to represent real world objects; used for discrete data) and the raster data model (which uses valued cells in a grid; used to represent variables with continuous data occurring over a region such as temperature, rain, elevation, etc.)
    - According to the raster model, the world consists of continuous objects. Is it true?
    - According to the vector model, the world consists of continuous objects. Is it true?
    - To map Montreal's bike path network, it is best to use a vector data model. True or false, why?
    - What is an example of an entity-object correspondence in GIS?
    - What is recorded in an attribute dataset?
    - What are the basic types of vector objects?
    - What can topological models be used for?

- Data in GIS represents a simplified view of physical entities (roads, counties, mountains, etc.), GIS data includes information on the **spatial location** as well as **non-spatial properties** of entities (spatial + attribute data)

- Spatial data model = means of representing and manipulating spatially referenced information; A data model consist of two parts: 
    1. A graphical layer of points, lines, and polygons representing areas of interest spatially referenced to real world entities
    2. an identification number associated with each entity holding its **attribute data** (income, population, crime rate, etc.)

- Most GIS stores our data as a set of **layers**, each layer organizes the spatial and attribute data for a cartographic object
    - Ex: A GIS database of an area that includes a soils data layer, a population data layer, an elevation data layer, and a roads data layer; these layers of distinct thematic data can be combined and analyzed to produce new composite data layers

- Coordinates are used to define the spatial location and extent of geographic objects, usually in the form of a pair or triplet of numbers that specify location relative to an origin

## Common Spatial Data Models (Vector & Raster)
- All spatial data models are based on a conceptualization of the real world into a graphical simplification of reality in the form of **points, lines, and polygons** to represent all real world entities graphically

- Data models are often interchangeable in that many geographic phenomena can be representing by multiple different models

- **Two main conceptualization for digital spatial data: vector & raster data**
    - **Vector data** uses points, lines, and polygons referenced using coordinates to define real world objects; vector data is **discrete** meaning it uses clear definable boundaries (roads, property lines, location of wells, etc.) and has no room for ambiguity such as outlining the boundary of a forest as it thins out into plains
    - **Raster data** uses a cell-based grid system to plot data across an array (like pixels on a screen) and uses the value of cells to represent the type or quality of a mapped variable; raster data is best used with variables that change continuously across a region (elevation, slope, temperature, etc.)