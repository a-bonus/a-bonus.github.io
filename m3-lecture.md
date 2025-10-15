---
layout: lecture
title: Module 3: Comparing Two Means
subtitle: Independent-Samples and Paired-Samples t-Tests
---

# Module 3: Comparing Two Means

## Independent-Samples and Paired-Samples t-Tests

**Estimated Study Time:** 1-2 hours  
**Prerequisites:** M1 (Data Setup & Description), M2 (One-Sample t-Tests)

---

## Learning Objectives

By the end of this module, you will be able to:

1. **Distinguish between independent-samples and paired-samples designs** and choose the appropriate t-test
2. **Understand the conceptual foundation** of comparing two means using distributions of mean differences
3. **Execute and interpret independent-samples t-tests** including Levene's test for equality of variances
4. **Execute and interpret paired-samples t-tests** using the difference score approach
5. **Calculate and interpret effect sizes** (Cohen's d) for both types of t-tests
6. **Check and understand assumptions** underlying two-sample t-tests
7. **Report results in proper APA format** with complete statistical information
8. **Apply decision-making frameworks** to real-world research scenarios

---

<div class="lecture-tabs">
    <div class="tab-navigation">
        <button class="tab-button active" onclick="showTab(1)">
            <input type="checkbox" id="progress-1" class="tab-checkbox" onchange="toggleTabComplete(1)">
            <span class="tab-label">Introduction & Research Designs</span>
        </button>
        <button class="tab-button" onclick="showTab(2)">
            <input type="checkbox" id="progress-2" class="tab-checkbox" onchange="toggleTabComplete(2)">
            <span class="tab-label">Independent-Samples t-Test</span>
        </button>
        <button class="tab-button" onclick="showTab(3)">
            <input type="checkbox" id="progress-3" class="tab-checkbox" onchange="toggleTabComplete(3)">
            <span class="tab-label">Paired-Samples t-Test</span>
        </button>
        <button class="tab-button" onclick="showTab(4)">
            <input type="checkbox" id="progress-4" class="tab-checkbox" onchange="toggleTabComplete(4)">
            <span class="tab-label">Effect Sizes & Assumptions</span>
        </button>
        <button class="tab-button" onclick="showTab(5)">
            <input type="checkbox" id="progress-5" class="tab-checkbox" onchange="toggleTabComplete(5)">
            <span class="tab-label">Application & Summary</span>
        </button>
    </div>
    
    <div class="tab-content">
        <div id="tab-1" class="tab-panel active">

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

> **⚠️ Critical Warning:** Choosing the wrong test (independent vs. paired) is the most common error in Module 3. Using the wrong test will give you incorrect results and invalid conclusions. Always verify your research design before selecting a test.

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

            <!-- Bottom Navigation -->
            <div class="tab-navigation bottom-nav">
                <button class="tab-button active" onclick="showTab(1)">
                    <input type="checkbox" id="progress-1-bottom" class="tab-checkbox" onchange="toggleTabComplete(1)">
                    <span class="tab-label">Introduction & Research Designs</span>
                </button>
                <button class="tab-button" onclick="showTab(2)">
                    <input type="checkbox" id="progress-2-bottom" class="tab-checkbox" onchange="toggleTabComplete(2)">
                    <span class="tab-label">Independent-Samples t-Test</span>
                </button>
                <button class="tab-button" onclick="showTab(3)">
                    <input type="checkbox" id="progress-3-bottom" class="tab-checkbox" onchange="toggleTabComplete(3)">
                    <span class="tab-label">Paired-Samples t-Test</span>
                </button>
                <button class="tab-button" onclick="showTab(4)">
                    <input type="checkbox" id="progress-4-bottom" class="tab-checkbox" onchange="toggleTabComplete(4)">
                    <span class="tab-label">Effect Sizes & Assumptions</span>
                </button>
                <button class="tab-button" onclick="showTab(5)">
                    <input type="checkbox" id="progress-5-bottom" class="tab-checkbox" onchange="toggleTabComplete(5)">
                    <span class="tab-label">Application & Summary</span>
                </button>
            </div>
        </div>

        <div id="tab-2" class="tab-panel">

## Part 3: The Independent-Samples t-Test

> **Before proceeding:** Make sure you've determined that independent-samples is the right test for your design (see [Part 2](#part-2-research-designs-and-the-critical-decision)). If your data involves the same people measured twice or matched pairs, you need the paired-samples t-test instead ([Part 4](#part-4-the-paired-samples-t-test)).

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
The approach differs depending on whether the two groups have equal variances:

**Equal Variances Assumed (Pooled Variance Method):**

```
s_pooled² = [(n₁-1)s₁² + (n₂-1)s₂²] / (n₁ + n₂ - 2)
SE = √[s_pooled² × (1/n₁ + 1/n₂)]
df = n₁ + n₂ - 2
```

This uses a weighted average (pooled variance) to estimate the common population variance.

**Equal Variances Not Assumed (Welch's t-test):**

```
SE = √[(s₁²/n₁) + (s₂²/n₂)]
df = (complex Welch-Satterthwaite approximation)
```

This uses each group's variance separately and adjusts the degrees of freedom. SPSS handles the df calculation automatically.

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

      <p class="explanation"><strong>Why this is correct:</strong> The p-value (.019) is less than .05, so the difference is statistically significant. Group A's mean (85.2) is higher than Group B's mean (78.9), so Group A is significantly higher. Cohen's d = 0.78 is approaching the 0.8 threshold for a large effect size and represents a medium-to-large effect.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>B) Not significant:</strong> p = .019 is less than .05, so it IS significant.</li>
        <li><strong>C) Group B higher:</strong> Group A's mean (85.2) > Group B's mean (78.9), so A is higher, not B.</li>
        <li><strong>D) Small effect:</strong> d = 0.78 is approaching a large effect size, not small (small is typically d = 0.2).</li>
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

            <!-- Bottom Navigation -->
            <div class="tab-navigation bottom-nav">
                <button class="tab-button" onclick="showTab(1)">
                    <input type="checkbox" id="progress-1-bottom" class="tab-checkbox" onchange="toggleTabComplete(1)">
                    <span class="tab-label">Introduction & Research Designs</span>
                </button>
                <button class="tab-button active" onclick="showTab(2)">
                    <input type="checkbox" id="progress-2-bottom" class="tab-checkbox" onchange="toggleTabComplete(2)">
                    <span class="tab-label">Independent-Samples t-Test</span>
                </button>
                <button class="tab-button" onclick="showTab(3)">
                    <input type="checkbox" id="progress-3-bottom" class="tab-checkbox" onchange="toggleTabComplete(3)">
                    <span class="tab-label">Paired-Samples t-Test</span>
                </button>
                <button class="tab-button" onclick="showTab(4)">
                    <input type="checkbox" id="progress-4-bottom" class="tab-checkbox" onchange="toggleTabComplete(4)">
                    <span class="tab-label">Effect Sizes & Assumptions</span>
                </button>
                <button class="tab-button" onclick="showTab(5)">
                    <input type="checkbox" id="progress-5-bottom" class="tab-checkbox" onchange="toggleTabComplete(5)">
                    <span class="tab-label">Application & Summary</span>
                </button>
            </div>
        </div>

        <div id="tab-3" class="tab-panel">

