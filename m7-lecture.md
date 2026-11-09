### **Module 7 Statistics Study Guide: The Complete Research Workflow**

This capstone module isn't about learning a new statistical test. It's about putting all the pieces together. We will walk through the entire quantitative research process, from the initial design blueprint to the final, ethical interpretation of results. This is the "how-to" guide for thinking like a statistician and a researcher.

**Estimated Study Time:** 2–3 hours

#### Learning Objectives

By the end of this capstone module, you will be able to:

1. Choose an appropriate research design and make defensible causal claims.
2. Prepare a dataset for analysis (handle missing data, detect outliers, check assumptions).
3. Select the correct statistical test based on variables and design.
4. Interpret statistical outputs beyond p-values (effect sizes, df, model fit).
5. Report results in clear APA style for t-tests, ANOVA, correlation, and regression.
6. Execute core analyses in SPSS and locate the exact values you need to report.

---

#### Table of Contents

1. [Part 1: The Blueprint — Choosing Your Research Design](#part-1-the-blueprint---choosing-your-research-design)
2. [Part 2: The "Data Janitor" Phase — Examining and Preparing Your Data](#part-2-the-data-janitor-phase---examining-and-preparing-your-data)
3. [Part 3: The Pre-Flight Check — Testing Statistical Assumptions](#part-3-the-pre-flight-check---testing-statistical-assumptions)
4. [Part 3.5: Master Comparison Tables](#part-35-master-comparison-tables)
5. [Part 4: The Art and Ethics of Statistics — Beyond the Numbers](#part-4-the-art-and-ethics-of-statistics---beyond-the-numbers)
6. [Part 5: Test Selection Decision Tree](#part-5-test-selection-decision-tree)
7. [Part 6: APA Reporting Quick Reference](#part-6-apa-reporting-quick-reference)
8. [Part 7: SPSS Playbook — Where to Click and What to Read](#part-7-spss-playbook---where-to-click-and-what-to-read)
9. [Part 8: Real Research Scenarios — Full Workflow Examples](#part-8-real-research-scenarios---full-workflow-examples)
10. [Part 9: Troubleshooting Guide](#part-9-troubleshooting-guide)
11. [Part 10: Knowledge Checks (Capstone Practice)](#part-10-knowledge-checks-capstone-practice)
12. [Module 7 Key Takeaways](#module-7-key-takeaways-a-researchers-mental-checklist)

#### **Part 1: The Blueprint - Choosing Your Research Design**

Your research design is the single most important decision you make. It determines the types of questions you can answer and the statistical tools you can use. The key question that guides your design is: **"Can I control and randomly assign variables?"**

| Research Design                      | Key Feature                                                                                   | What it allows you to do                                                                                       | Example                                                                                                            |
| :----------------------------------- | :-------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------- | :----------------------------------------------------------------------------------------------------------------- |
| **Experimental**                     | **Random Assignment** to groups/conditions. The researcher _manipulates_ the IV.              | The "gold standard." The only design that can establish a **cause-and-effect** relationship.                   | Randomly assigning students to either a "new teaching method" group or a "standard method" group.                  |
| **Quasi-Experimental**               | Uses **pre-existing, non-random groups.** The researcher cannot randomly assign participants. | Compare groups and identify strong associations, but **cannot make firm causal claims.**                       | Comparing the test scores of students from two different schools (you can't randomly assign students to a school). |
| **Non-Experimental (Correlational)** | **Observing and measuring** variables as they naturally exist. No manipulation or grouping.   | Identify relationships, associations, and make **predictions**, but **absolutely cannot establish causation.** | Measuring the relationship between hours spent studying and final GPA.                                             |

#### **Part 2: The "Data Janitor" Phase - Examining and Preparing Your Data**

Raw data is almost never perfect. Before running any analysis, you must clean and prepare it. This is a critical, non-negotiable step.

1.  **Handling Missing Data:**

    - **Why is it missing?** You must investigate. Is it random (a few people skipped a question) or is there a pattern (everyone skipped the same hard question)? A pattern suggests a flaw in your study or survey.
    - **How to handle it:** SPSS gives options like "listwise exclusion" (deleting a participant's entire row if any data is missing) or "pairwise exclusion" (only excluding them from analyses involving the specific variable they missed). Listwise is safer but can drastically reduce your sample size.

2.  **Finding Errors and Outliers:**
    - **Errors:** Simple data entry mistakes (e.g., typing "55" instead of "5" on a 1-7 scale). Find these by running descriptive statistics and looking for impossible values (e.g., minimums, maximums).
    - **Outliers:** Data points that are numerically extreme and far from the rest of the data. They can seriously distort your results, especially the mean.
    - **How to find them:**
      - **Visually:** Use a **Boxplot**. Points that appear far above or below the "whiskers" are potential outliers.
      - **Numerically:** Calculate Z-scores for your data. A common rule of thumb is that any data point with a **Z-score greater than +/- 3** is a potential outlier.

#### **Part 3: The Pre-Flight Check - Testing Statistical Assumptions**

The parametric tests we've learned (t-tests, ANOVA, Regression) are powerful, but they work best when certain assumptions about the data are met.

1.  **Scale of Measurement:** The Dependent Variable (DV) must be a **continuous scale** variable (Interval/Ratio). This is the most fundamental assumption.

2.  **Normality:** The distribution of the DV should be **approximately normal** (a symmetrical bell curve) within the population.

    - **How to check:**
      - **Visually:** Create a **histogram** with a normal curve overlay.
      - **Formally:** Use a statistical test like the **Shapiro-Wilk test**. If its p-value is _greater_ than .05, the normality assumption is met.

3.  **Homogeneity of Variances (for group comparisons):** The variance (spread) of the DV should be roughly **equal across all groups** being compared.
    - **How to check:** Use **Levene's Test**. If its p-value is _greater_ than .05, the assumption is met. We've seen this in the independent t-test and ANOVA outputs.

---

#### **Part 3.5: Master Comparison Tables**

These tables synthesize assumptions, requirements, and key information across all statistical tests covered in this course.

**Table 1: Assumptions by Test Type**

| Statistical Test | Scale of DV | Normality | Homogeneity of Variance | Independence | Additional Notes |
|:-----------------|:-----------|:----------|:------------------------|:-------------|:-----------------|
| **One-Sample t-test** | Scale (continuous) | DV approximately normal | N/A (one group) | Observations independent | Robust with n > 30 |
| **Paired-Samples t-test** | Scale | Differences approximately normal | N/A (within-subjects) | Pairs independent of each other | Check normality of difference scores |
| **Independent t-test** | Scale | DV normal in each group | Equal variances (Levene's test) | Groups independent | Can use Welch's correction if violated |
| **One-Way ANOVA** | Scale | DV normal in each group | Equal variances across groups | Observations independent | Robust to mild violations with equal n |
| **Factorial ANOVA** | Scale | DV normal in each cell | Equal variances across cells | Observations independent | More complex with unequal cell sizes |
| **Correlation** | Both variables scale | Bivariate normality | N/A | Observations independent | Check scatterplot for linearity |
| **Regression** | DV scale, IVs scale | **Residuals** normally distributed | Homoscedasticity of residuals | Observations independent | Check residual plots |

**Table 2: Effect Sizes Across Tests**

| Test Type | Effect Size Measure | Formula/Calculation | Interpretation Guidelines |
|:----------|:-------------------|:-------------------|:-------------------------|
| **t-tests** | Cohen's d | d = (M₁ - M₂) / SD_pooled | Small = 0.2, Medium = 0.5, Large = 0.8 |
| **ANOVA** | Eta-squared (η²) | η² = SS_between / SS_total | Small = .01, Medium = .06, Large = .14 |
| **ANOVA** | Partial η² | Partial η² = SS_effect / (SS_effect + SS_error) | Same as η² guidelines |
| **Correlation** | r² | r² = r × r | Proportion of shared variance |
| **Regression** | R² or Adjusted R² | From SPSS output | Proportion of variance explained by model |
| **Regression** | sr² (semipartial) | Square the "Part" column in SPSS | Unique variance from one predictor |

**Table 3: Degrees of Freedom Quick Reference**

| Test Type | df Formula | Example (N=60) |
|:----------|:-----------|:---------------|
| **One-Sample t** | df = N - 1 | df = 59 |
| **Paired t** | df = N - 1 (N = number of pairs) | df = 59 |
| **Independent t** | df = N₁ + N₂ - 2 | df = 58 (if n₁=30, n₂=30) |
| **One-Way ANOVA** | df_between = k - 1; df_within = N - k | df = 2, 57 (if k=3 groups) |
| **Factorial ANOVA (2×2)** | df_A = a-1; df_B = b-1; df_A×B = (a-1)(b-1); df_error = N-ab | df = 1, 1, 1, 56 |
| **Correlation** | df = N - 2 | df = 58 |
| **Regression** | df₁ = k (predictors); df₂ = N - k - 1 | df = 3, 56 (if 3 predictors) |

**Table 4: What to Do When Assumptions Are Violated**

| Assumption Violated | Options | Notes |
|:-------------------|:--------|:------|
| **Normality** | 1. Proceed if n > 30 (CLT)<br>2. Transform data (log, sqrt)<br>3. Use non-parametric test | t-tests/ANOVA fairly robust |
| **Homogeneity of Variance** | 1. Welch's correction (t-test)<br>2. Proceed if equal group sizes<br>3. Transform DV | Levene's p < .05 indicates violation |
| **Independence** | **STOP** - Use different analysis<br>(multilevel model, RM design) | Most serious violation - cannot ignore |
| **Linearity (correlation/regression)** | 1. Transform variables<br>2. Use polynomial regression<br>3. Use non-parametric (Spearman's rho) | Check scatterplot first |
| **Homoscedasticity (regression)** | 1. Transform DV<br>2. Use robust standard errors<br>3. Acknowledge limitation | Check residual plots |

---

#### **Part 4: The Art and Ethics of Statistics - Beyond the Numbers**

Choosing a statistical test isn't always a black-and-white decision. Sometimes, the data you collect might lead you to adjust your analysis plan. This flexibility is the "art" of statistics. However, with this flexibility comes great responsibility.

- **The Biggest Sin: Claiming Causation from Correlation.** This is the most common and serious error in interpreting statistics. Just because two variables are strongly related does not mean one causes the other. News headlines often make this mistake.

  - _Example:_ "Study finds e-cigarette use in teens leads to later smoking." The study was likely correlational. It only showed a relationship. It cannot prove that e-cigs _caused_ smoking. A third factor (e.g., a personality trait for risk-taking) could easily be the cause of both.

- **Be a Critical Consumer of Statistics:** When you read a study or a news report, always ask:
  - What was the actual **research design**? (Was it a true experiment?)
  - How were the variables **measured**? (Was a single question used to measure a complex concept like "motivation"?)
  - Is the conclusion justified by the design? (Are they claiming cause from a correlational study?)
  - What is the **effect size**? (Is a "significant" finding practically meaningful?)

---

#### **Part 5: Test Selection Decision Tree**

Use this quick guide to choose an analysis. When in doubt, revisit Modules 2–6.

- Start with your research question and variables:
  - Are you comparing a sample mean to a known value? → One-sample t-test (M2)
  - Are you comparing two means from the same people (pre/post or matched)? → Paired-samples t-test (M3)
  - Are you comparing two independent groups on one DV? → Independent-samples t-test (M3)
  - Are you comparing 3+ groups on one DV?
    - One factor (between-subjects) → One-way ANOVA (M4)
    - Within-subjects across levels → One-way repeated-measures ANOVA (M4)
    - Two factors (between, within, or mixed) → Factorial ANOVA (M5)
  - Are you assessing association between two scale variables? → Correlation (M6)
  - Are you predicting a DV from one or more predictors?
    - One predictor → Simple linear regression (M6)
    - 2+ predictors → Multiple regression (M6)

Key prerequisites (see Part 3): scale DV, approximate normality, and (for group comparisons) homogeneity of variance. If assumptions are seriously violated, consider transformations or nonparametric alternatives.

---

#### **Part 6: APA Reporting Quick Reference**

Use these templates; replace values with your results. Always include exact statistics and effect sizes when available.

- One-sample t-test: "M was significantly different from μ₀, t(df) = value, p = value, d = value."
- Paired-samples t-test: "Scores were higher after X than before, t(df) = value, p = value, d = value."
- Independent-samples t-test: "Group A (M = **, SD = **) differed from Group B (M = **, SD = **), t(df) = value, p = value, d = value."
- One-way ANOVA (omnibus): "There was a main effect of Factor, F(df_between, df_within) = value, p = value, η² = value."
- Factorial ANOVA: "Main effect of A: F(...)=...; Main effect of B: F(...)=...; Interaction A×B: F(...)=..., p=..., η²=...."
- Correlation: "X and Y were positively related, r(df) = value, p = value; r² = value variance explained."
- Regression (multiple): "The model was significant, F(df_model, df_resid) = value, p = value, R² = value. The strongest predictor was X (β = value, p = value)."

Notes:

- Report exact p-values (e.g., p = .023). If SPSS shows p = .000, report p < .001.
- Use two decimals for means/SDs where reasonable; match course conventions.

---

#### **Part 7: SPSS Playbook — Where to Click and What to Read**

- One-sample t-test: Analyze → Compare Means → One-Sample T Test → Test Value = μ₀. Read t, df, p.
- Paired t-test: Analyze → Compare Means → Paired-Samples T Test. Read Paired Samples Test (t, df, p) and Paired Samples Statistics (M, SD).
- Independent t-test: Analyze → Compare Means → Independent-Samples T Test. **SPSS v31+: Check "Homogeneity of variance test" box.** Check Levene's test in output; then t, df, p on the correct row.
- One-way ANOVA: Analyze → Compare Means → One-Way ANOVA. Read ANOVA table (F, df, p). If significant, use Post Hoc for pairwise.
- Factorial ANOVA (between): Analyze → General Linear Model → Univariate. Read Tests of Between-Subjects Effects (main effects, interaction).
- Repeated-measures: Analyze → General Linear Model → Repeated Measures. Read Within-Subjects Effects (and sphericity corrections if present).
- Correlation: Analyze → Correlate → Bivariate. Read Pearson Correlations (r, p, N). Square r for variance explained.
- Regression: Analyze → Regression → Linear. Read Model Summary (R²), ANOVA (F, p), Coefficients (β, p).

---

#### **Part 8: Real Research Scenarios — Full Workflow Examples**

These scenarios walk you through the complete research workflow, from research question to final APA write-up. Use these as templates for your own analyses.

**Scenario 1: Experimental Design — Testing a New Study Technique**

**Research Question:** Does a new mnemonic study technique improve memory test scores compared to traditional rereading?

**Step 1: Design Decision**
- **Design Type:** Experimental (random assignment to conditions)
- **IV:** Study method (mnemonic vs. rereading) — categorical, 2 levels
- **DV:** Memory test score (0-100) — scale/continuous
- **Sample:** 60 undergraduate students randomly assigned (n = 30 per group)
- **Analysis Plan:** Independent-samples t-test (comparing 2 independent groups on a continuous DV)

**Step 2: Data Cleaning**
- Run descriptive statistics: Min = 42, Max = 98, no impossible values detected
- Check for outliers: Create boxplot, calculate z-scores. One score (z = 3.1) flagged; investigate participant notes—legitimate high performer, keep in dataset
- Missing data: 2 participants dropped out (n = 29 mnemonic, n = 29 rereading)—still balanced groups

**Step 3: Check Assumptions**
- **Scale DV:** ✓ Memory score is continuous
- **Normality:** Run Shapiro-Wilk test for each group. Mnemonic group: p = .18; Rereading group: p = .24. Both p > .05 → assumption met ✓
- **Homogeneity of variance:** Levene's test p = .31 → assumption met ✓
- **Independence:** ✓ Participants randomly assigned, tested individually

**Step 4: Run Analysis in SPSS**
- Analyze → Compare Means → Independent-Samples T Test
- DV: Memory score; Grouping variable: Study method
- **SPSS v31+:** Check "Homogeneity of variance test" (older versions show Levene's automatically)
- Options: Check "Descriptive statistics"
- Results from output:
  - Mnemonic group: M = 78.5, SD = 12.3
  - Rereading group: M = 69.2, SD = 11.8
  - Levene's test: F = 1.05, p = .31 (use equal variances assumed row) — **Note:** In SPSS v31+, this may appear in a separate "Homogeneity of Variances" table
  - t(56) = 3.04, p = .004
  - Calculate Cohen's d: d = (78.5 - 69.2) / 12.05 = 0.77 (medium-to-large effect)

**Step 5: Interpret Results**
- t-test is significant (p = .004 < .05) → reject null hypothesis
- Mnemonic group scored significantly higher than rereading group
- Effect size (d = 0.77) indicates a medium-to-large practical difference
- **Can we claim causation?** YES! This is a true experiment with random assignment

**Step 6: APA Write-Up**

"An independent-samples t-test compared memory test scores between the mnemonic technique group and the traditional rereading group. The mnemonic group (M = 78.5, SD = 12.3) scored significantly higher than the rereading group (M = 69.2, SD = 11.8), t(56) = 3.04, p = .004, d = 0.77. This represents a medium-to-large effect, suggesting that the mnemonic technique is an effective strategy for improving memory performance."

---

**Scenario 2: Correlational Design — Screen Time and Sleep Quality**

**Research Question:** Is there a relationship between daily screen time and sleep quality in college students?

**Step 1: Design Decision**
- **Design Type:** Non-experimental/correlational (measuring existing variables)
- **Variable 1:** Daily screen time (hours) — scale/continuous
- **Variable 2:** Sleep quality index (1-10 scale) — treated as continuous
- **Sample:** 85 college students
- **Analysis Plan:** Bivariate correlation (examining relationship between two continuous variables)

**Step 2: Data Cleaning**
- Run descriptive statistics:
  - Screen time: M = 6.2 hours, SD = 2.1, Min = 2.0, Max = 12.5—all plausible
  - Sleep quality: M = 5.8, SD = 1.9, Min = 2, Max = 9—reasonable range
- Check for outliers: One participant reported 12.5 hours screen time (z = 3.0). Review data—valid response from heavy social media user; retain
- Missing data: 5 participants missing sleep quality data → use pairwise exclusion (n = 80 for this correlation)

**Step 3: Check Assumptions**
- **Both variables scale:** ✓ Both continuous measures
- **Linearity:** Create scatterplot—points show linear pattern, no obvious curve ✓
- **Normality:** Check histograms—both approximately normal ✓
- **Independence:** ✓ Each participant measured once

**Step 4: Run Analysis in SPSS**
- Analyze → Correlate → Bivariate
- Select both variables (screen time, sleep quality)
- Pearson correlation selected
- Results from output:
  - r = -.42, p < .001, N = 80
  - Calculate r²: (-.42)² = .18 (18% shared variance)

**Step 5: Interpret Results**
- Moderate negative correlation (r = -.42)
- Statistically significant (p < .001)
- As screen time increases, sleep quality tends to decrease
- 18% of variance in sleep quality is explained by screen time (moderate effect)
- **Can we claim causation?** NO! This is correlational—could be reverse causation or third variables

**Step 6: APA Write-Up**

"A bivariate correlation examined the relationship between daily screen time and sleep quality. There was a significant negative correlation between the two variables, r(78) = -.42, p < .001, r² = .18. Students who reported higher daily screen time tended to report lower sleep quality, with screen time accounting for 18% of the variance in sleep quality. However, as this is a correlational design, causation cannot be inferred—the direction of the relationship and potential third variables (e.g., stress levels affecting both variables) remain unclear."

**Common Pitfall to Avoid:** Do NOT write "increased screen time causes poor sleep." The correlation allows prediction but not causal claims.

---

#### **Part 9: Troubleshooting Guide**

**When Things Go Wrong: Common Problems and Solutions**

| Problem | Possible Cause | Solution |
|:--------|:--------------|:---------|
| **Levene's test significant (p < .05)** | Unequal variances across groups | 1. Check group sizes—if equal, proceed cautiously<br>2. Use Welch's correction (SPSS provides this)<br>3. Consider transforming DV<br>4. Report violation and robust results |
| **Shapiro-Wilk significant (p < .05)** | Non-normal distribution | 1. If n > 30, proceed (robust to mild violations)<br>2. Check histogram—severe skew?<br>3. Transform data (log, sqrt) or use non-parametric test<br>4. Report limitation |
| **SPSS won't run analysis** | Missing data or wrong variable type | 1. Check for missing values—remove or recode<br>2. Verify variable types (Measure column)<br>3. Ensure grouping variables are nominal/ordinal |
| **All F-tests non-significant** | Insufficient power or no real effect | 1. Check sample size—underpowered?<br>2. Verify IV manipulation worked<br>3. Check descriptive statistics—are means actually different?<br>4. Consider effect size—small but real? |
| **Interaction significant but main effects not** | Effect depends on combination of factors | **This is valid!** Focus interpretation on the interaction. Describe the pattern clearly. |
| **Very large F-statistic** | Possible data entry error | 1. Check descriptive statistics for outliers<br>2. Verify no typos in data entry<br>3. Check if variance is artificially small |
| **VIF > 10 in regression** | Multicollinearity among predictors | 1. Remove one of the correlated predictors<br>2. Combine correlated predictors<br>3. Interpret coefficients with extreme caution<br>4. Focus on overall model fit, not individual βs |
| **R² very low despite significant F** | Small effect that's statistically significant | **This happens with large samples!** Report honestly—statistically significant but limited practical importance. |

---

#### **Part 10: Knowledge Checks (Capstone Practice)**

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Missing Data Strategy</h4>
  <div class="quiz-question">
    <p><strong>Question:</strong> You plan multiple correlations among several scale variables and want to maximize usable N across different pairs. Which method is most appropriate?</p>
    <div class="options">
      <p>A) Listwise exclusion</p>
      <p>B) Pairwise exclusion</p>
      <p>C) Remove all rows with any missing values</p>
      <p>D) Mean imputation for all variables</p>
    </div>
  </div>
  <details>
    <summary>💡 Click to reveal answer and explanation</summary>
    <p><strong>Answer:</strong> B) Pairwise exclusion</p>
    <p>Pairwise keeps cases for each correlation even if they’re missing elsewhere (see M6 correlation setup).</p>
  </details>
</div>

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Meaning of F = 1</h4>
  <div class="quiz-question">
    <p><strong>Question:</strong> In a one-way ANOVA, F = 1. This implies that:</p>
    <div class="options">
      <p>A) Between-groups variance > within-groups variance</p>
      <p>B) Between-groups variance = within-groups variance</p>
      <p>C) Within-groups variance = 0</p>
      <p>D) Assumptions are violated</p>
    </div>
  </div>
  <details>
    <summary>💡 Click to reveal answer and explanation</summary>
    <p><strong>Answer:</strong> B) Between-groups variance = within-groups variance</p>
    <p>F is a ratio; near 1 indicates similar variances (see M4).</p>
  </details>
</div>

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: From r to r²</h4>
  <div class="quiz-question">
    <p><strong>Question:</strong> If r = −.36, approximately what proportion of variance is explained?</p>
    <div class="options">
      <p>A) .60</p>
      <p>B) .36</p>
      <p>C) .18</p>
      <p>D) .13</p>
    </div>
  </div>
  <details>
    <summary>💡 Click to reveal answer and explanation</summary>
    <p><strong>Answer:</strong> D) .13</p>
    <p>r² = .1296 ≈ .13 (see M6 correlation interpretation).</p>
  </details>
</div>

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Choosing t vs z</h4>
  <div class="quiz-question">
    <p><strong>Question:</strong> Which piece of information determines whether you should use a z-test instead of a t-test?</p>
    <div class="options">
      <p>A) Sample size exceeds 30</p>
      <p>B) Population standard deviation is known</p>
      <p>C) Population mean is unknown</p>
      <p>D) Number of predictors</p>
    </div>
  </div>
  <details>
    <summary>💡 Click to reveal answer and explanation</summary>
    <p><strong>Answer:</strong> B) Population standard deviation is known</p>
    <p>Use z when σ is known; otherwise, use t with s (see M2).</p>
  </details>
