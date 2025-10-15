---
layout: lecture
title: "Module 5: Two-Way Factorial ANOVA"
---

# Module 5: Two-Way Factorial ANOVA

## Understanding Complex Relationships Between Multiple Factors

**Estimated Study Time:** 2-3 hours

## Learning Objectives

By the end of this module, you will be able to:

1. Explain why factorial ANOVA is necessary when studying multiple independent variables
2. Understand and use factorial design notation (2x2, 2x3, 3x3, etc.)
3. Calculate the number of cells in a factorial design
4. Distinguish between between-groups, within-groups, and mixed-design factorial ANOVAs
5. Define and interpret main effects for each factor
6. Define and interpret interaction effects between factors
7. Understand why interactions are typically the most important finding in factorial ANOVA
8. Identify the three separate null hypotheses tested in a two-way ANOVA
9. Calculate degrees of freedom for factorial designs
10. Apply the decision tree for interpreting factorial ANOVA results
11. Determine when to run simple effects tests vs. post-hoc tests
12. Perform two-way ANOVA in SPSS and interpret the output
13. Calculate and interpret effect sizes for factorial ANOVA
14. Report factorial ANOVA results in proper APA format

---

## Table of Contents

1. [Introduction to Factorial ANOVA](#part-1-introduction-to-factorial-anova)
2. [Factorial Design Fundamentals](#part-2-factorial-design-fundamentals)
3. [Main Effects](#part-3-main-effects)
4. [Interaction Effects: The Heart of Factorial ANOVA](#part-4-interaction-effects-the-heart-of-factorial-anova)
5. [The Omnibus Test in Two-Way ANOVA](#part-5-the-omnibus-test-in-two-way-anova)
6. [The Decision Tree: Interpreting Factorial ANOVA Results](#part-6-the-decision-tree-interpreting-factorial-anova-results)
7. [Simple Effects Tests](#part-7-simple-effects-tests)
8. [Effect Size in Factorial ANOVA](#part-8-effect-size-in-factorial-anova)
9. [Assumptions of Factorial ANOVA](#part-9-assumptions-of-factorial-anova)
10. [SPSS Practical Guide](#part-10-spss-practical-guide)
11. [Reporting Factorial ANOVA in APA Format](#part-11-reporting-factorial-anova-in-apa-format)
12. [Summary and Key Formulas](#summary-and-key-formulas)

---

## Part 1: Introduction to Factorial ANOVA

### Moving Beyond Single Factors

So far in this course, you've learned to compare groups using:

- **Independent-samples t-test:** Comparing 2 groups
- **Paired-samples t-test:** Comparing 2 conditions (same participants)
- **One-way ANOVA:** Comparing 3+ groups on one independent variable

But what happens when you want to study **two or more independent variables simultaneously**? That's where **factorial ANOVA** comes in.

### Why Not Just Run Multiple One-Way ANOVAs?

Imagine you're studying the effects of:

- **Factor A:** Teaching method (lecture vs. hands-on)
- **Factor B:** Class size (small vs. large)
- **DV:** Student test scores

You could run two separate one-way ANOVAs:

1. Compare teaching methods (ignoring class size)
2. Compare class sizes (ignoring teaching method)

**But this approach has three major problems:**

**Problem 1: Inefficiency**

- You're running multiple separate analyses instead of one comprehensive test
- More time-consuming and complex to manage

**Problem 2: Inflated Type I Error**

- Each additional test increases the probability of a false positive
- Running 2 tests at α = .05 each gives you a familywise error rate > .05

**Problem 3: Missing the Interaction (THE BIG ONE)**

- **The real world is complex.** The effect of one factor often depends on the level of another factor
- Example: Hands-on teaching might work great in small classes but poorly in large classes
- Separate one-way ANOVAs can **never** detect this crucial interaction

### Real-World Examples of Interactions

**Example 1: Education**

- Teaching method (lecture, discussion, hands-on) × Student level (beginner, advanced)
- Interaction: Hands-on works best for beginners, but advanced students benefit most from discussion

**Example 2: Medicine**

- Drug dosage (low, medium, high) × Patient age (young, elderly)
- Interaction: Medium dose is optimal for young patients, but elderly patients need low dose

**Example 3: Marketing**

- Advertisement type (emotional, factual) × Product category (luxury, practical)
- Interaction: Emotional ads work for luxury products, factual ads work for practical products

**Example 4: Psychology**

- Therapy type (CBT, medication) × Disorder severity (mild, severe)
- Interaction: CBT works well for mild cases, but severe cases need medication

### The Three Advantages of Factorial ANOVA

**1. Efficiency:**

- Test multiple factors in a single analysis
- Saves time and resources
- More elegant research design

**2. Control of Type I Error:**

- One omnibus test controls familywise error rate
- Maintains α = .05 across all comparisons

**3. Detection of Interactions:**

- **This is the game-changer**
- Reveals how factors work together
- Provides a more complete, nuanced understanding of your data
- Often the most interesting and important finding

### When to Use Factorial ANOVA

**Use factorial ANOVA when:**

- You have **2 or more independent variables** (factors)
- Each factor has **2 or more levels**
- You want to test **main effects** and **interaction effects**
- Your dependent variable is **continuous** (interval or ratio)

**Research scenarios:**

- Examining how treatment type and patient characteristics affect outcomes
- Testing how product features and marketing strategies influence sales
- Investigating how teaching methods and student characteristics affect learning
- Studying how environmental factors and genetic factors affect behavior

### Quick Review: Building on One-Way ANOVA

Before diving into factorial ANOVA, let's briefly connect to what you already know. In one-way ANOVA, we tested one independent variable with multiple levels (e.g., three teaching methods) and partitioned variance into between-groups and within-groups components. **Factorial ANOVA extends this logic**: we still partition variance, but now the between-groups variance is further divided into separate main effects for each factor PLUS an interaction effect. The fundamental principle remains the same—we're comparing group means—but now we can examine multiple factors and how they work together. Everything you learned about F-ratios, assumptions, and effect sizes still applies.

### Why This Matters: Real Research Examples

**Research Example 1: Stereotype Threat (Steele & Aronson, 1995)**

Famous study examining test performance with factors: Race (Black, White) × Test Description (intelligence test, problem-solving task). The interaction revealed that Black students performed worse ONLY when the test was framed as an intelligence test—not when it was described as problem solving. This interaction changed our understanding of stereotype threat and led to practical interventions.

**Research Example 2: Memory and Sleep (Mednick et al., 2003)**

Researchers studied memory improvement with Time of Day (morning, evening) × Condition (nap, no nap). The interaction showed that napping improved memory performance for evening learners but had minimal effect for morning learners. Without examining the interaction, we'd miss that napping's benefits depend on individual chronotype.

**Research Example 3: Social Media and Well-Being (Current Research)**

Studies examine Screen Time (low, moderate, high) × Usage Type (active, passive). Interactions show that high screen time is associated with poor well-being ONLY for passive users (scrolling). Active users (messaging friends) don't show the same negative effects. The interaction reveals nuance that main effects alone would miss.

**The Bottom Line:** Factorial ANOVA reveals the complexity of real-world phenomena. Most psychological effects aren't universal—they depend on context, individual differences, and other factors. Learning factorial ANOVA makes you a better researcher and critical thinker.

---

## Part 2: Factorial Design Fundamentals

### Understanding Design Notation

Factorial designs are described using a **notation system** that tells you:

1. How many factors (IVs) are in the study
2. How many levels each factor has

**The Notation Format:** A × B × C...

**Examples:**

**2×2 Design ("two by two"):**

- 2 factors
- First factor has 2 levels
- Second factor has 2 levels
- Example: Gender (male, female) × Teaching method (lecture, hands-on)

**2×3 Design ("two by three"):**

- 2 factors
- First factor has 2 levels
- Second factor has 3 levels
- Example: Gender (male, female) × Class size (small, medium, large)

**3×3 Design ("three by three"):**

- 2 factors
- First factor has 3 levels
- Second factor has 3 levels
- Example: Teaching method (lecture, discussion, hands-on) × Class size (small, medium, large)

**2×2×2 Design ("two by two by two"):**

- 3 factors
- Each factor has 2 levels
- Example: Gender × Teaching method × Class size (all with 2 levels each)

### Calculating the Number of Cells

A **cell** is a unique combination of factor levels. The number of cells equals the number of **unique groups** in your study.

**Formula:** Number of cells = Level₁ × Level₂ × Level₃...

**Examples:**

**2×2 Design:**

- 2 × 2 = **4 cells**
- Gender (male, female) × Teaching method (lecture, hands-on)
- Cells: Male-Lecture, Male-Hands-on, Female-Lecture, Female-Hands-on

**2×3 Design:**

- 2 × 3 = **6 cells**
- Gender (male, female) × Class size (small, medium, large)
- Cells: Male-Small, Male-Medium, Male-Large, Female-Small, Female-Medium, Female-Large

**3×3 Design:**

- 3 × 3 = **9 cells**

**2×2×2 Design:**

- 2 × 2 × 2 = **8 cells**

### Visual Representation: The Factorial Design Table

**2×2 Design Example:**

|            | Lecture | Hands-on |
| ---------- | ------- | -------- |
| **Male**   | Cell 1  | Cell 2   |
| **Female** | Cell 3  | Cell 4   |

**2×3 Design Example:**

|            | Small  | Medium | Large  |
| ---------- | ------ | ------ | ------ |
| **Male**   | Cell 1 | Cell 2 | Cell 3 |
| **Female** | Cell 4 | Cell 5 | Cell 6 |

Each cell contains a group of participants experiencing that unique combination of conditions.

### Types of Factorial Designs

**Between-Groups (Independent-Groups) Factorial ANOVA:**

- **Different participants** in each cell
- Most common type of factorial design
- Example: Different students in each teaching method × class size combination

**Within-Groups (Repeated-Measures) Factorial ANOVA:**

- **Same participants** experience all combinations
- Requires participants to experience all levels of all factors
- Less common because it can be impractical

**Mixed-Design Factorial ANOVA:**

- **Combination** of between-groups and within-groups factors
- Some factors are between-groups, others are within-groups
- Example: Gender (between) × Time of testing (within: morning, afternoon, evening)

**Focus of this lecture:** We'll primarily focus on **between-groups factorial ANOVA**, as it's the most common and is what you'll use in your assignment.

### Identifying IVs and DVs in Factorial Studies

**Independent Variables (IVs) = Factors:**

- The variables you manipulate or categorize
- Each IV has 2+ levels
- In a 2×3 design, you have 2 IVs

**Dependent Variable (DV):**

- The outcome you measure
- Must be continuous (interval or ratio scale)
- Only ONE DV in a two-way ANOVA

**Example Study:**

- **Research Question:** "Do community type and religious affiliation affect the percentage of graduates going to college?"
- **IV 1 (Factor A):** Community type (city vs. suburb) - 2 levels
- **IV 2 (Factor B):** Religious affiliation (yes vs. no) - 2 levels
- **DV:** Percentage of graduates going to college (continuous)
- **Design:** 2×2 between-groups factorial ANOVA
- **Cells:** 4 (City-Religious, City-Non-religious, Suburb-Religious, Suburb-Non-religious)

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Factorial Design Fundamentals</h4>

  <div class="quiz-question">
    <p><strong>Question 1:</strong> Roediger and Karpicke (2006) investigated whether the test-enhanced learning effect was due merely to repeated exposure to material. They randomly assigned participants to one of two study conditions (study-study or study-test) and to one of three retention interval conditions (final test at a delay of 5 minutes, 2 days, or 1 week). The dependent variable was the proportion of idea units recalled. How should the analysis of these data be labeled?</p>
    <div class="options">
      <p>A) 2×3 between-groups ANOVA</p>
      <p>B) 2×2 between-groups ANOVA</p>
      <p>C) 2×2 within-groups ANOVA</p>
      <p>D) 2×3 within-groups ANOVA</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> A) 2×3 between-groups ANOVA</p>

      <p class="explanation"><strong>Why this is correct:</strong> There are 2 factors: study condition (2 levels: study-study, study-test) and retention interval (3 levels: 5 minutes, 2 days, 1 week). This is 2×3. Participants were "randomly assigned," meaning different participants in each condition, making it between-groups.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>B) 2×2 between-groups:</strong> The retention interval has 3 levels, not 2.</li>
        <li><strong>C) 2×2 within-groups:</strong> Wrong on both counts—it's 2×3, and it's between-groups.</li>
        <li><strong>D) 2×3 within-groups:</strong> Correct dimensions but wrong design—participants were randomly assigned to conditions, not measured repeatedly.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 2: Factorial Design Fundamentals for design notation.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 2:</strong> The sale amount was analyzed by store location (3 locations) and shelf position (2 positions). How many cells (groups) were in the factorial design?</p>
    <div class="options">
      <p>A) 4</p>
      <p>B) 6</p>
      <p>C) 2</p>
      <p>D) 5</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) 6</p>

      <p class="explanation"><strong>Why this is correct:</strong> Number of cells = levels of Factor 1 × levels of Factor 2 = 3 store locations × 2 shelf positions = 6 cells. This is a 3×2 factorial design.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) 4:</strong> This would be correct for a 2×2 design, but we have 3 locations.</li>
        <li><strong>C) 2:</strong> This is just the number of levels in one factor, not the total cells.</li>
        <li><strong>D) 5:</strong> This would be 3 + 2, but we multiply, not add.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Always multiply the number of levels across factors to get the total number of cells.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 3:</strong> A researcher is interested in whether circadian rhythms influence participants' performance on different kinds of memory tests. The researcher first classifies participants according to whether each is a morning person or an evening person. The researcher then randomly assigns participants to receive either an implicit memory test or an explicit memory test. The researcher then tests everyone at 8 A.M. What is(are) the main effect(s) being tested in the study?</p>
    <div class="options">
      <p>A) Type of person and performance</p>
      <p>B) Memory test</p>
      <p>C) Type of person</p>
      <p>D) Type of person and memory test</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> D) Type of person and memory test</p>

      <p class="explanation"><strong>Why this is correct:</strong> In a factorial ANOVA, we test the main effect of each independent variable. The two IVs are: (1) type of person (morning vs. evening), and (2) memory test type (implicit vs. explicit). Performance is the DV, not an IV.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Type of person and performance:</strong> Performance is the dependent variable, not an independent variable with a main effect.</li>
        <li><strong>B) Memory test only:</strong> This is only one of the two main effects being tested.</li>
        <li><strong>C) Type of person only:</strong> This is only one of the two main effects being tested.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 2: Factorial Design Fundamentals for identifying IVs.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 4:</strong> If an analysis of variance includes both within-groups factors and between-groups factors, it is called a ____ ANOVA.</p>
    <div class="options">
      <p>A) Complex-design</p>
      <p>B) Mixed-design</p>
      <p>C) Between-within</p>
      <p>D) Two-way</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) Mixed-design</p>

      <p class="explanation"><strong>Why this is correct:</strong> A mixed-design ANOVA (also called split-plot design) includes at least one between-groups factor and at least one within-groups (repeated-measures) factor.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Complex-design:</strong> This is not the standard statistical term for this type of ANOVA.</li>
        <li><strong>C) Between-within:</strong> While descriptive, "mixed-design" is the proper statistical terminology.</li>
        <li><strong>D) Two-way:</strong> This refers to the number of factors (2), not whether they're between or within.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 2: Factorial Design Fundamentals for types of factorial designs.</p>
    </div>

  </details>
