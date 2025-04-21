---
layout: default
title: Final Exam Study Guide
---

# PSY 330 Final Exam Study Guide

This comprehensive guide covers the core concepts, statistical tests, interpretation skills, and data analysis procedures for your PSY 330 Statistical Methods final exam. It's organized according to the course modules (M1-M7) while emphasizing critical thinking and understanding the "why" behind statistical procedures.

## I. Core Statistical Concepts (Module 1)

### Descriptive Statistics

- **Measures of Central Tendency**:

  - **Mean**: Average of all values (sum of values divided by number of values)
  - **Median**: Middle value when data is arranged in order (less affected by outliers)
  - **Mode**: Most frequently occurring value

- **Measures of Dispersion**:
  - **Standard Deviation**: Average distance of each value from the mean
  - **Variance**: Square of the standard deviation, measures spread of data

### Normal Distribution

- **Definition**: Bell-shaped, symmetrical distribution with specific properties
- **Characteristics**:
  - Mean = Median = Mode
  - Symmetrical around the mean
  - 68% of data falls within ±1 SD of mean
  - 95% of data falls within ±2 SD of mean
  - 99.7% of data falls within ±3 SD of mean

### Z-Scores

- **Definition**: Number of standard deviations a score is from the mean
- **Formula**: z = (X - μ) / σ (or z = (X - M) / SD for samples)
- **Uses**:
  - Standardize scores from different distributions
  - Determine relative position within a distribution
  - Calculate probabilities using the standard normal distribution

### Hypothesis Testing

- **Null Hypothesis (H₀)**: Statement of no effect, no difference, or no relationship
  - Example: "There is no difference in the mean number of hours of sleep between men and women"
- **Alternative/Research Hypothesis (H₁ or Hₐ)**: Statement of an effect, difference, or relationship
  - **Directional**: Specifies the direction of the effect (e.g., "There is a positive relationship between the number of hours of sleep and happiness")
  - **Non-directional**: States a difference exists but not the direction (e.g., "There is a difference in the mean number of hours of sleep between men and women")

### Significance & Errors (Module 2)

- **Alpha (α) Level**: Probability threshold for rejecting H₀ (typically .05 or .01)
  - Represents acceptable risk of Type I error
  - Lowering alpha (e.g., .05 to .01) makes it harder to find significance
- **p-value**: Probability of obtaining observed results (or more extreme) if H₀ were true
  - If p ≤ α: Reject H₀ (Statistically significant result)
  - If p > α: Fail to reject H₀ (Not statistically significant)
- **Type I Error**: Rejecting a true null hypothesis (false positive). Probability = α
- **Type II Error**: Failing to reject a false null hypothesis (false negative). Probability = β
- In simple terms, a Type I error is when you reject a true null hypothesis, and a Type II error is when you fail to reject a false null hypothesis, for example, when there is a relationship between the number of hours of sleep and happiness, but you fail to reject the null hypothesis that there is no relationship. And a Type II error is when you fail to reject the null hypothesis that there is no relationship between the number of hours of sleep and happiness, when there is actually a relationship.

- **Sampling Distribution**: Distribution of sample statistics (like means) if many samples were taken
- **Standard Error of the Mean**: Standard deviation of the sampling distribution of means
- **Central Limit Theorem**: As sample size increases, the sampling distribution of means approaches normal distribution regardless of the population's distribution

### Research Designs

- **Between-Subjects**: Different participants in different conditions
  - Used for: Independent-samples t-tests and between-subjects ANOVAs
- **Within-Subjects (Repeated-Measures)**: Same participants measured under all conditions
  - Used for: Paired-samples t-tests and repeated-measures ANOVAs
  - Example: Cornbread rating 1 vs. 2; Before vs. After medication
  - **Advantage**: Reduces error variance, increasing statistical power
  - **When to avoid**: When testing pre-existing groups or when carryover effects are likely
- **Factorial Design**: Two or more Independent Variables (Factors)
  - Examines: Main Effects and Interactions
- **Experimental vs. Quasi-Experimental**:
  - **Experiment**: Researcher manipulates IV and uses random assignment
  - **Quasi-Experiment**: Uses pre-existing groups or lacks random assignment
  - Key distinction: Only experiments allow for strong causal conclusions

### Variables & Measurement

