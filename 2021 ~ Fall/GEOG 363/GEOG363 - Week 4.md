# GEOG363 - Week 4: Attribute Data & Analysis
- Geographic data is represented by:
    - Spatial data
    - **Attribute data**
        - Describes the characteristics of spatial features; the "what"
        - Two major types: textual or alphanumerical
        - Attribute data is organized in a table; each row (record) represents a (spatial) object, and each column (field) describes a characteristic of that object
        - Managed by a Database Management System (DBMS) or a Relational DBMS (RDBMS)

# The Relational Database
- **The relational database** = a collection of tables (relations) where objects occurring between them are linked according to their unique ID
    - Allows to organize, update and interrogate data
    - **Has tables that are defined for each class of objects**
    - Each table can be managed separately from other tables, but can be connected when needed (Ex: for queries)
    - This type of structure is common in other information management systems
    - These tables could be connected to other tables (Ex: Architects table)
    - Only one value per cell
    - No significance to row, column sequence
    - Contains keys
    - Can perform relations on tables

- **Unique ID (key):**
    - The connection between the tables is made through a key
    - A key (or ID) is a common field whose values can **uniquely identify a record in a table**
    - Each key value is unique (numerical)
    - Can be multiple keys (primary and secondary) in a tuple (or row)
    - Keys can not have missing values
    - The Feature ID (FID) is a particular type of key: links spatial data with attribute data

- **Columns, Attributes, Fields:**
    - All Column values about the same subject and of the same type (Ex: integer, real, char)
    - Each column has a unique name

- **Rows, Records, Tuples:**
    - Set of facts that are related to each other
    - Supposed to be unique sets
        - Ex: no two tuples can have identical values for all their attributes
        - Rows are uniquely identified by a key value

- **Relationship types between objects in related tables:**
    - One-to-one:
    - One-to-many:
    - Many-to-many:

- **Relational database summary:**
    - Tables:
        - Are defined for each class of objects (e.g. table building, architect)
        - Contain keys; A key (or ID) is a common field whose values can uniquely identify a record in a table
        - Have only one value per cell
    - Columns:
        - Values are of the same type (e.g. integer, real, char)
        - Titles are unique
    - Rows:
        - no two rows can have identical values for all their attributes

# Measurement Levels
- **4 measurement levels for attribute data:**
    1. **Ratio** (ratios exist; fixed zero point)
        - There is a natural zero starting point and ratios are meaningful
        - Zero is absolute (there is an absence in value)
        - Ex: Salary, commuting distance
    2. **Interval** (distance exists, but no ratios; arbitrary zero point)
        - Differences are meaningful, but there is no natural zero starting point and ratios are meaningless
        - Zero is arbitrary (zero does NOT mean an absence in value)
        - Ex: Temperature
    3. **Ordinal** (ordering exists, but not distance; ranked categories)
        - Categories are ordered, but differences cant be found or are meaningless
        - Ex: Type of car (compact, mid-size, full-size)
    4. **Nominal** (no ordering; unranked categories)
        - Categories only, data cannot be organized into an ordering scheme and thus impossible to draw direct comparisons between objects; qualitative
        - Ex: residential, commercial, industrial zones

## Measurement Level Symbology Rules
- **Nominal map symbology rules:**
    - **Point:** different shapes and/or hues, and not different sizes
    - **Line:** vary only in pattern and/or hue, not in thickness
    - **Area:** only different area hues or patterns should be used, and not different values of selected hues

- **Ordinal map symbology rules:**
    - **Point:** geometric shape or a pictorial symbol; Variation of size, color or both color and size for emphasis
    - **Line:** rank data by line weight, style, or hue. Any combination of these methods is possible
    - **Areas:** can show quantitative differences in data by different hue/color value, and pattern fills. For further emphasis, patterns can also be in different colors

- **Interval/Ratio map symbology rule:**
    - **Point:** various colors, shapes, and size may be used (Ex: graduated dots, circles, squares, bars, block piles, pie charts)
    - **Line:** can be graduated. Contours are the most common form of this line symbol (elevation value and position & calculation of slope)
    - **Area:** can use variations in color value and pattern to show a gradual progression of data values

# Attribute Analysis
- GIS allows us to **answer questions related to the attributes of spatial data:**
    - Ex: Which city has the highest income? The largest population density?; Where are all the features that meet the following criteria?

- GIS allows us to **retrieve information about an entity or feature based on:**
    - One or more attribute(s) of an entity (Ex: average income per census tract; census data)
    - One or more attribute (s) of multiples entities that overlap in space (Ex: English speaking population that lives close to metro station; census data & metro data)

## Attribute Tables
- Attribute:
    - Value associated to geographical object
    - Value describing geographical object

- Attribute table: organized by row and column (georelational)

