---
layout: default
title: "Module 6: Correlation and Regression"
---

# Module 6: Correlation and Regression

## Learning Objectives

By the end of this lecture, you should be able to:

1. Distinguish between correlation and regression analyses
2. Run and interpret bivariate correlations in SPSS
3. Identify the strongest correlation among multiple variables
4. Understand and apply the regression equation (Ŷ = bX + a)
5. Calculate predicted values using regression equations
6. Interpret omnibus F-tests for regression models
7. Report degrees of freedom correctly for regression analyses
8. Understand R² and Adjusted R² as effect size measures
9. Distinguish between bivariate and multiple regression
10. Understand unique contributions of predictors in multiple regression
11. Interpret standardized beta (β) coefficients
12. Understand and detect multicollinearity
13. Compare regression models using Adjusted R²
14. Report regression results in proper APA format

---

## Table of Contents

1. [Introduction to Correlation and Regression](#part-1-introduction-to-correlation-and-regression)
2. [Bivariate Correlation](#part-2-bivariate-correlation)
3. [The Regression Equation](#part-3-the-regression-equation)
4. [Bivariate Regression (Simple Linear Regression)](#part-4-bivariate-regression-simple-linear-regression)
5. [Multiple Regression Fundamentals](#part-5-multiple-regression-fundamentals)
6. [Understanding Unique Contributions](#part-6-understanding-unique-contributions)
7. [Multicollinearity](#part-7-multicollinearity)
8. [Model Building and Comparison](#part-8-model-building-and-comparison)
9. [SPSS Practical Guide](#part-9-spss-practical-guide)
10. [Reporting Regression in APA Format](#part-10-reporting-regression-in-apa-format)
11. [Summary and Key Formulas](#part-11-summary-and-key-formulas)

---

## Part 1: Introduction to Correlation and Regression

### 1.1 A Fundamental Shift in Research Questions

Throughout this course, we've focused on **comparing groups**: Does Group A differ from Group B? Do treatment groups show different outcomes? These questions led us through t-tests and ANOVA.

Now we shift to a fundamentally different type of question: **What is the relationship between two variables?** Instead of dividing participants into groups and comparing means, we examine how two continuous (scale) variables **co-vary** together.

**Examples of Relational Questions:**

- How does study time relate to exam scores?
- Is there a relationship between exercise frequency and stress levels?
- Can we predict job performance from personality test scores?
- How do age, income, and education together predict life satisfaction?

### 1.2 Linear Relationships and Scatterplots

The foundation of correlation and regression is the **linear relationship**, visualized through a **scatterplot**.

**Scatterplot Basics:**

- Each point represents **one participant** with scores on both variables
- The **X-axis** (horizontal) shows the predictor variable
- The **Y-axis** (vertical) shows the outcome variable
- The **pattern of points** reveals the relationship

**Types of Relationships:**

**Positive Linear Relationship:**

- As X increases, Y tends to increase
- Points cluster around an upward-sloping line
- Example: Hours studying and exam scores

**Negative Linear Relationship:**

- As X increases, Y tends to decrease
- Points cluster around a downward-sloping line
- Example: Hours of sleep deprivation and cognitive performance

**No Relationship:**

- Points scattered randomly with no discernible pattern
- Knowing X tells you nothing about Y
- Example: Shoe size and IQ scores

**Non-Linear Relationship:**

- Points follow a curved pattern (not a straight line)
- Important: Correlation and regression only detect **linear** relationships
- Example: Arousal and performance (inverted U-shape)

### 1.3 Correlation vs. Regression vs. Multiple Regression

While these techniques are related, they serve different purposes:

**Bivariate Correlation:**

- **Purpose:** Describe the strength and direction of the relationship
- **Question:** "How closely are X and Y related?"
- **Symmetrical:** Correlating X with Y gives the same result as Y with X
- **Output:** Correlation coefficient (r) and coefficient of determination (r²)
- **Does not** imply prediction or causation

**Bivariate Regression (Simple Linear Regression):**

- **Purpose:** Use one variable to predict another
- **Question:** "How well can X predict Y?"
- **Directional:** X is explicitly the predictor (IV), Y is the outcome (DV)
- **Output:** Regression equation, F-test, R², slopes, and intercepts
- **Allows** prediction but does not prove causation

**Multiple Regression:**

- **Purpose:** Use multiple variables to predict an outcome
- **Question:** "How well can X₁, X₂, and X₃ together predict Y?"
- **Directional:** Multiple predictors (IVs) predict one outcome (DV)
- **Output:** Same as bivariate regression, plus unique contributions of each predictor
- **Advantage:** Accounts for overlap between predictors

### 1.4 When to Use Each Approach

**Use Bivariate Correlation when:**

- You want to describe how two variables are related
- You're exploring relationships without making predictions
- You're checking assumptions (e.g., multicollinearity)
- Example: "Are anxiety and depression correlated in college students?"

**Use Bivariate Regression when:**

- You have one predictor and one outcome
- You want to make predictions
- You want to test if the predictor significantly predicts the outcome
- Example: "Can GRE scores predict first-year graduate GPA?"

**Use Multiple Regression when:**

- You have multiple predictors for one outcome
- You want to know each predictor's unique contribution
- You want the most powerful predictive model
- Example: "Can GRE scores, undergraduate GPA, and research experience together predict graduate success?"

### 1.5 The Importance of Visualization

**Always examine your scatterplot first!**

Why? Because correlation and regression assume a **linear** relationship. If the relationship is:

- **Curvilinear:** You'll underestimate the true relationship
- **Contains outliers:** A few extreme points can distort your results
- **Non-existent:** You might find spurious relationships

**Key Principle:** Never run correlation or regression blindly. **Look at your data first.**

---

## Part 2: Bivariate Correlation

### 2.1 The Pearson Correlation Coefficient (r)

The **Pearson product-moment correlation coefficient** (usually just called "r") is a single number that summarizes the **strength** and **direction** of a linear relationship between two scale variables.

**Properties of r:**

**Range:**

- r ranges from **-1.0 to +1.0**
- r = +1.0: Perfect positive relationship (all points fall exactly on an upward-sloping line)
- r = -1.0: Perfect negative relationship (all points fall exactly on a downward-sloping line)
- r = 0: No linear relationship (points are scattered randomly)

**Sign (Direction):**

- **Positive (+):** As one variable increases, the other tends to increase
- **Negative (-):** As one variable increases, the other tends to decrease

**Magnitude (Strength):**

- We interpret the **absolute value** of r (ignoring the sign)
- Common guidelines (Cohen, 1988):
  - |r| = .10: Small effect
  - |r| = .30: Medium effect
  - |r| = .50: Large effect
- Note: These are guidelines, not rigid rules. Context matters!

**Examples:**

- r = +.75: Strong positive relationship
- r = -.40: Moderate negative relationship
- r = +.05: Virtually no relationship

### 2.2 The Coefficient of Determination (r²)

While r tells us about strength and direction, **r²** provides the most intuitive interpretation of effect size.

**What r² Means:**

**r² represents the proportion (or percentage) of variance in one variable that is "explained" or "shared" with the other variable.**

**Calculation:**
Simply square the correlation coefficient: r² = r × r

**Interpretation:**

- r² ranges from 0 to 1.0 (or 0% to 100%)
- Multiply by 100 to get percentage of explained variance
- The remaining variance (1 - r²) is unexplained or error variance

**Example:**

- If r = +.70, then r² = .49
- Interpretation: "49% of the variance in Y is explained by X"
- Or: "49% of individual differences in Y can be accounted for by individual differences in X"
- The remaining 51% is due to other factors

**Why r² is More Intuitive:**

Compare these two correlations:

- r = .30 vs. r = .60

At first glance, .60 seems "twice as strong" as .30. But look at r²:

- r² = .09 (9% variance explained)
- r² = .36 (36% variance explained)

The second correlation actually explains **four times** as much variance, not twice as much!

### 2.3 Interpreting Correlation Strength in Context

While Cohen's guidelines are helpful, **context is king**:

**In Physics or Chemistry:**

- r = .90 might be considered weak (high precision expected)

**In Psychology or Social Sciences:**

- r = .30 might be considered substantial (human behavior is complex)

**In Medical Research:**

- Even r = .10 might be clinically important if it relates to life-saving interventions

**Important:** Don't just recite "small, medium, large." Consider:

- What is typical in this field?
- What is the practical significance?
- What are the consequences of the relationship?

### 2.4 Correlation Does NOT Equal Causation

This is perhaps the most important principle in correlational research:

**A significant correlation between X and Y does NOT prove that X causes Y.**

**Why not?**

**1. Directionality Problem:**

- If ice cream sales and drowning deaths are correlated, does ice cream cause drowning?
- Or does drowning cause ice cream sales?
- Actually, neither!

**2. Third Variable Problem (Confounds):**

- Both variables might be caused by a third, unmeasured variable
- In the example above: Hot weather increases both ice cream sales AND swimming (leading to more drownings)
- The correlation is **spurious** (fake relationship)

**3. Coincidence:**

- Sometimes unrelated variables correlate by chance
- Websites like "Spurious Correlations" show hilarious examples (e.g., margarine consumption and divorce rates)

**What CAN correlation tell us?**

- Two variables are **related**
- They **co-vary together**
- Knowing one provides **information** about the other
- There's a **potential** avenue for further investigation

**To establish causation, you need:**

- **Experimental design** with random assignment
- **Temporal precedence** (cause comes before effect)
- **Control** over confounding variables

### 2.5 Running Correlations in SPSS

**Step-by-Step: Bivariate Correlations**

1. **Analyze → Correlate → Bivariate**

2. **Select variables:** Move all variables you want to correlate into the "Variables" box

   - You can select 2, 3, 4, or more variables
   - SPSS will create a correlation matrix with all pairwise correlations

3. **Correlation Coefficient:** Ensure "Pearson" is checked (default)

4. **Test of Significance:** Ensure "Two-tailed" is checked (unless you have a directional hypothesis)

5. **Flag significant correlations:** Check "Flag significant correlations" (adds asterisks)

6. **Click OK**

**Reading the Output: Correlation Matrix**

SPSS produces a **correlation matrix** (a table showing all pairwise correlations):

```
              Variable1  Variable2  Variable3
Variable1         1.000      .652**     .301*
Variable2          .652**   1.000      .458**
Variable3          .301*     .458**    1.000
```

**Interpreting the Matrix:**

- **Diagonal:** Always 1.000 (each variable correlates perfectly with itself)
- **Above/Below diagonal:** Mirror images (correlation is symmetrical)
- **Asterisks:** \* = p < .05, \*\* = p < .01
- **Find the strongest correlation:** Look for the largest absolute value (ignoring sign)

**Example Question:**
"Which variable has the strongest correlation with Acceleration?"

**Answer:** Look down the "Acceleration" column (or across the row), find the highest absolute value, ignoring the diagonal.

### 2.6 Interpreting Correlation Results

**Example Output:**

```
Correlations between Study Hours and Exam Score:
r = .68, p < .001
```

**What this means:**

1. **Direction:** Positive relationship (more study = higher scores)
2. **Strength:** r = .68 is a strong relationship
3. **Effect Size:** r² = .46, so 46% of variance in exam scores is explained by study hours
4. **Significance:** p < .001, so this relationship is extremely unlikely due to chance
5. **Practical Importance:** Knowing study hours provides substantial information about likely exam performance

**What this does NOT mean:**

- Studying causes higher scores (could be that smarter students both study more AND score higher)
- 68% of students who study more will score higher (r is not a percentage of people)
- You can predict exact scores (there's still 54% unexplained variance)

---

## Part 3: The Regression Equation

### 3.1 The Line of Best Fit

While correlation describes the relationship, regression goes further by **fitting a line** through the data points.

**The Goal of Regression:**
Find the one straight line that **best represents** the relationship between X and Y. This line minimizes the total distance between the line and all the individual data points.

**The Method:** Ordinary Least Squares (OLS)

- Calculates the **vertical distance** from each point to the line
- These distances are called **residuals** or **errors**
- Squares each residual (to make negative values positive)
- Finds the line that makes the sum of squared residuals as small as possible
- Hence: "Least Squares"

**Why is this useful?**
Once we have the line, we can use it to **make predictions** for new values of X.

### 3.2 The Regression Equation

Every straight line can be represented by an equation. The regression equation is:

**Ŷ = bX + a**

**Components:**

**Ŷ (pronounced "Y-hat"):**

- The **predicted value** of the outcome variable
- This is our best guess for Y based on knowing X
- It's an estimate, not a guarantee

**X:**

- The **known value** of the predictor variable
- The value we plug into the equation
- Must be within the range of X values in your data (don't extrapolate wildly)

**b (the slope):**

- Tells you **how much Y is predicted to change** for every one-unit increase in X
- **Positive b:** Y increases as X increases (upward slope)
- **Negative b:** Y decreases as X increases (downward slope)
- **b = 0:** No relationship (horizontal line)

**a (the y-intercept):**

- The **predicted value of Y when X = 0**
- Where the regression line crosses the Y-axis
- May or may not have practical meaning (depends on whether X = 0 makes sense)

### 3.3 Understanding the Slope (b)

The slope is the **heart of the regression equation**. It quantifies the relationship.

**Interpreting the Slope:**

**Example 1: Positive Slope**

- Equation: Ŷ (Exam Score) = 3.5(Study Hours) + 45
- Slope (b) = 3.5
- **Interpretation:** "For every additional hour of studying, exam scores are predicted to increase by 3.5 points, on average."

**Example 2: Negative Slope**

- Equation: Ŷ (Stress) = -2.1(Exercise Hours) + 75
- Slope (b) = -2.1
- **Interpretation:** "For every additional hour of exercise per week, stress scores are predicted to decrease by 2.1 points, on average."

**Example 3: Near-Zero Slope**

- Equation: Ŷ (Happiness) = 0.02(Shoe Size) + 50
- Slope (b) = 0.02
- **Interpretation:** "Shoe size has virtually no predictive relationship with happiness. For every unit increase in shoe size, happiness is predicted to increase by only 0.02 points—essentially negligible."

**Key Point:** The slope is in **the units of your variables**. Always include units when interpreting!

### 3.4 Understanding the Y-Intercept (a)

The y-intercept is where the line crosses the Y-axis (when X = 0).

**When the Intercept is Meaningful:**

- Equation: Ŷ (Distance) = 60(Time) + 0
- Intercept (a) = 0
- **Interpretation:** "When time = 0 hours, the car has traveled 0 miles." Makes sense!

**When the Intercept is Not Meaningful:**

- Equation: Ŷ (Salary) = 2000(Years of Education) + 10,000
- Intercept (a) = 10,000
- **Interpretation:** "When years of education = 0, predicted salary is $10,000."
- Problem: Nobody in your sample had 0 years of education. This is **extrapolation beyond your data** and may not be accurate.

**Key Principle:** The intercept is often less important than the slope for interpretation. Focus on the slope for understanding the relationship.

### 3.5 Making Predictions with the Equation

Once you have the regression equation, you can make predictions for new values of X.

**Example Equation:**
Ŷ (Exam Score) = 3.5(Study Hours) + 45

**Prediction Question:**
"What exam score would we predict for a student who studies 8 hours?"

**Calculation:**

1. Plug in X = 8
2. Ŷ = 3.5(8) + 45
3. Ŷ = 28 + 45
4. Ŷ = 73

**Answer:** We predict an exam score of 73 points.

**Important Caveats:**

**1. It's a Prediction, Not a Guarantee:**

- The actual student might score 65 or 82
- There's always error/residual variance
- Ŷ represents the **average** predicted value for people with X = 8

**2. Stay Within the Range of Your Data:**

- If your data ranged from 1-15 study hours, don't predict for 30 hours
- **Extrapolation** (predicting beyond your data) is risky
- The relationship might not be linear outside your observed range

**3. Remember: Correlation ≠ Causation:**

- Predicting doesn't mean causing
- We can predict Y from X without X causing Y
- Example: Ice cream sales predict drowning deaths, but don't cause them

### 3.6 Calculating Predicted Values Step-by-Step

Let's practice with a more complex example.

**Given:**

- Equation: Ŷ (Cholesterol) = 5(Saturated Fat) - 4(Exercise Hours) + 130
- Saturated Fat = 15 grams per day
- Exercise Hours = 1 hour per day

**Step 1:** Identify your equation components

- Slope for Saturated Fat (b₁) = 5
- Slope for Exercise Hours (b₂) = -4
- Intercept (a) = 130

**Step 2:** Plug in the values

- Ŷ = 5(15) - 4(1) + 130

**Step 3:** Calculate each term

- 5(15) = 75
- -4(1) = -4
- Intercept = 130

**Step 4:** Add them up

- Ŷ = 75 - 4 + 130
- Ŷ = 201

**Answer:** The predicted cholesterol level is 201.

**Interpretation:**
"For an individual who consumes 15 grams of saturated fat daily and exercises 1 hour per day, we predict a cholesterol level of 201."

---

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Regression Equation</h4>

  <div class="quiz-question">
    <p><strong>Question 1:</strong> In the equation Ŷ = 98 + 4.30(X₁) + 7.20(X₂), what is/are the slope(s)?</p>
    <div class="options">
      <p>A) 7.20</p>
      <p>B) 4.30</p>
      <p>C) 98</p>
      <p>D) 4.30 and 7.20</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> D) 4.30 and 7.20</p>

      <p class="explanation"><strong>Why this is correct:</strong> In a multiple regression equation, there is one slope for each predictor variable. Here, 4.30 is the slope for X₁ and 7.20 is the slope for X₂. Both are slopes (b coefficients).</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) 7.20 only:</strong> This is one slope, but it's not the only slope in the equation.</li>
        <li><strong>B) 4.30 only:</strong> This is one slope, but it's not the only slope in the equation.</li>
        <li><strong>C) 98:</strong> This is the y-intercept (a), not a slope. It's the predicted value when all X variables equal 0.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 3.2: The Regression Equation for the components of Ŷ = bX + a.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 2:</strong> In the equation Ŷ = 130 + 5(X₁) + 3(X₂), what is the y-intercept?</p>
    <div class="options">
      <p>A) 3</p>
      <p>B) 130</p>
      <p>C) 5</p>
      <p>D) 8</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) 130</p>

      <p class="explanation"><strong>Why this is correct:</strong> The y-intercept is the constant term in the regression equation—the value that remains when all X variables equal 0. In this equation, 130 is the y-intercept (a).</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) 3:</strong> This is the slope (b₂) for the second predictor variable X₂.</li>
        <li><strong>C) 5:</strong> This is the slope (b₁) for the first predictor variable X₁.</li>
        <li><strong>D) 8:</strong> This is the sum of the two slopes (5 + 3), which has no special meaning in regression.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 3.4: Understanding the Y-Intercept (a).</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 3:</strong> In a study designed to predict blood cholesterol levels from amount of daily saturated fat in grams (X₁) and the number of hours of daily exercise (X₂), the slope of X₁ is 5, the slope of X₂ is -4, and the y-intercept is 130. If an individual reports that he or she typically eats 15 grams of saturated fat daily and exercises 1 hour every day, what would be the predicted cholesterol level for this individual?</p>
    <div class="options">
      <p>A) 145</p>
      <p>B) 75</p>
      <p>C) 180</p>
      <p>D) 201</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> D) 201</p>

      <p class="explanation"><strong>Why this is correct:</strong> Using the regression equation Ŷ = 5(X₁) - 4(X₂) + 130, we plug in X₁ = 15 and X₂ = 1:
        <br>Ŷ = 5(15) - 4(1) + 130
        <br>Ŷ = 75 - 4 + 130
        <br>Ŷ = 201</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) 145:</strong> This might result from forgetting to include all terms or calculation errors.</li>
        <li><strong>B) 75:</strong> This is only the contribution from saturated fat (5 × 15), not the complete prediction.</li>
        <li><strong>C) 180:</strong> This might result from using +4 instead of -4 for the exercise slope, or other calculation errors.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 3.6: Calculating Predicted Values Step-by-Step.</p>
    </div>

  </details>