</div>

---

## Part 3: Main Effects

### What is a Main Effect?

A **main effect** is the effect of **one independent variable on the dependent variable, averaging across (ignoring) all other independent variables**.

**Key Insight:** In a two-way ANOVA, you test for **two separate main effects**:

1. Main effect of Factor A
2. Main effect of Factor B

**Definition:** A main effect tells you whether the levels of one factor differ significantly from each other, **on average**, when you collapse (average) across all levels of the other factor(s).

### Main Effect of Factor A

**Question asked:** "Does Factor A have an effect on the DV, ignoring Factor B?"

**Example:**

- Factor A: Community type (city vs. suburb)
- Factor B: Religious affiliation (yes vs. no)
- DV: Percentage going to college

**Main Effect of Community Type:**

- Do city schools differ from suburban schools in college-going rates, **averaging across both religious and non-religious schools**?

### Main Effect of Factor B

**Question asked:** "Does Factor B have an effect on the DV, ignoring Factor A?"

**Example:**
**Main Effect of Religious Affiliation:**

- Do religious schools differ from non-religious schools in college-going rates, **averaging across both city and suburban schools**?

### Marginal Means

**Marginal means** are the averages for each level of one factor, collapsed across all levels of the other factor.

**Example Data Table:**

|                          | City Schools | Suburban Schools | **Row Marginal Mean** |
| ------------------------ | ------------ | ---------------- | --------------------- |
| **Religious**            | 75%          | 85%              | **80%**               |
| **Non-Religious**        | 60%          | 70%              | **65%**               |
| **Column Marginal Mean** | **67.5%**    | **77.5%**        |                       |

**Main Effect of Religious Affiliation:**

- Compare row marginal means: 80% vs. 65%
- Religious schools have higher college-going rates (averaging across city and suburb)

**Main Effect of Community Type:**

- Compare column marginal means: 67.5% vs. 77.5%
- Suburban schools have higher college-going rates (averaging across religious and non-religious)

### Hypotheses for Main Effects

**For Factor A (Community Type):**

- **H₀:** μ_city = μ_suburb (No difference in college-going rates between city and suburban schools)
- **H₁:** μ_city ≠ μ_suburb (There is a difference)

**For Factor B (Religious Affiliation):**

- **H₀:** μ_religious = μ_non-religious (No difference between religious and non-religious schools)
- **H₁:** μ_religious ≠ μ_non-religious (There is a difference)

### Testing Main Effects

Each main effect is tested with its own **F-test**:

- **F for Factor A:** Tests whether the marginal means for Factor A differ significantly
- **F for Factor B:** Tests whether the marginal means for Factor B differ significantly

**Decision Rule (for each main effect):**

- **p < .05:** Reject H₀, the main effect is significant
- **p ≥ .05:** Fail to reject H₀, the main effect is not significant

### When Main Effects Have 2 Levels

**If a factor has only 2 levels:**

- A significant F-test tells you which direction the effect goes
- Just compare the two marginal means
- **No post-hoc tests needed**

**Example:** Religious (yes vs. no) has 2 levels

- If F is significant, compare marginal means: 80% vs. 65%
- Conclusion: Religious schools have higher rates

### When Main Effects Have 3+ Levels

**If a factor has 3 or more levels:**

- A significant F-test only tells you that differences exist somewhere
- You **must run post-hoc tests** to determine which specific levels differ
- Use Tukey, Bonferroni, or Scheffé

**Example:** Class size (small, medium, large) has 3 levels

- If F is significant, marginal means might be: 70%, 75%, 85%
- Post-hoc tests tell you: Large > Small, Large > Medium, Medium = Small

<div class="common-mistakes">
  <h4>⚠️ Common Mistakes with Main Effects</h4>
  <ul>
    <li><strong>Mistake 1:</strong> Confusing main effects with interactions. Main effects look at each factor SEPARATELY, averaging across the other factor.</li>
    <li><strong>Mistake 2:</strong> Comparing cell means instead of marginal means for main effects. Main effects use marginal means (averages across rows or columns).</li>
    <li><strong>Mistake 3:</strong> Interpreting main effects as meaningful when there's a significant interaction. Always check the interaction first!</li>
    <li><strong>Mistake 4:</strong> Forgetting to run post-hoc tests when a main effect has 3+ levels. The F-test only tells you differences exist, not which groups differ.</li>
  </ul>
</div>

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Main Effects</h4>

  <div class="quiz-question">
    <p><strong>Question 1:</strong> Main effects refer to the _____.</p>
    <div class="options">
      <p>A) Effect of a single independent variable on the dependent variable, disregarding all other variables in the study</p>
      <p>B) Combined effects of two dependent variables</p>
      <p>C) Effect of one level of the independent variable on the dependent variable, disregarding other levels of the independent variable</p>
      <p>D) Combined effects of two independent variables</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> A) Effect of a single independent variable on the dependent variable, disregarding all other variables in the study</p>

      <p class="explanation"><strong>Why this is correct:</strong> A main effect examines the effect of ONE independent variable by itself, averaging across (ignoring) all other independent variables in the design.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>B) Combined effects of two DVs:</strong> Factorial ANOVA has only one DV. This describes multivariate analysis.</li>
        <li><strong>C) Effect of one level:</strong> Main effects compare across all levels of the IV, not just one level.</li>
        <li><strong>D) Combined effects of two IVs:</strong> This describes an interaction, not a main effect.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 3: Main Effects for the definition.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 2:</strong> The owners of the Syfy channel are interested in whether watching the Syfy channel causes people to become "geeky," and if so, whether any such effects depend on a person's gender. They hire a researcher to design and carry out the appropriate study. The researcher randomly assigns an equal number of men and women to watch 0, 3, 5, or 9 hours of the Syfy channel each week for 6 weeks. What is the research hypothesis for the main effect of hours watched?</p>
    <div class="options">
      <p>A) On average, watchers are equally geeky regardless of the hours of the Syfy channel they watch.</p>
      <p>B) On average, men are geekier than women when watching fewer hours but less geeky than women when watching more hours of the Syfy channel.</p>
      <p>C) On average, watchers differ in their geekiness levels across the various hours of the Syfy channel watched.</p>
      <p>D) On average, men and women differ in their geekiness levels.</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> C) On average, watchers differ in their geekiness levels across the various hours of the Syfy channel watched.</p>

      <p class="explanation"><strong>Why this is correct:</strong> The research hypothesis for a main effect predicts that there will be differences across the levels of that factor (hours watched), averaging across the other factor (gender). This statement says geekiness differs across hours watched.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Equally geeky regardless of hours:</strong> This is the NULL hypothesis, not the research (alternative) hypothesis.</li>
        <li><strong>B) Men vs women pattern:</strong> This describes an interaction between gender and hours, not the main effect of hours.</li>
        <li><strong>D) Men and women differ:</strong> This is the research hypothesis for the main effect of GENDER, not hours watched.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Main effect hypotheses focus on one factor at a time, averaging across all other factors.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 3:</strong> Based on the ANOVA results below showing Religious affiliation has F = 70.285, p < .001, what is the correct description of the main effect of "Religious"?</p>
    <div class="options">
      <p>A) Schools with religious affiliations have significantly higher percentages of graduates going to college, compared to schools without religious affiliation.</p>
      <p>B) There is no significant difference in percentage of graduates going to college between schools with religious affiliations and schools without religious affiliations.</p>
      <p>C) Schools with religious affiliations have significantly lower percentages of graduates going to college, compared to schools without religious affiliation.</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> A) Schools with religious affiliations have significantly higher percentages of graduates going to college, compared to schools without religious affiliation.</p>

      <p class="explanation"><strong>Why this is correct:</strong> The main effect is significant (p < .001), so there IS a difference. Based on typical patterns in such data and the need to describe the direction, religious schools have higher college-going rates. You would confirm the direction by examining the marginal means.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>B) No significant difference:</strong> The p < .001 indicates a highly significant difference exists.</li>
        <li><strong>C) Religious schools lower:</strong> This has the direction backwards based on typical educational patterns and marginal means.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 3: Main Effects for interpreting significant main effects.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 4:</strong> Based on the ANOVA results showing Community type has F = 106.736, p < .001, what is the correct description of the main effect of "Community"?</p>
    <div class="options">
      <p>A) Suburban schools have significantly lower percentages of graduates going to college compared to city schools.</p>
      <p>B) There is no significant difference in percentage of graduates going to college between city schools and suburban schools.</p>
      <p>C) Suburban schools have significantly higher percentages of graduates going to college compared to city schools.</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> C) Suburban schools have significantly higher percentages of graduates going to college compared to city schools.</p>

      <p class="explanation"><strong>Why this is correct:</strong> The main effect is significant (p < .001), so there IS a difference. Based on typical socioeconomic patterns, suburban schools generally have higher college-going rates than city schools. You would confirm by examining the marginal means.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Suburban lower than city:</strong> This has the direction backwards.</li>
        <li><strong>B) No significant difference:</strong> The p < .001 indicates a highly significant difference exists.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Always check the marginal means to determine the direction of a significant main effect.</p>
    </div>

  </details>
