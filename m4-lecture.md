---
layout: lecture
title: "Module 4: Analysis of Variance (ANOVA)"
---

# Module 4: Analysis of Variance (ANOVA)

## Comparing Multiple Groups with Statistical Power

**Estimated Study Time:** 2-3 hours

## Learning Objectives

By the end of this module, you will be able to:

1. Explain why ANOVA is necessary when comparing three or more groups and the problems with multiple t-tests
2. Understand the core logic of ANOVA through the F-ratio and variance decomposition
3. Distinguish between one-way between-groups and one-way repeated-measures ANOVA designs
4. Identify independent and dependent variables in ANOVA research scenarios
5. Calculate and interpret degrees of freedom for between-groups and within-groups designs
6. Understand and check the assumptions of ANOVA, including homogeneity of variances and sphericity
7. Interpret ANOVA output from SPSS, including F-statistics, p-values, and effect sizes
8. Determine when post-hoc tests are warranted and interpret their results
9. Calculate and interpret eta squared (η²) as a measure of effect size
10. Report ANOVA results in proper APA format
11. Select the appropriate ANOVA design based on research questions and study design

---

## Table of Contents

1. [Introduction to ANOVA: Why We Need It](#part-1-introduction-to-anova-why-we-need-it)
2. [The F-Ratio: Core Logic of ANOVA](#part-2-the-f-ratio-core-logic-of-anova)
3. [One-Way Between-Groups ANOVA](#part-3-one-way-between-groups-anova)
4. [Post-Hoc Tests: Finding Specific Differences](#part-4-post-hoc-tests-finding-specific-differences)
5. [One-Way Repeated-Measures ANOVA](#part-5-one-way-repeated-measures-anova)
6. [Effect Size for ANOVA: Eta Squared](#part-6-effect-size-for-anova-eta-squared)
7. [ANOVA Assumptions](#part-7-anova-assumptions)
8. [SPSS Practical Guide](#part-8-spss-practical-guide)
9. [Decision Framework and Reporting](#part-9-decision-framework-and-reporting)
10. [Summary and Key Formulas](#summary-and-key-formulas)

---

## Part 1: Introduction to ANOVA - Why We Need It

### The Problem with Multiple t-Tests

Imagine you're a researcher studying the effectiveness of three different teaching methods on student performance. You have three groups:

- Group 1: Traditional lecture
- Group 2: Interactive discussion
- Group 3: Hands-on activities

Your first instinct might be to run three separate t-tests:

- Traditional vs. Interactive
- Traditional vs. Hands-on
- Interactive vs. Hands-on

**This approach has a critical flaw: the multiple comparisons problem.**

### The Multiple Comparisons Problem

When you run multiple statistical tests on the same data, the probability of making at least one Type I error (false positive) increases dramatically.

**With one test at α = .05:**

- Probability of Type I error = .05 (5%)

**With three tests at α = .05 each:**

- Probability of at least one Type I error = 1 - (1 - .05)³ = .143 (14.3%)

**With k tests:**

- Probability of at least one Type I error = 1 - (1 - α)^k

This inflation of Type I error rate is unacceptable in statistical analysis.

> **⚠️ THE MULTIPLE COMPARISONS PROBLEM: Why ANOVA is Essential**
>
> **The Risk:** Running multiple t-tests on the same data inflates Type I error dramatically!
>
> - 1 test at α = .05 → 5% error rate ✓
> - 3 tests at α = .05 → 14.3% error rate ⚠️
> - 10 tests at α = .05 → 40% error rate ❌
>
> **The Solution:** ANOVA tests all groups simultaneously in one test
> - Maintains α = .05 across all comparisons
> - Then uses "protected" post-hoc tests if significant
>
> **Remember:** Never run multiple t-tests when you have 3+ groups!

### The ANOVA Solution

**Analysis of Variance (ANOVA)** solves this problem by:

1. **Testing all groups simultaneously** in a single omnibus test
2. **Controlling Type I error** at the desired level (typically .05)
3. **Following up with protected comparisons** (post-hoc tests) only when the omnibus test is significant

### Research Scenarios Requiring ANOVA

> **🔗 Connection to Module 3:** Remember independent-samples t-tests from Module 3? They compare TWO groups. ANOVA extends this logic to THREE OR MORE groups, while controlling Type I error. Think of ANOVA as the "big sibling" of the t-test!

**When to Use ANOVA:**

- Comparing **3 or more groups** on a continuous dependent variable
- Testing the effect of one independent variable with multiple levels
- Both between-subjects and within-subjects designs

**Quick Decision:**
- 2 groups → Use t-test (see [Module 3: Comparing Two Means](#))
- 3+ groups → Use ANOVA (this module)

**Examples:**

- Comparing effectiveness of 4 different teaching methods
- Testing impact of 3 dosage levels of a medication
- Measuring performance across 5 different time points
- Comparing satisfaction ratings across 6 different service providers

### Between-Groups vs. Within-Groups Designs

**Between-Groups (Independent-Samples) ANOVA:**

- Different participants in each group
- Each person experiences only one condition
- More participants needed overall
- Less statistical power

**Within-Groups (Repeated-Measures) ANOVA:**

- Same participants in all conditions
- Each person experiences all conditions
- Fewer participants needed overall
- More statistical power (controls for individual differences)

**Key Insight:** Within-groups designs are generally preferred because they control for individual differences, resulting in less error variance and greater statistical power.

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: ANOVA Fundamentals and Design Selection</h4>

  <div class="quiz-question">
    <p><strong>Question 1:</strong> A researcher can't just run multiple t-tests when the independent variable has more than two levels because as more statistical tests are run, _____.</p>
    <div class="options">
      <p>A) Degrees of freedom are lost</p>
      <p>B) The probability of making a Type I error in one of the tests increases</p>
      <p>C) It becomes harder and harder to reject the null hypothesis</p>
      <p>D) The probability of making a Type II error in one of the tests increases</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) The probability of making a Type I error in one of the tests increases</p>

      <p class="explanation"><strong>Why this is correct:</strong> When you run multiple t-tests on the same data, the probability of making at least one Type I error (false positive) increases dramatically. With three tests at α = .05, the probability of at least one Type I error becomes about 14.3%.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Degrees of freedom are lost:</strong> Degrees of freedom don't accumulate across multiple tests in this way.</li>
        <li><strong>C) Harder to reject null hypothesis:</strong> This is backwards—multiple tests actually make it easier to find significance by chance.</li>
        <li><strong>D) Type II error increases:</strong> The main concern is Type I error inflation, not Type II error.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 1: Introduction to ANOVA for the multiple comparisons problem.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 2:</strong> Which statement accurately captures why within-groups designs are preferred over between-groups designs?</p>
    <div class="options">
      <p>A) Loss of participants has a more significant negative impact on between-groups designs</p>
      <p>B) Control of extraneous variables is easier when using between-groups designs</p>
      <p>C) Within-groups designs take less time than between-groups designs</p>
      <p>D) Variability due to participants' differences is held constant across levels of the independent variable in within-groups design, resulting in less within-groups variability</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> D) Variability due to participants' differences is held constant across levels of the independent variable in within-groups design, resulting in less within-groups variability</p>

      <p class="explanation"><strong>Why this is correct:</strong> In within-groups designs, the same participants are measured across all conditions, so individual differences between people are held constant. This reduces the error variance, making it easier to detect real effects.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Participant loss impact:</strong> This is a practical consideration but not the main statistical advantage.</li>
        <li><strong>B) Easier control in between-groups:</strong> This is backwards—within-groups designs provide better control.</li>
        <li><strong>C) Takes less time:</strong> This may or may not be true and isn't the statistical advantage.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Within-groups designs are more powerful because they control for individual differences, reducing error variance.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 3:</strong> A researcher is interested in whether a sensitivity training class changes attitudes toward minority populations. The researcher assesses these attitudes in participants who have and have not had the sensitivity training class. Which research design should be used?</p>
    <div class="options">
      <p>A) One-way within-groups ANOVA</p>
      <p>B) Paired-samples t-test</p>
      <p>C) One-way between-groups ANOVA</p>
      <p>D) Independent-samples t-test</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> C) One-way between-groups ANOVA</p>

      <p class="explanation"><strong>Why this is correct:</strong> The researcher is comparing two different groups of people (those who have had training vs. those who have not). This is a between-groups design where different participants are in each condition.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Within-groups ANOVA:</strong> This would be used if the same people were measured before and after training.</li>
        <li><strong>B) Paired-samples t-test:</strong> This is for two conditions, not multiple groups, and would be within-subjects.</li>
        <li><strong>D) Independent-samples t-test:</strong> This would be appropriate if there were only two groups, but the question asks about ANOVA design.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 1: Introduction to ANOVA for distinguishing between-groups and within-groups designs.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 4:</strong> A researcher wants to examine people's preference for pets by having 10 people act as "foster owners" for four different types of family pets: dogs, cats, birds, and fish. The participants will foster each type of pet for one week, and a scale measure will be used to assess preference. Which research design should be used?</p>
    <div class="options">
      <p>A) One-way within-groups ANOVA</p>
      <p>B) Paired-samples t-test</p>
      <p>C) One-way between-groups ANOVA</p>
      <p>D) Independent-samples t-test</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> A) One-way within-groups ANOVA</p>

      <p class="explanation"><strong>Why this is correct:</strong> The same 10 people will experience all four conditions (fostering dogs, cats, birds, and fish). This is a within-subjects design where each participant serves in all conditions.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>B) Paired-samples t-test:</strong> This is for comparing two conditions, not four.</li>
        <li><strong>C) Between-groups ANOVA:</strong> This would be used if different people fostered each type of pet.</li>
        <li><strong>D) Independent-samples t-test:</strong> This is for two groups only, not four conditions.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Ask yourself: "Are the same people experiencing all conditions?" If yes, use within-groups design.</p>
    </div>

  </details>
