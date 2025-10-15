---
layout: lecture
title: "Module 2: Introduction to Hypothesis Testing and the One-Sample t-Test"
---

<h1>Module 2: Introduction to Hypothesis Testing and the One-Sample t-Test</h1>

<strong>Estimated Study Time:</strong> 2-3 hours

<h2>Learning Objectives</h2>

By the end of this module, you will be able to:

<ol>
<li>Explain the logic and purpose of hypothesis testing</li>
<li>Formulate null and alternative hypotheses for research questions</li>
<li>Distinguish between one-tailed and two-tailed tests</li>
<li>Understand and interpret p-values in the context of statistical decisions</li>
<li>Identify and explain Type I and Type II errors</li>
<li>Apply the Central Limit Theorem to understand sampling distributions</li>
<li>Conduct and interpret a one-sample t-test (manually and using SPSS)</li>
<li>Calculate and interpret effect sizes (Cohen's d)</li>
<li>Understand the concept of statistical power and factors that influence it</li>
<li>Report statistical results in APA format</li>
</ol>

---

<div class="lecture-tabs">
    <div class="tab-navigation">
        <button class="tab-button active" onclick="showTab(1)">
            <input type="checkbox" id="progress-1" class="tab-checkbox" onchange="toggleTabComplete(1)">
            <span class="tab-label">Hypothesis Testing Logic</span>
        </button>
        <button class="tab-button" onclick="showTab(2)">
            <input type="checkbox" id="progress-2" class="tab-checkbox" onchange="toggleTabComplete(2)">
            <span class="tab-label">Decision Making & Errors</span>
        </button>
        <button class="tab-button" onclick="showTab(3)">
            <input type="checkbox" id="progress-3" class="tab-checkbox" onchange="toggleTabComplete(3)">
            <span class="tab-label">Sampling & t-Tests</span>
        </button>
        <button class="tab-button" onclick="showTab(4)">
            <input type="checkbox" id="progress-4" class="tab-checkbox" onchange="toggleTabComplete(4)">
            <span class="tab-label">Effect Size & Power</span>
        </button>
        <button class="tab-button" onclick="showTab(5)">
            <input type="checkbox" id="progress-5" class="tab-checkbox" onchange="toggleTabComplete(5)">
            <span class="tab-label">Application & Summary</span>
        </button>
    </div>
    
    <div class="tab-content">
        <div id="tab-1" class="tab-panel active">

<h2>Part 1: The Logic of Hypothesis Testing</h2>

<h3>From Description to Inference</h3>

In Module 1, you learned to <strong>describe</strong> data using means, standard deviations, and graphs. Now we take the crucial next step: using sample data to make <strong>inferences</strong> about populations.

<strong>The Central Challenge:</strong> We can't study everyone, so we study a sample. But how do we know if what we observe in our sample reflects a real pattern in the population, or is just random chance?

<strong>The Solution:</strong> Hypothesis testing—a systematic method for distinguishing signal from noise.

<h3>The Courtroom Analogy</h3>

Hypothesis testing works like a legal trial. This analogy is powerful and worth understanding deeply.

<strong>In a Courtroom:</strong>

<ul>
<li><strong>Presumption of Innocence:</strong> The defendant is assumed innocent until proven guilty</li>
<li><strong>Burden of Proof:</strong> The prosecution must provide strong evidence of guilt</li>
<li><strong>Standard of Proof:</strong> "Beyond a reasonable doubt"</li>
<li><strong>Decision:</strong> If evidence is overwhelming, we reject innocence and conclude guilt. If evidence is weak, we maintain the presumption of innocence (we don't declare the person "innocent," just "not proven guilty")</li>
</ul>

<strong>In Hypothesis Testing:</strong>

<ul>
<li><strong>Null Hypothesis (H₀):</strong> We assume "nothing special is happening" (like presuming innocence)</li>
<li><strong>Burden of Proof:</strong> Our data must provide strong evidence against this assumption</li>
<li><strong>Standard of Proof:</strong> p < .05 (less than 5% probability the result is due to chance)</li>
<li><strong>Decision:</strong> If evidence is strong (p < .05), we reject H₀ and conclude there IS an effect. If evidence is weak (p ≥ .05), we maintain H₀ (we don't "prove" H₀, just fail to find evidence against it)</li>
</ul>

<strong>Key Concept:</strong> We never "prove" anything in statistics. We only collect evidence strong enough to reject the null hypothesis, or fail to do so.

<h3>Why This Backward Logic?</h3>

<strong>Why not just test our research hypothesis directly?</strong>

Because we can never observe all possible outcomes. Consider:

<strong>Direct Approach (doesn't work):</strong> "Does this drug improve memory?"

<ul>
<li>To prove this directly, we'd need to test every possible person, under every possible condition, forever</li>
<li>Impossible!</li>
</ul>

<strong>Indirect Approach (hypothesis testing):</strong> "Assume the drug does nothing. How likely is it we'd see results this good by chance alone?"

<ul>
<li>If the probability is very low (p < .05), the "does nothing" assumption is probably wrong</li>
<li>We reject that assumption and conclude the drug likely works</li>
</ul>

<strong>Think of it like proof by contradiction in mathematics:</strong> To prove X is true, assume X is false and show that leads to an impossible or highly unlikely situation. Therefore, X must be true.

<h3>The Hypothesis Testing Process: Overview</h3>

Here's the big picture before we dive into details:

1. <strong>Start with a research question</strong>

   - Example: "Does meditation reduce anxiety?"

2. <strong>Formulate hypotheses</strong>

   - H₀ (Null): Meditation has no effect on anxiety (μ = population mean)
   - H₁ (Alternative): Meditation does affect anxiety (μ ≠ population mean)

3. <strong>Set decision criteria</strong>

   - Alpha level: Usually α = .05

4. <strong>Collect data</strong>

   - Sample of people who meditate regularly

5. <strong>Calculate a test statistic</strong>

   - Measures how far your sample result is from what H₀ predicts

6. <strong>Determine probability (p-value)</strong>

   - If H₀ were true, how likely would we see a result this extreme?

7. <strong>Make a decision</strong>

   - If p < .05: Reject H₀ (conclude meditation likely works)
   - If p ≥ .05: Fail to reject H₀ (insufficient evidence)

8. <strong>Interpret in context</strong>
   - Translate statistical decision back into meaningful conclusion

<h3>Real-World Example</h3>

<strong>Scenario:</strong> A school psychologist believes a new reading program improves comprehension.

<strong>What We Know:</strong>

<ul>
<li>National average reading score: μ = 100, σ = 15</li>
<li>Our sample of 25 students using the new program: M = 107</li>
</ul>

<strong>The Question:</strong> Is 107 significantly higher than 100, or could this difference be just random sampling variation?

<strong>Hypothesis Testing Answers This:</strong>

1. H₀: The program doesn't work (students are just a random sample from the population where μ = 100)
2. H₁: The program does work (students come from a different population where μ > 100)
3. Calculate: How unlikely is it to get M = 107 from a population where μ = 100?
4. Result: If probability is < 5%, we conclude the program likely works

<strong>Why This Matters:</strong> Without hypothesis testing, we couldn't distinguish:

<ul>
<li>Real improvements from natural variation</li>
<li>Effective treatments from placebos</li>
<li>Meaningful differences from random noise</li>
</ul>

<h3>Common Misconceptions</h3>

❌ <strong>Misconception:</strong> "If p < .05, we've proven our theory is true"
✓ <strong>Reality:</strong> We've only shown the null hypothesis is unlikely. Our theory is supported, not proven.

❌ <strong>Misconception:</strong> "If p > .05, we've proven there's no effect"
✓ <strong>Reality:</strong> We failed to find evidence of an effect. Maybe it doesn't exist, or maybe our sample was too small to detect it.

❌ <strong>Misconception:</strong> "p-value tells us the probability our hypothesis is true"
✓ <strong>Reality:</strong> p-value tells us the probability of getting our data IF the null hypothesis is true.

<strong>Think About It:</strong> Why is the distinction between "failing to find evidence" and "finding evidence of no effect" important? (Hint: absence of evidence is not evidence of absence!)

---

<h2>Part 2: Formulating Hypotheses</h2>

Every hypothesis test requires two competing hypotheses: the null (H₀) and the alternative (H₁ or Hₐ).

<h3>The Null Hypothesis (H₀)</h3>

<strong>Definition:</strong> A statement of "no effect," "no difference," or "no relationship." It represents the status quo or what we'd expect if nothing special is happening.

<strong>Key Characteristics:</strong>

- Always includes an equals sign (=, ≤, or ≥)
- Represents the assumption we're trying to disprove
- The hypothesis we "presume true" until proven otherwise

<strong>Examples:</strong>

| Research Context                | Null Hypothesis                                                     |
| :------------------------------ | :------------------------------------------------------------------ |
| New drug for headaches          | H₀: The drug has no effect on headache duration (μ = 24 hours)      |
| Mindfulness training for stress | H₀: Training doesn't reduce stress (μ = 50 on stress scale)         |
| Teaching method comparison      | H₀: The new method produces the same scores as traditional (μ = 75) |
| Gender and salary               | H₀: There is no gender difference in salary (μ_male = μ_female)     |

<h3>The Alternative Hypothesis (H₁ or Hₐ)</h3>

<strong>Definition:</strong> The research hypothesis—what you actually believe or predict. It represents "something special is happening."

<strong>Key Characteristics:</strong>

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

<h3>Directional vs. Non-Directional Hypotheses</h3>

This is one of the most important decisions in hypothesis testing.

<h4>Non-Directional (Two-Tailed) Hypotheses</h4>

**Used when:** You predict a difference or effect but **not which direction**

**Symbols:** H₁: μ ≠ [value]

<strong>Examples:</strong>

- "Does caffeine affect reaction time?" (could make it faster OR slower)
- "Is the average age of psychology majors different from 20?" (could be higher OR lower)
- "Does music affect study performance?" (could help OR hurt)

**Why two-tailed?** You're looking for extreme results in BOTH directions (both tails of the distribution)

<h4>Directional (One-Tailed) Hypotheses</h4>

**Used when:** You predict a **specific direction** of difference or effect

**Symbols:**

- H₁: μ > [value] (predicting an increase)
- H₁: μ < [value] (predicting a decrease)

<strong>Examples:</strong>

- "Does this anti-anxiety medication reduce anxiety?" (specifically predicts decrease)
- "Are basketball players taller than average?" (specifically predicts increase)
- "Does sleep deprivation impair performance?" (specifically predicts impairment, not improvement)

**Why one-tailed?** You're only looking for extreme results in ONE direction (one tail of the distribution)

<h3>How to Choose: Decision Tree</h3>

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

> **⚠️ CRITICAL WARNING:** You MUST decide whether to use a one-tailed or two-tailed test BEFORE collecting or looking at your data. Switching from two-tailed to one-tailed after seeing your results is called **p-hacking** and invalidates your statistical inference. This inflates your Type I error rate and is considered research misconduct.

<h3>Practice: Writing Hypotheses</h3>

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

<h3>Common Mistakes in Hypothesis Formulation</h3>

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

<strong>Key Concept:</strong> The null hypothesis always represents the "boring" or "no effect" outcome. The alternative represents the "interesting" or "something is happening" outcome.

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Selecting the Appropriate Test</h4>

  <div class="quiz-question">
    <p><strong>Question 1:</strong> Of all the online courses offered through the New College, the average rating on instructor presence is 0.8 (4 on a scale of 5). You want to compare your own sample of ratings to this college average to see if you deviate from it. Which test should you use?</p>
    <div class="options">
      <p>A) Independent-samples t-test</p>
      <p>B) Z-test</p>
      <p>C) One-sample t-test</p>
      <p>D) Paired-samples t-test</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> C) One-sample t-test</p>

      <p class="explanation"><strong>Why this is correct:</strong> You're comparing a sample mean (your ratings) to a known population value (college average of 0.8). This is exactly what the one-sample t-test is designed for.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Independent-samples t-test:</strong> This compares two different groups, but you only have one group (your ratings) and want to compare it to a population value.</li>
        <li><strong>B) Z-test:</strong> While similar to one-sample t-test, z-tests require knowing the population standard deviation, which you don't have here.</li>
        <li><strong>D) Paired-samples t-test:</strong> This compares the same people measured twice, but you're comparing one group to a population average.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 1: Introduction to One-Sample t-Tests for when to use this test.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 2:</strong> In order to run a one-sample t-test on a variable in SPSS, it must be coded as a _____ variable.</p>
    <div class="options">
      <p>A) Nominal</p>
      <p>B) Scale</p>
      <p>C) Discrete</p>
      <p>D) Ordinal</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) Scale</p>

      <p class="explanation"><strong>Why this is correct:</strong> One-sample t-tests require continuous data (interval or ratio level) that can be meaningfully averaged. In SPSS, this is coded as "Scale" measure.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Nominal:</strong> Nominal variables are categorical with no order. You can't calculate a meaningful mean of categories.</li>
        <li><strong>C) Discrete:</strong> This isn't a measurement level in SPSS. Discrete variables can still be scale if they represent meaningful numeric values.</li>
        <li><strong>D) Ordinal:</strong> Ordinal variables have order but unequal intervals. While sometimes used, scale variables are preferred for t-tests.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Always check your variable's measurement level in SPSS before running statistical tests. Scale variables are required for most parametric tests.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 3:</strong> A researcher wants to test if the average IQ in their sample differs from the population average of 100. What type of research design is this?</p>
    <div class="options">
      <p>A) Between-subjects design</p>
      <p>B) Within-subjects design</p>
      <p>C) Single-group design</p>
      <p>D) Correlational design</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> C) Single-group design</p>

      <p class="explanation"><strong>Why this is correct:</strong> In a one-sample t-test, you have one group of participants that you're comparing to a known population value. This is a single-group design, not a comparison between groups.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Between-subjects design:</strong> This would compare two different groups of people, but here you only have one group.</li>
        <li><strong>B) Within-subjects design:</strong> This would measure the same people twice, but here you're measuring them once and comparing to a population.</li>
        <li><strong>D) Correlational design:</strong> This would examine relationships between variables, not compare a group to a population value.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 1: Introduction to One-Sample t-Tests for the research design context.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 4:</strong> The numerator (top portion) of the t-test formula contains _____.</p>
    <div class="options">
      <p>A) A difference between means</p>
      <p>B) The degrees of freedom</p>
      <p>C) A difference between variances</p>
      <p>D) The sample mean</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> A) A difference between means</p>

      <p class="explanation"><strong>Why this is correct:</strong> The t-test formula is t = (M - μ) / SE. The numerator is (M - μ), which is the difference between the sample mean (M) and the population mean (μ).</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>B) Degrees of freedom:</strong> Degrees of freedom are used in the calculation but appear in the denominator (SE calculation), not the numerator.</li>
        <li><strong>C) Difference between variances:</strong> T-tests don't directly compare variances in the numerator. The variance affects the standard error calculation.</li>
        <li><strong>D) Sample mean alone:</strong> The numerator needs both the sample mean and population mean to calculate the difference.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 2: The Logic of One-Sample t-Tests for the t-test formula breakdown.</p>
    </div>

  </details>