## Part 4: The Paired-Samples t-Test

> **Before proceeding:** Make sure you've determined that paired-samples is the right test for your design (see [Part 2](#part-2-research-designs-and-the-critical-decision)). If your data involves two completely different groups (not the same people), you need the independent-samples t-test instead ([Part 3](#part-3-the-independent-samples-t-test)).

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

> **💡 Important:** The order matters! If Difference = Time2 - Time1:
>
> - **Positive difference** means Time2 scores are higher
> - **Negative difference** means Time2 scores are lower (Time1 was higher)
>
> Always note which direction you're subtracting to interpret your results correctly.

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
   - Welch's t-test is more conservative and provides accurate results even with unequal variances

4. **Report appropriately:** Mention that you used Welch's t-test due to unequal variances

> **📝 Note:** Welch's t-test adjusts both the standard error calculation and the degrees of freedom to account for unequal variances. This makes it robust to violations of the homogeneity of variance assumption. The adjusted degrees of freedom are usually non-integer values (e.g., df = 41.2).

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

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Levene's Test and Variance Assumptions</h4>

  <div class="quiz-question">
    <p><strong>Question 1:</strong> In an independent-samples t-test, Levene's test produces p = .023. What does this tell us about the assumption of equal variances?</p>
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

      <p class="review-tip"><em>💭 Need to review?</em> See Part 5: Levene's Test - Understanding Homogeneity of Variance for the interpretation rules.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 2:</strong> Based on the Levene's test result in the previous question (p = .023), which row of the t-test output should you use?</p>
    <div class="options">
      <p>A) "Equal variances assumed" row</p>
      <p>B) "Equal variances not assumed" row</p>
      <p>C) Either row is acceptable</p>
      <p>D) You need to run the test again</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) "Equal variances not assumed" row</p>

      <p class="explanation"><strong>Why this is correct:</strong> Since Levene's test showed unequal variances (p = .023 < .05), you should use the "Equal variances not assumed" row, which applies Welch's correction for unequal variances.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) "Equal variances assumed" row:</strong> This row should only be used when Levene's test shows p > .05 (equal variances).</li>
        <li><strong>C) Either row is acceptable:</strong> You must use the appropriate row based on Levene's test results.</li>
        <li><strong>D) Run test again:</strong> The test is fine; you just need to use the correct row from the existing output.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Always check Levene's test first, then use the appropriate row. This ensures you're using the correct statistical procedure.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 3:</strong> A researcher reports that Levene's test showed F(1, 38) = 0.847, p = .364. What can be concluded about the variances?</p>
    <div class="options">
      <p>A) The two populations have equal variances</p>
      <p>B) The two populations have unequal variances</p>
      <p>C) The groups differ significantly in their means</p>
      <p>D) The groups do not differ significantly in their means</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> A) The two populations have equal variances</p>

      <p class="explanation"><strong>Why this is correct:</strong> Levene's test has p = .364 > .05, so we fail to reject the null hypothesis of equal variances. This means we can conclude that the assumption of equal variances is met.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>B) Unequal variances:</strong> This would be true if p < .05, but here p = .364 > .05.</li>
        <li><strong>C) Groups differ in means:</strong> Levene's test doesn't tell us about differences in means—only about differences in variances.</li>
        <li><strong>D) Groups don't differ in means:</strong> Again, Levene's test is about variances, not means.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 5.1: What is Levene's Test for what this test actually measures.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 4:</strong> In SPSS output for an independent-samples t-test, you see two rows of results. What determines which row you should use?</p>
    <div class="options">
      <p>A) The larger t-value</p>
      <p>B) The smaller p-value</p>
      <p>C) The result of Levene's test</p>
      <p>D) The sample sizes of the groups</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> C) The result of Levene's test</p>

      <p class="explanation"><strong>Why this is correct:</strong> The choice between "Equal variances assumed" and "Equal variances not assumed" rows depends entirely on Levene's test. If Levene's p > .05, use "assumed" row; if p < .05, use "not assumed" row.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Larger t-value:</strong> You don't choose based on which t-value is larger—you use the correct statistical procedure.</li>
        <li><strong>B) Smaller p-value:</strong> You don't cherry-pick the more significant result—you use the appropriate test.</li>
        <li><strong>D) Sample sizes:</strong> Sample sizes don't determine which row to use—only Levene's test does.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Always follow the statistical procedure correctly. Don't choose results based on what looks better—use the appropriate test for the data.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 5:</strong> What is the null hypothesis for Levene's test?</p>
    <div class="options">
      <p>A) The two groups have equal means</p>
      <p>B) The two groups have equal variances</p>
      <p>C) The two groups have different means</p>
      <p>D) The two groups have different variances</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) The two groups have equal variances</p>

      <p class="explanation"><strong>Why this is correct:</strong> Levene's test specifically tests the null hypothesis that the variances of the two groups are equal (homogeneity of variance). The alternative hypothesis is that the variances are unequal.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Equal means:</strong> This would be the null hypothesis for the t-test itself, not Levene's test.</li>
        <li><strong>C) Different means:</strong> This would be the alternative hypothesis for the t-test, not related to Levene's test.</li>
        <li><strong>D) Different variances:</strong> This is the alternative hypothesis for Levene's test, not the null hypothesis.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 5.1: What is Levene's Test for the specific hypotheses being tested.</p>
    </div>

  </details>
