# GEOG363 - Week 3: Mapping

# Lecture Notes: Mapping I
- **Cartography** = "representation, normally to scale and on a flat medium, of a selection of material or abstract features on, or in relation to, the surface of the Earth"

- **Maps and GIS**
    - GIS are often used mainly for mapping purposes
    - A map is the major outcome of GIS analysis (Ex: informing decision making)
    - Inappropriate maps are commonly designed in GIS (Ex: wrong methods, bad classification, poor design)
    - Designing proper maps is a key elements for any GIS project

- **The power of maps:** can simultaneously communicate the relationships between 3 dimensions:
    - Locations in 2 dimensions (x,y); describes **where**
    - Attributes related to the "where" (describes **what**)

## The Cartographic Elements
- The main function of a map is to better **understand** and/or **communicate** geographic information and structure

- **Maps must:**
    1. Include all necessary map elements **(ALWAYS: north arrow, legend, source, title, scale bar)**
    2. Be clear (written and visual information)
        - Clear message: adapted to a specific public/viewer (is the map for an expert or novice?)
        - Clear representation: make use of appropriate symbols to represent the spatial pattern and processes; map symbology
        - Clear visual perception: follow the rules of visual perception and design (color conventions, visual hierarchy, balance)
        - Conventional (water in blue, etc.)

### Map Elements
1. **Projection** (depends)
    - The link between the ellipsoid (Earth) and a flat map; projection method of projecting the 3-D earth onto a 2-D map (Ex: Mercator, Robinson, etc.)
    - Fundamental concept in GIS
    - Only appears on maps when accurate location is fundamental
    - Not necessary to represent:
        - At fine scale
        - When location is secondary

2. **Scale** (always)
    - Link between the real world and its representation
    - A ratio representing a distance on the map compared to a distance on Earth
    - Useful for:
        - Evaluating the size of the area mapped
        - Measuring distances
    - **A graphic scale is essential on every map**
        - Simple, not too big, and with **round values**

3. **Title** (always) 
    - A synopsis of the cartographic message being conveyed
    - Must be complete, concise, and visible
    - Two kinds of titles:
        - Neutral
        - Leading

4. **Other descriptive text** (depends)
    - Ideally 1 font on a map
    - Size: not under 7 points (paper map)

5. **Source** (always)
    - The source of the information should always appear:
        - For ethical reasons (academic honesty, respect of source, etc.)
        - To present verifiable and reliable information
        - To give possible access to the original data
    - Should be small but visible (this is NOT the main information)

6. **Legend** (always)
    - Translation from graphical to textual language
    - Divided into two parts:
        - Graphical signs
        - The text explaining them
    - **Every feature's color should be in your legend**
    - The legend must be structured and clear:
        - Values must be easy to read
        - Elements must be aligned
        - Avoid redundancy and non-useful information (Ex: "Legend" heading)
        - Information should be consistent

### Map Symbology
- **Map Symbology** = the use of appropriate **symbols** to represent the spatial patterns and process

- **For nominal data:**
    - Points: different shapes and/or hues, and not different sizes
    - Lines: vary only in pattern and/or hue, not in thickness
    - Polygons: only different area hues or patterns should be used, and not different values of selected hues.
    - **Not implying ranking or relationship (no variance in size, thickness, or value)**

- **For ordinal data:**
    - Points: geometric shape or a pictorial symbol. Variation of size, color or both color and size for emphasis
    - Lines: rank data by line weight, style, or hue. Any combination of these methods is possible.
    - Polygons: can show quantitative differences in data by different hue/color value, and pattern fills. For further emphasis, patterns can also be in different colors

- **For interval/ratio data:**
    - Points: various colors, shapes, and size may be used (e.g. graduated dots, circles, squares, bars, block piles, pie charts)
    - Lines: can be graduated. Contours are the most common form of this line symbol (elevation value and position & calculation of slope).
    - Polygons: can use variations in color value and pattern to show a gradual progression of data values

### Rules of Visual Perception
- **Visual acuity**
    - Ability of the human eye to differentiate between fine details; includes differentiation of gray tones, color hues, linework, symbol, etc.
    - Legibility of the smallest details: (assumes perfect vision)
        - Points: 0.2 mm diameter
        - Lines: 0.1 mm thickness
        - Area: 0.4 mm side filled or 0.6 mm side empty