</div>

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Interpreting p</h4>
  <div class="quiz-question">
    <p><strong>Question:</strong> A test yields p = .02. Which interpretation is most accurate?</p>
    <div class="options">
      <p>A) The null is false with 98% probability</p>
      <p>B) There is a 2% chance the result is due to chance</p>
      <p>C) If the null were true, results this extreme would occur ~2% of the time</p>
      <p>D) The effect size is .02</p>
    </div>
  </div>
  <details>
    <summary>💡 Click to reveal answer and explanation</summary>
    <p><strong>Answer:</strong> C) If the null were true, results this extreme would occur ~2% of the time</p>
    <p>This is the frequentist definition of the p-value (see M2).</p>
  </details>
</div>

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Univariate vs Multiple Regression</h4>
  <div class="quiz-question">
    <p><strong>Question:</strong> Which pairing is correct?</p>
    <div class="options">
      <p>A) Univariate: two DVs; Multiple: one DV</p>
      <p>B) Univariate: one predictor; Multiple: two or more predictors</p>
      <p>C) Univariate: two or more predictors; Multiple: one predictor</p>
      <p>D) Univariate: two DVs; Multiple: two DVs</p>
    </div>
  </div>
  <details>
    <summary>💡 Click to reveal answer and explanation</summary>
    <p><strong>Answer:</strong> B) Univariate: one predictor; Multiple: two or more predictors</p>
    <p>Predictor count differentiates simple vs multiple regression (see M6).</p>
  </details>
