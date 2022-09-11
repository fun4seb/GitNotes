# SOCI213 - Week 2

# Info
- Assignment must be typed and due next Monday

# Finishing Up Chapter 2: R^2
> Explained Variance ~ R^2 = 1 - (SSE/SST) = 1 - (123.68/398)

> R^2 x 100 = 0.68 x 100 = 68%

> Therefor 68% = impact of all x's (1-5) that contributes to y (100%)

> Unexplained Variance = 1 - R^2

> = 1 - .68 = .32 = other 32% that contribute to y (68% + 32% = 100%)

- R^2 **MUST NOT** exede +1

# Chapter 2: Final Example

## My Attempt
> Y = a + b1x1

> a = MOY - b1MOx1 = 13.2 - (1.34x3.06) = -22.704
	- The final sum is wrong, however the formula is correct, error in calculating as -22.704 should be 9.10

> Y = -22.704 + 1.34(x1)
	- This is incorrect as well due to above

> If x1 = 3 children then Y = -22.704 + 1.34(3) = -18.64
	- This is incorrect as well due to above

## Correct Attempt

> Y = a + b1x1

> a = MOY - b1MOx1 = 13.2 - 13.2(3.06) = 9.10

> Y = 9.10 + 1.34(x1)

# Chapter 3: Sampling
- Most important topic in statistics; cannot get real world statistics without some way of collecting data
- Most research is based on sampled surveys that make conclusions about the population because it is unreasonable to have to census the entire population which takes a lot of work and time to process
- An ideal sample is one that matches the population on every characteristic except the size, however this is unreasonable; because of this there are often errors of varying sizes called **sampling errors**

## Rules of sampling:
1. **Everyone in the population should have an equal chance of being selected**
2. The probability of any selection should be calculable
3. Selections ought to be independent of each other
4. Sample size should be acceptable
5. **Sample should reflect the characteristics of the population**

## Systematic Sampling
> Systematic Sampling ~ Selecting every Kth individual of the population using a skip interval

> Skip Interval (K) = population/sample
	- Ex: K = 2700/300 = 9

- Start by selecting the first case randomly and from there you select every Kth case forward and backwards until you get target sample size
- This sampling method breaks two rules:
	1. The independence of selections (rule #3; only starting point is independent of other cases, every Kth selection is then based off this point and therefor not independent)
	2. The representability of the characteristics (rule #5; possible to not accurately represent a population by skipping representative individuals)

## Cluster Sampling
- Does not respect first rule

## Convenience Sampling
- Sampling from a specific situation or environment and utilizes limited elements
	- Ex: Surveying people on the street or in a company cafeteria

## Stratified Proportionate Sampling
- Ideal; respects all 5 rules
- Selects sampling categories based on the proportions of the larger populations in relation to each other; stays insistent with ratios between sampling groups and ratios between population groups

## Calculating
1. Calculate proportions between population groups as a decimal integer out of 1.0
	- Ex: Population of departments: production = 1350, marketing = 900, management = 450	
	- -> Population proportions: production = 0.50, marketing = 0.33, management = 0.17
2. Then calculate sample size for each department based on proportions from 0 to 1.0 by multiplying total desired sample size by population of each department to scale the group down to proportionate sample size