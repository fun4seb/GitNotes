# GEOG260 - Week 6: Data & Maps

# Data
- **Qualitative** = describes quality (what kind)
    - Nominal
- **Quantitative** = quantify a problem (how much)
    - Ordinal
    - Interval
    - Ratio

## Data Categories
- **Primary sources vs. secondary sources**
    - Primary data = data collected by hand/yourself
    - Secondary data = data collected by others (Ex: census data)

- **Metadata** = data about the Data
    - In the context of maps, it comes in the form of attribute tables/"excel files"
    - Headers, rows, and fields

## Data Quality (Precision & Accuracy)
- **Precision vs. accuracy** (using dartboard metaphor)
    - If the darts hit the same spot, but that spot is not the desired location (center), the darts were **precise, but not accurate**
    - If the darts generally hit towards the center but were not in the same spot, the darts were **accurate but not precise**
    - If the darts hit the center AND are in the same spot, the darts were **accurate AND precise** (best)

### Errors in Precision & Accuracy
- **Errors (specifically in GIS) can be due to inaccuracies in these 5 categories:**
    1. Positional errors
    2. Attribute errors
    3. Temporal errors
    4. Logical errors
    5. Comprehensiveness errors
    - **This means that accuracy and precision in maps is dependent on these 5 characteristics being as correct as possible**

- **Positional errors can be due to:**
    - Input errors (the wrong data has been recorded)
    - Physical errors (physical changes in the medium the map is on; more relavent to print maps as paper/ink can warp, stretch, and fade over time)
    - Conversion errors (Ex: if datums are not converted corrected)
    - Vagueness in position (Ex: Where 2 biomes meet is not always a clear-cut line)

- **Attribute errors can be due to:**
    - Errors in the quality of the **metadata** (basically how accurate and clear is ALL the data as a whole)

- **Temporal errors can be due to:**
    - Not using the most up-to-date, punctual data
    - Not revising the map over time; data and maps change of time and must be updated as such to maintain their accuracy

- **Logical errors can be due to:**
    - Are all the underlying layers of a map in **alignment** in relation to their reference points

- **Comprehensiveness errors can be due to:**
    - Errors in the comprehensiveness/effectivity of the dataset as a whole
    - Does the map accomplish what you set out to accomplish; is it accurate/clear at every step of the way
    - Did the map-maker show integrity in the creation of the final outcome

# Statistics
- **Descriptive vs. inferential statistics**
    - Descriptive statistics **describe things**
    - Inferential statistics **allow you to make predictions about things**
    - **In mapping we do both**

## Levels of Measurement
- **4 main levels of measurement**
    1. Nominal = no implied order
        - Naming/labeling things into separate categories without overlap (Ex: ethnicity, marriage status, gender, etc.)
        - Words/numbers that are not ordered or mathematical; least precise data type
        - **Qualitative**
    2. Ordinal = order but not metric
        - Categorical data that can be ordered (Ex: small, medium, large)
        - **Quantitative**
    3. Interval = measurable distances/differences
        - Numerical data with an **arbitrary zero point** (Ex: temperature, age, test scores, etc.)
        - Similar to ordinal, but with categories being rankable according to numerical differences in the data
        - **Quantitative** and **additive** (dealing with differences between points that are always constant)
    4. Ratio = measurable in relation to true zero
        - Numerical data with a **fixed zero point** (Ex: height, weight, kelvin)
        - **Quantitative** and **multiplicative** (dealing with multiples/ratios of previous points)

- **Selecting which level of measurement to use:**
    - If dealing with something **categorical**, you can use: nominal, ordinal, interval, or ratio
    - If dealing with something based on **rank**, you can use: ordinal, interval, or ratio
    - If dealing with something based on the **space between points**, you can use: interval or ratio
    - If dealing with something with a **fixed zero point**, you can use: ratio

