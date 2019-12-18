# SOCI212 - Final Notes

## Final Exam Topics

- Bivariate table to measures of association
- Chapters 8-9, 13
  - **IGNORE** any reference to **statistical significance** and **hypothesis testing** in these chapters
  - Measures of association between nominal, ordinal, and interval-ratio variables
    - Calculations (formulas are provided)
    - Statistical calculations
    - Interpretation of results

## Question Format

- Part 1: multiple choice questions (35)
- Part 2: Short question (likely on scattergrams)
- Part 3: 2-4 calculation problems with interpretation (bring scientific calculator)

# Elaboration: Multivariate

- **RARELY** bivariate, almost always multivariate
  - In the real world things are determined by many factors, income for example is determined by many facotrs outside of hours worked, it could be determined by socio-economic background, level of education, gender, tax rates, etc.

# Measures of Association

## Association

- 2 variables are associated when they vary together, when one changes so does the other
  - This could mean either a **positive relationship** or **negative relationship**
- Positive relationship:
  - As one score rises so does another score
    - Ex: As length of residence within a country lengthens, so does ones level of fluency with the national language
- Negative relationship:
  - As one score rises or falls, another score does the opposite
    - Ex: As income rises for an individual, number of days spent hungry lowers

- Association can be important evidence for causal relationships, particularly if the association is strong
- **Correlation and Causality doesnt/shouldnt imply proof**
  - While there may be evidence (strong) that a phenomena causes an effect, it is only evidence of causation and not proof

### Direct Relationship

- In a **direct** relationship, the control variable (Z) has little to know effect on the relationship between X & Y
- The column %'s and gammas in the partial tables are about the same as the bivariate table
  - This outcome supports the argument that **X causes Y**

### Other Possible Relationships Between X, Y, and Z

- **Spurious** relationship (also called explanation):
  - X and Y are not related, both are **caused** by Z (X <- Z -> Y)
- **Intervening** relationship (also called interpretation):
  - X and Y are not directly related but are **linked** by Z (X -> Z -> Y)
- **Interaction** (also called specification):
  - The relationship between X and Y changed for each value of Z (Y <- Z1 <- X -> Z2 -> 0)

- The partial tables look the **same** for spurious and interveneing relationships but for very different causal reasons

## Prediction

- If variables are associated, the score on one variable can be predicted from the score of another variable
- The **stronger** the association, the more **accurate** the prediction

## Association and Bivariate Tables

- Association between 2 variables... (bivariate associations)
  - Are best illustrated with bivariate tables
  - Can be investigated by finding answers to three questions:
    1. Does an association **exist**?
    2. How **strong** is the association?
    3. What is the **pattern or direction** of the association?

## Limitation of Elaborating Bivariate Tables

- Basic limitation: sample size
  - Greater the number of partial tables, the more lively to have cells with low to zero frequencies
- Potential solutions:
  - Reduce number of cells by collapsing categories (recoding)
  - Use a much larger sample size

## Nominal Level Measures of Association

- For nominal level variables there are 2 commonly used measures of association:
  - Phi
  - Cramer's V
  - Lambda

### Decision Tree: What Method to Use?

- If 2x2 table and...
  - Chi-square based measure of association -> use **Phi** OR
  - PRE measure of association -> use **Lambda**
- If greater than 2x2 and...
  - Chi-square based measure of association -> use **Cramer's V** OR
  - PRE measure of association -> use **Lambda**

### Phi

### Cramer's V

### Lambda

> Lambda = (E1 – E2) / E1

- Lambda provides us with an indication of the strength of the relationship between independent and dependent variables
- To calculate lambda, you need two numbers: E1 and E2.
  1. E1 is the error of prediction made when the independent variable is ignored. To find E1, you first need to find the mode of the dependent variable and subtract its frequency from N. E1 = N – Modal frequency.
  2. E2 is the errors made when the prediction is based on the independent variable. To find E2, you first need to find the modal frequency for each category of the independent variables, subtract it from the category total to find the number of errors, then add up all the errors.
  3. 

## Ordinal Level Measures of Association

### Gamma

> Gamma = (Ns - Nd)/(Ns + Nd)

- **Can only use Gamma if the variables are ORDINAL**
- In addition to **strength**, gamma also identifies the **direction** of the relationship
- In a **negative** relationship between authoritarianism and depression symptoms:
  - as authoritarianism increases, depression symptoms decrease
- In a **positive** relationship between authoritarianism and depression symptoms:
  - as authoritarianism increases, depression symptoms increase

#### Limitations of Gamma

- Because gamma can "exaggerate" the actual strength of the relationship, other odinal measures that take ties into account, such as **Kendall's tau-b, Kendall's tau-c**, or **Somer's d**, should be used instead

### Kendall's tau-b and Kendall's tau-c, Somer's d

- Kendall's tau-b includes pairs tied on the independent variable, t(x), and pairs tied on the dependent variable, t(y)
  - Kendall's tau-b ranges between +-1.00 and should only be used when both the independent and dependent varaibles have the **SAME** # of categories
  - Kendall's tau-c also ranges between +-1.00 and is used as an alternate to tau-b when the variables have an **UNEQUAL** # of categories
- Somer's d includes only pairs tied on the dependent variable, t(y)

## Interval-Ratio Measures of Association

### Scattergrams

#### Definition

- Graphs that display the relationship between 2 interval-ratio variables
- **First step** in assessing a relationship between 2 interval-ratio variables
- Inspection of the scattergram should always be the first step in assessing the correlation between two I‐R variables
- The scattergram provides a first impression about:
  - The **existence** of a relationship
  - The **strength** of a relationship
  - The **direction** of a relationship

#### Anatomy of a Scattergram

- Scattergrams have 2 dimensions:
  1. The X (independent) variable is arrayed along the horizontal axis
  2. The Y (dependent) variable is arroayed along the verticle axis
- The dot is placed at the intersection of the case's scores on X & Y
- Each **dot** on the scattergram is a **case**

> Pattern of Dots ~ summarizes the relationship between 2 variables
> Regression Line ~ come as close as posible to the dots

#### Regression Line

- The regression line indicates strength and direction of the linear relationship between 2 variables
  - The greater the extent to which the dots are clustered around the regression line, the stronger the relationship
- Regression line = **prediction line**

### Pearson's r

- Correlation = degree of association between 2 variables
  - Correlation lies with respect to **strength**
  - Correlation lies with respect to **direction**
- If the value of the correlation coefficient varies from -1.00 to +1.00...
  - Perfect negative (-1.00) and perfect positive (+1.00) associations
  - Provides a measure of how scores on X and Y are scattered throughout the range of possible scores
- If the value of the coefficient is equal to 0...
  - No association between the variables

### Coefficient of Determination

- Coefficient of determination represents the proportion of variation in a dependent variable that is explained by the independent variable
- It can also be interpreted in terms of the **proportional reduction of error** in predicting a dependent variable (Y)
  - Taking into account scores on the independent variable (X) when trying to predict scores on the dependent variable (Y)
  - Rather than ignoring scores on the  independent variable (X) when trying to predict scores on the dependent variable (Y)
- Provides a **more** direct and **less** arbitrary interpretation than r