</div>

---

## Part 4: Bivariate Regression (Simple Linear Regression)

### 4.1 From Description to Prediction

While correlation simply describes the relationship between two variables, **regression** takes the next step: using one variable to **predict** another.

**Key Distinction:**

- **Correlation:** Symmetrical relationship (X with Y = Y with X)
- **Regression:** Directional prediction (X predicts Y, but not necessarily vice versa)

**In Regression, We Explicitly Define:**

- **Predictor (IV):** The variable we use to make predictions (X)
- **Outcome (DV):** The variable we're trying to predict (Ŷ)

**Example:**

- Correlation: "Study hours and exam scores are correlated at r = .68"
- Regression: "Study hours (predictor) significantly predict exam scores (outcome), F(1, 48) = 32.15, p < .001"

### 4.2 The Omnibus F-Test

The first and most important result in regression is the **omnibus F-test** (also called the "overall model test").

**What It Tests:**

**H₀ (Null Hypothesis):**

- The regression model does NOT significantly predict the outcome variable
- The slope of the regression line equals 0 (b = 0)
- Knowing X provides no better prediction than just guessing the mean of Y

**H₁ (Alternative Hypothesis):**

- The regression model DOES significantly predict the outcome
- The slope is significantly different from 0 (b ≠ 0)
- Knowing X improves our prediction beyond just guessing the mean

**The F-Statistic:**

Just like in ANOVA, the F-statistic represents a ratio:

**F = Variance Explained by the Model / Variance Not Explained (Error)**

**Interpretation:**