</div>

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Main Effects in Factorial ANOVA</h4>
  <div class="quiz-question">
    <p><strong>Question:</strong> In a two-factor design, a main effect refers to:</p>
    <div class="options">
      <p>A) The difference between the largest and smallest cell mean</p>
      <p>B) Mean differences among levels of one factor, averaging over the other</p>
      <p>C) The overall interaction across both factors</p>
      <p>D) The difference between factors</p>
    </div>
  </div>
  <details>
    <summary>💡 Click to reveal answer and explanation</summary>
    <p><strong>Answer:</strong> B) Mean differences among levels of one factor, averaging over the other</p>
    <p>Factorial ANOVA tests each main effect and their interaction (see M5).</p>
  </details>
</div>

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: APA Reporting Choice</h4>
  <div class="quiz-question">
    <p><strong>Question:</strong> Which APA sentence is most appropriate for a significant independent-samples t-test?</p>
    <div class="options">
      <p>A) "The groups were different, F = 5.20, p = .03"</p>
      <p>B) "Group A (M = __, SD = __) differed from Group B (M = __, SD = __), t(df) = value, p = value, d = value"</p>
      <p>C) "The model was significant, R² = .42"</p>
      <p>D) "X and Y were positively related, r = .41, p = .01"</p>
    </div>
  </div>
  <details>
    <summary>💡 Click to reveal answer and explanation</summary>
    <p><strong>Answer:</strong> B) ...t(df) = value, p = value, d = value</p>
    <p>Independent t-tests are reported with t, df, p, and an effect size (see M2/M3).</p>
  </details>