- **Independent Variable (IV)**: Variable manipulated/categorized by researcher (presumed cause)
- **Dependent Variable (DV)**: Variable measured by researcher (presumed effect)
- **Predictor Variable**: Used in regression/correlation (similar to IV)
- **Criterion/Outcome Variable**: Used in regression/correlation (similar to DV)

- **Levels of Measurement**:
  - **Nominal**: Categories with no order (e.g., gender, marital status)
  - **Ordinal**: Categories with meaningful order.
  - **Scale** (Interval/Ratio): Continuous measurements with equal intervals
  - **Important**: Most statistical tests (t-tests, ANOVA, Correlation, Regression) require scale DVs

## II. t-Tests (Module 3)

### Z-Test

- **Purpose**: Compare a sample mean to a known population mean when population standard deviation is known
- **Requirements**:
  - Population standard deviation (σ) must be known (rare in practice)
  - Sample size should be large (n > 30) if population not normal
- **When to Use**: When you have complete information about the population parameters
- **Formula**: z = (M - μ) / (σ / √n)
- **Interpretation**: Similar to t-test, but uses z-distribution for critical values

### One-Sample t-Test

- **Purpose**: Compare a sample mean to a known or hypothesized population mean
- **Requirements**:
  - Population standard deviation (σ) is unknown (uses sample SD instead)
- **Key SPSS Steps**:
  1. Analyze → Compare Means → One-Sample T Test
  2. Move variable to "Test Variable(s)"
  3. Enter test value (hypothesized population mean)