- **F > 1:** Model explains more variance than error (good sign)
- **F >> 1:** Model explains much more variance than error (better!)
- **F ≈ 1:** Model is no better than chance
- **F < 1:** Something went wrong (F can't be less than 0, but can be close to 0)

**Example:**
F(1, 48) = 32.15, p < .001

**What this means:**

- The model explains 32 times more variance than error variance
- This is extremely unlikely to occur by chance (p < .001)
- Therefore, we reject H₀: The model significantly predicts the outcome

### 4.3 Degrees of Freedom for Regression

Regression has two df values, just like ANOVA:

**df₁ (Model df):**

- df₁ = k (number of predictors)
- For bivariate regression: df₁ = 1 (one predictor)
- For multiple regression with 3 predictors: df₁ = 3

**df₂ (Error df):**

- df₂ = N - k - 1
- N = total sample size
- k = number of predictors

**Example:**

- Sample size = 207
- Number of predictors = 1
- df₁ = 1
- df₂ = 207 - 1 - 1 = 205
- APA format: F(1, 205) = ...

**Why These Matter:**

- Needed for APA-style reporting
- Indicate sample size and model complexity
- Used to look up critical values (if not using p-values)

### 4.4 R² and Adjusted R²

The **Model Summary** table provides the effect size for your regression model.

**R² (R-squared):**

- Same concept as r² in correlation
- **Proportion of variance in the outcome (DV) explained by the model**
- Ranges from 0 to 1.0 (or 0% to 100%)

**Adjusted R²:**

- A more conservative estimate of R²
- Adjusts for the number of predictors in the model
- Penalizes you for adding predictors that don't improve the model much
- Always slightly smaller than R² (unless you have only one predictor)
- **This is the value you should report in APA format**

**Why Use Adjusted R²?**

Adding predictors to a model will **always** increase R², even if the new predictors are useless. Adjusted R² corrects for this:

- If a predictor genuinely improves the model: Adjusted R² increases
- If a predictor doesn't help: Adjusted R² stays the same or even decreases

**Interpretation Example:**

- R² = .658
- Adjusted R² = .653

**What to report:** "The model explained 65.3% of the variance in acceleration, Adjusted R² = .653."

### 4.5 The Coefficients Table

After confirming the overall model is significant (via the F-test), we examine the **Coefficients table** to get the specific details of our regression equation.

**What the Coefficients Table Provides:**

**1. The Slope (b):**

- Found in the "B" column under "Unstandardized Coefficients"
- This is the value you plug into your equation: Ŷ = bX + a
- Interpret as: "For every 1-unit increase in X, Y changes by b units"

**2. The Y-Intercept (a):**

- Found in the row labeled "(Constant)"
- This is the constant term in your equation
- Interpret as: "When X = 0, the predicted value of Y is a"

**3. The t-Test for the Slope:**

- Tests H₀: b = 0 (slope is zero, no relationship)
- Provides t-statistic and p-value
- In **bivariate regression**, this p-value will be **identical** to the omnibus F-test p-value

**4. Standardized Coefficient (Beta β):**

- Found in the "Standardized Coefficients" column
- Used to compare effect sizes when variables are on different scales
- For **bivariate regression**, Beta = r (the correlation coefficient)

**Example Coefficients Table:**

```
                    B        Std. Error    Beta      t        p
(Constant)       17.850        .652                 27.38   <.001
Weight           -.006         .001        -.859   -7.05   <.001
```

**Interpretation:**

- Equation: Ŷ (Acceleration) = -.006(Weight) + 17.850
- Slope: For every 1-pound increase in weight, acceleration time decreases by .006 seconds
- Wait, that's backwards! Actually, weight is in hundreds of pounds, so for every 100-pound increase, acceleration decreases by .6 seconds (car takes longer to accelerate)
- The negative sign means heavier cars have slower acceleration (makes sense!)
- t(205) = -7.05, p < .001: The slope is significantly different from zero

### 4.6 Effect Size for Bivariate Regression

For bivariate regression, we have multiple ways to express effect size:

**1. R² (or Adjusted R²):**

- Overall model effect size
- "The model explains 65.8% of the variance in the outcome"

**2. r (Correlation Coefficient):**

- r = √R² (take the square root of R²)
- For bivariate regression: r = Beta (the standardized coefficient)
- Describes the strength of the linear relationship

**3. Beta² (β²):**

- For bivariate regression: β² = R²
- Squared standardized coefficient
- Proportion of variance explained by this specific predictor

**Example:**
If R² = .658 for a bivariate regression:

- r = √.658 = .811
- Beta (β) = .811 (or -.811 if negative relationship)
- β² = .658

**Quiz Terminology:**
When a quiz asks about "Beta squared as the effect size," it's referring to β², which equals R² in bivariate regression.

---

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Bivariate Regression</h4>

  <div class="quiz-question">
    <p><strong>Question 1:</strong> You run a bivariate regression using Weight as the predictor and Acceleration as the outcome. The SPSS output shows F(1, 205) = 49.778, p < .001. What does this tell you?</p>
    <div class="options">
      <p>A) The model does not significantly predict Acceleration</p>
      <p>B) The model significantly predicts Acceleration</p>
      <p>C) Weight has a small effect size</p>
      <p>D) There is a calculation error (F should have two different df values)</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) The model significantly predicts Acceleration</p>

      <p class="explanation"><strong>Why this is correct:</strong> The omnibus F-test yielded a large F-statistic (49.778) with p < .001, which is well below the typical alpha of .05. This means we reject the null hypothesis and conclude that Weight significantly predicts Acceleration.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Not significant:</strong> With p < .001, this is definitely significant.</li>
        <li><strong>C) Small effect size:</strong> We can't determine effect size from the F-statistic alone—we need R² or Adjusted R². However, F = 49.778 suggests a substantial relationship.</li>
        <li><strong>D) Calculation error:</strong> The df are different: df₁ = 1 (one predictor) and df₂ = 205 (N - 1 - 1 = 207 - 1 - 1).</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 4.2: The Omnibus F-Test.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 2:</strong> When reporting the F-test result from this bivariate regression in APA format, what is the second df for the F statistic? F(1, ___) = </p>
    <div class="options">
      <p>A) 246</p>
      <p>B) 854</p>
      <p>C) 206</p>
      <p>D) 205</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> D) 205</p>

      <p class="explanation"><strong>Why this is correct:</strong> For a bivariate regression with sample size N = 207:
        <br>df₁ = k = 1 (one predictor)
        <br>df₂ = N - k - 1 = 207 - 1 - 1 = 205</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) 246:</strong> This doesn't match the formula N - k - 1 for any reasonable sample size.</li>
        <li><strong>B) 854:</strong> This is way too large and doesn't fit the df formula.</li>
        <li><strong>C) 206:</strong> This would be N - 1, which is df for a one-sample test, not regression error df.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 4.3: Degrees of Freedom for Regression.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 3:</strong> In the bivariate regression, Beta (β) = -.859. Based on the t-test result (p < .001) for the predictor variable and Beta² as the effect size estimate, we can conclude that _____.</p>
    <div class="options">
      <p>A) The predictor can significantly predict Acceleration, with a medium to large effect size</p>
      <p>B) The predictor can significantly predict Acceleration, with a small effect size</p>
      <p>C) The predictor does not significantly predict Acceleration, with a small effect size</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> A) The predictor can significantly predict Acceleration, with a medium to large effect size</p>

      <p class="explanation"><strong>Why this is correct:</strong>
        <br>• Significance: p < .001, so the predictor is highly significant
        <br>• Effect size: β² = (-.859)² = .738, meaning 73.8% of variance explained
        <br>• This is a large effect by any standard (Cohen's guideline for large is .50 or r² = .25)</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>B) Small effect size:</strong> β² = .738 is a very large effect size, not small.</li>
        <li><strong>C) Not significant:</strong> With p < .001, this is definitely statistically significant.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 4.6: Effect Size for Bivariate Regression.</p>
    </div>

  </details>

</div>

---

## Part 5: Multiple Regression Fundamentals

### 5.1 Why Use Multiple Predictors?

Real-world outcomes are rarely determined by a single variable. **Multiple regression** allows us to create more realistic and powerful predictive models by using **two or more predictor variables** to predict a single outcome.

**Advantages of Multiple Regression:**

**1. More Realistic Models:**

- Academic success isn't just about IQ—it's also study habits, motivation, prior knowledge, etc.
- Job performance isn't just about experience—it's also personality, training, work environment, etc.
- Multiple regression captures this complexity

**2. Better Predictions:**

- Combining multiple predictors usually explains more variance than any single predictor
- Higher R² = more accurate predictions
- Example: Predicting GPA from SAT alone (R² = .25) vs. SAT + HS GPA + Study Hours (R² = .52)

**3. Control for Confounds:**

- Allows you to ask: "Does X₁ predict Y **after controlling for** X₂?"
- Example: Does gender predict salary after controlling for years of experience and education?
- Helps isolate unique effects

**4. Identify the Most Important Predictors:**

- Which variables matter most?
- Which can be dropped without hurting the model?
- Useful for theory building and practical applications

### 5.2 The Expanded Regression Equation

The regression equation expands to include multiple predictors:

**Ŷ = b₁X₁ + b₂X₂ + b₃X₃ + ... + a**

**Components:**

- **Ŷ:** Predicted value of the outcome (DV)
- **X₁, X₂, X₃, ...:** Predictor variables (IVs)
- **b₁, b₂, b₃, ...:** Slopes (regression coefficients) for each predictor
- **a:** Y-intercept (constant)

**Example:**
Ŷ (Acceleration) = .002(Horsepower) + .012(Engine) - .005(Weight) + 17.5

**Interpretation:**

- For every 1-unit increase in Horsepower (holding Engine and Weight constant), Acceleration increases by .002 seconds
- For every 1-unit increase in Engine size (holding others constant), Acceleration increases by .012 seconds
- For every 1-unit increase in Weight (holding others constant), Acceleration decreases by .005 seconds
- The y-intercept is 17.5 seconds

**Key Phrase: "Holding Other Variables Constant"**

In multiple regression, each slope represents the unique effect of that predictor **while controlling for** or **holding constant** all other predictors in the model.

### 5.3 Unique vs. Shared Variance

This is the KEY concept that makes multiple regression superior to running separate bivariate regressions.

**The Problem with Separate Bivariate Regressions:**

Imagine you run three separate bivariate regressions:

- Acceleration predicted by Horsepower: R² = .62
- Acceleration predicted by Engine: R² = .71
- Acceleration predicted by Weight: R² = .74

**Can you add these up?** NO! If you did, you'd get R² = 2.07 (207% of variance explained)—impossible!

**Why Not?** Because the predictors **overlap**. They're correlated with each other:

- Heavier cars tend to have larger engines
- Cars with larger engines tend to have more horsepower
- So these predictors share some of their predictive power

**The Solution: Multiple Regression**

Multiple regression intelligently partitions the variance into:

**1. Shared Variance:**

- Variance in Y explained by multiple predictors together
- "Overlap" between predictors
- Can't be attributed to any single predictor

**2. Unique Variance:**

- Variance in Y explained by one predictor **after removing** the effects of all other predictors
- This is what each predictor contributes **uniquely**
- Sum of all unique variances + shared variance = Total R²

**Visual Analogy:**

Imagine a Venn diagram:

- Circle A = Variance Horsepower explains
- Circle B = Variance Engine explains
- Circle C = Variance Weight explains
- Where circles overlap = Shared variance
- Where each circle is unique = Unique variance for that predictor

Multiple regression gives you both the overlapping parts AND the unique parts.

### 5.4 When to Use Multiple Regression

**Appropriate Scenarios:**

**1. Theory-Driven Models:**

- You have theoretical reasons to believe multiple factors influence the outcome
- Example: Social cognitive theory predicts that self-efficacy, outcome expectations, and social support all influence health behavior

**2. Practical Prediction:**

- You want the most accurate predictions possible
- Example: Predicting college GPA for admissions decisions using all available info

**3. Controlling for Covariates:**

- You want to test if X₁ predicts Y above and beyond known confounds
- Example: Does a new intervention predict recovery after controlling for baseline severity?

**4. Exploratory Research:**

- You have several potential predictors and want to see which matter most
- Example: What factors predict employee retention? (salary, job satisfaction, commute time, work-life balance, etc.)

**When NOT to Use Multiple Regression:**

**1. Predictors are Perfectly Collinear:**

- If two predictors are perfectly correlated, the model can't separate their effects
- SPSS will give you an error or exclude one variable

**2. Too Many Predictors for Sample Size:**

- Rule of thumb: At least 10-15 participants per predictor
- With only 30 participants, don't include 20 predictors!

**3. Non-Linear Relationships:**

- Standard regression assumes linear relationships
- If relationships are curvilinear, you need polynomial regression or other techniques

**4. You Want to Compare Group Means:**

- If your IVs are categorical groups, use ANOVA instead
- (Though you can include categorical predictors using dummy coding)

### 5.5 Interpreting Multiple Regression Coefficients

Each slope in multiple regression has a specific interpretation:

**"The slope b₁ represents the predicted change in Y for every one-unit increase in X₁, **holding all other predictors constant**."**

**Example:**
Ŷ (Salary) = 2000(Education) + 1500(Experience) + 500(Gender) + 10,000

**Interpreting Each Slope:**

**Education (b₁ = 2000):**
"For every additional year of education, salary is predicted to increase by $2,000, holding years of experience and gender constant."

**Experience (b₂ = 1500):**
"For every additional year of work experience, salary is predicted to increase by $1,500, holding education and gender constant."

**Gender (b₃ = 500):**
"Comparing people with the same education and experience, one gender is predicted to earn $500 more than the other." (Note: Gender would be dummy coded, e.g., 0 = female, 1 = male)

**Key Point:** Each slope is the **unique** effect of that predictor, independent of the others.

---

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Multiple Regression Concepts</h4>

  <div class="quiz-question">
    <p><strong>Question 1:</strong> What unique information can be gleaned from a multiple linear regression that is not available from a bivariate linear regression?</p>
    <div class="options">
      <p>A) The relative contributions from different predictors to the regression model</p>
      <p>B) Whether the model effect can be generalized to the population</p>
      <p>C) The parameters of the regression equation for predicting the outcome variable</p>
      <p>D) The measure of how well the model fit the data set</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> A) The relative contributions from different predictors to the regression model</p>

      <p class="explanation"><strong>Why this is correct:</strong> Multiple regression's key advantage is that it shows you the **unique contribution** of each predictor while controlling for all others. This allows you to compare which predictors are most important, which is impossible with separate bivariate regressions.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>B) Generalizability:</strong> Both bivariate and multiple regression use significance tests to assess generalizability to the population.</li>
        <li><strong>C) Regression equation parameters:</strong> Both types provide regression equations (Ŷ = bX + a for bivariate; Ŷ = b₁X₁ + b₂X₂ + ... + a for multiple).</li>
        <li><strong>D) Model fit:</strong> Both provide R² and Adjusted R² to indicate how well the model fits the data.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 5.3: Unique vs. Shared Variance.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 2:</strong> Which of these is an example of multiple regression?</p>
    <div class="options">
      <p>A) The effect of temperatures in Celsius and the possibility of rainfall on a particular day</p>
      <p>B) The effect of the number of employees in a company and their height</p>
      <p>C) The effect of the price and the sweetness of a pastry affecting a taster's rating</p>
      <p>D) The effect of the weight of a student and his or her grade point average</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> C) The effect of the price and the sweetness of a pastry affecting a taster's rating</p>

      <p class="explanation"><strong>Why this is correct:</strong> This has **two predictors** (price and sweetness) predicting **one outcome** (taster's rating). That's the definition of multiple regression: multiple IVs → one DV.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Temperature and rainfall:</strong> This is backwards—it's unclear what is predicting what. Also, "possibility of rainfall" is likely categorical (yes/no), not continuous.</li>
        <li><strong>B) Employees and height:</strong> This describes only one predictor (height) and the outcome isn't clear. It's not structured as a multiple regression.</li>
        <li><strong>D) Weight and GPA:</strong> This has only one predictor (weight) predicting one outcome (GPA). This would be bivariate regression, not multiple regression.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 5.1: Why Use Multiple Predictors?</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 3:</strong> You perform a multiple linear regression with Acceleration as the outcome variable, with Horsepower, Engine, and Weight as the predictor variables. The Model Summary shows R² = .658 and Adjusted R² = .653. What does the Adjusted R² value mean?</p>
    <div class="options">
      <p>A) The model explains 65.3% of the variance in Acceleration</p>
      <p>B) The predictors are 65.3% correlated with each other</p>
      <p>C) 65.3% of the sample supports the model</p>
      <p>D) The model is 65.3% certain to generalize to the population</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> A) The model explains 65.3% of the variance in Acceleration</p>

      <p class="explanation"><strong>Why this is correct:</strong> Adjusted R² represents the proportion of variance in the outcome variable (Acceleration) that is explained by the predictors in the model, adjusted for the number of predictors. 0.653 = 65.3% of variance explained.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>B) Predictors are correlated:</strong> Adjusted R² doesn't measure correlation among predictors—that would be assessed through correlation matrices or VIF.</li>
        <li><strong>C) Sample supports model:</strong> Adjusted R² isn't about what percentage of people support the model; it's about variance explained.</li>
        <li><strong>D) Certainty of generalization:</strong> This would be related to confidence intervals or significance tests, not Adjusted R².</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 4.4: R² and Adjusted R².</p>
    </div>

  </details>

