# GEOG363 - Week 2: Vector & Raster Data

# Lecture Notes: Vector Data

# Lecture Notes: Raster Data

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

- All spatial data models are based on a conceptualization of the real world into a graphical simplification of reality in the form of **points, lines, and polygons** to represent all real world entities

- **Two main conceptualization for digital spatial data: vector & raster data**
    - Vector data uses points, lines, and polygons referenced using coordinates to define real world objects; vector data is **discrete** meaning it uses clear definable boundaries (roads, property lines, location of wells, etc.) and has no room for ambiguity such as outlining the boundary of a forest as it thins out into plains
    - Raster data uses a cell-based grid system to plot data across an array (like pixels on a screen) and uses the value of cells to represent the type or quality of a mapped variable; raster data is best used with variables that change continuously across a region (elevation, slope, temperature, etc.)