</div>

---

## Part 2: The F-Ratio - Core Logic of ANOVA

### Understanding Variance Decomposition

ANOVA's power comes from its clever way of partitioning variance. All the variation in your data can be broken down into two components:

**Total Variance = Between-Groups Variance + Within-Groups Variance**

### Between-Groups Variance (Effect Variance)

This measures how much the group means differ from each other. It represents the **"signal"** - the variation we hope is caused by our independent variable.

**Formula:** SS_between / df_between

**What it captures:**

- Differences between treatment conditions
- Effects of your manipulation
- Systematic variation due to your IV

**Example:** If teaching method A produces an average score of 85, method B produces 75, and method C produces 95, there's substantial between-groups variance.

### Within-Groups Variance (Error Variance)

This measures how much individual scores vary within each group. It represents the **"noise"** - random variation that's not due to your treatment.

**Formula:** SS_within / df_within

**What it captures:**

- Individual differences between participants
- Random measurement error
- Uncontrolled extraneous variables

**Example:** Even within method A, students might score 80, 85, 90, etc. This within-group variation is your error variance.

### The Grand Mean

The **grand mean** is the mean of all scores in the study, regardless of which group they belong to.

**Formula:** Grand Mean = Sum of all scores / Total number of scores

**Importance:** Both between-groups and within-groups variance are calculated relative to the grand mean.

### The F-Ratio Logic

The F-statistic is simply:

**F = Between-Groups Variance / Within-Groups Variance = Effect / Error**

**Interpreting F-values:**

- **F ≈ 1:** The difference between groups (effect) is about the same as the random variation within groups (error). This suggests no real effect. **Fail to reject H₀.**

- **F > 1:** The difference between groups is larger than the random variation within groups. This suggests a real effect. **Reject H₀.**

- **F >> 1:** The effect is much larger than the error. This suggests a strong effect.

> **📊 UNDERSTANDING THE F-RATIO: The Signal-to-Noise Metaphor**
>
> **Think of F as a Signal-to-Noise Ratio:**
>
> **F = Signal / Noise = Between-Groups Variance / Within-Groups Variance**
>
> - **High F:** Strong signal (clear group differences) relative to noise (random variation)
> - **Low F:** Weak signal (small group differences) buried in noise
>
> **Practical Interpretation:**
> - F = 1.0 → Signal equals noise → No real effect
> - F = 3.5 → Signal is 3.5× stronger than noise → Probably significant
> - F = 10.0 → Signal is 10× stronger than noise → Very significant
>
> **Key Insight:** ANOVA asks "Are group differences bigger than random individual differences?"

### Why F Cannot Be Negative

F-statistics are calculated as ratios of variances, and variances are always positive (they're squared values). Therefore, F must always be ≥ 0.

**If you see a negative F-statistic, there has been a calculation error.**

### The F-Ratio in Practice

**Scenario:** Testing three teaching methods with the following results:

| Method | Mean Score | Standard Deviation |
| ------ | ---------- | ------------------ |
| A      | 85         | 8                  |
| B      | 75         | 7                  |
| C      | 95         | 9                  |

**Between-groups variance:** Large (means are quite different: 75, 85, 95)
**Within-groups variance:** Moderate (SDs around 7-9)
**F-ratio:** Large between-groups / moderate within-groups = Large F

This would likely result in a significant F-test, indicating that teaching method does affect performance.

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: F-Ratio and Variance Components</h4>

  <div class="quiz-question">
    <p><strong>Question 1:</strong> If an F statistic is negative, which of these is true?</p>
    <div class="options">
      <p>A) The difference among the group means is less than what would have occurred by chance</p>
      <p>B) The difference among the group means is greater than what would have occurred by chance</p>
      <p>C) The within-groups variance exceeds the between-groups variance</p>
      <p>D) There has been a calculation error</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> D) There has been a calculation error</p>

      <p class="explanation"><strong>Why this is correct:</strong> F-statistics are calculated as ratios of variances, and variances are always positive (they're squared values). Therefore, F must always be ≥ 0. A negative F-statistic indicates an error in calculation.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Less than chance:</strong> Even if differences are small, F would be small but positive, not negative.</li>
        <li><strong>B) Greater than chance:</strong> This would result in a large positive F, not negative.</li>
        <li><strong>C) Within exceeds between:</strong> This would result in F < 1 (small but positive), not negative.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 2: The F-Ratio - Core Logic of ANOVA for why F cannot be negative.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 2:</strong> The t and F distributions have something in common—the numerator of the test statistic _____.</p>
    <div class="options">
      <p>A) Represents what would be expected to happen by chance</p>
      <p>B) Contains a measure of variability within the various groups</p>
      <p>C) Is a squared number</p>
      <p>D) Contains a measure of difference among group means</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> D) Contains a measure of difference among group means</p>

      <p class="explanation"><strong>Why this is correct:</strong> Both t and F statistics have numerators that measure differences among means. For t-tests, it's the difference between two means. For F-tests, it's the variance among group means (which is based on differences among means).</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Expected by chance:</strong> The numerator measures actual differences, not what's expected by chance.</li>
        <li><strong>B) Within-group variability:</strong> This is typically in the denominator, not the numerator.</li>
        <li><strong>C) Squared number:</strong> While F uses squared values, this isn't what t and F have in common.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Both t and F statistics measure differences among means in their numerators, with variability measures in their denominators.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 3:</strong> The grand mean is the _____.</p>
    <div class="options">
      <p>A) Mean of all the scores in the study squared</p>
      <p>B) Average difference of each of the group means</p>
      <p>C) Average of each of the group means</p>
      <p>D) Mean of every score in the study, regardless of the sample</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> D) Mean of every score in the study, regardless of the sample</p>

      <p class="explanation"><strong>Why this is correct:</strong> The grand mean is calculated by taking all individual scores across all groups, adding them up, and dividing by the total number of scores. It's the overall average of all data points in the study.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Scores squared:</strong> The grand mean is not calculated using squared scores.</li>
        <li><strong>B) Average difference:</strong> This describes something else entirely, not the grand mean.</li>
        <li><strong>C) Average of group means:</strong> While this might give a similar result in some cases, it's not the definition of the grand mean.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 2: The F-Ratio - Core Logic of ANOVA for the grand mean definition.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 4:</strong> If between-groups variance is much larger than within-groups variance, we infer that the sample means are _____ one another, and we _____ the null hypothesis.</p>
    <div class="options">
      <p>A) Similar to; reject</p>
      <p>B) Different from; reject</p>
      <p>C) Similar to; fail to reject</p>
      <p>D) Different from; fail to reject</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) Different from; reject</p>

      <p class="explanation"><strong>Why this is correct:</strong> Large between-groups variance means the group means are quite different from each other. When between-groups variance is much larger than within-groups variance, F > 1, indicating a significant effect, so we reject the null hypothesis.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Similar; reject:</strong> If means were similar, between-groups variance would be small, and we'd fail to reject.</li>
        <li><strong>C) Similar; fail to reject:</strong> This would be correct if between-groups variance were small.</li>
        <li><strong>D) Different; fail to reject:</strong> If means are different (large between-groups variance), we should reject the null hypothesis.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Large between-groups variance relative to within-groups variance indicates real differences among groups, leading to rejection of the null hypothesis.</p>
    </div>

  </details>
</div>

---

## Part 3: One-Way Between-Groups ANOVA

### Research Design Requirements

**One-way between-groups ANOVA** is used when:

- You have **one independent variable** with **3 or more levels**
- Different participants are in each group (between-subjects design)
- You're comparing means on a continuous dependent variable

**Example Research Question:** "Do different teaching methods (lecture, discussion, hands-on) affect student test scores?"

### Identifying Variables

**Independent Variable (IV):** The variable you manipulate or categorize

- **Levels:** The different conditions or groups (e.g., lecture, discussion, hands-on)
- **Type:** Usually categorical/nominal

**Dependent Variable (DV):** The variable you measure

- **Type:** Must be continuous (interval or ratio)
- **Example:** Test scores, reaction times, ratings

### Hypotheses for One-Way ANOVA

**Null Hypothesis (H₀):**

- μ₁ = μ₂ = μ₃ = ... = μₖ
- "There is no significant difference among any of the group means"
- All groups have the same population mean

**Alternative Hypothesis (H₁):**

- Not H₀
- "At least one group mean is significantly different from another"
- **Important:** This is an "omnibus" test - it tells you that a difference exists somewhere, but not where

### Degrees of Freedom

**Between-Groups df:**

- df_between = k - 1
- Where k = number of groups
- Example: 3 groups → df_between = 2

**Within-Groups df:**

- df_within = N - k
- Where N = total number of participants, k = number of groups
- Example: 60 participants, 3 groups → df_within = 57