</div>

---

## Part 6: Understanding Unique Contributions

### 6.1 Standardized Coefficients (Beta β)

When predictors are measured on different scales, comparing unstandardized slopes (b) is like comparing apples to oranges.

**The Problem:**

- Predictor 1: Age (years), b₁ = 0.5
- Predictor 2: Income (dollars), b₂ = 0.0001
- Predictor 3: Education (years), b₃ = 2.0

**Which predictor is strongest?** You can't tell from these values because they're in different units!

**The Solution: Standardized Coefficients (Beta β)**

**Beta (β)** is the slope you would get if all variables were converted to **z-scores** (standardized to have M = 0, SD = 1).

**Properties of Beta:**

- **Unit-free:** All predictors are on the same scale (standard deviation units)
- **Comparable:** You can directly compare Betas to see which predictor is strongest
- **Ranges from -1 to +1** (though rarely reaches these extremes)
- **Sign indicates direction:** Positive = positive relationship; Negative = negative relationship

**Example:**

```
Predictor         b (Unstandardized)    Beta (β)
Horsepower       .002                   .367
Engine           .012                   .338
Weight           -.005                  -.859
```

**Interpretation:**
Even though Weight has the smallest unstandardized slope (-.005), it has the **largest** Beta (-.859 in absolute value). This means Weight is actually the strongest predictor when all variables are on the same scale.

### 6.2 Comparing Relative Importance

**How to Identify the Strongest Predictor:**

**Step 1:** Look at the Beta (β) column in the Coefficients table

**Step 2:** Find the largest **absolute value** (ignore the sign)

**Step 3:** That predictor has the strongest unique relationship with the outcome

**Example:**

```
Predictor         Beta (β)
Horsepower       .367
Engine           .338
Weight           -.859
```

**Strongest predictor:** Weight (|-.859| = .859)
**Second:** Horsepower (.367)
**Third:** Engine (.338)

**Important Caveat:**

Beta tells you the **relative strength within your model**, but:

- A large Beta doesn't guarantee statistical significance (check the p-value!)
- A small Beta might still be theoretically or practically important
- Betas can change if you add or remove predictors from the model

### 6.3 Semipartial Correlation (sr) and sr²

While Beta tells you **which** predictor is strongest, **semipartial correlation (sr)** tells you **how much** unique variance each predictor explains.

**What is Semipartial Correlation?**

**Semipartial correlation (sr)** is the correlation between:

- The **predictor** (with effects of other predictors removed)
- The **outcome** (in its original form)

**Why "Semipartial"?**

- "Semi" = halfway
- Only the predictor is "partialed" (other IVs removed from it)
- The outcome is left alone

**Semipartial Correlation Squared (sr²):**

**sr²** is the **unique variance** explained by that predictor:

- Proportion of total variance in Y explained by this predictor alone
- After removing overlap with other predictors
- This is the **unique contribution**

**Example:**

```
Predictor         Beta (β)    sr²
Horsepower       .367         .037
Engine           .338         .114
Weight           -.859        .136
```

**Interpretation:**

- Horsepower uniquely explains 3.7% of variance in Acceleration
- Engine uniquely explains 11.4% of variance
- Weight uniquely explains 13.6% of variance
- Unique contributions: 3.7% + 11.4% + 13.6% = 28.7%
- Total R² = .658 (65.8%)
- Shared variance = 65.8% - 28.7% = 37.1%

**Key Insight:**
More than half of the explained variance (37.1% out of 65.8%) is **shared** among the predictors. This is why multiple regression is better than separate bivariate regressions!

### 6.4 Part Correlation vs. Semipartial Correlation

This is a subtle distinction that often confuses students.

**Semipartial Correlation (sr):**

- Removes other IVs from the predictor of interest
- Leaves the DV in its original form
- **Squared semipartial (sr²)** tells you unique variance explained
- This is what you want for unique contributions

**Partial Correlation (pr):**

- Removes other IVs from BOTH the predictor and the DV
- Tells you the relationship between X and Y with other variables "partialed out" of both
- **Squared partial (pr²)** is always larger than sr²
- Less useful for understanding unique variance

**In SPSS:**

- The "Part" column = semipartial correlation (sr)
- The "Partial" column = partial correlation (pr)
- For unique contributions, use **Part²** (sr²)

**Why This Matters:**

If someone asks "What is the unique contribution of the strongest predictor?":

- Find the predictor with the largest |Beta|
- Look at its **sr²** (or square the value in the "Part" column)
- That's your answer

### 6.5 VIF and Detecting Multicollinearity (Preview)

When examining unique contributions, you might notice that some predictors have small sr² values even though they're significantly correlated with the outcome. This could indicate **multicollinearity** (predictors are highly correlated with each other).

**Variance Inflation Factor (VIF):**

- Indicates how much multicollinearity is inflating the standard errors
- **VIF > 10:** Serious multicollinearity problem
- **VIF > 5:** Potential concern
- **VIF < 5:** Usually acceptable

**Tolerance:**

- Tolerance = 1 / VIF
- **Tolerance < .10:** Serious problem
- **Tolerance < .20:** Potential concern

**Why It Matters:**
High multicollinearity makes it hard to isolate unique effects. We'll cover this more in Part 7.

---

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Unique Contributions and Beta</h4>

  <div class="quiz-question">
    <p><strong>Question 1:</strong> What is the best measure for evaluating the relative contributions of the individual predictors in a multiple regression?</p>
    <div class="options">
      <p>A) VIF</p>
      <p>B) β (Beta)</p>
      <p>C) p (p-value)</p>
      <p>D) t (t-statistic)</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) β (Beta)</p>

      <p class="explanation"><strong>Why this is correct:</strong> Standardized beta coefficients (β) are specifically designed to compare the relative strength of predictors. They put all predictors on the same scale (standard deviation units), making them directly comparable. The predictor with the largest absolute value of β has the strongest relative contribution.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) VIF:</strong> Variance Inflation Factor measures multicollinearity (correlation among predictors), not the strength of individual predictors.</li>
        <li><strong>C) p-value:</strong> The p-value tells you whether a predictor is statistically significant, but not its relative strength. A predictor can be significant but weak, or strong but not significant.</li>
        <li><strong>D) t-statistic:</strong> The t-statistic tests significance and is influenced by sample size and standard errors. It doesn't directly indicate relative strength across predictors.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 6.1: Standardized Coefficients (Beta β).</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 2:</strong> In your multiple regression output, you see the following unique contributions (sr²):
    <br>Horsepower: .037
    <br>Engine: .114
    <br>Weight: .136
    <br><br>What is the unique contribution from the strongest predictor and what is the unique contribution from the weakest predictor in this regression model?</p>
    <div class="options">
      <p>A) .136; .037</p>
      <p>B) .136; .114</p>
      <p>C) .114; .037</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> A) .136; .037</p>

      <p class="explanation"><strong>Why this is correct:</strong>
        <br>• Strongest predictor: Weight with sr² = .136 (13.6% unique variance explained)
        <br>• Weakest predictor: Horsepower with sr² = .037 (3.7% unique variance explained)</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>B) .136; .114:</strong> The second value (.114) is Engine, which is the middle predictor, not the weakest.</li>
        <li><strong>C) .114; .037:</strong> The first value should be the strongest (.136 for Weight), not the middle (.114 for Engine).</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 6.3: Semipartial Correlation (sr) and sr².</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 3:</strong> For Engine as a predictor for Acceleration in your multiple regression, the slope (b) = .012 and Beta (β) = .338. The t-test shows p = .004. What does this tell us?</p>
    <div class="options">
      <p>A) The larger the engine, the lower the acceleration (time needed to go from 0 to 60 mph)</p>
      <p>B) The smaller the engine, the lower the acceleration (time needed to go from 0 to 60 mph)</p>
      <p>C) Neither of the other answer options is true</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) The smaller the engine, the lower the acceleration (time needed to go from 0 to 60 mph)</p>

      <p class="explanation"><strong>Why this is correct:</strong> The positive slope (b = .012) means that as engine size increases, acceleration TIME increases. Since acceleration is measured as time to go from 0-60 mph, a longer time means worse (slower) acceleration. So: larger engine → higher acceleration time → worse acceleration performance. Conversely, smaller engine → lower acceleration time → better acceleration performance.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Larger engine = lower acceleration:</strong> This is backwards. The positive slope means larger engine = HIGHER acceleration time (worse performance).</li>
        <li><strong>C) Neither is true:</strong> Option B is actually correct based on the positive slope.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 3.3: Understanding the Slope (b). Remember: acceleration TIME goes up = acceleration performance goes down!</p>
    </div>

  </details>

</div>

---

## Part 7: Multicollinearity

### 7.1 What is Multicollinearity?

**Multicollinearity** occurs when two or more predictor variables in your regression model are **highly correlated with each other**.

**Example:**

- Predicting heart disease from: cholesterol level, triglyceride level, and LDL level
- Problem: These variables are all measures of blood lipids and are highly correlated
- This creates multicollinearity

**Why is This a Problem?**

When predictors are highly correlated:

1. It becomes difficult to separate their **unique** effects
2. The regression coefficients become **unstable**
3. Standard errors increase (coefficients become less precise)
4. You might incorrectly conclude a predictor isn't important when it actually is

**Analogy:**

Imagine trying to determine whether height or arm length is a better predictor of basketball performance. Since height and arm length are highly correlated, it's nearly impossible to say "This much is due to height alone" vs. "This much is due to arm length alone." The effects are confounded.

### 7.2 Effects on Regression Coefficients

Multicollinearity primarily affects the **estimation of individual predictor regression coefficients**.

**What Gets Affected:**

- **Standard errors increase:** Coefficients become less precise
- **t-statistics decrease:** Predictors may appear non-significant even if they're important
- **Coefficients become unstable:** Small changes in data can cause big changes in coefficients
- **Signs can flip:** A predictor might show a positive relationship in one sample, negative in another

**What Does NOT Get Affected:**

- **Overall model F-test:** The omnibus test is usually still valid
- **R² and Adjusted R²:** Model fit statistics remain accurate
- **Predictions (Ŷ):** You can still make accurate predictions
- **The overall model:** The combined effect of all predictors is still valid

**Quiz Connection:**

"High multicollinearity affects primarily which aspect of multiple regression analysis?"

- Answer: **Estimation of the individual predictor's regression coefficient**
- Not the F-statistic, not the model fit (R²), just the individual coefficients

### 7.3 Detecting Multicollinearity

SPSS provides diagnostic tools to detect multicollinearity:

**Variance Inflation Factor (VIF):**

VIF tells you how much the variance of a regression coefficient is **inflated** due to collinearity with other predictors.

**Interpreting VIF:**

- **VIF = 1:** No correlation with other predictors (ideal)
- **VIF < 5:** Acceptable, no major concern
- **VIF 5-10:** Moderate multicollinearity, worth investigating
- **VIF > 10:** Serious multicollinearity, problematic

**Tolerance:**

Tolerance is the reciprocal of VIF: **Tolerance = 1 / VIF**

**Interpreting Tolerance:**

- **Tolerance = 1:** No correlation with other predictors
- **Tolerance > .20:** Acceptable
- **Tolerance .10-.20:** Moderate concern
- **Tolerance < .10:** Serious problem

**Relationship:**

- High VIF = Low Tolerance = High Multicollinearity
- Low VIF = High Tolerance = Low Multicollinearity

**Example:**

```
Predictor      VIF     Tolerance
Horsepower    2.34      .427      ✓ Acceptable
Engine        1.98      .505      ✓ Acceptable
Weight        2.67      .375      ✓ Acceptable
```

All VIFs < 5, so multicollinearity is not a major concern in this model.