</div>

            <!-- Bottom Navigation -->
            <div class="tab-navigation bottom-nav">
                <button class="tab-button" onclick="showTab(1)">
                    <input type="checkbox" id="progress-1-bottom" class="tab-checkbox" onchange="toggleTabComplete(1)">
                    <span class="tab-label">Introduction & Research Designs</span>
                </button>
                <button class="tab-button" onclick="showTab(2)">
                    <input type="checkbox" id="progress-2-bottom" class="tab-checkbox" onchange="toggleTabComplete(2)">
                    <span class="tab-label">Independent-Samples t-Test</span>
                </button>
                <button class="tab-button active" onclick="showTab(3)">
                    <input type="checkbox" id="progress-3-bottom" class="tab-checkbox" onchange="toggleTabComplete(3)">
                    <span class="tab-label">Paired-Samples t-Test</span>
                </button>
                <button class="tab-button" onclick="showTab(4)">
                    <input type="checkbox" id="progress-4-bottom" class="tab-checkbox" onchange="toggleTabComplete(4)">
                    <span class="tab-label">Effect Sizes & Assumptions</span>
                </button>
                <button class="tab-button" onclick="showTab(5)">
                    <input type="checkbox" id="progress-5-bottom" class="tab-checkbox" onchange="toggleTabComplete(5)">
                    <span class="tab-label">Application & Summary</span>
                </button>
            </div>
        </div>

        <div id="tab-4" class="tab-panel">

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

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Effect Sizes for Two-Sample Tests</h4>

  <div class="quiz-question">
    <p><strong>Question 1:</strong> A study found statistically significant results for a hypothesis tested with an independent-samples t-test. The author reported the effect size as 1.24. What is true of the two sample means?</p>
    <div class="options">
      <p>A) The two sample means overlap 85 percent</p>
      <p>B) The two sample means are 1.24 standard deviations apart</p>
      <p>C) The two sample means likely come from the same distribution</p>
      <p>D) The two sample means do not indicate meaningful differences between groups</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) The two sample means are 1.24 standard deviations apart</p>

      <p class="explanation"><strong>Why this is correct:</strong> Cohen's d measures the standardized difference between means. A d = 1.24 means the two sample means are 1.24 standard deviation units apart, which is a very large effect size.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Overlap 85 percent:</strong> A large effect size (d = 1.24) means LESS overlap, not more. Large effects mean the distributions are well-separated.</li>
        <li><strong>C) Same distribution:</strong> If means are 1.24 SDs apart, they clearly don't come from the same distribution.</li>
        <li><strong>D) No meaningful differences:</strong> A d = 1.24 is a very large effect, indicating highly meaningful differences between groups.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 6.2: Cohen's d for Independent-Samples t-Tests for the interpretation of effect sizes.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 2:</strong> What would be the effect size interpretation for Cohen's d = 0.50 in a paired-samples t-test?</p>
    <div class="options">
      <p>A) Small effect</p>
      <p>B) Medium effect</p>
      <p>C) Large effect</p>
      <p>D) Very large effect</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) Medium effect</p>

      <p class="explanation"><strong>Why this is correct:</strong> According to Cohen's (1988) guidelines: d = 0.2 is small, d = 0.5 is medium, and d = 0.8 is large. This applies to both independent-samples and paired-samples t-tests.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Small effect:</strong> Small effects are around d = 0.2, which is smaller than 0.5.</li>
        <li><strong>C) Large effect:</strong> Large effects are around d = 0.8, which is larger than 0.5.</li>
        <li><strong>D) Very large effect:</strong> Cohen's original guidelines only go up to "large" (d = 0.8). Values above 0.8 are typically considered very large.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Remember Cohen's benchmarks: 0.2 (small), 0.5 (medium), 0.8 (large). These are rough guidelines but useful for initial interpretation.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 3:</strong> In SPSS output for an independent-samples t-test, where would you typically find Cohen's d?</p>
    <div class="options">
      <p>A) In the main t-test table</p>
      <p>B) In a separate "Effect Sizes" table</p>
      <p>C) In the descriptive statistics table</p>
      <p>D) Cohen's d is never available in SPSS</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) In a separate "Effect Sizes" table</p>

      <p class="explanation"><strong>Why this is correct:</strong> Cohen's d is not automatically calculated in SPSS. You must request it in the Options (Effect Sizes → Cohen's d), and it appears in a separate table, not in the main t-test output.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Main t-test table:</strong> This table shows t-statistics, p-values, and confidence intervals, but not effect sizes unless specifically requested.</li>
        <li><strong>C) Descriptive statistics table:</strong> This shows means, standard deviations, and sample sizes, but not effect sizes.</li>
        <li><strong>D) Never available:</strong> SPSS can calculate Cohen's d, but only if you specifically request it in the Options before running the test.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Always remember to request effect sizes in SPSS Options before running your t-test. You can't add them after the fact.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 4:</strong> What does it mean when Cohen's d = 0.20 in a two-sample comparison?</p>
    <div class="options">
      <p>A) The groups are very different</p>
      <p>B) The groups have a small but meaningful difference</p>
      <p>C) The groups are essentially identical</p>
      <p>D) The test was not significant</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) The groups have a small but meaningful difference</p>

      <p class="explanation"><strong>Why this is correct:</strong> According to Cohen's guidelines, d = 0.20 represents a small effect size. While small, it still indicates a meaningful difference between groups, just not a large one.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Very different:</strong> d = 0.20 is classified as a small effect, not a very large difference.</li>
        <li><strong>C) Essentially identical:</strong> Even a small effect (d = 0.20) indicates some difference between groups.</li>
        <li><strong>D) Not significant:</strong> Effect size and statistical significance are independent. A small effect can still be statistically significant with sufficient power.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 6.1: Why Effect Size Matters for the distinction between statistical significance and effect size.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 5:</strong> How do you calculate Cohen's d for a paired-samples t-test?</p>
    <div class="options">
      <p>A) d = (M₁ - M₂) / SD_pooled</p>
      <p>B) d = (M₁ - M₂) / SD₁</p>
      <p>C) d = M_diff / SD_diff</p>
      <p>D) d = t / √n</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> C) d = M_diff / SD_diff</p>

      <p class="explanation"><strong>Why this is correct:</strong> For paired-samples t-tests, Cohen's d is calculated using the mean of the difference scores (M_diff) divided by the standard deviation of the difference scores (SD_diff).</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Using pooled SD:</strong> This is the formula for independent-samples t-tests, not paired-samples.</li>
        <li><strong>B) Using SD₁:</strong> This doesn't use the appropriate standard deviation for paired-samples tests.</li>
        <li><strong>D) t / √n:</strong> This is an alternative formula but not the most common one for paired-samples Cohen's d.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 6.3: Cohen's d for Paired-Samples t-Tests for the correct formula.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 6:</strong> A researcher reports Cohen's d = 0.85 for an independent-samples t-test. What can be concluded about the practical significance?</p>
    <div class="options">
      <p>A) The effect is small and not practically important</p>
      <p>B) The effect is medium and somewhat important</p>
      <p>C) The effect is large and practically important</p>
      <p>D) Effect size tells us nothing about practical significance</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> C) The effect is large and practically important</p>

      <p class="explanation"><strong>Why this is correct:</strong> Cohen's d = 0.85 is slightly above the 0.8 threshold for "large" effects. Large effect sizes typically indicate practically important differences that have real-world significance.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Small and not important:</strong> d = 0.85 is well above the 0.2 threshold for small effects.</li>
        <li><strong>B) Medium and somewhat important:</strong> d = 0.85 is above the 0.5 threshold for medium effects and exceeds the 0.8 threshold for large effects.</li>
        <li><strong>D) Tells us nothing:</strong> Effect size is specifically designed to provide information about practical significance.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Large effect sizes (d > 0.8) generally indicate findings that are not just statistically significant but also practically meaningful.</p>
    </div>

  </details>