</div>

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Variables → Test</h4>
  <div class="quiz-question">
    <p><strong>Question:</strong> Does daily screen time (hours; scale) relate to stress score (scale)? Which analysis?</p>
    <div class="options">
      <p>A) Independent-samples t-test</p>
      <p>B) Correlation</p>
      <p>C) One-way ANOVA</p>
      <p>D) Paired-samples t-test</p>
    </div>
  </div>
  <details>
    <summary>💡 Click to reveal answer and explanation</summary>
    <p><strong>Answer:</strong> B) Correlation</p>
    <p>Two scale variables → assess linear association (see M6).</p>
  </details>
</div>

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Prediction vs Association</h4>
  <div class="quiz-question">
    <p><strong>Question:</strong> Predict stress (scale) from work hours (scale) and sleep (scale). Which analysis?</p>
    <div class="options">
      <p>A) Simple regression</p>
      <p>B) Multiple regression</p>
      <p>C) One-way ANOVA</p>
      <p>D) Factorial ANOVA</p>
    </div>
  </div>
  <details>
    <summary>💡 Click to reveal answer and explanation</summary>
    <p><strong>Answer:</strong> B) Multiple regression</p>
    <p>Two predictors → multiple regression (see M6).</p>
  </details>
</div>

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Within vs Between</h4>
  <div class="quiz-question">
    <p><strong>Question:</strong> Same participants rated mood before and after a mindfulness session. Which test compares means?</p>
    <div class="options">
      <p>A) Independent-samples t-test</p>
      <p>B) Paired-samples t-test</p>
      <p>C) One-way ANOVA</p>
      <p>D) Repeated-measures ANOVA with 3 groups</p>
    </div>
  </div>
  <details>
    <summary>💡 Click to reveal answer and explanation</summary>
    <p><strong>Answer:</strong> B) Paired-samples t-test</p>
    <p>Two measurements from the same participants → paired design (see M3).</p>
  </details>