</div>

---

## Part 4: Interaction Effects - The Heart of Factorial ANOVA

### What is an Interaction?

An **interaction effect** occurs when **the effect of one independent variable depends on the level of another independent variable**.

**Formal Definition:** An interaction exists when the effect of Factor A is **not the same** at all levels of Factor B (or vice versa).

**Simple Way to Think About It:**

- Do the two factors work together in a special way?
- Does the effect of one factor change depending on the other factor?
- Is the pattern different for different groups?

### Why Interactions Are the Most Important Finding

**THE GOLDEN RULE:** In factorial ANOVA, **the interaction is almost always the most interesting and important finding**.

**Why?**

1. **Interactions reveal complexity:** They show how the real world works
2. **Interactions are more informative:** They tell you when and for whom an effect occurs
3. **Interactions change interpretation:** A significant interaction can make main effects misleading

**Critical Point:** If you have a significant interaction, **you must interpret it carefully** and be cautious about interpreting main effects.

### Examples of Interactions

**Example 1: Teaching Method × Student Level**

**No Interaction:**

- Hands-on is better than lecture for BOTH beginners and advanced students
- The difference is the same for both groups
- Effect of teaching method does NOT depend on student level

**Interaction Present:**

- Hands-on is much better for beginners, but lecture is better for advanced students
- The effect of teaching method DOES depend on student level
- The pattern reverses across groups

**Example 2: Drug Dosage × Age**

**No Interaction:**

- Higher doses work better for both young and elderly patients
- The pattern is the same for both age groups

**Interaction Present:**

- Higher doses work better for young patients, but lower doses work better for elderly
- The optimal dosage depends on age
- What works for one group doesn't work for the other

**Example 3: Study Location × Gender**

**No Interaction:**

- Library is best for both males and females
- The rank order of locations is the same for both genders

**Interaction Present:**

- Library is best for females, but home is best for males
- The best study location depends on gender
- You can't give one recommendation for everyone

### Visualizing Interactions with Line Graphs

Interaction plots show the dependent variable on the Y-axis, one factor on the X-axis, and separate lines for each level of the other factor.

**No Interaction Pattern (Parallel Lines):**

Imagine a graph where:
- X-axis shows Teaching Method: Lecture → Hands-on
- Y-axis shows Test Scores (0-100)
- Two lines: one for Males (solid), one for Females (dashed)

```
Both lines rise from left to right at the SAME angle:
  Males: 40 → 60 (increase of 20 points)
  Females: 80 → 100 (increase of 20 points)

The lines stay parallel and never meet.
```

**What this means:** Hands-on is better than lecture for BOTH groups by the same amount (20 points). The effect of teaching method doesn't depend on gender.

---

**Interaction Pattern (Non-Parallel Lines):**

Imagine a graph where:
- X-axis shows Teaching Method: Lecture → Hands-on
- Y-axis shows Test Scores (0-100)
- Two lines: one for Males (solid), one for Females (dashed)

```
Lines move in opposite directions and CROSS:
  Males: 60 → 40 (decrease of 20 points)
  Females: 80 → 100 (increase of 20 points)

The lines intersect in the middle of the graph.
```

**What this means:** The effect of teaching method DEPENDS on gender. Females benefit from hands-on while males do worse. Males do better with lecture.

---

**Key Visual Cues:**

- **Parallel lines** = No interaction (consistent effect across groups)
- **Non-parallel lines** = Possible interaction (effect varies by group)
- **Crossing lines** = Definite interaction (effect reverses across groups)

### Types of Interactions

**1. Crossover Interaction:**

- The lines actually cross
- The rank order reverses
- Example: Drug A is best for young, Drug B is best for elderly

**2. Spreading Interaction:**

- Lines diverge but don't cross
- One factor has a bigger effect at certain levels of the other factor
- Example: Hands-on helps beginners much more than it helps advanced students

**3. No Interaction:**

- Lines are parallel (or close to it)
- One factor has the same effect at all levels of the other factor

### Hypotheses for Interaction Effects

**Null Hypothesis (H₀):**

- There is no interaction between Factor A and Factor B
- The effect of Factor A is the same at all levels of Factor B
- The lines on the graph will be parallel

**Alternative Hypothesis (H₁):**

- There is an interaction between Factor A and Factor B
- The effect of Factor A depends on the level of Factor B
- The lines on the graph will not be parallel

### What a Significant Interaction Tells You

**If the interaction is significant (p < .05):**

- ✅ The effect of one factor **depends on** the level of the other factor
- ✅ You **cannot** make simple statements about main effects
- ✅ You **must** explore the interaction with simple effects tests
- ✅ This is your **main story** to report

**Example Interpretation:**
"The effect of teaching method on test scores depends on student level. Hands-on instruction is more effective for beginners, while lecture is more effective for advanced students."

<div class="common-mistakes">
  <h4>⚠️ Common Mistakes with Interactions</h4>
  <ul>
    <li><strong>Mistake 1:</strong> Thinking non-parallel lines always mean a significant interaction. Lines must be NON-PARALLEL ENOUGH for statistical significance. Always check the p-value!</li>
    <li><strong>Mistake 2:</strong> Ignoring the interaction when it's significant and only reporting main effects. The interaction is usually your most important finding.</li>
    <li><strong>Mistake 3:</strong> Confusing "no main effect" with "no interaction." These are independent - you can have an interaction without main effects.</li>
    <li><strong>Mistake 4:</strong> Saying "Factor A and Factor B interact" without explaining WHAT the interaction means. Always describe the pattern in plain language.</li>
  </ul>
</div>

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Interaction Effects</h4>

  <div class="quiz-question">
    <p><strong>Question 1:</strong> An interaction occurs when _____.</p>
    <div class="options">
      <p>A) Two independent variables both influence the dependent variable</p>
      <p>B) The effects of one independent variable depend on the level of the other independent variable</p>
      <p>C) A single independent variable changes the dependent variable, disregarding all other variables in the study</p>
      <p>D) The dependent variable does not depend on any of the independent variables</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) The effects of one independent variable depend on the level of the other independent variable</p>

      <p class="explanation"><strong>Why this is correct:</strong> An interaction means that the effect of one IV changes depending on which level of the other IV you're looking at. The two factors work together in a way that can't be explained by their individual main effects alone.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Both influence the DV:</strong> This describes having two significant main effects, not an interaction.</li>
        <li><strong>C) Single IV changes DV:</strong> This describes a main effect, not an interaction.</li>
        <li><strong>D) DV doesn't depend on IVs:</strong> This describes a non-significant result, not an interaction.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 4: Interaction Effects for the definition.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 2:</strong> In addition to assessing whether each independent variable has an effect on the dependent variable, a factorial ANOVA also allows one to _____.</p>
    <div class="options">
      <p>A) Use multiple dependent measures in a single analysis</p>
      <p>B) Determine whether the effects of one factor depend on the other factor</p>
      <p>C) Control for a third variable that might be related to the dependent measure, prior to investigating the independent variable of interest</p>
      <p>D) Partition out the variability due to individual differences and the variability due to measurement error</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) Determine whether the effects of one factor depend on the other factor</p>

      <p class="explanation"><strong>Why this is correct:</strong> The key advantage of factorial ANOVA over one-way ANOVA is the ability to test for interactions—whether the effect of one factor depends on (varies with) the level of the other factor.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Multiple DVs:</strong> Factorial ANOVA has one DV. Multiple DVs would require MANOVA (multivariate ANOVA).</li>
        <li><strong>C) Control for third variable:</strong> This describes ANCOVA (analysis of covariance), not factorial ANOVA.</li>
        <li><strong>D) Partition individual differences:</strong> This better describes repeated-measures designs, not the unique feature of factorial ANOVA.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> The power of factorial ANOVA is detecting interactions, which reveal how factors work together.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 3:</strong> Based on a 2×2 factorial ANOVA on teacher salary with factors of gender (male vs female) and community type (suburban vs rural), if the interaction is significant, what does this tell us?</p>
    <div class="options">
      <p>A) The gender discrepancy in teacher salary varies between suburban and rural schools.</p>
      <p>B) Teacher salary differs significantly between suburban and rural schools.</p>
      <p>C) Teacher salary differs significantly between male and female teachers.</p>
      <p>D) The effect of community type on teacher salary depends on gender.</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> A) The gender discrepancy in teacher salary varies between suburban and rural schools. (Also D is correct)</p>

      <p class="explanation"><strong>Why this is correct:</strong> A significant interaction means the difference between males and females (the gender effect) is not the same in suburban vs. rural schools. Both A and D describe this interaction correctly—they're just phrased differently.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>B) Salary differs by community:</strong> This describes the main effect of community type, not the interaction.</li>
        <li><strong>C) Salary differs by gender:</strong> This describes the main effect of gender, not the interaction.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 4: Interaction Effects for interpreting interactions.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 4:</strong> If the interaction between Religious affiliation and Community type is significant (p < .05), what does this tell us?</p>
    <div class="options">
      <p>A) Religious affiliation has no effect on college-going rates</p>
      <p>B) Community type has no effect on college-going rates</p>
      <p>C) The effect of religious affiliation on college-going rates depends on whether the school is in a city or suburb</p>
      <p>D) Both factors independently affect college-going rates</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> C) The effect of religious affiliation on college-going rates depends on whether the school is in a city or suburb</p>

      <p class="explanation"><strong>Why this is correct:</strong> A significant interaction means the two factors work together—the effect of one factor (religious affiliation) is not the same at all levels of the other factor (community type).</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Religious affiliation has no effect:</strong> The interaction being significant doesn't mean no effect—it means the effect varies.</li>
        <li><strong>B) Community has no effect:</strong> Same issue as A.</li>
        <li><strong>D) Both factors independently affect:</strong> This describes main effects without interaction. The interaction means they DON'T work independently.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> A significant interaction means you cannot interpret the factors as working independently.</p>
    </div>

  </details>
</div>

---

## Part 5: The Omnibus Test in Two-Way ANOVA

### Three Separate Null Hypotheses

In a two-way ANOVA, the **omnibus test** actually tests **three separate null hypotheses simultaneously**:

**H₀₁: Main Effect of Factor A**

- μ_A1 = μ_A2 = μ_A3... (all marginal means for Factor A are equal)
- Example: μ_city = μ_suburb

**H₀₂: Main Effect of Factor B**

- μ_B1 = μ_B2 = μ_B3... (all marginal means for Factor B are equal)
- Example: μ_religious = μ_non-religious

**H₀₃: Interaction Between A and B**

- There is no interaction between Factor A and Factor B
- The effect of Factor A is the same at all levels of Factor B

**Important:** Each of these three hypotheses is tested with its own **separate F-test**, meaning you get three F-statistics in your output.

### In a Two-Way ANOVA, the Researcher Makes Decisions Regarding...

**Answer:** Three separate null hypotheses