</div>

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

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Degrees of Freedom and Sample Sizes</h4>

  <div class="quiz-question">
    <p><strong>Question 1:</strong> The results of an independent-samples t-test were t(19) = 4.02, p = 0.01. In this example, the degrees of freedom are _____.</p>
    <div class="options">
      <p>A) 4.02</p>
      <p>B) 20</p>
      <p>C) 18</p>
      <p>D) 19</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> D) 19</p>

      <p class="explanation"><strong>Why this is correct:</strong> The degrees of freedom are explicitly stated in the t-statistic: t(19). The number in parentheses is always the degrees of freedom. For independent-samples t-tests, df = n₁ + n₂ - 2.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) 4.02:</strong> This is the t-value, not the degrees of freedom.</li>
        <li><strong>B) 20:</strong> If df = 19, then total sample size = df + 2 = 19 + 2 = 21, not 20.</li>
        <li><strong>C) 18:</strong> This would be correct if the t-statistic was t(18), but it's t(19).</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 7: Assumptions and Diagnostics for the degrees of freedom formulas.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 2:</strong> Based on the previous question (t(19) = 4.02), what is the total sample size in this independent-samples t-test?</p>
    <div class="options">
      <p>A) 19</p>
      <p>B) 20</p>
      <p>C) 21</p>
      <p>D) Cannot be determined</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> C) 21</p>

      <p class="explanation"><strong>Why this is correct:</strong> For independent-samples t-tests, df = n₁ + n₂ - 2. If df = 19, then n₁ + n₂ = df + 2 = 19 + 2 = 21. The total sample size is 21.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) 19:</strong> This is the degrees of freedom, not the total sample size.</li>
        <li><strong>B) 20:</strong> This would be correct if df = 18, but df = 19.</li>
        <li><strong>D) Cannot be determined:</strong> We can calculate the total sample size from the degrees of freedom using the formula.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Remember: Total sample size = df + 2 for independent-samples t-tests. This helps you check your work and understand your sample.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 3:</strong> A researcher reported the result from an independent-samples t-test as t(43) = 3.56, p = .04. The data were collected from how many subjects?</p>
    <div class="options">
      <p>A) 43</p>
      <p>B) 42</p>
      <p>C) 45</p>
      <p>D) 44</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> C) 45</p>

      <p class="explanation"><strong>Why this is correct:</strong> For independent-samples t-tests, total sample size = df + 2. If df = 43, then total sample size = 43 + 2 = 45 subjects.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) 43:</strong> This is the degrees of freedom, not the total sample size.</li>
        <li><strong>B) 42:</strong> This would be correct if df = 40, but df = 43.</li>
        <li><strong>D) 44:</strong> This would be correct if df = 42, but df = 43.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 7: Assumptions and Diagnostics for the relationship between df and sample size.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 4:</strong> Researchers were interested in whether relaxation training works better than fitness training in decreasing headaches. They randomly assigned 20 participants to either the fitness training group or relaxation training group. The dependent variable in this study is _____.</p>
    <div class="options">
      <p>A) Training type</p>
      <p>B) Fitness training</p>
      <p>C) Change in number of headaches</p>
      <p>D) Relaxation training</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> C) Change in number of headaches</p>

      <p class="explanation"><strong>Why this is correct:</strong> The dependent variable is what you're measuring—the outcome variable. In this study, they're measuring the change in number of headaches, which is the outcome they're interested in.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Training type:</strong> This is the independent variable—what they're manipulating (fitness vs. relaxation training).</li>
        <li><strong>B) Fitness training:</strong> This is one level of the independent variable, not the dependent variable.</li>
        <li><strong>D) Relaxation training:</strong> This is one level of the independent variable, not the dependent variable.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 1: Introduction to Comparing Two Means for the distinction between independent and dependent variables.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 5:</strong> _____ is a weighted average of the two estimates of _____.</p>
    <div class="options">
      <p>A) Population standard deviation; pooled variance</p>
      <p>B) Variance; pooled variance</p>
      <p>C) Pooled variance; population variance</p>
      <p>D) Pooled variance; population standard deviation</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> C) Pooled variance; population variance</p>

      <p class="explanation"><strong>Why this is correct:</strong> Pooled variance is a weighted average of the two sample variances, which are estimates of the population variance. It combines information from both groups to get a better estimate of the common population variance.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Population SD; pooled variance:</strong> Pooled variance is not a weighted average of population standard deviation.</li>
        <li><strong>B) Variance; pooled variance:</strong> This is backwards—pooled variance is the weighted average, not what's being averaged.</li>
        <li><strong>D) Pooled variance; population SD:</strong> Pooled variance estimates population variance, not population standard deviation.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 3: The Independent-Samples t-Test for the concept of pooled variance.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 6:</strong> Which of the following dependent variables would suggest the use of a non-parametric test like the Mann-Whitney U test?</p>
    <div class="options">
      <p>A) Number of customers served daily through the customer service call center</p>
      <p>B) Customer satisfaction score on a rating scale from 1 to 5</p>
      <p>C) Quarterly profit (in dollar amount) of a company</p>
      <p>D) Monthly sales volume of a product</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) Customer satisfaction score on a rating scale from 1 to 5</p>

      <p class="explanation"><strong>Why this is correct:</strong> Customer satisfaction scores on a 1-5 scale are ordinal data. The intervals between ratings may not be equal (the difference between "1" and "2" may not equal the difference between "4" and "5"). Non-parametric tests like Mann-Whitney U are appropriate for ordinal data.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Number of customers served:</strong> This is ratio data (count data with a true zero), which is appropriate for parametric tests.</li>
        <li><strong>C) Quarterly profit:</strong> This is ratio data (dollar amounts with a true zero), which is appropriate for parametric tests.</li>
        <li><strong>D) Monthly sales volume:</strong> This is ratio data (quantities with a true zero), which is appropriate for parametric tests.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Use non-parametric tests when data are ordinal or when parametric assumptions are severely violated. Ordinal scales with few categories are prime candidates for non-parametric alternatives.</p>
    </div>

  </details>
