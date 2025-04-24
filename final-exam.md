---
layout: default
title: Final Exam Study Guide
---

# PSY 330 Final Exam: Master Study Guide

This comprehensive guide integrates core concepts, statistical test details, interpretation skills, practical application examples, and exam strategies for your PSY 330 Statistical Methods final exam. It combines structured learning with insights derived from typical exam questions and explanations.

## I. Core Statistical Concepts (Module 1 Foundations)

### Descriptive Statistics

**Measures of Central Tendency:**

- **Mean:** Average of all values (sum/count). Sensitive to outliers.
- **Median:** Middle value when data is ordered. Less affected by outliers.
- **Mode:** Most frequently occurring value(s).

**Measures of Dispersion:**

- **Standard Deviation (SD or σ):** Average distance of scores from the mean. Indicates typical spread.
- **Variance (SD² or σ²):** Square of the standard deviation. Also measures spread.

### Normal Distribution

- **Definition:** A theoretical, bell-shaped, symmetrical distribution.
- **Characteristics:**
  - Mean = Median = Mode at the center.
  - Symmetrical around the mean.
  - Defined percentages of scores fall within specific standard deviations:
    - ~68% within ±1 SD
    - ~95% within ±2 SD
    - ~99.7% within ±3 SD

### Z-Scores (Standard Scores)

- **Definition:** Indicates how many standard deviations a specific score is above or below the mean.
- **Formula:** `z = (Score - Mean) / Standard Deviation` or `z = (X - μ) / σ` or `z = (X - M) / SD`
- **Uses:**
  - Standardize scores: Allows comparison across different distributions (different means/SDs).
    - _Example:_ To compare performance in History (M=60, SD=2, Score=63 -> z=+1.5) and Biology (M=40, SD=1, Score=43 -> z=+3.0), the higher z-score in Biology indicates better performance relative to classmates in that specific course.
  - Determine relative position: Shows where a score sits within its distribution.
    - _Example:_ A z-score of 0 means the score is exactly average. A z-score of +3.50 indicates a position very far above the mean in the extreme upper tail.
  - Calculate probabilities using the standard normal table.
  - _Symmetry:_ The normal distribution is symmetrical, so the proportion of scores above a positive z (e.g., P(Z > 0.89)) is equal to the proportion below the corresponding negative z (e.g., P(Z < -0.89)).

### Hypothesis Testing Framework

- **Null Hypothesis (H₀):** Statement of no effect, no difference, or no relationship. (The hypothesis the statistical test _directly_ evaluates).
  - _Example:_ "There is no difference in mean happiness scores between bike riders and non-riders."