</div>

            <!-- Bottom Navigation -->
            <div class="tab-navigation bottom-nav">
                <button class="tab-button active" onclick="showTab(1)">
                    <input type="checkbox" id="progress-1-bottom" class="tab-checkbox" onchange="toggleTabComplete(1)">
                    <span class="tab-label">Hypothesis Testing Logic</span>
                </button>
                <button class="tab-button" onclick="showTab(2)">
                    <input type="checkbox" id="progress-2-bottom" class="tab-checkbox" onchange="toggleTabComplete(2)">
                    <span class="tab-label">Decision Making & Errors</span>
                </button>
                <button class="tab-button" onclick="showTab(3)">
                    <input type="checkbox" id="progress-3-bottom" class="tab-checkbox" onchange="toggleTabComplete(3)">
                    <span class="tab-label">Sampling & t-Tests</span>
                </button>
                <button class="tab-button" onclick="showTab(4)">
                    <input type="checkbox" id="progress-4-bottom" class="tab-checkbox" onchange="toggleTabComplete(4)">
                    <span class="tab-label">Effect Size & Power</span>
                </button>
                <button class="tab-button" onclick="showTab(5)">
                    <input type="checkbox" id="progress-5-bottom" class="tab-checkbox" onchange="toggleTabComplete(5)">
                    <span class="tab-label">Application & Summary</span>
                </button>
            </div>
        </div>

        <div id="tab-2" class="tab-panel">

<h2>Part 3: The Decision-Making Framework</h2>

Once we've formulated hypotheses and collected data, we need a systematic way to decide which hypothesis the evidence supports.

<h3>Understanding p-Values</h3>

The **p-value** is the most important concept in hypothesis testing—and also the most misunderstood.

<strong>Definition:</strong> The probability of obtaining a result as extreme as (or more extreme than) the one observed, **assuming the null hypothesis is true**.

**In Plain English:** If there really is no effect (H₀ is true), how surprising would our result be? How often would random chance alone produce data this extreme?

**Example:** You test a memory drug and get p = .03

**This means:** If the drug actually does nothing (H₀ is true), there's only a 3% chance we'd see improvement this large due to random sampling variation alone.

**Interpretation:** That's pretty unlikely! Either:

1. We got really lucky with our random sample (3% chance), OR
2. The drug actually works (H₀ is probably false)

We conclude #2 is more plausible.

> **📊 UNDERSTANDING P-VALUES: The Most Misunderstood Concept**
>
> **What p-values ARE:**
>
> - The probability of getting your data (or more extreme) IF H₀ is true
> - A measure of how surprising your results are under the null hypothesis
> - Conditional on H₀ being true
>
> **What p-values are NOT:**
>
> - ❌ The probability that H₀ is true
> - ❌ The probability that your results are due to chance
> - ❌ The probability that H₁ is true
> - ❌ The probability you made a mistake
>
> **Key Insight:** p-values assume H₀ is true and ask "how weird is our data?" They do NOT tell us the probability that our hypothesis is correct!

<h3>The Alpha Level (α)</h3>

<strong>Definition:</strong> The threshold for deciding if a p-value is "small enough" to reject H₀. The maximum probability of making a Type I error we're willing to accept.

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

<h3>Worked Example: Making a Decision</h3>

<strong>Scenario:</strong> Testing if a new teaching method improves test scores

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

<h3>Statistical Significance vs. Practical Significance</h3>

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

<strong>The Solution:</strong> Always consider BOTH statistical significance (p-value) AND effect size (how big the difference is).

<h3>One-Tailed vs. Two-Tailed: How p-Values Differ</h3>

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

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Understanding p-Values and Statistical Decisions</h4>
  
  <div class="quiz-question">
    <p><strong>Question 1:</strong> What does p = .08 mean in hypothesis testing?</p>
    <div class="options">
      <p>A) There's an 8% chance the null hypothesis is true</p>
      <p>B) There's an 8% chance of getting results this extreme if the null hypothesis is true</p>
      <p>C) There's an 8% chance your alternative hypothesis is correct</p>
      <p>D) The effect size is 0.08</p>
    </div>
  </div>
  
  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) There's an 8% chance of getting results this extreme if the null hypothesis is true</p>
      
      <p class="explanation"><strong>Why this is correct:</strong> The p-value is the probability of obtaining a result as extreme as (or more extreme than) the one observed, assuming the null hypothesis is true. It's NOT the probability that the null hypothesis is true.</p>
      
      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) 8% chance null is true:</strong> This is a common misconception! The p-value doesn't tell us the probability that H₀ is true.</li>
        <li><strong>C) 8% chance alternative is correct:</strong> The p-value doesn't directly tell us about the probability of H₁ being true either.</li>
        <li><strong>D) Effect size is 0.08:</strong> The p-value and effect size are completely different concepts. Effect size measures how big the difference is.</li>
      </ul>
      
      <p class="review-tip"><em>💭 Need to review?</em> See Part 3: The Decision-Making Framework for the definition of p-values.</p>
    </div>
  </details>
  
  <div class="quiz-question">
    <p><strong>Question 2:</strong> If p = .08 and α = .05, what decision should you make?</p>
    <div class="options">
      <p>A) Reject the null hypothesis</p>
      <p>B) Fail to reject the null hypothesis</p>
      <p>C) Accept the null hypothesis</p>
      <p>D) The result is inconclusive</p>
    </div>
  </div>
  
  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) Fail to reject the null hypothesis</p>
      
      <p class="explanation"><strong>Why this is correct:</strong> Since p (.08) ≥ α (.05), the result is not statistically significant. We fail to reject the null hypothesis because we don't have sufficient evidence against it.</p>
      
      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Reject H₀:</strong> You only reject H₀ when p < α. Since .08 > .05, you don't have strong enough evidence.</li>
        <li><strong>C) Accept H₀:</strong> We never "accept" the null hypothesis. We either reject it or fail to reject it. Failing to reject doesn't mean H₀ is true.</li>
        <li><strong>D) Inconclusive:</strong> The result is conclusive—it's not statistically significant. We just can't conclude there's an effect.</li>
      </ul>
      
      <p class="application-tip"><em>🌟 Real-world tip:</em> p = .08 is close to .05, so you might want to mention this in your discussion. "While not statistically significant (p = .08), the result approaches significance and warrants further investigation with a larger sample."</p>
    </div>
  </details>
  
  <div class="quiz-question">
    <p><strong>Question 3:</strong> Can a result be statistically significant but practically unimportant?</p>
    <div class="options">
      <p>A) No, statistical significance always means practical importance</p>
      <p>B) Yes, large samples can detect tiny, meaningless differences</p>
      <p>C) No, if it's significant, it must be important</p>
      <p>D) It depends on the research field</p>
    </div>
  </div>
  
  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) Yes, large samples can detect tiny, meaningless differences</p>
      
      <p class="explanation"><strong>Why this is correct:</strong> Statistical significance (p < .05) only tells you that the result is unlikely due to chance. It doesn't tell you how big or important the effect is. With very large samples, even tiny differences become statistically significant.</p>
      
      <p class="explanation"><strong>Example:</strong> A new diet pill might help people lose 0.1 pounds more than a placebo. With 10,000 participants, this tiny difference could be statistically significant (p < .001), but who cares about 0.1 pounds?</p>
      
      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Always means importance:</strong> Statistical significance and practical significance are different concepts.</li>
        <li><strong>C) Must be important:</strong> Significance ≠ importance. You need to look at effect size to judge importance.</li>
        <li><strong>D) Depends on field:</strong> While interpretation varies by field, the principle that significance ≠ importance is universal.</li>
      </ul>
      
      <p class="application-tip"><em>🌟 Key insight:</em> Always report both statistical significance (p-value) AND effect size (Cohen's d) to give readers the complete picture!</p>
    </div>
  </details>
  
  <div class="quiz-question">
    <p><strong>Question 4:</strong> If SPSS reports p = .06 for a two-tailed test, what would the one-tailed p be (if the result is in the predicted direction)?</p>
    <div class="options">
      <p>A) .06</p>
      <p>B) .03</p>
      <p>C) .12</p>
      <p>D) It depends on the sample size</p>
    </div>
  </div>
  
  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) .03</p>
      
      <p class="explanation"><strong>Why this is correct:</strong> For one-tailed tests, you divide the two-tailed p-value by 2 (if the result is in the predicted direction). .06 ÷ 2 = .03.</p>
      
      <p class="explanation"><strong>Why this works:</strong> In a two-tailed test, alpha is split between both tails (.025 in each tail for α = .05). In a one-tailed test, all alpha goes in one tail (.05 in the predicted direction). So the one-tailed p-value is half the two-tailed p-value.</p>
      
      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) .06:</strong> This would be the two-tailed p-value, not the one-tailed.</li>
        <li><strong>C) .12:</strong> This would be doubling the p-value, which doesn't make sense.</li>
        <li><strong>D) Depends on sample size:</strong> The conversion from two-tailed to one-tailed p is always divide by 2, regardless of sample size.</li>
      </ul>
      
      <p class="review-tip"><em>💭 Important reminder:</em> You must decide one-tailed vs. two-tailed BEFORE seeing your data. Converting after seeing results is p-hacking!</p>
    </div>
  </details>
</div>

---

<h2>Part 4: Understanding Errors in Hypothesis Testing</h2>

Because hypothesis testing is based on probability, not certainty, we can make mistakes. Understanding these errors is crucial for interpreting research.

<h3>The Two Types of Errors</h3>

Every hypothesis test can result in four possible outcomes:

|                                                               | **Reality: H₀ is TRUE** (No real effect)                       | **Reality: H₀ is FALSE** (Real effect exists)                  |
| :------------------------------------------------------------ | :------------------------------------------------------------- | :------------------------------------------------------------- |
| **Decision: Reject H₀** (Claim effect exists)                 | **TYPE I ERROR** ❌<br>False Positive<br>Probability = α       | **CORRECT DECISION** ✓<br>True Positive<br>Probability = Power |
| **Decision: Fail to reject H₀** (Claim no evidence of effect) | **CORRECT DECISION** ✓<br>True Negative<br>Probability = 1 - α | **TYPE II ERROR** ❌<br>False Negative<br>Probability = β      |

<h3>Type I Error (False Positive)</h3>

<strong>Definition:</strong> Rejecting H₀ when it's actually true. Concluding there's an effect when there isn't one.

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

<h3>Type II Error (False Negative)</h3>

<strong>Definition:</strong> Failing to reject H₀ when it's actually false. Missing a real effect.

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

<h3>Balancing the Two Errors</h3>

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

> **📋 ERROR TYPES SUMMARY**
>
> | Aspect               | Type I Error (α)           | Type II Error (β)                       |
> | -------------------- | -------------------------- | --------------------------------------- |
> | **What happens**     | Reject true H₀             | Fail to reject false H₀                 |
> | **In plain English** | False positive             | False negative                          |
> | **Analogy**          | Convict innocent person    | Let guilty person go free               |
> | **Probability**      | α (usually .05 = 5%)       | β (varies, often 20-50%)                |
> | **To reduce**        | Lower α, replicate studies | Increase n, increase power              |
> | **Controlled by**    | Researcher (set α)         | Study design (sample size, effect size) |
>
> **Key Trade-off:** ↓ Type I → ↑ Type II (and vice versa)
> **Solution:** Increase sample size (reduces Type II without affecting Type I)

<h3>Which Error is Worse?</h3>

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

<h3>Mnemonics for Remembering</h3>

**Type I Error:**

- "Type I, α (first letter of alphabet), reject when shouldn't"
- Think: "I wrongly claimed I found something" (I = Type I)

**Type II Error:**

- "Type II, β (second letter of Greek alphabet), fail to reject when should"
- Think: "Two blind to see the real effect" (Two = Type II)

**Or use the pregnancy test analogy:**

- Type I: Test says pregnant when not (false positive)
- Type II: Test says not pregnant when actually pregnant (false negative)

<h3>Real-World Example</h3>

**Clinical Trial for Depression Medication:**

**Sample:** 50 patients with depression
**Result:** Average improvement of 5 points on depression scale
**Statistical test:** p = .08

<strong>Decision:</strong> Fail to reject H₀ (p > .05)
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

<h3>Quick Check</h3>

1. What type of error do you make if you reject H₀ but it's actually true?
2. How does increasing sample size affect Type II error?
3. If α = .05, how often will we make Type I errors in the long run?
4. Which error is committed more often: Type I or Type II?

<details>
<summary>Click to see answers</summary>

