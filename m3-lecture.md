---
layout: lecture
title: M3 Lecture - Comparing Two Means
subtitle: Independent-Samples and Paired-Samples t-Tests
---

# M3 Lecture: Comparing Two Means

## Independent-Samples and Paired-Samples t-Tests

**Estimated Reading Time:** 45-60 minutes  
**Prerequisites:** M1 (Data Setup & Description), M2 (One-Sample t-Tests)

---

## Learning Objectives

By the end of this lecture, you will be able to:

1. **Distinguish between independent-samples and paired-samples designs** and choose the appropriate t-test
2. **Understand the conceptual foundation** of comparing two means using distributions of mean differences
3. **Execute and interpret independent-samples t-tests** including Levene's test for equality of variances
4. **Execute and interpret paired-samples t-tests** using the difference score approach
5. **Calculate and interpret effect sizes** (Cohen's d) for both types of t-tests
6. **Check and understand assumptions** underlying two-sample t-tests
7. **Report results in proper APA format** with complete statistical information
8. **Apply decision-making frameworks** to real-world research scenarios

---

## Table of Contents

1. [Introduction to Comparing Two Means](#part-1-introduction-to-comparing-two-means)
2. [Research Designs and the Critical Decision](#part-2-research-designs-and-the-critical-decision)
3. [The Independent-Samples t-Test](#part-3-the-independent-samples-t-test)
4. [The Paired-Samples t-Test](#part-4-the-paired-samples-t-test)
5. [Levene's Test Explained](#part-5-levens-test-explained)
6. [Effect Sizes for Comparing Means](#part-6-effect-sizes-for-comparing-means)
7. [Assumptions and Diagnostics](#part-7-assumptions-and-diagnostics)
8. [Putting It All Together](#part-8-putting-it-all-together)
9. [Practical Guide: SPSS](#part-9-practical-guide-spss)
10. [Summary and Key Formulas](#part-10-summary-and-key-formulas)

---

## Part 1: Introduction to Comparing Two Means

### The Evolution from One Sample to Two Samples

In M2, we learned to compare a single sample mean to a known population value using the one-sample t-test. Now we're taking the next logical step: **comparing two sample means to each other**. This is where most real-world research happens.

**The Fundamental Shift:**

- **M2 (One-Sample):** Compare sample mean (M) to known population mean (μ)
- **M3 (Two-Sample):** Compare sample mean 1 (M₁) to sample mean 2 (M₂)

### Why We Need Different Tests for Different Designs

When comparing two means, we face a critical question that didn't exist in one-sample testing: **What's the relationship between the data points in our two samples?**

This relationship is determined by your **research design**, and it fundamentally changes how we approach the statistical test:

- **Different people in each group** → Independent-Samples t-Test
- **Same people measured twice** → Paired-Samples t-Test

### The Core Challenge

With two samples, we have two challenges the one-sample test didn't have:

1. **Two means, one decision:** We have M₁ and M₂, but hypothesis testing requires evaluating a single value
2. **Two unknown populations:** Unlike M2 where we had a known population mean, both populations are hypothetical

**The Solution:** We shift our entire framework to focus on the **difference** between the groups.

- **New Research Question:** "Is the difference between Population A and Population B significantly different from 0?"
- **New Null Hypothesis:** "The difference between the two populations is 0 (they are the same)"
- **New Comparison Distribution:** A distribution of mean differences, centered at 0

### Real-World Examples

**Independent-Samples (Between-Subjects):**

- Comparing test scores of students who received tutoring vs. those who didn't
- Comparing salary between male and female employees
- Comparing reaction time between coffee drinkers and non-coffee drinkers

**Paired-Samples (Within-Subjects):**

- Measuring blood pressure before and after medication
- Comparing memory performance at age 70 vs. age 80
- Testing the same students before and after a training program

---

## Part 2: Research Designs and the Critical Decision

### The Golden Rule: One Group or Two?

The most important question you must ask is: **"Are the two sets of scores from the same people or from two different, unrelated groups?"**

This single question determines which t-test you will use.

### Between-Subjects Design → Independent-Samples t-Test

**What it is:** Two separate, unrelated groups of participants. Each person is in only one group.

**Characteristics:**

- Different individuals in each group
- No systematic relationship between participants
- Each participant contributes one score
- Groups are independent of each other

**Examples:**

- Treatment group vs. Control group
- Male vs. Female participants
- Experienced vs. Novice users
- High stress vs. Low stress conditions

**Advantages:**

- No carryover effects between conditions
- Participants can't figure out the hypothesis
- Simpler experimental setup

**Disadvantages:**

- Need more participants overall
- Individual differences between groups can mask effects
- Less statistical power (harder to detect true effects)

### Within-Subjects Design → Paired-Samples t-Test

**What it is:** The same individuals measured twice, or meaningfully linked pairs.

**Characteristics:**

- Same participants in both conditions
- Each participant contributes two scores
- Scores are naturally paired or dependent
- Individual differences are controlled

**Examples:**

- Before vs. After measurements
- Time 1 vs. Time 2
- Condition A vs. Condition B (same people)
- Matched pairs (twins, siblings, partners)

**Advantages:**

- Controls for individual differences
- More statistical power (easier to detect effects)
- Fewer participants needed
- More efficient use of resources

**Disadvantages:**

- Potential carryover effects
- Participants may figure out the hypothesis
- Dropout risk (need same people twice)
- Order effects (which condition comes first)

### Matched Pairs: A Special Case

Sometimes you have **natural pairs** that aren't the same person:

- Identical twins
- Siblings
- Spouses or partners
- Matched participants (same age, gender, education)

**Decision Rule:** If the pairs are meaningfully linked and you expect them to be more similar to each other than to random people, treat as **paired-samples**.

### The Decision Tree

```
Do you have the same people measured twice?
├─ YES → Paired-Samples t-Test
└─ NO
   ├─ Are the groups meaningfully matched?
   │  ├─ YES → Paired-Samples t-Test
   │  └─ NO → Independent-Samples t-Test
```

### Common Scenarios Practice

**Scenario 1:** A researcher wants to compare the effectiveness of two teaching methods. She randomly assigns 20 students to Method A and 20 different students to Method B.

- **Design:** Between-subjects
- **Test:** Independent-samples t-test

**Scenario 2:** A psychologist measures anxiety levels in 15 patients before and after therapy.

- **Design:** Within-subjects
- **Test:** Paired-samples t-test

**Scenario 3:** A researcher compares job satisfaction between 25 married couples, testing both the husband and wife.

- **Design:** Matched pairs (within-subjects)
- **Test:** Paired-samples t-test

**Scenario 4:** An education researcher compares reading scores between 30 third-grade boys and 30 third-grade girls.

- **Design:** Between-subjects
- **Test:** Independent-samples t-test

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Research Design Decisions</h4>

  <div class="quiz-question">
    <p><strong>Question 1:</strong> A researcher wants to test if a new study technique improves test scores. She has 40 students take a practice test, teaches them the new technique, then has the same 40 students take another practice test. What type of t-test should she use?</p>
    <div class="options">
      <p>A) Independent-samples t-test</p>
      <p>B) Paired-samples t-test</p>
      <p>C) One-sample t-test</p>
      <p>D) It depends on the sample size</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) Paired-samples t-test</p>

      <p class="explanation"><strong>Why this is correct:</strong> The same 40 students are measured twice - once before learning the technique and once after. This is a classic within-subjects (repeated measures) design where each participant contributes two scores that are naturally paired.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Independent-samples t-test:</strong> This would be used if different groups of students were compared (e.g., one group gets the technique, another doesn't).</li>
        <li><strong>C) One-sample t-test:</strong> This compares a single sample to a known population value, not two groups to each other.</li>
        <li><strong>D) Sample size:</strong> The type of test depends on the research design, not the sample size.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 2: Research Designs and the Critical Decision for the decision tree.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 2:</strong> A researcher compares memory performance between 20 identical twins, testing one twin from each pair under high-stress conditions and the other under low-stress conditions. What type of t-test is appropriate?</p>
    <div class="options">
      <p>A) Independent-samples t-test because they're different people</p>
      <p>B) Paired-samples t-test because they're meaningfully matched</p>
      <p>C) One-sample t-test because it's about memory</p>
      <p>D) Either independent or paired would work</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) Paired-samples t-test because they're meaningfully matched</p>

      <p class="explanation"><strong>Why this is correct:</strong> Identical twins are genetically identical and share similar environmental backgrounds, making them meaningfully matched pairs. They're expected to be more similar to each other than to random people, so their scores should be treated as dependent/paired.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Independent-samples:</strong> While they are different people, their genetic and environmental similarity makes them a matched pair, not independent groups.</li>
        <li><strong>C) One-sample t-test:</strong> This is still comparing two groups (high vs. low stress), not one group to a population.</li>
        <li><strong>D) Either would work:</strong> Using the wrong test would give incorrect results. The matched nature of twins requires paired-samples treatment.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> When in doubt, ask: "Are these participants more similar to each other than they would be to random people?" If yes, use paired-samples.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 3:</strong> Which of the following is a key advantage of within-subjects designs over between-subjects designs?</p>
    <div class="options">
      <p>A) They require fewer participants</p>
      <p>B) They have more statistical power</p>
      <p>C) They control for individual differences</p>
      <p>D) All of the above</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> D) All of the above</p>

      <p class="explanation"><strong>Why this is correct:</strong> Within-subjects designs have multiple advantages: they control for individual differences (each person serves as their own control), they have more statistical power (easier to detect true effects), and they require fewer participants overall since each person provides data for both conditions.</p>

      <p class="explanation"><strong>Individual advantages explained:</strong></p>
      <ul>
        <li><strong>Fewer participants:</strong> Each person contributes to both conditions, so you need half as many people as a between-subjects design.</li>
        <li><strong>More statistical power:</strong> By controlling individual differences, you eliminate "noise" that can hide true effects.</li>
        <li><strong>Control individual differences:</strong> Each person is compared to themselves, so factors like ability, motivation, and background are held constant.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 2: Research Designs and the Critical Decision for the advantages and disadvantages of each design.</p>
    </div>

  </details>