### 7.4 When Multicollinearity is a Problem

Multicollinearity is **problematic** when:

**1. You Care About Individual Coefficients:**

- If you want to interpret "the unique effect of X₁," multicollinearity makes this difficult
- If you want to identify which predictors matter most, multicollinearity confounds this

**2. You're Building Theory:**

- If you're trying to understand causal mechanisms, multicollinearity obscures individual effects
- You can't confidently say "X₁ is important" vs. "X₂ is important"

**3. Coefficients are Unstable:**

- If adding/removing one predictor drastically changes other coefficients
- If different samples yield wildly different results

**Multicollinearity is LESS problematic when:**

**1. You Only Care About Prediction:**

- If your goal is just to predict Y accurately, multicollinearity doesn't hurt predictions
- Ŷ remains accurate even if individual coefficients are unstable

**2. You're Using the Overall Model:**

- The F-test and R² are still valid
- You can say "These predictors together explain 65% of variance" even with multicollinearity

**3. All Predictors are Theoretically Important:**

- Sometimes correlated predictors all belong in your model for theoretical reasons
- Example: A comprehensive health model might include correlated variables because they're all part of the construct

### 7.5 Addressing Multicollinearity

If multicollinearity is a problem, you have several options:

**1. Remove One of the Correlated Predictors:**

- Drop the predictor that's less theoretically important
- Or drop the one with the weaker zero-order correlation with the DV
- Simplifies the model and reduces multicollinearity

**2. Combine Correlated Predictors:**

- Create a composite score or index
- Example: Average several correlated health measures into one "health index"
- Reduces number of predictors and eliminates multicollinearity among them

**3. Use a Different Analysis:**

- Principal Components Analysis (PCA) to create uncorrelated components
- Factor Analysis to identify underlying factors
- Ridge Regression or LASSO (advanced techniques that handle multicollinearity better)

**4. Collect More Data:**

- Sometimes multicollinearity is due to small sample size
- Larger samples can provide more stable estimates

**5. Accept It (If Appropriate):**

- If you only care about prediction, leave the model as is
- Report VIF values so readers know multicollinearity exists
- Focus interpretation on the overall model, not individual coefficients

**Key Principle:**

Don't automatically remove predictors just because VIF > 5. Consider:

- Your research question (prediction vs. explanation)
- Theoretical importance of each predictor
- Practical implications

---

## Part 8: Model Building and Comparison

### 8.1 Methods for Building Regression Models

When you have many potential predictors, how do you decide which ones to include? SPSS offers several methods:

**1. Simultaneous (Enter) Method:**

- Enters all predictors into the model at once
- Most common and straightforward approach
- You decide which predictors based on theory

**2. Forward Method:**

- Starts with no predictors
- Adds predictors one at a time
- Each step: adds the predictor that improves the model most (highest correlation with residuals)
- Stops when no remaining predictor significantly improves the model
- **Result:** A model with only significant predictors

**3. Backward Method:**

- Starts with ALL predictors in the model
- Removes predictors one at a time
- Each step: removes the predictor that hurts the model least (smallest contribution)
- Stops when all remaining predictors are significant

**4. Stepwise Method:**

- Combination of forward and backward
- At each step: can add OR remove a predictor
- More complex, can be unstable

**When to Use Each:**

**Use Simultaneous (Enter) when:**

- You have a strong theoretical model
- You want to include all predictors regardless of significance
- You have a small number of predictors

**Use Forward/Backward/Stepwise when:**

- You have many potential predictors
- You're conducting exploratory research
- You want a parsimonious (simple) model with only significant predictors
- **Caution:** These methods can be influenced by small sample variations

### 8.2 Forward Method in Detail

Since the quiz asks about Forward method, let's examine it closely:

**How Forward Method Works:**

**Step 1:** Start with no predictors (just the intercept)

**Step 2:** Test all available predictors

- Find the one most strongly correlated with Y
- Add it to the model if p < .05 (or your chosen alpha)

**Step 3:** Test all remaining predictors

- Find the one that improves the model most (highest partial correlation with residuals)
- Add it to the model if p < .05

**Step 4:** Repeat until no remaining predictor significantly improves the model

**Advantage:**

- Results in a model with **only significant predictors**
- Efficient when you have many potential predictors
- Easy to interpret (no non-significant predictors cluttering the model)

**Disadvantages:**

- Not theoretically driven (data-driven instead)
- Can be influenced by multicollinearity
- Might exclude theoretically important predictors
- Results can vary between samples (less stable)

**Example:**

- Available predictors: Horsepower, Engine, Weight, Year, Cylinders
- Step 1: Weight added (strongest correlation with Acceleration)
- Step 2: Horsepower added (significantly improves model)
- Step 3: Engine not added (p > .05 after accounting for Weight and Horsepower)
- Final model: Weight + Horsepower

### 8.3 Comparing Models with Adjusted R²

When comparing different regression models, **Adjusted R²** is your primary tool.

**Why Not Regular R²?**

R² **always increases** when you add predictors, even if they're useless:

- Model 1 (1 predictor): R² = .50
- Model 2 (2 predictors): R² = .52
- Model 3 (10 predictors): R² = .54

Did those extra predictors really help? Or is the increase just due to chance?

**Adjusted R² Corrects for This:**

Adjusted R² **penalizes** you for adding predictors:

- If a predictor genuinely improves the model: Adjusted R² increases
- If a predictor doesn't help much: Adjusted R² stays the same or even decreases

**Comparing Two Models:**

**Model 1 (Bivariate):**

- Predictor: Weight only
- R² = .739
- Adjusted R² = .738

**Model 2 (Multiple):**

- Predictors: Weight, Horsepower, Engine
- R² = .658
- Adjusted R² = .653

**Wait... Model 1 has a HIGHER R²!**

This is unusual but possible. Sometimes adding predictors actually makes things worse if they:

- Add noise without adding signal
- Introduce multicollinearity
- Are poorly measured

**In this case:** The single predictor (Weight) is actually superior to the three-predictor model.

**However, in most cases, you'd see:**

**Model 1:** Adjusted R² = .738
**Model 2:** Adjusted R² = .771

**Conclusion:** Model 2 is better (explains 77.1% vs. 73.8% of variance)

### 8.4 Change in R²

When you add predictors to a model, the **change in R²** (ΔR²) tells you how much the new predictor(s) improved the model.

**Formula:**
ΔR² = R² (new model) - R² (old model)

**Example:**

**Model 1 (X₁ only):**

- R² = .754
- Adjusted R² = .754

**Model 2 (X₁ + X₂):**

- R² = .771
- Adjusted R² = .771

**Change in R²:**
ΔR² = .771 - .754 = .017

**Change in Adjusted R²:**
ΔAdj R² = .771 - .754 = .017

**Interpretation:**
"Adding X₂ to the model increased the explained variance by 1.7 percentage points, from 75.4% to 77.1%."

**Is This Improvement Significant?**

SPSS can test whether ΔR² is statistically significant:

- H₀: ΔR² = 0 (the new predictor doesn't improve the model)
- H₁: ΔR² > 0 (the new predictor significantly improves the model)

### 8.5 Adding vs. Removing Predictors

**Adding a Predictor:**

When you add a predictor to a model:

- **R² will increase** (or stay the same, never decrease)
- **Adjusted R² might increase OR decrease** (depends on whether the predictor genuinely helps)
- **F-statistic usually increases** (if predictor is helpful)
- **Individual coefficients may change** (especially if new predictor correlates with existing ones)

**Example from Quiz:**
"The change amount in Adjusted R² from .754 to .771 indicates \_\_\_"

- Answer: "The increased proportion of the outcome variance that can be explained by the model due to the **inclusion** of X₂"
- The model got better by including the new predictor

**Removing a Predictor:**

When you remove a predictor:

- **R² will decrease** (or stay the same)
- **Adjusted R² might decrease OR increase** (if you removed a useless predictor, Adjusted R² might increase!)
- **Model becomes simpler**
- **Remaining coefficients may change**

**Key Principle:**

"Removing a predictor from a multiple regression model **does not always** lower the effect size of the model."

- If you remove a useless predictor: Adjusted R² might increase (model becomes more efficient)
- If you remove a useful predictor: Adjusted R² will decrease

### 8.6 Evaluating Model Improvement

How do you know if your model is actually better?

**Criteria for a Better Model:**

**1. Higher Adjusted R²:**

- The gold standard for comparing models
- Accounts for model complexity

**2. Significant Change in R²:**

- ΔR² is statistically significant (p < .05)
- The improvement isn't just due to chance

**3. Theoretical Justification:**

- The added predictor makes theoretical sense
- Not just data fishing

**4. Parsimony:**

- Simpler models are better if they explain similar variance
- Don't add 10 predictors to gain 2% more variance

**5. Stability:**

- Results should replicate in new samples
- Overly complex models often don't generalize

**Example Decision:**

**Model A:** 3 predictors, Adjusted R² = .653
**Model B:** 1 predictor, Adjusted R² = .738

**Decision:** Choose Model B (simpler and better fit!)

**Model C:** 3 predictors, Adjusted R² = .653
**Model D:** 5 predictors, Adjusted R² = .659

**Decision:** Probably choose Model C (simpler, and only .6% improvement doesn't justify two extra predictors)

---

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Multicollinearity and Model Issues</h4>

  <div class="quiz-question">
    <p><strong>Question 1:</strong> High multicollinearity affects primarily which aspect of multiple regression analysis?</p>
    <div class="options">
      <p>A) Estimation of the parameters of the regression equation</p>
      <p>B) Estimation of the model fit</p>
      <p>C) Estimation of the F statistic</p>
      <p>D) Estimation of the individual predictor's regression coefficient</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> D) Estimation of the individual predictor's regression coefficient</p>

      <p class="explanation"><strong>Why this is correct:</strong> Multicollinearity makes it difficult to separate the unique effects of individual predictors. This causes the regression coefficients (slopes, b values) to become unstable and have larger standard errors, making them less precise and reliable.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Parameters of the equation:</strong> This is too vague. The intercept is not typically affected much, and this answer doesn't specify which parameters.</li>
        <li><strong>B) Model fit:</strong> R² and Adjusted R² remain accurate even with multicollinearity. The overall model fit is not compromised.</li>
        <li><strong>C) F statistic:</strong> The omnibus F-test for the overall model remains valid with multicollinearity. It tests whether the combined predictors are significant.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 7.2: Effects on Regression Coefficients.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 2:</strong> You check the VIF values for your predictors and find:
    <br>Horsepower: VIF = 2.34
    <br>Engine: VIF = 1.98
    <br>Weight: VIF = 2.67
    <br><br>What should you conclude about multicollinearity?</p>
    <div class="options">
      <p>A) Serious multicollinearity problem—remove at least one predictor</p>
      <p>B) Moderate multicollinearity—consider removing a predictor</p>
      <p>C) Acceptable levels of multicollinearity—no major concern</p>
      <p>D) Perfect collinearity—SPSS will exclude variables automatically</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> C) Acceptable levels of multicollinearity—no major concern</p>

      <p class="explanation"><strong>Why this is correct:</strong> All VIF values are well below 5 (the typical cutoff for concern) and below 10 (the cutoff for serious problems). VIF values between 1-5 indicate low to moderate correlation among predictors, which is normal and acceptable in most regression models.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Serious problem:</strong> VIF would need to be > 10 for a serious problem. These values are far below that threshold.</li>
        <li><strong>B) Moderate multicollinearity needing action:</strong> While there is some correlation (VIF > 1), values < 5 don't typically require removing predictors.</li>
        <li><strong>D) Perfect collinearity:</strong> Perfect collinearity would result in SPSS excluding a variable and giving an error, or VIF values approaching infinity. These moderate values don't indicate perfect collinearity.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 7.3: Detecting Multicollinearity.</p>
    </div>

  </details>

</div>