**Total df:**

- df_total = N - 1
- df_total = df_between + df_within

### The ANOVA Table

SPSS produces an ANOVA table with this structure:

| Source         | SS         | df  | MS         | F   | Sig.    |
| -------------- | ---------- | --- | ---------- | --- | ------- |
| Between Groups | SS_between | k-1 | MS_between | F   | p-value |
| Within Groups  | SS_within  | N-k | MS_within  |     |         |
| Total          | SS_total   | N-1 |            |     |         |

**Key Values to Extract:**

- **F-statistic:** MS_between / MS_within
- **p-value ("Sig."):** Probability of getting this F if H₀ is true
- **df:** (df_between, df_within) for reporting

### Homogeneity of Variances Assumption

**Levene's Test** checks whether the variances of the groups are equal.

**Interpretation:**

- **p > .05:** Equal variances assumed (assumption met)
- **p ≤ .05:** Equal variances not assumed (assumption violated)

**What to do if violated:**

- Report the violation in your results
- Consider using a more robust test (Welch's ANOVA)
- Transform the data if appropriate

> **🔍 LEVENE'S TEST: The "Backwards" Logic**
>
> **This confuses almost everyone at first!**
>
> **What you want:** Equal variances (assumption met)
> **What you need:** p > .05
>
> **Interpretation:**
> - **p > .05:** ✓ Assumption met (variances are equal)
> - **p ≤ .05:** ✗ Assumption violated (variances are NOT equal)
>
> **Why it's backwards:** In most tests, p < .05 is "good" (significant result). But for Levene's test, you WANT p > .05!
>
> **H₀ for Levene's test:** "Variances are equal"
> - p > .05 → Fail to reject → Variances are equal ✓
> - p < .05 → Reject → Variances are NOT equal ✗
>
> **Remember:** For assumption tests, you want HIGH p-values (> .05)!

### Reading ANOVA Output in SPSS

**Example Output:**

```
ANOVA
TestScores
                Sum of Squares    df    Mean Square    F      Sig.
Between Groups    1901.425        2      950.713      2.805   .048
Within Groups    51524.485       152     338.977
Total           53425.910        154
```

**What to extract:**

- **F = 2.805**
- **df = (2, 152)**
- **p = .048**
- **SS_between = 1901.425**
- **SS_total = 53425.910**

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Degrees of Freedom and ANOVA Table</h4>

  <div class="quiz-question">
    <p><strong>Question 1:</strong> Between-groups degrees of freedom is calculated by _____.</p>
    <div class="options">
      <p>A) Subtracting 1 from the number of subjects within each group and then adding those numbers together</p>
      <p>B) Multiplying the number of subjects by the number of conditions in the study and then subtracting 1</p>
      <p>C) Subtracting 1 from the total number of subjects in the study</p>
      <p>D) Subtracting 1 from the total number of groups in the study</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> D) Subtracting 1 from the total number of groups in the study</p>

      <p class="explanation"><strong>Why this is correct:</strong> Between-groups degrees of freedom = k - 1, where k is the number of groups. If you have 3 groups, df_between = 3 - 1 = 2.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Within each group:</strong> This describes how to calculate within-groups df, not between-groups df.</li>
        <li><strong>B) Total subjects × conditions:</strong> This doesn't match the correct formula for between-groups df.</li>
        <li><strong>C) Total subjects - 1:</strong> This is the formula for total df, not between-groups df.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 3: One-Way Between-Groups ANOVA for the degrees of freedom formulas.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 2:</strong> Within-groups degrees of freedom is calculated by _____.</p>
    <div class="options">
      <p>A) Subtracting 1 from the total number of groups in the study</p>
      <p>B) Multiplying the number of subjects by the number of conditions in the study and then subtracting 1</p>
      <p>C) For each condition, subtracting 1 from the number of subjects in that group and then adding together the totals for all the groups</p>
      <p>D) Subtracting 1 from the total number of subjects in the study</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> C) For each condition, subtracting 1 from the number of subjects in that group and then adding together the totals for all the groups</p>

      <p class="explanation"><strong>Why this is correct:</strong> Within-groups df = (n₁ - 1) + (n₂ - 1) + ... + (nₖ - 1) = N - k, where nᵢ is the number of subjects in group i, N is total subjects, and k is number of groups.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Groups - 1:</strong> This is the formula for between-groups df.</li>
        <li><strong>B) Subjects × conditions - 1:</strong> This doesn't match the correct formula.</li>
        <li><strong>D) Total subjects - 1:</strong> This is total df, not within-groups df.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Within-groups df = Total subjects - Number of groups. This represents the degrees of freedom for error variance.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 3:</strong> In an ANOVA table, the F-statistic is calculated as _____.</p>
    <div class="options">
      <p>A) SS_between / SS_within</p>
      <p>B) MS_between / MS_within</p>
      <p>C) df_between / df_within</p>
      <p>D) SS_total / df_total</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) MS_between / MS_within</p>

      <p class="explanation"><strong>Why this is correct:</strong> F = MS_between / MS_within, where MS = Mean Square = SS / df. This gives us the ratio of between-groups variance to within-groups variance.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) SS_between / SS_within:</strong> This would be incorrect because it doesn't account for degrees of freedom.</li>
        <li><strong>C) df_between / df_within:</strong> This would just give you a ratio of degrees of freedom, not variances.</li>
        <li><strong>D) SS_total / df_total:</strong> This would give you the grand mean squared, not the F-statistic.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 3: One-Way Between-Groups ANOVA for the ANOVA table structure.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 4:</strong> A researcher wants to know if there is a significant difference in the percentage of graduates going to college across three geographic locations (city, suburb, and town/rural). What is the dependent variable in this analysis?</p>
    <div class="options">
      <p>A) Geographic location</p>
      <p>B) Percentage of graduates going to college</p>
      <p>C) Type of community</p>
      <p>D) Number of graduates</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) Percentage of graduates going to college</p>

      <p class="explanation"><strong>Why this is correct:</strong> The dependent variable is what you're measuring - the outcome variable. In this case, the researcher is measuring the percentage of graduates going to college across different locations.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Geographic location:</strong> This is the independent variable - what the researcher is comparing across.</li>
        <li><strong>C) Type of community:</strong> This is another way of describing the independent variable (geographic location).</li>
        <li><strong>D) Number of graduates:</strong> This isn't what's being measured - it's the percentage that matters.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 3: One-Way Between-Groups ANOVA for identifying IV and DV.</p>
    </div>

  </details>
</div>

---

## Part 4: Post-Hoc Tests - Finding Specific Differences

### When Post-Hoc Tests Are Warranted

**Post-hoc tests are warranted when:**

1. You have **rejected the null hypothesis** in the omnibus F-test
2. There are **more than two groups** in your study
3. You want to know **which specific groups differ** from each other

**Remember:** A significant F-test only tells you that a difference exists somewhere among the groups, not where the differences are.

> **🎯 POST-HOC TESTS: When and Why**
>
> **CRITICAL RULE:** Only run post-hoc tests if the F-test is significant!
>
> **The Three Requirements:**
> 1. ✓ F-test must be significant (p ≤ .05)
> 2. ✓ Must have 3+ groups
> 3. ✓ Want to know which specific groups differ
>
> **Why this rule?**
> - Running post-hoc tests after non-significant F = "fishing" for significance
> - The significant F-test "protects" post-hoc tests from inflating error rate
> - Without significant F, there's nothing to follow up on!
>
> **Think of it as:** F-test is the gatekeeper. Only if it says "yes, differences exist" can you go investigate WHERE those differences are.

### The Problem Post-Hoc Tests Solve

**The Omnibus F-Test Limitation:**

- Significant F: "At least one group is different from another"
- But which groups? We don't know!

**Example:** F-test shows p < .05 for teaching methods A, B, C

- Possible differences: A vs. B, A vs. C, B vs. C, or all combinations
- We need post-hoc tests to find out

### Common Post-Hoc Tests

**Tukey's HSD (Honestly Significant Difference):**

- Most commonly used
- Controls familywise error rate
- Good for equal sample sizes
- Conservative (less likely to find false positives)

**Bonferroni:**

- More conservative than Tukey
- Good for small number of comparisons
- Divides alpha by number of comparisons

**Scheffe:**

- Most conservative
- Good for complex comparisons
- Less powerful than Tukey

### Interpreting Post-Hoc Output

**SPSS Post-Hoc Output Example:**

```
Multiple Comparisons
Dependent Variable: TestScores
Tukey HSD

(I) Method    (J) Method    Mean Difference (I-J)    Std. Error    Sig.    95% Confidence Interval
                                                                         Lower Bound    Upper Bound
Lecture       Discussion    -10.50*                 3.45          .015    -19.23        -1.77
              Hands-on      -15.20*                 3.45          .001    -23.93        -6.47
Discussion    Lecture        10.50*                 3.45          .015     1.77          19.23
              Hands-on       -4.70                  3.45          .456    -13.43         4.03
Hands-on      Lecture        15.20*                 3.45          .001     6.47          23.93
              Discussion     4.70                   3.45          .456    -4.03          13.43

* The mean difference is significant at the .05 level.
```

**Key Information:**

- **Mean Difference:** How much one group differs from another
- **Sig. (p-value):** Whether the difference is statistically significant
- **95% Confidence Interval:** Range of likely differences