1.  Type I error (false positive)
2.  Decreases Type II error (increases power to detect real effects)
3.  5% of the time (when H₀ is true, we'll wrongly reject it 5% of the time)
4.  Trick question! Type I rate is fixed at α. Type II rate (β) varies. Generally, Type II errors are more common because most studies are underpowered.
    </details>

                <!-- Bottom Navigation -->
                <div class="tab-navigation bottom-nav">
                    <button class="tab-button" onclick="showTab(1)">
                        <input type="checkbox" id="progress-1-bottom" class="tab-checkbox" onchange="toggleTabComplete(1)">
                        <span class="tab-label">Hypothesis Testing Logic</span>
                    </button>
                    <button class="tab-button active" onclick="showTab(2)">
                        <input type="checkbox" id="progress-2-bottom" class="tab-checkbox" onchange="toggleTabComplete(2)">
                        <span class="tab-label">Decision Making & Errors</span>
                    </button>
                    <button class="tab-button" onclick="showTab(3)">
                        <input type="checkbox" id="progress-3-bottom" class="tab-checkbox" onchange="toggleTabComplete(3)">
                        <span class="tab-label">Sampling & t-Tests</span>
                    </button>
                    <button class="tab-button" onclick="showTab(4)">
                        <input type="checkbox" id="progress-4-bottom" class="tab-checkbox" onchange="toggleTabComplete(4)">
                        <span class="tab-label">Effect Size & Power</span>
                    </button>
                    <button class="tab-button" onclick="showTab(5)">
                        <input type="checkbox" id="progress-5-bottom" class="tab-checkbox" onchange="toggleTabComplete(5)">
                        <span class="tab-label">Application & Summary</span>
                    </button>
                </div>
            </div>

            <div id="tab-3" class="tab-panel">

<h2>Part 5: The Central Limit Theorem</h2>

The Central Limit Theorem (CLT) is one of the most important concepts in statistics. It's the "magic" that makes hypothesis testing work.

<h3>The Problem It Solves</h3>

**Challenge:** Many populations in the real world aren't normally distributed.

- Income is right-skewed (few very wealthy people)
- Reaction times are right-skewed (can't be faster than 0, but can be very slow)
- Test scores might be bimodal (two groups with different abilities)

**Issue:** Many statistical tests assume normal distributions. What do we do?

**Solution:** The Central Limit Theorem!

<h3>What the CLT States</h3>

**Formal Statement:** If you take many random samples of size n from ANY population (regardless of the population's shape) and calculate the mean of each sample, the distribution of those sample means will be approximately normal—especially as sample size increases.

**In Plain English:**

1. Take a population (any shape—skewed, uniform, bimodal, whatever)
2. Draw lots of random samples from it (each of size n)
3. Calculate the mean of each sample
4. Plot those sample means
5. **Result:** The distribution of sample means will be bell-shaped (normal)!

**The Bigger the Sample:** The more perfectly normal the distribution of sample means becomes.

<h3>Why This is Magical</h3>

**It means:**

- Even if your population is weirdly shaped...
- You can still use the normal distribution to make inferences...
- Because you're testing a SAMPLE MEAN, not individual scores!

**Practical Implication:** This is why the t-test and other tests work even when populations aren't perfectly normal. We're comparing means, and the distribution of means is (nearly) always normal!

<h3>Visual Example</h3>

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

<h3>Key Properties</h3>

**1. The mean of the sampling distribution equals the population mean**

μ<sub>M</sub> = μ

The average of all possible sample means equals the true population mean.

**2. The standard deviation of the sampling distribution (Standard Error) is smaller than the population SD**

σ<sub>M</sub> = σ / √n

Sample means vary less than individual scores. Larger samples have even less variation.

**3. The shape approaches normal as n increases**

- n ≥ 30: Usually sufficient for good approximation
- n ≥ 100: Very close to perfect normal
- For populations already normal: Works even with small n

<h3>Standard Error: The Variability of Means</h3>

**Standard Deviation (σ or s):** Measures how much individual scores vary around the population/sample mean

**Standard Error (σ_M or SE):** Measures how much sample means vary around the population mean

**Formula:**

SE = s / √n

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

SE = s / √n = 108 / √36 = 108 / 6 = 18 ms

**Step 2: Calculate z-score for the sample mean**

z = (M - μ) / SE = (520 - 500) / 18 = 20 / 18 = 1.11

**Step 3: Interpret**

- Sample mean is 1.11 standard errors above population mean
- Using z-table: About 13% of sample means would be this high or higher
- Not particularly unusual (p = .13 > .05)

**The CLT in Action:** Even though the population is skewed, we could use the normal distribution to evaluate our sample mean because the sampling distribution of means is normal!

<h3>Quick Check</h3>

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

<h2>Part 6: The One-Sample t-Test</h2>

Now we put everything together into our first formal hypothesis test!

> **Before proceeding:** Make sure you understand these prerequisite concepts:
>
> - Hypothesis formulation ([Part 2](#part-2-formulating-hypotheses))
> - p-values and decision-making ([Part 3](#part-3-the-decision-making-framework))
> - Type I and Type II errors ([Part 4](#part-4-understanding-errors-in-hypothesis-testing))
> - Central Limit Theorem and standard error ([Part 5](#part-5-the-central-limit-theorem))
>
> The one-sample t-test brings all these concepts together into a single, systematic procedure.

### When to Use a One-Sample t-Test

**Purpose:** Compare a sample mean to a known population mean

**Use when:**

- You have ONE sample
- You know the population mean (μ)
- You want to know if your sample is different from that population
- You DON'T know the population standard deviation (σ)

<strong>Examples:</strong>

- Do students at your university sleep less than the national average of 8 hours?
- Is the average IQ of chess players different from 100?
- Do elderly patients with Alzheimer's score below the normal MMSE score of 25?

### Why "t-Test" and Not "z-Test"?

**If we knew σ (population SD):** We'd use a z-test

z = (M - μ) / (σ / √n)

**But we almost never know σ!**

**Solution:** Use the sample SD (s) to estimate it, giving us the t-test

t = (M - μ) / (s / √n)

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

SE = s / √n

#### Step 5: Calculate t-Statistic

t = (M - μ) / SE = (M - μ) / (s / √n)

**Interpretation:** How many standard errors is your sample mean from the population mean?

#### Step 6: Determine Degrees of Freedom and Find p-Value

**Degrees of freedom:** df = n - 1

**Then:**

- Use t-table to find critical value (manual method), OR
- Use SPSS to get exact p-value (easier!)

#### Step 7: Make Decision and State Conclusion

<strong>Decision:</strong>

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

SE = s / √n = 12 / √25 = 12 / 5 = 2.4

**Step 5: Calculate t**

t = (M - μ) / SE = (45 - 50) / 2.4 = -5 / 2.4 = -2.08

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

**What This Means in Practice:**

**Effect Size:** Let's calculate Cohen's d to understand practical significance:

d = (M - μ) / s = (45 - 50) / 12 = -5 / 12 = -0.42

This is a **small to medium effect** (between 0.2 and 0.5), meaning:

- The difference is not just statistically significant, but also practically meaningful
- Meditators score about 0.4 standard deviations lower on stress than the general population
- This represents a noticeable improvement in real-world terms

**Practical Interpretation:**

- **For researchers:** This provides evidence that meditation programs may be worth investigating further
- **For practitioners:** A 5-point reduction in stress (on this scale) could represent meaningful relief for clients
- **For policymakers:** This effect size suggests meditation could be a cost-effective stress management intervention
- **Limitations:** This is correlational (people who meditate may differ in other ways); a randomized experiment would provide stronger evidence

**Next Steps:**

- Replicate with larger sample (n = 25 is modest)
- Use random assignment (assign people to meditate vs. control)
- Follow up over time to see if effects persist
- Calculate confidence intervals to understand range of plausible effects

### Manual Calculation Practice

<strong>Scenario:</strong> National average depression score is μ = 30. A sample of 16 therapy patients has M = 25, s = 8. Test if therapy patients score differently from the national average.

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

> **🧮 CALCULATION CHECKLIST: Avoid These Common Errors**
>
> Before finalizing your t-test calculations, verify:
>
> ✓ **Standard Error vs. Standard Deviation**
>
> - Did you use SE = s/√n (NOT just s)?
> - SE should always be smaller than s
>
> ✓ **Degrees of Freedom**
>
> - Did you use df = n - 1 (NOT n)?
> - Example: If n = 25, then df = 24
>
> ✓ **Sign of t-Value**
>
> - Keep the negative sign if M < μ
> - The sign indicates direction
>
> ✓ **Formula Check**
>
> - t = (M - μ) / SE
> - NOT t = (μ - M) / SE (order matters!)
>
> ✓ **One-Tailed p-Value**
>
> - Did you divide SPSS p by 2?
> - Only if result is in predicted direction!

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

            <!-- Bottom Navigation -->
            <div class="tab-navigation bottom-nav">
                <button class="tab-button" onclick="showTab(1)">
                    <input type="checkbox" id="progress-1-bottom" class="tab-checkbox" onchange="toggleTabComplete(1)">
                    <span class="tab-label">Hypothesis Testing Logic</span>
                </button>
                <button class="tab-button" onclick="showTab(2)">
                    <input type="checkbox" id="progress-2-bottom" class="tab-checkbox" onchange="toggleTabComplete(2)">
                    <span class="tab-label">Decision Making & Errors</span>
                </button>
                <button class="tab-button active" onclick="showTab(3)">
                    <input type="checkbox" id="progress-3-bottom" class="tab-checkbox" onchange="toggleTabComplete(3)">
                    <span class="tab-label">Sampling & t-Tests</span>
                </button>
                <button class="tab-button" onclick="showTab(4)">
                    <input type="checkbox" id="progress-4-bottom" class="tab-checkbox" onchange="toggleTabComplete(4)">
                    <span class="tab-label">Effect Size & Power</span>
                </button>
                <button class="tab-button" onclick="showTab(5)">
                    <input type="checkbox" id="progress-5-bottom" class="tab-checkbox" onchange="toggleTabComplete(5)">
                    <span class="tab-label">Application & Summary</span>
                </button>
            </div>
        </div>

        <div id="tab-4" class="tab-panel">

<h2>Part 7: Effect Size: Measuring Practical Significance</h2>

<p>Statistical significance tells you IF there's an effect. Effect size tells you HOW BIG the effect is.</p>

<blockquote>
<p><strong>Connection to previous concepts:</strong> Remember the distinction between statistical and practical significance from <a href="#part-3-the-decision-making-framework">Part 3</a>? Effect size is how we measure practical significance. A result can be statistically significant (p < .05) but have a tiny effect size, or have a large effect size but not be statistically significant (underpowered study).</p>
</blockquote>

<h3>Why Effect Size Matters</h3>

<p><strong>The Problem with p-Values Alone:</strong></p>

<p><strong>Example 1:</strong> Tiny, trivial difference</p>

<ul>
<li>New diet: Participants lose M = 0.1 pounds more than control</li>
<li>Sample size: n = 10,000</li>
<li>Result: p = .001 (highly significant!)</li>
<li><strong>But:</strong> Who cares about 0.1 pounds? Practically meaningless.</li>
</ul>

<p><strong>Example 2:</strong> Large, important difference</p>

<ul>
<li>New therapy: Participants improve M = 15 points on depression scale</li>
<li>Sample size: n = 12</li>
<li>Result: p = .08 (not significant)</li>
<li><strong>But:</strong> 15 points is a huge improvement! Likely very important.</li>
</ul>

<p><strong>Key Insight:</strong> With large samples, even tiny differences become "significant." With small samples, even large differences might not reach "significance."</p>

<p><strong>Solution:</strong> ALWAYS report effect size alongside p-values.</p>

<h3>Cohen's d: The Most Common Effect Size</h3>

<p><strong>Definition:</strong> Cohen's d measures the standardized difference between a sample mean and population mean (or between two means).</p>

<p><strong>For One-Sample t-Test:</strong></p>

<p>d = (M - μ) / s</p>

<p>Where:</p>

<ul>
<li>M = sample mean</li>
<li>μ = population mean</li>
<li>s = sample standard deviation</li>
</ul>

<p><strong>Interpretation:</strong> How many standard deviations apart are the two means?</p>

<h3>Cohen's Benchmarks</h3>

<p>Jacob Cohen proposed rough guidelines for interpreting d:</p>

<table>
<thead>
<tr>
<th>Cohen's d</th>
<th>Interpretation</th>
<th>Overlap Between Distributions</th>
</tr>
</thead>
<tbody>
<tr>
<td>d = 0.2</td>
<td><strong>Small</strong> effect</td>
<td>85% overlap</td>
</tr>
<tr>
<td>d = 0.5</td>
<td><strong>Medium</strong> effect</td>
<td>67% overlap</td>
</tr>
<tr>
<td>d = 0.8</td>
<td><strong>Large</strong> effect</td>
<td>53% overlap</td>
</tr>
</tbody>
</table>

<p><strong>Important Caveats:</strong></p>

<ul>
<li>These are just guidelines, not rigid rules</li>
<li>What's "large" in one field might be "small" in another</li>
<li>Consider practical/clinical significance in your specific context</li>
</ul>

<h3>Calculating Cohen's d: Examples</h3>

<p><strong>Example 1:</strong> Meditation and stress</p>

<ul>
<li>Population mean: μ = 50</li>
<li>Sample: M = 45, s = 12</li>
<li>d = (45 - 50) / 12 = -5 / 12 = -0.42</li>
<li><strong>Interpretation:</strong> Small to medium effect (stress is 0.42 SD below population mean)</li>
</ul>

<p><strong>Example 2:</strong> Reading program effectiveness</p>

<ul>
<li>Population mean: μ = 100</li>
<li>Sample: M = 112, s = 15</li>
<li>d = (112 - 100) / 15 = 12 / 15 = 0.80</li>
<li><strong>Interpretation:</strong> Large effect (reading scores are 0.80 SD above population mean)</li>
</ul>

<p><strong>What This Means in Practice:</strong></p>

<ul>
<li>This is a <strong>substantial improvement</strong> - students improved by 12 points on average</li>
<li>A Cohen's d of 0.80 is considered educationally significant</li>
<li>In practical terms: If the program works, it could move an average student from the 50th percentile to approximately the 79th percentile</li>
<li><strong>Cost-benefit consideration:</strong> If the program is affordable and scalable, this effect size would strongly support implementation</li>
<li><strong>Caution:</strong> Need to verify with randomized controlled trial to rule out selection effects (maybe better students chose the program)</li>
</ul>

<p><strong>Example 3:</strong> Memory drug trial</p>

<ul>
<li>Population mean: μ = 50</li>
<li>Sample: M = 52, s = 10</li>
<li>d = (52 - 50) / 10 = 2 / 10 = 0.20</li>
<li><strong>Interpretation:</strong> Small effect (memory is 0.20 SD above population mean)</li>
</ul>

<h3>Interpreting Effect Sizes in Context</h3>

<p><strong>Don't just rely on Cohen's benchmarks!</strong> Consider:</p>

<p><strong>1. Field-Specific Norms</strong></p>

<ul>
<li>In physics: d = 0.2 might be considered large</li>
<li>In psychology/education: d = 0.2 is genuinely small</li>
</ul>

<p><strong>2. Clinical/Practical Importance</strong></p>

<ul>
<li>d = 0.3 for a simple, cheap intervention might be very valuable</li>
<li>d = 0.3 for an expensive, risky treatment might not be worthwhile</li>
</ul>

<p><strong>3. Costs and Benefits</strong></p>

<ul>
<li>Small effects can matter if intervention is inexpensive or harm-free</li>
<li>Large effects are needed if intervention is costly or has risks</li>
</ul>

<p><strong>4. Comparison to Existing Alternatives</strong></p>

<ul>
<li>d = 0.4 is impressive if current best treatment has d = 0.2</li>
<li>d = 0.4 is unimpressive if current treatment already achieves d = 0.8</li>
</ul>

<h3>Effect Size vs. Statistical Significance: Four Scenarios</h3>

<p><strong>Scenario A: Large effect, significant (ideal!)</strong></p>

<ul>
<li>d = 0.9, p = .001, n = 50</li>
<li><strong>Interpretation:</strong> Strong evidence of a substantial effect</li>
<li><strong>Action:</strong> Strong support for the intervention/theory</li>
</ul>

<p><strong>Scenario B: Small effect, significant (common with large samples)</strong></p>

<ul>
<li>d = 0.1, p = .02, n = 1000</li>
<li><strong>Interpretation:</strong> Statistically reliable but tiny effect</li>
<li><strong>Action:</strong> Consider practical value before implementing</li>
</ul>

<p><strong>Scenario C: Large effect, not significant (underpowered study)</strong></p>

<ul>
<li>d = 0.9, p = .09, n = 10</li>
<li><strong>Interpretation:</strong> Possibly important effect, but insufficient evidence</li>
<li><strong>Action:</strong> Replicate with larger sample</li>
</ul>

<p><strong>Scenario D: Small effect, not significant</strong></p>

<ul>
<li>d = 0.1, p = .45, n = 30</li>
<li><strong>Interpretation:</strong> Little evidence of an effect</li>
<li><strong>Action:</strong> Likely not worthwhile to pursue</li>
</ul>

<p><strong>The Complete Picture:</strong> Always report BOTH p-value AND effect size. They tell different parts of the story.</p>

<h3>Reporting Effect Size in APA Format</h3>

<p><strong>Include d in your results statement:</strong></p>

<p><strong>Format:</strong><br>
"[Group description], M = [mean], SD = [standard deviation], [comparison description], t([df]) = [t-value], p = [p-value], d = [Cohen's d]."</p>

<p><strong>Examples:</strong></p>

<p><strong>Example 1:</strong><br>
"Participants who meditated regularly (M = 45, SD = 12) reported significantly lower stress than the general population mean of 50, t(24) = -2.08, p = .012, d = 0.42."</p>

<p><strong>Example 2:</strong><br>
"Students using the new reading program (M = 112, SD = 15) scored significantly higher than the national average of 100, t(29) = 4.38, p < .001, d = 0.80."</p>

<p><strong>Example 3:</strong><br>
"Patients receiving the experimental memory drug (M = 52, SD = 10) did not differ significantly from the population mean of 50, t(19) = 0.89, p = .38, d = 0.20."</p>

<p><strong>Note:</strong> Report d even when results are not significant! Effect size estimates are valuable regardless.</p>

<h3>Complete APA Reporting Guidelines</h3>

<p><strong>Essential Components to Include:</strong></p>

<ol>
<li><strong>Descriptive statistics:</strong> M and SD for your sample</li>
<li><strong>Comparison value:</strong> The population mean you're comparing against</li>
<li><strong>Test statistic:</strong> t(df) = value</li>
<li><strong>p-value:</strong> Exact value when possible, or p < .001 for very small values</li>
<li><strong>Effect size:</strong> Cohen's d</li>
<li><strong>Direction and significance:</strong> Clearly state whether the difference was significant and in which direction</li>
</ol>

<p><strong>Reporting p-Values:</strong></p>

<table>
<thead>
<tr>
<th>SPSS Output</th>
<th>How to Report</th>
<th>Why</th>
</tr>
</thead>
<tbody>
<tr>
<td>p = .000</td>
<td><strong>p < .001</strong></td>
<td>Never report p = .000; it's rounded</td>
</tr>
<tr>
<td>p = .0234</td>
<td><strong>p = .023</strong></td>
<td>Round to 2-3 decimal places</td>
</tr>
<tr>
<td>p = .050</td>
<td><strong>p = .050</strong></td>
<td>Report exactly (borderline case)</td>
</tr>
<tr>
<td>p = .0499</td>
<td><strong>p = .050</strong></td>
<td>Round to 3 decimals, or report exactly</td>
</tr>
<tr>
<td>p = .347</td>
<td><strong>p = .347</strong> or <strong>p = .35</strong></td>
<td>Either is acceptable</td>
</tr>
</tbody>
</table>

<p><strong>Common Reporting Mistakes to Avoid:</strong></p>

<p>❌ <strong>Wrong:</strong> "The result was p = .000"<br>
✓ <strong>Right:</strong> "The result was p < .001"</p>

<p>❌ <strong>Wrong:</strong> "t = 2.45 with p < .05"<br>
✓ <strong>Right:</strong> "t(23) = 2.45, p = .023" (report exact p when available)</p>

<p>❌ <strong>Wrong:</strong> "The difference was not significant (p = .08)"<br>
✓ <strong>Right:</strong> "The difference was not significant, t(45) = 1.78, p = .08, d = 0.26"</p>

<p>❌ <strong>Wrong:</strong> "Participants scored M = 85"<br>
✓ <strong>Right:</strong> "Participants (M = 85, SD = 12) scored..."</p>

<p>❌ <strong>Wrong:</strong> "Results were significant at the .05 level"<br>
✓ <strong>Right:</strong> "Results were significant, t(30) = 2.34, p = .026"</p>

<h3>APA Format for Different Scenarios</h3>

<p><strong>Scenario 1: Significant Result (Two-Tailed)</strong><br>
"College students (M = 6.2, SD = 1.3) slept significantly less than the recommended 8 hours, t(149) = -8.52, p < .001, d = 1.38, suggesting substantial sleep deprivation in this population."</p>

<p><strong>Scenario 2: Non-Significant Result (Two-Tailed)</strong><br>
"Participants receiving the new study technique (M = 78.5, SD = 11.2) did not differ significantly from the national average of 75, t(32) = 1.79, p = .082, d = 0.31, though the medium effect size suggests the study may have been underpowered."</p>

<p><strong>Scenario 3: Significant Result (One-Tailed)</strong><br>
"As predicted, athletes who underwent visualization training (M = 142.3, SD = 18.7) performed significantly better than the population mean of 130, t(27) = 3.48, p = .001 (one-tailed), d = 0.66."</p>

<p><strong>Scenario 4: Reporting with Context</strong><br>
"Participants in the mindfulness intervention group (M = 42.1, SD = 9.3) showed significantly lower anxiety scores compared to the clinical cutoff of 50, t(38) = -5.30, p < .001, d = 0.85. This large effect suggests the intervention moved participants from clinically significant anxiety to subclinical levels."</p>

<p><strong>Best Practices:</strong></p>

<ul>
<li><strong>Always include SD:</strong> Readers need it to understand variability and calculate effect sizes</li>
<li><strong>Report exact p-values:</strong> Don't just say "p < .05" when you have the exact value</li>
<li><strong>Include effect size:</strong> Required by most journals and essential for meta-analyses</li>
<li><strong>Interpret in context:</strong> Don't just report numbers; explain what they mean</li>
<li><strong>Be honest about limitations:</strong> Mention if sample was small, not randomized, etc.</li>
</ul>

<h3>Quick Check</h3>

<ol>
<li>Why is effect size important beyond just p-values?</li>
<li>Calculate Cohen's d: M = 85, μ = 75, s = 20</li>
<li>Is d = 0.3 always a "small" effect?</li>
<li>Can you have a significant result with a small effect size?</li>
</ol>

<details>
<summary>Click to see answers</summary>

<ol>
<li>p-value tells IF there's an effect; d tells HOW BIG it is. Large samples can make trivial differences significant.</li>
<li>d = (85-75)/20 = 10/20 = 0.5 (medium effect)</li>
<li>No! Context matters. It might be large in physics, meaningful for a cheap intervention, or insufficient for a risky treatment.</li>
<li>Yes! With very large samples, even d = 0.1 can be p < .05 (statistically significant but practically small)</li>
</ol>
</details>

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Effect Size - Cohen's d</h4>

  <div class="quiz-question">
    <p><strong>Question 1:</strong> Cohen's d is a measure of _____.</p>
    <div class="options">
      <p>A) Statistical significance</p>
      <p>B) Effect size</p>
      <p>C) Confidence interval</p>
      <p>D) Power</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) Effect size</p>

      <p class="explanation"><strong>Why this is correct:</strong> Cohen's d specifically measures the magnitude or size of an effect, standardized in terms of standard deviation units. It tells us how large a difference is, regardless of sample size.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Statistical significance:</strong> This is measured by p-values, not Cohen's d. You can have large effects that aren't significant (small samples) or small effects that are significant (large samples).</li>
        <li><strong>C) Confidence interval:</strong> This provides a range of plausible values for a parameter, not the size of an effect.</li>
        <li><strong>D) Power:</strong> This is the probability of detecting an effect when it exists, which is related to but different from effect size.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 7: Effect Size - Measuring Practical Significance for the definition and purpose of Cohen's d.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 2:</strong> Effect size in a t-test assesses the degree to which _____.</p>
    <div class="options">
      <p>A) Two populations are separated</p>
      <p>B) Two populations overlap</p>
      <p>C) Two samples are separated</p>
      <p>D) Two samples overlap</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> A) Two populations are separated</p>

      <p class="explanation"><strong>Why this is correct:</strong> Effect size measures how much the populations differ from each other. A larger effect size means the populations are more separated (less overlap), while a smaller effect size means they overlap more.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>B) Two populations overlap:</strong> This is the opposite. Large effect sizes mean LESS overlap between populations.</li>
        <li><strong>C) Two samples are separated:</strong> Effect size is about populations, not samples. We use samples to estimate population effect sizes.</li>
        <li><strong>D) Two samples overlap:</strong> Again, effect size is about populations, and large effects mean less overlap, not more.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Think of effect size as measuring how "different" the populations are. Large effect = very different populations, small effect = similar populations.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 3:</strong> Imagine the average time to complete a 4-year bachelor degree is actually 4.7 years, based on national data. You collect data on 68 psychology students, finding an average completion time of 4.3 years with a standard deviation of 0.6 years. What would be the effect size for a single-sample t-test?</p>
    <div class="options">
      <p>A) -5.50</p>
      <p>B) -0.67</p>
      <p>C) 0.20</p>
      <p>D) 0.82</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) -0.67</p>

      <p class="explanation"><strong>Why this is correct:</strong> Cohen's d = (M - μ) / s = (4.3 - 4.7) / 0.6 = -0.4 / 0.6 = -0.67. The negative sign indicates the sample mean is below the population mean.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) -5.50:</strong> This would result from using the wrong formula or calculation error. The difference (-0.4) divided by standard deviation (0.6) cannot equal -5.50.</li>
        <li><strong>C) 0.20:</strong> This might be the result of using the wrong population mean or calculation error.</li>
        <li><strong>D) 0.82:</strong> This might be using the absolute value or incorrect calculation.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 7.2: Cohen's d - The Most Common Effect Size for the formula and calculation steps.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 4:</strong> When performing a single-sample t-test, an effect size of 0.50 would be interpreted as a _____ effect.</p>
    <div class="options">
      <p>A) Small</p>
      <p>B) Negligible</p>
      <p>C) Medium</p>
      <p>D) Large</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> C) Medium</p>

      <p class="explanation"><strong>Why this is correct:</strong> According to Cohen's (1988) guidelines: d = 0.2 is small, d = 0.5 is medium, and d = 0.8 is large. An effect size of 0.50 falls exactly at the medium benchmark.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Small:</strong> Small effects are around d = 0.2, which is smaller than 0.5.</li>
        <li><strong>B) Negligible:</strong> There's no "negligible" category in Cohen's guidelines. 0.5 is definitely not negligible.</li>
        <li><strong>D) Large:</strong> Large effects are around d = 0.8, which is larger than 0.5.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Remember Cohen's benchmarks: 0.2 (small), 0.5 (medium), 0.8 (large). These are rough guidelines, but useful for initial interpretation.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 5:</strong> What is the key difference between effect size and statistical significance?</p>
    <div class="options">
      <p>A) Effect size depends on sample size; significance doesn't</p>
      <p>B) Statistical significance depends on sample size; effect size doesn't</p>
      <p>C) They measure the same thing in different ways</p>
      <p>D) Effect size is always larger than significance</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) Statistical significance depends on sample size; effect size doesn't</p>

      <p class="explanation"><strong>Why this is correct:</strong> Statistical significance (p-value) is heavily influenced by sample size—larger samples make it easier to achieve significance. Effect size (Cohen's d) measures the magnitude of the difference independent of sample size.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Effect size depends on sample size:</strong> This is backwards. Effect size is calculated from means and standard deviations, not sample size.</li>
        <li><strong>C) Same thing in different ways:</strong> They measure completely different concepts—significance tests whether an effect exists, effect size measures how large it is.</li>
        <li><strong>D) Effect size is always larger:</strong> These are incomparable metrics. Effect size is in standard deviation units, significance is a probability.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 7.4: Effect Size vs. Statistical Significance for the key distinctions between these concepts.</p>
    </div>

  </details>