</div>

---

## Part 3: The Independent-Samples t-Test

### Conceptual Foundation

The independent-samples t-test works by creating a **distribution of mean differences**. Here's the key insight:

**If the null hypothesis is true** (the two populations have the same mean), then when we take many random samples from both populations and calculate the difference between their means, these differences should center around **0**.

**The Logic:**

1. We calculate the observed difference: M₁ - M₂
2. We compare this to a distribution of possible differences centered at 0
3. We ask: "How likely is it to get a difference this extreme if the populations are really the same?"

### The Mathematical Approach

**Test Statistic:**

```
t = (M₁ - M₂) / SE(M₁ - M₂)
```

Where:

- M₁ - M₂ = observed difference between sample means
- SE(M₁ - M₂) = standard error of the difference between means

**Standard Error Calculation:**
The formula for standard error depends on whether the two groups have equal variances:

**Equal Variances Assumed:**

```
SE = √[(s₁²/n₁) + (s₂²/n₂)]
```

**Equal Variances Not Assumed (Welch's t-test):**

```
SE = √[(s₁²/n₁) + (s₂²/n₂)]
```

(Note: The degrees of freedom calculation is different, but SPSS handles this automatically)

### Step-by-Step Process

**Step 1: State Your Hypotheses**

For a two-tailed test:

- H₀: μ₁ = μ₂ (population means are equal)
- H₁: μ₁ ≠ μ₂ (population means are different)

For a one-tailed test:

- H₀: μ₁ = μ₂
- H₁: μ₁ > μ₂ (or μ₁ < μ₂, depending on your prediction)

**Step 2: Check Assumptions**

- Independence of observations
- Normality (for each group)
- Homogeneity of variance (equal variances between groups)

**Step 3: Run Levene's Test**

- This tells you whether to assume equal variances
- p > .05: Use "Equal variances assumed" row
- p ≤ .05: Use "Equal variances not assumed" row

**Step 4: Calculate the t-statistic and p-value**

- SPSS does this automatically
- Use the appropriate row based on Levene's test

**Step 5: Make a decision**

- Compare p-value to α (usually .05)
- p ≤ .05: Reject H₀
- p > .05: Fail to reject H₀

**Step 6: Calculate effect size**

- Cohen's d = (M₁ - M₂) / pooled SD
- Interpret the magnitude of the effect

### Worked Example: Salary Comparison

**Research Question:** Do male and female employees have significantly different salaries?

**Hypotheses:**

- H₀: μ_male = μ_female
- H₁: μ_male ≠ μ_female

**Data:**

- Male employees: n₁ = 25, M₁ = $52,000, s₁ = $8,000
- Female employees: n₂ = 30, M₂ = $48,000, s₂ = $7,500

**Levene's Test Result:** p = .156 (not significant)

**t-test Results (Equal variances assumed):**

- t(53) = 1.89, p = .064, d = 0.52

**Interpretation:**

- Fail to reject H₀ (p > .05)
- The difference in salary is not statistically significant
- Effect size is medium (d = 0.52)

### Common Mistakes

**Mistake 1:** Forgetting to check Levene's test

- Always check which row to use before interpreting results

**Mistake 2:** Only reporting significance

- Always report the means and direction of difference

**Mistake 3:** Confusing statistical and practical significance

- A significant result doesn't guarantee practical importance
- Always consider effect size

**Mistake 4:** Using independent-samples when you should use paired-samples

- This is the most common error in M3
- Always verify your design choice

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Independent-Samples t-Test</h4>

  <div class="quiz-question">
    <p><strong>Question 1:</strong> In an independent-samples t-test, Levene's test has p = .023. Which row of the t-test output should you use?</p>
    <div class="options">
      <p>A) "Equal variances assumed"</p>
      <p>B) "Equal variances not assumed"</p>
      <p>C) Either row, they're the same</p>
      <p>D) It doesn't matter</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) "Equal variances not assumed"</p>

      <p class="explanation"><strong>Why this is correct:</strong> When Levene's test is significant (p ≤ .05), it means the assumption of equal variances is violated. Therefore, you must use the "Equal variances not assumed" row, which uses a modified calculation that doesn't assume the groups have equal variances.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) "Equal variances assumed":</strong> This row assumes the groups have equal variances, but Levene's test just told us they don't!</li>
        <li><strong>C) Either row:</strong> The rows can give different results. Using the wrong one can lead to incorrect conclusions.</li>
        <li><strong>D) It doesn't matter:</strong> It absolutely matters! Using the wrong assumption can affect your p-value and degrees of freedom.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Always check Levene's test first, then use the appropriate row. This is a critical step that many students miss!</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 2:</strong> An independent-samples t-test comparing two groups yields t(38) = 2.45, p = .019, d = 0.78. The mean for Group A is 85.2 and the mean for Group B is 78.9. How should you interpret this result?</p>
    <div class="options">
      <p>A) Group A is significantly higher than Group B, with a large effect size</p>
      <p>B) The difference is not significant because the means are close</p>
      <p>C) Group B is significantly higher than Group A</p>
      <p>D) The effect size is small</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> A) Group A is significantly higher than Group B, with a large effect size</p>

      <p class="explanation"><strong>Why this is correct:</strong> The p-value (.019) is less than .05, so the difference is statistically significant. Group A's mean (85.2) is higher than Group B's mean (78.9), so Group A is significantly higher. Cohen's d = 0.78 is considered a large effect size (typically d > 0.8 is large).</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>B) Not significant:</strong> p = .019 is less than .05, so it IS significant.</li>
        <li><strong>C) Group B higher:</strong> Group A's mean (85.2) > Group B's mean (78.9), so A is higher, not B.</li>
        <li><strong>D) Small effect:</strong> d = 0.78 is a large effect size, not small (small is typically d < 0.2).</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Always report the direction of difference by looking at which mean is higher, and interpret effect sizes using standard guidelines (small: d = 0.2, medium: d = 0.5, large: d = 0.8).</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 3:</strong> What is the null hypothesis for an independent-samples t-test?</p>
    <div class="options">
      <p>A) The two sample means are equal</p>
      <p>B) The two population means are equal</p>
      <p>C) The difference between means is zero</p>
      <p>D) Both B and C</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> D) Both B and C</p>

      <p class="explanation"><strong>Why this is correct:</strong> The null hypothesis states that the two population means are equal (μ₁ = μ₂). Since the population means are equal, their difference is zero (μ₁ - μ₂ = 0). These are two ways of expressing the same null hypothesis.</p>

      <p class="explanation"><strong>Why A is incorrect:</strong></p>
      <ul>
        <li><strong>A) Sample means equal:</strong> We don't test whether sample means are equal - we test whether population means are equal. Sample means will almost never be exactly equal due to sampling error.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 3: The Independent-Samples t-Test for the hypothesis testing framework.</p>
    </div>

  </details>