</div>

            <!-- Bottom Navigation -->
            <div class="tab-navigation bottom-nav">
                <button class="tab-button" onclick="showTab(1)">
                    <input type="checkbox" id="progress-1-bottom" class="tab-checkbox" onchange="toggleTabComplete(1)">
                    <span class="tab-label">Introduction & Research Designs</span>
                </button>
                <button class="tab-button" onclick="showTab(2)">
                    <input type="checkbox" id="progress-2-bottom" class="tab-checkbox" onchange="toggleTabComplete(2)">
                    <span class="tab-label">Independent-Samples t-Test</span>
                </button>
                <button class="tab-button" onclick="showTab(3)">
                    <input type="checkbox" id="progress-3-bottom" class="tab-checkbox" onchange="toggleTabComplete(3)">
                    <span class="tab-label">Paired-Samples t-Test</span>
                </button>
                <button class="tab-button active" onclick="showTab(4)">
                    <input type="checkbox" id="progress-4-bottom" class="tab-checkbox" onchange="toggleTabComplete(4)">
                    <span class="tab-label">Effect Sizes & Assumptions</span>
                </button>
                <button class="tab-button" onclick="showTab(5)">
                    <input type="checkbox" id="progress-5-bottom" class="tab-checkbox" onchange="toggleTabComplete(5)">
                    <span class="tab-label">Application & Summary</span>
                </button>
            </div>
        </div>

        <div id="tab-5" class="tab-panel">

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
"An independent-samples t-test [with Welch's correction if applicable] revealed that [Group A] (M = [mean], SD = [sd]) scored significantly [higher/lower] than [Group B] (M = [mean], SD = [sd]), t([df]) = [t-value], p = [p-value], d = [effect-size]."

**Example:** "An independent-samples t-test revealed that students who received tutoring (M = 85.2, SD = 12.4) scored significantly higher than students who did not receive tutoring (M = 78.9, SD = 11.8), t(53) = 2.15, p = .037, d = 0.52."

**Paired-Samples t-Test:**
"A paired-samples t-test revealed that [Condition 2] scores (M = [mean], SD = [sd]) were significantly [higher/lower] than [Condition 1] scores (M = [mean], SD = [sd]), t([df]) = [t-value], p = [p-value], d = [effect-size]."

**Example:** "A paired-samples t-test revealed that post-intervention anxiety scores (M = 42.5, SD = 8.3) were significantly lower than pre-intervention scores (M = 51.0, SD = 9.1), t(14) = -3.45, p = .004, d = 0.89."

### Key Takeaways