</div>

---

<h2>Part 8: Statistical Power</h2>

<p>Power is your study's ability to detect a real effect when one exists. Understanding power helps you design better studies and interpret null results.</p>

<blockquote>
<p><strong>Connection to previous concepts:</strong></p>
<ul>
<li>Power is directly related to <strong>Type II errors</strong> from <a href="#part-4-understanding-errors-in-hypothesis-testing">Part 4</a>: Power = 1 - β</li>
<li>Power depends on <strong>effect size</strong> from <a href="#part-7-effect-size-measuring-practical-significance">Part 7</a>: Larger effects are easier to detect</li>
<li>Power is why we care about <strong>sample size</strong>: Bigger samples = more power to detect real effects</li>
</ul>
</blockquote>

<h3>What is Statistical Power?</h3>

<p><strong>Definition:</strong> The probability of correctly rejecting a false null hypothesis (detecting a real effect when it exists).</p>

<p><strong>In the Error Matrix:</strong></p>

<ul>
<li>Power = Probability of True Positive</li>
<li>Power = 1 - β (where β = probability of Type II error)</li>
</ul>

<p><strong>Standard Goal:</strong> Power ≥ .80 (80% chance of detecting a real effect)</p>

<p><strong>What Power Means:</strong></p>

<table>
<thead>
<tr>
<th>Power</th>
<th>Interpretation</th>
</tr>
</thead>
<tbody>
<tr>
<td>.50</td>
<td>50% chance of detecting real effect (coin flip—terrible!)</td>
</tr>
<tr>
<td>.80</td>
<td>80% chance of detecting real effect (acceptable)</td>
</tr>
<tr>
<td>.90</td>
<td>90% chance of detecting real effect (good)</td>
</tr>
<tr>
<td>.95</td>
<td>95% chance of detecting real effect (excellent)</td>
</tr>
</tbody>
</table>

