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
4. [Part 4: The Art and Ethics of Statistics — Beyond the Numbers](#part-4-the-art-and-ethics-of-statistics---beyond-the-numbers)
5. [Part 5: Test Selection Decision Tree](#part-5-test-selection-decision-tree)
6. [Part 6: APA Reporting Quick Reference](#part-6-apa-reporting-quick-reference)
7. [Part 7: SPSS Playbook — Where to Click and What to Read](#part-7-spss-playbook---where-to-click-and-what-to-read)
8. [Part 8: Knowledge Checks (Capstone Practice)](#part-8-knowledge-checks-capstone-practice)
9. [Module 7 Key Takeaways](#module-7-key-takeaways-a-researchers-mental-checklist)

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
- Independent t-test: Analyze → Compare Means → Independent-Samples T Test. Check Levene's test; then t, df, p on the correct row.
- One-way ANOVA: Analyze → Compare Means → One-Way ANOVA. Read ANOVA table (F, df, p). If significant, use Post Hoc for pairwise.
- Factorial ANOVA (between): Analyze → General Linear Model → Univariate. Read Tests of Between-Subjects Effects (main effects, interaction).
- Repeated-measures: Analyze → General Linear Model → Repeated Measures. Read Within-Subjects Effects (and sphericity corrections if present).
- Correlation: Analyze → Correlate → Bivariate. Read Pearson Correlations (r, p, N). Square r for variance explained.
- Regression: Analyze → Regression → Linear. Read Model Summary (R²), ANOVA (F, p), Coefficients (β, p).

---

#### **Part 8: Knowledge Checks (Capstone Practice)**

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