1. **Design determines the test:** Always start by identifying your research design
2. **Check assumptions:** Don't skip the diagnostic steps
3. **Use the right row:** Levene's test tells you which output to trust
4. **Report completely:** Include means, significance, and effect size
5. **Consider practical significance:** Statistical significance isn't everything

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Test Selection and APA Reporting</h4>

  <div class="quiz-question">
    <p><strong>Question 1:</strong> Mehl et al. (2007) published a study comparing the number of words uttered per day by men and women (396 participants total). Which statistical test should they use to analyze their data?</p>
    <div class="options">
      <p>A) Independent-samples t-test</p>
      <p>B) Single-sample t-test</p>
      <p>C) Z-test</p>
      <p>D) Paired-samples t-test</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> A) Independent-samples t-test</p>

      <p class="explanation"><strong>Why this is correct:</strong> The researchers are comparing two different groups (men vs. women) on the same variable (words per day). This is a classic independent-samples design where different people are in each group.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>B) Single-sample t-test:</strong> This would compare one group to a known population value, but here they're comparing two groups to each other.</li>
        <li><strong>C) Z-test:</strong> This requires knowing the population standard deviation, which they don't have.</li>
        <li><strong>D) Paired-samples t-test:</strong> This would be used if the same people were measured twice or if there were matched pairs, but here they have two separate groups.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 2: Research Design Decisions for when to use independent-samples t-tests.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 2:</strong> A researcher would like to find out whether taking the GRE a second time produces a significantly higher score compared to the first time. This question can be answered by performing _____.</p>
    <div class="options">
      <p>A) Paired-samples t-test</p>
      <p>B) One-sample t-test</p>
      <p>C) Descriptive statistics</p>
      <p>D) Independent-samples t-test</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> A) Paired-samples t-test</p>

      <p class="explanation"><strong>Why this is correct:</strong> The same people are being measured twice (first GRE score vs. second GRE score). This is a within-subjects design where you compare the same participants' scores across two time points.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>B) One-sample t-test:</strong> This would compare one group to a known population value, but here they're comparing the same people's two scores.</li>
        <li><strong>C) Descriptive statistics:</strong> Descriptive statistics alone can't test for significance—you need inferential statistics.</li>
        <li><strong>D) Independent-samples t-test:</strong> This would compare two different groups, but here the same people are measured twice.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Ask yourself: "Are these the same people measured twice, or different groups?" Same people = paired-samples; different groups = independent-samples.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 3:</strong> Which of these illustrates the APA format for reporting statistically significant results for an independent-samples t-test?</p>
    <div class="options">
      <p>A) t(15) = 3.89, p = 0.5</p>
      <p>B) t(15) = 3.89, p < 0.05</p>
      <p>C) t(15) = 3.89, p = 0.013</p>
      <p>D) t(15) = 3.89, p > 0.05</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> C) t(15) = 3.89, p = 0.013</p>

      <p class="explanation"><strong>Why this is correct:</strong> APA format requires: t(df) = value, p = exact value. The exact p-value should be reported when available. Since p = 0.013 < 0.05, this would be statistically significant.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) p = 0.5:</strong> This would not be statistically significant (p > 0.05), and the question asks for significant results.</li>
        <li><strong>B) p < 0.05:</strong> When the exact p-value is available (0.013), report it exactly rather than using the inequality.</li>
        <li><strong>D) p > 0.05:</strong> This would not be statistically significant, and the question asks for significant results.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 8: Putting It All Together for APA reporting guidelines.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 4:</strong> I am planning to implement a new collaborative learning tool for next semester. To examine its effect on learning, I can analyze this semester's class performance and next semester's class performance with _____.</p>
    <div class="options">
      <p>A) Z-test</p>
      <p>B) One-sample t-test</p>
      <p>C) Independent-samples t-test</p>
      <p>D) Paired-samples t-test</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> C) Independent-samples t-test</p>

      <p class="explanation"><strong>Why this is correct:</strong> You're comparing two different groups of students (this semester's class vs. next semester's class) on the same outcome variable (class performance). These are different people in each group, making it an independent-samples design.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Z-test:</strong> This requires knowing the population standard deviation, which you don't have.</li>
        <li><strong>B) One-sample t-test:</strong> This would compare one group to a known population value, but you're comparing two groups to each other.</li>
        <li><strong>D) Paired-samples t-test:</strong> This would be used if the same students were measured twice, but here you have two different groups of students.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Even though it's the same course, different semesters mean different students, so it's an independent-samples design.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 5:</strong> What is an adequate conclusion from SPSS output showing a paired-samples t-test comparing writing scores and reading scores of the same test takers?</p>
    <div class="options">
      <p>A) Writing score and reading score of the same test taker are not significantly different</p>
      <p>B) A sample of writing scores are not significantly different from a separate sample of reading scores</p>
      <p>C) Writing score and reading score of the same test taker are significantly different</p>
      <p>D) A sample of writing scores are significantly different from a separate sample of reading scores</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> A) Writing score and reading score of the same test taker are not significantly different</p>

      <p class="explanation"><strong>Why this is correct:</strong> A paired-samples t-test compares the same people on two different variables. The conclusion should reflect that you're comparing the same test takers' writing vs. reading scores, and the result is non-significant (assuming p > 0.05).</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>B) Separate samples:</strong> This describes an independent-samples design, but paired-samples compares the same people.</li>
        <li><strong>C) Significantly different:</strong> The question asks for an "adequate" conclusion, and if the test is non-significant, you shouldn't conclude significance.</li>
        <li><strong>D) Separate samples, significant:</strong> Again, this describes independent-samples design, not paired-samples.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 4: The Paired-Samples t-Test for how to interpret paired-samples results.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 6:</strong> According to SPSS output for an independent-samples t-test, how many subjects were in the study if the output shows N = 200 for Group 1 and N = 200 for Group 2?</p>
    <div class="options">
      <p>A) 400</p>
      <p>B) 200</p>
      <p>C) 398</p>
      <p>D) 199</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> A) 400</p>

      <p class="explanation"><strong>Why this is correct:</strong> The total sample size is the sum of both groups: N₁ + N₂ = 200 + 200 = 400 subjects. SPSS shows the sample size for each group separately, so you add them together for the total.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>B) 200:</strong> This is the sample size for one group, not the total.</li>
        <li><strong>C) 398:</strong> This would be the degrees of freedom (df = n₁ + n₂ - 2 = 200 + 200 - 2 = 398), not the sample size.</li>
        <li><strong>D) 199:</strong> This doesn't match any calculation from the given information.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Remember: Total N = N₁ + N₂, while df = N₁ + N₂ - 2. Don't confuse sample size with degrees of freedom.</p>
    </div>

  </details>
</div>

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

## Quick Reference Card

### When to Use Each Test

| Question to Ask                                             | Answer           | Test to Use                |
| ----------------------------------------------------------- | ---------------- | -------------------------- |
| Are the same people measured twice?                         | YES              | Paired-Samples t-Test      |
| Are the participants meaningfully matched (twins, couples)? | YES              | Paired-Samples t-Test      |
| Are there two completely different groups?                  | YES              | Independent-Samples t-Test |
| Do I need to check equal variances?                         | Independent only | Run Levene's test          |

### Critical Steps Checklist

**For Independent-Samples:**

- ☐ Verify groups are truly independent
- ☐ Check normality for each group
- ☐ Run Levene's test (p > .05 = equal variances)
- ☐ Use correct row in output based on Levene's test
- ☐ Calculate Cohen's d using pooled SD
- ☐ Report: groups, means, SDs, t, df, p, d

**For Paired-Samples:**

- ☐ Verify data is paired correctly
- ☐ Calculate difference scores
- ☐ Check normality of difference scores
- ☐ Run paired-samples t-test
- ☐ Calculate Cohen's d using difference SD
- ☐ Report: conditions, means, SDs, t, df, p, d

### Effect Size Interpretation