<h3>Why Power Matters</h3>

<p><strong>Low Power Studies (e.g., power = .30):</strong></p>

<ul>
<li>Even if effect exists, you'll probably miss it (70% chance of Type II error)</li>
<li>Null results are uninterpretable (effect might exist but study couldn't detect it)</li>
<li>Waste of resources and participants' time</li>
</ul>

<p><strong>High Power Studies (e.g., power = .85):</strong></p>

<ul>
<li>Good chance of detecting real effects</li>
<li>Null results are more meaningful (if effect existed, you likely would've found it)</li>
<li>Efficient use of resources</li>
</ul>

<p><strong>Real-World Consequence:</strong> Many published studies are underpowered, leading to:</p>

<ul>
<li>Missed discoveries (Type II errors)</li>
<li>Overestimated effect sizes (only the "lucky" studies reach significance)</li>
<li>Non-replicable findings</li>
</ul>

<h3>Factors Affecting Power</h3>

<p><strong>Four main factors determine power:</strong></p>

<h4>1. Sample Size (n)</h4>

<p><strong>Effect on Power:</strong> ↑ Larger sample = ↑ Higher power</p>

<p><strong>Why:</strong> Larger samples give more precise estimates (smaller SE), making it easier to detect real differences.</p>

<p><strong>Example:</strong> True effect size d = 0.5</p>

<ul>
<li>n = 10: Power = .18 (only 18% chance of detecting it!)</li>
<li>n = 30: Power = .48</li>
<li>n = 64: Power = .80 (acceptable!)</li>
<li>n = 100: Power = .94</li>
</ul>

<p><strong>This is the easiest factor to control!</strong> Want more power? Get more participants.</p>

<h4>2. Effect Size in Population</h4>

<p><strong>Effect on Power:</strong> ↑ Larger effect = ↑ Higher power</p>

<p><strong>Why:</strong> Larger effects are easier to detect.</p>

<p><strong>Example:</strong> With n = 30</p>

<ul>
<li>Small effect (d = 0.2): Power = .11 (very low!)</li>
<li>Medium effect (d = 0.5): Power = .48</li>
<li>Large effect (d = 0.8): Power = .80</li>
</ul>

<p><strong>Implication:</strong> If effects are small, you need larger samples to detect them.</p>

<p><strong>But:</strong> You can't control true effect size! You can only estimate it and plan accordingly.</p>

<h4>3. Alpha Level (α)</h4>

<p><strong>Effect on Power:</strong> ↑ Higher α = ↑ Higher power</p>

<p><strong>Why:</strong> Being less strict (larger α) makes it easier to reject H₀.</p>

<p><strong>Example:</strong> With n = 50, d = 0.5</p>

<ul>
<li>α = .01: Power = .59</li>
<li>α = .05: Power = .80</li>
<li>α = .10: Power = .90</li>
</ul>

<p><strong>Trade-off:</strong> Higher α increases power BUT also increases Type I error rate.</p>

<p><strong>Standard Practice:</strong> Keep α = .05 and adjust sample size instead.</p>

<h4>4. One-Tailed vs. Two-Tailed Test</h4>

<p><strong>Effect on Power:</strong> One-tailed test has higher power (for detecting effects in predicted direction)</p>

<p><strong>Why:</strong> All alpha is concentrated in one tail instead of split between two.</p>

<p><strong>Example:</strong> n = 30, d = 0.5</p>

<ul>
<li>Two-tailed: Power = .48</li>
<li>One-tailed: Power = .61</li>
</ul>

<p><strong>Caution:</strong> Only use one-tailed if you have strong directional prediction and truly don't care about effects in the opposite direction.</p>

<h3>Power Analysis: Before vs. After Study</h3>

<h4>A Priori Power Analysis (BEFORE collecting data)</h4>

<p><strong>Purpose:</strong> Determine required sample size to achieve desired power</p>

<p><strong>Process:</strong></p>

<ol>
<li>Decide desired power (usually .80)</li>
<li>Set alpha level (usually .05)</li>
<li>Estimate expected effect size (from literature or pilot study)</li>
<li>Use power analysis software to calculate required n</li>
</ol>

<p><strong>Example:</strong> Planning a study</p>

<ul>
<li>Expected effect: d = 0.5 (medium)</li>
<li>Desired power: .80</li>
<li>Alpha: .05 (two-tailed)</li>
<li><strong>Result:</strong> Need n ≥ 64</li>
</ul>

<p><strong>This is best practice for study design!</strong></p>

<h4>Post Hoc Power Analysis (AFTER collecting data)</h4>

<p><strong>Purpose:</strong> Understand the power you actually had</p>

<p><strong>Process:</strong></p>

<ol>
<li>Calculate observed effect size from your data</li>
<li>Use your actual sample size</li>
<li>Calculate power you had to detect an effect that size</li>
</ol>

<p><strong>Example:</strong> After a study with null result</p>

<ul>
<li>n = 20</li>
<li>Observed d = 0.3</li>
<li><strong>Retrospective power:</strong> .14 (only 14%!)</li>
<li><strong>Interpretation:</strong> Study was severely underpowered; null result is uninterpretable</li>
</ul>

<p><strong>Controversy:</strong> Some statisticians argue post-hoc power is not useful. But it helps explain why you might have gotten null results.</p>

<h3>Interpreting Null Results Through the Lens of Power</h3>

<p><strong>High-Powered Study with Null Result:</strong></p>

<ul>
<li>n = 100, power was .90 for medium effects</li>
<li>p = .52</li>
<li><strong>Interpretation:</strong> Strong evidence that effect is small or non-existent</li>
<li><strong>Confidence:</strong> Can reasonably conclude no meaningful effect</li>
</ul>

<p><strong>Low-Powered Study with Null Result:</strong></p>

<ul>
<li>n = 15, power was .20 for medium effects</li>
<li>p = .31</li>
<li><strong>Interpretation:</strong> Study couldn't detect an effect even if one exists</li>
<li><strong>Confidence:</strong> Can't conclude anything; study was inadequate</li>
</ul>

<p><strong>The Bottom Line:</strong> Null results from underpowered studies are meaningless!</p>

<h3>Increasing Power: Practical Strategies</h3>

<p><strong>1. Increase Sample Size (Most Important!)</strong></p>

<ul>
<li>Recruit more participants</li>
<li>Even small increases help</li>
<li>Calculate required n before starting</li>
</ul>

<p><strong>2. Use More Reliable Measures</strong></p>

<ul>
<li>Reduces random error (noise)</li>
<li>Makes real effects easier to detect</li>
<li>Use validated, well-tested instruments</li>
</ul>

<p><strong>3. Reduce Variability in Procedures</strong></p>

<ul>
<li>Standardize testing conditions</li>
<li>Train experimenters thoroughly</li>
<li>Control extraneous variables</li>
<li>Less noise = easier to see signal</li>
</ul>

<p><strong>4. Use Within-Subjects Designs (When Possible)</strong></p>

<ul>
<li>More powerful than between-subjects</li>
<li>Reduces individual differences</li>
<li>(Covered more in Module 3)</li>
</ul>

<p><strong>5. Maximize Effect Size</strong></p>

<ul>
<li>Use stronger manipulations/interventions</li>
<li>Ensure treatment fidelity</li>
<li>Select participants likely to show effects</li>
</ul>

<p><strong>What NOT to Do:</strong></p>

<ul>
<li>❌ Don't just increase alpha (increases Type I errors)</li>
<li>❌ Don't use one-tailed tests just for power (unless genuinely appropriate)</li>
<li>❌ Don't run underpowered studies and hope for the best</li>
</ul>

<h3>Power in Research Ethics</h3>

<p><strong>Ethical Issue:</strong> Running underpowered studies is arguably unethical.</p>

<p><strong>Why:</strong></p>

<ul>
<li>Wastes participants' time and trust</li>
<li>Wastes research resources</li>
<li>Unlikely to contribute meaningful knowledge</li>
<li>May lead to false conclusions</li>
</ul>

<p><strong>Best Practice:</strong></p>

<ul>
<li>Always conduct power analysis before data collection</li>
<li>Aim for power ≥ .80</li>
<li>If you can't achieve adequate power, reconsider the study design</li>
</ul>

<h3>Quick Check</h3>

<ol>
<li>What does power = .70 mean?</li>
<li>What's the easiest way to increase statistical power?</li>
<li>Why is a null result from a low-powered study hard to interpret?</li>
<li>If you have power = .80 for d = 0.5, is your power higher or lower for d = 0.8?</li>
</ol>

<details>
<summary>Click to see answers</summary>

<ol>
<li>70% probability of detecting a real effect if one exists (30% chance of Type II error)</li>
<li>Increase sample size</li>
<li>You don't know if there's no effect, or if the effect exists but your study couldn't detect it</li>
<li>Higher! Larger effects are easier to detect, so power would be > .80</li>
</ol>
</details>

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Statistical Power and Errors</h4>

  <div class="quiz-question">
    <p><strong>Question 1:</strong> _____ is the ability to reject the null hypothesis when the null hypothesis is actually false.</p>
    <div class="options">
      <p>A) Statistical power</p>
      <p>B) Effect size</p>
      <p>C) Probability of Type I error</p>
      <p>D) Probability of Type II error</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> A) Statistical power</p>

      <p class="explanation"><strong>Why this is correct:</strong> Statistical power is defined as the probability of correctly rejecting the null hypothesis when it is false (i.e., when there really is an effect). This is what we want our study to do.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>B) Effect size:</strong> This measures how large an effect is, not the probability of detecting it.</li>
        <li><strong>C) Probability of Type I error:</strong> This is the probability of incorrectly rejecting a true null hypothesis (false positive).</li>
        <li><strong>D) Probability of Type II error:</strong> This is the probability of failing to reject a false null hypothesis (false negative), which is the opposite of power.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 8.1: What is Statistical Power for the definition and importance of power.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 2:</strong> The practical use of statistical power is that it informs researchers _____.</p>
    <div class="options">
      <p>A) Whether they will find significant results</p>
      <p>B) What effect size they can expect to find in conducting their study</p>
      <p>C) Whether they will find important results</p>
      <p>D) How many participants are needed to conduct a study with findings they can trust</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> D) How many participants are needed to conduct a study with findings they can trust</p>

      <p class="explanation"><strong>Why this is correct:</strong> Power analysis is primarily used for sample size planning. Before conducting a study, researchers calculate how many participants they need to have adequate power (typically 80%) to detect an effect of a certain size.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Whether they will find significant results:</strong> Power doesn't guarantee significance—it only increases the probability of detecting real effects.</li>
        <li><strong>B) What effect size to expect:</strong> Researchers typically assume an expected effect size when planning power analysis, not the other way around.</li>
        <li><strong>C) Whether they will find important results:</strong> Power relates to detecting effects, not to their importance or practical significance.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Power analysis is most valuable for study planning. Always calculate required sample size before collecting data to ensure your study can detect meaningful effects.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 3:</strong> Alpha level in a hypothesis test refers to _____.</p>
    <div class="options">
      <p>A) Probability of making a Type II error</p>
      <p>B) Probability of making a Type I error</p>
      <p>C) Statistical power</p>
      <p>D) Probability of the null hypothesis being true</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) Probability of making a Type I error</p>

      <p class="explanation"><strong>Why this is correct:</strong> Alpha (α) is the significance level that sets the probability of making a Type I error—incorrectly rejecting a true null hypothesis. It's typically set at 0.05 (5%).</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Probability of Type II error:</strong> This is beta (β), which is related to but different from alpha.</li>
        <li><strong>C) Statistical power:</strong> Power is 1 - β, not alpha. Power is the probability of correctly rejecting a false null hypothesis.</li>
        <li><strong>D) Probability of null being true:</strong> Alpha doesn't tell us about the probability that the null hypothesis is true—it's about our decision criterion.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 8.3: The Relationship Between Power and Error Types for how alpha relates to Type I errors.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 4:</strong> When alpha increases, both _____ and _____ increase.</p>
    <div class="options">
      <p>A) Probability of Type II error; statistical power</p>
      <p>B) Probability of Type I error; probability of Type II error</p>
      <p>C) Statistical power; probability of Type I error</p>
      <p>D) Effect size; statistical power</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> C) Statistical power; probability of Type I error</p>

      <p class="explanation"><strong>Why this is correct:</strong> When alpha increases (e.g., from 0.05 to 0.10), you become more willing to reject the null hypothesis. This increases both Type I error rate (false positives) and statistical power (ability to detect real effects).</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Type II error and power:</strong> These have an inverse relationship—when one increases, the other decreases.</li>
        <li><strong>B) Both error types:</strong> Type I and Type II errors typically have an inverse relationship, not both increasing together.</li>
        <li><strong>D) Effect size and power:</strong> Effect size is independent of alpha—it's a property of the population, not our decision criterion.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> There's always a trade-off between Type I and Type II errors. Lower alpha reduces false positives but increases false negatives (and vice versa).</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 5:</strong> Which statement best describes the relationship between power and Type II error?</p>
    <div class="options">
      <p>A) They are the same thing</p>
      <p>B) Power = 1 - Type II error rate</p>
      <p>C) Power = Type II error rate</p>
      <p>D) There is no relationship between them</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) Power = 1 - Type II error rate</p>

      <p class="explanation"><strong>Why this is correct:</strong> Power and Type II error are complementary probabilities. Type II error is the probability of missing a real effect (β), while power is the probability of detecting a real effect (1 - β).</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Same thing:</strong> They're related but opposite—one is the probability of detecting effects, the other is the probability of missing effects.</li>
        <li><strong>C) Power = Type II error:</strong> This would mean they're equal, but they're complementary (add up to 1).</li>
        <li><strong>D) No relationship:</strong> They're directly related as complementary probabilities that sum to 1.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 8.3: The Relationship Between Power and Error Types for the mathematical relationship between power and Type II errors.</p>
    </div>

  </details>