</div>

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Outlier Screening</h4>
  <div class="quiz-question">
    <p><strong>Question:</strong> A score has z = 3.25 in a large sample. How should you flag it?</p>
    <div class="options">
      <p>A) Not an outlier</p>
      <p>B) Potential outlier (investigate)</p>
      <p>C) Remove automatically</p>
      <p>D) Winsorize to z = 2.00</p>
    </div>
  </div>
  <details>
    <summary>💡 Click to reveal answer and explanation</summary>
    <p><strong>Answer:</strong> B) Potential outlier (investigate)</p>
    <p>Common screening rule is |z| ≥ 3 as potential outlier; investigate before removal (see M1).</p>
  </details>
</div>

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Normality Test</h4>
  <div class="quiz-question">
    <p><strong>Question:</strong> Shapiro–Wilk p = .21 for the DV within each group. What does this indicate?</p>
    <div class="options">
      <p>A) Normality not met</p>
      <p>B) Normality met</p>
      <p>C) Homogeneity met</p>
      <p>D) Sphericity met</p>
    </div>
  </div>
  <details>
    <summary>💡 Click to reveal answer and explanation</summary>
    <p><strong>Answer:</strong> B) Normality met</p>
    <p>p > .05 suggests no evidence against normality (see M4/M5 assumption checks).</p>
  </details>
