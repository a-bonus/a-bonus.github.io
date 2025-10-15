### **Module 7 Statistics Study Guide: The Complete Research Workflow**

This capstone module isn't about learning a new statistical test. It's about putting all the pieces together. We will walk through the entire quantitative research process, from the initial design blueprint to the final, ethical interpretation of results. This is the "how-to" guide for thinking like a statistician and a researcher.

#### **Part 1: The Blueprint - Choosing Your Research Design**

Your research design is the single most important decision you make. It determines the types of questions you can answer and the statistical tools you can use. The key question that guides your design is: **"Can I control and randomly assign variables?"**

| Research Design                      | Key Feature                                                                                   | What it allows you to do                                                                                       | Example                                                                                                            |
| :----------------------------------- | :-------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------- | :----------------------------------------------------------------------------------------------------------------- |
| **Experimental**                     | **Random Assignment** to groups/conditions. The researcher _manipulates_ the IV.              | The "gold standard." The only design that can establish a **cause-and-effect** relationship.                   | Randomly assigning students to either a "new teaching method" group or a "standard method" group.                  |
| **Quasi-Experimental**               | Uses **pre-existing, non-random groups.** The researcher cannot randomly assign participants. | Compare groups and identify strong associations, but **cannot make firm causal claims.**                       | Comparing the test scores of students from two different schools (you can't randomly assign students to a school). |
| **Non-Experimental (Correlational)** | **Observing and measuring** variables as they naturally exist. No manipulation or grouping.   | Identify relationships, associations, and make **predictions**, but **absolutely cannot establish causation.** | Measuring the relationship between hours spent studying and final GPA.                                             |

#### **Part 2: The "Data Janitor" Phase - Examining and Preparing Your Data**

Raw data is almost never perfect. Before running any analysis, you must clean and prepare it. This is a critical, non-negotiable step.

1.  **Handling Missing Data:**

    - **Why is it missing?** You must investigate. Is it random (a few people skipped a question) or is there a pattern (everyone skipped the same hard question)? A pattern suggests a flaw in your study or survey.
    - **How to handle it:** SPSS gives options like "listwise exclusion" (deleting a participant's entire row if any data is missing) or "pairwise exclusion" (only excluding them from analyses involving the specific variable they missed). Listwise is safer but can drastically reduce your sample size.

2.  **Finding Errors and Outliers:**
    - **Errors:** Simple data entry mistakes (e.g., typing "55" instead of "5" on a 1-7 scale). Find these by running descriptive statistics and looking for impossible values (e.g., minimums, maximums).
    - **Outliers:** Data points that are numerically extreme and far from the rest of the data. They can seriously distort your results, especially the mean.
    - **How to find them:**
      - **Visually:** Use a **Boxplot**. Points that appear far above or below the "whiskers" are potential outliers.
      - **Numerically:** Calculate Z-scores for your data. A common rule of thumb is that any data point with a **Z-score greater than +/- 3** is a potential outlier.

#### **Part 3: The Pre-Flight Check - Testing Statistical Assumptions**

The parametric tests we've learned (t-tests, ANOVA, Regression) are powerful, but they work best when certain assumptions about the data are met.

1.  **Scale of Measurement:** The Dependent Variable (DV) must be a **continuous scale** variable (Interval/Ratio). This is the most fundamental assumption.

2.  **Normality:** The distribution of the DV should be **approximately normal** (a symmetrical bell curve) within the population.

    - **How to check:**
      - **Visually:** Create a **histogram** with a normal curve overlay.
      - **Formally:** Use a statistical test like the **Shapiro-Wilk test**. If its p-value is _greater_ than .05, the normality assumption is met.

3.  **Homogeneity of Variances (for group comparisons):** The variance (spread) of the DV should be roughly **equal across all groups** being compared.
    - **How to check:** Use **Levene's Test**. If its p-value is _greater_ than .05, the assumption is met. We've seen this in the independent t-test and ANOVA outputs.

#### **Part 4: The Art and Ethics of Statistics - Beyond the Numbers**

Choosing a statistical test isn't always a black-and-white decision. Sometimes, the data you collect might lead you to adjust your analysis plan. This flexibility is the "art" of statistics. However, with this flexibility comes great responsibility.

- **The Biggest Sin: Claiming Causation from Correlation.** This is the most common and serious error in interpreting statistics. Just because two variables are strongly related does not mean one causes the other. News headlines often make this mistake.

  - _Example:_ "Study finds e-cigarette use in teens leads to later smoking." The study was likely correlational. It only showed a relationship. It cannot prove that e-cigs _caused_ smoking. A third factor (e.g., a personality trait for risk-taking) could easily be the cause of both.

- **Be a Critical Consumer of Statistics:** When you read a study or a news report, always ask:
  - What was the actual **research design**? (Was it a true experiment?)
  - How were the variables **measured**? (Was a single question used to measure a complex concept like "motivation"?)
  - Is the conclusion justified by the design? (Are they claiming cause from a correlational study?)
  - What is the **effect size**? (Is a "significant" finding practically meaningful?)

### **Module 7 Key Takeaways: A Researcher's Mental Checklist**

1.  **Start with Design:** Is my study Experimental, Quasi-Experimental, or Non-Experimental? This dictates my conclusions.
2.  **Choose the Right Tool:** Based on my design and variables, which test is appropriate (t-test, ANOVA, Regression)?
3.  **Clean the Data:** Have I checked for errors, outliers, and investigated any missing data?
4.  **Check Assumptions:** Does my data meet the requirements for the test I want to run (normality, equal variances)?
5.  **Run and Interpret:** Execute the analysis, but don't stop at the p-value.
6.  **Tell the Whole Story:** What is the effect size? What is the practical meaning of the result?
7.  **Be Honest:** Does my conclusion match the limitations of my design? Am I avoiding the temptation to claim causation where there is only correlation?