- **"The difference between interval and ratio scales comes down to their ability to dip below zero"**
    - "A ratio variable has all the same properties of an interval variable, but also has a clear definition of zero. When the variable equals zero there is none of that variable"

## Discrete vs. Continuous Data
- **Discrete data** = individual data points; where each **exact value** is plotted (Ex: 13, 14, 15, 17, 21, 88)
- **Continuous data** = ranges of data points; where **ranges of values** are plotted (Ex: 13-15, 17-88)

- **Visual data** (on maps) can also be plotted in either a discrete or continuous form (Ex: plotting the location of each instance of oil spill is discrete, however drawing an area/polygon where oil spills occur is continuous)

- Other names for these concepts are **isolated (discrete)** vs. **interpolated (continuous)**

## Classifying Data
- A set of many discrete data points can be classified and grouped/divided to create continuous ranges of data

- **Why classify data?**
    - Helps you simplify large datasets into something more readable
    - A way of identifying patterns in the dataset
    - Allows for continuity so you can compare between classes
    - Lets you see differences/similarities

- **Classifying discrete data into continuous can be done in many different ways:**
    - Unclassified (kept as discrete)
    - Manual (arbitrarily dividing the discrete data points into groups manually)
    - Natural breaks
    - Equal interval/ranges
    - Quantile/equal count
    - Standard deviation

- **Criteria that can assist in selecting a classification scheme:**
    - The public (goal of the map)
    - The data distribution
    - Ease of understanding the map
    - Ease of understanding the legend
    - Ease of computation

- **Determining the number of classes (groups of discrete data) is based on:**
    - The public/viewer (Ex: Experts viewing the data = higher number of classes)
    - The volume of data (subjects)
    - The type of data (Ex: if it changes over time)

- **Guidelines for determining number of classes:**
    - Less than 20 subjects = 3 or 4 classes
    - From 20-30 subjects = 4 or 5 classes
    - From 30-50 subjects = 4 to 6 classes
    - From 50-100 subjects = 5 to 7 classes
    - Greater than 100 subjects = 5-8 classes

### Determining the Classification Scheme
- In order to determine the classification scheme you must first understand the distribution of data, this starts with the creation of a **histogram** based on the data
- Through organizing the data into a histogram, the **bins** (groups of frequencies) can then be organized according to the various classification schemes and ascribed visual values to be plotted on a map

- **Natural-breaks scheme**
    - Classes are based on **natural groupings inherent to the data**
    - You (or software) identifies break points by picking the class breaks that best group similar values and maximize the differences between classes
    - The features are divided into classes whose boundaries are set where there are **relatively big jumps in the data values**

- **Equal interval/range scheme**
    - Divides the range of attributes into **equal-sized sub-ranges**, allowing you to specify the number of intervals (Ex: a ranging from 0-300 with 3 classes will have equal interval ranges from 0-100, 101-200, 201-300)
    - Emphasizes the amount of an attribute value relative to others
    - Best applied to familiar data ranges such as size, percentages, and temperature
    - Based on the **range (R)** of the distribution (R = max-min), divided by the number of **classes (C)**, to obtain the **extent (E)** of each class; add this extent to the minimal value (min + E) to get the upper limit of the first class, repeat etc.

- **Quantile/equal count scheme**
    - Each class contains an **equal number of features**
    - A quantile classification is good for linearly distributed data
    - Similar features can be placed in adjacent classes, or features with widely different values can be put in the same class so the resulting map can be misleading
    - Minimize distortion by increasing the number of classes
    - Based on the number of **items (I)**, divided by the number of **classes (C)**, to obtain the **number (n)** of subjects in each class; **n = I/C**, count n (starting from the minimal value) to get the upper limit of the lower class

- **Standard deviation scheme**
    - This classification scheme shows you **how much a feature's attribute value varies from the mean**
    - Calculate the mean and the standard deviation from the mean
    - Class breaks are then created using these values
    - Classic "bell curve"