---

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Model Building and Comparison</h4>

  <div class="quiz-question">
    <p><strong>Question 1:</strong> Which statement is accurate about multiple linear regression?</p>
    <div class="options">
      <p>A) The effect of each individual predictor is tested through an F test</p>
      <p>B) The strength of the Pearson's correlation between a predictor and the outcome variable is usually weaker than that of the semipartial correlation between the same two variables</p>
      <p>C) Removing a predictor from a multiple regression model always lowers the effect size of the model</p>
      <p>D) Using the method of "Forward" to build a multiple regression model in SPSS should result in a model with only significant predictors</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> D) Using the method of "Forward" to build a multiple regression model in SPSS should result in a model with only significant predictors</p>

      <p class="explanation"><strong>Why this is correct:</strong> The Forward method adds predictors one at a time, only including those that significantly improve the model (typically using p < .05 as the criterion). Once no remaining predictors meet the significance criterion, the method stops, resulting in a model where all included predictors are statistically significant.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) F test for individual predictors:</strong> Individual predictors are tested using t-tests, not F-tests. The F-test is used for the overall model.</li>
        <li><strong>B) Pearson's r vs. semipartial r:</strong> This is backwards. Pearson's r (zero-order correlation) is usually STRONGER than the semipartial correlation because semipartial removes shared variance with other predictors.</li>
        <li><strong>C) Removing predictors always lowers effect size:</strong> This is false. Removing a useless or harmful predictor can actually INCREASE Adjusted R² by making the model more efficient.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 8.2: Forward Method in Detail.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 2:</strong> In the SPSS output tables, the change in Adjusted R² from .754 to .771 indicates _____.</p>
    <div class="options">
      <p>A) The increased proportion of the outcome variance that can be explained by the model due to the inclusion of X₂</p>
      <p>B) The increased effect of the predictor X₂ in predicting the variance of the outcome variable</p>
      <p>C) The increased proportion of the outcome variance that can be explained by the model due to the removal of X₁</p>
      <p>D) The increased effect of the predictor X₁ in predicting the variance of the outcome variable</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> A) The increased proportion of the outcome variance that can be explained by the model due to the inclusion of X₂</p>

      <p class="explanation"><strong>Why this is correct:</strong> The change in Adjusted R² from .754 (75.4%) to .771 (77.1%) represents a 1.7 percentage point increase in the proportion of outcome variance explained. This increase is due to adding (including) a new predictor (X₂) to the model.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>B) Increased effect of X₂:</strong> ΔR² shows the overall model improvement, not specifically the "effect" of X₂. The unique effect of X₂ would be shown by its sr².</li>
        <li><strong>C) Due to removal of X₁:</strong> Removing a predictor typically decreases R², not increases it. The increase here indicates addition, not removal.</li>
        <li><strong>D) Increased effect of X₁:</strong> This is about adding X₂ to the model, not about X₁'s effect changing.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 8.4: Change in R².</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 3:</strong> Compare a bivariate regression (Model 1: Weight only, Adjusted R² = .738) and a multiple regression (Model 2: Weight + Horsepower + Engine, Adjusted R² = .653). Does the current model with three predictors better account for acceleration, compared to the model with just one predictor? How do you know?</p>
    <div class="options">
      <p>A) Yes, based on the p-value</p>
      <p>B) Yes, based on the adjusted R²</p>
      <p>C) No, based on the adjusted R²</p>
      <p>D) No, based on the p-value</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> C) No, based on the adjusted R²</p>

      <p class="explanation"><strong>Why this is correct:</strong> Model 1 (Adjusted R² = .738) explains more variance than Model 2 (Adjusted R² = .653). The simpler one-predictor model is actually superior, explaining 73.8% of variance compared to only 65.3% for the three-predictor model. Adjusted R² is the appropriate metric for comparing models with different numbers of predictors.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Yes, based on p-value:</strong> Both models might be significant (p < .05), but that doesn't tell you which is better. Adjusted R² is the correct comparison metric.</li>
        <li><strong>B) Yes, based on adjusted R²:</strong> The direction is wrong—Model 2 has a LOWER Adjusted R², so it's not better.</li>
        <li><strong>D) No, based on p-value:</strong> While the answer (No) is correct, p-values don't directly compare model quality. Adjusted R² is the right justification.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 8.3: Comparing Models with Adjusted R².</p>
    </div>

  </details>

</div>

---

## Part 9: SPSS Practical Guide

### 9.1 Running Bivariate Correlations

**Step-by-Step Instructions:**

**1. Open your data file in SPSS**

**2. Analyze → Correlate → Bivariate**

**3. Select Variables:**

- Move all variables you want to correlate into the "Variables" box
- Example: Move Engine, Horsepower, Weight, and Acceleration

**4. Correlation Coefficient:**

- Ensure "Pearson" is checked (this is the default)
- Leave "Kendall's tau-b" and "Spearman" unchecked (unless you have ordinal data)

**5. Test of Significance:**

- Select "Two-tailed" (unless you have a specific directional hypothesis)

**6. Flag Significant Correlations:**

- Check "Flag significant correlations" (adds asterisks: \* for p < .05, \*\* for p < .01)

**7. Click OK**

**Reading the Output:**

SPSS produces a **correlation matrix**:

```
Correlations
                 Engine    Horsepower    Weight    Acceleration
Engine              1         .897**      .933**      .843**
Horsepower        .897**       1          .865**      .790**
Weight            .933**      .865**        1         .859**
Acceleration      .843**      .790**      .859**        1
```

**To answer: "Which variable has the strongest correlation with Acceleration?"**

- Look at the Acceleration row (or column)
- Ignore the diagonal (1.000 = perfect correlation with itself)
- Find the largest absolute value: .859 (Weight)
- **Answer: Weight** has the strongest correlation with Acceleration

### 9.2 Running Bivariate Regression

**Step-by-Step Instructions:**

**1. Analyze → Regression → Linear**

**2. Move Variables:**

- **Dependent:** Move your outcome variable (e.g., Acceleration)
- **Independent(s):** Move your ONE predictor variable (e.g., Weight)

**3. Statistics Button:**

- Check "Estimates" (gives you the regression equation)
- Check "Model fit" (gives you R² and Adjusted R²)
- Check "Descriptives" (optional, gives you means and correlations)
- Click Continue

**4. Method:**

- Keep "Enter" selected (this is simultaneous entry)

**5. Click OK**

**Reading the Output:**

**Table 1: Model Summary**

```
R       R²      Adjusted R²    Std. Error
.859    .738      .736           2.340
```

- R² = .738: Model explains 73.8% of variance
- Adjusted R² = .736: Report this value in APA format

**Table 2: ANOVA (Omnibus F-Test)**

```
              Sum of Squares    df    Mean Square    F        Sig.
Regression       860.22          1      860.22      49.778   <.001
Residual        1058.11        205        5.16
Total           1918.33        206
```

- F(1, 205) = 49.778, p < .001
- The model is highly significant

**Table 3: Coefficients**

```
                  B         Std. Error    Beta      t        p
(Constant)     17.850        .652                 27.38   <.001
Weight         -.006         .001        -.859   -7.06   <.001
```

- Regression equation: Ŷ = -.006(Weight) + 17.850
- Weight significantly predicts Acceleration, t(205) = -7.06, p < .001

### 9.3 Running Multiple Regression

**Step-by-Step Instructions:**

**1. Analyze → Regression → Linear**

**2. Move Variables:**

- **Dependent:** Acceleration
- **Independent(s):** Move ALL predictors (Horsepower, Engine, Weight)

**3. Statistics Button:**

- Check "Estimates"
- Check "Model fit"
- Check "R squared change" (to see improvement from adding predictors)
- Check "Collinearity diagnostics" (to get VIF values)
- Click Continue

**4. Method:**

- **Enter:** To force all predictors into the model
- **Forward:** To build model with only significant predictors
- **Backward:** To start with all and remove non-significant ones

**5. Click OK**

**Reading the Output:**

**Table 1: Model Summary**

```
R       R²      Adjusted R²    Std. Error    R² Change
.811    .658      .653           2.679          .658
```

- Model explains 65.3% of variance (Adjusted R²)

**Table 2: ANOVA**

```
              Sum of Squares    df    Mean Square    F         Sig.
Regression      1262.46         3      420.82      133.024   <.001
Residual         655.87       203        3.23
Total           1918.33       206
```

- F(3, 203) = 133.024, p < .001
- Overall model is significant
- For APA: F(3, 203) = 133.024, p < .001

**Degrees of Freedom Calculation:**

- df₁ = k (number of predictors) = 3
- df₂ = N - k - 1 = 207 - 3 - 1 = 203

**Table 3: Coefficients**

```
              B       Std. Error    Beta      t       p      Part (sr)    VIF
(Constant)  12.342      .847                14.56  <.001
Horsepower   .002       .010        .367    2.52   .012     .192        2.34
Engine       .012       .006        .338    2.32   .021     .338        1.98
Weight      -.005       .001       -.859   -5.78  <.001    -.369        2.67
```

**Interpreting Each Column:**

- **B:** Unstandardized slope (for regression equation)
- **Beta:** Standardized coefficient (for comparing relative strength)
- **t and p:** Significance test for each predictor
- **Part (sr):** Semipartial correlation (square this to get sr², the unique contribution)
- **VIF:** Variance Inflation Factor (multicollinearity diagnostic)

**Answering Quiz Questions:**

**Q: Which variable is NOT a significant predictor?**

- Look at p-values: All are < .05, so all are significant
- Answer: "All predictors are significant"

**Q: What is the unique contribution from the strongest and weakest predictor?**

- Strongest Beta: Weight (|-.859| = .859)
- Weakest Beta: Engine (.338)
- Square the Part (sr) values:
  - Weight: sr² = (-.369)² = .136
  - Engine: sr² = (.338)² = .114
- Wait, that doesn't match! Use Horsepower as weakest:
  - Horsepower: sr² = (.192)² = .037
- Answer: .136 (strongest); .037 (weakest)

### 9.4 Extracting F-Statistics and Degrees of Freedom

**Common Quiz Question Format:**

"Report the F statistic for the regression model."

- Look in the ANOVA table
- Find the row labeled "Regression"
- Look in the "F" column
- **Answer: Enter the exact number provided (e.g., 49.778)**

"When reporting the F test result in APA format, what is the second df?"

- Formula: df₂ = N - k - 1
- Example: 207 participants, 1 predictor
- df₂ = 207 - 1 - 1 = 205
- **Answer: 205**

"Select the correct APA format: F(**, **) = , p \_\_"

- df₁ = number of predictors = 3
- df₂ = N - k - 1 = 207 - 3 - 1 = 203
- F = 133.024
- p < .001 (never report as = .000)
- **Answer: F(3, 203) = 133.024, p < .001**

### 9.5 Reading SPSS Output for Model Summary

**Question: "Which statement is accurate based on the SPSS output for a multiple regression model?"**

**Given Output:**

```
Model Summary
R       R²      Adjusted R²    Std. Error
.644    .415      .396           5.23
```

**Analysis of Options:**

**A) "The model can explain 41.5% of the variance in the outcome variable."**

- Technically true if using R² = .415
- But you should report Adjusted R² = .396 (39.6%)
- If the question asks about "the model," use Adjusted R²
- Likely **incorrect** (should use Adjusted R²)

**B) "The F statistic is .007."**

- This is nonsense—you can't get F from the Model Summary table
- F is in the ANOVA table
- **Incorrect**

**C) "The sample size is 56."**

- You can't determine sample size from Model Summary alone
- Need the ANOVA table (df₂ + k + 1 = N)
- **Incorrect**

**D) "Because the R is positive, both predictors have positive correlations with the outcome variable."**