### What a Significant F-Test Tells You

**Important Limitation:** When you reject the null hypothesis in ANOVA, you know:

- ✅ At least one group mean is different from another
- ❌ You don't know which specific groups differ
- ❌ You don't know the direction of differences
- ❌ You don't know how many pairs differ

**Example:** Lucille finds significant F for alcohol consumption effects on gaming style. She knows:

- ✅ Drinking affects gaming style somehow
- ❌ She doesn't know if more alcohol = more/less prosocial behavior
- ❌ She doesn't know if the effect is linear or more complex

> **🔗 How to Report Post-Hoc Results:** Once you've run post-hoc tests and identified specific differences, see [Part 9: Decision Framework and Reporting](#part-9-decision-framework-and-reporting) for APA format examples showing how to report both the omnibus F-test and post-hoc test results together.

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Post-Hoc Tests and Interpretation</h4>

  <div class="quiz-question">
    <p><strong>Question 1:</strong> A post hoc test is warranted when a researcher _____.</p>
    <div class="options">
      <p>A) Rejects the null hypothesis when performing an independent-groups t-test</p>
      <p>B) Has an a priori prediction about which group means will differ</p>
      <p>C) Fails to reject the null hypothesis in an ANOVA</p>
      <p>D) Rejects the null hypothesis and there are more than two groups</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> D) Rejects the null hypothesis and there are more than two groups</p>

      <p class="explanation"><strong>Why this is correct:</strong> Post-hoc tests are only needed when: (1) the omnibus F-test is significant (reject H₀), AND (2) there are more than two groups. This is because a significant F-test only tells you that differences exist somewhere, not where they are.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Independent t-test:</strong> T-tests only compare two groups, so you already know which groups differ.</li>
        <li><strong>B) A priori prediction:</strong> If you have specific predictions, you'd use planned comparisons, not post-hoc tests.</li>
        <li><strong>C) Fails to reject H₀:</strong> If the F-test isn't significant, there are no differences to explore with post-hoc tests.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 4: Post-Hoc Tests - Finding Specific Differences for when post-hoc tests are warranted.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 2:</strong> Lucille is interested in the effects of alcohol consumption on style of play while playing The Sims. She asks 15 college students to play under one of four conditions: no alcohol, 1 ounce, 2 ounces, or 3 ounces. She measures how prosocial their play style is (1-10 scale). After performing an ANOVA, she finds she can reject the null hypothesis. On this basis, what does Lucille know?</p>
    <div class="options">
      <p>A) She knows that greater levels of alcohol consumption are associated with a more prosocial style of play</p>
      <p>B) She knows that drinking any amount of alcohol affects the style of play</p>
      <p>C) She knows that moderate alcohol consumption is associated with prosocial play, but greater consumption is associated with antisocial play</p>
      <p>D) She knows that there is a difference among the groups somewhere, but she does not know where</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> D) She knows that there is a difference among the groups somewhere, but she does not know where</p>

      <p class="explanation"><strong>Why this is correct:</strong> A significant F-test in ANOVA is an "omnibus" test that only tells you that at least one group mean is different from another. It doesn't tell you which specific groups differ or the direction of the differences.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Greater alcohol = more prosocial:</strong> This assumes a specific pattern that the F-test doesn't reveal.</li>
        <li><strong>B) Any amount affects play:</strong> The F-test doesn't tell you that every amount has an effect, just that some amounts do.</li>
        <li><strong>C) Moderate vs. greater amounts:</strong> This assumes a specific pattern that requires post-hoc tests to determine.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Significant F-test = "Something is different somewhere." Post-hoc tests = "Here's exactly what's different."</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 3:</strong> Which of these is NOT an assumption of an ANOVA?</p>
    <div class="options">
      <p>A) Normally distributed populations</p>
      <p>B) Independent variable has only three levels</p>
      <p>C) Random selection for samples</p>
      <p>D) Samples come from populations with equal variances</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) Independent variable has only three levels</p>

      <p class="explanation"><strong>Why this is correct:</strong> ANOVA can handle independent variables with 3 or more levels (not just 3). There's no requirement that the IV must have exactly three levels.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Normal populations:</strong> This is a key assumption of ANOVA - populations should be normally distributed.</li>
        <li><strong>C) Random selection:</strong> This is an assumption - samples should be randomly selected from populations.</li>
        <li><strong>D) Equal variances:</strong> This is the homogeneity of variances assumption, tested with Levene's test.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 7: ANOVA Assumptions for all the key assumptions.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 4:</strong> What is the main purpose of post-hoc tests in ANOVA?</p>
    <div class="options">
      <p>A) To determine if the overall F-test is significant</p>
      <p>B) To identify which specific groups differ from each other</p>
      <p>C) To calculate effect size</p>
      <p>D) To check assumptions</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) To identify which specific groups differ from each other</p>

      <p class="explanation"><strong>Why this is correct:</strong> Post-hoc tests are follow-up tests that identify which specific pairs of groups are significantly different from each other after finding a significant omnibus F-test.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Determine F-test significance:</strong> The F-test itself tells you if the overall test is significant.</li>
        <li><strong>C) Calculate effect size:</strong> Effect size is calculated separately, typically as eta squared.</li>
        <li><strong>D) Check assumptions:</strong> Assumptions are checked before running the main ANOVA, not with post-hoc tests.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Think of post-hoc tests as "detective work" - they find the specific differences that the omnibus F-test detected.</p>
    </div>

  </details>
</div>

---

## Part 5: One-Way Repeated-Measures ANOVA

### When to Use Repeated-Measures ANOVA

**Repeated-measures ANOVA** is used when:

- The same participants are measured across multiple conditions
- You want to compare means across 3 or more time points or conditions
- You're interested in within-subject changes over time

**Example Research Questions:**

- "Do students' test scores improve across three exam periods?"
- "How does mood change across four seasons?"
- "Does reaction time decrease with practice across five sessions?"

### Advantages of Repeated-Measures Design