- **Visual contrast**
    - Having clear visual contrast between map elements leads to:
        - Easier map reading
        - Easier differentiation
        - Establishes visual hierarchy of importance

- **Visual balance**
    - Always consider **order** (the sequence in which map readers view components of the map); eye moves from upper left, through the optical center, to the lower right
        - The sense of orderliness in a map determines if it is comfortable to look at to the eye
    - Pleasing page layout (symmetrical vs. asymmetrical layout)

- **Visual hierarchy**
    - Ordering of map elements where important features are "popping" in the foreground and less important features are less visually grabbing; if every feature is competing for your attention the map becomes confusing and messy
        - Adds **depth** and **ordinality** to map

### Color Conventions
- Certain color associations have been used to derive color conventions in mapping:
    - Land masses = tan
    - Water = blue
    - Vegetation = greens

- **Bold indicates IMPORTANCE**

## Map Types
- **Reference maps:**
    - Emphasis is on location; the **
    - All data is at the same level of importance
    - Serve mobility and navigation needs
    - Reference map examples: topographic, street, atlas

- **Thematic maps:**
    - Emphasis is on location AND attribute values
    - Attributes = qualities or magnitudes related to the graphical information (non-graphical information that describes the **"what"**)
    - By mapping locations AND attributes we can formulate:
        - Relationships among locations (Ex: distance)
        - Relationships among various attributes at one location (Ex: temperature, rainfall)
        - Relationships among the locations of a given attribute (e.g. rainfall or temperature from place to place)
        - Two or more levels of importance
    - Thematic map examples: choropleth, dot, graduated symbol, isoline, flow, value-by-area maps

# Lecture Notes: Mapping II
- Map types:
    1. Reference maps
    2. Thematic maps
        - Require a **classification method**

## Reference Maps
- Emphasis is on location; the **“where”**
- All data is at the same level of importance; categories do not have any specific order **(nominal data)**
- Serve mobility and navigation needs (Ex: topographic, street, atlas)

- Category approach:
    - Simplest type of mapping
    - Simply assigning different colors or symbols to each feature within a category (Ex: soil types, land use zones, biomes, etc.)

## Thematic Maps
- Emphasis is on attribute values (at locations)
    - **Attributes** = qualities or magnitudes related to the graphical information (non-graphical information that describes the **"what"**)
    - The "what" is tied to the "where"

- By combining locations and attributes into thematic maps we can formulate:
    - Relationships among various attributes at one location (Ex: temperature, rainfall, etc.)
    - Relationships among the locations of a given attribute (e.g. rainfall, temperature or income from place to place)

- **Types of thematic maps:**
    - Choropleth (only for rates or relative data; data needs to be classified)
    - Graduated symbols (can be used with count or raw data, and rates; data needs to be classified)
    - Proportional symbols (can be used with count or raw data, and rates)
    - Dot density (can be used with count or raw data, and rates)
    - Cartograms
    - Isarithmic/isoline

### Choropleth
- Uses graduated colors to show **relative data** (no raw data, no counts)
- Quantitative values are grouped into classes (classification) and each class is identified by a particular **color**

- **Choropleth maps are meaningful with relative data, but misleading with absolute data**
    - Ex: mapping total deaths vs. death rate; by mapping the total count of deaths it might lead one to believe the most populous areas are the most dangerous while mapping the death rate may actually reveal that people are dying disproportionately somewhere else

### Graduated Symbols
- Uses graduates symbols to show **relative data or counts**
- Quantitative values are grouped into classes (classification) and each class is identified by a particular symbol **size**

### Proportional Symbols
- Proportional symbols use the visual variable **size** for representing quantities (absolute value)
- **The size of each symbol reflects the actual data value in reality**; The sizes are directly proportional to the data
    - Ex: if you map earthquakes using proportional circles, the radius of the circle is proportional to the magnitude of the quake

- Size can be used for hierarchy (ordinal)