- Two types of attribute table:
    - Feature attribute table
        - Access to spatial data
        - Feature ID: link to a feature's geometry (georelational)
        - Required
    - Non-spatial attribute table
        - Stores additional information (Ex: population per polygon)
        - One common field with the feature attribute table (ID)
        - Not required

- **Tables are linked through an ID (field)**
    - This "linking" is what makes this a **relational** database
    - One ID for each geographic feature
    - Identifier (ID) is **numerical**
    - Each ID is **unique**
    - Limit redundancy and duplication
    - **NOTE: tables cannot be linked through the FID**

### Join and Relate Tables
- **Join:**
    - Consists in appending the attributes from one table into the other based on a common key field (Ex: joining two tables by ID's)
    - Can be used to join a non-spatial table(s) to a georeferenced feature attribute table
    - Recommended for one-to-one or many-to-one relationships

- **Relate:**
    - Consists in defining a relationship between two tables (also based on a common field) but without appending the attributes of one to the other
    - Recommended for one-to-many or many-to-many relationships
    - Slow down data access

# Querying the Database
- **Query** = inquiry, question; In GIS: retrieve and display features that meet specific criteria

- A query is an operation **(Select)** that allows us to:
    - Retrieve a subset of a total number of records
    - Uses a common language: **SQL (Structured Query Language)**
        - Created by IBM in the 70's
        - Designed for RDBMS
        - Combine **Map Algebra operators**
        - Most common language in the domain of databases
        - Powerful language to isolate, count and locate individual
        - Generate alphanumerical AND geographical requests

- Can also use **(Find)** as a simple way to retrieve attribute data
    - From attribute data table
    - From the geographic features
    - Little value for spatial analysis

- **Two forms of restricted operations:**
    - **Attribute** (non-spatial) queries
        - Ex?
    - **Spatial queries**
        - Ex: "Select all garbage dumps within 5 km of a rive"

## Map Algebra Operators for Querying
- Basic structure in SQL **(syntax)** is:
    - Select: <attribute>; Ex: * (select all columns)
    - From: <database>; Ex: ContaminatedSites
    - Where <condition>; Ex: "Toxicity" > 8
    - Ex: **Select** * (=all columns) **From** ContaminatedSites **Where** "Toxicity" > 8

- **Usable algebra operators:**
    - **Logical operators:** =, >, <, >=, <=, <>
        - Ex: "Toxicity" > 8
    - **Arithmetic operators:** +, -, x, /, ^
        - Ex: "POP2001"/"AREA"
    - **Boolean operators:** AND, OR, NOT, XOR
        - AND: intersection of 2 sets (Belong to A and B)
        - OR: Union of 2 sets (belong either to A or B)
        - XOR: Exclusive OR (Belong to A or B but not both)
        - NOT: Difference operator (belong to A but not to B)
        - Can be used for attribute OR spatial selection
    - **Mathematical functions** (Ex: trigonometric functions, logarithms, etc.)

## Query Building
- In ArcGIS use quotation mark (“) for field names, apostrophe for text (‘) and nothing for numbers

- Use equal (=) or different (<>) to select features or string values:
    - Ex: “PROV” = ‘QC’
    - Ex: “PROV” <> ‘QC’

- Use logical operators (e.g. >), to select string values based on sorting order:
    - Ex: “POP2001” > “POP2006”
    - Ex: “POP2001” >= 500
    - Ex: “DISTRICT_NAME" > 'M’

- Use **LIKE** to build a partial string search
    - If you are querying a shapefile:
        - ' _ ' indicates one character
            - Ex: [OWNER_NAME] LIKE ’_ atherine smith‘
        - ' % ' indicates any number of characters
            - Ex: [STATE_NAME] LIKE 'Miss%'
    
- Queries are evaluated from according to standard operator precedence rules. Expression enclosed in parentheses is evaluated before the part that isn't enclosed
    - For example: "HOUSEHOLDS" > "MALES" * "POP90_SQMI" + "AREA“ 
    - is evaluated differently from: "HOUSEHOLDS" > "MALES" * ("POP90_SQMI" + "AREA")
    - **General rules of BEDMAS apply**

## Spatial Queries
- Spatial queries are queries that are made to select objects according to their spatial location in relation to other objects
    - Ex: Querying all zones with 200 m of a train station; querying based on the spatial relation of something to something else

- **Select by Location** = lets you select features from one or more layers based on where they are located in relation to the features in another layer
    - Ex: select features from table "Restaurants" that "are within a distance of" 1 km to the features in table "Food distributors"; find **restaurants** within **1 km** of **food distributors**

## Queries Summary
- Data stored in a GIS are explored through **Querying**
    - Queries: An input **(SQL syntax)** to the computer that aims to retrieve data from a database

- **Purpose:**
    - Explore the data
    - Focus on a data subset of interest