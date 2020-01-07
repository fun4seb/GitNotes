# SOCI213 - Week 1

# Chapter 1: Summary of Descriptive Statistics

## I: Research Process and the Types of Statistics

### Stage 1: State the research question
- The question must be clear and precise, and should help narrow the scope of the research as much as possible

### Stage 2: Literature Review
- The literature review has two specific purposes: to select the variables and to formulate the hypothesis

### Stage 3: Construct the Research Design
- The research design consists of several tasks:
	1. Choose a research method: a census or a survey
	2. Choose an appropriate sampling procedure
	3. Choose an instrument of data collection
	4. Develop the chosen instrument of data collection

### Stage 4 Data Collection

### Stage 5: Data Analysis
- Applying two types of statistics: **descriptive & inferential**. Descriptive statistics are used to describe the sample; whereas inferential statistics are used to generalize the sample findings to the population from which the sample was drawn

## II: Types of Variables: Levels and Scales of Measurments
- By definition, a variable is a characteristics that varies from ne person to another or from one element to another such as gender, age, color, etc...
- The first distinction we can make is between two types of cariables: **Independent & Dependent**. The independent variable is considered to be the cause and the dependet variable is the effect. Variables are also distinguished in terms of their level of measurment; **There are four levels of measurments**.

- Nominal scores can be:
	- Classified
	- **ALWAYS DESCRETE**
- Ordinal scores can be:
	- Classified
	- Rank-ordered
	- **ALWAYS DESCRETE**
- Interval scores can be:
	- Classified
	- Rank-ordered
	- Subtracted from each other
	- **EITHER DESCRETE OR CONTINUOUS**
- Ratio scores can be:
	- Classified
	- Rank-ordered
	- Subtracted from each other
	- Divided by each other
	- **EITHER DESCRETE OR CONTINUOUS**

### Scales of Measurments
- There are two types of measurments: **discrete & continuous**
- Nominal and ordinal variables can only have a discrete scale
- Interval and ratio variables can have one or the other.
- A discrete scale consists of finite or whole numbers such as the number of dependent children at your home; You cant have 1.25 kids
	- **Discrete means it CANNOT be subdivided**
- A continuous scale consists of numberswith decimal values such as "Age", which can be expressed in fraction of a year
	- **Continuous means it CAN be subdivided**

## III: Statistics Applied to Univariate Variables
- Measures of Central Tendency
	1. Mode
	2. Median
	3. Mean
- Position
	1. Quartile
	2. Decile
	3. Percentile
- Variation
	1. Range
	2. Variance
	3. Standard deviation

## IV: Measures of Association & their Characteristics
- There are **positive & negative** associations

### Nominal Measures of Association

### Ordinal Measures of Association

## V: Elaborating bivariate association: Introducing control variables
- The reason for introducing a third variable (Z) to the association between X & Y is to determine:
	- Whether the association between X & Y is statistical or causal; and
	- The type of variable is Z

## VI: Bivariate Correlation & Regression
- Utilize a scatter plot to visualize regression and correlation
- Direction of regression line determines **positive/negative** correlation
	- Positive correlation = +slope
	- Negative correlation = -slope

# Chapter 2: Multiple Correlation and Regression

## Multivariate or Multiple Regression
> Multiple Regression ~ The extension of simple regression. It helps explain and predict the variation of one dependent variable using more than one independent variable

- Ex: Determining correlation between Y (# of crimes/month) and several X variables (Unemployment rate, average # of children/family, average income $, population density, average age in years)

### Example 1: Determining Crimes/Months (y) From x1-5
MO = mean of...
> y = a + b1x1 + b2x2 + b3x3 + b4x4 + b5x5
> a = MOy - [b1MOx1 + b2MOx2 + b3MOx3 + b4MOx4 + b5MOx5]
>   = 15 - [1.80(9) + 1.14(3) - .00015(18000) + .008(200) - .20(29)]
> 	= 15 - 12.72 = 2.28
> y = 2.28 + 1.80x1 + 1.14x2 - .00015x3 + .008x4 - .20x5

- Explain variation in Y, using all 5 X's
- Predict y, knowing all 5 x's
- a = 2.28; If all 5 x's = 0, y = 2.28 crimes/month

> b1 = 1.80 -> if x1 increases by 1%, y increases by 1.80 crimes/month, holding all other x's constant
> b2 = 1.14 -> if x2 increases by 1 child, y increases by 1.14 crimes/month, holding all other x's constant
> b3 = -.00015 -> if x3 increases by $1000, y decreases by .15 crimes/month, holding all other x's constant
> b4 = .008 -> if x4 increases by 100 people, y increases by 0.8 crimes/month, holding all other x's constant
> b5 = -.20 -> if x5 increases by 10 years, y decreases by 2 crimes/month, holding all other x's constant

> y - 2.28 + 1.80(10) + 1.14(3) -.00015(15000) + .008(250) -.20(25) = 18.45 crimes/month