> **🔗 Comparison to Between-Groups:** Repeated-measures and between-groups ANOVA (see [Part 3](#part-3-one-way-between-groups-anova)) answer similar questions but with different designs. The key difference: same vs. different participants. Both use the F-ratio logic from [Part 2](#part-2-the-f-ratio-core-logic-of-anova), but repeated-measures removes individual differences from error variance, making it more powerful.

**1. Controls Individual Differences:**

- Each person serves as their own control
- Eliminates between-subject variability
- More statistical power

**2. Requires Fewer Participants:**

- Same people in all conditions
- More cost-effective
- Easier recruitment

**3. Reduces Error Variance:**

- Individual differences are held constant
- More sensitive to detecting effects

### The Sphericity Assumption

**Sphericity (Mauchly's Test):**

- Tests whether variances of differences between conditions are equal
- More complex than homogeneity of variances

**Interpretation:**

- **p > .05:** Sphericity assumed (assumption met)
- **p ≤ .05:** Sphericity not assumed (assumption violated)

**What to do if violated:**

- Use Greenhouse-Geisser correction
- Use Huynh-Feldt correction
- Report the violation

> **⚖️ SPHERICITY: The Unique Repeated-Measures Assumption**
>
> **What makes sphericity special:**
> - Only applies to repeated-measures ANOVA (NOT between-groups!)
> - More complex than homogeneity of variances
> - Tests equality of variance of DIFFERENCES between conditions
>
> **Mauchly's Test Interpretation:** (Same "backwards" logic as Levene's!)
> - **p > .05:** ✓ Assumption met (sphericity assumed)
> - **p ≤ .05:** ✗ Assumption violated (use corrections)
>
> **If violated, use corrections:**
> - **Greenhouse-Geisser:** More conservative, always works
> - **Huynh-Feldt:** Less conservative, better with larger samples
>
> **SPSS tip:** SPSS shows all corrections in output. Look at:
> - "Sphericity Assumed" row if Mauchly's p > .05
> - "Greenhouse-Geisser" row if Mauchly's p ≤ .05
>
> **Remember:** Sphericity is to repeated-measures what Levene's test is to between-groups!

### Degrees of Freedom in Repeated-Measures

**Between-Subjects df:**

- df_between_subjects = N - 1
- Where N = number of participants

**Within-Subjects df:**

- df_within_subjects = (k - 1) × (N - 1)
- Where k = number of conditions, N = number of participants

**Total df:**

- df_total = (N × k) - 1

### Reading Repeated-Measures Output

**Example Output:**

```
Tests of Within-Subjects Effects
Measure: TestScores

Source                    Type III Sum    df    Mean Square    F      Sig.
                          of Squares
Time                      Sphericity Assumed    245.800    2      122.900    8.425   .001
                          Greenhouse-Geisser     245.800    1.234   199.189    8.425   .004
                          Huynh-Feldt           245.800    1.267   194.030    8.425   .004
                          Lower-bound           245.800    1.000   245.800    8.425   .012
Error(Time)               Sphericity Assumed    291.200    20      14.560
                          Greenhouse-Geisser     291.200    12.344   23.595
                          Huynh-Feldt           291.200    12.667   22.988
                          Lower-bound           291.200    10.000   29.120
```

**Key Information:**

- **F = 8.425**
- **df = (2, 20)** for sphericity assumed
- **p = .001**

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Repeated-Measures ANOVA</h4>

  <div class="quiz-question">
    <p><strong>Question 1:</strong> A researcher wants to examine people's preference for pets by having 10 people act as "foster owners" for four different types of family pets: dogs, cats, birds, and fish. The participants will foster each type of pet for one week, and a scale measure will be used to assess preference. Which research design should be used?</p>
    <div class="options">
      <p>A) One-way within-groups ANOVA</p>
      <p>B) Paired-samples t-test</p>
      <p>C) One-way between-groups ANOVA</p>
      <p>D) Independent-samples t-test</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> A) One-way within-groups ANOVA</p>

      <p class="explanation"><strong>Why this is correct:</strong> The same 10 people will experience all four conditions (fostering dogs, cats, birds, and fish). This is a within-subjects design where each participant serves in all conditions.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>B) Paired-samples t-test:</strong> This is for comparing two conditions, not four.</li>
        <li><strong>C) Between-groups ANOVA:</strong> This would be used if different people fostered each type of pet.</li>
        <li><strong>D) Independent-samples t-test:</strong> This is for two groups only, not four conditions.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 5: One-Way Repeated-Measures ANOVA for when to use within-subjects designs.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 2:</strong> In repeated-measures ANOVA, the sphericity assumption is tested using:</p>
    <div class="options">
      <p>A) Levene's test</p>
      <p>B) Mauchly's test</p>
      <p>C) Shapiro-Wilk test</p>
      <p>D) Kolmogorov-Smirnov test</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) Mauchly's test</p>

      <p class="explanation"><strong>Why this is correct:</strong> Mauchly's test specifically tests the sphericity assumption in repeated-measures ANOVA. It checks whether the variances of differences between all pairs of conditions are equal.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Levene's test:</strong> This tests homogeneity of variances in between-subjects designs.</li>
        <li><strong>C) Shapiro-Wilk test:</strong> This tests normality of distributions.</li>
        <li><strong>D) Kolmogorov-Smirnov test:</strong> This also tests normality, not sphericity.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Sphericity is a unique assumption for repeated-measures designs, tested with Mauchly's test.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 3:</strong> Which statement accurately captures why within-groups designs are preferred over between-groups designs?</p>
    <div class="options">
      <p>A) Loss of participants has a more significant negative impact on between-groups designs</p>
      <p>B) Control of extraneous variables is easier when using between-groups designs</p>
      <p>C) Within-groups designs take less time than between-groups designs</p>
      <p>D) Variability due to participants' differences is held constant across levels of the independent variable in within-groups design, resulting in less within-groups variability</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> D) Variability due to participants' differences is held constant across levels of the independent variable in within-groups design, resulting in less within-groups variability</p>

      <p class="explanation"><strong>Why this is correct:</strong> In within-groups designs, the same participants are measured across all conditions, so individual differences between people are held constant. This reduces the error variance, making it easier to detect real effects.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Participant loss impact:</strong> This is a practical consideration but not the main statistical advantage.</li>
        <li><strong>B) Easier control in between-groups:</strong> This is backwards—within-groups designs provide better control.</li>
        <li><strong>C) Takes less time:</strong> This may or may not be true and isn't the statistical advantage.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Within-groups designs are more powerful because they control for individual differences, reducing error variance.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 4:</strong> A researcher wants to know if there is a significant difference in the percentage of graduates going to college across three geographic locations (city, suburb, and town/rural). What is the dependent variable in this analysis?</p>
    <div class="options">
      <p>A) Geographic location</p>
      <p>B) Percentage of graduates going to college</p>
      <p>C) Type of community</p>
      <p>D) Number of graduates</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) Percentage of graduates going to college</p>

      <p class="explanation"><strong>Why this is correct:</strong> The dependent variable is what you're measuring - the outcome variable. In this case, the researcher is measuring the percentage of graduates going to college across different locations.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Geographic location:</strong> This is the independent variable - what the researcher is comparing across.</li>
        <li><strong>C) Type of community:</strong> This is another way of describing the independent variable (geographic location).</li>
        <li><strong>D) Number of graduates:</strong> This isn't what's being measured - it's the percentage that matters.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 5: One-Way Repeated-Measures ANOVA for identifying IV and DV.</p>
    </div>

  </details>
</div>

---

## Part 6: Effect Size for ANOVA - Eta Squared

### Understanding Effect Size in ANOVA

**Effect size** tells us how much of the variance in the dependent variable is explained by the independent variable. Unlike p-values, effect sizes are not affected by sample size.

### Eta Squared (η²)

**Formula:** η² = SS_between / SS_total

**Interpretation:**

- **η² = .01:** Small effect (1% of variance explained)
- **η² = .06:** Medium effect (6% of variance explained)
- **η² = .14:** Large effect (14% of variance explained)

### Calculating Eta Squared from SPSS Output

**From the previous example:**

- SS_between = 1901.425
- SS_total = 53425.910
- η² = 1901.425 / 53425.910 = .036 (3.6% of variance explained)

### Partial Eta Squared

**Formula:** Partial η² = SS_between / (SS_between + SS_within)

**Use when:**

- You have multiple factors in your ANOVA
- You want to isolate the effect of one factor

### Reading Effect Size from SPSS

SPSS often provides effect size automatically in the output. Look for:

- **Eta Squared** column
- **Partial Eta Squared** column
- Values between 0 and 1

### Interpreting Effect Size

**Cohen's Guidelines for η²:**

- **Small:** η² = .01
- **Medium:** η² = .06
- **Large:** η² = .14

**Important:** These are guidelines, not rules. Context matters for interpretation.

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Effect Size and Reporting</h4>

  <div class="quiz-question">
    <p><strong>Question 1:</strong> Eta squared (η²) is calculated as _____.</p>
    <div class="options">
      <p>A) SS_between / SS_within</p>
      <p>B) SS_between / SS_total</p>
      <p>C) MS_between / MS_within</p>
      <p>D) df_between / df_total</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) SS_between / SS_total</p>

      <p class="explanation"><strong>Why this is correct:</strong> Eta squared = SS_between / SS_total. This tells you what proportion of the total variance is explained by the independent variable.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) SS_between / SS_within:</strong> This would be incorrect because it doesn't include all variance.</li>
        <li><strong>C) MS_between / MS_within:</strong> This is the F-statistic, not eta squared.</li>
        <li><strong>D) df_between / df_total:</strong> This would just give you a ratio of degrees of freedom, not variance explained.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 6: Effect Size for ANOVA - Eta Squared for the calculation formula.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 2:</strong> A researcher reports η² = .08 for their ANOVA. How should this be interpreted?</p>
    <div class="options">
      <p>A) Small effect size</p>
      <p>B) Medium effect size</p>
      <p>C) Large effect size</p>
      <p>D) Cannot be determined without more information</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) Medium effect size</p>

      <p class="explanation"><strong>Why this is correct:</strong> According to Cohen's guidelines, η² = .06 is medium effect size. Since .08 is between .06 and .14, it's closer to medium than large.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Small effect:</strong> Small effect is η² = .01, much smaller than .08.</li>
        <li><strong>C) Large effect:</strong> Large effect is η² = .14, and .08 is not quite there.</li>
        <li><strong>D) Cannot be determined:</strong> We have enough information to make a reasonable interpretation.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> η² = .08 means the IV explains 8% of the variance in the DV - a moderate amount.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 3:</strong> What is the main advantage of reporting effect size along with statistical significance?</p>
    <div class="options">
      <p>A) It makes the results more statistically significant</p>
      <p>B) It provides information about the practical importance of the effect</p>
      <p>C) It reduces the chance of Type I error</p>
      <p>D) It increases statistical power</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) It provides information about the practical importance of the effect</p>

      <p class="explanation"><strong>Why this is correct:</strong> Effect size tells you how big the effect is in practical terms, while p-values only tell you if the effect is statistically significant. A statistically significant result might be very small in practical terms.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) More statistically significant:</strong> Effect size doesn't change statistical significance.</li>
        <li><strong>C) Reduces Type I error:</strong> Effect size doesn't affect Type I error rates.</li>
        <li><strong>D) Increases power:</strong> Effect size doesn't increase statistical power.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Always report both statistical significance (p-value) and practical significance (effect size) for complete interpretation.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 4:</strong> In APA format, how should you report an ANOVA result with F(2, 57) = 3.45, p = .038, η² = .11?</p>
    <div class="options">
      <p>A) F(2, 57) = 3.45, p = .038, η² = .11</p>
      <p>B) F(2, 57) = 3.45, p = .038, eta squared = .11</p>
      <p>C) F(2, 57) = 3.45, p = .038, η² = .11</p>
      <p>D) All of the above are correct</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> D) All of the above are correct</p>

      <p class="explanation"><strong>Why this is correct:</strong> APA format accepts multiple ways of reporting effect size: the Greek letter η², "eta squared" spelled out, or both. The key is to be consistent within your paper.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A, B, C:</strong> Each of these formats is acceptable in APA style.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 6: Effect Size for ANOVA - Eta Squared for APA reporting guidelines.</p>
    </div>

  </details>
</div>

---

## Part 7: ANOVA Assumptions

### Key Assumptions of ANOVA

**1. Normality:**

- Populations from which samples are drawn should be normally distributed
- Most important for small samples (n < 30 per group)
- Less critical for large samples due to Central Limit Theorem

