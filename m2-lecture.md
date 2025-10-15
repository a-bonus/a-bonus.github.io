---
layout: lecture
title: "Module 2: Introduction to Hypothesis Testing and the One-Sample t-Test"
---

# Module 2: Introduction to Hypothesis Testing and the One-Sample t-Test

**Estimated Study Time:** 2-3 hours

## Learning Objectives

By the end of this module, you will be able to:

1. Explain the logic and purpose of hypothesis testing
2. Formulate null and alternative hypotheses for research questions
3. Distinguish between one-tailed and two-tailed tests
4. Understand and interpret p-values in the context of statistical decisions
5. Identify and explain Type I and Type II errors
6. Apply the Central Limit Theorem to understand sampling distributions
7. Conduct and interpret a one-sample t-test (manually and using SPSS)
8. Calculate and interpret effect sizes (Cohen's d)
9. Understand the concept of statistical power and factors that influence it
10. Report statistical results in APA format

---

## Table of Contents

1. [The Logic of Hypothesis Testing](#part-1-the-logic-of-hypothesis-testing)
2. [Formulating Hypotheses](#part-2-formulating-hypotheses)
3. [The Decision-Making Framework](#part-3-the-decision-making-framework)
4. [Understanding Errors in Hypothesis Testing](#part-4-understanding-errors-in-hypothesis-testing)
5. [The Central Limit Theorem](#part-5-the-central-limit-theorem)
6. [The One-Sample t-Test](#part-6-the-one-sample-t-test)
7. [Effect Size: Measuring Practical Significance](#part-7-effect-size-measuring-practical-significance)
8. [Statistical Power](#part-8-statistical-power)
9. [The t-Distribution](#part-9-the-t-distribution)
10. [Practical Guide: SPSS for One-Sample t-Tests](#part-10-practical-guide-spss-for-one-sample-t-tests)
11. [Summary and Key Formulas](#summary-and-key-formulas)

---

## Part 1: The Logic of Hypothesis Testing

### From Description to Inference

In Module 1, you learned to **describe** data using means, standard deviations, and graphs. Now we take the crucial next step: using sample data to make **inferences** about populations.

**The Central Challenge:** We can't study everyone, so we study a sample. But how do we know if what we observe in our sample reflects a real pattern in the population, or is just random chance?

**The Solution:** Hypothesis testing—a systematic method for distinguishing signal from noise.

### The Courtroom Analogy

Hypothesis testing works like a legal trial. This analogy is powerful and worth understanding deeply.

**In a Courtroom:**

- **Presumption of Innocence:** The defendant is assumed innocent until proven guilty
- **Burden of Proof:** The prosecution must provide strong evidence of guilt
- **Standard of Proof:** "Beyond a reasonable doubt"
- **Decision:** If evidence is overwhelming, we reject innocence and conclude guilt. If evidence is weak, we maintain the presumption of innocence (we don't declare the person "innocent," just "not proven guilty")

**In Hypothesis Testing:**

- **Null Hypothesis (H₀):** We assume "nothing special is happening" (like presuming innocence)
- **Burden of Proof:** Our data must provide strong evidence against this assumption
- **Standard of Proof:** p < .05 (less than 5% probability the result is due to chance)
- **Decision:** If evidence is strong (p < .05), we reject H₀ and conclude there IS an effect. If evidence is weak (p ≥ .05), we maintain H₀ (we don't "prove" H₀, just fail to find evidence against it)

**Key Concept:** We never "prove" anything in statistics. We only collect evidence strong enough to reject the null hypothesis, or fail to do so.

### Why This Backward Logic?

**Why not just test our research hypothesis directly?**

Because we can never observe all possible outcomes. Consider:

**Direct Approach (doesn't work):** "Does this drug improve memory?"

- To prove this directly, we'd need to test every possible person, under every possible condition, forever
- Impossible!

**Indirect Approach (hypothesis testing):** "Assume the drug does nothing. How likely is it we'd see results this good by chance alone?"

- If the probability is very low (p < .05), the "does nothing" assumption is probably wrong
- We reject that assumption and conclude the drug likely works

**Think of it like proof by contradiction in mathematics:** To prove X is true, assume X is false and show that leads to an impossible or highly unlikely situation. Therefore, X must be true.

### The Hypothesis Testing Process: Overview

Here's the big picture before we dive into details:

1. **Start with a research question**

   - Example: "Does meditation reduce anxiety?"

2. **Formulate hypotheses**

   - H₀ (Null): Meditation has no effect on anxiety (μ = population mean)
   - H₁ (Alternative): Meditation does affect anxiety (μ ≠ population mean)

3. **Set decision criteria**

   - Alpha level: Usually α = .05

4. **Collect data**

   - Sample of people who meditate regularly

5. **Calculate a test statistic**

   - Measures how far your sample result is from what H₀ predicts

6. **Determine probability (p-value)**

   - If H₀ were true, how likely would we see a result this extreme?

7. **Make a decision**

   - If p < .05: Reject H₀ (conclude meditation likely works)
   - If p ≥ .05: Fail to reject H₀ (insufficient evidence)

8. **Interpret in context**
   - Translate statistical decision back into meaningful conclusion

### Real-World Example

**Scenario:** A school psychologist believes a new reading program improves comprehension.

**What We Know:**

- National average reading score: μ = 100, σ = 15
- Our sample of 25 students using the new program: M = 107

**The Question:** Is 107 significantly higher than 100, or could this difference be just random sampling variation?

**Hypothesis Testing Answers This:**

1. H₀: The program doesn't work (students are just a random sample from the population where μ = 100)
2. H₁: The program does work (students come from a different population where μ > 100)
3. Calculate: How unlikely is it to get M = 107 from a population where μ = 100?
4. Result: If probability is < 5%, we conclude the program likely works

**Why This Matters:** Without hypothesis testing, we couldn't distinguish:

- Real improvements from natural variation
- Effective treatments from placebos
- Meaningful differences from random noise

### Common Misconceptions

❌ **Misconception:** "If p < .05, we've proven our theory is true"
✓ **Reality:** We've only shown the null hypothesis is unlikely. Our theory is supported, not proven.

❌ **Misconception:** "If p > .05, we've proven there's no effect"
✓ **Reality:** We failed to find evidence of an effect. Maybe it doesn't exist, or maybe our sample was too small to detect it.

❌ **Misconception:** "p-value tells us the probability our hypothesis is true"
✓ **Reality:** p-value tells us the probability of getting our data IF the null hypothesis is true.

**Think About It:** Why is the distinction between "failing to find evidence" and "finding evidence of no effect" important? (Hint: absence of evidence is not evidence of absence!)

---

## Part 2: Formulating Hypotheses

Every hypothesis test requires two competing hypotheses: the null (H₀) and the alternative (H₁ or Hₐ).

### The Null Hypothesis (H₀)

**Definition:** A statement of "no effect," "no difference," or "no relationship." It represents the status quo or what we'd expect if nothing special is happening.

**Key Characteristics:**

- Always includes an equals sign (=, ≤, or ≥)
- Represents the assumption we're trying to disprove
- The hypothesis we "presume true" until proven otherwise

**Examples:**

| Research Context                | Null Hypothesis                                                     |
| :------------------------------ | :------------------------------------------------------------------ |
| New drug for headaches          | H₀: The drug has no effect on headache duration (μ = 24 hours)      |
| Mindfulness training for stress | H₀: Training doesn't reduce stress (μ = 50 on stress scale)         |
| Teaching method comparison      | H₀: The new method produces the same scores as traditional (μ = 75) |
| Gender and salary               | H₀: There is no gender difference in salary (μ_male = μ_female)     |

### The Alternative Hypothesis (H₁ or Hₐ)

**Definition:** The research hypothesis—what you actually believe or predict. It represents "something special is happening."

**Key Characteristics:**

- Never includes an equals sign (uses ≠, <, or >)
- Represents what you're trying to find evidence for
- Can be directional or non-directional

**Examples (matching the null hypotheses above):**

| Research Context                | Alternative Hypothesis                                         |
| :------------------------------ | :------------------------------------------------------------- |
| New drug for headaches          | H₁: The drug reduces headache duration (μ < 24 hours)          |
| Mindfulness training for stress | H₁: Training reduces stress (μ < 50 on stress scale)           |
| Teaching method comparison      | H₁: The new method produces different scores (μ ≠ 75)          |
| Gender and salary               | H₁: There is a gender difference in salary (μ_male ≠ μ_female) |

### Directional vs. Non-Directional Hypotheses

This is one of the most important decisions in hypothesis testing.

#### Non-Directional (Two-Tailed) Hypotheses

**Used when:** You predict a difference or effect but **not which direction**

**Symbols:** H₁: μ ≠ [value]

**Examples:**

- "Does caffeine affect reaction time?" (could make it faster OR slower)
- "Is the average age of psychology majors different from 20?" (could be higher OR lower)
- "Does music affect study performance?" (could help OR hurt)

**Why two-tailed?** You're looking for extreme results in BOTH directions (both tails of the distribution)

#### Directional (One-Tailed) Hypotheses

**Used when:** You predict a **specific direction** of difference or effect

**Symbols:**

- H₁: μ > [value] (predicting an increase)
- H₁: μ < [value] (predicting a decrease)

**Examples:**

- "Does this anti-anxiety medication reduce anxiety?" (specifically predicts decrease)
- "Are basketball players taller than average?" (specifically predicts increase)
- "Does sleep deprivation impair performance?" (specifically predicts impairment, not improvement)

**Why one-tailed?** You're only looking for extreme results in ONE direction (one tail of the distribution)

### How to Choose: Decision Tree

**Ask yourself:** Does my research question predict a specific direction?

```
Research Question
    |
    ├─ Predicts specific direction (increase/decrease, higher/lower, more/less)
    |   └─→ ONE-TAILED TEST
    |       • H₁: μ > [value] or μ < [value]
    |       • More statistical power to detect effect in predicted direction
    |       • But: Can't detect effects in opposite direction
    |
    └─ Asks about any difference/change (different from, affects, changes)
        └─→ TWO-TAILED TEST
            • H₁: μ ≠ [value]
            • Can detect effects in either direction
            • More conservative (safer choice when unsure)
```

**When in Doubt:** Use a two-tailed test. It's more conservative and protects against missing unexpected findings.

### Practice: Writing Hypotheses

For each research question, write H₀ and H₁, and indicate whether you'd use a one-tailed or two-tailed test.

**Scenario 1:** "A researcher wants to know if college students sleep less than the recommended 8 hours per night."

<details>
<summary>Click to see answer</summary>

- **Type:** One-tailed (predicts "less than")
- **H₀:** μ ≥ 8 hours (students sleep 8 hours or more)
- **H₁:** μ < 8 hours (students sleep less than 8 hours)
</details>

**Scenario 2:** "Does listening to classical music while studying affect test scores? The national average is 75."

<details>
<summary>Click to see answer</summary>

- **Type:** Two-tailed (asks "affect" without direction)
- **H₀:** μ = 75 (music has no effect)
- **H₁:** μ ≠ 75 (music affects scores, either way)
</details>

**Scenario 3:** "A therapist predicts that cognitive-behavioral therapy will lower depression scores below the clinical cutoff of 30."

<details>
<summary>Click to see answer</summary>

- **Type:** One-tailed (predicts "lower")
- **H₀:** μ ≥ 30 (therapy doesn't lower scores below cutoff)
- **H₁:** μ < 30 (therapy lowers scores below cutoff)
</details>

**Scenario 4:** "Is the average IQ of chess champions different from the population mean of 100?"

<details>
<summary>Click to see answer</summary>

- **Type:** Two-tailed (asks "different from")
- **H₀:** μ = 100 (chess champions have average IQ)
- **H₁:** μ ≠ 100 (chess champions differ from average)
</details>

### Common Mistakes in Hypothesis Formulation

❌ **Mistake 1:** Making H₀ the research hypothesis

- Wrong: H₀: The drug reduces pain
- Right: H₁: The drug reduces pain; H₀: The drug has no effect

❌ **Mistake 2:** Forgetting the equals sign in H₀

- Wrong: H₀: μ > 50
- Right: H₀: μ = 50 (or μ ≤ 50 for one-tailed)

❌ **Mistake 3:** Using wrong direction for one-tailed test

- If predicting scores will increase: H₁: μ > [value], not μ < [value]

❌ **Mistake 4:** Being too specific in the alternative hypothesis

- Wrong: H₁: μ = 105 (this is too specific; we don't know the exact value)
- Right: H₁: μ > 100 (we predict it's greater, but not a specific value)

**Key Concept:** The null hypothesis always represents the "boring" or "no effect" outcome. The alternative represents the "interesting" or "something is happening" outcome.

---

## Part 3: The Decision-Making Framework

Once we've formulated hypotheses and collected data, we need a systematic way to decide which hypothesis the evidence supports.

### Understanding p-Values

The **p-value** is the most important concept in hypothesis testing—and also the most misunderstood.

**Definition:** The probability of obtaining a result as extreme as (or more extreme than) the one observed, **assuming the null hypothesis is true**.

**In Plain English:** If there really is no effect (H₀ is true), how surprising would our result be? How often would random chance alone produce data this extreme?

**Example:** You test a memory drug and get p = .03

**This means:** If the drug actually does nothing (H₀ is true), there's only a 3% chance we'd see improvement this large due to random sampling variation alone.

**Interpretation:** That's pretty unlikely! Either:

1. We got really lucky with our random sample (3% chance), OR
2. The drug actually works (H₀ is probably false)

We conclude #2 is more plausible.

### The Alpha Level (α)

**Definition:** The threshold for deciding if a p-value is "small enough" to reject H₀. The maximum probability of making a Type I error we're willing to accept.

**Standard Value:** α = .05 (5%)

**The Decision Rule:**

- If p < α (.05): Reject H₀ → Result is **statistically significant**
- If p ≥ α (.05): Fail to reject H₀ → Result is **not statistically significant**

**Why .05?**

This is somewhat arbitrary! It was popularized by statistician Ronald Fisher in the 1920s.

**Different fields sometimes use different alphas:**

- Physics: α = .0000003 (very stringent)
- Medicine: α = .05 (standard)
- Exploratory research: Sometimes α = .10 (more lenient)

**The principle:** Lower α = more conservative (harder to reject H₀) = less risk of false positives

### Worked Example: Making a Decision

**Scenario:** Testing if a new teaching method improves test scores

**Given Information:**

- National average: μ = 70
- Sample of 30 students using new method: M = 75, s = 12
- Statistical test yields: t(29) = 2.36, p = .025
- Alpha level: α = .05

**Step 1: State hypotheses**

- H₀: μ = 70 (method doesn't work)
- H₁: μ ≠ 70 (method has an effect)

**Step 2: Compare p-value to alpha**

- p = .025
- α = .05
- Is .025 < .05? **Yes**

**Step 3: Make statistical decision**

- Since p < α, we **reject the null hypothesis**

**Step 4: State conclusion**
"The new teaching method produced significantly different test scores (M = 75, SD = 12) compared to the national average of 70, t(29) = 2.36, p = .025. Students using the new method scored higher than expected if the method had no effect."

### Statistical Significance vs. Practical Significance

This is a crucial distinction that students often miss.

**Statistical Significance:** p < .05

- Means: The difference is unlikely due to chance
- Answers: "Is there an effect?"

**Practical Significance:** Effect is large/meaningful enough to matter

- Means: The difference is big enough to care about
- Answers: "Is the effect important?"

**These are NOT the same thing!**

**Example 1: Statistically Significant but Practically Trivial**

- New diet pill produces weight loss: M = 0.5 pounds
- With 10,000 participants, p = .001 (highly significant!)
- But who cares about half a pound? Not practically meaningful.

**Example 2: Practically Important but Not Statistically Significant**

- New cancer treatment extends life: M = 6 months longer
- With only 15 participants, p = .08 (not significant)
- Six months of life is hugely important! But our sample was too small to prove it statistically.

**The Solution:** Always consider BOTH statistical significance (p-value) AND effect size (how big the difference is).

### One-Tailed vs. Two-Tailed: How p-Values Differ

This is where the directional vs. non-directional distinction becomes concrete.

**Two-Tailed Test:**

- Splits alpha between both tails of the distribution
- α = .05 means .025 in each tail
- SPSS always reports two-tailed p-values
- Use the reported p-value directly

**One-Tailed Test:**

- Puts all alpha in one tail
- α = .05 means .05 in the predicted direction only
- Must divide SPSS p-value by 2 (if result is in predicted direction)
- Only reject H₀ if result is in the predicted direction

**Example:** Testing if exercise reduces stress (predicting decrease)

- Sample shows M_stress = 45, population μ = 50
- SPSS output: p = .04 (two-tailed)

**If you planned a ONE-TAILED test:**

- p_one-tailed = .04 / 2 = .02
- Result is in predicted direction (decrease) AND p < .05
- **Reject H₀**

**If you planned a TWO-TAILED test:**

- p = .04 (use as reported)
- p < .05
- **Reject H₀**

**Important:** You must decide one-tailed vs. two-tailed BEFORE seeing your data. Otherwise it's cheating (p-hacking).

### Quick Check

1. What does p = .08 mean?
2. If p = .08 and α = .05, what decision do you make?
3. Can a result be statistically significant but practically unimportant?
4. If SPSS reports p = .06 for a two-tailed test, what would the one-tailed p be?

<details>
<summary>Click to see answers</summary>

1. If H₀ is true, there's an 8% chance of getting a result this extreme by random chance
2. Fail to reject H₀ (p ≥ α, so not statistically significant)
3. Yes! Large samples can detect tiny, meaningless differences
4. p_one-tailed = .06 / 2 = .03 (if result is in predicted direction)
</details>

---

## Part 4: Understanding Errors in Hypothesis Testing

Because hypothesis testing is based on probability, not certainty, we can make mistakes. Understanding these errors is crucial for interpreting research.

### The Two Types of Errors

Every hypothesis test can result in four possible outcomes:

|                                                               | **Reality: H₀ is TRUE** (No real effect)                       | **Reality: H₀ is FALSE** (Real effect exists)                  |
| :------------------------------------------------------------ | :------------------------------------------------------------- | :------------------------------------------------------------- |
| **Decision: Reject H₀** (Claim effect exists)                 | **TYPE I ERROR** ❌<br>False Positive<br>Probability = α       | **CORRECT DECISION** ✓<br>True Positive<br>Probability = Power |
| **Decision: Fail to reject H₀** (Claim no evidence of effect) | **CORRECT DECISION** ✓<br>True Negative<br>Probability = 1 - α | **TYPE II ERROR** ❌<br>False Negative<br>Probability = β      |

### Type I Error (False Positive)

**Definition:** Rejecting H₀ when it's actually true. Concluding there's an effect when there isn't one.

**Probability:** α (your alpha level, usually .05)

**Real-World Examples:**

**Medical:** Approving a drug that doesn't actually work

- Consequences: Patients waste money, experience side effects, don't get real treatment

**Legal:** Convicting an innocent person

- Consequences: Injustice, real criminal goes free

**Education:** Adopting a teaching program that doesn't actually help

- Consequences: Wasted resources, missed opportunity for real improvements

**Psychology Research:** Publishing a finding that's actually just random chance

- Consequences: Other researchers waste time trying to replicate, field is misled

**Why It Happens:** Random sampling variation can produce "lucky" samples that look like there's an effect when there isn't one. With α = .05, this happens 5% of the time.

**How to Reduce Type I Errors:**

- Use lower α (e.g., .01 instead of .05)
- Require replication before accepting findings
- Use more conservative statistical tests

**Trade-off:** Being more conservative increases Type II errors

### Type II Error (False Negative)

**Definition:** Failing to reject H₀ when it's actually false. Missing a real effect.

**Probability:** β (beta, varies based on sample size, effect size, and alpha)

**Real-World Examples:**

**Medical:** Rejecting a drug that actually works

- Consequences: Patients don't get effective treatment

**Legal:** Failing to convict a guilty person

- Consequences: Dangerous person remains free

**Education:** Discarding a teaching program that actually helps

- Consequences: Students miss out on better instruction

**Psychology Research:** Concluding "no effect" when there really is one

- Consequences: Important findings are missed, research direction is misguided

**Why It Happens:**

- Sample size too small to detect the effect
- Effect is real but small
- Too much random variation in data

**How to Reduce Type II Errors:**

- Increase sample size (most important!)
- Use more sensitive measures
- Reduce random variation in procedures
- Use higher α (but this increases Type I errors)

**Trade-off:** Being less conservative increases Type I errors

### Balancing the Two Errors

You can't eliminate both types of errors simultaneously. There's always a trade-off.

**Making α more stringent (.01 instead of .05):**

- ↓ Decreases Type I errors (fewer false positives)
- ↑ Increases Type II errors (more false negatives)

**Making α more lenient (.10 instead of .05):**

- ↑ Increases Type I errors (more false positives)
- ↓ Decreases Type II errors (fewer false negatives)

**Increasing sample size:**

- ↓ Decreases Type II errors (more power to detect real effects)
- → Does NOT change Type I error rate (α stays the same)
- **This is why larger samples are almost always better!**

### Which Error is Worse?

**It depends on context!**

**When Type I is worse (false positives):**

- Approving dangerous medications
- Convicting innocent people
- Making expensive policy changes

**Strategy:** Use lower α, require strong evidence

**When Type II is worse (false negatives):**

- Screening for serious diseases (better to have false alarms than miss real cases)
- Exploratory research (missing real effects is costly)
- Safety testing (better to err on the side of caution)

**Strategy:** Use higher α, larger samples

### Mnemonics for Remembering

**Type I Error:**

- "Type I, α (first letter of alphabet), reject when shouldn't"
- Think: "I wrongly claimed I found something" (I = Type I)

**Type II Error:**

- "Type II, β (second letter of Greek alphabet), fail to reject when should"
- Think: "Two blind to see the real effect" (Two = Type II)

**Or use the pregnancy test analogy:**

- Type I: Test says pregnant when not (false positive)
- Type II: Test says not pregnant when actually pregnant (false negative)

### Real-World Example

**Clinical Trial for Depression Medication:**

**Sample:** 50 patients with depression
**Result:** Average improvement of 5 points on depression scale
**Statistical test:** p = .08

**Decision:** Fail to reject H₀ (p > .05)
**Conclusion:** No significant evidence the drug works

**But what if:**

- The drug really does work (5-point improvement is real)?
- Our sample was too small to detect it?
- We made a **Type II error**?

**Consequences:**

- Effective drug might be abandoned
- Patients miss out on helpful treatment
- Company loses money on drug development

**Better approach:**

- Run a larger study (more power to detect real effects)
- Look at effect size (is 5 points clinically meaningful?)
- Don't rely on a single study

### Quick Check

1. What type of error do you make if you reject H₀ but it's actually true?
2. How does increasing sample size affect Type II error?
3. If α = .05, how often will we make Type I errors in the long run?
4. Which error is committed more often: Type I or Type II?

<details>
<summary>Click to see answers</summary>

1. Type I error (false positive)
2. Decreases Type II error (increases power to detect real effects)
3. 5% of the time (when H₀ is true, we'll wrongly reject it 5% of the time)
4. Trick question! Type I rate is fixed at α. Type II rate (β) varies. Generally, Type II errors are more common because most studies are underpowered.
</details>

---

## Part 5: The Central Limit Theorem

The Central Limit Theorem (CLT) is one of the most important concepts in statistics. It's the "magic" that makes hypothesis testing work.

### The Problem It Solves

**Challenge:** Many populations in the real world aren't normally distributed.

- Income is right-skewed (few very wealthy people)
- Reaction times are right-skewed (can't be faster than 0, but can be very slow)
- Test scores might be bimodal (two groups with different abilities)

**Issue:** Many statistical tests assume normal distributions. What do we do?

**Solution:** The Central Limit Theorem!

### What the CLT States

**Formal Statement:** If you take many random samples of size n from ANY population (regardless of the population's shape) and calculate the mean of each sample, the distribution of those sample means will be approximately normal—especially as sample size increases.

**In Plain English:**

1. Take a population (any shape—skewed, uniform, bimodal, whatever)
2. Draw lots of random samples from it (each of size n)
3. Calculate the mean of each sample
4. Plot those sample means
5. **Result:** The distribution of sample means will be bell-shaped (normal)!

**The Bigger the Sample:** The more perfectly normal the distribution of sample means becomes.

### Why This is Magical

**It means:**

- Even if your population is weirdly shaped...
- You can still use the normal distribution to make inferences...
- Because you're testing a SAMPLE MEAN, not individual scores!

**Practical Implication:** This is why the t-test and other tests work even when populations aren't perfectly normal. We're comparing means, and the distribution of means is (nearly) always normal!

### Visual Example

**Starting Population:** Highly skewed (like income)

- Most people earn $30K-$50K
- A few earn $200K+
- Shape: Long right tail

**Sampling Process:**

- Sample 1 (n=25): M = $48,000
- Sample 2 (n=25): M = $52,000
- Sample 3 (n=25): M = $45,000
- ...
- Sample 1000 (n=25): M = $49,500

**Distribution of These 1000 Sample Means:**

- Shape: Bell curve! (Even though the population was skewed)
- Center: Near the true population mean
- Spread: Much narrower than the original population

### Key Properties

**1. The mean of the sampling distribution equals the population mean**
\[ \mu_M = \mu \]

The average of all possible sample means equals the true population mean.

**2. The standard deviation of the sampling distribution (Standard Error) is smaller than the population SD**
\[ \sigma_M = \frac{\sigma}{\sqrt{n}} \]

Sample means vary less than individual scores. Larger samples have even less variation.

**3. The shape approaches normal as n increases**

- n ≥ 30: Usually sufficient for good approximation
- n ≥ 100: Very close to perfect normal
- For populations already normal: Works even with small n

### Standard Error: The Variability of Means

**Standard Deviation (σ or s):** Measures how much individual scores vary around the population/sample mean

**Standard Error (σ_M or SE):** Measures how much sample means vary around the population mean

**Formula:**
\[ SE = \frac{s}{\sqrt{n}} \]

Where:

- s = sample standard deviation
- n = sample size

**Interpretation:** The standard error is the "typical distance" a sample mean is from the true population mean.

**Example:** Population with σ = 15

- Sample size n = 9: SE = 15/√9 = 15/3 = 5
- Sample size n = 25: SE = 15/√25 = 15/5 = 3
- Sample size n = 100: SE = 15/√100 = 15/10 = 1.5

**Notice:** As sample size increases, SE decreases. Larger samples give more precise estimates!

### Why the CLT Matters for Hypothesis Testing

**When we do a t-test, we're asking:**
"Is our sample mean far enough from the population mean to be unusual?"

**The CLT tells us:**

1. What "usual" sample means look like (normal distribution centered on μ)
2. How much variation to expect (standard error)
3. Therefore, how to calculate "how unusual" our sample mean is

**Without the CLT:** We couldn't use the t-test or most other inferential tests. We'd need different tests for every different population shape.

**With the CLT:** We can use the same tools for almost any population!

### Sample Size Requirements

**General Rules:**

- n ≥ 30: CLT works well for most populations
- n ≥ 15-20: Usually okay for roughly symmetric populations
- n < 15: Should check that population is approximately normal

**Exceptions:**

- If population is exactly normal: CLT works even with n = 2
- If population is extremely skewed or has outliers: Might need n > 50

**Practical Advice:** Aim for n ≥ 30 when possible. Larger is always better!

### Worked Example

**Population:** Reaction times (right-skewed)

- μ = 500 ms
- σ = 100 ms
- Shape: Skewed right (most fast, some very slow)

**You take a sample of n = 36 participants:**

- M = 520 ms
- s = 108 ms

**Question:** Is this sample mean unusual?

**Step 1: Calculate Standard Error**
\[ SE = \frac{s}{\sqrt{n}} = \frac{108}{\sqrt{36}} = \frac{108}{6} = 18 \text{ ms} \]

**Step 2: Calculate z-score for the sample mean**
\[ z = \frac{M - \mu}{SE} = \frac{520 - 500}{18} = \frac{20}{18} = 1.11 \]

**Step 3: Interpret**

- Sample mean is 1.11 standard errors above population mean
- Using z-table: About 13% of sample means would be this high or higher
- Not particularly unusual (p = .13 > .05)

**The CLT in Action:** Even though the population is skewed, we could use the normal distribution to evaluate our sample mean because the sampling distribution of means is normal!

### Quick Check

1. What does the Central Limit Theorem tell us about the distribution of sample means?
2. How does increasing sample size affect standard error?
3. Why can we use normal-distribution-based tests even when populations aren't normal?
4. What's the difference between standard deviation and standard error?

<details>
<summary>Click to see answers</summary>

1. They will be approximately normally distributed, regardless of population shape (especially with n ≥ 30)
2. Larger sample → smaller SE → more precise estimates (SE = s/√n)
3. Because we're testing sample means, and the CLT guarantees sample means are normally distributed
4. SD measures variability of individual scores; SE measures variability of sample means
</details>

---

## Part 6: The One-Sample t-Test

Now we put everything together into our first formal hypothesis test!

### When to Use a One-Sample t-Test

**Purpose:** Compare a sample mean to a known population mean

**Use when:**

- You have ONE sample
- You know the population mean (μ)
- You want to know if your sample is different from that population
- You DON'T know the population standard deviation (σ)

**Examples:**

- Do students at your university sleep less than the national average of 8 hours?
- Is the average IQ of chess players different from 100?
- Do elderly patients with Alzheimer's score below the normal MMSE score of 25?

### Why "t-Test" and Not "z-Test"?

**If we knew σ (population SD):** We'd use a z-test
\[ z = \frac{M - \mu}{\sigma / \sqrt{n}} \]

**But we almost never know σ!**

**Solution:** Use the sample SD (s) to estimate it, giving us the t-test
\[ t = \frac{M - \mu}{s / \sqrt{n}} \]

**The catch:** Using s instead of σ adds uncertainty, so we need a different distribution (t-distribution, covered in Part 9).

### The Seven Steps of Hypothesis Testing

#### Step 1: State Hypotheses

**For Two-Tailed Test:**

- H₀: μ = [known value]
- H₁: μ ≠ [known value]

**For One-Tailed Test (predicting higher):**

- H₀: μ ≤ [known value]
- H₁: μ > [known value]

**For One-Tailed Test (predicting lower):**

- H₀: μ ≥ [known value]
- H₁: μ < [known value]

#### Step 2: Set Alpha Level

Usually α = .05

#### Step 3: Calculate Descriptive Statistics

From your sample data:

- n (sample size)
- M (sample mean)
- s (sample standard deviation)

#### Step 4: Calculate Standard Error

\[ SE = \frac{s}{\sqrt{n}} \]

#### Step 5: Calculate t-Statistic

\[ t = \frac{M - \mu}{SE} = \frac{M - \mu}{s / \sqrt{n}} \]

**Interpretation:** How many standard errors is your sample mean from the population mean?

#### Step 6: Determine Degrees of Freedom and Find p-Value

**Degrees of freedom:** df = n - 1

**Then:**

- Use t-table to find critical value (manual method), OR
- Use SPSS to get exact p-value (easier!)

#### Step 7: Make Decision and State Conclusion

**Decision:**

- If p < α: Reject H₀ (significant result)
- If p ≥ α: Fail to reject H₀ (non-significant result)

**Conclusion:** Translate into meaningful statement about your research question

### Detailed Worked Example

**Research Question:** Does meditation reduce stress below the population mean of 50?

**Step 1: Hypotheses**

- H₀: μ ≥ 50 (meditation doesn't reduce stress below 50)
- H₁: μ < 50 (meditation reduces stress below 50)
- **Test type:** One-tailed (predicting specific direction)

**Step 2: Alpha**

- α = .05

**Step 3: Sample Data**

- n = 25 people who meditate regularly
- M = 45 (average stress score)
- s = 12 (standard deviation of stress scores)

**Step 4: Standard Error**
\[ SE = \frac{s}{\sqrt{n}} = \frac{12}{\sqrt{25}} = \frac{12}{5} = 2.4 \]

**Step 5: Calculate t**
\[ t = \frac{M - \mu}{SE} = \frac{45 - 50}{2.4} = \frac{-5}{2.4} = -2.08 \]

**Interpretation:** Our sample mean is 2.08 standard errors below the population mean.

**Step 6: Degrees of Freedom and p-Value**

- df = n - 1 = 25 - 1 = 24
- Using t-table or SPSS: p = .024 (two-tailed)
- For our one-tailed test: p_one-tailed = .024 / 2 = .012
- **Note:** Only divide by 2 if result is in predicted direction (it is—we predicted lower, and we got lower)

**Step 7: Decision**

- p (.012) < α (.05)
- **Reject H₀**

**Conclusion:**
"Individuals who meditate regularly (M = 45, SD = 12) had significantly lower stress scores than the general population mean of 50, t(24) = -2.08, p = .012, suggesting meditation is associated with reduced stress."

### Manual Calculation Practice

**Scenario:** National average depression score is μ = 30. A sample of 16 therapy patients has M = 25, s = 8. Test if therapy patients score differently from the national average.

**Your turn! Work through all 7 steps.**

<details>
<summary>Click to see solution</summary>

**Step 1:** H₀: μ = 30; H₁: μ ≠ 30 (two-tailed)

**Step 2:** α = .05

**Step 3:** n = 16, M = 25, s = 8

**Step 4:** SE = 8/√16 = 8/4 = 2

**Step 5:** t = (25-30)/2 = -5/2 = -2.5

**Step 6:** df = 15; from t-table, p < .05 (exact: p ≈ .025 two-tailed)

**Step 7:** Reject H₀. Therapy patients (M = 25) scored significantly lower than the national average of 30, t(15) = -2.5, p = .025.

</details>

### Assumptions of the One-Sample t-Test

For results to be valid, certain assumptions should be met:

**1. Random Sampling**

- Participants should be randomly selected from population
- **Why:** Ensures sample is representative
- **If violated:** Results may not generalize

**2. Independence of Observations**

- Each participant's score is independent of others
- **Why:** Violations inflate Type I error
- **If violated:** Use different analyses (e.g., multilevel models)

**3. Approximately Normal Distribution**

- Data should be roughly bell-shaped, OR sample size ≥ 30
- **Why:** t-test relies on normality (but robust to violations with larger n)
- **Check:** Look at histogram
- **If violated:** Consider non-parametric test (e.g., Wilcoxon signed-rank)

**Practical Note:** The t-test is "robust" to violations of normality, especially with n ≥ 30. Minor violations usually don't matter.

### Interpreting t-Values

**What does the t-value tell you?**

The t-value (like a z-score) measures how many standard errors your sample mean is from the population mean.

**Rules of Thumb:**

- |t| < 1.0: Sample mean is pretty close to population mean (probably not significant)
- |t| ≈ 2.0: Sample mean is ~2 SE from population mean (borderline significant)
- |t| > 3.0: Sample mean is far from population mean (likely very significant)

**Note:** Exact cutoffs depend on df (degrees of freedom) and alpha level.

### Common Mistakes

❌ **Mistake 1:** Using one-tailed when you should use two-tailed

- If research doesn't predict direction, use two-tailed!

❌ **Mistake 2:** Forgetting to divide SPSS p-value by 2 for one-tailed tests

- SPSS always gives two-tailed p
- For one-tailed: divide by 2 (if result is in predicted direction)

❌ **Mistake 3:** Interpreting "fail to reject" as "prove H₀ is true"

- You haven't proven no effect exists
- You just didn't find evidence of an effect

❌ **Mistake 4:** Confusing s (sample SD) with SE (standard error)

- SE = s / √n (always smaller than s)

❌ **Mistake 5:** Stopping at p-value without interpreting the result

- Always describe what the result means in context
- Include descriptive statistics (M, SD)

---

## Part 7: Effect Size: Measuring Practical Significance

Statistical significance tells you IF there's an effect. Effect size tells you HOW BIG the effect is.

### Why Effect Size Matters

**The Problem with p-Values Alone:**

**Example 1:** Tiny, trivial difference

- New diet: Participants lose M = 0.1 pounds more than control
- Sample size: n = 10,000
- Result: p = .001 (highly significant!)
- **But:** Who cares about 0.1 pounds? Practically meaningless.

**Example 2:** Large, important difference

- New therapy: Participants improve M = 15 points on depression scale
- Sample size: n = 12
- Result: p = .08 (not significant)
- **But:** 15 points is a huge improvement! Likely very important.

**Key Insight:** With large samples, even tiny differences become "significant." With small samples, even large differences might not reach "significance."

**Solution:** ALWAYS report effect size alongside p-values.

### Cohen's d: The Most Common Effect Size

**Definition:** Cohen's d measures the standardized difference between a sample mean and population mean (or between two means).

**For One-Sample t-Test:**
\[ d = \frac{M - \mu}{s} \]

Where:

- M = sample mean
- μ = population mean
- s = sample standard deviation

**Interpretation:** How many standard deviations apart are the two means?

### Cohen's Benchmarks

Jacob Cohen proposed rough guidelines for interpreting d:

| Cohen's d | Interpretation    | Overlap Between Distributions |
| :-------- | :---------------- | :---------------------------- |
| d = 0.2   | **Small** effect  | 85% overlap                   |
| d = 0.5   | **Medium** effect | 67% overlap                   |
| d = 0.8   | **Large** effect  | 53% overlap                   |

**Important Caveats:**

- These are just guidelines, not rigid rules
- What's "large" in one field might be "small" in another
- Consider practical/clinical significance in your specific context

### Calculating Cohen's d: Examples

**Example 1:** Meditation and stress

- Population mean: μ = 50
- Sample: M = 45, s = 12
- \[ d = \frac{45 - 50}{12} = \frac{-5}{12} = -0.42 \]
- **Interpretation:** Small to medium effect (stress is 0.42 SD below population mean)

**Example 2:** Reading program effectiveness

- Population mean: μ = 100
- Sample: M = 112, s = 15
- \[ d = \frac{112 - 100}{15} = \frac{12}{15} = 0.80 \]
- **Interpretation:** Large effect (reading scores are 0.80 SD above population mean)

**Example 3:** Memory drug trial

- Population mean: μ = 50
- Sample: M = 52, s = 10
- \[ d = \frac{52 - 50}{10} = \frac{2}{10} = 0.20 \]
- **Interpretation:** Small effect (memory is 0.20 SD above population mean)

### Interpreting Effect Sizes in Context

**Don't just rely on Cohen's benchmarks!** Consider:

**1. Field-Specific Norms**

- In physics: d = 0.2 might be considered large
- In psychology/education: d = 0.2 is genuinely small

**2. Clinical/Practical Importance**

- d = 0.3 for a simple, cheap intervention might be very valuable
- d = 0.3 for an expensive, risky treatment might not be worthwhile

**3. Costs and Benefits**

- Small effects can matter if intervention is inexpensive or harm-free
- Large effects are needed if intervention is costly or has risks

**4. Comparison to Existing Alternatives**

- d = 0.4 is impressive if current best treatment has d = 0.2
- d = 0.4 is unimpressive if current treatment already achieves d = 0.8

### Effect Size vs. Statistical Significance: Four Scenarios

**Scenario A: Large effect, significant (ideal!)**

- d = 0.9, p = .001, n = 50
- **Interpretation:** Strong evidence of a substantial effect
- **Action:** Strong support for the intervention/theory

**Scenario B: Small effect, significant (common with large samples)**

- d = 0.1, p = .02, n = 1000
- **Interpretation:** Statistically reliable but tiny effect
- **Action:** Consider practical value before implementing

**Scenario C: Large effect, not significant (underpowered study)**

- d = 0.9, p = .09, n = 10
- **Interpretation:** Possibly important effect, but insufficient evidence
- **Action:** Replicate with larger sample

**Scenario D: Small effect, not significant**

- d = 0.1, p = .45, n = 30
- **Interpretation:** Little evidence of an effect
- **Action:** Likely not worthwhile to pursue

**The Complete Picture:** Always report BOTH p-value AND effect size. They tell different parts of the story.

### Reporting Effect Size in APA Format

**Include d in your results statement:**

**Format:**
"[Group description], M = [mean], SD = [standard deviation], [comparison description], t([df]) = [t-value], p = [p-value], d = [Cohen's d]."

**Examples:**

**Example 1:**
"Participants who meditated regularly (M = 45, SD = 12) reported significantly lower stress than the general population mean of 50, t(24) = -2.08, p = .012, d = 0.42."

**Example 2:**
"Students using the new reading program (M = 112, SD = 15) scored significantly higher than the national average of 100, t(29) = 4.38, p < .001, d = 0.80."

**Example 3:**
"Patients receiving the experimental memory drug (M = 52, SD = 10) did not differ significantly from the population mean of 50, t(19) = 0.89, p = .38, d = 0.20."

**Note:** Report d even when results are not significant! Effect size estimates are valuable regardless.

### Quick Check

1. Why is effect size important beyond just p-values?
2. Calculate Cohen's d: M = 85, μ = 75, s = 20
3. Is d = 0.3 always a "small" effect?
4. Can you have a significant result with a small effect size?

<details>
<summary>Click to see answers</summary>

1. p-value tells IF there's an effect; d tells HOW BIG it is. Large samples can make trivial differences significant.
2. d = (85-75)/20 = 10/20 = 0.5 (medium effect)
3. No! Context matters. It might be large in physics, meaningful for a cheap intervention, or insufficient for a risky treatment.
4. Yes! With very large samples, even d = 0.1 can be p < .05 (statistically significant but practically small)
</details>

---

## Part 8: Statistical Power

Power is your study's ability to detect a real effect when one exists. Understanding power helps you design better studies and interpret null results.

### What is Statistical Power?

**Definition:** The probability of correctly rejecting a false null hypothesis (detecting a real effect when it exists).

**In the Error Matrix:**

- Power = Probability of True Positive
- Power = 1 - β (where β = probability of Type II error)

**Standard Goal:** Power ≥ .80 (80% chance of detecting a real effect)

**What Power Means:**

| Power | Interpretation                                            |
| :---- | :-------------------------------------------------------- |
| .50   | 50% chance of detecting real effect (coin flip—terrible!) |
| .80   | 80% chance of detecting real effect (acceptable)          |
| .90   | 90% chance of detecting real effect (good)                |
| .95   | 95% chance of detecting real effect (excellent)           |

### Why Power Matters

**Low Power Studies (e.g., power = .30):**

- Even if effect exists, you'll probably miss it (70% chance of Type II error)
- Null results are uninterpretable (effect might exist but study couldn't detect it)
- Waste of resources and participants' time

**High Power Studies (e.g., power = .85):**

- Good chance of detecting real effects
- Null results are more meaningful (if effect existed, you likely would've found it)
- Efficient use of resources

**Real-World Consequence:** Many published studies are underpowered, leading to:

- Missed discoveries (Type II errors)
- Overestimated effect sizes (only the "lucky" studies reach significance)
- Non-replicable findings

### Factors Affecting Power

**Four main factors determine power:**

#### 1. Sample Size (n)

**Effect on Power:** ↑ Larger sample = ↑ Higher power

**Why:** Larger samples give more precise estimates (smaller SE), making it easier to detect real differences.

**Example:** True effect size d = 0.5

- n = 10: Power = .18 (only 18% chance of detecting it!)
- n = 30: Power = .48
- n = 64: Power = .80 (acceptable!)
- n = 100: Power = .94

**This is the easiest factor to control!** Want more power? Get more participants.

#### 2. Effect Size in Population

**Effect on Power:** ↑ Larger effect = ↑ Higher power

**Why:** Larger effects are easier to detect.

**Example:** With n = 30

- Small effect (d = 0.2): Power = .11 (very low!)
- Medium effect (d = 0.5): Power = .48
- Large effect (d = 0.8): Power = .80

**Implication:** If effects are small, you need larger samples to detect them.

**But:** You can't control true effect size! You can only estimate it and plan accordingly.

#### 3. Alpha Level (α)

**Effect on Power:** ↑ Higher α = ↑ Higher power

**Why:** Being less strict (larger α) makes it easier to reject H₀.

**Example:** With n = 50, d = 0.5

- α = .01: Power = .59
- α = .05: Power = .80
- α = .10: Power = .90

**Trade-off:** Higher α increases power BUT also increases Type I error rate.

**Standard Practice:** Keep α = .05 and adjust sample size instead.

#### 4. One-Tailed vs. Two-Tailed Test

**Effect on Power:** One-tailed test has higher power (for detecting effects in predicted direction)

**Why:** All alpha is concentrated in one tail instead of split between two.

**Example:** n = 30, d = 0.5

- Two-tailed: Power = .48
- One-tailed: Power = .61

**Caution:** Only use one-tailed if you have strong directional prediction and truly don't care about effects in the opposite direction.

### Power Analysis: Before vs. After Study

#### A Priori Power Analysis (BEFORE collecting data)

**Purpose:** Determine required sample size to achieve desired power

**Process:**

1. Decide desired power (usually .80)
2. Set alpha level (usually .05)
3. Estimate expected effect size (from literature or pilot study)
4. Use power analysis software to calculate required n

**Example:** Planning a study

- Expected effect: d = 0.5 (medium)
- Desired power: .80
- Alpha: .05 (two-tailed)
- **Result:** Need n ≥ 64

**This is best practice for study design!**

#### Post Hoc Power Analysis (AFTER collecting data)

**Purpose:** Understand the power you actually had

**Process:**

1. Calculate observed effect size from your data
2. Use your actual sample size
3. Calculate power you had to detect an effect that size

**Example:** After a study with null result

- n = 20
- Observed d = 0.3
- **Retrospective power:** .14 (only 14%!)
- **Interpretation:** Study was severely underpowered; null result is uninterpretable

**Controversy:** Some statisticians argue post-hoc power is not useful. But it helps explain why you might have gotten null results.

### Interpreting Null Results Through the Lens of Power

**High-Powered Study with Null Result:**

- n = 100, power was .90 for medium effects
- p = .52
- **Interpretation:** Strong evidence that effect is small or non-existent
- **Confidence:** Can reasonably conclude no meaningful effect

**Low-Powered Study with Null Result:**

- n = 15, power was .20 for medium effects
- p = .31
- **Interpretation:** Study couldn't detect an effect even if one exists
- **Confidence:** Can't conclude anything; study was inadequate

**The Bottom Line:** Null results from underpowered studies are meaningless!

### Increasing Power: Practical Strategies

**1. Increase Sample Size (Most Important!)**

- Recruit more participants
- Even small increases help
- Calculate required n before starting

**2. Use More Reliable Measures**

- Reduces random error (noise)
- Makes real effects easier to detect
- Use validated, well-tested instruments

**3. Reduce Variability in Procedures**

- Standardize testing conditions
- Train experimenters thoroughly
- Control extraneous variables
- Less noise = easier to see signal

**4. Use Within-Subjects Designs (When Possible)**

- More powerful than between-subjects
- Reduces individual differences
- (Covered more in Module 3)

**5. Maximize Effect Size**

- Use stronger manipulations/interventions
- Ensure treatment fidelity
- Select participants likely to show effects

**What NOT to Do:**

- ❌ Don't just increase alpha (increases Type I errors)
- ❌ Don't use one-tailed tests just for power (unless genuinely appropriate)
- ❌ Don't run underpowered studies and hope for the best

### Power in Research Ethics

**Ethical Issue:** Running underpowered studies is arguably unethical.

**Why:**

- Wastes participants' time and trust
- Wastes research resources
- Unlikely to contribute meaningful knowledge
- May lead to false conclusions

**Best Practice:**

- Always conduct power analysis before data collection
- Aim for power ≥ .80
- If you can't achieve adequate power, reconsider the study design

### Quick Check

1. What does power = .70 mean?
2. What's the easiest way to increase statistical power?
3. Why is a null result from a low-powered study hard to interpret?
4. If you have power = .80 for d = 0.5, is your power higher or lower for d = 0.8?

<details>
<summary>Click to see answers</summary>

1. 70% probability of detecting a real effect if one exists (30% chance of Type II error)
2. Increase sample size
3. You don't know if there's no effect, or if the effect exists but your study couldn't detect it
4. Higher! Larger effects are easier to detect, so power would be > .80
</details>

---

## Part 9: The t-Distribution

We've been using the t-test, but what exactly is this "t-distribution"?

### Why Not Use the Normal Distribution (z)?

**Remember the z-score formula:**
\[ z = \frac{X - \mu}{\sigma} \]

**For testing sample means:**
\[ z = \frac{M - \mu}{\sigma / \sqrt{n}} \]

**The problem:** We almost never know σ (population standard deviation)!

**Our solution:** Substitute s (sample standard deviation)
\[ t = \frac{M - \mu}{s / \sqrt{n}} \]

**New problem:** Using s instead of σ adds uncertainty. The regular normal distribution doesn't account for this extra uncertainty.

**The fix:** Use the t-distribution, which adjusts for this uncertainty!

### Properties of the t-Distribution

**Similarities to Normal Distribution:**

- Symmetrical
- Bell-shaped
- Centered on zero
- Area under curve = 1.0

**Differences from Normal Distribution:**

- **Heavier tails** (more area in the extremes)
- **Flatter peak** (less area in the center)
- **Shape depends on degrees of freedom (df)**

**Why Heavier Tails?**

- Reflects the extra uncertainty from estimating σ with s
- Means you need a larger t-value (vs. z-value) to reach significance
- More conservative than z-test (less likely to make Type I errors)

### Degrees of Freedom (df)

**Definition:** The number of values that are "free to vary" when calculating a statistic.

**For One-Sample t-Test:**
\[ df = n - 1 \]

**Why n - 1?**

- Once you know the mean and (n-1) scores, the last score is determined
- Example: If M = 10 and you know 4 out of 5 scores are {8, 9, 11, 12}, the 5th MUST be 10 (to make the mean = 10)

**Effect on t-Distribution:**

| df                  | Shape of t-Distribution          |
| :------------------ | :------------------------------- |
| Small (df = 1-5)    | Very heavy tails, very flat      |
| Medium (df = 10-20) | Moderately heavy tails           |
| Large (df = 30+)    | Very close to normal             |
| df = ∞              | Identical to normal distribution |

**Practical Implication:** With larger samples (higher df), the t-distribution approaches the normal distribution.

### Critical Values: t vs. z

**Critical values** are the thresholds for significance. Let's compare for α = .05, two-tailed:

| df  | t-critical | z-critical |
| :-- | :--------- | :--------- |
| 5   | ±2.571     | ±1.96      |
| 10  | ±2.228     | ±1.96      |
| 20  | ±2.086     | ±1.96      |
| 30  | ±2.042     | ±1.96      |
| 60  | ±2.000     | ±1.96      |
| ∞   | ±1.96      | ±1.96      |

**Notice:**

- With small samples (low df), t-critical is much larger than z-critical
- As sample size increases, t-critical approaches z-critical
- You need a more extreme t-value to reject H₀ with small samples

**Why This Matters:** Small samples require stronger evidence (larger t-values) to reach the same significance level. This protects against Type I errors when sample information is limited.

### Using the t-Table

**To find critical value (manual hypothesis testing):**

1. Calculate df = n - 1
2. Choose alpha level (usually .05)
3. Determine one-tailed vs. two-tailed
4. Find where df row meets alpha column
5. That's your critical value

**Example:** n = 25, α = .05, two-tailed

- df = 24
- Look up df = 24, α = .05 (two-tailed)
- Critical value = ±2.064

**Decision:**

- If |t_calculated| > 2.064: Reject H₀
- If |t_calculated| ≤ 2.064: Fail to reject H₀

**Modern Approach:** SPSS calculates exact p-values for you, so you rarely need t-tables for research. But understanding them builds intuition!

### t vs. z: When to Use Each

**Use z-test when:**

- You know the population standard deviation (σ)
- This is rare! Usually only in textbook examples

**Use t-test when:**

- You don't know population standard deviation (most real research)
- You're estimating σ with sample s
- This is the standard approach!

**Practical Reality:** You'll almost always use t-tests, not z-tests.

---

## Part 10: Practical Guide: SPSS for One-Sample t-Tests

This section walks you through conducting one-sample t-tests in SPSS, from data setup to interpretation.

### Setting Up Your Data

**Step 1: Import or Enter Data**

- `File → Import Data → Excel` (if importing)
- Or manually enter data in Data View

**Step 2: Configure Variables (Variable View)**

- Set measurement level to "Scale" for your continuous variable
- Add descriptive labels
- Set appropriate decimals

**Step 3: Check Your Data**

- Look for outliers (extremely high/low values)
- Check for data entry errors
- Verify n is correct

### Running a Basic One-Sample t-Test

**Step 1: Access the Menu**

- `Analyze → Compare Means → One-Sample T Test`

**Step 2: Select Variables**

- Move your test variable from left box to "Test Variable(s)" box
- You can test multiple variables at once if they're all compared to the same test value

**Step 3: Enter Test Value**

- In "Test Value" box, enter the known population mean (μ)
- Example: If testing against population mean of 100, enter 100

**Step 4: Request Effect Size (Recommended)**

- Click "Options" button
- Check "Confidence Intervals"
- Click "Effect Sizes" tab
- Check "Cohen's d"
- Click "Continue"

**Step 5: Run the Test**

- Click "OK"
- Results appear in Output window

### Reading SPSS Output

SPSS produces two main tables:

#### Table 1: One-Sample Statistics

| Variable | N   | Mean   | Std. Deviation | Std. Error Mean |
| :------- | :-- | :----- | :------------- | :-------------- |
| IQ_Score | 30  | 107.50 | 14.23          | 2.60            |

**What It Tells You:**

- **N:** Sample size (30)
- **Mean:** Sample mean (107.50)
- **Std. Deviation:** Sample SD (14.23)
- **Std. Error Mean:** SE = s/√n (2.60)

**Use these for:** Describing your sample, calculating effect size

#### Table 2: One-Sample Test (Testing against μ = 100)

| Variable | t    | df  | Sig. (2-tailed) | Mean Difference | 95% CI Lower | 95% CI Upper | Cohen's d |
| :------- | :--- | :-- | :-------------- | :-------------- | :----------- | :----------- | :-------- |
| IQ_Score | 2.88 | 29  | .007            | 7.50            | 2.17         | 12.83        | 0.53      |

**What It Tells You:**

- **t:** t-statistic (2.88)
- **df:** Degrees of freedom (29 = 30-1)
- **Sig. (2-tailed):** p-value for two-tailed test (.007)
- **Mean Difference:** M - μ (107.50 - 100 = 7.50)
- **95% CI:** Confidence interval for the difference (2.17 to 12.83)
- **Cohen's d:** Effect size (0.53, medium effect)

### Interpreting Results

**Decision:**

- p = .007
- α = .05
- Since .007 < .05, **reject H₀**

**Interpretation:**
"The sample (M = 107.50, SD = 14.23) scored significantly higher than the population mean of 100, t(29) = 2.88, p = .007, d = 0.53."

### One-Tailed Tests in SPSS

**SPSS always reports two-tailed p-values.** For one-tailed tests:

**Step 1: Check Direction**

- Is your result in the predicted direction?
- If predicting higher: Is M > μ?
- If predicting lower: Is M < μ?

**Step 2: Convert p-Value**

- If result is in predicted direction: p_one-tailed = p_two-tailed / 2
- If result is in opposite direction: p_one-tailed = 1 - (p_two-tailed / 2)
  - But you'd fail to reject H₀ anyway!

**Example 1:** Predicting IQ > 100

- Observed: M = 107.50 (higher than 100 ✓)
- SPSS gives: p = .007 (two-tailed)
- One-tailed p = .007 / 2 = **.0035**
- Even more significant!

**Example 2:** Predicting stress < 50

- Observed: M = 52 (higher than 50, wrong direction ✗)
- SPSS gives: p = .20 (two-tailed)
- **Fail to reject H₀** (result is opposite of prediction)

### Filtering Data in SPSS

Sometimes you need to analyze a subset of your data.

**Step 1: Select Cases**

- `Data → Select Cases`

**Step 2: Specify Condition**

- Choose "If condition is satisfied"
- Click "If..." button

**Step 3: Write the Condition**

- Examples:
  - `Age >= 75` (select only ages 75+)
  - `Gender = 1` (select only code 1, if 1=Female)
  - `Score > 50 AND Group = 2` (combine conditions)

**Step 4: Click OK**

- Filtered-out cases show diagonal slash through row number
- Only selected cases are used in analyses

**Step 5: Turn Off Filter When Done**

- `Data → Select Cases → All cases`

### Common SPSS Issues and Solutions

**Issue:** "Test Value" is grayed out
**Solution:** Make sure you've moved a variable to the Test Variable(s) box first

**Issue:** Can't find effect size in output
**Solution:** You must request it before running the test (Options → Effect Sizes → Cohen's d)

**Issue:** p-value shows as .000
**Solution:** SPSS rounds very small p-values. Report as "p < .001" (not p = .000)

**Issue:** Results seem wrong after filtering
**Solution:** Check that filter is set correctly. Look for slash marks on rows to see what's filtered out.

**Issue:** Want to compare to a value not in my data
**Solution:** That's fine! The "Test Value" doesn't need to be in your dataset—it's the population value you're testing against.

### Practice Exercise

**Scenario:** You have data on reaction times (in ms) for 40 gamers. Population average for non-gamers is μ = 250 ms. Test if gamers are significantly faster.

**Your Data:**

- n = 40
- M = 235 ms
- s = 30 ms

**Tasks:**

1. Write hypotheses (one-tailed, predicting faster = lower times)
2. Run one-sample t-test in SPSS
3. Interpret results with APA formatting

<details>
<summary>Click to see expected results</summary>

**Hypotheses:**

- H₀: μ ≥ 250
- H₁: μ < 250 (gamers are faster)

**Expected Calculations:**

- SE = 30/√40 = 4.74
- t = (235-250)/4.74 = -3.16
- df = 39
- p (two-tailed) ≈ .003
- p (one-tailed) = .003/2 = .0015
- d = (235-250)/30 = -0.50

**APA Report:**
"Gamers (M = 235, SD = 30) had significantly faster reaction times than the non-gamer population mean of 250 ms, t(39) = -3.16, p = .002, d = 0.50."

</details>

---

## Summary and Key Formulas

### The Hypothesis Testing Process

1. Formulate hypotheses (H₀ and H₁)
2. Set alpha level (α = .05)
3. Collect data and calculate statistics
4. Compute test statistic and p-value
5. Compare p to α
6. Make decision (reject or fail to reject H₀)
7. Interpret in context

### Core Concepts

**Null Hypothesis (H₀):** Statement of no effect/no difference

**Alternative Hypothesis (H₁):** Research prediction; what you're trying to support

**p-Value:** Probability of getting your results (or more extreme) if H₀ is true

**Alpha (α):** Significance threshold (usually .05)

**Type I Error:** False positive (reject true H₀), probability = α

**Type II Error:** False negative (fail to reject false H₀), probability = β

**Power:** Probability of correctly detecting real effect = 1 - β

**Effect Size (d):** Standardized measure of how large an effect is

### Key Formulas

**Standard Error:**
\[ SE = \frac{s}{\sqrt{n}} \]

**t-Statistic (One-Sample):**
\[ t = \frac{M - \mu}{SE} = \frac{M - \mu}{s / \sqrt{n}} \]

**Degrees of Freedom (One-Sample t-Test):**
\[ df = n - 1 \]

**Cohen's d (One-Sample):**
\[ d = \frac{M - \mu}{s} \]

**Interpretation:**

- d = 0.2: Small effect
- d = 0.5: Medium effect
- d = 0.8: Large effect

### Decision Rules

**Statistical Significance:**

- If p < α: Reject H₀ (significant)
- If p ≥ α: Fail to reject H₀ (not significant)

**One-Tailed p-Value (in SPSS):**

- If result is in predicted direction: p_one-tailed = p_SPSS / 2
- If result is in wrong direction: Fail to reject H₀

### APA Format for One-Sample t-Test

**Template:**
"[Sample description] (M = [mean], SD = [SD]) [comparison statement], t([df]) = [t-value], p = [p-value], d = [Cohen's d]."

**Example:**
"College students (M = 6.2, SD = 1.3) slept significantly less than the recommended 8 hours, t(149) = -8.52, p < .001, d = 1.38."

### Critical Distinctions

**Statistical vs. Practical Significance:**

- Statistical: p < .05 (unlikely due to chance)
- Practical: Effect is large enough to matter

**One-Tailed vs. Two-Tailed:**

- One-tailed: Predicts specific direction; more power
- Two-tailed: Detects any difference; more conservative

**Sample SD (s) vs. Standard Error (SE):**

- s: Variability of individual scores
- SE: Variability of sample means (always smaller)

**Reject H₀ vs. Accept H₁:**

- Don't say "accept H₁" or "prove H₁"
- Say "reject H₀" or "evidence supports H₁"

---

## Glossary

**Alpha Level (α):** Threshold for significance; probability of Type I error

**Alternative Hypothesis (H₁):** Research prediction; statement of effect/difference

**Central Limit Theorem (CLT):** Distribution of sample means approaches normal

**Cohen's d:** Standardized effect size measure

**Critical Value:** Threshold t-value for rejecting H₀

**Degrees of Freedom (df):** Number of values free to vary; n - 1 for one-sample t-test

**Effect Size:** Magnitude of difference/effect, independent of sample size

**Null Hypothesis (H₀):** Statement of no effect/no difference

**One-Tailed Test:** Directional hypothesis (predicts specific direction)

**p-Value:** Probability of results (or more extreme) if H₀ is true

**Power:** Probability of detecting real effect; 1 - β

**Standard Error (SE):** Standard deviation of sampling distribution of means

**Statistical Significance:** Result unlikely due to chance alone (p < α)

**t-Distribution:** Probability distribution used when σ is unknown

**t-Statistic:** Test statistic measuring how many SEs sample mean is from μ

**Test Statistic:** Calculated value used to determine p-value

**Two-Tailed Test:** Non-directional hypothesis (detects any difference)

**Type I Error:** False positive; rejecting true H₀

**Type II Error:** False negative; failing to reject false H₀

---

## Frequently Asked Questions

**Q: What's the difference between failing to reject H₀ and accepting H₀?**
A: "Failing to reject" means you didn't find sufficient evidence against H₀—not that you proved it true. "Accepting H₀" wrongly implies you've proven no effect exists. Always use "fail to reject."

**Q: When should I use a one-tailed vs. two-tailed test?**
A: Use one-tailed only when you have a strong, directional prediction AND truly don't care about effects in the opposite direction. When in doubt, use two-tailed (safer, more conservative).

**Q: Why is α = .05 the standard?**
A: Somewhat arbitrary! Ronald Fisher proposed it in the 1920s. It balances Type I and Type II errors reasonably well. Some fields use stricter (.01) or more lenient (.10) standards.

**Q: Can I change from two-tailed to one-tailed after seeing my data?**
A: No! This is p-hacking and inflates Type I error. You must decide before collecting data.

**Q: What if my p-value is exactly .05?**
A: Technically not significant (need p < .05, not p ≤ .05). But in practice, report the exact p-value and let readers judge. Don't obsess over arbitrary cutoffs.

**Q: Is a larger or smaller t-value better?**
A: Larger absolute value (farther from zero) is more extreme. |t| = 3.5 is more significant than |t| = 1.2.

**Q: Do I report negative t-values as negative?**
A: Yes! The sign indicates direction. t = -2.5 means sample mean is below population mean.

**Q: What if my effect size is large but p > .05?**
A: Likely underpowered study. The effect might be real but you needed more participants. Report both statistics and discuss power.

**Q: Should I remove outliers from my data?**
A: Only if you have a valid reason (data entry error, participant didn't follow instructions, etc.). Never remove outliers just to get significance. If outliers are legitimate data, consider robust methods or report results with and without them.

**Q: What's a "good" sample size for a one-sample t-test?**
A: Depends on expected effect size. For medium effects (d = 0.5), n ≈ 34 gives power = .80. Always conduct power analysis before collecting data!

---

## Connections to Other Modules

**From Module 1:**

- Sample vs. population (statistics vs. parameters)
- Mean and standard deviation calculations
- Normal distribution and z-scores
- **Building to M2:** Now we use these to test hypotheses!

**To Module 3:**

- One-sample t-test compares sample to known population
- **Next:** Independent-samples t-test compares TWO samples
- Same logic, different formula

**To Module 4:**

- t-test compares two means (sample vs. population, or sample 1 vs. sample 2)
- **Next:** ANOVA compares THREE OR MORE means
- Extension of the same hypothesis testing framework

**To Module 6:**

- Hypothesis testing logic applies to all statistical tests
- **Next:** Test relationships (correlation) and prediction (regression)
- Same decision-making framework (p-values, effect sizes, power)

**The Through-Line:** The hypothesis testing logic you learned in M2 applies to EVERY statistical test you'll learn. Master this framework now!

---

## Final Thoughts

Hypothesis testing is the foundation of inferential statistics. The logic—testing the null hypothesis, calculating p-values, considering effect sizes and power—applies to virtually every statistical method you'll encounter.

**Key Principles to Remember:**

1. **We never prove, only disprove:** We reject H₀ or fail to reject it; we don't "accept" or "prove" hypotheses

2. **Statistical significance ≠ importance:** Always consider effect size alongside p-values

3. **Power matters:** Underpowered studies waste resources and provide uninterpretable null results

4. **Context is crucial:** Numbers don't interpret themselves; connect statistics to research questions

5. **Be honest and transparent:** Report all results, not just significant ones; decide analysis plans before seeing data

As you complete the M2 assignment, focus on understanding the **why** behind each step. When you calculate a t-statistic, think about what it represents. When you see a p-value, consider what it does (and doesn't) tell you. When you compute Cohen's d, reflect on what it means practically.

The one-sample t-test is just the beginning. The logic you've learned here will serve you throughout your statistical journey—and throughout your career as you evaluate claims, interpret research, and make evidence-based decisions.

**You've got this!** Hypothesis testing is logical, systematic, and powerful. Take it one step at a time, and it will all make sense.

---

_Remember: Statistics is a way of thinking about evidence, not just a set of formulas. When in doubt, ask yourself: "What question am I trying to answer, and what would constitute convincing evidence?"_