- R is always positive (it's the multiple correlation, like |r|)
- Individual predictors can still have negative correlations
- **Incorrect**

### 9.6 Identifying Non-Significant Predictors

**Question: "Select the variable that is NOT a significant predictor in this multiple regression model."**

**How to Answer:**

1. Look at the Coefficients table
2. Find the "p" or "Sig." column
3. Find any p-value > .05
4. That predictor is non-significant

**Example Coefficients Table:**

```
              B       Std. Error    Beta      t       p
(Constant)  12.342      .847                14.56  <.001
Horsepower   .002       .010        .367    2.52   .012
Engine       .004       .006        .128    0.67   .504
Weight      -.005       .001       -.859   -5.78  <.001
```

**Answer: Engine** (p = .504 > .05, not significant)

**Note:** If all p-values < .05, the answer is "all predictors are significant"

### 9.7 Understanding SPSS Output for Significance

**Question: "Which statement is accurate based on the SPSS output for multiple regression with two predictors?"**

**Possible Scenarios:**

**Scenario A: Model significant, both predictors significant**

```
ANOVA: F = 25.6, p < .001
Coefficients:
  X₁: t = 3.2, p = .002
  X₂: t = 4.1, p < .001
```

Answer: "The model is significant in predicting the outcome variable so both X₁ and X₂ are significant predictors."
**WAIT—this is wrong logic!** A significant model doesn't guarantee all predictors are significant.

**Scenario B: Model significant, only one predictor significant**

```
ANOVA: F = 18.3, p < .001
Coefficients:
  X₁: t = 0.8, p = .421
  X₂: t = 5.2, p < .001
```

Answer: "X₂ is a significant predictor but X₁ is not." OR "X₁ is a significant predictor but X₂ is not" (depending on which is significant).

**Key Principle:**

- Check the **omnibus F-test** for overall model significance
- Check **individual t-tests** for each predictor's significance
- These are INDEPENDENT: Model can be significant even if individual predictors aren't all significant

---

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: Correlation Fundamentals</h4>

  <div class="quiz-question">
    <p><strong>Question 1:</strong> You run bivariate correlations for Engine, Horsepower, Weight, and Acceleration. The correlation matrix shows:
    <br>Engine-Acceleration: r = .843
    <br>Horsepower-Acceleration: r = .790
    <br>Weight-Acceleration: r = .859
    <br><br>Which variable has the strongest correlation with Acceleration (regardless of direction)?</p>
    <div class="options">
      <p>A) Engine</p>
      <p>B) Weight</p>
      <p>C) Horsepower</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) Weight</p>

      <p class="explanation"><strong>Why this is correct:</strong> Weight has the highest correlation coefficient with Acceleration (r = .859), which is larger than Engine (r = .843) and Horsepower (r = .790). The largest absolute value indicates the strongest linear relationship.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Engine:</strong> While r = .843 is a strong correlation, it's not the strongest. Weight's r = .859 is higher.</li>
        <li><strong>C) Horsepower:</strong> This has the weakest correlation (r = .790) among the three variables, though it's still a strong relationship.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 9.1: Running Bivariate Correlations.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 2:</strong> The correlation between study hours and exam scores is r = .68. What does r² tell us?</p>
    <div class="options">
      <p>A) 68% of students who study more will score higher</p>
      <p>B) Study hours explain 46% of the variance in exam scores</p>
      <p>C) The relationship is 68% likely to be real</p>
      <p>D) Study hours cause 68% of the change in exam scores</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> B) Study hours explain 46% of the variance in exam scores</p>

      <p class="explanation"><strong>Why this is correct:</strong> r² = (.68)² = .46, which means 46% of the individual differences (variance) in exam scores can be accounted for by individual differences in study hours. This is the proportion of shared variance.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) 68% of students:</strong> r is not a percentage of people. It's a measure of relationship strength, not the proportion of individuals.</li>
        <li><strong>C) 68% likely to be real:</strong> This confuses correlation with probability or significance. The p-value tells us about likelihood of being real, not r.</li>
        <li><strong>D) Causes 68% of change:</strong> Correlation does NOT imply causation. We can't conclude that study hours cause exam scores from correlation alone.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 2.2: The Coefficient of Determination (r²).</p>
    </div>

  </details>

</div>

---

## Part 10: Reporting Regression in APA Format

### 10.1 Reporting Correlation Results

**Basic Format:**

"There was a [strong/moderate/weak] [positive/negative] correlation between [Variable 1] and [Variable 2], r = [value], p [< or =] [value]."

**Example 1:**

"There was a strong positive correlation between study hours and exam scores, r = .68, p < .001."

**Example 2:**

"Weight was strongly correlated with acceleration time, r = -.86, p < .001, indicating that heavier cars took longer to accelerate."

**Including Effect Size:**

"Study hours and exam scores were significantly correlated, r = .68, p < .001. Study hours explained 46% of the variance in exam scores (r² = .46)."

**Multiple Correlations:**

"Bivariate correlations revealed that acceleration time was significantly correlated with engine size (r = .84, p < .001), horsepower (r = .79, p < .001), and weight (r = .86, p < .001). Weight showed the strongest relationship with acceleration."

### 10.2 Reporting Bivariate Regression

**Complete APA Format:**

A bivariate regression was conducted to examine whether [IV] could predict [DV]. The overall model was significant, F(1, [df₂]) = [F-value], p [< or =] [p-value], with [IV] explaining [Adjusted R² × 100]% of the variance in [DV], Adjusted R² = [value]. [IV] was a significant predictor, β = [Beta], t([df₂]) = [t-value], p [< or =] [p-value]. The regression equation was: Ŷ = [b](X) + [a].

**Example:**

"A bivariate regression was conducted to examine whether weight could predict acceleration time. The overall model was significant, F(1, 205) = 49.78, p < .001, with weight explaining 73.6% of the variance in acceleration, Adjusted R² = .736. Weight was a significant predictor, β = -.86, t(205) = -7.06, p < .001. The regression equation was: Ŷ = -.006(Weight) + 17.85. Heavier cars took significantly longer to accelerate from 0 to 60 mph."

**Shorter Version:**

"Weight significantly predicted acceleration time, F(1, 205) = 49.78, p < .001, Adjusted R² = .736, β = -.86."

### 10.3 Reporting Multiple Regression

**Complete APA Format:**

A multiple regression was conducted to examine whether [list IVs] could predict [DV]. The overall model was significant, F([df₁], [df₂]) = [F-value], p [< or =] [p-value], with the predictors explaining [Adjusted R² × 100]% of the variance in [DV], Adjusted R² = [value]. [List significant predictors with their statistics]. [List non-significant predictors].

**Example:**

"A multiple regression was conducted to examine whether horsepower, engine size, and weight could predict acceleration time. The overall model was significant, F(3, 203) = 133.02, p < .001, with the three predictors explaining 65.3% of the variance in acceleration, Adjusted R² = .653. Weight was a significant predictor, β = -.86, t(203) = -5.78, p < .001, uniquely explaining 13.6% of the variance (sr² = .136). Horsepower was also a significant predictor, β = .37, t(203) = 2.52, p = .012, uniquely explaining 3.7% of the variance (sr² = .037). However, engine size was not a significant predictor after controlling for weight and horsepower, β = .34, t(203) = 2.32, p = .021."

**Note:** In this example, p = .021 is actually significant if using α = .05, so you would say "Engine size was also a significant predictor..."

**Reporting Only Significant Predictors:**

"A multiple regression with three predictors (horsepower, engine size, and weight) significantly predicted acceleration time, F(3, 203) = 133.02, p < .001, Adjusted R² = .653. Weight (β = -.86, p < .001) and horsepower (β = .37, p = .012) were significant predictors, while engine size was not (β = .34, p = .504)."

### 10.4 APA Format for F-Tests

**Key Rules:**

1. **Italicize statistics:** F, p, df
2. **Degrees of freedom in parentheses:** F(df₁, df₂)
3. **No zero before decimal for p-values:** p < .001, not p < 0.001
4. **Never report p = .000:** Use p < .001 instead
5. **Report exact p-values when p > .001:** p = .023, not p < .05
6. **Use "< .001" for very small p-values:** Not "p = .0003"

**Correct Examples:**

- F(1, 205) = 49.78, p < .001 ✓
- F(3, 203) = 133.024, p < .001 ✓
- F(2, 97) = 5.63, p = .005 ✓

**Incorrect Examples:**

- F(1, 205) = 49.78, p = .000 ✗ (use p < .001)
- F(3, 203) = 133.024, p < 0.001 ✗ (no zero before decimal)
- F(2, 97) = 5.63, p < .05 ✗ (report exact p if p > .001)
- F = 49.78, p < .001 ✗ (missing df)

**Quiz Question Format:**

"Select the correct answer to complete the F test result in APA format:
F(\_\_, \_\_) = 133.024, p \_\_"

**Options:**
A) 3; 203; < .001 ✓ Correct
B) 3; 206; = .000 ✗ (Wrong df₂, wrong p format)
C) 3; 206; < .001 ✗ (Wrong df₂)
D) 3; 203; = .000 ✗ (Wrong p format)

### 10.5 Reporting Effect Sizes

**For Correlation:**

"r² = .46, indicating that study hours explained 46% of the variance in exam scores."

**For Bivariate Regression:**

"Adjusted R² = .736, indicating that weight explained 73.6% of the variance in acceleration time."

**For Multiple Regression (Overall Model):**

"Adjusted R² = .653, indicating that the three predictors together explained 65.3% of the variance in acceleration time."

**For Multiple Regression (Individual Predictors):**

"Weight uniquely explained 13.6% of the variance (sr² = .136), while horsepower uniquely explained 3.7% (sr² = .037)."

**For Model Comparison:**

"Adding X₂ to the model increased the explained variance from 75.4% to 77.1%, ΔAdjusted R² = .017, representing a 1.7 percentage point improvement."

### 10.6 Interpreting and Describing Results

**Beyond Just Numbers:**

Always interpret your results in the context of your research question.

**Example 1: Positive Relationship**

**Numbers only:**
"SAT scores significantly predicted first-year GPA, F(1, 148) = 32.5, p < .001, Adjusted R² = .179, β = .42."

**With interpretation:**
"SAT scores significantly predicted first-year GPA, F(1, 148) = 32.5, p < .001, Adjusted R² = .179, β = .42. Students with higher SAT scores tended to achieve higher GPAs in their first year, with SAT scores explaining approximately 18% of the variance in academic performance."

**Example 2: Negative Relationship**

**Numbers only:**
"Exercise hours significantly predicted stress levels, F(1, 95) = 18.7, p < .001, Adjusted R² = .158, β = -.41."

**With interpretation:**
"Exercise hours significantly predicted stress levels, F(1, 95) = 18.7, p < .001, Adjusted R² = .158, β = -.41. Individuals who exercised more hours per week reported significantly lower stress levels, with exercise explaining approximately 16% of the variance in stress."

**Example 3: Multiple Regression**

"A multiple regression examined predictors of job satisfaction. The overall model was significant, F(4, 195) = 45.3, p < .001, Adjusted R² = .467, explaining 46.7% of the variance. Salary (β = .35, p < .001), work-life balance (β = .42, p < .001), and supervisor support (β = .28, p = .002) were all significant predictors, while commute time was not (β = -.08, p = .234). Work-life balance emerged as the strongest predictor, suggesting it plays a central role in employee satisfaction beyond financial compensation."

---

<div class="knowledge-check">
  <h4>🧠 Knowledge Check: SPSS Output and APA Reporting</h4>

  <div class="quiz-question">
    <p><strong>Question 1:</strong> You run a bivariate regression and get the following output:
    <br>F(1, 205) = 49.778, p < .001
    <br>Which is the correct value to report for the F statistic?</p>
    <div class="options">
      <p>A) 49.778</p>
      <p>B) 246.722</p>
      <p>C) .739</p>
      <p>D) 854.396</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> A) 49.778</p>

      <p class="explanation"><strong>Why this is correct:</strong> The F-statistic is found in the ANOVA table under the "F" column in the "Regression" row. Report the exact number provided by SPSS, keeping all decimal places as shown in the output.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>B) 246.722:</strong> This might be a value from elsewhere in the output (perhaps Sum of Squares), but it's not the F-statistic.</li>
        <li><strong>C) .739:</strong> This looks like it could be R² or Adjusted R², which is found in the Model Summary table, not the F-statistic.</li>
        <li><strong>D) 854.396:</strong> This doesn't match typical SPSS output values for this analysis.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 9.4: Extracting F-Statistics and Degrees of Freedom.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 2:</strong> Select the correct answer to complete the F test result in APA format for a multiple regression with 3 predictors and N = 207:
    <br>F(\_\_, \_\_) = 133.024, p \_\_</p>
    <div class="options">
      <p>A) 3; 203; < .001</p>
      <p>B) 3; 206; = .000</p>
      <p>C) 3; 206; < .001</p>
      <p>D) 3; 203; = .000</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> A) 3; 203; < .001</p>

      <p class="explanation"><strong>Why this is correct:</strong>
        <br>• df₁ = k (number of predictors) = 3
        <br>• df₂ = N - k - 1 = 207 - 3 - 1 = 203
        <br>• p-values < .001 should be reported as "< .001" not "= .000" in APA format</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>B) 3; 206; = .000:</strong> Wrong df₂ (should be 203, not 206) and wrong p format (should be < .001, not = .000).</li>
        <li><strong>C) 3; 206; < .001:</strong> Wrong df₂. This would be N - 1 = 206, which is not correct for regression error df.</li>
        <li><strong>D) 3; 203; = .000:</strong> Correct df values, but APA format requires p < .001, never p = .000.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 10.4: APA Format for F-Tests.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 3:</strong> In your multiple regression output, you see:
    <br>Horsepower: p = .012
    <br>Engine: p = .504
    <br>Weight: p < .001
    <br><br>Which variable is NOT a significant predictor?</p>
    <div class="options">
      <p>A) All predictors are significant</p>
      <p>B) Acceleration</p>
      <p>C) Horsepower</p>
      <p>D) Weight</p>
      <p>E) Engine</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> E) Engine</p>

      <p class="explanation"><strong>Why this is correct:</strong> Engine has p = .504, which is greater than the typical alpha level of .05. This means Engine is NOT a significant predictor of the outcome after controlling for the other predictors in the model.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) All significant:</strong> This is false because Engine has p = .504 > .05.</li>
        <li><strong>B) Acceleration:</strong> Acceleration is the outcome variable (DV), not a predictor, so this doesn't make sense.</li>
        <li><strong>C) Horsepower:</strong> Horsepower is significant (p = .012 < .05).</li>
        <li><strong>D) Weight:</strong> Weight is highly significant (p < .001).</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 9.6: Identifying Non-Significant Predictors.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 4:</strong> Based on the SPSS output showing R = .644, R² = .415, Adjusted R² = .396, which statement is most accurate?</p>
    <div class="options">
      <p>A) The model explains 64.4% of the variance</p>
      <p>B) The model explains 41.5% of the variance</p>
      <p>C) The model explains 39.6% of the variance</p>
      <p>D) The F statistic is .396</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> C) The model explains 39.6% of the variance</p>

      <p class="explanation"><strong>Why this is correct:</strong> When reporting model fit for regression, you should use Adjusted R² (not R or R²) because it accounts for the number of predictors and provides a more honest estimate. Adjusted R² = .396 = 39.6% of variance explained.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) 64.4%:</strong> This is R (.644), not R². R is the multiple correlation coefficient, not the proportion of variance explained.</li>
        <li><strong>B) 41.5%:</strong> This is R² (.415), which is technically correct but Adjusted R² is the preferred value to report in APA format.</li>
        <li><strong>D) F = .396:</strong> The F-statistic is not shown in the Model Summary table. .396 is Adjusted R², not F.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 9.5: Reading SPSS Output for Model Summary.</p>
    </div>

  </details>

  <div class="quiz-question">
    <p><strong>Question 5:</strong> Which statement is accurate based on SPSS output showing:
    <br>Overall Model: F(2, 53) = 15.8, p < .001
    <br>Coefficients: X₁: t = 0.9, p = .372; X₂: t = 5.2, p < .001</p>
    <div class="options">
      <p>A) The model is not significant so neither predictor has a significant effect</p>
      <p>B) X₁ is a significant predictor but X₂ is not</p>
      <p>C) The model is significant so both X₁ and X₂ are significant predictors</p>
      <p>D) X₂ is a significant predictor but X₁ is not</p>
    </div>
  </div>

  <details class="answer-section">
    <summary>💡 Click to reveal answer and explanation</summary>
    <div class="answer-content">
      <p class="correct-answer"><strong>✓ Answer:</strong> D) X₂ is a significant predictor but X₁ is not</p>

      <p class="explanation"><strong>Why this is correct:</strong> The overall model is significant (F test p < .001), meaning the predictors together significantly predict the outcome. However, looking at individual predictors: X₁ is not significant (p = .372 > .05), while X₂ is significant (p < .001). The overall model can be significant even when not all individual predictors are significant.</p>

      <p class="explanation"><strong>Why the others are incorrect:</strong></p>
      <ul>
        <li><strong>A) Model not significant:</strong> False. F(2, 53) = 15.8, p < .001 indicates a highly significant model.</li>
        <li><strong>B) X₁ significant, X₂ not:</strong> Backwards. X₁ has p = .372 (not significant), X₂ has p < .001 (significant).</li>
        <li><strong>C) Both significant because model is significant:</strong> This is faulty logic. A significant overall model doesn't guarantee all individual predictors are significant. You must check each predictor's individual t-test.</li>
      </ul>

      <p class="review-tip"><em>💭 Need to review?</em> See Part 9.7: Understanding SPSS Output for Significance.</p>
    </div>

  </details>