</div>

---

## Part 4: The Paired-Samples t-Test

### Why Paired-Samples Tests Are More Powerful

The paired-samples t-test has a major advantage: **it eliminates individual differences**. Here's why this matters:

**The Problem with Independent Groups:**
When you compare two different groups, individual differences (ability, motivation, background) create "noise" that can hide true effects. Even if your treatment works, these individual differences might make it hard to detect.

**The Solution with Paired Samples:**
By comparing each person to themselves, you control for all individual differences. This makes it much easier to detect true effects.

### The Difference Score Approach

The paired-samples t-test is clever because it transforms a two-sample problem back into a one-sample problem:

**Step 1:** Calculate difference scores for each pair

- Difference = Score_Time2 - Score_Time1
- Or: Difference = Score_ConditionA - Score_ConditionB

**Step 2:** Create a single sample of difference scores

**Step 3:** Run a one-sample t-test on the difference scores

- H₀: μ_difference = 0
- H₁: μ_difference ≠ 0

### Conceptual Foundation

**The Logic:**
If there's no real difference between conditions, the difference scores should center around 0. If there is a real difference, the difference scores should be systematically positive or negative.

**Test Statistic:**

```
t = M_difference / SE_difference
```

Where:

- M_difference = mean of the difference scores
- SE_difference = standard error of the difference scores