This is a critical concept that distinguishes two-way ANOVA from simpler tests:

- One-way ANOVA: 1 null hypothesis (one factor)
- Independent t-test: 1 null hypothesis (two groups)
- Two-way ANOVA: **3 null hypotheses** (2 main effects + 1 interaction)

### Variance Partitioning in Factorial ANOVA

In one-way ANOVA, we partitioned variance into:

- Between-groups variance
- Within-groups variance

**In two-way ANOVA, between-groups variance is further divided into THREE components:**

**Total Between-Groups Variance = Main Effect A + Main Effect B + Interaction (A×B)**

This is why factorial ANOVA is so powerful—it breaks down the differences among groups into interpretable pieces:

1. How much is due to Factor A alone?
2. How much is due to Factor B alone?
3. How much is due to the combination/interaction of A and B?

**Visual Representation:**

```
Total Variance in DV
    |
    ├─ Between-Groups Variance
    |    ├─ Main Effect of A
    |    ├─ Main Effect of B
    |    └─ Interaction (A × B)
    |
    └─ Within-Groups Variance (Error)
```

### Understanding Degrees of Freedom in Factorial ANOVA

**Degrees of freedom** become more complex in factorial designs because we're testing multiple effects.

**Between-Groups Degrees of Freedom:**

**df for Main Effect A:**

- df_A = a - 1
- Where a = number of levels of Factor A
- Example: 2 community types → df = 2 - 1 = 1

**df for Main Effect B:**

- df_B = b - 1
- Where b = number of levels of Factor B
- Example: 2 religious affiliations → df = 2 - 1 = 1

**df for Interaction (A × B):**

- df_A×B = (a - 1) × (b - 1)
- Example: (2-1) × (2-1) = 1 × 1 = 1

**Within-Groups Degrees of Freedom:**

**df for Within-Groups (Error):**

- df_within = N - (a × b)
- Where N = total number of participants, a × b = total number of cells
- Alternative formula: Subtract 1 participant from each cell, then add up
- Example: 60 participants, 2×2 design (4 cells) → df = 60 - 4 = 56

**Total Degrees of Freedom:**

- df_total = N - 1
- Example: 60 participants → df = 60 - 1 = 59

**Check:** df_A + df_B + df_A×B + df_within = df_total

- Example: 1 + 1 + 1 + 56 = 59 ✓

### Worked Example: Calculating Degrees of Freedom

**Research Scenario:**
A researcher conducts a 3×2 factorial ANOVA examining the effects of study method (flashcards, practice tests, re-reading) and study time (1 hour vs. 3 hours) on exam scores. There are 60 total participants with 10 participants per cell.

**Step 1: Identify the design**
- Factor A (Study Method): 3 levels (a = 3)
- Factor B (Study Time): 2 levels (b = 2)
- Total N = 60
- Number of cells = 3 × 2 = 6 cells
- Participants per cell = 10

**Step 2: Calculate df for Main Effect A (Study Method)**
- df_A = a - 1 = 3 - 1 = **2**

**Step 3: Calculate df for Main Effect B (Study Time)**
- df_B = b - 1 = 2 - 1 = **1**

**Step 4: Calculate df for Interaction (A×B)**
- df_A×B = (a - 1) × (b - 1) = (3 - 1) × (2 - 1) = 2 × 1 = **2**

**Step 5: Calculate df for Within-Groups (Error)**
- df_within = N - (a × b) = 60 - (3 × 2) = 60 - 6 = **54**
- Alternative: (10-1) + (10-1) + (10-1) + (10-1) + (10-1) + (10-1) = 9×6 = 54 ✓

**Step 6: Calculate df for Total**
- df_total = N - 1 = 60 - 1 = **59**

**Step 7: Verify the calculations**
- df_A + df_B + df_A×B + df_within = df_total
- 2 + 1 + 2 + 54 = 59 ✓

**How to report in APA format:**
- Main effect of Study Method: F(2, 54) = ...
- Main effect of Study Time: F(1, 54) = ...
- Interaction: F(2, 54) = ...

---

### Reading the SPSS Output Table

SPSS produces a "Tests of Between-Subjects Effects" table that looks like this:

```
Tests of Between-Subjects Effects
Dependent Variable: Pcollege

Source                     Type III SS    df    Mean Square    F        Sig.    Partial η²
Corrected Model           24255.640      3     8085.213       68.502   .000    .780
Intercept                 285120.000     1     285120.000     2416.00  .000    .977
Community                 12600.840      1     12600.840      106.736  .000    .656
Religious                 8294.400       1     8294.400       70.285   .000    .557
Community * Religious     3360.400       1     3360.400       28.476   .000    .330
Error                     6616.320       56    118.113
Total                     316000.000     60
Corrected Total           30871.960      59
```

**Key Information to Extract:**

**1. Omnibus F-statistic** (Corrected Model row):

- F = 68.502
- This tests whether the overall model (all three effects combined) is significant
- df = (3, 56)

**2. Main Effect of Community:**

- F = 106.736, df = (1, 56), p < .001
- Significant main effect

**3. Main Effect of Religious:**

- F = 70.285, df = (1, 56), p < .001
- Significant main effect

**4. Interaction (Community × Religious):**

- F = 28.476 (or sometimes labeled as 35.616 in some outputs), df = (1, 56), p < .001
- Significant interaction

**5. Error (Within-Groups):**

- MS_error = 118.113
- df = 56

### Extracting Exact F-Statistics from SPSS

**Critical SPSS Skill:** You must be able to extract the exact F-values for:

1. **Omnibus test** (Corrected Model row)
2. **Main effect of Factor A** (first IV row)
3. **Main effect of Factor B** (second IV row)
4. **Interaction** (IV1 × IV2 row)

**Tip:** SPSS provides many decimal places—use all of them when reporting F-statistics in assignments.

### Example: Interpreting SPSS Output Step-by-Step

**Scenario:** You run a 2×2 ANOVA on college-going rates with Community (city, suburb) and Religious affiliation (yes, no).

**Your SPSS Output Table:**

| Source | Type III SS | df | Mean Square | F | Sig. | Partial η² |
|--------|------------|-----|-------------|---------|------|------------|
| Corrected Model | 24255.640 | 3 | 8085.213 | 68.502 | <.001 | .786 |
| Intercept | 285120.000 | 1 | 285120.000 | 2416.00 | <.001 | .977 |
| Community | 12600.840 | 1 | 12600.840 | 106.736 | <.001 | .656 |
| Religious | 8294.400 | 1 | 8294.400 | 70.285 | <.001 | .557 |
| Community * Religious | 3360.400 | 1 | 3360.400 | 28.476 | <.001 | .337 |
| Error | 6616.320 | 56 | 118.113 | | | |
| Total | 316000.000 | 60 | | | | |
| Corrected Total | 30871.960 | 59 | | | | |

**Step-by-Step Interpretation:**

**Step 1: Check the Omnibus Test (Corrected Model)**
- F(3, 56) = 68.502, p < .001, partial η² = .786
- ✓ Model is significant - at least one effect is significant
- ✓ Model explains 78.6% of variance (very strong!)

**Step 2: Check the Interaction FIRST**
- Community × Religious: F(1, 56) = 28.476, p < .001, partial η² = .337
- ✓ Interaction IS significant - this is your main story!
- ✓ Large effect size (33.7% of variance)

**Step 3: Note the Main Effects (but interpret cautiously)**
- Community: F(1, 56) = 106.736, p < .001, partial η² = .656 (significant)
- Religious: F(1, 56) = 70.285, p < .001, partial η² = .557 (significant)
- ⚠️ Both significant, but must interpret in light of the interaction

**Step 4: Next Steps**
- Because interaction is significant → Run SIMPLE EFFECTS tests
- Split by Community and test effect of Religious in each
- This will reveal the pattern of the interaction

**Step 5: Check Levene's Test (in different table)**
- If p > .05 → Assumption of homogeneity met ✓
- If p < .05 → Assumption violated, note in write-up

---

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Omnibus Test and Variance Partitioning</h4>

  <div class="quiz-question">
    <p><strong>Question 1:</strong> In a two-way ANOVA, the researcher makes decisions regarding _____ when the omnibus test is significant.</p>
    <div class="options">
      <p>A) Three separate null hypotheses</p>
      <p>B) Four separate null hypotheses</p>
      <p>C) One null hypothesis and one alternative hypothesis</p>
      <p>D) Two separate null hypotheses</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> A) Three separate null hypotheses</p>

      <p class="explanation"><strong>Why this is correct:</strong> A two-way ANOVA tests three separate null hypotheses: (1) Main effect of Factor A, (2) Main effect of Factor B, and (3) Interaction between A and B. Each has its own F-test.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>B) Four separate hypotheses:</strong> Only three effects are tested in a two-way ANOVA.</li>
        <li><strong>C) One null and one alternative:</strong> This describes a simpler test like a t-test, not factorial ANOVA.</li>
        <li><strong>D) Two separate hypotheses:</strong> This misses the interaction—there are three separate tests.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 5: The Omnibus Test for the three null hypotheses.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 2:</strong> In a two-way factorial ANOVA, between-groups variance is divided into _____.</p>
    <div class="options">
      <p>A) Two main effects and two interactions</p>
      <p>B) One main effect and a single interaction</p>
      <p>C) Two main effects and a single interaction</p>
      <p>D) One main effect and two interactions</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> C) Two main effects and a single interaction</p>

      <p class="explanation"><strong>Why this is correct:</strong> Between-groups variance in a two-way ANOVA is partitioned into three components: Main effect of Factor A, Main effect of Factor B, and the A×B interaction. That's two main effects plus one interaction.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Two main effects and two interactions:</strong> A two-way ANOVA has only one interaction (A×B).</li>
        <li><strong>B) One main effect and one interaction:</strong> There are two main effects (one for each factor).</li>
        <li><strong>D) One main effect and two interactions:</strong> There are two main effects and only one interaction.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Always remember: 2 factors = 2 main effects + 1 interaction.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 3:</strong> Looking at SPSS output, you see F = 68.502 in the "Corrected Model" row. What is this F-statistic testing?</p>
    <div class="options">
      <p>A) Only the main effect of Factor A</p>
      <p>B) Only the interaction effect</p>
      <p>C) The overall significance of the entire model (all three effects combined)</p>
      <p>D) Only the main effect of Factor B</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> C) The overall significance of the entire model (all three effects combined)</p>

      <p class="explanation"><strong>Why this is correct:</strong> The "Corrected Model" row provides the omnibus F-test, which tests whether the overall model (combining both main effects and the interaction) is significant. It tells you if there's any significant variation explained by your factors.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A, B, D) Only one effect:</strong> The Corrected Model tests all effects together, not individual effects. Individual effects have their own rows.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 5: The Omnibus Test for reading SPSS output.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 4:</strong> Based on the SPSS output showing Community (F = 106.736), Religious (F = 70.285), and Community × Religious (F = 35.616), which F-statistic represents the interaction effect?</p>
    <div class="options">
      <p>A) 106.736</p>
      <p>B) 70.285</p>
      <p>C) 35.616</p>
      <p>D) 68.502</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> C) 35.616</p>

      <p class="explanation"><strong>Why this is correct:</strong> The interaction is labeled as "Community × Religious" or "Community * Religious" in SPSS output. The asterisk (*) or × symbol indicates an interaction between the two factors.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) 106.736:</strong> This is the F-statistic for the main effect of Community.</li>
        <li><strong>B) 70.285:</strong> This is the F-statistic for the main effect of Religious.</li>
        <li><strong>D) 68.502:</strong> This is the omnibus F-statistic for the overall model.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Look for the "*" or "×" symbol in SPSS output to identify the interaction effect.</p>
    </div>

  </details>
</div>

---

