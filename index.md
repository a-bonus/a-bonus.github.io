---
layout: default
title: M4 Assignment Guide
---

# How to use this guide

This guide and website is a new tool I'm developing to help you navigate statistical methods. It's a work in progress, but I'm hoping it will be useful for you. You'll find useful resources that I've collected and created to help you learn and apply statistical methods, this site is not a substitute for the lectures and discussions, but rather a tool to help you make sense of the material in more depth, and in a different way than you might be used to. Written more like documentation and a guide, rather than a traditional textbook.


# M4 Assignment Guide: Thinking Through ANOVA Analyses

This guide helps you navigate the M4 assignment, focusing on the *why* behind the steps in ANOVA and Repeated Measures ANOVA. It encourages you to think critically about the process and interpret results thoughtfully. Use the hints provided to steer you in the right direction in SPSS and your interpretations.

**Goal:** To develop your understanding and application of ANOVA techniques by actively engaging with the data and research questions.

**General Principles:**
* Always consider the research question first. What are you trying to find out?
* Understand the assumptions of each test. Why are they important?
* Don't just report numbers; interpret what they mean in the context of the research question.
* APA format requires specific conventions – pay attention to italics, p-value reporting, etc.

---

## Part 1: Data Preparation (Q1 & Q2 Dataset)

**Objective:** Correctly set up your SPSS data file from the provided Excel sheet. Accurate setup is crucial for valid analyses.

**Process:**

1. **Import:** Bring the data from the first 'page' of the Excel file into SPSS.
   * `Hint:` SPSS has a dedicated function for importing data directly from Excel files under the `File` menu. Ensure variable names are read correctly.
2. **Configure Variables:** Switch to SPSS's "Variable View". This is where you define your data structure.
   * **Measure Type:** For each variable, consider what kind of data it represents (categorical, continuous ranking, continuous measurement). Assign the appropriate "Measure" level.
     * `Think:` What distinguishes `Nominal`, `Ordinal`, and `Scale` measures? Refer to the Codebook.
   * **Value Labels:** For categorical variables (`Marital`, `Employment Status`, `EducR`), numeric codes are used in the data. You need to tell SPSS what these codes mean.
     * `Hint:` The "Values" column in Variable View is where you link numeric codes (like `1`) to their text labels (like `"Married"`). Consult the Codebook for the correct codes and labels.
3. **Save:** Save your configured SPSS data file (.sav).

---

## Part 2: Question 1 - One-Way ANOVA (Education & Executive Function)

**Research Question:** Does executive function (EF1) seem to differ based on educational attainment (EducR)?

### A. Hypotheses and Variables

* **Identify:** What is the outcome measure being influenced (DV)? What variable defines the groups being compared (IV)?
* **Null Hypothesis (H₀):** Formulate the statement of "no difference" or "no relationship" between your IV and DV in the context of this research question. Remember, ANOVA tests if group *means* are equal.

### B. Assumption Check: Homogeneity of Variances

* **Concept:** ANOVA assumes the variability (variance) within each group is roughly similar. Why is this important for comparing means?
* **Test:** Use SPSS to perform Levene's test for homogeneity of variances.
  * `Hint:` This option is usually found within the main `One-Way ANOVA` procedure settings (`Analyze -> Compare Means -> One-Way ANOVA`). Look under `Options`.
* **Interpretation:**
  1. Locate Levene's test result (specifically the p-value, often labeled "Sig.") in your SPSS output.
  2. Compare this p-value to the standard alpha level (α = 0.05).
  3. `Think:` What does it mean if Levene's test is significant (p ≤ .05) versus non-significant (p > .05) regarding the ANOVA assumption?
* **Action:** Paste the relevant output table and state your conclusion about the assumption.

### C. Main ANOVA Results

* **Perform Test:** Run the One-Way ANOVA in SPSS using `EF1` as the DV and `EducR` as the Factor/IV.
* **Locate Key Statistics:** In the main ANOVA table of your output, find the F-statistic, degrees of freedom (df - there are two!), and the p-value (Sig.).
* **Effect Size (η²):** Determine the practical significance. How much of the variance in EF1 is associated with EducR?
  * `Hint:` SPSS can calculate this for you (look in `Options` for effect size estimates), or you can calculate it manually using Sum of Squares values from the ANOVA table (η² = SS_between / SS_total). If calculating manually, show your work.
* **Report in APA Format:** Present the results concisely using standard APA symbols and format (e.g., *F*(df1, df2) = ..., *p* = ..., η² = ...).
  * `Think:` Are the symbols correctly italicized? Is the p-value reported exactly?
