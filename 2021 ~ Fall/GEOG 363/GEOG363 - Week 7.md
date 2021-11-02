# GEOG363 - Week 7: Vector Analysis I

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
    - AND: intersection of 2 sets (features belonging only to A AND B)
        - Intersect tool
    - OR: Union of 2 sets (features belonging either to A OR B)
        - Union tool
    - XOR: Exclusive OR (features belonging to only A OR B but but not those belonging to BOTH)
        - Symmetrical difference tool
    - NOT: Difference operator (features belonging only to A NOT B)
        - Erase tool

- **Overlay:**
    - Vector based overlaying in ArcGIS:
        - **Erase tool** = A NOT B
            - Creates a feature class by overlaying the input features with the polygons of the Erase features. Only those portions of the input features falling outside the erase features boundaries are copied to the output feature class
        - **Intersect tool** = A AND B
            - Computes a geometric intersection of the input features. Features or portions of features which overlap in all layers and/or feature classes will be written to the output feature class
        - **Symmetrical difference tool** = A XOR B
            - Features or portions of features in the input and update features that do not overlap will be written to the output feature class
        - **Union tool** = A OR B
            - Computes a geometric union of the input features. All features and their attributes will be written to the output feature class

- **Buffering tool:**
    - Buffering is when you draw a polygon around a feature (point, line, or polygon) a set distance in every direction
        - To delineate protected zones around features
        - To show areas of influence
    - Can be used to do analysis related to the proximity of features
        - Ex: you might buffer a school by one mile and use the buffer to select all of the students that live more than one mile from the school
        - You could use a multi-ring buffer tool to classify the areas around a feature into near, moderate distance, and long distance classes for an analysis
    - Buffers are sometimes used to clip data to a given study area, or to exclude features within a critical distance of something
    - **Different types of buffering:**
        - Simple buffer (uniform distance)
        - Multiple ring buffer
        - Variable buffer (buffer distance changes based on attributes)
    - **Buffering boundaries:**
        - Dissolve vs. no dissolve (union of boundaries vs. no union of boundaries)

# Spatial Join
- **Spatial join** = Creates a table join in which fields from one layer's attribute table are appended to another layer's attribute table based on the relative locations of the features in the two layers

- Can join features according to boolean operators (OR, XOR, AND, NOT)

# Areal Interpolation
- **Areal interpolation** = Transferring known data from one set of polygons (source) to another set of polygons (target)

- **Steps for areal interpolation (Area-weighting):**
    1. Overlay both layers
    2. Query the areal proportion of each source polygon (e.g. census tracts) that is within each target polygon (e.g. school dist.)
    3. Apportion the data from source polygon (e.g. population) to target polygon according to the areal proportion
    4. Sum the apportioned data from each source polygon for each target polygon