## Part 5 (continued): Degrees of Freedom

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Degrees of Freedom</h4>

  <div class="quiz-question">
    <p><strong>Question 1:</strong> Within-groups degrees of freedom in a two-way ANOVA is calculated by _____.</p>
    <div class="options">
      <p>A) Multiplying together the degrees of freedom associated with each of the main effects</p>
      <p>B) Subtracting a single participant from each cell of the study and then adding the results for all the cells</p>
      <p>C) Subtracting the degrees of freedom for the first main effect from that of the second main effect</p>
      <p>D) Adding together the degrees of freedom associated with each of the main effects</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) Subtracting a single participant from each cell of the study and then adding the results for all the cells</p>

      <p class="explanation"><strong>Why this is correct:</strong> Within-groups df = (n₁-1) + (n₂-1) + ... + (nₖ-1), where each cell loses 1 df. This equals N - (number of cells). For a 2×2 design with 60 participants: df = 60 - 4 = 56.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Multiply main effects df:</strong> Multiplying gives you interaction df, not within-groups df.</li>
        <li><strong>C) Subtract main effects df:</strong> This operation doesn't match any df calculation in factorial ANOVA.</li>
        <li><strong>D) Add main effects df:</strong> This doesn't give you within-groups df.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 5: Understanding Degrees of Freedom for the formulas.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 2:</strong> In a 2×2 factorial ANOVA on teacher salary with factors of gender and community type, what are the degrees of freedom for reporting the gender × community interaction effect (given N = 62 total participants)?</p>
    <div class="options">
      <p>A) 3, 58</p>
      <p>B) 1, 62</p>
      <p>C) 1, 58</p>
      <p>D) 3, 62</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> C) 1, 58</p>

      <p class="explanation"><strong>Why this is correct:</strong> Interaction df = (a-1) × (b-1) = (2-1) × (2-1) = 1. Within-groups df = N - (a × b) = 62 - 4 = 58. So the interaction is reported as F(1, 58).</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) 3, 58:</strong> df₁ = 3 would be for a 2×3 or 4×1 design, not 2×2.</li>
        <li><strong>B) 1, 62:</strong> The within-groups df should be 62 - 4 cells = 58, not 62.</li>
        <li><strong>D) 3, 62:</strong> Wrong on both—interaction df should be 1, and within should be 58.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> For a 2×2 design, interaction df is always (2-1)×(2-1) = 1.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 3:</strong> In a 3×2 factorial design with 60 total participants, what are the degrees of freedom for the main effect of the factor with 3 levels?</p>
    <div class="options">
      <p>A) 2</p>
      <p>B) 1</p>
      <p>C) 3</p>
      <p>D) 5</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> A) 2</p>

      <p class="explanation"><strong>Why this is correct:</strong> Main effect df = levels - 1 = 3 - 1 = 2. The number of participants doesn't affect the df for the main effect, only the number of levels does.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>B) 1:</strong> This would be the df for the factor with 2 levels, not 3.</li>
        <li><strong>C) 3:</strong> You must subtract 1 from the number of levels.</li>
        <li><strong>D) 5:</strong> This doesn't correspond to any df calculation for this design.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 5: Understanding Degrees of Freedom for main effect df calculations.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 4:</strong> In a 2×3 design, what is the df for the interaction?</p>
    <div class="options">
      <p>A) 5</p>
      <p>B) 3</p>
      <p>C) 2</p>
      <p>D) 1</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> C) 2</p>

      <p class="explanation"><strong>Why this is correct:</strong> Interaction df = (a-1) × (b-1) = (2-1) × (3-1) = 1 × 2 = 2.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) 5:</strong> This would be 2 + 3, but we multiply (2-1) and (3-1), not add the levels.</li>
        <li><strong>B) 3:</strong> This would be if one factor had 4 levels in a 2×4 design.</li>
        <li><strong>D) 1:</strong> This would be correct for a 2×2 design, not 2×3.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Interaction df = (levels₁ - 1) × (levels₂ - 1).</p>
    </div>

  </details>
</div>

---

## Part 6: The Decision Tree - Interpreting Factorial ANOVA Results

### The Golden Rule: Check the Interaction FIRST

**Most Important Principle in Factorial ANOVA:**
When interpreting your results, **ALWAYS examine the interaction effect before looking at the main effects.**

**Why?**

- The interaction tells you whether the main effects can be interpreted independently
- A significant interaction changes how you interpret everything else
- The interaction is usually the most interesting and informative finding

### The Decision Tree

```
Step 1: Look at the Interaction (A × B)
    |
    ├─ Is interaction significant (p < .05)?
    |    |
    |    ├─ YES → Interaction is SIGNIFICANT
    |    |    |
    |    |    ├─ 1. Report the significant interaction as your main finding
    |    |    ├─ 2. Run SIMPLE EFFECTS tests to explore the interaction
    |    |    ├─ 3. Interpret main effects with EXTREME CAUTION (or ignore them)
    |    |    └─ 4. Focus on describing the pattern of the interaction
    |    |
    |    └─ NO → Interaction is NOT SIGNIFICANT
    |         |
    |         ├─ 1. Report that the interaction is not significant
    |         ├─ 2. NOW you can interpret main effects independently
    |         └─ 3. For each significant main effect:
    |              |
    |              ├─ If factor has 2 levels → Compare marginal means
    |              └─ If factor has 3+ levels → Run POST-HOC tests
```

### When the Interaction is Significant

**What this means:**

- The effect of Factor A depends on the level of Factor B
- You cannot make simple statements like "Factor A increases the DV"
- The two factors work together in a complex way

**What to do:**

1. **Report the interaction:** "There was a significant interaction between A and B, F(1, 56) = 35.62, p < .001."

2. **Run simple effects tests:** Break down your data by levels of one factor and test the effect of the other factor separately at each level

3. **Describe the pattern:** Explain how the effect of one factor changes across levels of the other

4. **Be cautious with main effects:** If you report them at all, note that they must be interpreted in light of the significant interaction

**Example Interpretation:**
"The effect of religious affiliation on college-going rates depends on community type. In city schools, religious affiliation had a large significant effect (p < .001), but in suburban schools, the effect was not significant (p = .45)."

### When the Interaction is NOT Significant

**What this means:**

- The effect of Factor A is consistent across all levels of Factor B
- The two factors work independently
- Main effects can be interpreted separately

**What to do:**

1. **Report that interaction is not significant:** "There was no significant interaction, F(1, 56) = 0.85, p = .36."

2. **Interpret each main effect separately:**
   - For each significant main effect with 2 levels: Compare marginal means
   - For each significant main effect with 3+ levels: Run post-hoc tests

**Example Interpretation:**
"There was no significant interaction. The main effect of community type was significant, F(1, 56) = 106.74, p < .001, with suburban schools having higher rates than city schools. The main effect of religious affiliation was also significant, F(1, 56) = 70.29, p < .001, with religious schools having higher rates than non-religious schools."

### When to Run Post-Hoc Tests

**Post-hoc tests are needed when:**

- The interaction is **NOT significant**, AND
- A main effect is **significant**, AND
- That factor has **3 or more levels**

**When post-hoc tests are NOT needed:**

- Interaction is significant (run simple effects tests instead)
- Main effect has only 2 levels (just compare marginal means)
- Main effect is not significant

**Example from Quiz:**
Based on ANOVA results showing:

- Community effect: F = 106.74, p < .001 (2 levels: city, suburb)
- Religious effect: F = 70.29, p < .001 (2 levels: yes, no)
- Interaction: F = 35.62, p < .001

**Answer: Post hoc tests are not necessary**

**Why?** The interaction is significant, so you should run simple effects tests instead. Even if the interaction weren't significant, both main effects have only 2 levels each, so no post-hoc tests would be needed—just compare the two marginal means for each factor.

### Caution: Don't Over-Interpret Main Effects with Significant Interactions

**Common Mistake:**
Reporting "Religious schools have higher college-going rates" when there's a significant interaction.

**Problem:**
This statement might be true on average (the marginal means), but it hides the complexity revealed by the interaction.

**Better Approach:**
"The effect of religious affiliation depends on community type. In city schools, religious schools have much higher rates (85% vs. 60%), but in suburban schools, the difference is smaller (88% vs. 75%)."

<div class="common-mistakes">
  <h4>⚠️ Common Mistakes with the Decision Tree</h4>
  <ul>
    <li><strong>Mistake 1:</strong> Looking at main effects BEFORE checking the interaction. Always start with the interaction!</li>
    <li><strong>Mistake 2:</strong> Running post-hoc tests when you should run simple effects (or vice versa). Post-hoc = main effects with 3+ levels. Simple effects = significant interaction.</li>
    <li><strong>Mistake 3:</strong> Running post-hoc tests for a 2-level factor. With only 2 levels, just compare the two marginal means.</li>
    <li><strong>Mistake 4:</strong> Reporting main effects as the "answer" when there's a significant interaction. The interaction changes everything!</li>
  </ul>
</div>

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: The Decision Tree</h4>

  <div class="quiz-question">
    <p><strong>Question 1:</strong> Based on ANOVA results showing a significant interaction between CityRural and SchoolType (p < .001), but non-significant main effects for both factors (p > .05), what post hoc tests should be performed?</p>
    <div class="options">
      <p>A) Post hoc tests are not necessary</p>
      <p>B) Post hoc tests for the CityRural × SchoolType effect</p>
      <p>C) Post hoc tests for the SchoolType effect</p>
      <p>D) Post hoc tests for the CityRural effect</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> A) Post hoc tests are not necessary</p>

      <p class="explanation"><strong>Why this is correct:</strong> When the interaction is significant, you run SIMPLE EFFECTS tests, not post-hoc tests. Post-hoc tests are only used for significant main effects with 3+ levels when the interaction is NOT significant.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>B) Post hoc for interaction:</strong> You don't run post-hoc tests on interactions—you run simple effects tests.</li>
        <li><strong>C, D) Post hoc for main effects:</strong> The main effects aren't significant, and even if they were, the significant interaction means you should focus on simple effects tests.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 6: The Decision Tree for when to run post-hoc tests vs. simple effects tests.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 2:</strong> If the interaction is significant (p < .001), should you interpret the main effects?</p>
    <div class="options">
      <p>A) Yes, always interpret main effects regardless of the interaction</p>
      <p>B) No, completely ignore the main effects</p>
      <p>C) Interpret main effects with extreme caution, noting they must be understood in light of the interaction</p>
      <p>D) Only interpret the main effect if it's also significant</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> C) Interpret main effects with extreme caution, noting they must be understood in light of the interaction</p>

      <p class="explanation"><strong>Why this is correct:</strong> A significant interaction means the effect of one factor depends on the other. Main effects can still be reported, but you must emphasize that the interaction is the more complete story. Marginal means can be misleading when an interaction is present.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Always interpret normally:</strong> This ignores the critical information provided by the interaction.</li>
        <li><strong>B) Completely ignore:</strong> Too extreme—you can mention them but must emphasize the interaction.</li>
        <li><strong>D) Only if significant:</strong> Even significant main effects need careful interpretation when interaction is present.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Focus on the interaction when it's significant—it tells the more complete and nuanced story.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 3:</strong> You find F = 5.23, p = .028 for the interaction. What should you do next?</p>
    <div class="options">
      <p>A) Run post-hoc tests on the main effects</p>
      <p>B) Run simple effects tests to explore the interaction</p>
      <p>C) Report only the main effects and ignore the interaction</p>
      <p>D) Run another ANOVA to confirm the result</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) Run simple effects tests to explore the interaction</p>

      <p class="explanation"><strong>Why this is correct:</strong> p = .028 < .05, so the interaction is significant. When the interaction is significant, you must run simple effects tests to understand the pattern of the interaction.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Post-hoc on main effects:</strong> With a significant interaction, you run simple effects tests, not post-hoc tests.</li>
        <li><strong>C) Ignore interaction:</strong> The interaction is your most important finding and must be explored.</li>
        <li><strong>D) Run another ANOVA:</strong> No need to repeat the analysis—the result is already clear.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 6: The Decision Tree for the steps after finding a significant interaction.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 4:</strong> The interaction is NOT significant (p = .52). Factor A has 2 levels and is significant (p = .003). Factor B has 4 levels and is significant (p = .001). What should you do?</p>
    <div class="options">
      <p>A) Run post-hoc tests for both Factor A and Factor B</p>
      <p>B) Run post-hoc tests only for Factor B</p>
      <p>C) Run post-hoc tests only for Factor A</p>
      <p>D) No post-hoc tests are needed</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) Run post-hoc tests only for Factor B</p>

      <p class="explanation"><strong>Why this is correct:</strong> The interaction is not significant, so we can interpret main effects. Factor A has only 2 levels (just compare the two marginal means), but Factor B has 4 levels, so post-hoc tests are needed to determine which specific levels differ.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Post-hoc for both:</strong> Factor A only has 2 levels, so no post-hoc test is needed.</li>
        <li><strong>C) Post-hoc only for A:</strong> It's Factor B with 4 levels that needs post-hoc tests.</li>
        <li><strong>D) No post-hoc needed:</strong> Factor B has 4 levels and is significant, so post-hoc tests ARE needed.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Post-hoc tests are only needed for significant main effects with 3+ levels when the interaction is NOT significant.</p>
    </div>

  </details>