</div>

---

## Statistics Quick Reference Cheat Sheet

**Print this page for exams and assignments!**

### Core Statistical Tests At-A-Glance

| When to Use | Statistical Test | SPSS Path | Key Output | Effect Size |
|:-----------|:----------------|:----------|:-----------|:------------|
| Compare sample to known value | One-Sample t-test | Compare Means → One-Sample T Test | t, df, p | Cohen's d |
| Compare 2 means, same people | Paired t-test | Compare Means → Paired-Samples T Test | t, df, p | Cohen's d |
| Compare 2 means, different people | Independent t-test | Compare Means → Independent-Samples T Test (v31+: check "Homogeneity of variance test") | t, df, p, Levene's | Cohen's d |
| Compare 3+ groups, 1 factor | One-Way ANOVA | Compare Means → One-Way ANOVA | F, df, p, post-hoc | η² or partial η² |
| Compare groups, 2 factors | Factorial ANOVA | GLM → Univariate | F for main effects & interaction | Partial η² |
| Relationship between 2 variables | Correlation | Correlate → Bivariate | r, p, N | r² |
| Predict DV from 1 IV | Simple Regression | Regression → Linear | R², F, β, t | R² or Adjusted R² |
| Predict DV from 2+ IVs | Multiple Regression | Regression → Linear | R², F, β, t, VIF | Adjusted R², sr² |