### Step-by-Step Process

**Step 1: Calculate Difference Scores**
For each participant, calculate: D = X₂ - X₁

**Step 2: State Your Hypotheses**

- H₀: μ_difference = 0 (no difference between conditions)
- H₁: μ_difference ≠ 0 (there is a difference between conditions)

**Step 3: Check Assumptions**

- Independence of observations
- Normality of difference scores
- (No homogeneity of variance assumption needed)

**Step 4: Calculate the t-statistic**

- t = M_difference / (s_difference / √n)
- df = n - 1 (where n is the number of pairs)

**Step 5: Make a decision**

- Compare p-value to α
- Interpret the direction based on the sign of M_difference

### Worked Example: Memory Decline

**Research Question:** Do executive function scores decline significantly from age 70 to age 80?

**Data (first 5 participants):**

```
Participant  Age70  Age80  Difference
1            95     89     -6
2            92     88     -4
3            98     90     -8
4            87     85     -2
5            94     91     -3
```

**Calculations:**

- n = 20 pairs
- M_difference = -4.2
- s_difference = 2.8
- SE_difference = 2.8 / √20 = 0.626

**t-test:**

- t = -4.2 / 0.626 = -6.71
- df = 19
- p < .001

**Interpretation:**

- Reject H₀ (p < .001)
- Executive function scores significantly decline from age 70 to 80
- The negative difference score confirms the decline

### When to Use vs. Avoid Paired-Samples

**Use Paired-Samples When:**

- Same participants measured twice
- Natural pairs (twins, siblings)
- Matched participants
- You want maximum power to detect effects

**Avoid Paired-Samples When:**

- Carryover effects are likely
- Participants might figure out the hypothesis
- High dropout risk
- Order effects are a concern

### Advantages of Paired-Samples Design

1. **Controls individual differences:** Each person serves as their own control
2. **More statistical power:** Easier to detect true effects
3. **Fewer participants needed:** Each person contributes to both conditions
4. **Eliminates between-group confounds:** No need to worry about group differences

### Disadvantages of Paired-Samples Design

1. **Carryover effects:** First condition might affect second condition
2. **Demand characteristics:** Participants might figure out the hypothesis
3. **Order effects:** Which condition comes first might matter
4. **Dropout risk:** Need the same people for both measurements

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Paired-Samples t-Test</h4>

  <div class="quiz-question">
    <p><strong>Question 1:</strong> A researcher measures anxiety levels in 15 patients before and after therapy. The mean difference score is +8.5 points. What does this tell us?</p>
    <div class="options">
      <p>A) Anxiety increased after therapy</p>
      <p>B) Anxiety decreased after therapy</p>
      <p>C) There was no change in anxiety</p>
      <p>D) We need the p-value to know</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> A) Anxiety increased after therapy</p>

      <p class="explanation"><strong>Why this is correct:</strong> The positive difference score (+8.5) means that the "after" scores are higher than the "before" scores. Since difference = After - Before, a positive value indicates that anxiety levels increased after therapy.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>B) Anxiety decreased:</strong> A decrease would show a negative difference score (After - Before would be negative).</li>
        <li><strong>C) No change:</strong> No change would result in a difference score of 0.</li>
        <li><strong>D) Need p-value:</strong> The p-value tells us if the change is statistically significant, but the direction of change comes from the sign of the difference score.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Always pay attention to how you calculate difference scores. If Difference = Time2 - Time1, then positive values mean Time2 is higher. If Difference = Time1 - Time2, then positive values mean Time1 is higher.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 2:</strong> Why are paired-samples t-tests generally more powerful than independent-samples t-tests?</p>
    <div class="options">
      <p>A) They use fewer participants</p>
      <p>B) They eliminate individual differences</p>
      <p>C) They have simpler calculations</p>
      <p>D) They don't require normality assumptions</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) They eliminate individual differences</p>

      <p class="explanation"><strong>Why this is correct:</strong> By comparing each person to themselves, paired-samples tests control for all the individual differences (ability, motivation, background, etc.) that can create "noise" in independent-samples tests. This reduction in noise makes it easier to detect true effects.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Fewer participants:</strong> While this is true, it's not why they're more powerful. Power comes from controlling variables, not sample size.</li>
        <li><strong>C) Simpler calculations:</strong> The calculations aren't necessarily simpler, and simplicity doesn't affect statistical power.</li>
        <li><strong>D) Don't require normality:</strong> Both tests have normality assumptions, just for different things (individual scores vs. difference scores).</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 4: The Paired-Samples t-Test for why paired designs are more powerful.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 3:</strong> In a paired-samples t-test, what does the null hypothesis state?</p>
    <div class="options">
      <p>A) The two sample means are equal</p>
      <p>B) The mean of the difference scores is zero</p>
      <p>C) The two population means are equal</p>
      <p>D) Both B and C</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> D) Both B and C</p>

      <p class="explanation"><strong>Why this is correct:</strong> In a paired-samples t-test, the null hypothesis states that the mean of the difference scores is zero (μ_difference = 0). Since the difference scores represent the difference between the two conditions, if their mean is zero, it means the two population means are equal (μ₁ = μ₂). These are equivalent ways of stating the same null hypothesis.</p>

      <p class="explanation"><strong>Why A is incorrect:</strong></p>
      <ul>
        <li><strong>A) Sample means equal:</strong> We don't test whether sample means are equal. We test whether the population means are equal by examining the difference scores.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 4: The Paired-Samples t-Test for the hypothesis testing framework.</p>
    </div>

  </details>