- **Alternative/Research Hypothesis (H₁ or Hₐ):** Statement predicting an effect, difference, or relationship exists.
  - **Non-directional:** States a difference/relationship exists but doesn't specify the direction. Uses words like "differs," "is related," "changes."
    - _Example:_ "People who ride bikes _differ_ in happiness from people who do not ride bikes." (Doesn't say happier or less happy).
  - **Directional:** Specifies the direction of the difference/relationship. Uses words like "greater than," "less than," "positively related," "happier than."
    - _Example:_ "People who ride bikes are _happier than_ people who do not ride bikes."

### Variables & Measurement

- **Independent Variable (IV):** Variable manipulated or categorized by the researcher (presumed cause).
- **Dependent Variable (DV):** Variable measured by the researcher (presumed effect/outcome).
- **Predictor Variable:** Used in regression/correlation (conceptually similar to IV).
- **Criterion/Outcome Variable:** Used in regression/correlation (conceptually similar to DV).
- **Levels of Measurement:**
  - **Nominal:** Categories, no inherent order (e.g., Type of Music: Classical, Pop, Hip Hop).
  - **Ordinal:** Ordered categories, but intervals may not be equal (e.g., Likert scale: Strongly Disagree to Strongly Agree).
  - **Scale (Interval/Ratio):** Meaningful order with equal intervals between values. Ratio has a true zero. (e.g., temperature, height, weight, reaction time, test score).
- **_Critical Requirement:_** Most common parametric tests (t-tests, ANOVAs, Pearson correlation, linear regression) require the dependent variable (or both variables in correlation/regression) to be measured on a **scale** level. This allows for meaningful calculation of means and variances.

### Reliability

- **Concept:** The consistency or stability of a measurement instrument. Does it yield similar results under consistent conditions?
- **Cronbach's Alpha (α):** A common measure of _internal consistency reliability_ (how well items on a scale measure the same construct). Ranges 0 to 1.
- **Interpretation:** Higher values = better reliability. A very low value (e.g., α = .02) means the test is highly unreliable and scores are untrustworthy. Values > .70 or .80 are often considered acceptable/good.

## II. Significance, Errors, and Power (Module 2 Insights)

- **Alpha (α) Level:** The pre-set probability threshold for rejecting H₀ (commonly `.05`). Represents the maximum acceptable risk of a Type I error.
  - _Consequence of Changing Alpha:_ Lowering alpha (e.g., from .05 to .01) decreases the probability of a Type I error but makes it harder to reject H₀ (smaller critical region), thus increasing the probability of a Type II error.
- **p-value:** The probability of obtaining the observed test results (or results more extreme) _if the null hypothesis were actually true_.
- **Decision Rule:**
  - If `p ≤ α`: **Reject H₀** → Statistically significant result. The observed data are unlikely under the null hypothesis.
  - If `p > α`: **Fail to reject H₀** → Not statistically significant. The observed data are reasonably plausible under the null hypothesis.
  - _Example:_ A p-value of 0.02 means there's a 2% chance of getting such results if H₀ is true. Since `.02 < .05` (conventional alpha), reject H₀.
- **Type I Error:** Rejecting a **true** null hypothesis (a "false positive"). Probability = `α`.
  - _Definition:_ Concluding there is an effect/difference when there isn't one in reality.
- **Type II Error:** Failing to reject a **false** null hypothesis (a "false negative"). Probability = `β`.
  - _Definition:_ Concluding there isn't an effect/difference when there _is_ one in reality.
- **Statistical Power:** The probability of correctly rejecting a false null hypothesis (`1 - β`). The ability to detect a true effect.
- **Factors Influencing Significance & Power:** Even a small mean difference can be statistically significant if:
  - **Sample Size (N)** is very large: Larger N increases power.
  - **Variability within groups (error variance)** is very small: Less "noise" makes the "signal" (difference) easier to detect.
- **Sampling Distribution:** Theoretical distribution of a statistic (e.g., sample means) calculated from all possible samples of a given size from a population.
- **Standard Error:** The standard deviation of a sampling distribution (e.g., standard error of the mean). Measures variability of sample statistics.
- **Central Limit Theorem:** The sampling distribution of the mean tends towards a normal distribution as sample size increases, regardless of the population distribution's shape.

## III. Research Designs & Corresponding Tests

### Between-Subjects vs. Within-Subjects Designs

- **Between-Subjects (Independent Groups):**
  - Different participants are assigned to different conditions/levels of the IV. Each participant experiences only one level.
  - _Examples:_ Comparing spaced vs. massed practice groups (different people); comparing plant vs. no-plant classroom groups; comparing different ethnic groups.
  - **Tests used:** Independent-Samples t-test (2 groups), One-Way Between-Subjects ANOVA (3+ groups).
  - **Advantage:** No carryover/order effects.
  - **Disadvantage:** Requires more participants; individual differences contribute to error variance.
- **Within-Subjects (Repeated Measures):**
  - The same participants are measured under all conditions/levels of the IV or at multiple time points.
  - _Examples:_ Rating two cornbread recipes (same friends); blood pressure before vs. after medication (same people); memory tested under binaural beats vs. static (same people); memory tested for high, medium, low arousal words (same people).
  - **Tests used:** Paired-Samples t-test (2 conditions), One-Way Repeated-Measures ANOVA (3+ conditions).
  - **_Key Advantage:_** More powerful because it removes/controls for stable individual differences between participants from the error term, making it easier to detect the effect of the IV.
  - **Disadvantage:** Potential for order effects, practice effects, fatigue (carryover).
  - _When NOT appropriate:_ When comparing pre-existing, distinct groups (e.g., ethnic groups, age groups where participants cannot be in both).
- **Factorial Design:** Involves two or more Independent Variables (Factors). Allows examination of main effects and interactions. Can be between-subjects, within-subjects, or mixed.

### Experimental vs. Quasi-Experimental Designs:

- **True Experiment:** Researcher manipulates IV(s) **AND** uses **random assignment** to conditions. Allows for strong causal inferences.
- **Quasi-Experiment:** Lacks random assignment. Often uses pre-existing groups (e.g., different classrooms, smokers vs. non-smokers). Causal inferences are weaker due to potential confounding variables.
- **_Essential Difference:_** **Random assignment** is the key distinction enabling causal claims in experiments.

## IV. t-Tests (Comparing Two Means - Module 3)

### Z-Test vs. t-Test: The Crucial Decision

- **_Key Distinction:_** The choice depends on whether the **population standard deviation (σ)** is known.
  - Use **z-test** IF σ is known. (Rare in psychology).
  - Use **t-test** IF σ is unknown and must be estimated from the sample SD. (Most common scenario).

### One-Sample t-Test

- **Purpose:** Compare a single sample mean (M) to a known or hypothesized population mean (μ).
- **Requirements:** Population SD (σ) is unknown. DV is scale.
- **SPSS:** `Analyze → Compare Means → One-Sample T Test`. Enter test value (μ).
- **APA:** _t_(df) = [t-value], _p_ = [p-value], _d_ = [Cohen's d] (df = N-1). (Effect size: Small ≈ 0.2, Medium ≈ 0.5, Large ≈ 0.8)

### Independent-Samples t-Test

- **Purpose:** Compare the means of two independent groups (between-subjects design).
- **Requirements:** One categorical IV with exactly 2 levels; one scale DV; independence of observations.
- **_Design Link:_** Used for **between-subjects** designs with two groups (e.g., spaced vs. massed practice; plant vs. no-plant).
- **Assumption:** Homogeneity of variances (tested with Levene's Test).
- **SPSS:** `Analyze → Compare Means → Independent-Samples T Test`. Define groups for the IV.
- **Interpretation:** Check Levene's Test first. Report t, p, and effect size (Cohen's d) from the appropriate row ("Equal variances assumed" or "not assumed").
- **APA:** _t_(df) = [t-value], _p_ = [p-value], _d_ = [Cohen's d] (df based on output, often N-2). (Effect size: Small ≈ 0.2, Medium ≈ 0.5, Large ≈ 0.8)
- _Interpreting Output:_ In _t_(37) = 5.95, _p_ < .001, the `5.95` is the calculated t-statistic value.

### Paired-Samples t-Test (Dependent-Samples t-Test)

- **Purpose:** Compare the means of two related measurements (within-subjects design).
- **Requirements:** Two related variables (often the same DV measured at two times or under two conditions for the same participants); DV is scale.
- **_Design Link:_** Used for **within-subjects** designs with two conditions (e.g., cornbread ratings; before/after medication; binaural beats vs. static).
- **_Advantage:_** More power than independent t-test because it controls for individual differences.
- **SPSS:** `Analyze → Compare Means → Paired-Samples T Test`. Select the pair of variables.
- **APA:** _t_(df) = [t-value], _p_ = [p-value], _d_ = [Cohen's d] (df = N_pairs - 1). (Effect size: Small ≈ 0.2, Medium ≈ 0.5, Large ≈ 0.8)

## V. ANOVA (Comparing Means of 2+ Groups - Modules 4 & 5)

### Core ANOVA Concepts

- **Purpose:** Compare means across two or more groups/conditions.
- **Data Requirement:** Dependent Variable must be **Scale** level.
- **F-Ratio:** The test statistic. `F = Variance Between Groups / Variance Within Groups` (MS_between / MS_within).
  - **Interpretation:**
    - If `F ≈ 1`: Variance between groups is similar to variance within groups (error). Suggests no significant effect; fail to reject H₀.
    - If `F > 1`: Variance between groups is larger than variance within groups. Suggests the IV may have caused differences beyond chance.
  - _Large F-ratio likely with:_ Large differences between group means **AND** small variances within groups.
- **Omnibus Test:** The overall F-test in ANOVA tells you _if_ there is _any_ significant difference among the means, but not _which_ specific means differ.
- **Post-Hoc Tests:** Used _after_ a significant omnibus F-test (when IV has 3+ levels) to determine which specific pairs of means are significantly different. Choice depends on assumptions (e.g., Levene's test).
- **Effect Size:** η² (Eta squared) or ηₚ² (Partial eta squared) = proportion of variance in the DV explained by the IV(s). (Conventionally: Small ≈ .01, Medium ≈ .06, Large ≈ .14).
  - _Interpretation:_ ηₚ² = .099 means approx. 9.9% of the variance in the DV is attributable to the IV in this analysis (a medium effect).

### One-Way Between-Subjects ANOVA (Module 4)

- **Purpose:** Compare means of three or more independent groups.
- **_Design Link:_** Used for **between-subjects** designs with one IV having 3+ levels (e.g., comparing memory scores across 4 different music conditions).
- **Requirements:** One categorical IV (3+ levels); one scale DV; independence; homogeneity of variances (Levene's test).
- **SPSS:** `Analyze → Compare Means → One-Way ANOVA`. Check Homogeneity test & select Post Hoc tests.
- **APA:** _F_(df*between, df_within) = [F-value], \_p* = [p-value], η² = [value]. Report post-hoc results if F is significant.

### One-Way Repeated-Measures ANOVA (Module 4)

- **Purpose:** Compare means across three or more related conditions (within-subjects design).
- **_Design Link:_** Used for **within-subjects** designs with one IV having 3+ levels (e.g., testing memory for high, medium, low arousal words in the same people).
- **Requirements:** One categorical IV (3+ levels, experienced by all participants); one scale DV; sphericity assumption (Mauchly's test).
- **_Advantage:_** More powerful than between-subjects ANOVA due to removing individual difference variance.
- **SPSS:** `Analyze → General Linear Model → Repeated Measures`. Define factor, assign variables.
- **Interpretation:** Check Mauchly's Test. Use "Sphericity Assumed" row if _p_ > .05, otherwise use correction (e.g., "Greenhouse-Geisser"). Report within-subjects contrasts or post-hoc tests if F is significant.
- **APA:** _F_(df*factor, df_error) = [F-value], \_p* = [p-value], ηₚ² = [value]. Mention if correction was used.

### Factorial ANOVA (Between-Subjects, e.g., Two-Way - Module 5)

- **Purpose:** Examine effects of two or more IVs (factors) on a scale DV, including their interaction.
- **Key Concepts:**
  - **Main Effect:** The overall effect of one IV, averaging across the levels of the other IV(s). There is one main effect tested for each IV. (e.g., In a 2x2 design, there are 2 main effects).
  - **Interaction Effect:** Occurs when the effect of one IV _depends_ on the level of another IV. (e.g., In a 2x2 design, there is 1 two-way interaction).
- **Design:** Can be fully between-subjects, fully within-subjects (Repeated Measures Factorial), or mixed. This section focuses on between-subjects.
- **Requirements:** Two+ categorical IVs; one scale DV; independence; homogeneity of variances.
- **SPSS:** `Analyze → General Linear Model → Univariate`. Add IVs to "Fixed Factors". Request Plots and Effect Size.
- **Interpretation:** Check main effects and interaction effect F-tests and p-values. If interaction is significant, interpret main effects _with caution_ (the effect of one IV isn't simple; it depends). Use plots to visualize interaction.
- **APA:** Report _F_, _p_, and ηₚ² for each main effect and the interaction effect. E.g., Main Effect A: _F_(...) = ..., _p_ = ..., ηₚ² = ...; Main Effect B: _F_(...) = ..., _p_ = ..., ηₚ² = ...; Interaction AxB: _F_(...) = ..., _p_ = ..., ηₚ² = ....

### Mixed-Factors ANOVA

- **Purpose:** Analyzes designs with at least one **between-subjects** IV AND at least one **within-subjects** IV.
- **_Design Link:_** Used when you have both types of factors simultaneously. (e.g., Class [Between: Cog vs. Stats] x Prompt [Within: Expressive vs. Control]; Story Type [Between: News vs. Social Media] x Story Valence [Within: Positive vs. Negative]).
- **SPSS:** `Analyze → General Linear Model → Repeated Measures`. Define within-factor(s), assign within-variables, **AND** add between-subjects factor(s) to the "Between-Subjects Factor(s)" box.
- **Interpretation:** Check assumptions (Sphericity for within-effects, Homogeneity for between-effects). Examine _F_, _p_, ηₚ² for the main effect of the between-subjects IV, the main effect of the within-subjects IV, and their interaction.
- **APA:** Report results for all effects, similar to Factorial ANOVA, noting which are between- vs. within-subjects effects.

## VI. Correlation and Regression (Relationships & Prediction - Module 6)

### Correlation

- **Purpose:** Measure the strength and direction of the **linear** relationship between two **scale** variables.
- **Pearson's r:** The correlation coefficient.
  - **Range:** -1.0 (perfect negative linear relationship) to +1.0 (perfect positive linear relationship). 0 indicates no linear relationship.
  - **Direction (Sign):** Positive (+) means variables tend to move in the same direction; Negative (-) means variables tend to move in opposite directions.
    - _Example:_ Higher optimism associated with lower depression (negative _r_); Higher introversion associated with higher depression (positive _r_).
  - **Strength (Magnitude/Absolute Value):** The closer `|r|` is to 1, the stronger the linear relationship.
    - _Example:_ _r_ = -0.90 is a _stronger_ relationship than _r_ = +0.50 because `|-0.90| > |+0.50|`.
  - **General Guidelines (Cohen, 1988):** Small ≈ |.1|, Medium ≈ |.3|, Large ≈ |.5|. (Note: Field-specific interpretations may vary).
  - _Interpreting Tables:_ To find weakest/strongest relationship in a table, find the 'r' value closest to 0 (weakest) or farthest from 0 (strongest), _ignoring the sign_.
- **Coefficient of Determination (r²):**
  - Calculated by squaring 'r'.
  - Represents the proportion of variance in one variable that is statistically _explained by_ (or shared with) the other variable (sometimes called shared variance). (Benchmarks for η² can provide a rough guide, but context is important).
  - _Example:_ If _r_ = -0.36 (a medium effect), then _r²_ = (-0.36)² ≈ 0.13, meaning about 13% of the variance is shared/explained.
- **Requirements:** Two scale variables; linear relationship; no significant outliers.
- **SPSS:** `Analyze → Correlate → Bivariate`. Select variables.
- **APA:** _r_(df) = [r-value], _p_ = [p-value] (df = N - 2).
- **_CRITICAL CAUTION:_** Correlation does **NOT** imply causation!

### Regression

- **Purpose:** Predict the value of one scale outcome/criterion variable (Y) based on one or more predictor variables (X).
- **Types:**
  - **Univariate (Simple) Regression:** One predictor variable.
  - **Multiple Regression:** Two or more predictor variables.
- **Regression Equation:** Represents the best-fitting line/plane.
  - Simple: `Ŷ = bX + a` (or `Ŷ = b₁X₁ + b₀`)
  - Multiple: `Ŷ = b₁X₁ + b₂X₂ + ... + b₀`
  - `Ŷ` = Predicted value of Y.
  - `a` or `b₀` = Y-intercept (Predicted Y when all X=0).
  - `b` or `b₁, b₂...` = Slopes (Unstandardized Coefficients).
  - _Using the Equation:_ If `Ŷ = 5x + 25` (salary in $1k, x=years education), for x=9, predicted salary `Ŷ = 5(9)+25 = 70`, or $70,000.
- **Key Output Interpretation:**
  - **Model Summary:**
    - **R²:** Proportion of variance in Y explained by the predictor(s) _together_. (Interpretation depends heavily on the research field; η² benchmarks like Small ≈ .01, Medium ≈ .06, Large ≈ .14 offer only a rough guide).
    - **Adjusted R²:** More conservative estimate, adjusted for number of predictors and N. Often preferred, especially with multiple predictors.
  - **ANOVA Table:** Tests the overall significance of the regression model (Is R² significantly different from zero?). Look at _F_ and _p_-value.
  - **Coefficients Table:**
    - **Unstandardized Coefficients (b):** Predict change in Y in its _original units_ for a one-unit change in X. Useful for making predictions. _Not directly comparable_ if Xs have different scales.
    - **Standardized Coefficients (Beta, β):** Predict change in Y in _standard deviation units_ for a one-SD change in X. Used to compare relative strength of predictors _within the same model_ because they are on the same scale. Larger absolute Beta = stronger unique predictor (no standard small/medium/large benchmarks, comparison is relative).
    - **t-tests and p-values:** Indicate whether each individual predictor significantly contributes to the model _after accounting for other predictors_.
  - _Simple Regression Equivalence:_ In simple linear regression (one predictor), the standardized coefficient Beta (β) is equal to the Pearson correlation coefficient (r) between X and Y.
- **SPSS:** `Analyze → Regression → Linear`. Add DV to "Dependent", IV(s) to "Independent(s)".
- **APA:** Report overall model significance: _F_(df*reg, df_resid) = [F-value], \\\_p* = [p-value], _R²_ = [value]. Report coefficients for significant predictors: _b_ = [value], β = [value], _t_(df*resid) = [t-value], \\\_p* = [p-value].

## VII. Data Preparation and Assumptions

- **Data Cleaning:** Check for errors, outliers, missing values. Configure variables correctly in SPSS (type, labels, values).
- **Assumption Checking:** Essential before interpreting results!
  - **Normality:** DV distribution (histograms, Q-Q plots, Shapiro-Wilk). Less critical with large N (CLT).
  - **Homogeneity of Variance** (t-tests, Between-Subjects ANOVA): Levene's Test.
  - **Sphericity** (Repeated-Measures ANOVA): Mauchly's Test.
  - **Independence of Observations:** Assumed based on design (usually met if participants are unrelated and measured once, or if dependencies are modeled).
  - **Linearity** (Correlation, Regression): Scatterplots.
  - **Homoscedasticity** (Regression): Scatterplot of residuals vs. predicted values.
- **Data Transformation:** Consider if assumptions are badly violated (e.g., log, square root). Use cautiously.

## VIII. Practical Data Analysis & Exam Strategy

### Choosing the Right Test (Summary Table)

| Goal?             | # of IVs | IV Type(s)  | IV Levels | DV Type | Design           | Test                       |
| :---------------- | :------- | :---------- | :-------- | :------ | :--------------- | :------------------------- |
| **Difference?**   | 1        | Categorical | 2         | Scale   | Between (Indep)  | Independent-samples t-test |
| **Difference?**   | 1        | Categorical | 2         | Scale   | Within (Related) | Paired-samples t-test      |
| **Difference?**   | 1        | Categorical | 3+        | Scale   | Between (Indep)  | One-way ANOVA              |
| **Difference?**   | 1        | Categorical | 3+        | Scale   | Within (Related) | Repeated-measures ANOVA    |
| **Difference?**   | 2+       | Categorical | Any       | Scale   | Between (Indep)  | Factorial ANOVA            |
| **Difference?**   | 2+       | Mixed (B/W) | Any       | Scale   | Mixed            | Mixed-factors ANOVA        |
| **Relationship?** | N/A      | Scale       | N/A       | Scale   | Correlational    | Pearson correlation        |
| **Prediction?**   | 1        | Any         | N/A       | Scale   | Regression       | Bivariate regression       |
| **Prediction?**   | 2+       | Any         | N/A       | Scale   | Regression       | Multiple regression        |
| **Compare M?**    | N/A      | N/A         | N/A       | Scale   | (vs. Pop μ)      | One-sample t-test / Z-test |

### Interpretation & Reporting

**Key Steps:**

1.  **Check Assumptions.**
2.  Identify the key test statistic (_t_, _F_, _r_) and its _p_-value.
3.  Determine **Statistical Significance** (Is _p_ ≤ α?).
4.  Assess **Practical Significance / Effect Size** (_d_, η², ηₚ², *r*², *R*², β). How big is the effect?
5.  **Describe the Pattern:** Which groups differ? What is the direction of the relationship/prediction? Use means, correlation signs, coefficient signs.
6.  Relate back to the research question.
7.  **APA Format:** Follow specific guidelines (italics, spacing, decimal places, reporting df, exact p-values unless _p_ < .001). See examples under each test.

### Common Pitfalls to Avoid:

- Choosing the wrong test.
- Ignoring assumptions.
- Misinterpreting p-values (≠ effect size, ≠ practical importance).
- Forgetting effect sizes.
- Claiming causation from non-experimental designs (correlation, regression, quasi-experiments).
- Over-interpreting non-significant results ("proving" the null).
- Ignoring context.
- Confusing statistical significance with practical importance (large N or low variability can make tiny, unimportant effects statistically significant).

### Exam Strategy

- **Focus on Understanding:** Why use this test? What do the results mean conceptually?
- **Practice Test Selection:** Given a scenario, identify IVs, DV, design -> choose test.
- **Practice Interpretation:** Given output, find key numbers, state the conclusion in plain language and APA format.
- **Understand Key Distinctions:** Between vs. Within; Z vs. t; Main Effect vs. Interaction; Correlation vs. Causation; Statistical vs. Practical Significance.

**Good luck with your exam!**