</div>

            <!-- Bottom Navigation -->
            <div class="tab-navigation bottom-nav">
                <button class="tab-button" onclick="showTab(1)">
                    <input type="checkbox" id="progress-1-bottom" class="tab-checkbox" onchange="toggleTabComplete(1)">
                    <span class="tab-label">Hypothesis Testing Logic</span>
                </button>
                <button class="tab-button" onclick="showTab(2)">
                    <input type="checkbox" id="progress-2-bottom" class="tab-checkbox" onchange="toggleTabComplete(2)">
                    <span class="tab-label">Decision Making & Errors</span>
                </button>
                <button class="tab-button" onclick="showTab(3)">
                    <input type="checkbox" id="progress-3-bottom" class="tab-checkbox" onchange="toggleTabComplete(3)">
                    <span class="tab-label">Sampling & t-Tests</span>
                </button>
                <button class="tab-button active" onclick="showTab(4)">
                    <input type="checkbox" id="progress-4-bottom" class="tab-checkbox" onchange="toggleTabComplete(4)">
                    <span class="tab-label">Effect Size & Power</span>
                </button>
                <button class="tab-button" onclick="showTab(5)">
                    <input type="checkbox" id="progress-5-bottom" class="tab-checkbox" onchange="toggleTabComplete(5)">
                    <span class="tab-label">Application & Summary</span>
                </button>
            </div>
        </div>

        <div id="tab-5" class="tab-panel">

<h2>Part 9: The t-Distribution</h2>

<p>We've been using the t-test, but what exactly is this "t-distribution"?</p>

<h3>Why Not Use the Normal Distribution (z)?</h3>

<p><strong>Remember the z-score formula:</strong></p>

<p>z = (X - μ) / σ</p>

<p><strong>For testing sample means:</strong></p>

<p>z = (M - μ) / (σ / √n)</p>

<p><strong>The problem:</strong> We almost never know σ (population standard deviation)!</p>

<p><strong>Our solution:</strong> Substitute s (sample standard deviation)</p>

<p>t = (M - μ) / (s / √n)</p>

<p><strong>New problem:</strong> Using s instead of σ adds uncertainty. The regular normal distribution doesn't account for this extra uncertainty.</p>

<p><strong>The fix:</strong> Use the t-distribution, which adjusts for this uncertainty!</p>

<h3>Properties of the t-Distribution</h3>

<p><strong>Similarities to Normal Distribution:</strong></p>

<ul>
<li>Symmetrical</li>
<li>Bell-shaped</li>
<li>Centered on zero</li>
<li>Area under curve = 1.0</li>
</ul>

<p><strong>Differences from Normal Distribution:</strong></p>

<ul>
<li><strong>Heavier tails</strong> (more area in the extremes)</li>
<li><strong>Flatter peak</strong> (less area in the center)</li>
<li><strong>Shape depends on degrees of freedom (df)</strong></li>
</ul>

<p><strong>Why Heavier Tails?</strong></p>

<ul>
<li>Reflects the extra uncertainty from estimating σ with s</li>
<li>Means you need a larger t-value (vs. z-value) to reach significance</li>
<li>More conservative than z-test (less likely to make Type I errors)</li>
</ul>

<h3>Degrees of Freedom (df)</h3>

<p><strong>Definition:</strong> The number of values that are "free to vary" when calculating a statistic.</p>

<p><strong>For One-Sample t-Test:</strong></p>

<p>df = n - 1</p>

<p><strong>Why n - 1?</strong></p>

<ul>
<li>Once you know the mean and (n-1) scores, the last score is determined</li>
<li>Example: If M = 10 and you know 4 out of 5 scores are {8, 9, 11, 12}, the 5th MUST be 10 (to make the mean = 10)</li>
</ul>

<p><strong>Effect on t-Distribution:</strong></p>

<table>
<thead>
<tr>
<th>df</th>
<th>Shape of t-Distribution</th>
</tr>
</thead>
<tbody>
<tr>
<td>Small (df = 1-5)</td>
<td>Very heavy tails, very flat</td>
</tr>
<tr>
<td>Medium (df = 10-20)</td>
<td>Moderately heavy tails</td>
</tr>
<tr>
<td>Large (df = 30+)</td>
<td>Very close to normal</td>
</tr>
<tr>
<td>df = ∞</td>
<td>Identical to normal distribution</td>
</tr>
</tbody>
</table>

<p><strong>Practical Implication:</strong> With larger samples (higher df), the t-distribution approaches the normal distribution.</p>

<h3>Critical Values: t vs. z</h3>

<p><strong>Critical values</strong> are the thresholds for significance. Let's compare for α = .05, two-tailed:</p>

<table>
<thead>
<tr>
<th>df</th>
<th>t-critical</th>
<th>z-critical</th>
</tr>
</thead>
<tbody>
<tr>
<td>5</td>
<td>±2.571</td>
<td>±1.96</td>
</tr>
<tr>
<td>10</td>
<td>±2.228</td>
<td>±1.96</td>
</tr>
<tr>
<td>20</td>
<td>±2.086</td>
<td>±1.96</td>
</tr>
<tr>
<td>30</td>
<td>±2.042</td>
<td>±1.96</td>
</tr>
<tr>
<td>60</td>
<td>±2.000</td>
<td>±1.96</td>
</tr>
<tr>
<td>∞</td>
<td>±1.96</td>
<td>±1.96</td>
</tr>
</tbody>
</table>

<p><strong>Notice:</strong></p>

<ul>
<li>With small samples (low df), t-critical is much larger than z-critical</li>
<li>As sample size increases, t-critical approaches z-critical</li>
<li>You need a more extreme t-value to reject H₀ with small samples</li>
</ul>

<p><strong>Why This Matters:</strong> Small samples require stronger evidence (larger t-values) to reach the same significance level. This protects against Type I errors when sample information is limited.</p>

<h3>Using the t-Table</h3>

<p><strong>To find critical value (manual hypothesis testing):</strong></p>

<ol>
<li>Calculate df = n - 1</li>
<li>Choose alpha level (usually .05)</li>
<li>Determine one-tailed vs. two-tailed</li>
<li>Find where df row meets alpha column</li>
<li>That's your critical value</li>
</ol>

<p><strong>Example:</strong> n = 25, α = .05, two-tailed</p>

<ul>
<li>df = 24</li>
<li>Look up df = 24, α = .05 (two-tailed)</li>
<li>Critical value = ±2.064</li>
</ul>

<p><strong>Decision:</strong></p>

<ul>
<li>If |t_calculated| > 2.064: Reject H₀</li>
<li>If |t_calculated| ≤ 2.064: Fail to reject H₀</li>
</ul>

<p><strong>Modern Approach:</strong> SPSS calculates exact p-values for you, so you rarely need t-tables for research. But understanding them builds intuition!</p>

<h3>t vs. z: When to Use Each</h3>

<p><strong>Use z-test when:</strong></p>

<ul>
<li>You know the population standard deviation (σ)</li>
<li>This is rare! Usually only in textbook examples</li>
</ul>

<p><strong>Use t-test when:</strong></p>

<ul>
<li>You don't know population standard deviation (most real research)</li>
<li>You're estimating σ with sample s</li>
<li>This is the standard approach!</li>
</ul>

<p><strong>Practical Reality:</strong> You'll almost always use t-tests, not z-tests.</p>

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Sample Size Effects</h4>

  <div class="quiz-question">
    <p><strong>Question 1:</strong> When conducting a hypothesis test such as the t-test, having a larger sample size means that the value of the test statistic would _____ and the effect size would _____.</p>
    <div class="options">
      <p>A) Increase; remain the same</p>
      <p>B) Remain the same; decrease</p>
      <p>C) Remain the same; increase</p>
      <p>D) Decrease; remain the same</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> A) Increase; remain the same</p>

      <p class="explanation"><strong>Why this is correct:</strong> Larger sample sizes lead to smaller standard errors, which increases the t-statistic (t = difference / SE). However, effect size (Cohen's d) is calculated from means and standard deviations, not sample size, so it remains unchanged.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>B) Remain same; decrease:</strong> The test statistic definitely changes with sample size, and effect size doesn't decrease with larger samples.</li>
        <li><strong>C) Remain same; increase:</strong> The test statistic changes with sample size, and effect size doesn't increase with larger samples.</li>
        <li><strong>D) Decrease; remain same:</strong> Larger samples increase, not decrease, the test statistic.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 8.4: Factors Affecting Power for how sample size affects test statistics and effect sizes.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 2:</strong> Why does effect size remain the same when sample size increases?</p>
    <div class="options">
      <p>A) Effect size is calculated from the means and standard deviations, not sample size</p>
      <p>B) Larger samples always have smaller effect sizes</p>
      <p>C) Effect size automatically adjusts to sample size</p>
      <p>D) Effect size and sample size are unrelated concepts</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> A) Effect size is calculated from the means and standard deviations, not sample size</p>

      <p class="explanation"><strong>Why this is correct:</strong> Cohen's d = (M - μ) / s. The formula only uses the sample mean (M), population mean (μ), and standard deviation (s). Sample size (n) doesn't appear in this formula, so increasing n doesn't change d.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>B) Larger samples have smaller effects:</strong> This is incorrect—effect size is independent of sample size.</li>
        <li><strong>C) Automatically adjusts:</strong> Effect size doesn't automatically adjust to anything—it's a fixed property of the population difference.</li>
        <li><strong>D) Unrelated concepts:</strong> They're related in that larger samples help you detect smaller effect sizes, but the effect size itself doesn't change.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Think of effect size as measuring "how different" the populations are. This difference doesn't change just because you measured more people.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 3:</strong> What happens to statistical power when sample size increases?</p>
    <div class="options">
      <p>A) Power decreases</p>
      <p>B) Power increases</p>
      <p>C) Power remains the same</p>
      <p>D) Power becomes zero</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) Power increases</p>

      <p class="explanation"><strong>Why this is correct:</strong> Larger sample sizes reduce the standard error, making it easier to detect real effects. This increases statistical power—the probability of correctly rejecting a false null hypothesis.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Power decreases:</strong> This is backwards—larger samples make it easier to detect effects, increasing power.</li>
        <li><strong>C) Power remains same:</strong> Sample size is one of the main factors that affects power, so it definitely changes.</li>
        <li><strong>D) Power becomes zero:</strong> This would only happen with extremely problematic samples, not simply larger samples.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 8.4: Factors Affecting Power for how sample size influences statistical power.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 4:</strong> A researcher conducts the same study with two different sample sizes: n = 25 and n = 100. Both studies find the same sample mean and standard deviation. Which study is more likely to find statistical significance?</p>
    <div class="options">
      <p>A) The study with n = 25</p>
      <p>B) The study with n = 100</p>
      <p>C) Both are equally likely</p>
      <p>D) It depends on the population mean</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) The study with n = 100</p>

      <p class="explanation"><strong>Why this is correct:</strong> Since both studies have the same means and standard deviations, they have the same effect size. However, the larger sample (n = 100) will have a smaller standard error, leading to a larger t-statistic and greater likelihood of statistical significance.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) n = 25:</strong> The smaller sample has less power to detect the same effect size.</li>
        <li><strong>C) Equally likely:</strong> Larger samples are more likely to find significance for the same effect size.</li>
        <li><strong>D) Depends on population mean:</strong> Both studies are comparing to the same population mean, so this doesn't affect the comparison.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> This is why sample size planning is crucial. Larger samples can detect smaller effects and are more likely to find significance for real effects.</p>
    </div>

  </details>