**2. Homogeneity of Variances (Between-Groups ANOVA):**

- All groups should have equal population variances
- Tested with Levene's test
- More important when sample sizes are unequal

**3. Independence of Observations:**

- Each observation should be independent of others
- Violated when participants are measured multiple times (use repeated-measures instead)
- Important for both between-groups and within-groups designs

**4. Random Selection:**

- Samples should be randomly selected from populations
- Important for generalizability
- Often violated in convenience samples

### Checking Assumptions

**Normality:**

- Visual inspection of histograms
- Q-Q plots
- Shapiro-Wilk test for small samples
- Kolmogorov-Smirnov test for large samples

**Homogeneity of Variances:**

- Levene's test (p > .05 = assumption met)
- Visual inspection of boxplots
- Compare standard deviations across groups

**Independence:**

- Review study design
- Ensure no participant appears in multiple groups
- Check for clustering effects

### What to Do When Assumptions Are Violated

**Normality Violations:**

- Transform the data (log, square root)
- Use non-parametric alternatives (Kruskal-Wallis)
- Proceed with caution if sample size is large

**Homogeneity Violations:**

- Use Welch's ANOVA (more robust)
- Transform the data
- Report the violation and proceed cautiously

**Independence Violations:**

- Use repeated-measures ANOVA instead
- Account for clustering in analysis
- Consider multilevel modeling

> **🔗 Where to Check These in SPSS:** See [Part 8: SPSS Practical Guide](#part-8-spss-practical-guide) for step-by-step instructions on how to check each assumption in SPSS. The Options dialog has settings for Levene's test (between-groups) and sphericity tests (repeated-measures).

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Assumptions and Homogeneity Tests</h4>

  <div class="quiz-question">
    <p><strong>Question 1:</strong> Which of these is NOT an assumption of an ANOVA?</p>
    <div class="options">
      <p>A) Normally distributed populations</p>
      <p>B) Independent variable has only three levels</p>
      <p>C) Random selection for samples</p>
      <p>D) Samples come from populations with equal variances</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) Independent variable has only three levels</p>

      <p class="explanation"><strong>Why this is correct:</strong> ANOVA can handle independent variables with 3 or more levels (not just 3). There's no requirement that the IV must have exactly three levels.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Normal populations:</strong> This is a key assumption of ANOVA - populations should be normally distributed.</li>
        <li><strong>C) Random selection:</strong> This is an assumption - samples should be randomly selected from populations.</li>
        <li><strong>D) Equal variances:</strong> This is the homogeneity of variances assumption, tested with Levene's test.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 7: ANOVA Assumptions for all the key assumptions.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 2:</strong> In an independent-samples ANOVA, Levene's test produces p = .023. What does this tell us about the assumption of equal variances?</p>
    <div class="options">
      <p>A) The assumption is met because p < .05</p>
      <p>B) The assumption is not met because p < .05</p>
      <p>C) The assumption is met because p > .05</p>
      <p>D) The assumption is not met because p > .05</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) The assumption is not met because p < .05</p>

      <p class="explanation"><strong>Why this is correct:</strong> Levene's test null hypothesis is that variances are equal. When p < .05, we reject this null hypothesis, concluding that variances are NOT equal. Therefore, the assumption of equal variances is violated.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Assumption met because p < .05:</strong> This is backwards. p < .05 means we reject equal variances, so the assumption is NOT met.</li>
        <li><strong>C) Assumption met because p > .05:</strong> This would be correct if p > .05, but here p = .023 < .05.</li>
        <li><strong>D) Assumption not met because p > .05:</strong> This is backwards. p > .05 would mean we fail to reject equal variances, so the assumption WOULD be met.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 7: ANOVA Assumptions for the interpretation of Levene's test.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 3:</strong> What should you do if the homogeneity of variances assumption is violated in ANOVA?</p>
    <div class="options">
      <p>A) Stop the analysis and report that ANOVA cannot be used</p>
      <p>B) Use Welch's ANOVA instead of regular ANOVA</p>
      <p>C) Transform the data to meet the assumption</p>
      <p>D) Both B and C are appropriate options</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> D) Both B and C are appropriate options</p>

      <p class="explanation"><strong>Why this is correct:</strong> When homogeneity of variances is violated, you can use Welch's ANOVA (which is more robust to this violation) or transform the data to try to meet the assumption. Both approaches are valid.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Stop analysis:</strong> This is too extreme - there are ways to address the violation.</li>
        <li><strong>B) Welch's ANOVA only:</strong> While this is good, data transformation is also a valid option.</li>
        <li><strong>C) Transform only:</strong> While this is good, Welch's ANOVA is also a valid option.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> When assumptions are violated, try multiple approaches and report what you did.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 4:</strong> Which assumption is most critical to check when using ANOVA with small sample sizes?</p>
    <div class="options">
      <p>A) Homogeneity of variances</p>
      <p>B) Normality</p>
      <p>C) Independence of observations</p>
      <p>D) Random selection</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) Normality</p>

      <p class="explanation"><strong>Why this is correct:</strong> Normality is most critical with small samples because the Central Limit Theorem doesn't apply as strongly. With large samples, violations of normality are less problematic.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Homogeneity of variances:</strong> Important but not as critical as normality for small samples.</li>
        <li><strong>C) Independence:</strong> Always important regardless of sample size.</li>
        <li><strong>D) Random selection:</strong> Important for generalizability but not as critical for the statistical test itself.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 7: ANOVA Assumptions for the importance of assumptions with different sample sizes.</p>
    </div>

  </details>
</div>

---

## Part 8: SPSS Practical Guide

### Running One-Way Between-Groups ANOVA in SPSS

**Step 1: Data Setup**

- Ensure your IV is coded as numbers (1, 2, 3, etc.)
- Ensure your DV is continuous
- Check for missing values

**Step 2: Run the Analysis**

1. Go to **Analyze** → **Compare Means** → **One-Way ANOVA**
2. Move your DV to the **Dependent List**
3. Move your IV to the **Factor** box
4. Click **Options** and check:
   - Descriptive statistics
   - Homogeneity of variance test (Levene's test)
   - Means plot
5. Click **Post Hoc** and select **Tukey** (if you have 3+ groups)
6. Click **Continue** and **OK**

**Step 3: Interpret Output**

- **Descriptives:** Check means and standard deviations
- **Test of Homogeneity of Variances:** Check Levene's test
- **ANOVA:** Check F-statistic, df, and p-value
- **Post Hoc Tests:** Check which groups differ significantly

### Running One-Way Repeated-Measures ANOVA in SPSS

**Step 1: Data Setup**

- Each condition should be a separate column
- Each row represents one participant
- No missing values allowed

**Step 2: Run the Analysis**

1. Go to **Analyze** → **General Linear Model** → **Repeated Measures**
2. Define your factor:
   - **Within-Subject Factor Name:** Enter a name (e.g., "Time")
   - **Number of Levels:** Enter number of conditions
   - Click **Add** and **Define**
3. Move your condition columns to the **Within-Subjects Variables** box
4. Click **Options** and check:
   - Descriptive statistics
   - Estimates of effect size
5. Click **Continue** and **OK**

**Step 3: Interpret Output**

- **Descriptive Statistics:** Check means and standard deviations
- **Mauchly's Test of Sphericity:** Check sphericity assumption
- **Tests of Within-Subjects Effects:** Check F-statistic and p-value
- **Pairwise Comparisons:** Check which conditions differ

### Common SPSS Issues and Solutions

**Issue 1: "Factor must be numeric"**

- **Solution:** Recode your IV as numbers (1, 2, 3, etc.)

**Issue 2: Missing values in repeated-measures**

- **Solution:** Remove participants with missing data or use imputation

**Issue 3: No post-hoc tests available**

- **Solution:** You need 3+ groups for post-hoc tests

**Issue 4: Sphericity violated**

- **Solution:** Use Greenhouse-Geisser or Huynh-Feldt corrections

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: SPSS Output and Decision Making</h4>

  <div class="quiz-question">
    <p><strong>Question 1:</strong> A researcher runs a one-way ANOVA and obtains F(2, 57) = 3.45, p = .038. What should they conclude?</p>
    <div class="options">
      <p>A) There is no significant difference among the groups</p>
      <p>B) There is a significant difference among the groups</p>
      <p>C) The effect size is large</p>
      <p>D) The assumption of equal variances is violated</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) There is a significant difference among the groups</p>

      <p class="explanation"><strong>Why this is correct:</strong> Since p = .038 < .05, the null hypothesis is rejected, indicating that there is a significant difference among the group means.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) No significant difference:</strong> This would be correct if p > .05, but here p = .038 < .05.</li>
        <li><strong>C) Large effect size:</strong> The F-statistic doesn't tell us about effect size - we need eta squared for that.</li>
        <li><strong>D) Equal variances violated:</strong> This would be determined by Levene's test, not the F-test.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 8: SPSS Practical Guide for interpreting ANOVA output.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 2:</strong> In SPSS output, where would you find the exact F-statistic value?</p>
    <div class="options">
      <p>A) In the Descriptives table</p>
      <p>B) In the ANOVA table</p>
      <p>C) In the Post Hoc Tests table</p>
      <p>D) In the Test of Homogeneity of Variances table</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) In the ANOVA table</p>

      <p class="explanation"><strong>Why this is correct:</strong> The F-statistic is reported in the main ANOVA table, along with degrees of freedom and p-value.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Descriptives:</strong> This table contains means and standard deviations, not F-statistics.</li>
        <li><strong>C) Post Hoc Tests:</strong> This table contains pairwise comparisons, not the overall F-statistic.</li>
        <li><strong>D) Homogeneity test:</strong> This table contains Levene's test results, not the main F-statistic.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Look for the "ANOVA" table in SPSS output to find the main F-statistic and p-value.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 3:</strong> A researcher obtains F(2, 57) = 3.45, p = .038 from their ANOVA. What should they do next?</p>
    <div class="options">
      <p>A) Stop the analysis since the result is significant</p>
      <p>B) Run post-hoc tests to identify which groups differ</p>
      <p>C) Check assumptions before proceeding</p>
      <p>D) Both B and C are appropriate</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> D) Both B and C are appropriate</p>

      <p class="explanation"><strong>Why this is correct:</strong> After finding a significant F-test, you should run post-hoc tests to identify which specific groups differ. You should also check assumptions to ensure the results are valid.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Stop analysis:</strong> A significant F-test only tells you that differences exist somewhere - you need post-hoc tests to find where.</li>
        <li><strong>B) Post-hoc only:</strong> While important, checking assumptions is also crucial for valid results.</li>
        <li><strong>C) Check assumptions only:</strong> While important, post-hoc tests are needed to identify specific differences.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Always follow up significant F-tests with post-hoc tests and assumption checks.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 4:</strong> In SPSS, which menu path would you use to run a one-way between-groups ANOVA?</p>
    <div class="options">
      <p>A) Analyze → General Linear Model → Univariate</p>
      <p>B) Analyze → Compare Means → One-Way ANOVA</p>
      <p>C) Analyze → General Linear Model → Repeated Measures</p>
      <p>D) Analyze → Nonparametric Tests → Independent Samples</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) Analyze → Compare Means → One-Way ANOVA</p>

      <p class="explanation"><strong>Why this is correct:</strong> The standard menu path for one-way between-groups ANOVA in SPSS is Analyze → Compare Means → One-Way ANOVA.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) GLM Univariate:</strong> This is for more complex designs, not simple one-way ANOVA.</li>
        <li><strong>C) Repeated Measures:</strong> This is for within-subjects designs, not between-groups.</li>
        <li><strong>D) Nonparametric:</strong> This is for non-parametric tests, not ANOVA.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 8: SPSS Practical Guide for the correct menu paths.</p>
    </div>

  </details>
