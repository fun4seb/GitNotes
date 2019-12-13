---
tags: [Notebooks/SOCI212]
title: SOCI212 - Midterm Notes
created: '2019-10-18T20:50:43.254Z'
modified: '2019-10-23T21:22:12.725Z'
---

# SOCI212 - Midterm Notes

# Types of Variables and their Characteristics

* Variables could have the following characteristics:
  - Independent OR dependent
  - Discrete OR continuous
  - Nominal OR ordinal OR interval-ratio

## Independent & Dependent

* Basically **cause -> effect** relationship; **independent -> dependent**
  - Independant variable determines the state of the dependent variable. Example: level of heat applied when cooking meat (independent) -> time it takes for meat to reach medium-rare (dependent)

### Independent

> Independent ~ "cause" in a cause & effect relationship, **what we can control/manipulate**

### Dependent

> Dependent ~ "effect" in a cause & effect relationship, **what the result is**

## Discrete & Continuous

### Discrete

> Discrete ~ variable measured in units that cannot be subdevided

* Example: Number of children

### Continuous

> Continuous ~ variable measured in units that can be subdevided infinitely

* Example: Age, income, test score

## Nominal, Ordinal & Interval-Ratio

### Nominal

* Scores are labels only, **NEVER** numbers, and ALWAYS **descrete**

### Ordinal

* Scores have some numerical quality, can be ranked, and are ALWAYS **descrete**

### Interval-Ratio

* Scores are ALWAYS numbers, can be analyzed with a broad range of statistics, and can be **descrete** or **continuous**
  - Example: Number of brothers? **Descrete**
  - Example: Weight? **Continuous**

# Descriptive Statistics

1. Univariate ~ includes percentages, averages, and visual representation of data
  - Example: On average students have a GPA of **3.1**
2. Bivariate ~ describe the **existence, strength and direction** of the relationship between two variables
  - Example: **Older students** have **Higher GPAs**, **smoking** is linked to **lung cancer**
3. Multivariate ~ describe the relationships between three or more variables
  - Example: **Grades** increase with **age** for **females** but not **males**

# Frequency Distributions

* Summarizes the distribution of a variable visually by reporting the frequency in which each variable occured
* Categories of frequency distribution must be both exaustive and mutually exclusive (no overlap)

# Main Formulas

## Proportion

> Proportion = *f* / N

## Percentage

> Percentage = ( *f* / N ) * 100

## Ratios

> Ratio = *f1* / *f2*

* *f1* is number of cases in the first category
* *f2* is number of cases in the second category

## Rates

* Express the number of actual occurrences of an event (births, deaths, homicides) vs. the number of possible occurrences per some unit of time
  - Example: Crude death rate, birth rate

## Percentage Change

> Percentage Change = ( ( *f1* - *f2* ) / *f1* ) * 100

* *f1* is the **earlier** occuring frequency
* *f2* is the **later** occuring frequency
* Can be calculated with percentages, ratios and other values

# "Relatively Speaking"

* When prompted with "relatively speaking", it means being derived from some absolute numbers such as frequency, percentage, etc.
  - Compairing a **part** to a **whole** is a **proportion** or a **percentage**
  - Compairing a **part** to another **part** is a **ratio**
  - Measuring the change from one **part** to another **part** is a **percentage change**

# Measures of Central Tendency

1. Mode ~ most common score
2. Median ~ score of the middle case
3. Mean - average score

* Are 3 different statistics that report 3 different kinds of information however can all have the same value under certain cicumstances
* Measures of central tendency vary in terms of how they describe/define the centrality of the distribution; one may be more faithfully representative than another
* Another important measure is percentiles

## Mode

* Most common score
* Can be used with **all three levels of variables** (nominal, ordinal, interval-ratio)
* Most often used with nominal variables and is the **only** measure of central tendency usable with nominal variables

### Limitations

* Too many modes
* No mode
* Bi modal
* Mode shows most common but not most typical score

### Finding the Mode

1. Count number of times each score occured
2. The score that occured the most times is the mode

## Median

* Score of the middle case
* Exact center of the distribution of scores; score of the middle case
* Can be used with variables measured at **ordinal or interval-ratio** levels
  - Cannot be used with nominal level variables

### Finding the Median

* If N is odd: median = ( N + 1 ) / 2
* If N is even: median = average of N / 2 & ( N / 2 ) + 1 (basically the average of the 2 middle case because there is no singular middle case)

## Mean

* Average score
* Can usually only be used with variables measured at **interval-ratio** level however sometimes may be used with ordinal as well
  - Cannot be used with nominal level variables