</div>

---

## Part 5: Levene's Test Explained

### What is Levene's Test?

Levene's test is a **preliminary check** that determines whether the assumption of **homogeneity of variance** is met in independent-samples t-tests.

**The Assumption:** The variance (spread) of your outcome variable should be roughly the same in both groups.

**The Test:** Levene's test checks whether this assumption is violated.

### The Logic Behind Levene's Test

**Null Hypothesis of Levene's Test:**

- H₀: σ²₁ = σ²₂ (the variances of the two groups are equal in the population)

**Alternative Hypothesis:**

- H₁: σ²₁ ≠ σ²₂ (the variances of the two groups are not equal)

**Interpretation:**

- If p > .05: Fail to reject H₀ → Variances are equal → Use "Equal variances assumed" row
- If p ≤ .05: Reject H₀ → Variances are not equal → Use "Equal variances not assumed" row

### Why This Matters

The formula for the t-test is slightly different depending on whether the groups have equal variances:

**Equal Variances Assumed:**

- Uses a pooled estimate of variance
- Simpler calculation
- Standard degrees of freedom: df = n₁ + n₂ - 2

**Equal Variances Not Assumed (Welch's t-test):**

- Uses separate variance estimates for each group
- More complex calculation
- Adjusted degrees of freedom (usually lower)

### How to Read Levene's Test Output

**SPSS Output Example:**

```
Levene's Test for Equality of Variances
                    F      Sig.
Equal variances assumed    2.847   .098
Equal variances not assumed
```

**Interpretation:**

- F = 2.847, p = .098
- Since p > .05, we fail to reject the null hypothesis
- Conclusion: Variances are equal
- Action: Use the "Equal variances assumed" row for the t-test

### Common Misconceptions

**Misconception 1:** "Levene's test tells me if my t-test is significant"

- **Reality:** Levene's test only tells you which row to use. The t-test significance comes from the t-test itself.

**Misconception 2:** "If Levene's test is significant, my t-test is invalid"

- **Reality:** You just need to use the correct row. Both rows are valid, just based on different assumptions.

**Misconception 3:** "I should report Levene's test in my results"

- **Reality:** Levene's test is a preliminary check. Report the t-test results, not Levene's test.

### What to Do When Assumptions Are Violated

**If Levene's Test is Significant (p ≤ .05):**

1. **Don't panic!** This is common and not necessarily a problem.

2. **Use the correct row:** Switch to "Equal variances not assumed"

3. **Consider the implications:**

   - Your groups have different amounts of variability
   - This might indicate that the treatment affects not just the mean, but also the spread

4. **Report appropriately:** Mention that you used Welch's t-test due to unequal variances

### Example: Reading SPSS Output

**Scenario:** Comparing test scores between two teaching methods

**Levene's Test Output:**

```
Levene's Test for Equality of Variances
                    F      Sig.
Equal variances assumed    4.231   .043
Equal variances not assumed
```

**t-Test Output:**

```
Independent Samples Test
                    t      df    Sig. (2-tailed)    Mean Difference
Equal variances assumed    2.145  48    .037          5.2
Equal variances not assumed 2.089  41.2  .043          5.2
```

**Interpretation:**

1. Levene's test: F = 4.231, p = .043 (significant)
2. Since p ≤ .05, use "Equal variances not assumed" row
3. t-test result: t(41.2) = 2.089, p = .043
4. Conclusion: Significant difference between groups

### Tips for Success

1. **Always check Levene's test first** before interpreting the t-test
2. **Use the appropriate row** based on Levene's test result
3. **Don't report Levene's test** in your final results
4. **Consider why variances might be unequal** - it can provide additional insights

---

## Part 6: Effect Sizes for Comparing Means

### Why Effect Size Matters

Statistical significance tells us **whether** there's an effect, but effect size tells us **how big** the effect is. This is crucial for practical interpretation.

### Cohen's d for Independent-Samples t-Test

**Formula:**

```
d = (M₁ - M₂) / s_pooled
```

Where s_pooled is the pooled standard deviation:

**Equal Variances Assumed:**

```
s_pooled = √[((n₁-1)s₁² + (n₂-1)s₂²) / (n₁ + n₂ - 2)]
```

**Equal Variances Not Assumed:**

```
s_pooled = √[(s₁² + s₂²) / 2]
```

### Cohen's d for Paired-Samples t-Test

**Formula:**

```
d = M_difference / s_difference
```

Where:

- M_difference = mean of difference scores
- s_difference = standard deviation of difference scores

### Interpretation Guidelines

**Cohen's (1988) Guidelines:**

- **Small effect:** d = 0.2
- **Medium effect:** d = 0.5
- **Large effect:** d = 0.8

**Important Notes:**

- These are rough guidelines, not strict rules
- Context matters - what's "small" in one field might be "large" in another
- Always interpret in the context of your research question

### Worked Examples

**Independent-Samples Example:**

- Group A: M = 85.2, s = 12.4, n = 25
- Group B: M = 78.9, s = 11.8, n = 30
- s_pooled = √[((24)(12.4)² + (29)(11.8)²) / (25 + 30 - 2)] = 12.1
- d = (85.2 - 78.9) / 12.1 = 0.52 (medium effect)

**Paired-Samples Example:**

- M_difference = -4.2
- s_difference = 2.8
- d = -4.2 / 2.8 = -1.50 (very large effect)
- Note: The negative sign indicates direction, but effect size magnitude is 1.50

### Effect Size vs. Statistical Significance

**Key Distinction:**

- **Statistical significance:** Is the effect real (not due to chance)?
- **Effect size:** How big is the effect?

**Why Both Matter:**

- A statistically significant result might have a tiny effect size
- A large effect size might not be statistically significant (small sample)
- You need both pieces of information for complete interpretation

### Practical Significance

Effect sizes help us judge **practical significance**:

**Example:** A study finds that a new teaching method increases test scores by 2 points (d = 0.15, small effect).

**Questions to consider:**

- Is a 2-point increase meaningful in this context?
- What would it cost to implement this method?
- Are there other methods with larger effects?

### Reporting Effect Sizes

**APA Style:**

- Always report effect size alongside statistical significance
- Use the symbol _d_ (italicized)
- Include confidence intervals when possible

**Example:**
"A paired-samples t-test revealed that executive function scores at age 80 (M = 89.9, SD = 4.9) were significantly lower than at age 70 (M = 94.6, SD = 7.7), _t_(19) = 3.05, _p_ = .007, _d_ = 0.68."

---

## Part 7: Assumptions and Diagnostics

### Assumptions of Independent-Samples t-Test

**1. Independence of Observations**

- Each observation is independent of all others
- No participant contributes more than one score per group
- **How to check:** Review your research design
- **What to do if violated:** Consider the implications for your conclusions

**2. Normality**

- The outcome variable is normally distributed in each population
- **How to check:** Histograms, Q-Q plots, Shapiro-Wilk test
- **What to do if violated:**
  - Large samples (n > 30): Usually robust to violations
  - Small samples: Consider nonparametric alternatives (Mann-Whitney U)

**3. Homogeneity of Variance**

- The variances of the two populations are equal
- **How to check:** Levene's test
- **What to do if violated:** Use "Equal variances not assumed" row

### Assumptions of Paired-Samples t-Test

**1. Independence of Observations**

- Each pair of observations is independent of all other pairs
- **How to check:** Review your research design
- **What to do if violated:** Consider the implications

**2. Normality of Difference Scores**

- The difference scores are normally distributed
- **How to check:** Histogram or Q-Q plot of difference scores
- **What to do if violated:**
  - Large samples: Usually robust
  - Small samples: Consider Wilcoxon signed-rank test

**Note:** Paired-samples t-test does NOT require equal variances between the original groups.

### Checking Normality

**Visual Methods:**

- **Histogram:** Look for roughly bell-shaped distribution
- **Q-Q Plot:** Points should fall roughly on a straight line
- **Box Plot:** Look for symmetry and appropriate tail lengths

**Statistical Tests:**

- **Shapiro-Wilk test:** Good for small samples (n < 50)
- **Kolmogorov-Smirnov test:** Better for large samples
- **Interpretation:** p > .05 suggests normality

### What to Do When Assumptions Are Violated

**For Normality Violations:**

**Small Samples (n < 30):**

- Consider nonparametric alternatives
- Independent-samples: Mann-Whitney U test
- Paired-samples: Wilcoxon signed-rank test

**Large Samples (n ≥ 30):**

- t-tests are usually robust to normality violations
- Central Limit Theorem provides protection

**For Variance Violations (Independent-Samples Only):**

- Use "Equal variances not assumed" row
- This automatically handles the violation

### Robust Alternatives

**When Assumptions Are Severely Violated:**

**Independent-Samples:**

- **Mann-Whitney U test:** Nonparametric alternative
- Tests whether one group tends to have higher scores than the other
- Less powerful but more robust

**Paired-Samples:**

- **Wilcoxon signed-rank test:** Nonparametric alternative
- Tests whether the median difference is significantly different from zero
- Good alternative when difference scores are not normal

### Diagnostic Checklist

**Before Running Your t-Test:**

□ **Design Check:** Are you using the right test (independent vs. paired)?

□ **Independence:** Are observations truly independent?

□ **Normality:** Check histograms/Q-Q plots of outcome variables (or difference scores for paired)

□ **Variance:** Run Levene's test for independent-samples

□ **Sample Size:** Is your sample large enough for the assumptions?

**After Running Your Test:**

□ **Levene's Test:** Which row should you use?

□ **Effect Size:** Calculate and interpret Cohen's d

□ **Practical Significance:** Is the effect meaningful in context?

---

## Part 8: Putting It All Together

### The Decision Flowchart

```
Do you want to compare two means?
├─ NO → Use one-sample t-test (M2)
└─ YES
   ├─ Are the scores from the same people or matched pairs?
   │  ├─ YES → Paired-Samples t-Test
   │  │   ├─ Check normality of difference scores
   │  │   ├─ Run paired-samples t-test
   │  │   ├─ Calculate Cohen's d
   │  │   └─ Report results
   │  └─ NO → Independent-Samples t-Test
   │      ├─ Check normality for each group
   │      ├─ Run Levene's test
   │      ├─ Run independent-samples t-test
   │      ├─ Use appropriate row based on Levene's test
   │      ├─ Calculate Cohen's d
   │      └─ Report results
```

### Comparison Table: One-Sample vs. Independent vs. Paired

| Aspect              | One-Sample                         | Independent-Samples                      | Paired-Samples                           |
| ------------------- | ---------------------------------- | ---------------------------------------- | ---------------------------------------- |
| **Purpose**         | Compare sample to known population | Compare two different groups             | Compare same group twice                 |
| **Design**          | Single group                       | Between-subjects                         | Within-subjects                          |
| **Null Hypothesis** | μ = known value                    | μ₁ = μ₂                                  | μ_difference = 0                         |
| **Test Statistic**  | t = (M - μ) / SE                   | t = (M₁ - M₂) / SE                       | t = M_difference / SE                    |
| **Assumptions**     | Normality, Independence            | Normality, Independence, Equal variances | Normality of differences, Independence   |
| **Effect Size**     | Cohen's d = (M - μ) / s            | Cohen's d = (M₁ - M₂) / s_pooled         | Cohen's d = M_difference / s_difference  |
| **Power**           | Medium                             | Lower (due to individual differences)    | Higher (controls individual differences) |

### Common Scenarios and Solutions

**Scenario 1: Comparing Two Different Groups**

- **Example:** Male vs. female salaries
- **Design:** Between-subjects
- **Test:** Independent-samples t-test
- **Key Steps:** Check Levene's test, use appropriate row

**Scenario 2: Before and After Measurement**

- **Example:** Test scores before and after training
- **Design:** Within-subjects
- **Test:** Paired-samples t-test
- **Key Steps:** Calculate difference scores, check normality of differences

**Scenario 3: Matched Pairs**

- **Example:** Twin studies, married couples
- **Design:** Within-subjects (matched)
- **Test:** Paired-samples t-test
- **Key Steps:** Treat as paired, calculate difference scores

**Scenario 4: Multiple Time Points**

- **Example:** Baseline, 6 months, 12 months
- **Design:** Repeated measures
- **Test:** Repeated measures ANOVA (M4)
- **Note:** t-tests only compare two time points

### APA Reporting Template

**Independent-Samples t-Test:**
"An independent-samples t-test revealed that [Group A] (M = [mean], SD = [sd]) scored significantly [higher/lower] than [Group B] (M = [mean], SD = [sd]), t([df]) = [t-value], p = [p-value], d = [effect-size]."

**Paired-Samples t-Test:**
"A paired-samples t-test revealed that [Condition 2] scores (M = [mean], SD = [sd]) were significantly [higher/lower] than [Condition 1] scores (M = [mean], SD = [sd]), t([df]) = [t-value], p = [p-value], d = [effect-size]."

### Key Takeaways

1. **Design determines the test:** Always start by identifying your research design
2. **Check assumptions:** Don't skip the diagnostic steps
3. **Use the right row:** Levene's test tells you which output to trust
4. **Report completely:** Include means, significance, and effect size
5. **Consider practical significance:** Statistical significance isn't everything

---

## Part 9: Practical Guide: SPSS

### Independent-Samples t-Test in SPSS

**Step 1: Data Setup**

- Ensure your grouping variable has proper value labels
- Check that your continuous variable is set to "Scale" measure

**Step 2: Running the Test**

1. Go to `Analyze` → `Compare Means` → `Independent-Samples T Test`
2. Move your continuous variable to "Test Variable(s)"
3. Move your categorical variable to "Grouping Variable"
4. Click `Define Groups` and enter the values for your two groups
5. Click `Options` and check "Estimate effect sizes" (SPSS v27+)
6. Click `Continue` and `OK`

**Step 3: Reading the Output**

- **Group Statistics:** Shows means and standard deviations
- **Levene's Test:** Check the "Sig." column
- **Independent Samples Test:** Use the appropriate row based on Levene's test
- **Effect Sizes:** If requested, appears in a separate table

### Paired-Samples t-Test in SPSS

**Step 1: Data Setup**

- Ensure both variables are in the same row (same participant)
- Check that both variables are set to "Scale" measure

**Step 2: Running the Test**

1. Go to `Analyze` → `Compare Means` → `Paired-Samples T Test`
2. Select your first variable and then your second variable
3. They will appear as a pair in the "Paired Variables" box
4. Click `Options` and check "Estimate effect sizes" (SPSS v27+)
5. Click `OK`

**Step 3: Reading the Output**

- **Paired Samples Statistics:** Shows means and standard deviations for each variable
- **Paired Samples Correlations:** Shows correlation between the two variables
- **Paired Samples Test:** Shows the t-test results
- **Effect Sizes:** If requested, appears in a separate table

### Troubleshooting Common Issues

**Issue 1: "Grouping Variable has more than two groups"**

- **Solution:** Your grouping variable has more than two values
- **Fix:** Recode the variable or use a different grouping variable

**Issue 2: "No cases to process"**

- **Solution:** Check for missing data or incorrect group definitions
- **Fix:** Define groups correctly or handle missing data

**Issue 3: "Equal variances not assumed" row shows different results**

- **Solution:** This is normal! Use the row indicated by Levene's test
- **Fix:** Always check Levene's test first

**Issue 4: Effect size not showing**

- **Solution:** Your SPSS version might not have this option
- **Fix:** Calculate manually using the formulas provided

### Reading Output Tables

**Group Statistics Table (Independent-Samples):**

```
Group Statistics
Group        N    Mean    Std. Deviation    Std. Error Mean
Score   1.00   25    85.20    12.40           2.48
        2.00   30    78.90    11.80           2.15
```

**Independent Samples Test Table:**

```
Independent Samples Test
                    Levene's Test    t-test for Equality of Means
                    F      Sig.      t      df    Sig. (2-tailed)
Equal variances assumed    2.847   .098    2.145  48    .037
Equal variances not assumed                   2.089  41.2  .043
```

**Paired Samples Test Table:**

```
Paired Samples Test
                    Paired Differences
                    Mean    Std. Dev.    t      df    Sig. (2-tailed)
Pair 1  Var1-Var2   4.20    2.80        6.71   19    .000
```

### Best Practices

1. **Always check Levene's test first** before interpreting t-test results
2. **Request effect sizes** if your SPSS version supports it
3. **Save your output file** (.spv) along with your data file (.sav)
4. **Use value labels** for categorical variables to make output readable
5. **Check assumptions** before running tests
6. **Report means and standard deviations** along with significance tests

---

## Part 10: Summary and Key Formulas

### Key Concepts Review

**The Fundamental Question:** Are you comparing the same people twice (paired) or different people (independent)?

**Independent-Samples t-Test:**

- Use when comparing two different groups
- Must check Levene's test for equal variances
- Less powerful due to individual differences
- Formula: t = (M₁ - M₂) / SE(M₁ - M₂)

**Paired-Samples t-Test:**

- Use when comparing same people twice or matched pairs
- More powerful due to controlling individual differences
- Uses difference scores: t = M_difference / SE_difference
- No homogeneity of variance assumption needed

### Essential Formulas

**Independent-Samples t-Test:**

```
t = (M₁ - M₂) / SE(M₁ - M₂)

SE (equal variances) = √[(s₁²/n₁) + (s₂²/n₂)]

s_pooled = √[((n₁-1)s₁² + (n₂-1)s₂²) / (n₁ + n₂ - 2)]

df = n₁ + n₂ - 2
```

**Paired-Samples t-Test:**

```
t = M_difference / (s_difference / √n)

df = n - 1

d = M_difference / s_difference
```

**Effect Sizes:**

```
Independent: d = (M₁ - M₂) / s_pooled
Paired: d = M_difference / s_difference
```

### Decision Framework

1. **Identify your design:** Same people twice or different people?
2. **Choose your test:** Paired or independent?
3. **Check assumptions:** Normality, independence, equal variances (independent only)
4. **Run Levene's test:** If independent-samples
5. **Interpret results:** Use correct row, report effect size
6. **Report in APA style:** Include means, significance, effect size

### Common Mistakes to Avoid

1. **Using the wrong test:** Most common error in M3
2. **Ignoring Levene's test:** Always check which row to use
3. **Only reporting significance:** Include means and effect size
4. **Confusing statistical and practical significance:** Both matter
5. **Not checking assumptions:** Can invalidate your results

### Connections to Other Modules

**From M2:** One-sample t-test concepts apply to paired-samples (difference scores)
**To M4:** ANOVA extends t-tests to compare more than two groups
**To M5:** Two-way ANOVA allows for multiple independent variables
**To M6:** Regression provides more flexible modeling approaches

### Final Thoughts

The choice between independent-samples and paired-samples t-tests is one of the most important decisions in statistical analysis. Getting this right is crucial because:

1. **It affects your conclusions:** Wrong test = wrong results
2. **It affects your power:** Paired tests are more sensitive
3. **It affects your assumptions:** Different tests have different requirements
4. **It affects your interpretation:** Different tests answer different questions

Remember: **The research design determines the statistical test, not the other way around.** Always start with your research question and design, then choose the appropriate statistical approach.

---

## Glossary

**Between-Subjects Design:** A research design where different participants are assigned to different conditions.

**Cohen's d:** A standardized measure of effect size representing the difference between means in standard deviation units.

**Difference Score:** The result of subtracting one measurement from another for the same participant (used in paired-samples t-tests).

**Effect Size:** A measure of the magnitude or practical significance of a statistical result, independent of sample size.

**Homogeneity of Variance:** The assumption that the variances of different groups are equal.

**Independent-Samples t-Test:** A statistical test used to compare the means of two different, unrelated groups.

**Levene's Test:** A statistical test that checks whether the assumption of equal variances is met in independent-samples t-tests.

**Matched Pairs:** Participants who are meaningfully linked (e.g., twins, siblings, spouses) and expected to be more similar to each other than to random people.

**Paired-Samples t-Test:** A statistical test used to compare the means of the same participants measured twice or meaningfully matched pairs.

**Pooled Standard Deviation:** A weighted average of the standard deviations from two groups, used in independent-samples t-tests.

**Within-Subjects Design:** A research design where the same participants are measured under different conditions.

---

_This lecture provides a comprehensive foundation for understanding and applying t-tests for comparing two means. Practice with real data and always remember that statistical analysis begins with understanding your research design._