</div>

---

## Part 9: Decision Framework and Reporting

### Making Statistical Decisions

**Step 1: Check Assumptions**

- Normality: Visual inspection, tests if needed
- Homogeneity of variances: Levene's test
- Independence: Review study design
- Random selection: Document sampling method

**Step 2: Run the Appropriate ANOVA**

- Between-groups: Different participants in each group
- Repeated-measures: Same participants in all conditions

**Step 3: Interpret the F-Test**

- **p ≤ .05:** Reject H₀, significant differences exist
- **p > .05:** Fail to reject H₀, no significant differences

**Step 4: Follow Up if Significant**

- Run post-hoc tests (Tukey, Bonferroni, etc.)
- Calculate effect size (eta squared)
- Interpret practical significance

**Step 5: Report Results**

- Use proper APA format
- Include all necessary statistics
- Discuss practical implications

### APA Format for ANOVA Results

**Between-Groups ANOVA:**
"A one-way between-groups ANOVA was conducted to compare the effectiveness of three teaching methods on student test scores. There was a statistically significant difference among the groups, F(2, 57) = 3.45, p = .038, η² = .11. Post-hoc comparisons using Tukey's HSD test indicated that the hands-on method (M = 85.2, SD = 8.1) was significantly more effective than the lecture method (M = 75.0, SD = 7.3), p = .015. The discussion method (M = 80.1, SD = 6.8) did not differ significantly from either other method."

**Repeated-Measures ANOVA:**
"A one-way repeated-measures ANOVA was conducted to compare test scores across three time points. There was a statistically significant difference among the time points, F(2, 20) = 8.43, p = .001, η² = .46. Post-hoc comparisons using Bonferroni correction indicated that scores at Time 3 (M = 85.2, SD = 8.1) were significantly higher than scores at Time 1 (M = 75.0, SD = 7.3), p = .001, and Time 2 (M = 80.1, SD = 6.8), p = .015."

### Complete Example Write-Up

**Research Question:** "Do different teaching methods affect student performance?"

**Method:** "A one-way between-groups ANOVA was conducted to compare the effectiveness of three teaching methods (lecture, discussion, hands-on) on student test scores. Participants were randomly assigned to one of three conditions (n = 20 per group)."

**Results:** "There was a statistically significant difference among the groups, F(2, 57) = 3.45, p = .038, η² = .11, indicating a medium effect size. Post-hoc comparisons using Tukey's HSD test revealed that the hands-on method (M = 85.2, SD = 8.1) was significantly more effective than the lecture method (M = 75.0, SD = 7.3), p = .015. The discussion method (M = 80.1, SD = 6.8) did not differ significantly from either other method."

**Discussion:** "The results suggest that hands-on teaching methods are more effective than traditional lecture methods for improving student performance. The medium effect size (η² = .11) indicates that teaching method explains 11% of the variance in test scores, which is practically meaningful."

### Additional APA Reporting Examples

**Example 2: Non-Significant Result (Between-Groups)**

"A one-way between-groups ANOVA was conducted to compare customer satisfaction across three store locations (downtown, suburban, rural). There was no statistically significant difference in satisfaction ratings among the three locations, F(2, 147) = 1.23, p = .295, η² = .02. All three locations showed similar satisfaction levels (downtown: M = 7.2, SD = 1.5; suburban: M = 7.5, SD = 1.4; rural: M = 7.0, SD = 1.6)."

**Example 3: Reporting Assumption Violations (Between-Groups)**

"A one-way between-groups ANOVA was conducted to compare productivity scores across three work environments. Levene's test indicated that the assumption of homogeneity of variances was violated, F(2, 87) = 4.25, p = .017. Therefore, Welch's ANOVA was used instead. Results showed a statistically significant difference among the groups, Welch's F(2, 56.3) = 8.45, p = .001, η² = .16. Post-hoc comparisons using Games-Howell test indicated that the open-office environment (M = 78.5, SD = 12.3) had significantly lower productivity than both the private-office (M = 92.1, SD = 8.7) and hybrid (M = 89.3, SD = 9.2) environments."

**Example 4: Repeated-Measures with Sphericity Violation**

"A one-way repeated-measures ANOVA was conducted to examine changes in anxiety scores across four therapy sessions. Mauchly's test indicated that the assumption of sphericity was violated, χ²(5) = 15.24, p = .009. Therefore, degrees of freedom were corrected using Greenhouse-Geisser estimates of sphericity (ε = .78). There was a statistically significant effect of therapy session on anxiety scores, F(2.34, 44.46) = 12.87, p < .001, η² = .40, indicating a large effect. Post-hoc pairwise comparisons with Bonferroni correction revealed that anxiety scores significantly decreased from Session 1 (M = 45.2, SD = 6.8) to Session 4 (M = 28.5, SD = 7.2), p < .001."

**Example 5: Multiple Comparisons with Detailed Post-Hoc Results**

"A one-way between-groups ANOVA was conducted to compare reading comprehension scores across four instructional methods (phonics-only, whole-language, balanced-literacy, and technology-enhanced). There was a statistically significant difference among the groups, F(3, 156) = 7.32, p < .001, η² = .12. Post-hoc comparisons using Tukey's HSD test revealed several significant differences:

- Balanced-literacy (M = 85.3, SD = 8.2) scored significantly higher than phonics-only (M = 76.8, SD = 9.1), p = .002
- Technology-enhanced (M = 88.1, SD = 7.5) scored significantly higher than both phonics-only, p < .001, and whole-language (M = 79.2, SD = 8.6), p = .001
- No significant difference was found between balanced-literacy and technology-enhanced approaches, p = .485

These results suggest that integrated approaches (balanced-literacy and technology-enhanced) are more effective for reading comprehension than single-strategy approaches."

### Common APA Reporting Errors to Avoid

❌ **ERROR 1: Not reporting effect size**
- Wrong: "F(2, 57) = 3.45, p = .038"
- Right: "F(2, 57) = 3.45, p = .038, η² = .11"

❌ **ERROR 2: Reporting post-hoc without mentioning the omnibus F-test**
- Wrong: "Tukey's HSD showed that Group A differed from Group B, p = .015"
- Right: "ANOVA revealed significant differences, F(2, 57) = 3.45, p = .038, η² = .11. Post-hoc comparisons using Tukey's HSD showed..."

❌ **ERROR 3: Not reporting what test was used**
- Wrong: "There was a significant difference among groups"
- Right: "A one-way between-groups ANOVA revealed a significant difference among groups"

