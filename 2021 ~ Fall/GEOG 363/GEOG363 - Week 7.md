# GEOG363 - Week 7: Vector Analysis

# Measuring Vectors
- Measuring objects: **lines**
    - Line is based on a set of **vertices**, these vertices can be used to calculate:
        - Length
        - Shape
    - **Line length** = sum of all line segments
    - Line segment lengths are computed using **Pythagorean theorem**

- Measuring objects: **polygons**

- **Calculate geometry** = ArcGIS function allowing geometry calculations on **projected** data

# Geoprocessing Tools
- **Boolean operators:**
    - AND: intersection of 2 sets (Belong to A and B)
    - OR: Union of 2 sets (belong either to A or B)
    - XOR: Exclusive OR (Belong to A or B but not both)
    - NOT: Difference operator (belong to A but not to B)

- **Buffering:**
- **Overlay:**
    - Vector based overlaying in ArcGIS:
        - **Erase** = A NOT B
        - **Intersect** = A AND B
        - **Symmetrical difference** = A XOR B
        - **Union** = A OR B

# Spatial Join
- **Spatial join** = Creates a table join in which fields from one layer's attribute table are appended to another layer's attribute table based on the relative locations of the features in the two layers

- Can join features according to boolean operators (OR, XOR, AND, NOT)
    - **Symmetrical difference (XOR)** = Features or portions of features in the input and update features that do not overlap will be written to the output feature class
    - **Union (OR)** = Computes a geometric union of the input features. All features and their attributes will be written to the output feature class


# Areal Interpolation
- **Areal interpolation** = Transferring known data from one set of polygons (source) to another set of polygons (target)

- **Steps for areal interpolation (Area-weighting):**
    1. Overlay both layers
    2. Query the areal proportion of each source polygon (e.g. census tracts) that is within each target polygon (e.g. school dist.)
    3. Apportion the data from source polygon (e.g. population) to target polygon according to the areal proportion
    4. Sum the apportioned data from each source polygon for each target polygon
