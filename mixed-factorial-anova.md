# Understanding Mixed Factorial ANOVA

**Goal:** To understand what a Mixed Factorial ANOVA is, when to use it, how to interpret its results, and why it's a useful tool in research.

## Introduction - What's the Big Idea?

### Topic: Comparing Group Means

- We often want to know if the average scores (means) of different groups are truly different.
- Tools like t-tests work for comparing two means.
- **ANOVA (Analysis of Variance)** is a family of tests designed to compare three or more means (though it can compare two).

### Introducing Mixed Factorial ANOVA:

- Think of it as a more complex type of ANOVA.
- It's specifically designed for situations where you have different kinds of groups or variables you're comparing simultaneously.
- The **"Factorial"** part means you have two or more predictor variables (factors).
- The **"Mixed"** part is the key: you have a mix of predictor variable types.

## The Building Blocks - Between vs. Within

To understand "Mixed," we need to know the two types of factors it mixes:

1.  **Between-Subjects Factor:**

    - Think: **Independent Groups**.
    - Each participant is in **ONLY ONE** level or group of this variable.
    - _Example:_ Comparing a 'Treatment Group' vs. a 'Control Group'. A person is either in the treatment group or the control group, not both.

2.  **Within-Subjects Factor:**
    - Think: **Repeated Measures**.
    - Each participant experiences **ALL** levels or conditions of this variable.
    - _Example:_ Measuring participants' scores at 'Pre-test', then again at 'Post-test'. The same people provide scores at both time points.

**The "Mix":** A Mixed Factorial ANOVA includes **at least one Between-Subjects factor AND at least one Within-Subjects factor** in the same analysis.

## When Do You Use It? The Setup

You need this specific setup:

- **One or more Between-Subjects categorical predictor variables** (e.g., Treatment vs. Control; Male vs. Female; Beginner vs. Expert).
- **One or more Within-Subjects categorical predictor variables** (e.g., Time 1 vs. Time 2 vs. Time 3; Condition A vs. Condition B).
- **One Continuous Outcome Variable:** The thing you are measuring (e.g., test scores, reaction time, anxiety level). This variable should be interval or ratio scale.

### Research Questions it Answers:

- Does the outcome differ between the independent groups (overall)? (**Main effect of Between-Subjects factor**)
- Does the outcome change across the repeated measures (overall)? (**Main effect of Within-Subjects factor**)
- **Most Importantly:** Does the effect of one factor depend on the level of the other factor? (**The Interaction Effect**)
  - _Example:_ Does the change in scores from pre-test to post-test (within-subjects) differ depending on whether someone was in the treatment or control group (between-subjects)?

## Checking the Foundations - Assumptions

Like any statistical test, Mixed Factorial ANOVA has rules (assumptions) that should ideally be met for the results to be trustworthy. The main ones are:

- **Normality:** The outcome variable should be roughly normally distributed within each "cell" (combination of factor levels).
- **Homogeneity of Variances:** The variance (spread) of the outcome variable should be roughly equal across the between-subjects groups.
- **Sphericity:** The variances of the differences between levels of the within-subjects factor should be roughly equal. (This is specific to within-subjects factors).

_(Note: Don't worry too much about the technical details now, just know these checks are important before fully trusting the results. Statistical software often helps check these.)_

## Decoding the Results - Significance & Interpretation

When you run a Mixed Factorial ANOVA, you'll typically look at three main things (using F-tests and associated p-values):

1.  **The Interaction Effect: ALWAYS LOOK AT THIS FIRST!**

    - It tells you if the effect of the within-subjects factor is different across the levels of the between-subjects factor (or vice-versa).
    - **Significant Interaction (p < .05):** The factors influence each other. The effect of one depends on the other. You need to investigate this further!
      - **Follow-up:** Use **Simple Effects tests**. (e.g., Look at the pre/post difference separately for the treatment group, then separately for the control group. Or, compare groups only at post-test).
    - **Non-Significant Interaction (p ≥ .05):** The factors are acting independently. The effect of one factor is roughly the same regardless of the level of the other factor. You can now interpret the main effects cleanly.

2.  **The Main Effect of the Between-Subjects Factor:**

    - _If the interaction was NOT significant, look here._ Does the outcome differ overall between your independent groups (averaging across the within-subjects levels)?
    - _Example:_ Overall, did the treatment group score differently than the control group (averaging pre- and post-test scores)?

3.  **The Main Effect of the Within-Subjects Factor:**
    - _If the interaction was NOT significant, look here._ Does the outcome differ overall across your repeated measures (averaging across the between-subjects groups)?
    - _Example:_ Overall, did scores change significantly from pre-test to post-test (averaging treatment and control groups)?

**Remember:** If the interaction is significant, the main effects can be misleading on their own. Focus on understanding the interaction via simple effects.

## Beyond "Significant" - Effect Size & Practical Meaning

- **Statistical Significance (p-value):** Tells you if an effect is likely real (not just due to chance).
- **Effect Size:** Tells you how big or meaningful the effect is. This is crucial for practical interpretation.
  - For overall effects (Main Effects, Interaction): Use **Eta Squared (η²)** or **Partial Eta Squared (ηp²)**. These represent the proportion of variance in the outcome explained by the factor/interaction. (Common benchmarks: .01=small, .09=medium, .25=large).
  - For specific comparisons (like in simple effects or comparing pairs of means): Use **Cohen's d**. This is a standardized difference between two means. (Common benchmarks: 0.2=small, 0.5=medium, 0.8=large).
- **Practical Significance:** Combine the p-value and effect size. Is the difference statistically significant _and_ large enough to matter in the real world?

## A Classic Example - Pre-test/Post-test Control Group

This is a perfect scenario for a 2x2 Mixed Factorial ANOVA:

- **Factor 1 (Between-Subjects):** Group (Level 1: Treatment, Level 2: Control)
- **Factor 2 (Within-Subjects):** Time (Level 1: Pre-test, Level 2: Post-test)
- **Outcome Variable:** Score on some measure (e.g., knowledge test, symptom rating)

**The Key Question (Interaction):** Did the change in scores from pre-test to post-test differ between the Treatment and Control groups?

- **If yes (significant interaction):** The training likely had an effect (or lack thereof) different from just the passage of time/practice seen in the control group. Examine the simple effects (how much did each group change?).
- **If no (non-significant interaction):** Both groups changed similarly over time.

## Special Case & Alternatives (The 2x2 Design)

For the specific case of a **2x2 Mixed Factorial ANOVA** (like the example above) with a **balanced design** (equal group sizes), there are statistically equivalent, sometimes simpler, alternatives:

- **Independent Samples t-test on Difference Scores:**
  1.  Calculate a "change score" for each person (Post-test Score - Pre-test Score).
  2.  Run an independent samples t-test comparing the average change score of the Treatment group to the average change score of the Control group.
  - This often directly answers the key interaction question in a very intuitive way for this specific design.

## Quick Review - Key Takeaways

- Mixed Factorial ANOVA compares means when you have both **between-subjects** (independent groups) and **within-subjects** (repeated measures) factors.
- You need **categorical predictors** and a **continuous outcome**.
- Always interpret the **interaction effect first**.
- If the interaction is significant, explore it with **simple effects**.
- If the interaction is not significant, interpret the **main effects**.
- Don't forget **effect sizes** (like partial η² and Cohen's d) to judge practical significance.
- The pre-test/post-test control group design is a classic example.
- In a **balanced 2x2 design**, a t-test on difference scores is often an easier, equivalent alternative.