❌ **ERROR 4: Forgetting to report assumption violations**
- Wrong: [Ignoring failed Levene's test]
- Right: "Levene's test indicated violated assumptions (p = .017), so Welch's ANOVA was used..."

❌ **ERROR 5: Not including descriptive statistics**
- Wrong: "Group A was significantly higher than Group B"
- Right: "Group A (M = 85.2, SD = 8.1) was significantly higher than Group B (M = 75.0, SD = 7.3)"

❌ **ERROR 6: Saying "proves" instead of "suggests"**
- Wrong: "The results prove that Method A is better"
- Right: "The results suggest that Method A is more effective"

### Quick Checklist for APA-Style ANOVA Reporting

When writing up your ANOVA results, include:

☐ **1. Name of test:** "A one-way [between-groups/repeated-measures] ANOVA"

☐ **2. Purpose:** "was conducted to compare [DV] across [IV with levels]"

☐ **3. Assumption checks:** Report Levene's test (between) or Mauchly's test (repeated)

☐ **4. Corrections if needed:** Welch's ANOVA or Greenhouse-Geisser correction

☐ **5. F-statistic:** F(df_between, df_within) = [value]

☐ **6. P-value:** p = [exact value] or p < .001

☐ **7. Effect size:** η² = [value]

☐ **8. Descriptive statistics:** Means and SDs for all groups

☐ **9. Post-hoc results:** Which groups differed (if omnibus F was significant)

☐ **10. Interpretation:** Practical meaning of findings

---

## 📋 Quick Reference Card: ANOVA at a Glance

### ANOVA Decision Tree

```
START: Do you have 3+ groups to compare?
    |
    ├─ NO → Use t-test (see Module 3)
    |
    └─ YES → Continue
        |
        Are the same participants in all conditions?
        |
        ├─ YES → ONE-WAY REPEATED-MEASURES ANOVA
        |    • Controls individual differences
        |    • More statistical power
        |    • Check Mauchly's test for sphericity
        |    • Use Greenhouse-Geisser if violated
        |    • SPSS: Analyze → General Linear Model → Repeated Measures
        |
        └─ NO → ONE-WAY BETWEEN-GROUPS ANOVA
             • Different participants per group
             • More participants needed
             • Check Levene's test for equal variances
             • Use Welch's ANOVA if violated
             • SPSS: Analyze → Compare Means → One-Way ANOVA
```

### Degrees of Freedom Quick Reference

| Design Type | df_between | df_within | df_total |
|------------|------------|-----------|----------|
| **Between-Groups** | k - 1 | N - k | N - 1 |
| **Repeated-Measures** | k - 1 | (k-1)(N-1) | (N×k) - 1 |

**Where:** k = number of groups/conditions, N = total number of participants

**Examples:**
- 3 groups, 60 participants (between): df = (2, 57)
- 4 conditions, 15 participants (repeated): df = (3, 42)

### Post-Hoc Test Selection Guide

| Test | When to Use | Conservativeness |
|------|-------------|------------------|
| **Tukey's HSD** | Equal sample sizes, most common | Moderate |
| **Bonferroni** | Few comparisons, want strict control | Very conservative |
| **Scheffe** | Complex comparisons, unequal n | Most conservative |

**⚠️ CRITICAL:** Only run post-hoc tests if F-test is significant (p ≤ .05)!

### Effect Size Interpretation (Eta Squared)

**Formula:** η² = SS_between / SS_total

| η² Value | Effect Size | Interpretation |
|----------|-------------|----------------|
| .01 | Small | IV explains 1% of variance |
| .06 | Medium | IV explains 6% of variance |
| .14 | Large | IV explains 14% of variance |

**Example:** η² = .08 means teaching method explains 8% of variance in test scores (medium effect)

### SPSS Menu Paths Quick Reference

**Between-Groups ANOVA:**
```
Analyze → Compare Means → One-Way ANOVA
↓
Options: ✓ Descriptive statistics
         ✓ Homogeneity of variance test
         ✓ Means plot
↓
Post Hoc: ✓ Tukey (most common)
```

**Repeated-Measures ANOVA:**
```
Analyze → General Linear Model → Repeated Measures
↓
Define Factor: Name = "Time" (or condition name)
               Number of Levels = [enter number]
↓
Options: ✓ Descriptive statistics
         ✓ Estimates of effect size
```

### Assumption Checklist

**All ANOVA Designs:**
- ☐ **Normality:** Visual inspection, tests if n < 30
- ☐ **Independence:** Check study design
- ☐ **Random selection:** Document sampling method

**Between-Groups ONLY:**
- ☐ **Homogeneity of variances:** Levene's test (want p > .05)

**Repeated-Measures ONLY:**
- ☐ **Sphericity:** Mauchly's test (want p > .05)

### Common Mistakes to Avoid

❌ **Running post-hoc tests when F is not significant**
   - Post-hoc tests are only valid after rejecting H₀

❌ **Ignoring assumption violations**
   - Always check Levene's test (between-groups) or Mauchly's test (repeated-measures)
   - Report violations and use corrections

❌ **Running multiple t-tests instead of ANOVA**
   - Inflates Type I error rate dramatically

❌ **Forgetting to report effect size**
   - Always report η² along with F-statistic

❌ **Misinterpreting "no difference"**
   - Failing to reject H₀ ≠ "groups are the same"
   - It means "not enough evidence of difference"

❌ **Wrong ANOVA type**
   - Same participants = Repeated-measures
   - Different participants = Between-groups

### APA Reporting Template

**Between-Groups:**
"A one-way between-groups ANOVA was conducted to compare [DV] across [IV: levels]. There was a [significant/non-significant] difference among the groups, F(df_between, df_within) = [F-value], p = [p-value], η² = [effect size]. Post-hoc comparisons using [test name] indicated that [specific findings]."

**Repeated-Measures:**
"A one-way repeated-measures ANOVA was conducted to compare [DV] across [IV: levels]. Mauchly's test indicated that the assumption of sphericity [was/was not] violated, χ²([df]) = [value], p = [p-value]. [If violated: Therefore, degrees of freedom were corrected using [correction].] There was a [significant/non-significant] effect, F(df_between, df_within) = [F-value], p = [p-value], η² = [effect size]."

### F-Ratio Interpretation

**F = Between-Groups Variance / Within-Groups Variance**

- **F ≈ 1:** Effect ≈ Error (no real difference) → Fail to reject H₀
- **F > 1:** Effect > Error (possible real difference) → Check p-value
- **F >> 1:** Effect >> Error (strong difference) → Likely reject H₀

**Remember:** F is always ≥ 0 (negative F = calculation error!)

### Key Decision Points

**1. Check Assumptions First**
   - Visual inspection + statistical tests
   - Document any violations

**2. Run Appropriate ANOVA**
   - Match design to research question
   - Use SPSS menu paths above

**3. Interpret F-Test**
   - p ≤ .05 → Reject H₀ → Run post-hoc tests
   - p > .05 → Fail to reject H₀ → Stop here

**4. Calculate Effect Size**
   - Always report η²
   - Interpret using guidelines above

**5. Report Results**
   - Use APA format templates
   - Include all necessary statistics
   - Discuss practical significance

---

## Summary and Key Formulas

### Key Concepts Covered

1. **ANOVA solves the multiple comparisons problem** by testing all groups simultaneously
2. **F-ratio = Between-groups variance / Within-groups variance** measures effect relative to error
3. **Between-groups designs** use different participants in each group
4. **Within-groups designs** use the same participants across all conditions
5. **Post-hoc tests** identify specific group differences after significant F-tests
6. **Effect size (eta squared)** measures practical significance
7. **Assumptions** must be checked for valid results

### Essential Formulas

**Degrees of Freedom:**

- Between-groups: df = k - 1
- Within-groups: df = N - k
- Total: df = N - 1

**F-Statistic:**

- F = MS_between / MS_within
- MS = SS / df

**Effect Size:**

- η² = SS_between / SS_total
- Partial η² = SS_between / (SS_between + SS_within)

**Post-Hoc Tests:**

- Tukey's HSD: Most commonly used
- Bonferroni: More conservative
- Scheffe: Most conservative

### Decision Tree

1. **How many groups?** 3+ → Use ANOVA
2. **Same or different participants?**
   - Same → Repeated-measures ANOVA
   - Different → Between-groups ANOVA
3. **Significant F-test?**
   - Yes → Run post-hoc tests
   - No → Report no significant differences
4. **Check assumptions** throughout the process

### Key Terms Glossary

- **ANOVA:** Analysis of Variance - statistical test for comparing 3+ means
- **F-ratio:** Test statistic for ANOVA (between-groups variance / within-groups variance)
- **Between-groups design:** Different participants in each condition
- **Within-groups design:** Same participants in all conditions
- **Post-hoc test:** Follow-up test to identify specific group differences
- **Eta squared (η²):** Effect size measure for ANOVA
- **Sphericity:** Assumption for repeated-measures ANOVA
- **Homogeneity of variances:** Assumption that all groups have equal variances
- **Levene's test:** Test for homogeneity of variances
- **Mauchly's test:** Test for sphericity assumption

---

**Congratulations!** You've completed the comprehensive Module 4 on Analysis of Variance. You now have the knowledge and skills to:

- Understand when and why to use ANOVA
- Distinguish between between-groups and within-groups designs
- Interpret ANOVA output from SPSS
- Calculate and interpret effect sizes
- Check assumptions and handle violations
- Report results in proper APA format
- Make informed decisions about statistical analysis

Remember to practice these concepts with real data and always consider the practical implications of your statistical findings alongside their statistical significance.