</div>

---

<h2>Part 10: Practical Guide: SPSS for One-Sample t-Tests</h2>

<p>This section walks you through conducting one-sample t-tests in SPSS, from data setup to interpretation.</p>

<h3>Setting Up Your Data</h3>

<p><strong>Step 1: Import or Enter Data</strong></p>

<ul>
<li><code>File → Import Data → Excel</code> (if importing)</li>
<li>Or manually enter data in Data View</li>
</ul>

<p><strong>Step 2: Configure Variables (Variable View)</strong></p>

<ul>
<li>Set measurement level to "Scale" for your continuous variable</li>
<li>Add descriptive labels</li>
<li>Set appropriate decimals</li>
</ul>

<p><strong>Step 3: Check Your Data</strong></p>

<ul>
<li>Look for outliers (extremely high/low values)</li>
<li>Check for data entry errors</li>
<li>Verify n is correct</li>
</ul>

<h3>Running a Basic One-Sample t-Test</h3>

<p><strong>Step 1: Access the Menu</strong></p>

<ul>
<li><code>Analyze → Compare Means → One-Sample T Test</code></li>
</ul>

<p><strong>Step 2: Select Variables</strong></p>

<ul>
<li>Move your test variable from left box to "Test Variable(s)" box</li>
<li>You can test multiple variables at once if they're all compared to the same test value</li>
</ul>

<p><strong>Step 3: Enter Test Value</strong></p>

<ul>
<li>In "Test Value" box, enter the known population mean (μ)</li>
<li>Example: If testing against population mean of 100, enter 100</li>
</ul>

<p><strong>Step 4: Request Effect Size (Recommended)</strong></p>

<ul>
<li>Click "Options" button</li>
<li>Check "Confidence Intervals"</li>
<li>Click "Effect Sizes" tab</li>
<li>Check "Cohen's d"</li>
<li>Click "Continue"</li>
</ul>

<p><strong>Step 5: Run the Test</strong></p>

<ul>
<li>Click "OK"</li>
<li>Results appear in Output window</li>
</ul>

<h3>Reading SPSS Output</h3>

<p>SPSS produces two main tables:</p>

<h4>Table 1: One-Sample Statistics</h4>

<table>
<thead>
<tr>
<th>Variable</th>
<th>N</th>
<th>Mean</th>
<th>Std. Deviation</th>
<th>Std. Error Mean</th>
</tr>
</thead>
<tbody>
<tr>
<td>IQ_Score</td>
<td>30</td>
<td>107.50</td>
<td>14.23</td>
<td>2.60</td>
</tr>
</tbody>
</table>

<p><strong>What It Tells You:</strong></p>

<ul>
<li><strong>N:</strong> Sample size (30)</li>
<li><strong>Mean:</strong> Sample mean (107.50)</li>
<li><strong>Std. Deviation:</strong> Sample SD (14.23)</li>
<li><strong>Std. Error Mean:</strong> SE = s/√n (2.60)</li>
</ul>

<p><strong>Use these for:</strong> Describing your sample, calculating effect size</p>

<h4>Table 2: One-Sample Test (Testing against μ = 100)</h4>

<table>
<thead>
<tr>
<th>Variable</th>
<th>t</th>
<th>df</th>
<th>Sig. (2-tailed)</th>
<th>Mean Difference</th>
<th>95% CI Lower</th>
<th>95% CI Upper</th>
<th>Cohen's d</th>
</tr>
</thead>
<tbody>
<tr>
<td>IQ_Score</td>
<td>2.88</td>
<td>29</td>
<td>.007</td>
<td>7.50</td>
<td>2.17</td>
<td>12.83</td>
<td>0.53</td>
</tr>
</tbody>
</table>

<p><strong>What It Tells You:</strong></p>

<ul>
<li><strong>t:</strong> t-statistic (2.88)</li>
<li><strong>df:</strong> Degrees of freedom (29 = 30-1)</li>
<li><strong>Sig. (2-tailed):</strong> p-value for two-tailed test (.007)</li>
<li><strong>Mean Difference:</strong> M - μ (107.50 - 100 = 7.50)</li>
<li><strong>95% CI:</strong> Confidence interval for the difference (2.17 to 12.83)</li>
<li><strong>Cohen's d:</strong> Effect size (0.53, medium effect)</li>
</ul>

<h3>Interpreting Results</h3>

<p><strong>Decision:</strong></p>

<ul>
<li>p = .007</li>
<li>α = .05</li>
<li>Since .007 < .05, <strong>reject H₀</strong></li>
</ul>

<p><strong>Interpretation:</strong><br>
"The sample (M = 107.50, SD = 14.23) scored significantly higher than the population mean of 100, t(29) = 2.88, p = .007, d = 0.53."</p>

<h3>One-Tailed Tests in SPSS</h3>

<p><strong>SPSS always reports two-tailed p-values.</strong> For one-tailed tests:</p>

<p><strong>Step 1: Check Direction</strong></p>

<ul>
<li>Is your result in the predicted direction?</li>
<li>If predicting higher: Is M > μ?</li>
<li>If predicting lower: Is M < μ?</li>
</ul>

<p><strong>Step 2: Convert p-Value</strong></p>

<ul>
<li>If result is in predicted direction: p_one-tailed = p_two-tailed / 2</li>
<li>If result is in opposite direction: p_one-tailed = 1 - (p_two-tailed / 2)</li>
<li>But you'd fail to reject H₀ anyway!</li>
</ul>

<p><strong>Example 1:</strong> Predicting IQ > 100</p>

<ul>
<li>Observed: M = 107.50 (higher than 100 ✓)</li>
<li>SPSS gives: p = .007 (two-tailed)</li>
<li>One-tailed p = .007 / 2 = <strong>.0035</strong></li>
<li>Even more significant!</li>
</ul>

<p><strong>Example 2:</strong> Predicting stress < 50</p>

<ul>
<li>Observed: M = 52 (higher than 50, wrong direction ✗)</li>
<li>SPSS gives: p = .20 (two-tailed)</li>
<li><strong>Fail to reject H₀</strong> (result is opposite of prediction)</li>
</ul>

<h3>Filtering Data in SPSS</h3>

<p>Sometimes you need to analyze a subset of your data.</p>

<p><strong>Step 1: Select Cases</strong></p>

<ul>
<li><code>Data → Select Cases</code></li>
</ul>

<p><strong>Step 2: Specify Condition</strong></p>

<ul>
<li>Choose "If condition is satisfied"</li>
<li>Click "If..." button</li>
</ul>

<p><strong>Step 3: Write the Condition</strong></p>

<ul>
<li>Examples:</li>
<li><code>Age >= 75</code> (select only ages 75+)</li>
<li><code>Gender = 1</code> (select only code 1, if 1=Female)</li>
<li><code>Score > 50 AND Group = 2</code> (combine conditions)</li>
</ul>

<p><strong>Step 4: Click OK</strong></p>

<ul>
<li>Filtered-out cases show diagonal slash through row number</li>
<li>Only selected cases are used in analyses</li>
</ul>

<p><strong>Step 5: Turn Off Filter When Done</strong></p>

<ul>
<li><code>Data → Select Cases → All cases</code></li>
</ul>

<h3>Common SPSS Issues and Solutions</h3>

<p><strong>Issue:</strong> "Test Value" is grayed out<br>
<strong>Solution:</strong> Make sure you've moved a variable to the Test Variable(s) box first</p>

<p><strong>Issue:</strong> Can't find effect size in output<br>
<strong>Solution:</strong> You must request it before running the test (Options → Effect Sizes → Cohen's d)</p>

<p><strong>Issue:</strong> p-value shows as .000<br>
<strong>Solution:</strong> SPSS rounds very small p-values. Report as "p < .001" (not p = .000)</p>

<p><strong>Issue:</strong> Results seem wrong after filtering<br>
<strong>Solution:</strong> Check that filter is set correctly. Look for slash marks on rows to see what's filtered out.</p>

<p><strong>Issue:</strong> Want to compare to a value not in my data<br>
<strong>Solution:</strong> That's fine! The "Test Value" doesn't need to be in your dataset—it's the population value you're testing against.</p>

<h3>Practice Exercise</h3>

<p><strong>Scenario:</strong> You have data on reaction times (in ms) for 40 gamers. Population average for non-gamers is μ = 250 ms. Test if gamers are significantly faster.</p>

<p><strong>Your Data:</strong></p>

<ul>
<li>n = 40</li>
<li>M = 235 ms</li>
<li>s = 30 ms</li>
</ul>

<p><strong>Tasks:</strong></p>

<ol>
<li>Write hypotheses (one-tailed, predicting faster = lower times)</li>
<li>Run one-sample t-test in SPSS</li>
<li>Interpret results with APA formatting</li>
</ol>

<details>
<summary>Click to see expected results</summary>

<p><strong>Hypotheses:</strong></p>

<ul>
<li>H₀: μ ≥ 250</li>
<li>H₁: μ < 250 (gamers are faster)</li>
</ul>

<p><strong>Expected Calculations:</strong></p>

<ul>
<li>SE = 30/√40 = 4.74</li>
<li>t = (235-250)/4.74 = -3.16</li>
<li>df = 39</li>
</ul>
- p (two-tailed) ≈ .003
- p (one-tailed) = .003/2 = .0015
- d = (235-250)/30 = -0.50

**APA Report:**
"Gamers (M = 235, SD = 30) had significantly faster reaction times than the non-gamer population mean of 250 ms, t(39) = -3.16, p = .002, d = 0.50."

</details>

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: SPSS and APA Reporting</h4>

  <div class="quiz-question">
    <p><strong>Question 1:</strong> A one-sample t-test in SPSS produces output with t(44) = -2.386 and p = .021. How should this result be reported according to APA standards?</p>
    <div class="options">
      <p>A) t(45) = -2.386, p = .021</p>
      <p>B) t(44) = -2.386, p < .05</p>
      <p>C) t(44) = .021</p>
      <p>D) t(44) = -2.386, p = .021</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> D) t(44) = -2.386, p = .021</p>

      <p class="explanation"><strong>Why this is correct:</strong> APA format requires: t(df) = value, p = exact value. The degrees of freedom should be exactly as reported by SPSS, and the exact p-value should be reported unless it's less than .001.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) t(45):</strong> The degrees of freedom should be exactly as reported by SPSS (44), not rounded up.</li>
        <li><strong>B) p < .05:</strong> When the exact p-value is available (.021), report it exactly rather than using the inequality.</li>
        <li><strong>C) Missing p-value:</strong> APA format requires reporting both the t-statistic and p-value.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 10.4: Reading and Interpreting SPSS Output for APA reporting guidelines.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 2:</strong> In SPSS output, where would you find Cohen's d for a one-sample t-test?</p>
    <div class="options">
      <p>A) It's automatically included in the main t-test table</p>
      <p>B) In a separate "Effect Sizes" table (if requested)</p>
      <p>C) It's never available in SPSS</p>
      <p>D) In the "Descriptive Statistics" table</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) In a separate "Effect Sizes" table (if requested)</p>

      <p class="explanation"><strong>Why this is correct:</strong> Cohen's d is not automatically calculated in SPSS. You must request it before running the test (Options → Effect Sizes → Cohen's d), and it will appear in a separate table.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Automatically included:</strong> SPSS doesn't automatically calculate effect sizes—you must request them.</li>
        <li><strong>C) Never available:</strong> SPSS can calculate Cohen's d, but only if you specifically request it in the Options.</li>
        <li><strong>D) Descriptive Statistics table:</strong> This table shows means and standard deviations, not effect sizes.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Always remember to request effect sizes in SPSS before running your test. You can't add them after the fact.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 3:</strong> A one-sample t-test was conducted to see if blood pressure from a sample was significantly different from 90. The SPSS output shows a negative t-value and p < .05. What can be concluded?</p>
    <div class="options">
      <p>A) No conclusion can be drawn from the test result</p>
      <p>B) The sample blood pressure was significantly lower than 90</p>
      <p>C) The sample blood pressure was not significantly different from 90</p>
      <p>D) The sample blood pressure was significantly higher than 90</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) The sample blood pressure was significantly lower than 90</p>

      <p class="explanation"><strong>Why this is correct:</strong> A negative t-value means the sample mean is below the population value (90). Since p < .05, the difference is statistically significant. Therefore, the sample blood pressure is significantly lower than 90.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) No conclusion:</strong> The results are clear—negative t-value with p < .05 indicates significant difference below the population value.</li>
        <li><strong>C) Not significant:</strong> p < .05 means the result IS significant.</li>
        <li><strong>D) Significantly higher:</strong> A negative t-value indicates the sample mean is below, not above, the population value.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 10.4: Reading and Interpreting SPSS Output for how to interpret the direction of t-values.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 4:</strong> Which report of statistical results is in appropriate APA format?</p>
    <div class="options">
      <p>A) t = 1.2, df = 5</p>
      <p>B) t = 1.2, df = 5, p < 0.05</p>
      <p>C) t(5) = 1.2, p = .013</p>
      <p>D) t = 1.2, p = .000</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> C) t(5) = 1.2, p = .013</p>

      <p class="explanation"><strong>Why this is correct:</strong> APA format requires: t(df) = value, p = exact value. The degrees of freedom go in parentheses immediately after t, and the exact p-value should be reported when available.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Missing p-value:</strong> APA format requires reporting the p-value along with the t-statistic.</li>
        <li><strong>B) df = 5 instead of t(5):</strong> The degrees of freedom should be in parentheses immediately after t, not as a separate item.</li>
        <li><strong>D) p = .000:</strong> Never report p = .000. Use p < .001 instead.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Remember the APA format: t(df) = value, p = value. Always include both the test statistic and p-value.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 5:</strong> What is the independent variable in a graph comparing in-state tuition between public and private colleges?</p>
    <div class="options">
      <p>A) Type of college</p>
      <p>B) In-state tuition</p>
      <p>C) Private college</p>
      <p>D) Public college</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> A) Type of college</p>

      <p class="explanation"><strong>Why this is correct:</strong> The independent variable is what you're comparing or manipulating. In this case, you're comparing tuition between different types of colleges (public vs. private), so "Type of college" is the IV.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>B) In-state tuition:</strong> This is the dependent variable—what you're measuring (the outcome).</li>
        <li><strong>C) Private college:</strong> This is one level of the independent variable, not the IV itself.</li>
        <li><strong>D) Public college:</strong> This is one level of the independent variable, not the IV itself.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 1: Introduction to One-Sample t-Tests for the distinction between independent and dependent variables.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 6:</strong> Based on the statistical results provided, which would lead us to reject the null hypothesis using α = .05?</p>
    <div class="options">
      <p>A) t(4) = 2.2, p = .09</p>
      <p>B) t(11) = 2.2, p = .11</p>
      <p>C) t(12) = 2.2, p = .03</p>
      <p>D) t(10) = 2.2, p = .065</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> C) t(12) = 2.2, p = .03</p>

      <p class="explanation"><strong>Why this is correct:</strong> To reject the null hypothesis, the p-value must be less than or equal to α (.05). Only option C has p = .03, which is less than .05.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) p = .09:</strong> This is greater than .05, so we fail to reject the null hypothesis.</li>
        <li><strong>B) p = .11:</strong> This is greater than .05, so we fail to reject the null hypothesis.</li>
        <li><strong>D) p = .065:</strong> This is greater than .05, so we fail to reject the null hypothesis.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> The decision rule is simple: if p ≤ α, reject H₀; if p > α, fail to reject H₀. Always compare your p-value to your chosen alpha level.</p>
    </div>

  </details>
