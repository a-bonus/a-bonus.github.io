---
layout: lecture
title: "Module 1: Foundations of Statistical Reasoning and Data Analysis"
---

# Module 1: Foundations of Statistical Reasoning and Data Analysis

**Estimated Study Time:** 2-3 hours

## Learning Objectives

By the end of this module, you will be able to:

1. Explain the fundamental purpose of statistics in scientific research
2. Distinguish between descriptive and inferential statistics
3. Identify and correctly name variables in research scenarios
4. Classify variables by their role (IV/DV) and measurement scale (nominal, ordinal, scale)
5. Calculate and interpret measures of central tendency and variability
6. Create and interpret frequency distributions and appropriate visualizations
7. Understand the relationship between samples and populations
8. Use z-scores to standardize and compare values across different scales
9. Apply basic probability concepts to statistical inference
10. Perform data setup and basic analyses in SPSS

---

## Table of Contents

1. [The Purpose of Statistics](#part-1-the-purpose-of-statistics)
2. [Variables: The Building Blocks](#part-2-variables-the-building-blocks)
3. [Classifying Variables](#part-3-classifying-variables)
4. [Describing Data with Numbers](#part-4-describing-data-with-numbers)
5. [Visualizing Data: Frequency Distributions](#part-5-visualizing-data-frequency-distributions)
6. [From Sample to Population](#part-6-from-sample-to-population)
7. [The Normal Distribution and Z-Scores](#part-7-the-normal-distribution-and-z-scores)
8. [Probability and Inference](#part-8-probability-and-inference)
9. [Practical Guide: Working with SPSS](#part-9-practical-guide-working-with-spss)
10. [Summary and Key Formulas](#summary-and-key-formulas)

---

## Part 1: The Purpose of Statistics

### Why Do We Need Statistics?

Imagine you're a researcher trying to answer the question: "Does meditation reduce anxiety?" You could rely on personal experience, anecdotes, or intuition. But science demands something more rigorous—**objective evidence** based on systematic data collection and analysis.

This is where statistics comes in.

**Key Concept:** Statistics is the set of mathematical tools we use to organize, summarize, and interpret numerical data, allowing us to move from subjective opinion to objective evidence.

### The Two Branches of Statistics

Statistics serves two fundamental purposes, reflected in its two main branches:

#### 1. Descriptive Statistics

**Purpose:** To summarize and describe the data you have collected from your specific group.

**Example:** "In our study of 50 college students, the average hours of sleep per night was 6.8 hours, with most students sleeping between 6 and 8 hours."

**When to Use:**

- When you want to understand patterns in your collected data
- When presenting a summary of survey results
- When creating a profile of your participant group
- Any time you need to communicate "what the data looks like"

**Common Tools:**

- Averages (mean, median, mode)
- Measures of spread (range, standard deviation)
- Frequency tables
- Graphs and charts

#### 2. Inferential Statistics

**Purpose:** To make educated guesses (inferences) about a larger group (population) based on data from a smaller subset (sample).

**Example:** "Based on our sample of 50 college students, we can infer with 95% confidence that the average sleep time for _all_ college students at this university falls between 6.3 and 7.3 hours."

**When to Use:**

- When you want to generalize findings beyond your specific participants
- When testing hypotheses about population characteristics
- When determining if observed differences are "real" or due to chance
- Most research scenarios in psychology and social sciences

**Common Tools:**

- Hypothesis tests (t-tests, ANOVA, etc.)
- Confidence intervals
- p-values and significance testing

**Why This Matters:** Almost all psychological research uses inferential statistics because we can never study every single person. We study samples to learn about populations.

### Real-World Applications

**Medical Research:** A pharmaceutical company tests a new drug on 500 patients. They use _descriptive_ statistics to summarize the results in their sample (e.g., "60% showed improvement") and _inferential_ statistics to estimate effectiveness in the broader population (e.g., "We are 95% confident the drug helps between 55% and 65% of all patients with this condition").

**Educational Psychology:** A school psychologist measures reading scores for 30 third-graders using a new teaching method. Descriptive statistics show what happened in this specific classroom. Inferential statistics help determine if the method would likely work in other classrooms.

**Business Decisions:** A company surveys 200 customers about a product redesign. They describe their sample's preferences, then use inference to predict how their entire customer base (millions) would respond.

### Common Misconceptions

❌ **Misconception:** "Statistics can prove anything you want."
✓ **Reality:** When used correctly, statistics provide objective evidence. Misleading statistics usually involve inappropriate methods, selective reporting, or misinterpretation.

❌ **Misconception:** "A statistic is just a number."
✓ **Reality:** Statistics are numbers _with context_. The interpretation matters as much as the calculation.

❌ **Misconception:** "I only need statistics if I'm doing research."
✓ **Reality:** Statistical thinking helps you evaluate claims in news, advertising, health information, and everyday decision-making.

**Think About It:** When you see a headline like "New study shows coffee reduces heart disease risk by 30%," what questions should you ask? (Sample size? How was the study designed? What does "30%" actually mean?)

---

## Part 2: Variables: The Building Blocks

### What is a Variable?

In research, we don't measure everything—we measure specific **variables**.

**Definition:** A variable is any characteristic or measurement that can change or vary from one person, object, or situation to another.

**Key Concept:** If something doesn't vary, it's not a variable—it's a constant.

### The Golden Rule of Naming Variables

A variable's name must represent something that can have **different values or levels**.

**Example:** If you're studying whether exercise affects mood:

- ✓ **Good variable name:** "Exercise frequency" (can be 0, 1, 2, 3+ times per week)
- ✗ **Bad variable name:** "Exercise" (too vague—what about exercise?)

### Practice: Identifying Variables

Let's practice with some research scenarios:

**Scenario 1:** "Do college students who get more sleep perform better on exams?"

**Think About It:** What are we measuring that can vary?

- Sleep duration (varies from student to student)
- Exam performance (varies from student to student)

✓ **Good variable names:** `Hours of sleep`, `Exam score`
✗ **Bad variable names:** `Sleep`, `Test` (these don't clearly indicate what's being measured)

**Scenario 2:** "Are women more likely than men to volunteer for charity work?"

**Variables:**

- `Gender` (varies: male, female, non-binary, etc.)
- `Volunteer status` or `Number of volunteer hours` (varies by person)

✓ **Good variable names:** `Gender`, `Volunteer hours per month`
✗ **Bad variable names:** `Women`, `Men`, `Volunteering` (these suggest groups or activities, not measurable variables)

**Scenario 3:** "Does caffeine improve reaction time?"

**Variables:**

- `Caffeine consumption` or `Caffeine condition` (e.g., caffeine vs. no caffeine)
- `Reaction time` (measured in milliseconds)

### Quick Check

For each research question, identify the variables:

1. "Do children who watch more TV have shorter attention spans?"
2. "Is there a relationship between income level and job satisfaction?"
3. "Does listening to music while studying help or hurt test performance?"

<details>
<summary>Click to see answers</summary>

1. Variables: `TV viewing hours`, `Attention span` (measured in some standardized way)
2. Variables: `Income level`, `Job satisfaction` (perhaps measured on a rating scale)
3. Variables: `Music condition` (music vs. no music), `Test performance` (test score)
</details>

### Why Proper Variable Naming Matters

**In Research Papers:** Clear variable names make your methods transparent and reproducible.

**In SPSS:** The variable names you create will appear in all your output. Good names make your results instantly understandable. Compare:

- ❌ `VAR001`, `VAR002` → What do these mean?
- ✓ `Age`, `Depression_Score` → Immediately clear!

---

## Part 3: Classifying Variables

Not all variables are created equal. How we classify a variable determines which statistical analyses we can use and how we interpret our results.

### Classification System 1: By Role in Research

This classification describes the **cause-and-effect relationship** you're investigating.

#### Independent Variable (IV)

**Definition:** The variable you believe is the **cause** or **predictor**. It's "independent" because its value doesn't depend on other variables in your study.

**Other Names:** Predictor variable, explanatory variable

**Examples:**

- Type of therapy (CBT vs. medication)
- Amount of study time
- Experimental condition (treatment vs. control)

#### Dependent Variable (DV)

**Definition:** The variable you believe is the **effect** or **outcome**. Its value "depends on" the independent variable.

**Other Names:** Outcome variable, response variable, criterion variable

**Examples:**

- Depression symptoms (after therapy)
- Test score (after studying)
- Recovery rate (after treatment)

### How to Identify IV and DV

**The Simple Trick:** Ask yourself: "Does [Variable A] depend on [Variable B]?"

**Example:** "Does exercise frequency affect stress levels?"

- Question: Does `stress level` depend on `exercise frequency`? **Yes!**
- Therefore: **DV** = Stress level, **IV** = Exercise frequency

**Example:** "Is there a relationship between SAT scores and college GPA?"

- Question: Does `college GPA` depend on `SAT score`? **Yes!** (We're predicting GPA from SAT)
- Therefore: **DV** = College GPA, **IV** = SAT score

### Practice Scenarios

**Scenario 1:** A researcher investigates whether background noise affects concentration.

- **IV:** Background noise level (quiet, moderate, loud)
- **DV:** Concentration score

**Scenario 2:** A study examines whether age is related to smartphone usage.

- **IV:** Age
- **DV:** Smartphone usage (hours per day)

**Scenario 3:** Do students who attend review sessions score higher on exams?

- **IV:** Review session attendance (yes/no)
- **DV:** Exam score

**Common Mistake:** Sometimes students confuse which is which. Remember: The DV is what you're _measuring as an outcome_. The IV is what you're _manipulating or using to predict_.

**Advanced Note:** Not all research fits neatly into IV/DV categories. Correlational studies might examine relationships without clear causation. We'll explore this more in Module 6.

---

### Classification System 2: By Measurement Scale

This classification describes the **nature of the values** a variable can take. This is **crucial** because it determines which statistical procedures are appropriate.

#### Nominal Variables

**Definition:** Variables that represent categories or names with **no inherent order or ranking**.

**Key Property:** The numbers assigned are arbitrary labels—they have no mathematical meaning.

**Examples:**

- `Gender` (1 = Male, 2 = Female, 3 = Non-binary)
- `Marital Status` (1 = Single, 2 = Married, 3 = Divorced, 4 = Widowed)
- `Major` (1 = Psychology, 2 = Biology, 3 = English, etc.)
- `Type of therapy` (1 = CBT, 2 = Psychodynamic, 3 = Humanistic)

**What You Can Do:**

- Count frequencies (How many males? How many females?)
- Find the mode (most common category)
- Create bar charts or pie charts

**What You Cannot Do:**

- Calculate a meaningful average (What's the average of Male and Female? Nonsense!)
- Put categories in order (Unless there's a natural order—see Ordinal)

**SPSS Note:** In SPSS, set the "Measure" to "Nominal" and always define value labels (1 = "Male", 2 = "Female") to make output readable.

#### Ordinal Variables

**Definition:** Variables that represent categories with a **meaningful rank or order**, but the distance between ranks is **not equal or meaningful**.

**Key Property:** You can say A > B, but you can't say "how much more."

**Examples:**

- `Education level` (1 = High School, 2 = Bachelor's, 3 = Master's, 4 = Doctorate)
  - A Master's is "more" than a Bachelor's, but is the distance from HS to Bachelor's the same as Bachelor's to Master's? No!
- `Class rank` (1st place, 2nd place, 3rd place)
  - The difference between 1st and 2nd might be 0.01 points, but between 10th and 11th might be 5 points
- `Likert scale items` (1 = Strongly Disagree, 2 = Disagree, 3 = Neutral, 4 = Agree, 5 = Strongly Agree)
  - The "distance" from Disagree to Neutral might not equal the distance from Agree to Strongly Agree

**What You Can Do:**

- Everything you can do with nominal data
- Find the median (middle rank)
- Determine if one value is greater or less than another

**What You Should Be Cautious About:**

- Calculating means (technically debatable—see the note on Likert scales below)
- Assuming equal intervals

**SPSS Note:** Set "Measure" to "Ordinal" when the categories have an order but aren't true numbers.

**The Likert Scale Debate:** Many researchers treat Likert scales as interval/scale data and calculate means. This is acceptable when you have multiple items combined into a scale score, but be aware it's a simplification.

#### Scale Variables (Interval and Ratio)

**Definition:** Variables with **true numerical values** where the distance between any two values is **equal and meaningful**.

**Key Property:** You can do real math—add, subtract, average, etc.

**Two Subtypes:**

- **Interval:** Has equal intervals but no true zero point (e.g., temperature in Celsius—0° doesn't mean "no temperature")
- **Ratio:** Has equal intervals AND a true zero point (e.g., height, weight, age—0 means "none")

**In SPSS:** Both are labeled as "Scale" (SPSS doesn't distinguish between them)

**Examples:**

- `Age` (in years) → 30 years is exactly twice 15 years
- `Reaction time` (in milliseconds)
- `Test score` (0-100)
- `Income` (in dollars)
- `Height` (in inches)
- `IQ score`
- `Number of errors` on a task

**What You Can Do:**

- Everything from nominal and ordinal
- Calculate mean, median, mode
- Calculate standard deviation and variance
- Perform most statistical tests (t-tests, ANOVA, correlation, regression)

**SPSS Note:** Set "Measure" to "Scale" for all true numerical measurements.

### Discrete vs. Continuous

This is another way to classify **scale** variables:

**Discrete Variables:** Can only take specific, separate values (usually whole numbers).

- Examples: `Number of siblings` (0, 1, 2, 3...), `Number of errors`, `Number of children`
- You can't have 2.5 siblings!

**Continuous Variables:** Can take any value within a range (including decimals).

- Examples: `Height` (65.5, 65.51, 65.512 inches...), `Reaction time`, `Temperature`
- Theoretically infinite precision (limited only by your measurement tool)

**Practical Note:** The distinction matters for certain statistical procedures, but SPSS treats both as "Scale."

### Decision Tree: Determining Measurement Level

**Start Here:** What are the possible values?

1. **Are they categories/names?** → Nominal

   - Is there a natural order to the categories?
     - **No** → Nominal (e.g., hair color, major)
     - **Yes** → Ordinal (e.g., education level, class rank)

2. **Are they true numbers?** → Scale
   - Can you perform meaningful arithmetic (add, average)?
     - **Yes** → Scale
     - **No** → Probably ordinal (reconsider if they're really numbers)

### Why Measurement Level Matters

**The Golden Rule:** Your variable's measurement level determines which statistical procedures you can use.

| Measurement Level | Appropriate Central Tendency | Appropriate Graphs      | Common Statistical Tests               |
| :---------------- | :--------------------------- | :---------------------- | :------------------------------------- |
| **Nominal**       | Mode                         | Bar chart, Pie chart    | Chi-square test                        |
| **Ordinal**       | Median, Mode                 | Bar chart               | Mann-Whitney U, Kruskal-Wallis         |
| **Scale**         | Mean, Median, Mode           | Histogram, Scatter plot | t-test, ANOVA, Correlation, Regression |

**Common Mistake:** Students sometimes calculate the mean of a nominal variable because SPSS doesn't stop you. If you set `Gender` as 1=Male, 2=Female and calculate a mean of 1.6, what does that mean? Nothing! Always check your measurement level before choosing an analysis.

### Quick Check

Classify each variable:

1. Blood type (A, B, AB, O)
2. Pain rating (0 = No pain, 10 = Worst pain imaginable)
3. Salary in dollars
4. Political party (Republican, Democrat, Independent, Other)
5. Finishing position in a race (1st, 2nd, 3rd, etc.)
6. Reaction time in milliseconds

<details>
<summary>Click to see answers</summary>

1. **Nominal** (categories, no order)
2. **Ordinal** (or arguably scale if treating as continuous—this is a judgment call)
3. **Scale/Ratio** (true numbers with meaningful zero)
4. **Nominal** (categories, no inherent order)
5. **Ordinal** (ranked, but distances between ranks aren't equal)
6. **Scale/Ratio** (continuous measurement)
</details>

---

## Part 4: Describing Data with Numbers

Once you've collected data, the first step is to summarize it. With scale (numerical) data, we use two types of summary statistics:

1. **Central Tendency** - Where is the "center" or "typical" value?
2. **Variability** - How spread out are the scores?

### Measures of Central Tendency

#### The Mean (M or \(\bar{X}\))

**Definition:** The arithmetic average—the sum of all scores divided by the number of scores.

**Formula:**
\[ M = \frac{\sum X}{N} \]

Where:

- \(\sum X\) = sum of all scores
- \(N\) = number of scores

**Example:** Test scores: 75, 80, 85, 90, 95
\[ M = \frac{75 + 80 + 85 + 90 + 95}{5} = \frac{425}{5} = 85 \]

**When to Use:**

- Data is scale (interval/ratio)
- Distribution is relatively symmetrical
- No extreme outliers

**Strengths:**

- Uses all data points
- Most statistically powerful
- Required for most inferential tests

**Weaknesses:**

- Sensitive to extreme scores (outliers)
- Can be misleading with skewed distributions

**Real Example:** Average income is often misleading because billionaires pull the mean way up. The mean income in a town might be $120,000, but if one billionaire lives there, most residents might earn $40,000.

#### The Median (Mdn)

**Definition:** The middle score when all values are arranged in order.

**How to Calculate:**

1. Put all scores in order from lowest to highest
2. If N is odd: median is the middle score
3. If N is even: median is the average of the two middle scores

**Example 1 (odd N):** Scores: 65, 70, 75, 80, 95

- The middle score (3rd of 5) is **75**

**Example 2 (even N):** Scores: 65, 70, 75, 80, 85, 95

- The two middle scores (3rd and 4th) are 75 and 80
- Median = (75 + 80) / 2 = **77.5**

**When to Use:**

- Data is ordinal or scale
- Distribution is skewed (lopsided)
- Extreme outliers are present
- Describing income, home prices, etc.

**Strengths:**

- Not affected by extreme scores
- Better represents the "typical" value in skewed distributions
- Can be used with ordinal data

**Weaknesses:**

- Doesn't use all information in the dataset
- Less useful for inferential statistics

**Real Example:** Median household income is usually reported instead of mean because it's not inflated by the ultra-wealthy.

#### The Mode

**Definition:** The most frequently occurring score.

**Example:** Scores: 70, 75, 75, 75, 80, 85, 90

- The mode is **75** (appears three times)

**When to Use:**

- Any level of data (nominal, ordinal, or scale)
- Describing the most common category
- Identifying peaks in distributions

**Special Cases:**

- **Bimodal:** Two modes (two distinct peaks)
- **Multimodal:** More than two modes
- **No mode:** All values occur with equal frequency

**Strengths:**

- Only measure of central tendency for nominal data
- Can identify multiple peaks
- Not affected by outliers

**Weaknesses:**

- Might not exist or be useful
- Doesn't use most of the data
- Rarely used in inferential statistics

**Real Example:** The mode of `Favorite Color` in a class might be "Blue" (nominal data where mean and median are meaningless).

### Choosing the Right Measure

**Use the Mean when:**

- Data is scale/interval
- Distribution is roughly symmetrical
- No extreme outliers
- You need to do further statistical tests

**Use the Median when:**

- Data is ordinal
- Distribution is skewed
- Extreme outliers are present
- Describing income, housing prices, or other ratio variables prone to outliers

**Use the Mode when:**

- Data is nominal
- You want to identify the most common category
- Describing categorical preferences

**Example:** Consider ages at a children's birthday party: 5, 5, 6, 6, 6, 7, 7, 35 (one parent stayed)

- Mean = 9.6 years (Not representative! Pulled up by the outlier)
- Median = 6 years (Better representation of the typical partygoer)
- Mode = 6 years (Most common age)

### Measures of Variability

Knowing the center isn't enough. Consider two classes with the same mean test score of 75:

- **Class A:** Scores range from 73 to 77 (very consistent)
- **Class B:** Scores range from 20 to 100 (highly variable)

The mean doesn't tell the whole story! We need measures of **variability** (spread, dispersion).

#### Range

**Definition:** The distance between the highest and lowest scores.

**Formula:**
\[ \text{Range} = X*{\text{max}} - X*{\text{min}} \]

**Example:** Scores: 65, 70, 75, 80, 95
\[ \text{Range} = 95 - 65 = 30 \]

**Strengths:**

- Easy to calculate and understand
- Gives a quick sense of spread

**Weaknesses:**

- Based on only two scores (ignores everything else)
- Extremely sensitive to outliers
- Not useful for inferential statistics

#### Variance (s² or SD²)

**Definition:** The average of the squared deviations from the mean. It quantifies how much scores differ from the mean.

**Why We Square the Deviations:** If we just averaged the deviations \((X - M)\), they would sum to zero (positive and negative cancel out). Squaring makes all deviations positive.

**Formula (for a sample, describing only the data you have):**
\[ \text{Variance} = \frac{\sum(X - M)^2}{N} \]

**Formula (for estimating population variance from a sample):**
\[ s^2 = \frac{\sum(X - M)^2}{n - 1} \]

(More on this \(n - 1\) distinction in Part 6)

**Example:** Scores: 2, 4, 6, 8, 10

- Mean = 6
- Deviations: -4, -2, 0, +2, +4
- Squared deviations: 16, 4, 0, 4, 16
- Sum of squared deviations (SS) = 40
- Variance = 40 / 5 = **8**

**Interpretation:** Variance of 8... but 8 what? The units are squared (if original scores are in points, variance is in points²), which is hard to interpret.

**Strengths:**

- Uses all data points
- Foundation for many statistical procedures
- Mathematically important

**Weaknesses:**

- Units are squared (not intuitive)
- Hard to interpret directly

#### Standard Deviation (s or SD)

**Definition:** The square root of the variance. It represents the **average distance of scores from the mean** (in the original units).

**Formula:**
\[ SD = \sqrt{\text{Variance}} = \sqrt{\frac{\sum(X - M)^2}{N}} \]

**Or for population estimate:**
\[ s = \sqrt{\frac{\sum(X - M)^2}{n - 1}} \]

**Example (continuing from above):**

- Variance = 8
- Standard Deviation = √8 = **2.83**

**Interpretation:** On average, scores deviate from the mean by 2.83 points.

**Key Insight:**

- **Small SD** → Scores cluster tightly around the mean → Low variability → Group is homogeneous
- **Large SD** → Scores spread widely → High variability → Group is heterogeneous

**Real Example:**

- **Test A:** M = 75, SD = 3 → Most scores between 72-78 (consistent performance)
- **Test B:** M = 75, SD = 15 → Scores range widely from 60-90 (inconsistent performance)

**SPSS Note:** SPSS always reports the version using \(n-1\), which estimates the population SD. This is what you'll see in output.

### Worked Example: Calculating Descriptive Statistics

**Data:** Hours of sleep for 8 students: 5, 6, 6, 7, 7, 7, 8, 10

**Step 1: Mean**
\[ M = \frac{5 + 6 + 6 + 7 + 7 + 7 + 8 + 10}{8} = \frac{56}{8} = 7 \text{ hours} \]

**Step 2: Median**

- Ordered: 5, 6, 6, 7, 7, 7, 8, 10
- Middle scores (4th and 5th): 7 and 7
- Median = 7 hours

**Step 3: Mode**

- 7 appears three times (most frequent)
- Mode = 7 hours

**Step 4: Range**
\[ \text{Range} = 10 - 5 = 5 \text{ hours} \]

**Step 5: Variance and Standard Deviation**

| Score (X) | Deviation (X - M) | Squared Deviation (X - M)² |
| :-------- | :---------------- | :------------------------- |
| 5         | -2                | 4                          |
| 6         | -1                | 1                          |
| 6         | -1                | 1                          |
| 7         | 0                 | 0                          |
| 7         | 0                 | 0                          |
| 7         | 0                 | 0                          |
| 8         | 1                 | 1                          |
| 10        | 3                 | 9                          |
| **Sum**   |                   | **SS = 16**                |

\[ \text{Variance} = \frac{16}{8} = 2 \text{ hours}^2 \]

\[ SD = \sqrt{2} = 1.41 \text{ hours} \]

**Interpretation:** The average sleep time is 7 hours, with students typically varying by about 1.4 hours above or below this average.

### Quick Check

Calculate mean, median, mode, and range for these reaction times (in milliseconds):
250, 275, 280, 280, 290, 310, 500

<details>
<summary>Click to see answers</summary>

- **Mean:** (250+275+280+280+290+310+500)/7 = 312.1 ms
- **Median:** 280 ms (middle value)
- **Mode:** 280 ms (appears twice)
- **Range:** 500 - 250 = 250 ms

**Note:** The mean (312.1) is pulled up by the outlier (500). The median (280) better represents the typical response time.

</details>

---

## Part 5: Visualizing Data: Frequency Distributions

Numbers tell part of the story, but **visualizations** can reveal patterns that statistics alone might miss.

### What is a Frequency Distribution?

**Definition:** A summary showing how many times each value (or range of values) appears in a dataset.

**Purpose:** To see the shape, spread, and patterns in your data at a glance.

### For Categorical Data: Frequency Tables and Bar Charts

#### Frequency Tables

**Example:** Survey of 50 students' employment status

| Employment Status  | Frequency | Percent  |
| :----------------- | :-------: | :------: |
| Employed Full-Time |    12     |   24%    |
| Employed Part-Time |    23     |   46%    |
| Unemployed         |    10     |   20%    |
| Other              |     5     |   10%    |
| **Total**          |  **50**   | **100%** |

**What to Look For:**

- Which category is most common? (Part-time employment)
- Are categories evenly distributed or is there a dominant category?
- Any unexpected patterns?

#### Bar Charts

**Key Feature:** Bars are **separated** (gaps between them) to emphasize that categories are distinct.

**When to Use:** Nominal or ordinal data

**Best Practices:**

- Label axes clearly
- Include a descriptive title
- Order bars logically (by frequency, or natural order for ordinal data)

**SPSS Creation:**

- `Graphs → Chart Builder`
- Select "Bar" chart type
- Drag your categorical variable to the X-axis
- Y-axis automatically shows frequency (count)

### For Scale Data: Grouped Frequency Tables and Histograms

With continuous data, you might have many unique values. Grouping them into "bins" or "intervals" makes patterns visible.

#### Grouped Frequency Tables

**Example:** Ages of 100 participants

| Age Range | Frequency | Percent  |
| :-------- | :-------: | :------: |
| 18-22     |    25     |   25%    |
| 23-27     |    30     |   30%    |
| 28-32     |    20     |   20%    |
| 33-37     |    15     |   15%    |
| 38-42     |    10     |   10%    |
| **Total** |  **100**  | **100%** |

**Choosing Bin Width:**

- **Too many bins:** Table becomes cluttered, pattern is hard to see
- **Too few bins:** You lose important detail
- **Rule of thumb:** Aim for 5-15 bins, depending on sample size
- **Equal width:** Keep intervals consistent (each covers same range)

**SPSS Method:**

- Use `Transform → Visual Binning` to create equal-width intervals
- Then run `Analyze → Descriptive Statistics → Frequencies` on the binned variable

#### Histograms

**Key Feature:** Bars are **touching** (no gaps) to show that the variable is continuous.

**When to Use:** Scale (continuous) data

**What to Look For:**

1. **Shape:**

   - **Symmetrical/Normal:** Bell-shaped, mean ≈ median ≈ mode
   - **Skewed Right (Positive Skew):** Long tail to the right, mean > median
   - **Skewed Left (Negative Skew):** Long tail to the left, mean < median
   - **Bimodal:** Two distinct peaks (might indicate two subgroups)

2. **Center:** Where is the middle of the distribution?

3. **Spread:** How wide is the distribution?

4. **Outliers:** Any unusually extreme values?

**Examples of Distribution Shapes:**

- **Normal Distribution (Bell Curve):**

  - Most common in nature (height, IQ, many biological measures)
  - Symmetrical, one peak in the center
  - Most values cluster near the mean

- **Right-Skewed (Positively Skewed):**

  - Examples: Income, home prices, reaction times
  - Most values are low, but a few very high values create a long right tail
  - Mean > Median (pulled toward the tail)

- **Left-Skewed (Negatively Skewed):**

  - Examples: Age at retirement, test scores on an easy exam
  - Most values are high, but a few low values create a long left tail
  - Mean < Median

- **Bimodal:**
  - Examples: Height when measuring both men and women together
  - Two distinct peaks
  - Might indicate two separate groups in your data

**Why Shape Matters:**

- Determines which central tendency measure is best (mean vs. median)
- Affects which statistical tests are appropriate (many assume normal distribution)
- Reveals potential data issues or interesting subgroups

**SPSS Creation:**

- `Graphs → Chart Builder`
- Select "Histogram"
- Drag your scale variable to the X-axis
- Optional: Check "Display normal curve" to see how your data compares to a perfect bell curve

### Common Mistake: Choosing the Wrong Graph

❌ Creating a histogram for nominal data (e.g., gender)
✓ Use a bar chart instead

❌ Creating a bar chart for continuous data (e.g., age)
✓ Use a histogram instead

**The Difference:**

- **Bar charts:** For categories (gaps show distinct groups)
- **Histograms:** For continuous variables (touching bars show continuity)

### Quick Check

What type of graph should you create for each variable?

1. Type of smartphone (iPhone, Android, Other)
2. Daily screen time in hours
3. Education level (HS, Bachelor's, Master's, Doctorate)
4. Number of social media followers

<details>
<summary>Click to see answers</summary>

1. **Bar chart** (nominal data - categories)
2. **Histogram** (scale data - continuous)
3. **Bar chart** (ordinal data - ordered categories)
4. **Histogram** (scale data - discrete but treated as continuous)
</details>

---

## Part 6: From Sample to Population

This is where statistics gets its real power—using information from a small group to make educated guesses about a much larger group.

### Key Definitions

**Population:** The entire group you're interested in studying.

- Examples: All college students in the U.S., all people with depression, all registered voters

**Sample:** The subset of the population you actually collect data from.

- Examples: 200 students from your university, 50 patients in a clinical trial, 1,000 voters surveyed by phone

**Why We Use Samples:**

- **Practical:** Studying entire populations is usually impossible (too expensive, time-consuming, or logistically infeasible)
- **Sufficient:** A well-chosen sample can provide accurate estimates of population characteristics
- **Necessary:** Sometimes the population is infinite or hypothetical (e.g., all possible outcomes of a cognitive task)

### Parameters vs. Statistics

We use different symbols depending on whether we're describing a population or a sample:

| Measure                | Population (Parameter) | Sample (Statistic)   |
| :--------------------- | :--------------------- | :------------------- |
| **Size**               | \(N\)                  | \(n\)                |
| **Mean**               | \(\mu\) (mu)           | \(M\) or \(\bar{X}\) |
| **Standard Deviation** | \(\sigma\) (sigma)     | \(s\) or \(SD\)      |
| **Variance**           | \(\sigma^2\)           | \(s^2\)              |

**Mnemonic:**

- **P**opulation → **P**arameter → (G)reek letters
- **S**ample → **S**tatistic → (R)oman letters

**Key Concept:** We almost never know the true population parameters. We use sample statistics to **estimate** them.

### The Problem of Bias and the n-1 Correction

Here's a surprising fact: **Samples tend to be less variable than their populations.**

**Why?** By random chance, extreme values in the population are less likely to appear in a small sample. This means if we calculate variance using the sample formula \(\frac{\sum(X-M)^2}{n}\), we systematically **underestimate** the true population variance.

**The Solution:** Use \(n-1\) instead of \(n\) in the denominator when estimating population variance from a sample.

**Formulas:**

**Sample Variance (describes only your sample):**
\[ \text{Variance} = \frac{SS}{n} = \frac{\sum(X-M)^2}{n} \]

**Estimated Population Variance (what SPSS calculates):**
\[ s^2 = \frac{SS}{n-1} = \frac{\sum(X-M)^2}{n-1} \]

**Why This Works:** Dividing by a smaller number (n-1) makes the variance estimate slightly larger, correcting for the systematic underestimation. This is called **Bessel's correction** or the **degrees of freedom correction**.

**Degrees of Freedom (df):** \(df = n - 1\)

- Represents the number of values that are "free to vary" when calculating variance
- Once you know the mean and n-1 values, the last value is determined

### Worked Example: Sample vs. Population Calculation

**Data:** Quiz scores for 5 students: 6, 7, 8, 9, 10

**Mean:** \(M = \frac{40}{5} = 8\)

**Sum of Squares (SS):**

- Deviations: -2, -1, 0, 1, 2
- Squared: 4, 1, 0, 1, 4
- SS = 10

**Sample Variance (describes only these 5 students):**
\[ \text{Variance} = \frac{10}{5} = 2.0 \]
\[ SD = \sqrt{2} = 1.41 \]

**Estimated Population Variance (estimates all students in the class):**
\[ s^2 = \frac{10}{4} = 2.5 \]
\[ s = \sqrt{2.5} = 1.58 \]

**Notice:** The population estimate (s = 1.58) is larger than the sample SD (1.41), correcting for the underestimation bias.

**SPSS Always Uses n-1:** When you run descriptive statistics in SPSS, it calculates \(s\) (using n-1), not the sample SD. This is because we're almost always interested in making inferences about populations.

### Why This Matters for Your Assignment

**In Question 5 of the M1 assignment:**

- You calculate SD manually using the sample formula (dividing by n)
- SPSS calculates SD using the population estimate formula (dividing by n-1)
- **Your values will differ!**
- This isn't an error—it's demonstrating your understanding of the difference between describing a sample and estimating a population parameter

### Quick Check

True or False?

1. A sample statistic is always equal to the population parameter.
2. Greek letters (μ, σ) represent sample values.
3. SPSS calculates standard deviation using n-1 in the denominator.
4. We use samples because populations are usually too large to study completely.

<details>
<summary>Click to see answers</summary>

1. **False** - Sample statistics are estimates that vary from the true parameter
2. **False** - Greek letters represent population parameters; Roman letters represent sample statistics
3. **True** - SPSS estimates population SD using n-1 (degrees of freedom)
4. **True** - Samples are practical and cost-effective
</details>

---

## Part 7: The Normal Distribution and Z-Scores

### The Normal Distribution (The Bell Curve)

The normal distribution is the most important distribution in statistics.

**Characteristics:**

- **Symmetrical:** Mirror image on both sides of the mean
- **Bell-shaped:** Highest point at the center, tapering off toward the tails
- **Unimodal:** One peak at the mean
- **Mean = Median = Mode:** All three measures of central tendency are equal and located at the center
- **Asymptotic:** The tails never quite touch the x-axis (theoretically extend to infinity)

**Why It's Important:**

1. **Common in nature:** Many human characteristics (height, IQ, blood pressure) are normally distributed
2. **Foundation for inference:** Most statistical tests assume or rely on normality
3. **Predictable proportions:** The percentages of scores in different regions are always the same

### The 68-95-99.7 Rule (Empirical Rule)

In a normal distribution:

- **68%** of scores fall within **1 SD** of the mean (μ ± 1σ)
- **95%** of scores fall within **2 SDs** of the mean (μ ± 2σ)
- **99.7%** of scores fall within **3 SDs** of the mean (μ ± 3σ)

**Example:** IQ scores are normally distributed with μ = 100 and σ = 15

- **68%** of people have IQs between 85 and 115 (100 ± 15)
- **95%** of people have IQs between 70 and 130 (100 ± 30)
- **99.7%** of people have IQs between 55 and 145 (100 ± 45)

**Application:** If someone tells you they have an IQ of 145, you know they're in the top ~0.15% (above 3 SDs from the mean).

### Z-Scores: The Universal Translator

**The Problem:** How can you compare completely different measurements?

- Is a score of 85 on a test good or bad? (Depends on the test difficulty)
- Is being 6 feet tall more unusual than having an IQ of 120? (Different scales!)

**The Solution:** Convert everything to **z-scores**.

**Definition:** A z-score tells you **how many standard deviations** a score is away from the mean.

**Formula:**
\[ z = \frac{X - \mu}{\sigma} \]

Or for a sample:
\[ z = \frac{X - M}{s} \]

Where:

- \(X\) = the individual score
- \(\mu\) or \(M\) = the mean
- \(\sigma\) or \(s\) = the standard deviation

**Interpretation:**

- **z = 0:** Score is exactly at the mean
- **z = +1:** Score is 1 SD above the mean
- **z = -1:** Score is 1 SD below the mean
- **z = +2:** Score is 2 SDs above the mean (better than ~97.5% of scores)
- **z = -2.5:** Score is 2.5 SDs below the mean (worse than ~99% of scores)

### Worked Examples of Z-Scores

**Example 1:** Test scores with M = 75, SD = 10

- **Your score: 85**
  \[ z = \frac{85 - 75}{10} = \frac{10}{10} = +1.0 \]
  **Interpretation:** You scored 1 SD above average, better than about 84% of students

- **Your score: 60**
  \[ z = \frac{60 - 75}{10} = \frac{-15}{10} = -1.5 \]
  **Interpretation:** You scored 1.5 SDs below average, worse than about 93% of students

**Example 2:** Comparing apples and oranges

- **SAT Math:** Score = 650, μ = 500, σ = 100
  \[ z = \frac{650 - 500}{100} = +1.5 \]

- **ACT Math:** Score = 28, μ = 21, σ = 5
  \[ z = \frac{28 - 21}{5} = +1.4 \]

**Question:** Which test performance was better?
**Answer:** SAT (z = +1.5 is more above average than z = +1.4)

### Using Z-Scores to Find Probabilities

With a **z-table** (standard normal table), you can find the proportion of scores below, above, or between any z-score(s).

**Example:** IQ scores: μ = 100, σ = 15
**Question:** What percentage of people have IQ above 115?

**Step 1:** Convert to z-score
\[ z = \frac{115 - 100}{15} = +1.0 \]

**Step 2:** Look up z = 1.0 in a z-table (or remember the 68-95-99.7 rule)

- z = 1.0 means 84% of scores are _below_ this value
- Therefore, 16% are _above_ (100% - 84% = 16%)

**Answer:** 16% of people have IQ above 115

### Properties of Z-Scores

When you convert all scores in a distribution to z-scores:

- **Mean of z-scores = 0**
- **SD of z-scores = 1**
- **Shape stays the same** (if original was normal, z-distribution is normal)

This creates a **standard normal distribution** (μ = 0, σ = 1) that's the same for everyone.

### Real-World Application

**Clinical Psychology:** Depression screening scores (M = 20, SD = 5)

- Your patient scores 32
- \( z = \frac{32-20}{5} = +2.4 \)
- This is more than 2 SDs above the mean → Very high depression symptoms (top ~1% of the population)
- Warrants immediate clinical attention

**Education:** Standardized test scores are often reported as z-scores (or transformations of z-scores)

- SAT scores: Mean = 500, SD = 100 (basically z-scores × 100 + 500)
- IQ scores: Mean = 100, SD = 15 (basically z-scores × 15 + 100)

### Quick Check

Calculate and interpret these z-scores:

1. Reaction time: X = 450ms, M = 500ms, SD = 50ms
2. Height: X = 72 inches, M = 68 inches, SD = 3 inches
3. Which is more extreme: z = -1.8 or z = +1.5?

<details>
<summary>Click to see answers</summary>

1. z = (450-500)/50 = -1.0 → 1 SD faster than average (better performance)
2. z = (72-68)/3 = +1.33 → 1.33 SDs taller than average
3. z = -1.8 is more extreme (farther from zero, more unusual)
</details>

---

## Part 8: Probability and Inference

### What is Probability?

**Definition:** The likelihood of an event occurring, expressed as a number between 0 and 1.

- **p = 0:** Impossible (0% chance)
- **p = 0.50:** Equally likely to occur or not (50% chance)
- **p = 1.0:** Certain (100% chance)

**Examples:**

- Probability of heads on a fair coin flip: p = 0.50
- Probability of rolling a 3 on a six-sided die: p = 1/6 ≈ 0.167
- Probability of drawing a heart from a deck: p = 13/52 = 0.25

### Probability in Normal Distributions

The **area under the curve** represents probability (or proportion of cases).

**Example:** In a normal distribution, what's the probability of randomly selecting someone with a z-score less than -1?

Using the 68-95-99.7 rule:

- 68% fall between z = -1 and z = +1
- That leaves 32% in the two tails
- Half of that (16%) is below z = -1

**Answer:** p = 0.16 (or 16%)

### The Logic of Inferential Statistics (Preview)

Here's the fundamental logic that underlies all hypothesis testing:

**Step 1: Make an Assumption**

- Assume your sample comes from a known population (the "null hypothesis")
- Example: "This group receiving the drug is no different from the general population"

**Step 2: Calculate Probability**

- Given that assumption, what's the probability of getting results as extreme as yours?
- Example: If the drug does nothing, what's the probability of seeing an improvement this large?

**Step 3: Make a Decision**

- **If probability is high** (p > 0.05): Your results look typical → No evidence against the assumption → "We fail to reject the null hypothesis"
- **If probability is low** (p < 0.05): Your results look rare/unusual → Evidence against the assumption → "We reject the null hypothesis"

### Concrete Example: Does This Drug Work?

**Scenario:** A new medication claims to improve memory. Normal memory test scores have μ = 100, σ = 15.

You test 25 patients on the drug. They average M = 108.

**Question:** Is this evidence the drug works, or just random chance?

**Step 1:** Assume the drug does nothing (null hypothesis)

- If true, these patients are just a random sample from the normal population (μ = 100)

**Step 2:** Calculate how unusual this result is

- _Note: The actual calculation involves standard error, which you'll learn about later. For now, focus on the logic._
- Suppose the probability of getting M = 108 or higher (if the drug does nothing) is p = 0.02

**Step 3:** Make a decision

- p = 0.02 means only a 2% chance of this result if the drug has no effect
- This is rare! (Less than our standard cutoff of 5%)
- **Conclusion:** We reject the null hypothesis. The drug probably does improve memory.

**If instead p = 0.25:**

- A 25% chance is not unusual
- **Conclusion:** We fail to reject the null hypothesis. No convincing evidence the drug works.

### The p < 0.05 Convention

**Statistical Significance:** A result is called "statistically significant" if p < 0.05

**What this means:**

- Less than 5% chance of getting this result if the null hypothesis is true
- Conventional cutoff (arbitrary but widely used)
- Doesn't mean "important" or "large"—just "unlikely to be due to chance alone"

**Common Misconception:**
❌ "p < 0.05 means there's a 95% chance my hypothesis is true"
✓ "p < 0.05 means if the null hypothesis were true, I'd get results this extreme less than 5% of the time"

### Sampling Error

**Definition:** The natural variability in sample statistics due to random chance.

**Key Insight:** Every sample is different. If you took 100 samples from the same population, you'd get 100 slightly different means.

**Example:** True population mean IQ = 100

- Sample 1 (n=30): M = 98
- Sample 2 (n=30): M = 102
- Sample 3 (n=30): M = 99.5
- Sample 4 (n=30): M = 101

All four samples come from the same population, but random chance creates variability.

**Implication:** Not all differences between samples indicate real population differences. Statistics helps us distinguish:

- **Real effects** (systematic differences)
- **Sampling error** (random noise)

### Building Toward Hypothesis Testing

Everything in this module builds toward inferential statistics:

1. **Variables** → What we measure
2. **Descriptive statistics** → Summarizing sample data
3. **Sampling** → Understanding the sample-population relationship
4. **Normal distribution** → Model for most inferential tests
5. **Z-scores** → Standardizing scores for comparison
6. **Probability** → Quantifying likelihood
7. **Inference** → Drawing conclusions about populations from samples

**Coming in Module 2:** You'll learn your first formal hypothesis test—the one-sample t-test!

### Why This Matters

Statistical inference allows us to:

- **Test theories** (Does therapy reduce depression?)
- **Make predictions** (Will this student succeed in college?)
- **Inform decisions** (Should we approve this drug?)
- **Generalize findings** (Do results from our lab apply to the real world?)

Without inferential statistics, research would be limited to describing what we directly observe. We couldn't make claims about the broader world.

### Quick Check

1. What does p = 0.03 mean in hypothesis testing?
2. If you reject the null hypothesis, have you "proven" your alternative hypothesis is true?
3. Which provides stronger evidence: p = 0.001 or p = 0.04?

<details>
<summary>Click to see answers</summary>

1. If the null hypothesis were true, we'd see results this extreme only 3% of the time (rare, so we reject the null)
2. No - we've only shown the null hypothesis is unlikely. We haven't "proven" anything; we've provided evidence.
3. p = 0.001 provides stronger evidence (more unlikely under the null hypothesis)
</details>

---

## Part 9: Practical Guide: Working with SPSS

This section provides step-by-step guidance for completing the M1 assignment tasks in SPSS.

### Setting Up Your Dataset

**Step 1: Import Data from Excel**

1. Open SPSS
2. `File → Import Data → Excel`
3. Navigate to your data file
4. Select the worksheet containing your data
5. **Important:** Check "Read variable names from the first row of data"
6. Click OK

**Step 2: Configure Variables in Variable View**

After importing, click the **Variable View** tab at the bottom of the screen. This is where you define how SPSS interprets each variable.

**For Each Variable, Set:**

**a) Name:**

- Short, descriptive, no spaces
- Examples: `Age`, `Gender`, `Sleep_Hours`

**b) Type:**

- Usually "Numeric" (default)
- Use "String" only for text data like ID codes

**c) Width & Decimals:**

- Set decimals to 0 for whole numbers (age, counts)
- Set decimals to 1-2 for continuous measurements

**d) Label:**

- A longer, descriptive label
- Example: Name = `Sleep_Hours`, Label = `Hours of sleep per night`

**e) Values** (CRITICAL for categorical variables):

- Click in the Values cell → Click the `...` button
- For each numeric code, enter the value and its label:
  - Value: `1`, Label: `Male` → Add
  - Value: `2`, Label: `Female` → Add
  - Continue for all categories
- **Do this for EVERY nominal and ordinal variable!**

**f) Measure:**

- **Scale:** For continuous numerical data (age, test scores, income)
- **Ordinal:** For ranked categories (education level, class standing)
- **Nominal:** For unordered categories (gender, major, treatment group)

**Getting the Measure Right is Critical!** This determines which analyses SPSS will allow.

**Step 3: Save Your Work**

- `File → Save As`
- Save as a `.sav` file (SPSS data file)
- Also save output: `File → Save` in the Output window (creates `.spv` file)

### Creating Frequency Tables

**For Categorical Variables (Nominal/Ordinal):**

1. `Analyze → Descriptive Statistics → Frequencies`
2. Move your categorical variable(s) to the "Variable(s)" box
3. Click OK

**Reading the Output:**

- **Frequency:** Count in each category
- **Percent:** Percentage of total (including missing)
- **Valid Percent:** Percentage excluding missing data (usually what you report)
- **Cumulative Percent:** Running total (useful for ordinal data)

### Creating Grouped Frequency Tables

**For Scale Variables (to create bins):**

**Step 1: Use Visual Binning**

1. `Transform → Visual Binning`
2. Move your scale variable to "Variables to Bin" → Continue
3. Enter a name for your new binned variable (e.g., `Age_Grouped`)
4. Click `Make Cutpoints`
5. Select "Equal Width Intervals"
6. Set:
   - **First Cutpoint Location:** At or below your minimum value
   - **Number of Cutpoints:** One less than the number of bins you want (for 8 bins, enter 7)
   - **Width:** The size of each interval
7. Click Apply → OK

**Step 2: Create Frequency Table**

1. `Analyze → Descriptive Statistics → Frequencies`
2. Select your NEW binned variable
3. Click OK

### Creating Graphs

**Bar Chart (for Nominal/Ordinal Data):**

1. `Graphs → Chart Builder`
2. In the Gallery, select **Bar**
3. Drag "Simple Bar" to the chart preview area
4. Drag your categorical variable from the Variables list to the **X-Axis**
5. Y-Axis will automatically be "Count"
6. Click OK
7. Double-click the graph in output to edit (add title, format labels)

**Histogram (for Scale Data):**

1. `Graphs → Chart Builder`
2. In the Gallery, select **Histogram**
3. Drag "Simple Histogram" to the chart preview area
4. Drag your scale variable to the **X-Axis**
5. Optional: Check "Display normal curve" in Element Properties
6. Click OK
7. Double-click the graph to edit

**Graph Formatting Tips:**

- Always include a descriptive title
- Label axes clearly
- For bar charts, consider ordering bars by frequency or logical order
- Remove unnecessary gridlines for cleaner appearance

### Calculating Descriptive Statistics

**Method 1: For Basic Statistics (Mean, SD, Range)**

1. `Analyze → Descriptive Statistics → Descriptives`
2. Move your scale variable(s) to "Variable(s)"
3. Click `Options` to select which statistics to display:
   - Mean
   - Std. deviation
   - Minimum, Maximum (to calculate range)
4. Click Continue → OK

**Method 2: For Median and More Detail**

1. `Analyze → Descriptive Statistics → Frequencies`
2. Move your scale variable to "Variable(s)"
3. **Uncheck** "Display frequency tables" (unless you want them)
4. Click `Statistics` button
5. Select:
   - Mean, Median, Mode
   - Std. deviation, Variance
   - Range, Minimum, Maximum
6. Click Continue → OK

**Reading SPSS Output:**

- **N:** Sample size
- **Mean:** Average
- **Std. Deviation:** Standard deviation (calculated using n-1)
- **Variance:** SD squared
- **Minimum/Maximum:** Lowest and highest values
- **Range:** Maximum - Minimum (if reported)

### Common SPSS Errors and Troubleshooting

**Problem:** SPSS won't let me create a histogram for my variable
**Solution:** Check that the variable's Measure is set to "Scale" in Variable View

**Problem:** My frequency table shows numbers (1, 2, 3) instead of labels (Male, Female, Other)
**Solution:** You didn't define Value Labels in Variable View. Go back and add them.

**Problem:** SPSS is including missing data in my percentages
**Solution:** Report "Valid Percent" instead of "Percent" (excludes missing)

**Problem:** My histogram has too many/too few bars
**Solution:** Double-click the graph and adjust bin width in the chart editor

**Problem:** I can't find my output
**Solution:** Look for a separate Output window. If closed, you can reopen saved .spv files

### Try It Yourself: Practice Exercise

Using the M1 assignment data:

1. Import the data and configure all variables with appropriate:

   - Measure types (Nominal, Ordinal, or Scale)
   - Value labels for all categorical variables

2. Create a frequency table for Employment Status

3. Create a bar chart for Computer Type

4. Create a grouped frequency table for Age (use Visual Binning with 8 equal-width bins)

5. Create a histogram for Hours of Sleep

6. Calculate mean, median, SD, and range for Cell Phone Minutes

**Check Your Understanding:**

- Does your employment frequency table show text labels or just numbers?
- Do the bars in your computer type bar chart have gaps between them?
- Does your age frequency table have 8 rows (bins)?
- Do the bars in your sleep histogram touch each other?
- Is your mean for cell phone minutes reasonable given the range?

---

## Summary and Key Formulas

### Core Concepts

**Statistics:** Mathematical tools for organizing, summarizing, and interpreting data

**Two Branches:**

- **Descriptive:** Summarize the data you have
- **Inferential:** Make predictions about populations from samples

**Variables:** Characteristics that vary between individuals or situations

**Classification:**

- By role: Independent (predictor) vs. Dependent (outcome)
- By scale: Nominal (categories) → Ordinal (ranked) → Scale (true numbers)

### Measures of Central Tendency

**Mean:**
\[ M = \frac{\sum X}{N} \]

- Best for: Symmetrical distributions, no outliers
- Sensitive to: Extreme values

**Median:** Middle score when ordered

- Best for: Skewed distributions, ordinal data
- Resistant to: Outliers

**Mode:** Most frequent value

- Best for: Nominal data, identifying peaks
- Can have: Multiple modes or no mode

### Measures of Variability

**Range:**
\[ \text{Range} = X*{max} - X*{min} \]

**Variance (Population):**
\[ \sigma^2 = \frac{\sum(X-\mu)^2}{N} \]

**Variance (Sample Estimate):**
\[ s^2 = \frac{\sum(X-M)^2}{n-1} \]

**Standard Deviation:**
\[ \sigma = \sqrt{\sigma^2} \text{ or } s = \sqrt{s^2} \]

- Interpretation: Average distance from the mean
- Small SD = less variability (homogeneous group)
- Large SD = more variability (heterogeneous group)

### Z-Scores

**Formula:**
\[ z = \frac{X - \mu}{\sigma} \text{ or } z = \frac{X - M}{s} \]

**Interpretation:**

- Number of standard deviations from the mean
- z = 0 → at the mean
- z = +1 → 1 SD above mean
- z = -1.5 → 1.5 SDs below mean

**68-95-99.7 Rule:**

- 68% within 1 SD (z = ±1)
- 95% within 2 SDs (z = ±2)
- 99.7% within 3 SDs (z = ±3)

### Symbols Reference

| Concept            | Population         | Sample               |
| :----------------- | :----------------- | :------------------- |
| Size               | \(N\)              | \(n\)                |
| Mean               | \(\mu\) (mu)       | \(M\) or \(\bar{X}\) |
| Standard Deviation | \(\sigma\) (sigma) | \(s\) or \(SD\)      |
| Variance           | \(\sigma^2\)       | \(s^2\)              |

### Key Distinctions

| Descriptive vs. Inferential                         |
| :-------------------------------------------------- |
| **Descriptive:** Summarize collected data           |
| **Inferential:** Make predictions about populations |

| Sample vs. Population                      |
| :----------------------------------------- |
| **Sample:** Subset studied                 |
| **Population:** Entire group of interest   |
| **Statistic:** Describes sample (M, s)     |
| **Parameter:** Describes population (μ, σ) |

| Nominal vs. Ordinal vs. Scale                         |
| :---------------------------------------------------- |
| **Nominal:** Categories, no order                     |
| **Ordinal:** Ranked categories, unequal intervals     |
| **Scale:** True numbers, equal intervals, can do math |

### Analysis Decision Guide

**What graph should I use?**

- Nominal/Ordinal → Bar chart or pie chart
- Scale → Histogram

**What central tendency should I report?**

- Nominal → Mode only
- Ordinal → Median (and mode)
- Scale (symmetrical) → Mean (and SD)
- Scale (skewed) → Median (and range/IQR)

**When should I use n vs. n-1?**

- Describing only your sample → divide by n
- Estimating population from sample → divide by n-1
- **SPSS always uses n-1** (assumes you're inferring)

---

## Glossary

**Bar Chart:** Graph for categorical data with separated bars

**Central Tendency:** The "typical" or "center" value (mean, median, mode)

**Continuous Variable:** Can take any value within a range

**Dependent Variable (DV):** The outcome being measured

**Descriptive Statistics:** Tools to summarize collected data

**Discrete Variable:** Can only take specific values

**Frequency Distribution:** Summary of how often each value occurs

**Histogram:** Graph for continuous data with touching bars

**Independent Variable (IV):** The predictor or presumed cause

**Inferential Statistics:** Tools to make predictions about populations from samples

**Mean:** Arithmetic average

**Median:** Middle score when ordered

**Mode:** Most frequent value

**Nominal:** Categorical data with no inherent order

**Normal Distribution:** Symmetrical, bell-shaped distribution

**Ordinal:** Ranked categories with unequal intervals

**Outlier:** An extremely unusual value

**Parameter:** A measure describing a population (μ, σ)

**Population:** The entire group of interest

**Range:** Distance between highest and lowest scores

**Sample:** A subset of the population actually studied

**Scale:** Continuous numerical data with equal intervals

**Standard Deviation:** Average distance from the mean

**Statistic:** A measure describing a sample (M, s)

**Variable:** A characteristic that varies between individuals

**Variance:** Average squared deviation from the mean

**Z-Score:** Number of standard deviations from the mean

---

## Frequently Asked Questions

**Q: Why do we study samples instead of populations?**
A: Populations are usually too large, expensive, or impossible to study completely. A well-selected sample provides accurate estimates at a fraction of the cost and time.

**Q: When should I use mean vs. median?**
A: Use the mean for symmetrical distributions without extreme outliers. Use the median for skewed distributions or when outliers are present. The median is also appropriate for ordinal data.

**Q: What's the difference between variance and standard deviation?**
A: Variance is the average squared deviation. Standard deviation is the square root of variance, returning the measure to the original units. SD is easier to interpret because it's in the same units as your data.

**Q: Why does SPSS divide by n-1 instead of n?**
A: SPSS assumes you want to estimate population parameters from your sample. Dividing by n-1 corrects for the tendency of samples to underestimate population variability.

**Q: What does "statistically significant" mean?**
A: It means the probability of getting your results (if the null hypothesis were true) is less than 5% (p < 0.05). It suggests your results are unlikely to be due to chance alone.

**Q: Can I calculate a mean for nominal data?**
A: Technically you can, but it's meaningless. If gender is coded 1=Male, 2=Female, a mean of 1.6 tells you nothing useful. Only calculate means for scale data.

**Q: What's the difference between a bar chart and a histogram?**
A: Bar charts are for categorical data (bars have gaps). Histograms are for continuous data (bars touch). The gaps in bar charts emphasize that categories are distinct.

**Q: How do I know if my distribution is normal?**
A: Create a histogram and look for a symmetrical, bell-shaped curve. For formal testing, you can use tests like Shapiro-Wilk (covered in advanced courses), but visual inspection is usually sufficient at this level.

**Q: What's a "good" standard deviation?**
A: There's no universal answer. SD depends on the scale of measurement. What matters is interpreting it in context: small SD means consistency, large SD means variability.

**Q: Why can't I use certain tests with ordinal data?**
A: Many powerful statistical tests assume interval/ratio data with equal intervals. Ordinal data violates this assumption. You can use specialized non-parametric tests for ordinal data.

---

## Connections to Future Modules

**Module 1 Foundation →**

**Module 2 (One-Sample t-Test):**

- Uses z-score logic extended to t-distributions
- Compares sample mean to known population
- Applies hypothesis testing framework introduced here

**Module 3 (Independent & Paired t-Tests):**

- Compares means between two groups or conditions
- Uses SD to quantify variability in both groups
- IV/DV distinction becomes critical

**Module 4 (ANOVA):**

- Extends t-test logic to 3+ groups
- Heavy reliance on variance calculations
- Uses F-ratio (ratio of variances)

**Module 5 (Two-Way ANOVA):**

- Multiple IVs with one DV
- Everything from M1 about variables applies

**Module 6 (Correlation & Regression):**

- Relationship between two scale variables
- Z-scores used in correlation calculations
- Both variables often treated as continuous

**The Through-Line:** Every module builds on these fundamentals. Understanding variables, distributions, means, and standard deviations is essential for all future statistical analyses.

---

## Final Thoughts

Statistics is not just about numbers and formulas—it's about **thinking critically about evidence**. The concepts in this module form the foundation for understanding how we:

- Transform messy real-world observations into organized data
- Summarize complex patterns into interpretable statistics
- Make informed decisions despite uncertainty
- Distinguish signal from noise

As you work through the M1 assignment, focus not just on getting the right answers, but on understanding **why** we do each step. When you calculate a standard deviation, think about what it tells you. When you create a histogram, consider what patterns the shape reveals. When you compare your manual calculations to SPSS output, reflect on the purpose of the n-1 adjustment.

These fundamental statistical reasoning skills will serve you throughout your academic career and beyond—whether you're reading research papers, evaluating news headlines, or making data-driven decisions in your future career.

**You've got this!** Statistics builds logically, step by step. Master these foundations, and everything that follows will make sense.

---

_Remember: The goal isn't to memorize formulas—it's to understand the logic behind them. When in doubt, think about what the numbers mean in the context of your research question._