### All Formulas You Need

**Degrees of Freedom:**
- One-Sample t: df = N - 1
- Paired t: df = N - 1 (N = pairs)
- Independent t: df = N₁ + N₂ - 2
- One-Way ANOVA: df_between = k - 1; df_within = N - k
- Factorial (2×2): df_A = a-1; df_B = b-1; df_A×B = (a-1)(b-1); df_error = N-ab
- Correlation: df = N - 2
- Regression: df₁ = k; df₂ = N - k - 1

**Effect Sizes:**
- Cohen's d: (M₁ - M₂) / SD_pooled
- η²: SS_between / SS_total
- Partial η²: SS_effect / (SS_effect + SS_error)
- r²: r × r
- sr²: (Part correlation)²

**Interpretation Guidelines:**
- Cohen's d: .20 (small), .50 (medium), .80 (large)
- η² / Partial η²: .01 (small), .06 (medium), .14 (large)
- r: .10 (small), .30 (medium), .50 (large)

### Assumption Checklist

✓ **All parametric tests require:**
- Scale (continuous) DV
- Approximate normality
- Independence of observations

✓ **Group comparison tests (t-tests, ANOVA) also need:**
- Homogeneity of variance (Levene's test p > .05)

✓ **Correlation/Regression also need:**
- Linearity (check scatterplot)
- For regression: homoscedasticity of residuals

### Test Selection Flowchart

```
START: What type of variables do you have?

Categorical IV + Scale DV →
  ├─ 1 IV, 2 levels, same people → Paired t-test
  ├─ 1 IV, 2 levels, different people → Independent t-test
  ├─ 1 IV, 3+ levels → One-Way ANOVA
  └─ 2+ IVs → Factorial ANOVA

Scale IV + Scale DV →
  ├─ Examine relationship → Correlation
  └─ Predict DV from IV(s) →
      ├─ 1 predictor → Simple Regression
      └─ 2+ predictors → Multiple Regression

Comparing to known value →
  └─ One-Sample t-test
```

### APA Reporting Essentials

**Format Rules:**
- Italicize: F, t, r, p, df, n, M, SD
- Degrees of freedom in parentheses: t(df), F(df₁, df₂), r(df)
- No zero before decimal for p: p < .001 (not p < 0.001)
- Never report p = .000, use p < .001
- Report exact p when p > .001: p = .023
- Include effect sizes with all tests

**Templates:**
- t-test: "M = **, SD = **, t(df) = **, p = **, d = **"
- ANOVA: "F(df₁, df₂) = **, p = **, η² = **"
- Correlation: "r(df) = **, p = **, r² = **"
- Regression: "F(df₁, df₂) = **, p = **, Adjusted R² = **, β = **"

### Common Mistakes - Don't Do This!

❌ Claiming causation from correlation
❌ Forgetting to check assumptions
❌ Reporting main effects when interaction is significant
❌ Using p = .000 instead of p < .001
❌ Forgetting effect sizes
❌ Not reporting degrees of freedom
❌ Confusing r with r² (r = .50 means 25% variance, not 50%)
❌ Running post-hoc tests for 2-level factors
❌ Ignoring Levene's test results
❌ Extrapolating beyond your data range (regression)

### Critical Values to Remember

- α = .05 (most common significance level)
- |z| ≥ 3 = potential outlier
- VIF > 10 = serious multicollinearity problem
- Levene's p < .05 = violation of homogeneity
- Shapiro-Wilk p < .05 = violation of normality

### The Golden Rules

1. **Always visualize first** (scatterplots, boxplots, histograms)
2. **Check assumptions before testing**
3. **Report effect sizes, not just p-values**
4. **Correlation ≠ Causation** (only experiments can claim causation)
5. **Check the interaction first** (in factorial designs)
6. **Document all data cleaning decisions**
7. **Be honest about limitations**

---

### **Module 7 Key Takeaways: A Researcher's Mental Checklist**

1.  **Start with Design:** Is my study Experimental, Quasi-Experimental, or Non-Experimental? This dictates my conclusions.
2.  **Choose the Right Tool:** Based on my design and variables, which test is appropriate (t-test, ANOVA, Regression)?
3.  **Clean the Data:** Have I checked for errors, outliers, and investigated any missing data?
4.  **Check Assumptions:** Does my data meet the requirements for the test I want to run (normality, equal variances)?
5.  **Run and Interpret:** Execute the analysis, but don't stop at the p-value.
6.  **Tell the Whole Story:** What is the effect size? What is the practical meaning of the result?
7.  **Be Honest:** Does my conclusion match the limitations of my design? Am I avoiding the temptation to claim causation where there is only correlation?

---

#### Cross-Module References

- See M1 for z-scores, central tendency/variability, and measurement scales.
- See M2–M3 for t-tests and hypothesis testing workflow.
- See M4–M5 for ANOVA designs, main effects, and interactions.
- See M6 for correlation and regression, multicollinearity, and model interpretation.