- Size is:
    - Easy to calculate with **lines**
        - 2 problems:
            1. Eye perceives only few classes (5 max.). So not appropriate when you have too many values
            2. Very wide lines are not always a good idea (cover too much real estate)
    - Very common with **points**
        - Principle: there is a constant relationship between the quantities (data) and the symbols representing these quantities
        - Proportional symbols can serve to represent the center of **polygons**
        - Better with circles (or squares) than with pictographic symbols
    - Rare with **polygons** (often represented as points)

### Dot Density
- Dot density maps show the amount of an attribute within an area
- Each dot represents a specified number of features—for example, one dot represents 1,000 people or 10 burglaries within a given area

### Cartograms
- A cartogram is a type of graphic that depicts attributes of geographic objects as the object's area
- Because a cartogram does not depict geographic space, but rather changes the size of objects depending on a certain attribute, **a cartogram is not a true map**

### Isarithmic/Isoline
- **Isarithm** is the proper generic term for a line on a map connecting points of constant value
    - **Isoline** is the more common term used for this type of map
- Isoline refers to a line symbol to connect points of equal or constant value.
- For interval/ratio data

## Classification
- **Classification** = process of transforming quantitative data into ordinal data (classes)

- **Two step process:**
    1. Determine the number of classes
        - Number of classes should be based on the public (Ex: expert = higher number of classes) and the **volume of data (unique values)**
            - Less than 20: 3 or 4 classes
            - 20 to 30: 4 or 5 classes
            - 30 to 50: 4 to 6 classes
            - 50 to 100: 5 to 7 classes
            - Greater than 100: 5 to 8 classes
    2. Determine the classification method
        - Criteria that can assist in selecting a classification scheme:
            - The public (goal of the map)
            - The data distribution
            - Ease of understanding the map and legend
            - Unique map or multiple maps
        - **Context + data understanding must drive classification**
            - Best way of understanding a data distribution is the creation of a **histogram**

- **Histogram** = chart plotting the distribution of cases in a dataset and their frequency; useful in visualizing a data distribution to determine an appropriate classification method

- **Mean, median, and mode:**
    - **Mean** = the arithmetic average of a set of values, or distribution
    - **Median** = the median of a finite list of numbers can be found by arranging all the observations from lowest value to highest value and picking the middle one
    - **Mode** = represents the most frequent value occurring in a sampling of a random variable

### Classification Methods
- **Natural Breaks or Jenks method**
    - Class breaks are set where there are jumps in values
    - Minimizes within-class variation, maximizes between-class variation
    - Good for plurimodal distribution
    - Good if there are ruptures in the distribution
    - Totally arbitrary
    - Can be done manually or with an algorithm (Jenks; good default method)
- **Equal-interval method (equal range)**
    - Places boundaries between classes at regular intervals
    - Results in an easy to interpret legend
    - May result in empty classes (influenced by extreme values)
- **Equal-count method (quantile)**
    - Places the same number of data values in each class
- **Standard Deviation method**
    - Attributes are placed in a class depending on how much they vary from the mean; final map is expressed in terms of standard deviations from the mean
    - Good for seeing which features are above or below an average value, and for displaying values that follow a normal distribution (bell-curve)
- **Unique method**
    - Class boundaries are set in accordance with external criteria

# Reading Notes: Mapping
- What is a map?
    - Put simply a map is a **representation of the world** (Ex: road map, mental map, etc.)

- Types of maps:
    - **Reference maps** = used to deliver location information to the map user, and generally represent geographic reality accurately (Ex: topographic maps, satellite maps, navigational maps)
        - The accuracy of a reference map is critical to its users who may include government agencies or organizations who need up-to-date information in order to inform their practices
    - **Thematic maps** = concerned with mapping a particular theme or topic geographically (Ex: suicide rate of each EU country, legal drinking age around the world, etc.)
        - The benefit of thematic mapping is that it can take abstract concepts like life expectancy and display them visually on a map for easy comparison
    - **Dynamic maps** = changeable or interactive representations of the earth, "dynamic" refers to it's interactivity and delivery on a variety of modern devices (Ex: online, smart phone, etc.)
        - Both reference and dynamic maps can be "dynamic" in nature

- Within the context of GIS, we can **overlay** multiple maps on top of each other to convey new information or provide spatial context