</div>

---

## Part 7: Simple Effects Tests

### What Are Simple Effects?

**Simple effects** are the effects of one factor at **individual levels** of the other factor.

**Example:**
Instead of asking "Does teaching method affect scores?" (main effect), we ask:

- "Does teaching method affect scores **for beginners**?" (simple effect at beginner level)
- "Does teaching method affect scores **for advanced students**?" (simple effect at advanced level)

**Purpose:** Simple effects tests help you understand and describe the pattern of a significant interaction.

### When to Run Simple Effects Tests

**Run simple effects tests when:**

- The interaction is **significant** (p < .05)
- You want to understand **how** the two factors interact

**Do NOT run simple effects tests when:**

- The interaction is **not significant**
- In that case, interpret main effects instead

### How Simple Effects Tests Work

**Approach 1: Split by Factor A, Test Effect of Factor B**

**Steps:**

1. Split your data into separate groups based on Factor A levels
2. For each level of Factor A, run a one-way ANOVA testing the effect of Factor B
3. Compare results across the different levels of Factor A

**Example:**

- Split data by Community Type (City schools only, Suburb schools only)
- For City schools: Run one-way ANOVA testing effect of Religious affiliation
- For Suburb schools: Run one-way ANOVA testing effect of Religious affiliation
- Compare: Is the effect of Religious different in City vs. Suburb?

**Approach 2: Split by Factor B, Test Effect of Factor A**

You could also do it the other way:

- Split data by Religious affiliation (Religious schools only, Non-religious schools only)
- Test effect of Community Type separately for each group

**Choose based on your research question and which makes more conceptual sense.**

### Interpreting Simple Effects Results

**Example Results:**

**City Schools:**

- Religious vs. Non-religious: F(1, 28) = 45.23, p < .001
- Religious schools: M = 85%, Non-religious: M = 60%
- **Large, significant effect of religious affiliation**

**Suburban Schools:**

- Religious vs. Non-religious: F(1, 28) = 2.15, p = .154
- Religious schools: M = 88%, Non-religious: M = 82%
- **No significant effect of religious affiliation**

**Interpretation:**
"The effect of religious affiliation on college-going rates depends on community type. In city schools, religious affiliation has a large significant effect (religious schools: 85%, non-religious: 60%), F(1, 28) = 45.23, p < .001, η² = .62. However, in suburban schools, there is no significant difference between religious and non-religious schools (88% vs. 82%), F(1, 28) = 2.15, p = .154."

### Simple Effects in SPSS

**Method: Split File and Run One-Way ANOVAs**

**Step 1: Split the data**

1. Data → Split File
2. Select "Organize output by groups"
3. Move the splitting variable (e.g., Community Type) to "Groups Based on"
4. Click OK

**Step 2: Run One-Way ANOVA**

1. Analyze → Compare Means → One-Way ANOVA
2. DV: College percentage
3. Factor: Religious affiliation
4. Click OK

**Result:** SPSS will run separate one-way ANOVAs for each level of Community Type

**Step 3: Turn off Split File**

1. Data → Split File
2. Select "Analyze all cases, do not create groups"
3. Click OK

### Describing the Interaction Pattern

After running simple effects tests, describe the pattern:

**Crossover Interaction:**
"The effect of teaching method reverses across student levels. For beginners, hands-on is better than lecture, but for advanced students, lecture is better than hands-on."

**Spreading Interaction:**
"Teaching method has a larger effect for beginners than for advanced students. Beginners benefit greatly from hands-on vs. lecture, but advanced students show minimal differences."

**One-Level-Only Interaction:**
"Religious affiliation significantly affects college-going rates in city schools but not in suburban schools."

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Simple Effects and Follow-Up Tests</h4>

  <div class="quiz-question">
    <p><strong>Question 1:</strong> As follow-up tests for the interaction effect, you split the data points by community type and then run a one-way ANOVA on Pcollege as DV and religious affiliation as factor. Which of the following is a correct description of the results if you find: City schools - F(1,28) = 45.23, p < .001, η² = .62; Suburb schools - F(1,28) = 0.58, p = .45, η² = .02?</p>
    <div class="options">
      <p>A) The effect of religious affiliation on Pcollege is significant in both city schools and suburban schools, but the effect size is larger in the city schools.</p>
      <p>B) The effect of religious affiliation on Pcollege is significant in both city schools and suburban schools, but the effect size is larger in the suburb schools.</p>
      <p>C) The effect of religious affiliation on Pcollege is significant in city schools but not in suburban schools.</p>
      <p>D) The effect of religious affiliation on Pcollege is significant in suburban schools but not in city schools.</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> C) The effect of religious affiliation on Pcollege is significant in city schools but not in suburban schools.</p>

      <p class="explanation"><strong>Why this is correct:</strong> For city schools, p < .001 (significant), but for suburb schools, p = .45 (not significant). The effect of religious affiliation is only significant in city schools.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Significant in both:</strong> Suburb schools show p = .45, which is not significant.</li>
        <li><strong>B) Significant in both, larger in suburbs:</strong> Wrong on both counts—not significant in suburbs, and effect size is larger in city (.62 vs. .02).</li>
        <li><strong>D) Significant in suburbs only:</strong> This is backwards—it's significant in city schools, not suburban.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 7: Simple Effects Tests for interpreting simple effects results.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 2:</strong> When should you run simple effects tests?</p>
    <div class="options">
      <p>A) Always, for every factorial ANOVA</p>
      <p>B) Only when the interaction is significant</p>
      <p>C) Only when the main effects are significant</p>
      <p>D) Only when the interaction is NOT significant</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) Only when the interaction is significant</p>

      <p class="explanation"><strong>Why this is correct:</strong> Simple effects tests are specifically designed to explore and understand significant interactions. They break down the interaction to show how the effect of one factor changes across levels of the other factor.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Always:</strong> You only need simple effects when there's an interaction to explain.</li>
        <li><strong>C) Only when main effects significant:</strong> Simple effects are about interactions, not main effects.</li>
        <li><strong>D) When interaction NOT significant:</strong> This is backwards—you run simple effects when interaction IS significant.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> Significant interaction → Simple effects tests. No interaction → Interpret main effects.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 3:</strong> What is a simple effect?</p>
    <div class="options">
      <p>A) The main effect of one factor averaged across all levels</p>
      <p>B) The effect of one factor at a specific level of another factor</p>
      <p>C) The interaction between two factors</p>
      <p>D) The omnibus test result</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) The effect of one factor at a specific level of another factor</p>

      <p class="explanation"><strong>Why this is correct:</strong> A simple effect examines the effect of one IV at just one specific level of the other IV, rather than averaging across all levels (which would be a main effect).</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Main effect averaged across all levels:</strong> This is the definition of a main effect, not a simple effect.</li>
        <li><strong>C) The interaction:</strong> Simple effects help explain the interaction but are not the same as the interaction itself.</li>
        <li><strong>D) Omnibus test:</strong> The omnibus test is the overall model test, not a simple effect.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 7: Simple Effects Tests for the definition.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 4:</strong> How do you run simple effects tests in SPSS?</p>
    <div class="options">
      <p>A) Use a special "Simple Effects" menu option</p>
      <p>B) Split the file by one factor, then run one-way ANOVA on the other factor</p>
      <p>C) Run post-hoc tests in the factorial ANOVA dialog</p>
      <p>D) Use the "Interaction" button in SPSS</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) Split the file by one factor, then run one-way ANOVA on the other factor</p>

      <p class="explanation"><strong>Why this is correct:</strong> The standard method for simple effects in SPSS is to use Data → Split File to separate by one factor, then run separate one-way ANOVAs testing the effect of the other factor at each level.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Special menu option:</strong> SPSS doesn't have a dedicated "Simple Effects" menu—you use Split File and One-Way ANOVA.</li>
        <li><strong>C) Post-hoc tests:</strong> Post-hoc tests are for main effects with 3+ levels, not for exploring interactions.</li>
        <li><strong>D) Interaction button:</strong> No such button exists in SPSS.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 7: Simple Effects in SPSS for the step-by-step procedure.</p>
    </div>

  </details>
</div>

---

## Part 8: Effect Size in Factorial ANOVA

### Why Effect Size Matters

Just like with other ANOVAs, statistical significance (p-value) doesn't tell you about **practical significance**. Effect sizes answer the question: "How much of the variance in the DV is explained by the IVs?"

### Effect Sizes for Each Effect

In factorial ANOVA, you can calculate effect sizes for:

1. Main effect of Factor A
2. Main effect of Factor B
3. Interaction effect (A × B)
4. Total model (all effects combined)

### Partial Eta Squared (Partial η²)

**Partial η²** is the most commonly reported effect size for factorial ANOVA.

**Formula for each effect:**

- Partial η² = SS_effect / (SS_effect + SS_error)

**Example from SPSS Output:**

```
Source                     SS          Partial η²
Community                 12600.840    .656
Religious                 8294.400     .557
Community * Religious     3360.400     .330
Error                     6616.320
```

**Interpretation:**

- Community: 65.6% of variance (after removing other effects)
- Religious: 55.7% of variance (after removing other effects)
- Interaction: 33.0% of variance (after removing other effects)

### Total R² (R-Squared)

**Total R²** tells you how much variance is explained by the **entire model** (all effects combined).

**Formula:**

- R² = SS_between_total / SS_total
- Where SS_between_total = SS_A + SS_B + SS_A×B

**Example Calculation:**

```
SS_Community = 12600.840
SS_Religious = 8294.400
SS_Interaction = 3360.400
SS_between_total = 12600.840 + 8294.400 + 3360.400 = 24255.640

SS_total = 30871.960

R² = 24255.640 / 30871.960 = .786 (78.6%)
```

**Interpretation:** The combined model (community type, religious affiliation, and their interaction) explains 78.6% of the variance in college-going rates.

### Worked Example: Calculating Effect Sizes

**Given SPSS Output:**

```
Source                     SS          df    MS          F        Sig.
Community                 12600.840    1     12600.840   106.74   <.001
Religious                 8294.400     1     8294.400    70.29    <.001
Community * Religious     3360.400     1     3360.400    28.48    <.001
Error                     6616.320     56    118.113
Corrected Total          30871.960    59
```

**Calculate Partial η² for Each Effect:**

**1. Partial η² for Community:**
- Formula: Partial η² = SS_Community / (SS_Community + SS_error)
- Calculation: 12600.840 / (12600.840 + 6616.320)
- = 12600.840 / 19217.160
- = **.656** (large effect - explains 65.6% of variance)