</div>

---

## Quick Reference Card

### Hypothesis Testing Decision Tree

```
Start: Do you have a research question?
    |
    ├─ ONE sample comparing to known population value?
    |   └─→ ONE-SAMPLE T-TEST (Module 2)
    |
    ├─ TWO samples from different groups?
    |   └─→ INDEPENDENT-SAMPLES T-TEST (Module 3)
    |
    └─ Same people measured twice?
        └─→ PAIRED-SAMPLES T-TEST (Module 3)
```

### The 7-Step Hypothesis Testing Process

**Step 1:** State hypotheses (H₀ and H₁)
**Step 2:** Set alpha level (α = .05)
**Step 3:** Calculate descriptive statistics (n, M, s)
**Step 4:** Calculate standard error (SE = s/√n)
**Step 5:** Calculate t-statistic (t = (M - μ)/SE)
**Step 6:** Determine df and find p-value
**Step 7:** Make decision and interpret

### Critical Decision Rules

| Situation                                  | Decision           | Action                                  |
| ------------------------------------------ | ------------------ | --------------------------------------- |
| p < α (.05)                                | Reject H₀          | Result is statistically significant     |
| p ≥ α (.05)                                | Fail to reject H₀  | Result is not statistically significant |
| Result in predicted direction (one-tailed) | Divide SPSS p by 2 | p_one-tailed = p_SPSS / 2               |
| Result in wrong direction (one-tailed)     | Fail to reject H₀  | Don't divide p-value                    |

### Essential Formulas Quick Reference

| Formula            | Equation       | When to Use                |
| ------------------ | -------------- | -------------------------- |
| Standard Error     | SE = s/√n      | Always needed for t-test   |
| t-Statistic        | t = (M - μ)/SE | One-sample t-test          |
| Degrees of Freedom | df = n - 1     | One-sample t-test          |
| Cohen's d          | d = (M - μ)/s  | Effect size for one-sample |

### Effect Size Interpretation

| Cohen's d | Interpretation | Example                     |
| --------- | -------------- | --------------------------- |
| 0.2       | Small effect   | Noticeable to experts       |
| 0.5       | Medium effect  | Visible to careful observer |
| 0.8       | Large effect   | Obvious to anyone           |

> **Remember:** These are guidelines, not rigid rules. Context matters!

### One-Tailed vs. Two-Tailed Quick Guide

| Aspect          | One-Tailed                         | Two-Tailed             |
| --------------- | ---------------------------------- | ---------------------- |
| **When to use** | Specific directional prediction    | Any difference/change  |
| **Power**       | Higher (for predicted direction)   | Lower but safer        |
| **p-value**     | Divide SPSS p by 2\*               | Use SPSS p as reported |
| **Risk**        | Miss effects in opposite direction | More conservative      |

\*Only if result is in predicted direction!

### APA Format Template

**Complete reporting:**
"[Sample description] (M = [mean], SD = [SD]) [comparison statement], t([df]) = [t-value], p = [p-value], d = [Cohen's d]."

**Example:**
"College students (M = 6.2, SD = 1.3) slept significantly less than the recommended 8 hours, t(149) = -8.52, p < .001, d = 1.38."

### Common Mistakes Checklist

☐ **Don't say "accept H₀"** → Say "fail to reject H₀"
☐ **Don't forget effect size** → Always report Cohen's d
☐ **Don't decide one/two-tailed after seeing data** → Decide before data collection
☐ **Don't confuse s and SE** → SE = s/√n (always smaller)
☐ **Don't ignore power** → Check if your study could detect effects
☐ **Don't report p = .000** → Use p < .001 instead

### Statistical Power Quick Facts

| Factor             | Effect on Power           | How to Improve                |
| ------------------ | ------------------------- | ----------------------------- |
| Sample size (n)    | ↑ n = ↑ Power             | **Recruit more participants** |
| Effect size (d)    | ↑ d = ↑ Power             | Use stronger interventions    |
| Alpha (α)          | ↑ α = ↑ Power             | Usually keep at .05           |
| One vs. two-tailed | One-tailed has more power | Only if appropriate           |

**Target:** Aim for power ≥ .80 (80% chance of detecting real effects)

### Error Types at a Glance

| Error       | What It Is                        | Probability       | How to Reduce              |
| ----------- | --------------------------------- | ----------------- | -------------------------- |
| **Type I**  | False positive (reject true H₀)   | α (typically .05) | Lower α, replicate         |
| **Type II** | False negative (miss real effect) | β (varies)        | Increase n, increase power |

**Trade-off:** Can't minimize both simultaneously!

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

<strong>Null Hypothesis (H₀):</strong> Statement of no effect/no difference

**Alternative Hypothesis (H₁):** Research prediction; what you're trying to support

**p-Value:** Probability of getting your results (or more extreme) if H₀ is true

**Alpha (α):** Significance threshold (usually .05)

**Type I Error:** False positive (reject true H₀), probability = α

**Type II Error:** False negative (fail to reject false H₀), probability = β

**Power:** Probability of correctly detecting real effect = 1 - β

**Effect Size (d):** Standardized measure of how large an effect is

### Key Formulas

**Standard Error:**

SE = s / √n

**t-Statistic (One-Sample):**

t = (M - μ) / SE = (M - μ) / (s / √n)

**Degrees of Freedom (One-Sample t-Test):**

df = n - 1

**Cohen's d (One-Sample):**

d = (M - μ) / s

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

<strong>Null Hypothesis (H₀):</strong> Statement of no effect/no difference

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

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Hypothesis Testing Decisions</h4>

  <div class="quiz-question">
    <p><strong>Question 1:</strong> When comparing a p-value to alpha = .05, which statement is correct?</p>
    <div class="options">
      <p>A) If p > .05, reject the null hypothesis</p>
      <p>B) If p ≤ .05, reject the null hypothesis</p>
      <p>C) If p = .05, fail to reject the null hypothesis</p>
      <p>D) The p-value doesn't matter for decision making</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) If p ≤ .05, reject the null hypothesis</p>

      <p class="explanation"><strong>Why this is correct:</strong> The decision rule is: if p ≤ α, reject H₀; if p > α, fail to reject H₀. Since α = .05, we reject the null hypothesis when p ≤ .05.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) p > .05, reject:</strong> This is backwards—we reject when p is small (≤ α), not large.</li>
        <li><strong>C) p = .05, fail to reject:</strong> When p = α exactly, we reject H₀ (the inequality is ≤, not <).</li>
        <li><strong>D) p-value doesn't matter:</strong> The p-value is central to hypothesis testing decisions.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 3: The Decision-Making Framework for the decision rules.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 2:</strong> What is the difference between Type I and Type II errors?</p>
    <div class="options">
      <p>A) Type I error is rejecting a false null; Type II error is failing to reject a true null</p>
      <p>B) Type I error is rejecting a true null; Type II error is failing to reject a false null</p>
      <p>C) They are the same thing</p>
      <p>D) Type I error is always more serious than Type II error</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) Type I error is rejecting a true null; Type II error is failing to reject a false null</p>

      <p class="explanation"><strong>Why this is correct:</strong> Type I error (false positive) occurs when we reject a true null hypothesis. Type II error (false negative) occurs when we fail to reject a false null hypothesis.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Reverses the definitions:</strong> This has Type I and Type II errors backwards.</li>
        <li><strong>C) Same thing:</strong> They are completely different types of mistakes in hypothesis testing.</li>
        <li><strong>D) Always more serious:</strong> The seriousness depends on context—both can be problematic in different situations.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 4: Understanding Type I and Type II Errors for detailed explanations.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 3:</strong> If a researcher sets α = .01 instead of α = .05, what happens to the probability of Type I and Type II errors?</p>
    <div class="options">
      <p>A) Type I error increases; Type II error decreases</p>
      <p>B) Type I error decreases; Type II error increases</p>
      <p>C) Both errors increase</p>
      <p>D) Both errors decrease</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) Type I error decreases; Type II error increases</p>

      <p class="explanation"><strong>Why this is correct:</strong> Lowering alpha (from .05 to .01) makes it harder to reject the null hypothesis, reducing Type I errors (false positives) but increasing Type II errors (false negatives). There's always a trade-off between these errors.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Type I increases; Type II decreases:</strong> This would happen if alpha increased, not decreased.</li>
        <li><strong>C) Both increase:</strong> Type I and Type II errors have an inverse relationship—when one goes up, the other goes down.</li>
        <li><strong>D) Both decrease:</strong> You can't reduce both errors simultaneously—there's always a trade-off.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Think of alpha as your "skepticism level." Lower alpha = more skeptical = fewer false positives but more false negatives.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 4:</strong> A researcher finds p = .08 in their one-sample t-test with α = .05. What should they conclude?</p>
    <div class="options">
      <p>A) Reject the null hypothesis because the effect is close to significant</p>
      <p>B) Fail to reject the null hypothesis because p > α</p>
      <p>C) The result is significant because p < .10</p>
      <p>D) The test is inconclusive</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) Fail to reject the null hypothesis because p > α</p>

      <p class="explanation"><strong>Why this is correct:</strong> The decision rule is clear: if p > α, fail to reject H₀. Since .08 > .05, we fail to reject the null hypothesis. There's no "close to significant" in hypothesis testing—it's either significant or it isn't.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Close to significant:</strong> There's no such thing as "close to significant." The decision is binary based on the alpha level.</li>
        <li><strong>C) Significant because p < .10:</strong> The alpha level was set at .05, not .10. You can't change the criterion after seeing the results.</li>
        <li><strong>D) Inconclusive:</strong> The test is conclusive—we fail to reject H₀. The conclusion is that there's insufficient evidence for the alternative hypothesis.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Always stick to your predetermined alpha level. Don't change the rules after seeing the results—this would be p-hacking.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 5:</strong> What does it mean when we "fail to reject" the null hypothesis?</p>
    <div class="options">
      <p>A) We have proven the null hypothesis is true</p>
      <p>B) We have proven the alternative hypothesis is false</p>
      <p>C) We don't have enough evidence to conclude the alternative hypothesis is true</p>
      <p>D) The study was poorly designed</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> C) We don't have enough evidence to conclude the alternative hypothesis is true</p>

      <p class="explanation"><strong>Why this is correct:</strong> "Fail to reject H₀" means we don't have sufficient evidence to support the alternative hypothesis. It doesn't prove H₀ is true—it just means we can't confidently say H₁ is true.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Proven null is true:</strong> We never prove hypotheses in statistics—we only gather evidence for or against them.</li>
        <li><strong>B) Proven alternative is false:</strong> Again, we don't prove hypotheses false—we just don't have evidence for them.</li>
        <li><strong>D) Poorly designed study:</strong> A non-significant result doesn't necessarily mean poor design—it could mean insufficient power or a true null hypothesis.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 3: The Decision-Making Framework for the proper interpretation of statistical decisions.</p>
    </div>

  </details>
</div>

            <!-- Bottom Navigation -->
            <div class="tab-navigation bottom-nav">
                <button class="tab-button" onclick="showTab(1)">
                    <input type="checkbox" id="progress-1-bottom" class="tab-checkbox" onchange="toggleTabComplete(1)">
                    <span class="tab-label">Hypothesis Testing Logic</span>
                </button>
                <button class="tab-button" onclick="showTab(2)">
                    <input type="checkbox" id="progress-2-bottom" class="tab-checkbox" onchange="toggleTabComplete(2)">
                    <span class="tab-label">Decision Making & Errors</span>
                </button>
                <button class="tab-button" onclick="showTab(3)">
                    <input type="checkbox" id="progress-3-bottom" class="tab-checkbox" onchange="toggleTabComplete(3)">
                    <span class="tab-label">Sampling & t-Tests</span>
                </button>
                <button class="tab-button" onclick="showTab(4)">
                    <input type="checkbox" id="progress-4-bottom" class="tab-checkbox" onchange="toggleTabComplete(4)">
                    <span class="tab-label">Effect Size & Power</span>
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

_Remember: Statistics is a way of thinking about evidence, not just a set of formulas. When in doubt, ask yourself: "What question am I trying to answer, and what would constitute convincing evidence?"_

<script>
// Progress tracking storage key
const PROGRESS_KEY = 'm2-lecture-progress';

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
const KC_STORAGE_KEY = 'm2-knowledge-checks';

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