| Cohen's d | Interpretation |
| --------- | -------------- |
| 0.2       | Small effect   |
| 0.5       | Medium effect  |
| 0.8       | Large effect   |

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

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Reading SPSS Output for t-Tests</h4>

  <div class="quiz-question">
    <p><strong>Question 1:</strong> In SPSS output for an independent-samples t-test, you need to report the exact p-value from Levene's test. If SPSS shows "Sig." = .000, how should you report it?</p>
    <div class="options">
      <p>A) p = .000</p>
      <p>B) p < .001</p>
      <p>C) p = .001</p>
      <p>D) p = 0.000</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) p < .001</p>

      <p class="explanation"><strong>Why this is correct:</strong> When SPSS shows "Sig." = .000, it means the p-value is less than .001 (but not actually zero). According to APA format, you should report this as "p < .001" rather than "p = .000".</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) p = .000:</strong> You should never report p = .000 because p-values are never actually zero.</li>
        <li><strong>C) p = .001:</strong> This would be incorrect because the actual p-value is less than .001.</li>
        <li><strong>D) p = 0.000:</strong> Same issue as A - you should never report p = .000 or p = 0.000.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 9: Practical Guide - SPSS for reporting conventions.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 2:</strong> You're reading SPSS output for an independent-samples t-test. Levene's test shows F = 2.847, p = .023. Which row should you use for your t-test results?</p>
    <div class="options">
      <p>A) "Equal variances assumed" row</p>
      <p>B) "Equal variances not assumed" row</p>
      <p>C) Either row is acceptable</p>
      <p>D) You need to run the test again</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) "Equal variances not assumed" row</p>

      <p class="explanation"><strong>Why this is correct:</strong> Since Levene's test has p = .023 < .05, we reject the null hypothesis of equal variances. Therefore, you should use the "Equal variances not assumed" row, which applies Welch's correction.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) "Equal variances assumed" row:</strong> This should only be used when Levene's test shows p > .05.</li>
        <li><strong>C) Either row is acceptable:</strong> You must use the appropriate row based on Levene's test results.</li>
        <li><strong>D) Run test again:</strong> The test is fine; you just need to use the correct row from the existing output.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Always check Levene's test first, then use the appropriate row. This ensures you're using the correct statistical procedure.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 3:</strong> In SPSS output for a paired-samples t-test, you see "t = -2.386" and "Sig. (2-tailed) = .021". What is the correct t-statistic and p-value to report?</p>
    <div class="options">
      <p>A) t = -2.386, p = .021</p>
      <p>B) t = 2.386, p = .021</p>
      <p>C) t = -2.386, p = .042</p>
      <p>D) t = -2.386, p = .0105</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> A) t = -2.386, p = .021</p>

      <p class="explanation"><strong>Why this is correct:</strong> Report the t-statistic exactly as shown (including the negative sign) and the exact p-value from the "Sig. (2-tailed)" column. The negative t-value indicates the direction of the difference.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>B) t = 2.386:</strong> Don't remove the negative sign from the t-statistic - it indicates direction.</li>
        <li><strong>C) p = .042:</strong> Don't double the p-value - SPSS already gives you the correct 2-tailed p-value.</li>
        <li><strong>D) p = .0105:</strong> Don't halve the p-value - use the exact value from SPSS output.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 9: Practical Guide - SPSS for reading paired-samples output.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 4:</strong> The following SPSS output indicates that a(n) _____ was performed.</p>
    <div class="options">
      <p>A) Independent-samples t-test</p>
      <p>B) One-sample t-test</p>
      <p>C) Z-test</p>
      <p>D) Paired-samples t-test</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> D) Paired-samples t-test</p>

      <p class="explanation"><strong>Why this is correct:</strong> SPSS output for paired-samples t-tests typically shows "Paired Samples Test" in the table header, lists the two variables being compared (e.g., "Variable1 - Variable2"), and shows a single row of results (not two rows like independent-samples tests).</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Independent-samples t-test:</strong> This would show "Independent Samples Test" and have two rows of results (equal variances assumed/not assumed).</li>
        <li><strong>B) One-sample t-test:</strong> This would show "One-Sample Test" and compare to a test value.</li>
        <li><strong>C) Z-test:</strong> SPSS doesn't typically provide z-test output in the same format as t-tests.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Look at the table header and structure to identify the test type. Paired-samples shows variable differences, independent-samples shows two rows of results.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 5:</strong> In SPSS output for an independent-samples t-test, you need to extract the effect size (Cohen's d). Where would you find this information?</p>
    <div class="options">
      <p>A) In the main "Independent Samples Test" table</p>
      <p>B) In the "Group Statistics" table</p>
      <p>C) In a separate "Effect Sizes" table</p>
      <p>D) Cohen's d is never available in SPSS</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> C) In a separate "Effect Sizes" table</p>

      <p class="explanation"><strong>Why this is correct:</strong> Cohen's d is not automatically calculated in SPSS. You must request it in the Options (Effect Sizes → Cohen's d), and it appears in a separate "Effect Sizes" table, not in the main t-test output.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Main test table:</strong> This shows t-statistics, p-values, and confidence intervals, but not effect sizes unless specifically requested.</li>
        <li><strong>B) Group Statistics table:</strong> This shows means, standard deviations, and sample sizes, but not effect sizes.</li>
        <li><strong>D) Never available:</strong> SPSS can calculate Cohen's d, but only if you specifically request it in the Options before running the test.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Always remember to request effect sizes in SPSS Options before running your t-test. You can't add them after the fact.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 6:</strong> You're reading SPSS output for a paired-samples t-test comparing blood pressure before and after treatment. The output shows "Mean = -8.50" in the "Paired Differences" section. What does this mean?</p>
    <div class="options">
      <p>A) Blood pressure increased by 8.50 points</p>
      <p>B) Blood pressure decreased by 8.50 points</p>
      <p>C) The groups are 8.50 points apart</p>
      <p>D) The standard deviation is 8.50</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) Blood pressure decreased by 8.50 points</p>

      <p class="explanation"><strong>Why this is correct:</strong> The mean difference of -8.50 means that, on average, blood pressure after treatment was 8.50 points lower than before treatment. The negative sign indicates a decrease.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Increased by 8.50:</strong> This would be true if the mean difference was +8.50, but it's -8.50.</li>
        <li><strong>C) Groups are 8.50 apart:</strong> This describes independent-samples design, not paired-samples.</li>
        <li><strong>D) Standard deviation is 8.50:</strong> The mean difference and standard deviation are different statistics.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 4: The Paired-Samples t-Test for interpreting difference scores.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 7:</strong> Based on SPSS output for an independent-samples t-test, which statement correctly describes how to make a statistical decision?</p>
    <div class="options">
      <p>A) If p > .05, reject the null hypothesis</p>
      <p>B) If p ≤ .05, reject the null hypothesis</p>
      <p>C) If t > 2.0, reject the null hypothesis</p>
      <p>D) If the confidence interval contains zero, reject the null hypothesis</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) If p ≤ .05, reject the null hypothesis</p>

      <p class="explanation"><strong>Why this is correct:</strong> The standard decision rule is: if p ≤ α (typically .05), reject the null hypothesis; if p > α, fail to reject the null hypothesis. This is the fundamental rule for hypothesis testing.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) p > .05, reject:</strong> This is backwards—you reject when p is small (≤ .05), not large.</li>
        <li><strong>C) t > 2.0, reject:</strong> The critical t-value depends on degrees of freedom and alpha level, not a fixed value of 2.0.</li>
        <li><strong>D) CI contains zero, reject:</strong> If the confidence interval contains zero, you typically fail to reject the null hypothesis.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Always use the p-value for statistical decisions. Compare p to your chosen alpha level (usually .05).</p>
    </div>

  </details>