### Finding the Mean

1. Calculate the summation of all the scores
2. devide that sum by the number of total cases

## Other Measures of Position

* Percentiles ~ point below which a specific percentage of cases fall
* Deciles ~ devides distribution into tenths
* Quartiles ~ devides distribution intro quarters

### Finding a percentile

1. Say N = 20 And we want to know the 55th percentile
2. Position = 20 (cases) * 0.55 = 11 (the 11thcase)
3. The 55th percentile is equal to the value of the 11th case
4. 55% of the cases fall below the 11th case
  - Example: Being in the 99th percentile for height means that 99% of the population is shorter than whatever the 99th percentile height is (ie: 6'3")

## Skewness in Central Tendencies

* Median and mean aim to provide the typical value in that they describe the centrality of the distribution
* One measure of central tendency may be more adequate given the shape of the distribution
  - When the distribution is fairly symmetrical; it does not include extreme cases (outliers), the mean and the median will give similar (if not identical) values
  - When the distribution is asymmetrical; it does include extreme cases (outliers):
    - The **mean** could be **misleading** (artificially pulled towards the extreme cases)
    - The **median** is the preferred measure of central tendency

> When a distribution is **"positively skewed"**, it means the mean is greater than the median
> When a distribution is **"negatively skewed"**, it means the mean is less than the median

# Measures of Dispersion

1. Index of qualitative variation (IQV)
2. Range
3. Interquartile Range
4. Standard Deviation

## IQV

* Rarely used
* Only measure of dispersion for nominal-level variables (informational, no need to calculate)
* Also used for variables grouped into frequency distribution

> “The IQV is essentially the amount of variation actually observed in a distribution of scores to the maximum variation that could exist in that distribution”

* IQV goes from 0.00 (no variation) to 1.00 (maximum variation)

## Range (R)

* Range (R) = highest score - lowest score
* Quick and easy and just shows the maximum span the distribution takes up
* Can be used with ordinal and interval-ratio level variables

### Limitations

1. Due to being made of the polar opposites it is distorted by outliers (high or low)
2. Provides no variation about the specific variation between the high and low scores

## Interquartile Range (Q)

* Avoids some problems of R by focussing on only the middle 50% of scores
  - Focusing on only the middle 50% disregards outliers and produces a more representative and typical view of the data
* The interquartile range is the difference between the first quartile (25th percentile) and the third quartile (75th percentile)

### Finding Q

> Interquartile Range (Q) = Q3 - Q1

1. First we are trying to find the range between the first quartile and the third quartile
2. To find the first quartile, multiply N (total number of cases) by 0.25. The first quartile is the case at that number slot counting up from the lowest
  - Example: N = 20, 20 * 0.25 = **5**; the first quartile is the score located at the fifth case
3. to find the third quartile, multiple N by 0.75. The third quartile is the case at that number slot counting up from the lowest
  - Example: N = 20, 20 * 0.75 = **15**; the third quartile is the score located at the fifteenth case
4. Now simply subtract the first quartile from the third quartile and thats your interquartile range!
  - Example: Q1 = 5, Q3 = 15, 15 - 5 = **10**; The interquartile range is ten!


## Standard Deviation

* Most important and common measure of dispersion
* Should be used with interval-ratio level variables but is also used with ordinal level variables
* Deviations represent the spread or dispersion between any scorein a distribution and the mean
* The **standard deviation** is the **average size** of all the deviations in the distribution and gives us an indication of how dispersed or how **much** variety is in the distribution, or how **little** variety

### Large vs Small Dispersion

* The standard deviation is a measure of density around the mean of a distribution.
* Clusters, gaps and extreme cases affect the standard deviation.
  - The **denser** the distribution, the **smaller** the deviation
  - The **sparser** the distribution, the **greater** the deviation

### Finding the Standard Deviation

* To calculate the standard deviation of a set of numbers:
  1. Work out the Mean (the simple average of the numbers)
  2. Then for each number: subtract the Mean and square the result
  3. Then work out the mean of those squared differences.
  4. Take the square root of that and we are done!


## In General...

* Deviation is **higher** with more **diverse** data
* Deviation is **lower** with more **homogeneous** data

## Skewness in Measures of Dispersion

* The skewness in a distribution also affects which measure of dispersion should be used to describe the variability in the distribution, just as skewness in a distribution affects which measure of central tendency should be used to describe the centrality of the distribution
* If the dsitribution is skewed:
  - The **median** is a better descriptor than the **mean**
  - The **interquartile range** is a better descriptor than the **range**