</div>

---

## Part 11: Summary and Key Formulas

### 11.1 Key Formulas

**Regression Equation (Bivariate):**
Ŷ = bX + a

Where:

- Ŷ = Predicted value of Y
- b = Slope (regression coefficient)
- X = Value of the predictor
- a = Y-intercept (constant)

**Regression Equation (Multiple):**
Ŷ = b₁X₁ + b₂X₂ + b₃X₃ + ... + a

**Coefficient of Determination:**
r² = r × r

Interpretation: Proportion of variance in Y explained by X

**Effect Size Formulas:**

**For Correlation:**

- r² = proportion of variance explained

**For Regression:**

- R² = proportion of variance explained by the model
- Adjusted R² = R² adjusted for number of predictors (always report this)

**For Individual Predictors in Multiple Regression:**

- sr² = semipartial correlation squared = unique variance explained by one predictor
- β² = squared standardized coefficient (for bivariate regression, β² = R²)

**Degrees of Freedom for Regression:**

- df₁ = k (number of predictors)
- df₂ = N - k - 1

**Variance Inflation Factor:**

- VIF = 1 / Tolerance
- Tolerance = 1 / VIF

### 11.2 Decision Tree for Choosing Analyses

**Start Here: What is your research question?**

**↓**

**Do you want to examine relationships between variables? (YES → Continue | NO → Use t-tests/ANOVA)**

**↓**

**How many variables?**

**Two Variables:**

- Want to describe the relationship? → **Bivariate Correlation**
- Want to predict one from the other? → **Bivariate Regression**

**More than Two Variables:**

- Multiple predictors, one outcome → **Multiple Regression**
- Multiple predictors, multiple outcomes → Multivariate Analysis (beyond this course)
- Looking for patterns/groupings → Factor Analysis/PCA (beyond this course)

**↓**

**For Regression: How many predictors?**

**One Predictor:**

- Use **Bivariate (Simple Linear) Regression**
- Report: F(1, df₂), Adjusted R², β, regression equation

**Multiple Predictors:**

- Use **Multiple Regression**
- Report: F(df₁, df₂), Adjusted R², individual βs, sr² for unique contributions
- Consider: Multicollinearity (VIF), model comparison (ΔR²)

**↓**

**Method for Entering Predictors:**

**Theory-Driven (recommended):**

- Use **Enter** method (simultaneous)
- Include all theoretically relevant predictors

**Exploratory:**

- Use **Forward** method (only significant predictors)
- Or **Backward** method (remove non-significant predictors)
- **Caution:** Results may not replicate in new samples

### 11.3 Common Mistakes to Avoid

**1. Confusing Correlation with Causation**

- ✗ "Study hours cause higher exam scores" (from correlation)
- ✓ "Study hours are associated with higher exam scores"

**2. Mixing Up r and r²**

- ✗ "r = .50, so 50% of variance is explained"
- ✓ "r = .50, so r² = .25, meaning 25% of variance is explained"

**3. Using R² Instead of Adjusted R²**

- ✗ "The model explained 65.8% of variance, R² = .658"
- ✓ "The model explained 65.3% of variance, Adjusted R² = .653"

**4. Reporting p = .000**

- ✗ F(3, 203) = 133.02, p = .000
- ✓ F(3, 203) = 133.02, p < .001

**5. Ignoring Degrees of Freedom**

- ✗ F = 49.78, p < .001
- ✓ F(1, 205) = 49.78, p < .001

**6. Misinterpreting Beta (β)**

- ✗ "β = .50 means the predictor is 50% effective"
- ✓ "β = .50 indicates a moderate-to-strong standardized relationship"

**7. Assuming All Predictors in a Significant Model are Significant**

- ✗ "F is significant, so all predictors must be significant"
- ✓ "Check individual t-tests for each predictor, even if F is significant"

**8. Extrapolating Beyond Your Data**

- ✗ Predicting for X = 50 when your data ranged from X = 1-20
- ✓ Only predict within the range of observed X values

**9. Ignoring Multicollinearity**

- ✗ "VIF = 12 is fine, I'll interpret all coefficients"
- ✓ "VIF = 12 indicates serious multicollinearity—interpret individual coefficients with caution"

**10. Adding Too Many Predictors**

- ✗ 50 predictors with N = 60
- ✓ At least 10-15 participants per predictor

### 11.4 Key Terms Glossary

**Adjusted R²:** R² adjusted for the number of predictors; preferred over R² for reporting

**Beta (β):** Standardized regression coefficient; allows comparison of predictors on different scales

**Bivariate Correlation:** Analysis examining the relationship between two continuous variables

**Bivariate Regression:** Prediction of one variable from another using one predictor

**Coefficient of Determination (r²):** Proportion of variance in one variable explained by another

**Collinearity:** See Multicollinearity

**Correlation Coefficient (r):** Measure of the strength and direction of a linear relationship (-1 to +1)

**Degrees of Freedom (df):** Number of independent pieces of information in a calculation

**Forward Method:** Model-building approach that adds predictors one at a time

**Intercept (a):** The predicted value of Y when all X variables equal 0; where the line crosses the Y-axis

**Line of Best Fit:** The regression line that minimizes the sum of squared residuals

**Multicollinearity:** High correlation among predictor variables, making it difficult to separate their unique effects

**Multiple Correlation (R):** Overall correlation between the set of predictors and the outcome (always positive)

**Multiple Regression:** Prediction of one variable from two or more predictors

**Omnibus F-Test:** Overall test of whether the regression model significantly predicts the outcome

**Ordinary Least Squares (OLS):** Method for finding the regression line that minimizes squared residuals

**Pearson Correlation:** Most common correlation coefficient for continuous variables (Pearson product-moment correlation)

**Predicted Value (Ŷ):** The value of Y predicted by the regression equation for a given X

**Predictor (IV):** The independent variable used to predict the outcome in regression

**R²:** Coefficient of determination for regression; proportion of variance explained by the model

**Residual:** The difference between observed Y and predicted Ŷ; error in prediction

**Scatterplot:** Graph showing the relationship between two continuous variables

**Semipartial Correlation (sr):** Correlation between a predictor (with other IVs removed) and the outcome

**Semipartial Correlation Squared (sr²):** Unique variance explained by one predictor

**Shared Variance:** Variance in the outcome explained by multiple predictors together (overlapping)

**Slope (b):** The change in Y for every one-unit increase in X; the regression coefficient

**Standardized Coefficient:** See Beta (β)

**Tolerance:** 1 / VIF; indicator of multicollinearity (Tolerance < .10 is problematic)

**Unique Variance:** Variance explained by one predictor after removing effects of other predictors

**Variance Inflation Factor (VIF):** Measure of multicollinearity (VIF > 10 is problematic)

**Y-Intercept:** See Intercept (a)

**Ŷ (Y-hat):** See Predicted Value

### 11.5 Final Checklist for Regression Analysis

**Before Running the Analysis:**

- [ ] Check that all variables are scale (continuous)
- [ ] Examine scatterplots for linearity
- [ ] Check for outliers
- [ ] Ensure adequate sample size (at least 10-15 participants per predictor)

**Running the Analysis in SPSS:**

- [ ] Select appropriate analysis (Bivariate Correlation, Bivariate Regression, or Multiple Regression)
- [ ] Move correct variables to DV and IV boxes
- [ ] Request necessary statistics (Estimates, Model fit, Collinearity diagnostics)
- [ ] Choose appropriate method (Enter, Forward, Backward, Stepwise)

**Interpreting the Output:**

- [ ] Check omnibus F-test (is the overall model significant?)
- [ ] Note Adjusted R² (how much variance is explained?)
- [ ] Check individual t-tests (which predictors are significant?)
- [ ] Examine VIF values (is multicollinearity a problem?)
- [ ] Note Beta values (which predictor is strongest?)
- [ ] Calculate sr² if needed (unique contributions)

**Reporting Results:**

- [ ] Report degrees of freedom: F(df₁, df₂)
- [ ] Report Adjusted R² (not R²)
- [ ] Use correct p-value format (p < .001, not p = .000)
- [ ] Include effect sizes (Adjusted R², sr²)
- [ ] Interpret findings in context
- [ ] Avoid causal language (unless experimental design)

---

## Conclusion

Congratulations! You've completed a comprehensive journey through correlation and regression analysis. You've learned to:

- Distinguish between describing relationships (correlation) and making predictions (regression)
- Understand the fundamental concepts: r, r², regression equations, slopes, and intercepts
- Run and interpret bivariate and multiple regression analyses in SPSS
- Understand unique vs. shared variance in multiple regression
- Detect and address multicollinearity
- Compare regression models using Adjusted R²
- Report regression results in proper APA format

**Key Takeaways:**

1. **Correlation describes, regression predicts** (but neither proves causation)
2. **r² and R² are effect sizes** (proportion of variance explained)
3. **Always report Adjusted R²** for regression models
4. **Multiple regression partitions variance** into unique and shared components
5. **Beta (β) allows comparison** of predictors on different scales
6. **Multicollinearity affects individual coefficients** but not overall model fit
7. **APA format matters:** F(df₁, df₂) = value, p < .001, Adjusted R² = value

**Moving Forward:**

These regression skills are fundamental to psychological research and data analysis in many fields. Practice applying them to real datasets, always:

- Visualize your data first (scatterplots!)
- Check your assumptions
- Interpret results in context
- Remember: correlation ≠ causation

Best of luck with your regression analyses, and remember—the goal is not just to run the test, but to understand and communicate what your data are telling you about the relationships between variables!

---

_This concludes the M6 Lecture on Correlation and Regression. For additional practice, work through the M6 assignment guide and practice quiz._