</div>

            <!-- Bottom Navigation -->
            <div class="tab-navigation bottom-nav">
                <button class="tab-button" onclick="showTab(1)">
                    <input type="checkbox" id="progress-1-bottom" class="tab-checkbox" onchange="toggleTabComplete(1)">
                    <span class="tab-label">Introduction & Research Designs</span>
                </button>
                <button class="tab-button" onclick="showTab(2)">
                    <input type="checkbox" id="progress-2-bottom" class="tab-checkbox" onchange="toggleTabComplete(2)">
                    <span class="tab-label">Independent-Samples t-Test</span>
                </button>
                <button class="tab-button" onclick="showTab(3)">
                    <input type="checkbox" id="progress-3-bottom" class="tab-checkbox" onchange="toggleTabComplete(3)">
                    <span class="tab-label">Paired-Samples t-Test</span>
                </button>
                <button class="tab-button" onclick="showTab(4)">
                    <input type="checkbox" id="progress-4-bottom" class="tab-checkbox" onchange="toggleTabComplete(4)">
                    <span class="tab-label">Effect Sizes & Assumptions</span>
                </button>
                <button class="tab-button active" onclick="showTab(5)">
                    <input type="checkbox" id="progress-5-bottom" class="tab-checkbox" onchange="toggleTabComplete(5)">
                    <span class="tab-label">Application & Summary</span>
                </button>
            </div>
        </div>

    </div>

</div>

---

_This module provides a comprehensive foundation for understanding and applying t-tests for comparing two means. Practice with real data and always remember that statistical analysis begins with understanding your research design._

<script>
// Progress tracking storage key
const PROGRESS_KEY = 'm3-lecture-progress';

// Load saved progress on page load
function loadProgress() {
    const savedProgress = localStorage.getItem(PROGRESS_KEY);
    if (savedProgress) {
        const progress = JSON.parse(savedProgress);
        // Update all checkboxes based on saved progress
        for (let i = 1; i <= 5; i++) {
            const isComplete = progress[i] || false;
            document.getElementById(`progress-${i}`).checked = isComplete;
            document.getElementById(`progress-${i}-bottom`).checked = isComplete;
            updateTabVisualState(i, isComplete);
        }
    }
}

// Save progress to localStorage
function saveProgress(tabNumber, isComplete) {
    const savedProgress = localStorage.getItem(PROGRESS_KEY);
    const progress = savedProgress ? JSON.parse(savedProgress) : {};
    progress[tabNumber] = isComplete;
    localStorage.setItem(PROGRESS_KEY, JSON.stringify(progress));
}

// Toggle tab completion state
function toggleTabComplete(tabNumber) {
    // Determine which checkbox was clicked (top or bottom)
    const clickedCheckbox = event.target;
    const isComplete = clickedCheckbox.checked;
    
    // Update both top and bottom checkboxes to stay in sync
    document.getElementById(`progress-${tabNumber}`).checked = isComplete;
    document.getElementById(`progress-${tabNumber}-bottom`).checked = isComplete;
    
    // Update visual state
    updateTabVisualState(tabNumber, isComplete);
    
    // Save to localStorage
    saveProgress(tabNumber, isComplete);
}

// Update visual state of tab buttons when completed
function updateTabVisualState(tabNumber, isComplete) {
    // Update all tab buttons for this tab (top and bottom)
    const tabButtons = document.querySelectorAll(`button[onclick="showTab(${tabNumber})"]`);
    tabButtons.forEach(button => {
        if (isComplete) {
            button.classList.add('completed');
        } else {
            button.classList.remove('completed');
        }
    });
}

// Main tab switching function
function showTab(tabNumber) {
    // Hide all panels
    const panels = document.querySelectorAll('.tab-panel');
    panels.forEach(panel => panel.classList.remove('active'));
    
    // Remove active from all buttons
    const buttons = document.querySelectorAll('.tab-button');
    buttons.forEach(button => button.classList.remove('active'));
    
    // Show selected panel and activate button
    document.getElementById(`tab-${tabNumber}`).classList.add('active');
    
    // Activate the button that was clicked (could be top or bottom)
    event.target.classList.add('active');
    
    // Scroll to top of the tab navigation for better UX
    const tabContainer = document.querySelector('.lecture-tabs');
    if (tabContainer) {
        tabContainer.scrollIntoView({ behavior: 'smooth', block: 'start' });
    }
}

// Knowledge Check functionality
const KC_STORAGE_KEY = 'm3-knowledge-checks';

// Load answered questions on page load
function loadKnowledgeCheckProgress() {
    const savedProgress = localStorage.getItem(KC_STORAGE_KEY);
    if (savedProgress) {
        const answeredQuestions = JSON.parse(savedProgress);
        answeredQuestions.forEach(questionId => {
            markQuestionAsAnswered(questionId, false);
        });
    }
}

// Save answered question to localStorage
function saveAnsweredQuestion(questionId) {
    const savedProgress = localStorage.getItem(KC_STORAGE_KEY);
    const answeredQuestions = savedProgress ? JSON.parse(savedProgress) : [];
    
    if (!answeredQuestions.includes(questionId)) {
        answeredQuestions.push(questionId);
        localStorage.setItem(KC_STORAGE_KEY, JSON.stringify(answeredQuestions));
    }
}

// Reveal answer for a question
function revealAnswer(questionId) {
    const questionItem = document.querySelector(`[data-question-id="${questionId}"]`);
    const answerDiv = questionItem.querySelector('.answer-reveal');
    const button = questionItem.querySelector('.reveal-answer-btn');
    
    // Show the answer
    answerDiv.style.display = 'block';
    
    // Mark as answered
    markQuestionAsAnswered(questionId, true);
}

// Mark question as answered (visually and in storage)
function markQuestionAsAnswered(questionId, saveToStorage) {
    const questionItem = document.querySelector(`[data-question-id="${questionId}"]`);
    if (!questionItem) return;
    
    const answerDiv = questionItem.querySelector('.answer-reveal');
    const button = questionItem.querySelector('.reveal-answer-btn');
    
    // Update visual state
    questionItem.classList.add('answered');
    button.classList.add('answered');
    button.textContent = 'Answer Shown ✓';
    answerDiv.style.display = 'block';
    
    // Save to storage if requested
    if (saveToStorage) {
        saveAnsweredQuestion(questionId);
    }
}

// Load progress when page loads
document.addEventListener('DOMContentLoaded', function() {
    loadProgress();
    loadKnowledgeCheckProgress();
});
</script>