* **Action:** Paste the relevant ANOVA output table(s) to support your reported statistics.

### D. Decision and Conclusion

* **Decision:** Based on the p-value from the main ANOVA test (Part C) and α = 0.05, decide whether to reject or fail to reject the null hypothesis (H₀). Justify your decision.
* **Conclusion:** Translate your statistical decision back into a clear answer to the original research question about executive function and education level.

### E. Post Hoc Analysis (Conditional)

* **Necessity:** `Think:` When are post-hoc tests actually needed after an ANOVA? Consider two factors: 1) Was the overall ANOVA significant? 2) How many groups does your IV have?
* **If Necessary:**
  1. Choose an appropriate test (e.g., Tukey if variances are equal, Games-Howell if unequal - remember Levene's test result!).
     * `Hint:` Post-hoc tests are selected within the `One-Way ANOVA` dialog box.
  2. Interpret the "Multiple Comparisons" output table. Which specific group pairs show a significant difference (p ≤ .05)?
  3. Answer E1 (which test used) and E2 (describe significant/non-significant differences, citing p-values). Paste the table.
* **If Not Necessary:** Proceed to Part F.

### F. Graphing (Conditional)

* **Necessity:** If post-hoc tests were *not* required (based on your reasoning in Part E), visualize the group means.
* **Create Graph:** Use SPSS to generate a bar or line graph showing the mean EF1 for each EducR group.
  * `Hint:` `Graphs -> Chart Builder` is flexible. Drag the IV to the X-axis and the DV to the Y-axis (ensure it's set to display the Mean). `Legacy Dialogs` are another option.
* **Action:** Paste the graph, ensuring it has clear labels and a title.

---

## Part 3: Question 2 - Another One-Way ANOVA (Employment & Age)

**Research Question:** Is there an association between employment status (employed/unemployed) and age (age1) at the start of the study?

Follow the logic from Question 1 (Parts A-D), applying it to these new variables:
* DV = `age1`
* IV = `Employment Status`

* **A. Hypotheses & Variables:** Define for this specific question.
* **B. Assumption Check:** Run and interpret Levene's test for `age1` by `Employment Status`. Paste table, state conclusion about assumption.
* **C. Main ANOVA Results:** Run the ANOVA. Report F, df, p, and η² in APA format. Paste table(s).
* **D. Decision & Conclusion:** Make a decision about H₀ based on the p-value. Answer the research question about age and employment status.
* `Think:` Does this ANOVA require post-hoc tests? Why or why not? (Relates back to Q1 Part E logic).

---

## Part 4: Data Preparation (Q3 Dataset)

**Objective:** Import and prepare the dataset for the repeated measures analysis.

**Process:**

1. **Import:** Load the data from the "Q3data" worksheet ('page' 3) of the Excel file into a *new* or clean SPSS session.
2. **Check Variables:** Go to "Variable View". What "Measure" type is appropriate for the memory scores in each session? Are Value Labels needed here?
3. **Save:** Save this new SPSS data file (.sav) with a distinct name.

---

## Part 5: Question 3 - One-Way Repeated Measures ANOVA (Session & Memory Score)

**Research Question:** Does color memory performance change significantly across the three testing sessions?

**Concept:** We're now comparing means from the *same* individuals measured at multiple time points (within-subjects design).

### A. Assumption Check: Sphericity

* **Concept:** Repeated measures ANOVA has a specific assumption called sphericity, related to the variances of the differences between conditions. Mauchly's test evaluates this.
* **Test:** Perform the Repeated Measures ANOVA in SPSS.
  * `Hint:` This is found under `Analyze -> General Linear Model -> Repeated Measures`. You'll need to define your within-subjects factor (e.g., `session`, with 3 levels) and then assign the corresponding variables (`Session1_Score`, `Session2_Score`, `Session3_Score`) to the defined slots.
* **Interpretation:**
  1. Find Mauchly's Test of Sphericity in the output. Look at the p-value (Sig.).
  2. Compare p-value to α = 0.05.
  3. `Think:` The null hypothesis for Mauchly's test is that sphericity *holds*. What does a significant (p ≤ .05) or non-significant (p > .05) result mean for this assumption?
* **Action:** Paste the Mauchly's test table and state whether the assumption is met or violated.

### B. Main Repeated Measures ANOVA Results

* **Locate Key Table:** Find the "Tests of Within-Subjects Effects" table in your output.
* **Critical Step - Choose the Right Row:** Your interpretation depends on the Mauchly's test result from Part A.
  * If Sphericity Met (Mauchly's p > .05): Use the "Sphericity Assumed" row.
  * If Sphericity Violated (Mauchly's p ≤ .05): Use a corrected row. `Hint:` The Greenhouse-Geisser correction is commonly used and robust. Note how the df values might change.
* **Identify Statistics:** From the *correct* row, extract the F-statistic, the two df values, the p-value (Sig.), and the Partial Eta Squared (ηₚ² - a common effect size for RM ANOVA).
* **Report in APA Format:** Present these statistics using the correct format and symbols. Ensure your reported df match the row you chose (e.g., Greenhouse-Geisser dfs).
* **Action:** Paste the "Tests of Within-Subjects Effects" table.

### C. Answer the Research Question

* **Decision:** Based on the p-value from your chosen row in the "Tests of Within-Subjects Effects" table (Part B), decide whether to reject or fail to reject the null hypothesis (that mean scores are equal across all sessions).
* **Conclusion:** Answer the research question about whether color memory performance changed significantly across the sessions.

### D. Analyze Contrasts

* **Concept:** Even if the overall ANOVA isn't significant, specific comparisons between sessions might be. Contrasts test these specific hypotheses. "Simple" contrasts compare each level to a reference level (first or last).
* **Perform Contrasts:** If you didn't request them initially, re-run the RM ANOVA.
  * `Hint:` Use the `Contrasts` button in the Repeated Measures dialog. Select your within-subjects factor (`session`) and choose the `Simple` contrast type. You need to specify whether the `First` or `Last` category is the reference point for comparison (the key seems to use `First`).
* **Interpret:**
  1. Examine the "Tests of Within-Subjects Contrasts" table.
  2. For each comparison listed (e.g., Level 2 vs. Level 1), look at the p-value (Sig.).
  3. `Think:` Which specific session comparisons show a statistically significant difference (p ≤ .05)? What does this imply about practice effects or changes between specific sessions?
* **Action:** Paste the contrasts table and discuss your observations, citing the specific p-values for each comparison you discuss.

---

## Video Talking Points Outline (Revised for Critical Thinking)

1. **Intro:** Purpose of ANOVA (comparing means); Introduce Between-Subjects vs. Repeated Measures designs. Goal: Apply & interpret correctly.
2. **Data Prep Philosophy:** Importance of accurate setup; `Variable View` (`Measure`, `Values`); Role of the Codebook. `Think: Why define these?`
3. **Q1: One-Way Between-Subjects**
   * Concept & Research Question. Identifying DV/IV. Formulating H₀.
   * Assumption: Homogeneity of Variances. `Think: Why check this?` Levene's test interpretation (p vs .05). `Hint: Look in ANOVA options.`
   * Main Test: The F-statistic (`Think: What does it represent?`). Interpreting the p-value. Effect Size (η²) (`Think: Why is significance not enough?`). APA format essentials.
   * Decision Making: Rejecting vs. Failing to Reject H₀ based on p-value. Answering the research question.
   * Follow-up Logic: `Think: When are post-hoc tests needed? (Sig. F AND >2 groups)`. Contrast with when a graph suffices. `Hint: Post-hoc options in ANOVA dialog; Graph Builder for visuals.`
4. **Q2: One-Way (2 Groups)**
   * Apply Q1 logic. `Think: How is this different from Q1 regarding post-hoc tests?` Connection to t-tests.
5. **Data Prep (Q3):** Quick setup for the next analysis.
6. **Q3: Repeated Measures ANOVA**
   * Concept: Within-subjects comparisons. `Think: How does the design differ from Q1/Q2?`
   * Assumption: Sphericity. `Think: What is this checking?` Mauchly's test interpretation. `Hint: Run via GLM -> Repeated Measures.`
   * Main Test: `Tests of Within-Subjects Effects`. `CRITICAL THINKING:` How does Mauchly's result dictate which row to read (Sphericity Assumed vs. Greenhouse-Geisser)? Reporting F, *corrected* df, p, partial η².
   * Interpretation & Conclusion regarding changes across sessions.
   * Contrasts: `Think: Why use contrasts even if overall F isn't significant?` How to run `Simple` contrasts. Interpreting specific comparisons (p vs .05). `Hint: Contrast button in RM dialog.`
7. **Wrap-up:** Recap core concepts. Emphasize connecting statistical results back to the research question. Submission checklist (Word doc, .sav files, .spv file). 