**2. Partial η² for Religious:**
- Formula: Partial η² = SS_Religious / (SS_Religious + SS_error)
- Calculation: 8294.400 / (8294.400 + 6616.320)
- = 8294.400 / 14910.720
- = **.556** (large effect - explains 55.6% of variance)

**3. Partial η² for Interaction:**
- Formula: Partial η² = SS_Interaction / (SS_Interaction + SS_error)
- Calculation: 3360.400 / (3360.400 + 6616.320)
- = 3360.400 / 9976.720
- = **.337** (large effect - explains 33.7% of variance)

**Calculate Total R² for the Model:**

**Total R²:**
- Formula: R² = SS_between_total / SS_total
- First, find SS_between_total = SS_Community + SS_Religious + SS_Interaction
- = 12600.840 + 8294.400 + 3360.400 = 24255.640
- Now: R² = 24255.640 / 30871.960
- = **.786** (78.6% of variance explained by entire model)

**Interpretation:**
All three effects show large effect sizes according to Cohen's guidelines (> .14). The overall model explains nearly 79% of the variance in college-going rates, indicating a very strong model.

---

### Cohen's Guidelines for η²

**Small effect:** η² = .01 (1% of variance)
**Medium effect:** η² = .06 (6% of variance)
**Large effect:** η² = .14 (14% of variance)

**Important:** These are general guidelines. Context matters!

### Reporting Effect Sizes

**Always report effect sizes alongside F-statistics:**

**Example:**
"There was a significant main effect of community type, F(1, 56) = 106.74, p < .001, partial η² = .656, indicating a large effect. There was also a significant interaction between community type and religious affiliation, F(1, 56) = 35.62, p < .001, partial η² = .330."

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Effect Size</h4>

  <div class="quiz-question">
    <p><strong>Question 1:</strong> How much of the variance in "college percentage" can be accounted for by the total between-group variance if SS_between_total = 24255.640 and SS_total = 30871.960?</p>
    <div class="options">
      <p>A) 3.8%</p>
      <p>B) 25.3%</p>
      <p>C) 20%</p>
      <p>D) 78.6%</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> D) 78.6%</p>

      <p class="explanation"><strong>Why this is correct:</strong> Total R² = SS_between_total / SS_total = 24255.640 / 30871.960 = .786 = 78.6%. This tells us that the model explains 78.6% of the variance in college-going percentage.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) 3.8%:</strong> This is way too small and doesn't match the calculation.</li>
        <li><strong>B) 25.3%:</strong> This would be if you calculated SS_total / SS_between (reversed).</li>
        <li><strong>C) 20%:</strong> This doesn't correspond to the correct calculation.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> R² = SS_between_total / SS_total tells you the proportion of variance explained by the entire model.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 2:</strong> If partial η² = .656 for the main effect of community type, how should this be interpreted?</p>
    <div class="options">
      <p>A) Small effect</p>
      <p>B) Medium effect</p>
      <p>C) Large effect</p>
      <p>D) Cannot determine without more information</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> C) Large effect</p>

      <p class="explanation"><strong>Why this is correct:</strong> partial η² = .656 means 65.6% of the variance is explained, which is far above the threshold for a large effect (.14 or 14%). This is a very large effect.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Small:</strong> Small is η² = .01, much smaller than .656.</li>
        <li><strong>B) Medium:</strong> Medium is η² = .06, much smaller than .656.</li>
        <li><strong>D) Cannot determine:</strong> We have enough information with Cohen's guidelines.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 8: Effect Size for Cohen's guidelines.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 3:</strong> What is the difference between partial η² and total R²?</p>
    <div class="options">
      <p>A) They are the same thing</p>
      <p>B) Partial η² is for individual effects, R² is for the entire model</p>
      <p>C) Partial η² is always smaller than R²</p>
      <p>D) R² cannot be used in factorial ANOVA</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) Partial η² is for individual effects, R² is for the entire model</p>

      <p class="explanation"><strong>Why this is correct:</strong> Partial η² tells you how much variance each individual effect explains (after removing other effects). Total R² tells you how much variance the entire model (all effects combined) explains.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Same thing:</strong> They measure different aspects of effect size.</li>
        <li><strong>C) Always smaller:</strong> Not necessarily true—partial η² can be larger than R² in some cases.</li>
        <li><strong>D) Cannot use R²:</strong> You can and should calculate R² for factorial ANOVA.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 8: Effect Size for the distinction between partial η² and R².</p>
    </div>

  </details>
</div>

---

## Part 9: Assumptions of Factorial ANOVA

### The Four Critical Assumptions

Like all statistical tests, factorial ANOVA has assumptions that must be reasonably met for results to be valid.

**Assumption 1: Independence of Observations**

- Each participant's score must be independent of all other participants
- Violated by: Related participants (siblings, couples), repeated measures, clustered data
- **How to check:** Consider your research design and data collection method
- **Most important assumption** - violations seriously compromise results

**Assumption 2: Normality**

- The dependent variable should be approximately normally distributed **within each cell**
- More important with small sample sizes (n < 30 per cell)
- ANOVA is robust to mild violations, especially with equal cell sizes
- **How to check in SPSS:**
  - Run Analyze → Descriptive Statistics → Explore
  - Request histograms and Shapiro-Wilk test for each cell
  - Look for extreme skewness (±2) or kurtosis (±7)

**Assumption 3: Homogeneity of Variance**

- Variance should be approximately equal across all cells
- Tested with Levene's test in SPSS output
- ANOVA is fairly robust if cell sizes are equal
- **How to check:** Levene's test in SPSS (p > .05 indicates assumption met)
- **Rule of thumb:** Largest cell SD should be < 2× smallest cell SD

**Assumption 4: No Significant Outliers**

- Extreme outliers can distort means and inflate variance
- **How to check in SPSS:**
  - Look at boxplots (values beyond 3× IQR)
  - Check standardized residuals (values > ±3.29 are concerning)

### What to Do When Assumptions Are Violated

**If Independence is Violated:**
- ⚠️ STOP - This is serious
- Consider multilevel modeling or repeated-measures ANOVA instead
- Cannot proceed with standard factorial ANOVA

**If Normality is Violated:**
- With n > 30 per cell: Probably okay (Central Limit Theorem)
- With smaller samples: Consider data transformation (log, square root)
- Alternative: Use non-parametric methods or bootstrapping

**If Homogeneity of Variance is Violated:**
- If cell sizes are equal (within 10%): Probably okay to proceed
- If cell sizes are unequal: Use Welch's correction or report robust statistics
- Consider reporting with caution and noting the violation

**If Outliers are Present:**
- Investigate: Data entry error? True extreme case?
- Options: Remove (if error), winsorize (cap at less extreme value), or transform data
- Always report how you handled outliers

### Unequal Cell Sizes

**The Problem:**
- Unequal cell sizes complicate interpretation and reduce power
- Main effects and interaction become harder to interpret
- SPSS uses Type III sums of squares to handle this, but it's not perfect

**What to Do:**
- Try to balance cell sizes at the design stage
- If unavoidable: Use Type III sums of squares (SPSS default)
- Report cell sizes in your write-up
- Be extra cautious interpreting results with highly unbalanced designs

---

## Part 10: SPSS Practical Guide

### Running Two-Way Between-Groups ANOVA in SPSS

**Step-by-Step Instructions:**

**Step 1: Prepare Your Data**

- Ensure both IVs are coded numerically (or as string variables)
- Ensure DV is continuous
- Each row represents one participant
- No missing values in key variables

**Step 2: Access the GLM Univariate Menu**

1. Click **Analyze** → **General Linear Model** → **Univariate**

**Step 3: Define Variables**

1. Move your **Dependent Variable** to the "Dependent Variable" box
2. Move your **Independent Variables** (Factors) to the "Fixed Factor(s)" box
   - Example: Move "Community" and "Religious" to Fixed Factors

**Step 4: Request Descriptive Statistics and Effect Sizes**

1. Click **Options**
2. Check **Descriptive statistics**
3. Check **Estimates of effect size**
4. Move your factors and interaction to "Display Means for" (optional, for marginal means)
5. Click **Continue**

**Step 5: Create Interaction Plots (Optional but Recommended)**

1. Click **Plots**
2. Move one IV to "Horizontal Axis"
3. Move the other IV to "Separate Lines"
4. Click **Add**
5. Click **Continue**

**Step 6: Run the Analysis**

1. Click **OK**

### Reading the SPSS Output

**1. Descriptive Statistics Table:**
Shows means and SDs for each cell

**2. Levene's Test:**

- Tests homogeneity of variances assumption
- p > .05 = assumption met

**3. Tests of Between-Subjects Effects:**

- **Corrected Model:** Omnibus F-test
- **Each IV:** Main effect F-tests
- **IV1 × IV2:** Interaction F-test
- **Error:** Within-groups variance

**4. Profile Plots (if requested):**

- Visual representation of interaction
- Non-parallel lines = potential interaction

### Common SPSS Issues

**Issue 1: "Fixed factors must be categorical"**

- Solution: Ensure your IVs are properly coded

**Issue 2: "Too many empty cells"**

- Solution: You need participants in every cell of the design

**Issue 3: "Levene's test is significant"**

- Solution: Report the violation; consider robust methods or transformations

### Creating Simple Effects Tests in SPSS

**Method: Split File**

**Step 1:**

1. **Data** → **Split File**
2. Select "Organize output by groups"
3. Move splitting variable to "Groups Based on"
4. Click **OK**

**Step 2:**

1. **Analyze** → **Compare Means** → **One-Way ANOVA**
2. Set DV and Factor
3. Click **OK**

**Step 3:**

1. **Data** → **Split File**
2. Select "Analyze all cases"
3. Click **OK**

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: SPSS Output and APA Reporting</h4>

  <div class="quiz-question">
    <p><strong>Question 1:</strong> In the SPSS output, you see F = 68.502 for the Corrected Model row. What does this represent?</p>
    <div class="options">
      <p>A) The omnibus F-test for the overall model</p>
      <p>B) The interaction F-test</p>
      <p>C) The main effect of Factor A</p>
      <p>D) The main effect of Factor B</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> A) The omnibus F-test for the overall model</p>

      <p class="explanation"><strong>Why this is correct:</strong> The "Corrected Model" row shows the omnibus F-test, which tests whether the entire model (all three effects combined) significantly explains variance in the DV.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>B, C, D) Individual effects:</strong> Individual effects (main effects and interaction) have their own separate rows in the output table.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 9: SPSS Practical Guide for reading output tables.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 2:</strong> What is the correct APA format to report a p-value of .000 from SPSS output?</p>
    <div class="options">
      <p>A) p = .000</p>
      <p>B) p < .001</p>
      <p>C) p < .05</p>
      <p>D) p < .01</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) p < .001</p>

      <p class="explanation"><strong>Why this is correct:</strong> When SPSS shows p = .000, it means p < .001 (the actual p-value is very small, not exactly zero). APA format requires reporting "p < .001" rather than "p = .000".</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) p = .000:</strong> You cannot have a p-value of exactly zero. Report as "p < .001".</li>
        <li><strong>C) p < .05:</strong> While technically true, "p < .001" is more precise and informative.</li>
        <li><strong>D) p < .01:</strong> While technically true, "p < .001" is more precise and shows the p-value is even smaller.</li>
      </ul>

      <p class="application-tip"><em>💡 Application Tip:</em> SPSS output showing .000 should always be reported as "p < .001" in APA format.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 3:</strong> What is the hypothesis test result from the omnibus test if F(3, 56) = 68.502, p < .001?</p>
    <div class="options">
      <p>A) The null hypothesis is not rejected, and the model is significant.</p>
      <p>B) The null hypothesis is not rejected and the model is not significant.</p>
      <p>C) The null hypothesis is rejected, and the model is not significant.</p>
      <p>D) The null hypothesis is rejected, and the model is significant.</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> D) The null hypothesis is rejected, and the model is significant.</p>

      <p class="explanation"><strong>Why this is correct:</strong> p < .001 means we reject the null hypothesis. When we reject the null, the model IS significant—meaning at least one of the effects (main effects or interaction) is significant.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Not rejected but significant:</strong> These contradict each other. If p < .05, we reject H₀ AND the model is significant.</li>
        <li><strong>B) Not rejected and not significant:</strong> With p < .001, we DO reject H₀ and the model IS significant.</li>
        <li><strong>C) Rejected but not significant:</strong> These contradict each other. Rejecting H₀ means the model IS significant.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 9: SPSS Practical Guide for interpreting hypothesis test results.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 4:</strong> Which SPSS menu path do you use to run a two-way between-groups ANOVA?</p>
    <div class="options">
      <p>A) Analyze → Compare Means → One-Way ANOVA</p>
      <p>B) Analyze → General Linear Model → Univariate</p>
      <p>C) Analyze → General Linear Model → Repeated Measures</p>
      <p>D) Analyze → Regression → Linear</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) Analyze → General Linear Model → Univariate</p>

      <p class="explanation"><strong>Why this is correct:</strong> Two-way (factorial) between-groups ANOVA is run using the General Linear Model → Univariate menu in SPSS.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) One-Way ANOVA:</strong> This is only for designs with one independent variable, not two.</li>
        <li><strong>C) Repeated Measures:</strong> This is for within-subjects factors, not between-groups.</li>
        <li><strong>D) Linear Regression:</strong> This is for different types of analyses, not ANOVA.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 9: SPSS Practical Guide for the step-by-step procedure.</p>
    </div>

  </details>