- **APA Reporting**:
  - Format: t(df) = [t-value], p = [p-value], d = [Cohen's d value]
  - Example: t(24) = 2.68, p = .013, d = 0.54

### Independent-Samples t-Test

- **Purpose**: Compare means of two independent groups
- **Requirements**:
  - One categorical IV with exactly 2 levels (groups)
  - One continuous DV
  - Independent observations
- **Key SPSS Steps**:
  1. Analyze → Compare Means → Independent-Samples T Test
  2. Move DV to "Test Variable(s)"
  3. Move IV to "Grouping Variable"
  4. Define groups (specify values that define the two groups)
- **Interpretation**:
  - Check Levene's test for equality of variances first
  - Use appropriate row of t-test results based on Levene's test
  - Significant result: Groups differ significantly on the DV
- **APA Reporting**:
  - Format: t(df) = [t-value], p = [p-value], d = [Cohen's d value]
  - Example: t(46) = 3.27, p = .002, d = 0.95

### Paired-Samples t-Test

- **Purpose**: Compare means of two related measurements (same participants measured twice)
- **Requirements**:
  - Two measurements of the same continuous variable
  - Measurements are from the same participants or matched pairs
- **Advantages over Independent-Samples t-Test**:
  - Reduces error variance due to individual differences
  - Typically has more statistical power
- **Key SPSS Steps**:
  1. Analyze → Compare Means → Paired-Samples T Test
  2. Select pairs of variables for analysis
- **APA Reporting**:
  - Format: t(df) = [t-value], p = [p-value], d = [Cohen's d value]
  - Example: t(19) = 4.52, p < .001, d = 1.01

### Between-Subjects vs. Within-Subjects Designs

- **Between-Subjects (Independent Groups)**:
  - Different participants in different conditions
  - Advantages: No order or practice effects
  - Disadvantages: Requires more participants, more influenced by individual differences
- **Within-Subjects (Repeated Measures)**:
  - Same participants in all conditions
  - Advantages: Controls for individual differences, requires fewer participants
  - Disadvantages: Potential carryover effects, practice effects, fatigue

## III. Module 4: ANOVA

### One-Way ANOVA

- **Purpose**: Compare means of three or more groups
- **Requirements**:
  - One categorical IV with 3+ levels
  - One continuous DV (scale measurement)
  - Independent observations
- **Key Assumption - Homogeneity of Variances**:
  - Test with Levene's test
  - If p > .05: Assumption met (variances are similar)
  - If p ≤ .05: Assumption violated (consider alternative tests)
- **Key SPSS Steps**:
  1. Analyze → Compare Means → One-Way ANOVA
  2. Move DV to "Dependent List" and IV to "Factor"
  3. Options → Check "Homogeneity of variance test"
  4. Post Hoc → Select appropriate test based on Levene's results
- **Interpreting Results**:
  - **Main ANOVA table**: Look for F-statistic, degrees of freedom (df), and p-value
  - **Effect Size**: Calculate η² = SS_between / SS_total
    - Small: ~.01 (1% variance explained)
    - Medium: ~.06 (6% variance explained)
    - Large: ~.14 (14% variance explained)
- **Post-Hoc Tests**:
  - When needed: When overall ANOVA is significant AND IV has more than two groups
  - Purpose: Determine which specific groups differ significantly
  - Choice depends on equality of variances (from Levene's test)
- **APA Reporting**:
  - Format: F(df_between, df_within) = [F-value], p = [p-value], η² = [value]
  - Example: F(2, 78) = 3.89, p = .025, η² = .09

### Repeated Measures ANOVA

- **Purpose**: Compare means across 3+ conditions with the same participants
- **Advantage over One-Way ANOVA**: Reduces error variance from individual differences
- **Requirements**:
  - One categorical IV with 3+ levels (all participants experience all levels)
  - One continuous DV (scale measurement)
- **Key Assumption - Sphericity**:
  - Definition: Equal variances of the differences between all pairs of levels
  - Test with Mauchly's test
  - If p > .05: Assumption met (use "Sphericity Assumed" row)
  - If p ≤ .05: Assumption violated (use "Greenhouse-Geisser" row)
- **Key SPSS Steps**:
  1. Analyze → General Linear Model → Repeated Measures
  2. Define factor name and number of levels
  3. Assign variables to within-subjects levels
- **Interpreting Results**:
  - Find "Tests of Within-Subjects Effects" table
  - Choose correct row based on Mauchly's test
  - Look for F-statistic, degrees of freedom, p-value, and partial eta squared (ηₚ²)
- **Contrasts**:
  - Purpose: Pinpoint where significant differences occur between specific levels
  - "Simple" contrasts compare each level to a reference level
  - Look at "Tests of Within-Subjects Contrasts" table for significance of each comparison
- **APA Reporting**:
  - Format: F(df_factor, df_error) = [F-value], p = [p-value], ηₚ² = [value]
  - Note: If using Greenhouse-Geisser correction, df values may be non-integers

## IV. Module 5: Factorial ANOVA

### Two-Way ANOVA

- **Purpose**: Examine how two IVs affect a DV, both individually and together
- **Key Concepts**:
  - **Main Effects**: Individual impact of each IV (averaging across levels of other IV)
  - **Interaction Effect**: Whether the effect of one IV depends on levels of the other IV
- **Requirements**:
  - Two categorical IVs
  - One continuous DV (scale measurement)
  - Independent observations
- **Key SPSS Steps**:
  1. Analyze → General Linear Model → Univariate
  2. Put DV in "Dependent Variable" box
  3. Put both IVs in "Fixed Factor(s)" box
  4. Options → Check "Descriptive statistics" and "Estimates of effect size"
  5. Plots → Create interaction plots
- **Interpreting Results**:

  - **Omnibus Effect**: "Corrected Model" row in output table

    - Tests if overall model explains significant variance

  - **Main Effects**: Rows for each IV

    - Significant main effect (p ≤ .05): IV has significant impact on DV
    - Non-significant (p > .05): IV does not have significant impact on DV

  - **Interaction Effect**: Row with both IVs (e.g., "IV1 \* IV2")
    - Significant interaction (p ≤ .05): Effect of one IV depends on levels of other IV
    - Non-significant (p > .05): IVs affect DV independently

- **Visualizing Interactions**:
  - **Parallel lines**: No interaction
  - **Non-parallel lines**: Interaction exists
  - **Crossing lines**: Strong interaction
- **APA Reporting**:
  - Format for each effect: F(df1, df2) = [F-value], p = [p-value], partial η² = [value]
  - Report omnibus effect, both main effects, and interaction effect

### Important Considerations for Factorial Designs

- **Multiple Null Hypotheses**: Need to test and report on:
  1. Overall model (omnibus)
  2. First main effect
  3. Second main effect
  4. Interaction effect
- **Effect Size Interpretation**:
  - Small: partial η² ≈ .01
  - Medium: partial η² ≈ .06
  - Large: partial η² ≈ .14
- **Interpreting Complex Results**:
  - If interaction is significant: Main effects may be misleading (must interpret with caution)
  - Remember: "It depends" is often the key insight from factorial designs

## V. Module 6: Correlation and Regression

### Correlation

- **Purpose**: Examine strength and direction of linear relationship between two scale variables
- **Requirements**:
  - Two continuous variables (scale measurement)
  - Assumptions: Linear relationship, no extreme outliers
- **Pearson's Correlation Coefficient (r)**:
  - Range: -1.0 to +1.0
  - **Sign**: Indicates direction
    - Positive: Variables increase together
    - Negative: As one increases, other decreases
  - **Magnitude**: Indicates strength
    - |r| < 0.3: Weak relationship
    - 0.3 ≤ |r| < 0.7: Moderate relationship
    - |r| ≥ 0.7: Strong relationship
- **Coefficient of Determination (r²)**:
  - Proportion of variance in one variable explained by the other
  - Calculate by squaring r
  - Example: If r = -.36, then r² = .13 (13% of variance is shared)
- **Key SPSS Steps**:
  1. Analyze → Correlate → Bivariate
  2. Select variables to analyze
  3. Ensure "Pearson" is selected
- **APA Reporting**:
  - Format: r(df) = [r-value], p = [p-value]
  - Where df = N - 2
  - Example: r(37) = .56, p = .008
- **Important**: Correlation does not imply causation!

### Bivariate Regression

- **Purpose**: Predict a scale outcome variable (Y) from one predictor variable (X)
- **Requirements**:
  - Continuous outcome variable
  - Predictor can be continuous or categorical (dummy-coded)
- **Key Equation**: Ŷ = bX + a
  - Ŷ = Predicted outcome value
  - b = Slope (change in Y for one-unit increase in X)
  - a = Y-intercept (value of Y when X = 0)
- **Key SPSS Steps**:
  1. Analyze → Regression → Linear
  2. Move outcome variable to "Dependent"
  3. Move predictor variable to "Independent(s)"
- **Key Output Tables**:

  - **Model Summary**:

    - R²: Proportion of variance explained (0-1)
    - Adjusted R²: R² adjusted for sample size

  - **ANOVA Table**:

    - Tests overall significance of model
    - Significant F-test (p ≤ .05): Model explains significant variance

  - **Coefficients Table**:
    - Unstandardized B: Actual prediction weights
    - t-tests: Test significance of each coefficient
    - Significant t-test (p ≤ .05): Predictor significantly contributes to model

- **APA Reporting**:
  - Format for model: F(df_regression, df_residual) = [F-value], p = [p-value], R² = [value]
  - Format for coefficients: b = [value], t(df) = [t-value], p = [p-value]

### Multiple Regression

- **Purpose**: Predict outcome from two or more predictors
- **Key Equation**: Ŷ = b₁X₁ + b₂X₂ + ... + a
- **Key SPSS Steps**:
  - Same as bivariate regression, but include multiple predictors
- **Comparing Predictors**:

  - **Unstandardized Coefficients (B)**:

    - Original units of measurement
    - Not directly comparable between variables with different scales

  - **Standardized Coefficients (Beta, β)**:
    - Expressed in standard deviation units
    - Directly comparable between predictors
    - Larger absolute value = stronger predictor

- **Model Comparison**:
  - Compare Adjusted R² between models
  - Higher value indicates better prediction
  - Adding predictors should increase Adjusted R² to justify complexity
- **APA Reporting**:
  - Similar to bivariate regression
  - Include standardized coefficients: β = [value]

### Mixed Factorial ANOVA

- **Purpose**: Analyze data with at least one between-subjects factor and one within-subjects factor
- **Requirements**:
  - At least one categorical IV manipulated between subjects
  - At least one categorical IV manipulated within subjects
  - One continuous DV
- **Key SPSS Steps**:
  1. Analyze → General Linear Model → Repeated Measures
  2. Define within-subjects factor(s) and between-subjects factor(s)
  3. Add between-subjects factor(s) to the model
- **Interpreting Results**:
  - Check Mauchly's test for sphericity
  - Examine main effects for both within-subjects and between-subjects factors
  - Examine interaction between within-subjects and between-subjects factors
- **APA Reporting**: Similar to Two-Way ANOVA, but with appropriate df adjustments for within-subjects tests

## VI. Module 7: Data Preparation and Practical Applications

### Data Preparation

- **Importing and Cleaning Data**:
  - Properly importing data from Excel to SPSS
  - Checking for data entry errors and missing values
  - Configuring variable types and labels
- **Checking Assumptions**:
  - Normality: Histograms, Q-Q plots, Shapiro-Wilk test
  - Homogeneity of variance: Levene's test
  - Independence of observations
  - Linearity and homoscedasticity for regression/correlation
- **Data Transformation**:
  - When and why to transform data
  - Common transformations (log, square root, inverse)

### Research Design Considerations

- **How Statistical Approaches Influence Design**:
  - Matching research questions to appropriate statistical tests
  - Planning sample size based on power analysis
  - Choosing between within-subjects and between-subjects designs
- **Creating Multiple Research Designs**:
  - Converting between-subjects designs to within-subjects (and vice versa)
  - Adding factors to create factorial designs
  - Moving from experimental to correlational designs

## VII. Practical Data Analysis Skills

### Choosing the Right Test

| Research Question | # of IVs | IV Type     | # of IV Levels | DV Type | Participants | Appropriate Test           |
| ----------------- | -------- | ----------- | -------------- | ------- | ------------ | -------------------------- |
| Difference?       | 1        | Categorical | 2              | Scale   | Different    | Independent-samples t-test |
| Difference?       | 1        | Categorical | 2              | Scale   | Same         | Paired-samples t-test      |
| Difference?       | 1        | Categorical | 3+             | Scale   | Different    | One-way ANOVA              |
| Difference?       | 1        | Categorical | 3+             | Scale   | Same         | Repeated-measures ANOVA    |
| Difference?       | 2+       | Categorical | Any            | Scale   | Different    | Factorial ANOVA            |
| Difference?       | 2+       | Mixed       | Any            | Scale   | Mixed        | Mixed-factors ANOVA        |
| Relationship?     | 1        | Scale       | N/A            | Scale   | N/A          | Pearson correlation        |
| Prediction?       | 1        | Any         | N/A            | Scale   | N/A          | Bivariate regression       |
| Prediction?       | 2+       | Any         | N/A            | Scale   | N/A          | Multiple regression        |

### Interpreting Statistical Output

- **Always consider**:
  1. Is the effect statistically significant? (p ≤ α, usually .05)
  2. What is the practical significance? (effect size)
  3. What are the actual group differences or relationship patterns?
  4. How do these results relate to the research question?
- **Common Mistakes**:
  - Confusing statistical significance with practical importance
  - Ignoring effect sizes
  - Over-interpreting non-significant results
  - Claiming causation from correlation or regression

### APA Reporting Checklist

- **All Statistical Tests**:
  - Italicize statistical symbols (t, F, r, p, etc.)
  - Report exact p-values (e.g., p = .032) unless very small (p < .001)
  - Include appropriate degrees of freedom
- **t-test**: t(df) = [t-value], p = [p-value], d = [Cohen's d value]
- **ANOVA**: F(df_between, df_within) = [F-value], p = [p-value], η² or ηₚ² = [value]
- **Correlation**: r(df) = [r-value], p = [p-value]
- **Regression**: F(df_regression, df_residual) = [F-value], p = [p-value], R² = [value]

### Common Pitfalls to Avoid

1. **Using the wrong test** for your research question or data type
2. **Ignoring assumptions** of statistical tests
3. **Misinterpreting p-values** (they don't indicate effect size or importance)
4. **Failing to report effect sizes** along with significance tests
5. **Over-relying on p-values** without considering practical significance
6. **Confusing correlation with causation**
7. **Ignoring the context** of your research question when interpreting results

## VIII. Exam Preparation Strategies

### Critical Understanding vs. Memorization

- Focus on understanding concepts rather than memorizing formulas
- Practice applying concepts to different scenarios
- Think about why procedures work the way they do

### Practice with Specific Questions

1. **Test Selection Questions**:
   - "Given [scenario], which statistical test should be used?"
   - Practice identifying IVs, DVs, measurement types, and design types
2. **Interpretation Questions**:
   - "What does this output tell us about the research question?"
   - Practice finding key statistics and drawing appropriate conclusions
3. **APA Reporting Questions**:
   - "Write the results in APA format."
   - Practice proper formatting for each test type
4. **Application Questions**:
   - "What does this result mean in practical terms?"
   - Practice connecting statistics to real-world implications

### Study Flowchart Approach

1. Identify the research question (difference, relationship, prediction)
2. Identify the variables (how many, what types)
3. Identify the design (between-subjects, within-subjects, factorial)
4. Select the appropriate test
5. Determine what to look for in results
6. Apply appropriate interpretation

Remember: The exam is testing your understanding of statistical concepts and their application, not just your ability to run analyses in SPSS.

Good luck with your final exam!