</div>

---

## Part 11: Reporting Factorial ANOVA in APA Format

### APA Format Structure

A complete factorial ANOVA report includes:

1. Description of the analysis
2. Omnibus test result
3. Main effects results
4. Interaction result
5. Follow-up tests (simple effects or post-hoc)
6. Effect sizes throughout

### Reporting the Omnibus Test

**Template:**
"A two-way between-groups ANOVA was conducted to examine the effects of [Factor A] and [Factor B] on [DV]. The omnibus test was significant, F(df₁, df₂) = X.XX, p < .001, indicating that the model significantly explained variance in [DV]."

**Example:**
"A 2×2 between-groups ANOVA was conducted to examine the effects of community type (city vs. suburb) and religious affiliation (yes vs. no) on the percentage of graduates going to college. The omnibus test was significant, F(3, 56) = 68.50, p < .001, indicating that the model significantly explained variance in college-going rates."

### Reporting Main Effects

**Template:**
"There was a [significant/non-significant] main effect of [Factor], F(df₁, df₂) = X.XX, p = .XXX, partial η² = .XX. [Describe direction if significant]."

**Example:**
"There was a significant main effect of community type, F(1, 56) = 106.74, p < .001, partial η² = .66, with suburban schools (M = 77.5%, SD = 8.2) having higher college-going rates than city schools (M = 67.5%, SD = 9.1)."

### Reporting the Interaction

**Template (if significant):**
"There was a significant interaction between [Factor A] and [Factor B], F(df₁, df₂) = X.XX, p < .001, partial η² = .XX. Simple effects tests revealed that [describe the pattern]."

**Example:**
"There was a significant interaction between community type and religious affiliation, F(1, 56) = 35.62, p < .001, partial η² = .33. Simple effects tests revealed that the effect of religious affiliation was significant in city schools, F(1, 28) = 45.23, p < .001, with religious schools showing substantially higher rates (85% vs. 60%), but not significant in suburban schools, F(1, 28) = 2.15, p = .154 (88% vs. 82%)."

**Template (if not significant):**
"There was no significant interaction between [Factor A] and [Factor B], F(df₁, df₂) = X.XX, p = .XXX."

### Complete Example Write-Up

**Method:**
"A 2×2 between-groups factorial ANOVA was conducted to examine the effects of community type (city vs. suburb) and religious affiliation (yes vs. no) on the percentage of graduates going to college. The design included 60 schools with approximately equal cell sizes (n = 15 per cell)."

**Results:**
"The omnibus test was significant, F(3, 56) = 68.50, p < .001, with the model explaining 78.6% of the variance in college-going rates (R² = .786).

There was a significant main effect of community type, F(1, 56) = 106.74, p < .001, partial η² = .66, and a significant main effect of religious affiliation, F(1, 56) = 70.29, p < .001, partial η² = .56. However, these main effects must be interpreted in light of a significant interaction, F(1, 56) = 35.62, p < .001, partial η² = .33.

Simple effects tests revealed that the effect of religious affiliation differed significantly across community types. In city schools, religious schools had substantially higher college-going rates (M = 85%, SD = 7.2) compared to non-religious schools (M = 60%, SD = 8.1), F(1, 28) = 45.23, p < .001, partial η² = .62. However, in suburban schools, the difference between religious (M = 88%, SD = 6.5) and non-religious schools (M = 82%, SD = 7.8) was not statistically significant, F(1, 28) = 2.15, p = .154, partial η² = .07."

### APA Formatting Reminders

**p-values:**

- Report exact p-values for p ≥ .001: "p = .023"
- For very small p-values: "p < .001" (not "p = .000")
- Italicize the p

**F-statistics:**

- Italicize the F
- Include both degrees of freedom: F(df₁, df₂)
- Report to 2 decimal places

**Effect sizes:**

- Always report effect sizes
- Use partial η² for individual effects
- Can report R² for overall model
- Interpret size (small, medium, large)

---

## Summary and Key Formulas

### Key Concepts Covered

1. **Factorial ANOVA** allows testing of multiple IVs and their interaction simultaneously
2. **Design notation** (e.g., 2×3) indicates number of levels for each factor
3. **Number of cells** = levels of Factor 1 × levels of Factor 2
4. **Main effects** examine each IV separately, averaging across the other IV(s)
5. **Interaction effects** show when the effect of one IV depends on the other IV
6. **Three null hypotheses** are tested: Main effect A, Main effect B, Interaction A×B
7. **Between-groups variance** is partitioned into two main effects and one interaction
8. **Interaction is paramount**: Always check interaction first before interpreting main effects
9. **Simple effects tests** explore significant interactions
10. **Post-hoc tests** are for significant main effects with 3+ levels (when interaction is not significant)

### Essential Formulas

**Degrees of Freedom:**

- df_A = a - 1
- df_B = b - 1
- df_A×B = (a - 1) × (b - 1)
- df_within = N - (a × b)
- df_total = N - 1

**Effect Sizes:**

- Partial η² = SS_effect / (SS_effect + SS_error)
- Total R² = SS_between_total / SS_total
- SS_between_total = SS_A + SS_B + SS_A×B

**Variance Partitioning:**

- Total Variance = Between-Groups + Within-Groups
- Between-Groups = Main Effect A + Main Effect B + Interaction

### The Decision Tree (Summary)

```
1. Check INTERACTION first
   ↓
2. Interaction significant?
   ├─ YES → Run SIMPLE EFFECTS tests
   │         Report interaction pattern
   │         Be cautious with main effects
   │
   └─ NO  → Interpret MAIN EFFECTS independently
             Run POST-HOC tests for factors with 3+ levels
```

### Key Terms Glossary

- **Factorial ANOVA:** ANOVA with 2+ independent variables
- **Two-way ANOVA:** Factorial ANOVA with exactly 2 factors
- **Main effect:** Effect of one IV, averaging across other IV(s)
- **Interaction:** When effect of one IV depends on level of other IV
- **Simple effects:** Effect of one IV at specific level of other IV
- **Marginal means:** Means for each level of one factor, averaged across other factor
- **Cell:** Unique combination of factor levels
- **Omnibus test:** Overall test of the entire model
- **Between-groups variance:** Variance explained by IVs (main effects + interaction)
- **Within-groups variance:** Error variance not explained by IVs
- **Partial eta squared (partial η²):** Variance explained by one effect, removing others
- **Total R²:** Variance explained by entire model

---

**Congratulations!** You've completed the comprehensive M5 lecture on Two-Way Factorial ANOVA. You now have the knowledge and skills to:

- Understand factorial design notation and calculate number of cells
- Distinguish between main effects and interaction effects
- Recognize why interactions are the most important finding
- Test three separate null hypotheses in two-way ANOVA
- Calculate and interpret degrees of freedom for factorial designs
- Apply the decision tree for interpreting results
- Run simple effects tests when interactions are significant
- Run post-hoc tests for main effects when appropriate
- Calculate and interpret effect sizes (partial η² and R²)
- Perform two-way ANOVA in SPSS
- Report factorial ANOVA results in proper APA format
- Make informed decisions about statistical analysis with multiple factors

Remember: **Always check the interaction first!** It's the golden rule of factorial ANOVA and will guide all your subsequent interpretations.

---

## Quick Reference Sheet

**Print or save this one-page summary for quick review!**

### Design Notation
- **2×2 design:** 2 factors, each with 2 levels = 4 cells
- **3×2 design:** 2 factors (3 levels × 2 levels) = 6 cells
- **Number of cells = Level₁ × Level₂**

### Key Concepts
- **Main Effect:** Effect of one IV, averaging across the other IV(s)
- **Interaction:** Effect of one IV depends on level of other IV
- **Marginal Means:** Averages for each level of one factor (collapsed across other)
- **Simple Effects:** Effect of one IV at specific level of other IV

### Three Null Hypotheses Tested
1. H₀: Main effect of Factor A
2. H₀: Main effect of Factor B
3. H₀: Interaction between A and B

### Degrees of Freedom Formulas
- **df_A** = a - 1
- **df_B** = b - 1
- **df_A×B** = (a - 1) × (b - 1)
- **df_within** = N - (a × b)
- **df_total** = N - 1

### Effect Size Formulas
- **Partial η²** = SS_effect / (SS_effect + SS_error)
- **Total R²** = SS_between_total / SS_total
- **Cohen's Guidelines:** Small = .01, Medium = .06, Large = .14

### The Decision Tree (MEMORIZE THIS!)
```
1. Check INTERACTION first (p < .05?)
   │
   ├─ YES (Significant Interaction)
   │   → Run SIMPLE EFFECTS tests
   │   → Report interaction pattern
   │   → Cautiously interpret main effects
   │
   └─ NO (Not Significant)
       → Interpret MAIN EFFECTS independently
       → For each significant main effect:
           • 2 levels → Compare marginal means
           • 3+ levels → Run POST-HOC tests
```

### Four Assumptions
1. **Independence** (most critical!)
2. **Normality** (check per cell)
3. **Homogeneity of Variance** (Levene's test)
4. **No extreme outliers**

### SPSS Steps
1. Analyze → General Linear Model → Univariate
2. Move DV to "Dependent Variable"
3. Move IVs to "Fixed Factor(s)"
4. Options → Check "Descriptive statistics" and "Estimates of effect size"
5. OK

### APA Reporting Template
"A [design] between-groups factorial ANOVA examined the effects of [Factor A] and [Factor B] on [DV]. The interaction was [significant/not significant], F(df₁, df₂) = X.XX, p = .XXX, partial η² = .XX. [Describe pattern if significant]. Main effects showed [describe if interaction not significant]."

### Common Mistakes to Avoid
❌ Checking main effects before interaction
❌ Running post-hoc tests when you need simple effects
❌ Reporting p = .000 (use p < .001)
❌ Forgetting effect sizes
❌ Interpreting main effects when interaction is significant

### Study Tips
- Practice the decision tree until it's automatic
- Always draw the interaction plot
- Calculate degrees of freedom first to check your understanding
- Memorize: Interaction > Main Effects in importance!
