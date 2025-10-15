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

<div class="lecture-tabs">
    <div class="tab-navigation">
        <button class="tab-button active" onclick="showTab(1)">Foundations & Variables</button>
        <button class="tab-button" onclick="showTab(2)">Descriptive Statistics</button>
        <button class="tab-button" onclick="showTab(3)">Data Visualization</button>
        <button class="tab-button" onclick="showTab(4)">Population & Normal Distribution</button>
        <button class="tab-button" onclick="showTab(5)">Probability, SPSS & Summary</button>
    </div>
    
    <div class="tab-content">
        <div id="tab-1" class="tab-panel active">
            <h2>Part 1: The Purpose of Statistics</h2>

            <h3>Why Do We Need Statistics?</h3>

            <p>Imagine you're a researcher trying to answer the question: "Does meditation reduce anxiety?" You could rely on personal experience, anecdotes, or intuition. But science demands something more rigorous—<strong>objective evidence</strong> based on systematic data collection and analysis.</p>

            <p>This is where statistics comes in.</p>

            <p><strong>Key Concept:</strong> Statistics is the set of mathematical tools we use to organize, summarize, and interpret numerical data, allowing us to move from subjective opinion to objective evidence.</p>

            <h3>The Two Branches of Statistics</h3>

            <p>Statistics serves two fundamental purposes, reflected in its two main branches:</p>

            <h4>1. Descriptive Statistics</h4>

            <p><strong>Purpose:</strong> To summarize and describe the data you have collected from your specific group.</p>

            <p><strong>Example:</strong> "In our study of 50 college students, the average hours of sleep per night was 6.8 hours, with most students sleeping between 6 and 8 hours."</p>

            <p><strong>When to Use:</strong></p>

            <ul>
                <li>When you want to understand patterns in your collected data</li>
                <li>When presenting a summary of survey results</li>
                <li>When creating a profile of your participant group</li>
                <li>Any time you need to communicate "what the data looks like"</li>
            </ul>

            <p><strong>Common Tools:</strong></p>

            <ul>
                <li>Averages (mean, median, mode)</li>
                <li>Measures of spread (range, standard deviation)</li>
                <li>Frequency tables</li>
                <li>Graphs and charts</li>
            </ul>

            <h4>2. Inferential Statistics</h4>

            <p><strong>Purpose:</strong> To make educated guesses (inferences) about a larger group (population) based on data from a smaller subset (sample).</p>

            <p><strong>Example:</strong> "Based on our sample of 50 college students, we can infer with 95% confidence that the average sleep time for <em>all</em> college students at this university falls between 6.3 and 7.3 hours."</p>

            <p><strong>When to Use:</strong></p>

            <ul>
                <li>When you want to generalize findings beyond your specific participants</li>
                <li>When testing hypotheses about population characteristics</li>
                <li>When determining if observed differences are "real" or due to chance</li>
                <li>Most research scenarios in psychology and social sciences</li>
            </ul>

            <p><strong>Common Tools:</strong></p>

            <ul>
                <li>Hypothesis tests (t-tests, ANOVA, etc.)</li>
                <li>Confidence intervals</li>
                <li>p-values and significance testing</li>
            </ul>

            <p><strong>Why This Matters:</strong> Almost all psychological research uses inferential statistics because we can never study every single person. We study samples to learn about populations.</p>

            <h3>Real-World Applications</h3>

            <p><strong>Medical Research:</strong> A pharmaceutical company tests a new drug on 500 patients. They use <em>descriptive</em> statistics to summarize the results in their sample (e.g., "60% showed improvement") and <em>inferential</em> statistics to estimate effectiveness in the broader population (e.g., "We are 95% confident the drug helps between 55% and 65% of all patients with this condition").</p>

            <p><strong>Educational Psychology:</strong> A school psychologist measures reading scores for 30 third-graders using a new teaching method. Descriptive statistics show what happened in this specific classroom. Inferential statistics help determine if the method would likely work in other classrooms.</p>

            <p><strong>Business Decisions:</strong> A company surveys 200 customers about a product redesign. They describe their sample's preferences, then use inference to predict how their entire customer base (millions) would respond.</p>

            <h3>Common Misconceptions</h3>

            <p>❌ <strong>Misconception:</strong> "Statistics can prove anything you want."<br>
            ✓ <strong>Reality:</strong> When used correctly, statistics provide objective evidence. Misleading statistics usually involve inappropriate methods, selective reporting, or misinterpretation.</p>

            <p>❌ <strong>Misconception:</strong> "A statistic is just a number."<br>
            ✓ <strong>Reality:</strong> Statistics are numbers <em>with context</em>. The interpretation matters as much as the calculation.</p>

            <p>❌ <strong>Misconception:</strong> "I only need statistics if I'm doing research."<br>
            ✓ <strong>Reality:</strong> Statistical thinking helps you evaluate claims in news, advertising, health information, and everyday decision-making.</p>

            <p><strong>Think About It:</strong> When you see a headline like "New study shows coffee reduces heart disease risk by 30%," what questions should you ask? (Sample size? How was the study designed? What does "30%" actually mean?)</p>

            <hr>

            <h2>Part 2: Variables: The Building Blocks</h2>

            <h3>What is a Variable?</h3>

            <p><strong>Definition:</strong> A variable is any characteristic that can take on different values or categories across individuals, objects, or situations.</p>

            <p><strong>Key Point:</strong> The word "variable" comes from "vary"—it's something that changes or differs.</p>

            <h3>The Golden Rule of Naming Variables</h3>

            <p><strong>Always name variables based on WHAT you are measuring, not HOW you are measuring it.</strong></p>

            <p><strong>Example:</strong></p>
            <ul>
                <li>❌ "Survey_Question_5"</li>
                <li>✅ "Anxiety_Level"</li>
            </ul>

            <h3>Practice: Identifying Variables</h3>

            <p><strong>Scenario 1: Sleep Study</strong><br>
            A researcher wants to know if people who exercise regularly get better sleep. They ask 100 participants two questions:</p>
            <ol>
                <li>"How many minutes do you exercise per week?"</li>
                <li>"How many hours of sleep do you get per night on average?"</li>
            </ol>

            <p><strong>Variables:</strong></p>
            <ul>
                <li><strong>Exercise_Time</strong> (measured in minutes per week)</li>
                <li><strong>Sleep_Duration</strong> (measured in hours per night)</li>
            </ul>

            <p><strong>Scenario 2: Classroom Environment</strong><br>
            An educational psychologist studies whether classroom lighting affects student performance. She measures:</p>
            <ol>
                <li>The brightness of classroom lights (in lumens)</li>
                <li>Students' test scores on a standardized math test</li>
            </ol>

            <p><strong>Variables:</strong></p>
            <ul>
                <li><strong>Lighting_Brightness</strong> (measured in lumens)</li>
                <li><strong>Math_Test_Score</strong> (measured in points)</li>
            </ul>

            <p><strong>Scenario 3: Social Media Study</strong><br>
            A researcher investigates the relationship between social media usage and self-esteem. They collect:</p>
            <ol>
                <li>Number of hours spent on social media per day</li>
                <li>Responses to a self-esteem questionnaire (scores range from 10-50)</li>
            </ol>

            <p><strong>Variables:</strong></p>
            <ul>
                <li><strong>Social_Media_Usage</strong> (measured in hours per day)</li>
                <li><strong>Self_Esteem_Score</strong> (measured on a 10-50 scale)</li>
            </ul>

            <p><strong>Scenario 4: Job Satisfaction</strong><br>
            An organizational psychologist wants to understand what affects employee satisfaction. She measures:</p>
            <ol>
                <li>Employee age (in years)</li>
                <li>Years of experience in current job</li>
                <li>Annual salary (in dollars)</li>
                <li>Job satisfaction rating (1 = very dissatisfied, 5 = very satisfied)</li>
                <li>Department (Engineering, Marketing, HR, Sales)</li>
                <li>Whether the employee works remotely (Yes/No)</li>
            </ol>

            <p><strong>Variables:</strong></p>
            <ul>
                <li><strong>Employee_Age</strong> (measured in years)</li>
                <li><strong>Job_Experience</strong> (measured in years)</li>
                <li><strong>Annual_Salary</strong> (measured in dollars)</li>
                <li><strong>Job_Satisfaction</strong> (measured on a 1-5 scale)</li>
                <li><strong>Department</strong> (categories: Engineering, Marketing, HR, Sales)</li>
                <li><strong>Remote_Work</strong> (categories: Yes, No)</li>
            </ul>

            <p><strong>Scenario 5: Memory Experiment</strong><br>
            A cognitive psychologist tests whether background music affects memory performance. She:</p>
            <ol>
                <li>Assigns participants to either listen to classical music, rock music, or no music while studying</li>
                <li>Tests their memory with a recall task (number of words correctly remembered)</li>
                <li>Records their heart rate during the study session</li>
            </ol>

            <p><strong>Variables:</strong></p>
            <ul>
                <li><strong>Music_Condition</strong> (categories: Classical, Rock, None)</li>
                <li><strong>Memory_Performance</strong> (measured as number of words recalled)</li>
                <li><strong>Heart_Rate</strong> (measured in beats per minute)</li>
            </ul>

            <p><strong>Scenario 6: Customer Satisfaction</strong><br>
            A retail company wants to improve customer experience. They collect data on:</p>
            <ol>
                <li>Customer age group (18-25, 26-35, 36-45, 46-55, 56+)</li>
                <li>Time spent shopping (in minutes)</li>
                <li>Amount spent (in dollars)</li>
                <li>Overall satisfaction rating (1-10 scale)</li>
                <li>Whether they would recommend the store (Yes/No)</li>
            </ol>

            <p><strong>Variables:</strong></p>
            <ul>
                <li><strong>Age_Group</strong> (categories: 18-25, 26-35, 36-45, 46-55, 56+)</li>
                <li><strong>Shopping_Time</strong> (measured in minutes)</li>
                <li><strong>Purchase_Amount</strong> (measured in dollars)</li>
                <li><strong>Satisfaction_Rating</strong> (measured on a 1-10 scale)</li>
                <li><strong>Recommendation_Likelihood</strong> (categories: Yes, No)</li>
            </ul>

            <p><strong>Scenario 7: Health and Lifestyle</strong><br>
            A public health researcher studies factors related to physical fitness. She measures:</p>
            <ol>
                <li>Participants' height (in inches)</li>
                <li>Participants' weight (in pounds)</li>
                <li>Number of servings of fruits/vegetables consumed per day</li>
                <li>Minutes of moderate exercise per week</li>
                <li>Blood pressure reading (systolic pressure in mmHg)</li>
                <li>Whether participants smoke (Yes/No)</li>
            </ol>

            <p><strong>Variables:</strong></p>
            <ul>
                <li><strong>Height</strong> (measured in inches)</li>
                <li><strong>Weight</strong> (measured in pounds)</li>
                <li><strong>Fruit_Vegetable_Intake</strong> (measured in servings per day)</li>
                <li><strong>Exercise_Time</strong> (measured in minutes per week)</li>
                <li><strong>Blood_Pressure</strong> (measured in mmHg)</li>
                <li><strong>Smoking_Status</strong> (categories: Yes, No)</li>
            </ul>

            <p><strong>Scenario 8: Academic Performance</strong><br>
            A university researcher investigates factors that predict college success. They collect:</p>
            <ol>
                <li>High school GPA (0.0-4.0 scale)</li>
                <li>SAT score (400-1600 range)</li>
                <li>Number of hours studied per week</li>
                <li>Whether students live on campus or commute</li>
                <li>First-year college GPA</li>
                <li>Number of extracurricular activities</li>
            </ol>

            <p><strong>Variables:</strong></p>
            <ul>
                <li><strong>High_School_GPA</strong> (measured on a 0.0-4.0 scale)</li>
                <li><strong>SAT_Score</strong> (measured on a 400-1600 scale)</li>
                <li><strong>Study_Hours</strong> (measured in hours per week)</li>
                <li><strong>Housing_Type</strong> (categories: On-campus, Commute)</li>
                <li><strong>College_GPA</strong> (measured on a 0.0-4.0 scale)</li>
                <li><strong>Extracurricular_Count</strong> (measured as number of activities)</li>
            </ul>

            <h3>Why Proper Variable Naming Matters</h3>

            <ol>
                <li><strong>Clarity:</strong> Other researchers (and future you) can understand what was measured</li>
                <li><strong>Reproducibility:</strong> Studies can be replicated when variables are clearly defined</li>
                <li><strong>Communication:</strong> Results make sense when variables have meaningful names</li>
                <li><strong>Data Analysis:</strong> Statistical software works better with descriptive variable names</li>
            </ol>

            <p><strong>Remember:</strong> Good variable names are like good street signs—they tell you exactly where you are and where you're going.</p>

            <hr>

            <h2>Part 3: Classifying Variables</h2>

            <h3>Classification System 1: By Role in Research</h3>

            <p>Variables can be classified by their <strong>role</strong> in a research study:</p>

            <h4>Independent Variable (IV)</h4>
            <ul>
                <li><strong>Definition:</strong> The variable that the researcher manipulates or assumes causes changes in another variable</li>
                <li><strong>Also called:</strong> Predictor variable, explanatory variable, treatment variable</li>
                <li><strong>Purpose:</strong> This is what you're testing to see if it has an effect</li>
                <li><strong>Examples:</strong>
                    <ul>
                        <li>Teaching method (traditional vs. new method)</li>
                        <li>Drug dosage (0mg, 10mg, 20mg)</li>
                        <li>Study environment (quiet vs. noisy)</li>
                    </ul>
                </li>
            </ul>

            <h4>Dependent Variable (DV)</h4>
            <ul>
                <li><strong>Definition:</strong> The variable that is measured to see if it changes in response to the IV</li>
                <li><strong>Also called:</strong> Outcome variable, response variable, criterion variable</li>
                <li><strong>Purpose:</strong> This is what you're measuring to see the effect</li>
                <li><strong>Examples:</strong>
                    <ul>
                        <li>Test scores (after different teaching methods)</li>
                        <li>Pain level (after different drug dosages)</li>
                        <li>Concentration (in different study environments)</li>
                    </ul>
                </li>
            </ul>

            <p><strong>Memory Trick:</strong> Think of the IV as the "cause" and the DV as the "effect." The IV is independent (doesn't depend on other variables), while the DV depends on the IV.</p>

            <h3>How to Identify IV and DV</h3>

            <ol>
                <li><strong>Ask "What is the researcher trying to find out?"</strong> → This is usually the DV</li>
                <li><strong>Ask "What does the researcher control or manipulate?"</strong> → This is usually the IV</li>
                <li><strong>Look for causal language:</strong> "Does X affect Y?" → X is IV, Y is DV</li>
            </ol>

            <p><strong>Example:</strong> "Does exercise improve mood?"</p>
            <ul>
                <li>IV: Exercise (manipulated: some people exercise, others don't)</li>
                <li>DV: Mood (measured: how happy people report feeling)</li>
            </ul>

            <h3>Practice Scenarios</h3>

            <p><strong>Scenario 1:</strong> A researcher wants to know if background music affects productivity. She assigns some workers to listen to classical music and others to work in silence, then measures how many tasks they complete.</p>
            <ul>
                <li><strong>IV:</strong> Background Music (Classical vs. Silence)</li>
                <li><strong>DV:</strong> Productivity (Number of tasks completed)</li>
            </ul>

            <p><strong>Scenario 2:</strong> A psychologist studies whether meditation reduces anxiety. She measures anxiety levels before and after participants complete a 4-week meditation program.</p>
            <ul>
                <li><strong>IV:</strong> Meditation Program (Before vs. After)</li>
                <li><strong>DV:</strong> Anxiety Level</li>
            </ul>

            <p><strong>Scenario 3:</strong> A teacher wants to test if using technology improves student engagement. She teaches one class with traditional methods and another with tablets and apps, then measures how often students participate.</p>
            <ul>
                <li><strong>IV:</strong> Teaching Method (Traditional vs. Technology)</li>
                <li><strong>DV:</strong> Student Engagement (Participation frequency)</li>
            </ul>

            <h3>Classification System 2: By Measurement Scale</h3>

            <p>Variables can also be classified by their <strong>measurement scale</strong> (also called level of measurement):</p>

            <h4>1. Nominal (Categorical)</h4>
            <ul>
                <li><strong>Definition:</strong> Categories with no inherent order or ranking</li>
                <li><strong>Characteristics:</strong>
                    <ul>
                        <li>Categories are mutually exclusive</li>
                        <li>No mathematical operations possible (can't add, subtract, etc.)</li>
                        <li>Can count frequency of each category</li>
                    </ul>
                </li>
                <li><strong>Examples:</strong>
                    <ul>
                        <li>Gender (Male, Female, Other)</li>
                        <li>Eye Color (Blue, Brown, Green, Hazel)</li>
                        <li>Department (Psychology, Biology, English)</li>
                        <li>Blood Type (A, B, AB, O)</li>
                    </ul>
                </li>
            </ul>

            <p><strong>Think About It:</strong> You can say "There are 25 males and 30 females," but you can't say "Male is greater than Female."</p>

            <h4>2. Ordinal (Ranked)</h4>
            <ul>
                <li><strong>Definition:</strong> Categories with a meaningful order, but intervals between categories are not equal</li>
                <li><strong>Characteristics:</strong>
                    <ul>
                        <li>Categories can be ranked from low to high</li>
                        <li>Can determine which is greater/lesser</li>
                        <li>Cannot perform mathematical operations (because intervals aren't equal)</li>
                    </ul>
                </li>
                <li><strong>Examples:</strong>
                    <ul>
                        <li>Likert Scale (Strongly Disagree, Disagree, Neutral, Agree, Strongly Agree)</li>
                        <li>Education Level (High School, Bachelor's, Master's, PhD)</li>
                        <li>Pain Rating (Mild, Moderate, Severe)</li>
                        <li>Letter Grades (A, B, C, D, F)</li>
                    </ul>
                </li>
            </ul>

            <p><strong>Think About It:</strong> You can say "Master's is higher than Bachelor's," but you can't say the difference between Master's and Bachelor's equals the difference between Bachelor's and High School.</p>

            <h4>3. Scale (Interval/Ratio)</h4>
            <ul>
                <li><strong>Definition:</strong> Numeric data where intervals between values are equal</li>
                <li><strong>Two types:</strong>
                    <ul>
                        <li><strong>Interval:</strong> Equal intervals, no true zero (e.g., temperature in Celsius)</li>
                        <li><strong>Ratio:</strong> Equal intervals, true zero point (e.g., height, weight, age)</li>
                    </ul>
                </li>
                <li><strong>Characteristics:</strong>
                    <ul>
                        <li>All mathematical operations are meaningful</li>
                        <li>Can calculate means, standard deviations, etc.</li>
                        <li>True zero point (ratio) or arbitrary zero (interval)</li>
                    </ul>
                </li>
                <li><strong>Examples:</strong>
                    <ul>
                        <li><strong>Interval:</strong> Temperature (°C or °F), IQ scores, SAT scores</li>
                        <li><strong>Ratio:</strong> Height (inches), Weight (pounds), Age (years), Income (dollars)</li>
                    </ul>
                </li>
            </ul>

            <p><strong>Think About It:</strong> You can say "Person A is twice as tall as Person B" (ratio) but not "Today is twice as hot as yesterday" (interval).</p>

            <h3>Discrete vs. Continuous</h3>

            <p><strong>Discrete Variables:</strong></p>
            <ul>
                <li>Can only take specific, separate values</li>
                <li>Usually counted (not measured)</li>
                <li>Examples: Number of children, Number of correct answers, Number of pets</li>
            </ul>

            <p><strong>Continuous Variables:</strong></p>
            <ul>
                <li>Can take any value within a range</li>
                <li>Usually measured (not counted)</li>
                <li>Examples: Height, Weight, Time, Temperature</li>
            </ul>

            <h3>Decision Tree: Determining Measurement Level</h3>

            <ol>
                <li><strong>Can you perform meaningful mathematical operations?</strong>
                    <ul>
                        <li><strong>No</strong> → Go to question 2</li>
                        <li><strong>Yes</strong> → Scale (Interval/Ratio)</li>
                    </ul>
                </li>
                <li><strong>Do the categories have a meaningful order?</strong>
                    <ul>
                        <li><strong>No</strong> → Nominal</li>
                        <li><strong>Yes</strong> → Ordinal</li>
                    </ul>
                </li>
            </ol>

            <p><strong>Quick Examples:</strong></p>
            <ul>
                <li><strong>Number of siblings:</strong> Scale (Ratio) - you can add, subtract, and there's a true zero</li>
                <li><strong>Letter grade:</strong> Ordinal - A > B > C, but A-B ≠ B-C</li>
                <li><strong>Favorite color:</strong> Nominal - no order, no math operations</li>
            </ul>

            <h3>Why Measurement Level Matters</h3>

            <p><strong>Determines which statistics you can use:</strong></p>

            <ul>
                <li><strong>Nominal:</strong> Mode, frequency counts, chi-square tests</li>
                <li><strong>Ordinal:</strong> Mode, median, non-parametric tests</li>
                <li><strong>Scale:</strong> Mean, standard deviation, parametric tests (t-tests, ANOVA, correlation)</li>
            </ul>

            <p><strong>Real-world impact:</strong> Using the wrong statistic for your measurement level can lead to incorrect conclusions!</p>

            <p><strong>Example:</strong> You can't calculate the mean of "Favorite Color" (nominal), but you can calculate the mean of "Age" (scale).</p>

            <hr>
        </div>

        <div id="tab-2" class="tab-panel">
            <h2>Part 4: Describing Data with Numbers</h2>

            <p>Now that we understand what variables are and how to classify them, let's learn how to describe them with numbers. This is where <strong>descriptive statistics</strong> comes in—the tools we use to summarize and make sense of our data.</p>

            <h3>Measures of Central Tendency</h3>

            <p>These tell us about the "typical" or "average" value in our dataset.</p>

            <h4>1. Mean (Average)</h4>
            <p><strong>Formula:</strong> Mean = Sum of all values ÷ Number of values</p>

            <p><strong>Symbol:</strong> μ (population) or x̄ (sample)</p>

            <p><strong>When to use:</strong> Best for scale data that is roughly normally distributed</p>

            <p><strong>Example:</strong> Test scores: 85, 90, 78, 92, 88<br>
            Mean = (85 + 90 + 78 + 92 + 88) ÷ 5 = 433 ÷ 5 = 86.6</p>

            <p><strong>Pros:</strong></p>
            <ul>
                <li>Uses all data points</li>
                <li>Mathematically useful for further calculations</li>
                <li>Most common measure of central tendency</li>
            </ul>

            <p><strong>Cons:</strong></p>
            <ul>
                <li>Sensitive to outliers (extreme values)</li>
                <li>Can be misleading with skewed data</li>
            </ul>

            <h4>2. Median</h4>
            <p><strong>Definition:</strong> The middle value when data is arranged in order</p>

            <p><strong>When to use:</strong> Best when you have outliers or skewed data</p>

            <p><strong>How to find:</strong></p>
            <ol>
                <li>Arrange values from lowest to highest</li>
                <li>If odd number of values: middle value is median</li>
                <li>If even number of values: average of two middle values</li>
            </ol>

            <p><strong>Example:</strong> Test scores: 85, 90, 78, 92, 88<br>
            Ordered: 78, 85, 88, 90, 92<br>
            Median = 88 (middle value)</p>

            <p><strong>Example with even numbers:</strong> 78, 85, 88, 90, 92, 95<br>
            Two middle values: 88 and 90<br>
            Median = (88 + 90) ÷ 2 = 89</p>

            <p><strong>Pros:</strong></p>
            <ul>
                <li>Not affected by outliers</li>
                <li>Good for skewed distributions</li>
                <li>Easy to understand</li>
            </ul>

            <p><strong>Cons:</strong></p>
            <ul>
                <li>Doesn't use all data points</li>
                <li>Less useful for mathematical calculations</li>
            </ul>

            <h4>3. Mode</h4>
            <p><strong>Definition:</strong> The most frequently occurring value</p>

            <p><strong>When to use:</strong> Best for nominal data or when you want to know the most common category</p>

            <p><strong>Example:</strong> Eye colors in a class: Blue (12), Brown (18), Green (5), Hazel (3)<br>
            Mode = Brown (most frequent)</p>

            <p><strong>Pros:</strong></p>
            <ul>
                <li>Only measure that works with nominal data</li>
                <li>Easy to find and understand</li>
                <li>Good for categorical data</li>
            </ul>

            <p><strong>Cons:</strong></p>
            <ul>
                <li>May not exist (no repeated values)</li>
                <li>May have multiple modes</li>
                <li>Doesn't provide much information for scale data</li>
            </ul>

            <h3>Choosing the Right Measure</h3>

            <p><strong>For Scale Data:</strong></p>
            <ul>
                <li><strong>Normal distribution:</strong> Use mean</li>
                <li><strong>Skewed distribution:</strong> Use median</li>
                <li><strong>Many outliers:</strong> Use median</li>
            </ul>

            <p><strong>For Ordinal Data:</strong></p>
            <ul>
                <li>Use median (most appropriate)</li>
            </ul>

            <p><strong>For Nominal Data:</strong></p>
            <ul>
                <li>Use mode (only option)</li>
            </ul>

            <p><strong>Real-world example:</strong> Income data is usually right-skewed (few very high earners). Median income is often more representative than mean income.</p>

            <h3>Measures of Variability</h3>

            <p>These tell us how spread out our data is—how much the values differ from each other.</p>

            <h4>1. Range</h4>
            <p><strong>Formula:</strong> Range = Highest value - Lowest value</p>

            <p><strong>Example:</strong> Test scores: 78, 85, 88, 90, 92<br>
            Range = 92 - 78 = 14</p>

            <p><strong>Pros:</strong> Simple to calculate and understand</p>

            <p><strong>Cons:</strong> Only uses two values (min and max), very sensitive to outliers</p>

            <h4>2. Standard Deviation</h4>
            <p><strong>Purpose:</strong> Measures how much values typically deviate from the mean</p>

            <p><strong>Symbol:</strong> σ (population) or s (sample)</p>

            <p><strong>Formula (Conceptual):</strong> Average distance from the mean</p>

            <p><strong>Step-by-step calculation:</strong></p>
            <ol>
                <li>Calculate the mean</li>
                <li>Find the difference between each value and the mean</li>
                <li>Square each difference (to remove negative signs)</li>
                <li>Add up all the squared differences</li>
                <li>Divide by n-1 (for sample) or N (for population)</li>
                <li>Take the square root</li>
            </ol>

            <p><strong>Example:</strong> Test scores: 85, 90, 78, 92, 88<br>
            Mean = 86.6</p>

            <table>
                <tr>
                    <th>Score</th>
                    <th>(Score - Mean)</th>
                    <th>(Score - Mean)²</th>
                </tr>
                <tr>
                    <td>85</td>
                    <td>85 - 86.6 = -1.6</td>
                    <td>(-1.6)² = 2.56</td>
                </tr>
                <tr>
                    <td>90</td>
                    <td>90 - 86.6 = 3.4</td>
                    <td>(3.4)² = 11.56</td>
                </tr>
                <tr>
                    <td>78</td>
                    <td>78 - 86.6 = -8.6</td>
                    <td>(-8.6)² = 73.96</td>
                </tr>
                <tr>
                    <td>92</td>
                    <td>92 - 86.6 = 5.4</td>
                    <td>(5.4)² = 29.16</td>
                </tr>
                <tr>
                    <td>88</td>
                    <td>88 - 86.6 = 1.4</td>
                    <td>(1.4)² = 1.96</td>
                </tr>
                <tr>
                    <td></td>
                    <td>Sum = 0</td>
                    <td>Sum = 119.2</td>
                </tr>
            </table>

            <p>Variance = 119.2 ÷ (5-1) = 119.2 ÷ 4 = 29.8<br>
            Standard Deviation = √29.8 = 5.46</p>

            <p><strong>Interpretation:</strong> On average, scores deviate about 5.46 points from the mean of 86.6.</p>

            <p><strong>Why n-1 for samples?</strong> This is called the "degrees of freedom" correction. It makes our estimate of the population standard deviation more accurate when working with sample data.</p>

            <h4>3. Variance</h4>
            <p><strong>Definition:</strong> The square of the standard deviation</p>

            <p><strong>Symbol:</strong> σ² (population) or s² (sample)</p>

            <p><strong>Why use variance?</strong> It's easier to work with mathematically (no square roots), but harder to interpret (units are squared)</p>

            ### Worked Example: Calculating Descriptive Statistics

            **Data:** Hours of sleep per night for 10 college students
            6, 7, 8, 5, 9, 6, 7, 8, 7, 6

            **Step 1: Organize the data**
            Ordered: 5, 6, 6, 6, 7, 7, 7, 8, 8, 9

            **Step 2: Calculate measures of central tendency**

            **Mean:**
            Sum = 5 + 6 + 6 + 6 + 7 + 7 + 7 + 8 + 8 + 9 = 69
            Mean = 69 ÷ 10 = 6.9 hours

            **Median:**
            Even number of values (10), so average of 5th and 6th values
            Median = (7 + 7) ÷ 2 = 7 hours

            **Mode:**
            Most frequent values: 6 and 7 (each appears 3 times)
            Bimodal: 6 and 7 hours

            **Step 3: Calculate measures of variability**

            **Range:**
            Range = 9 - 5 = 4 hours

            **Standard Deviation:**
            Mean = 6.9

            | Hours | (Hours - Mean) | (Hours - Mean)² |
            |-------|----------------|-----------------|
            | 6     | 6 - 6.9 = -0.9 | (-0.9)² = 0.81 |
            | 7     | 7 - 6.9 = 0.1  | (0.1)² = 0.01 |
            | 8     | 8 - 6.9 = 1.1  | (1.1)² = 1.21 |
            | 5     | 5 - 6.9 = -1.9 | (-1.9)² = 3.61 |
            | 9     | 9 - 6.9 = 2.1  | (2.1)² = 4.41 |
            | 6     | 6 - 6.9 = -0.9 | (-0.9)² = 0.81 |
            | 7     | 7 - 6.9 = 0.1  | (0.1)² = 0.01 |
            | 8     | 8 - 6.9 = 1.1  | (1.1)² = 1.21 |
            | 7     | 7 - 6.9 = 0.1  | (0.1)² = 0.01 |
            | 6     | 6 - 6.9 = -0.9 | (-0.9)² = 0.81 |
            |       | Sum = 0        | Sum = 12.9     |

            Variance = 12.9 ÷ (10-1) = 12.9 ÷ 9 = 1.43
            Standard Deviation = √1.43 = 1.20 hours

            **Step 4: Interpret the results**

            **Central Tendency:**
            - Mean sleep time is 6.9 hours
            - Median sleep time is 7 hours (half sleep less, half sleep more)
            - Most common sleep times are 6 and 7 hours

            **Variability:**
            - Sleep times range from 5 to 9 hours (4-hour spread)
            - On average, sleep times deviate about 1.2 hours from the mean
            - This suggests relatively consistent sleep patterns

            **Summary:** These college students sleep an average of 6.9 hours per night, with most sleeping 6-7 hours. The variation is relatively small (standard deviation = 1.2 hours), indicating fairly consistent sleep habits.

            ---
        </div>

        <div id="tab-3" class="tab-panel">
            <h2>Part 5: Visualizing Data: Frequency Distributions</h2>

            <p>Numbers can tell us a lot, but sometimes a picture is worth a thousand data points. In this section, we'll learn how to create visual representations of our data that make patterns and relationships easier to see.</p>

            <h3>What is a Frequency Distribution?</h3>

            <p>A <strong>frequency distribution</strong> is a summary of how often each value (or range of values) occurs in your dataset. It shows the pattern of your data at a glance.</p>

            <p><strong>Two main types:</strong></p>
            <ol>
                <li><strong>Categorical frequency distribution</strong> - for nominal and ordinal data</li>
                <li><strong>Grouped frequency distribution</strong> - for scale data</li>
            </ol>

            <h3>For Categorical Data: Frequency Tables and Bar Charts</h3>

            <h4>Frequency Tables</h4>
            <p>Simply count how many times each category appears.</p>

            <p><strong>Example: Favorite Pizza Toppings</strong><br>
            Data: Pepperoni, Cheese, Mushroom, Pepperoni, Cheese, Pepperoni, Sausage, Cheese, Pepperoni, Mushroom</p>

            <table>
                <tr>
                    <th>Topping</th>
                    <th>Frequency</th>
                    <th>Percentage</th>
                </tr>
                <tr>
                    <td>Pepperoni</td>
                    <td>4</td>
                    <td>40%</td>
                </tr>
                <tr>
                    <td>Cheese</td>
                    <td>3</td>
                    <td>30%</td>
                </tr>
                <tr>
                    <td>Mushroom</td>
                    <td>2</td>
                    <td>20%</td>
                </tr>
                <tr>
                    <td>Sausage</td>
                    <td>1</td>
                    <td>10%</td>
                </tr>
                <tr>
                    <td><strong>Total</strong></td>
                    <td><strong>10</strong></td>
                    <td><strong>100%</strong></td>
                </tr>
            </table>

            <h4>Bar Charts</h4>
            <p>Visual representation of frequency tables.</p>

            <p><strong>When to use bar charts:</strong></p>
            <ul>
                <li>Nominal data (categories with no order)</li>
                <li>Ordinal data (categories with order)</li>
                <li>Comparing frequencies across categories</li>
            </ul>

            <p><strong>Characteristics:</strong></p>
            <ul>
                <li>Bars don't touch (categories are separate)</li>
                <li>Height represents frequency</li>
                <li>Can be horizontal or vertical</li>
            </ul>

            <p><strong>Example Bar Chart Data:</strong></p>
            <pre>
            Pepperoni  ████████ 4
            Cheese     ██████   3
            Mushroom   ████     2
            Sausage    ██       1
            </pre>

            <h3>For Scale Data: Grouped Frequency Tables and Histograms</h3>

            <h4>Grouped Frequency Tables</h4>
            <p>When you have many different values, group them into ranges (called "bins" or "intervals").</p>

            <p><strong>Example: Test Scores (0-100 scale)</strong><br>
            Raw data: 78, 85, 92, 67, 89, 94, 76, 83, 91, 88, 79, 86, 93, 75, 87</p>

            <p><strong>Step 1: Determine range</strong><br>
            Highest: 94, Lowest: 67<br>
            Range = 94 - 67 = 27</p>

            <p><strong>Step 2: Choose appropriate interval width</strong><br>
            Common rule: Use 5-15 intervals<br>
            With 15 data points, let's use 5-point intervals</p>

            <p><strong>Step 3: Create intervals</strong><br>
            Start just below the lowest value: 65-69, 70-74, 75-79, 80-84, 85-89, 90-94, 95-99</p>

            <p><strong>Step 4: Count frequencies</strong></p>
            <table>
                <tr>
                    <th>Score Range</th>
                    <th>Tally</th>
                    <th>Frequency</th>
                </tr>
                <tr>
                    <td>95-99</td>
                    <td></td>
                    <td>0</td>
                </tr>
                <tr>
                    <td>90-94</td>
                    <td>||||</td>
                    <td>4</td>
                </tr>
                <tr>
                    <td>85-89</td>
                    <td>|||||</td>
                    <td>5</td>
                </tr>
                <tr>
                    <td>80-84</td>
                    <td>||</td>
                    <td>2</td>
                </tr>
                <tr>
                    <td>75-79</td>
                    <td>|||</td>
                    <td>3</td>
                </tr>
                <tr>
                    <td>70-74</td>
                    <td></td>
                    <td>0</td>
                </tr>
                <tr>
                    <td>65-69</td>
                    <td>|</td>
                    <td>1</td>
                </tr>
            </table>

            <p><strong>Step 5: Calculate percentages</strong></p>
            <table>
                <tr>
                    <th>Score Range</th>
                    <th>Frequency</th>
                    <th>Percentage</th>
                </tr>
                <tr>
                    <td>95-99</td>
                    <td>0</td>
                    <td>0%</td>
                </tr>
                <tr>
                    <td>90-94</td>
                    <td>4</td>
                    <td>27%</td>
                </tr>
                <tr>
                    <td>85-89</td>
                    <td>5</td>
                    <td>33%</td>
                </tr>
                <tr>
                    <td>80-84</td>
                    <td>2</td>
                    <td>13%</td>
                </tr>
                <tr>
                    <td>75-79</td>
                    <td>3</td>
                    <td>20%</td>
                </tr>
                <tr>
                    <td>70-74</td>
                    <td>0</td>
                    <td>0%</td>
                </tr>
                <tr>
                    <td>65-69</td>
                    <td>1</td>
                    <td>7%</td>
                </tr>
                <tr>
                    <td><strong>Total</strong></td>
                    <td><strong>15</strong></td>
                    <td><strong>100%</strong></td>
                </tr>
            </table>

            <h4>Histograms</h4>
            <p>Visual representation of grouped frequency data.</p>

            <p><strong>When to use histograms:</strong></p>
            <ul>
                <li>Scale data (interval or ratio)</li>
                <li>Showing distribution shape</li>
                <li>Identifying patterns, outliers, skewness</li>
            </ul>

            <p><strong>Characteristics:</strong></p>
            <ul>
                <li>Bars touch (continuous scale)</li>
                <li>Width represents interval range</li>
                <li>Height represents frequency</li>
                <li>No gaps between bars (unless frequency is zero)</li>
            </ul>

            <p><strong>Example Histogram:</strong></p>
            <pre>
            Frequency
                5 |     ███
                4 | ███ ███ ███
                3 | ███ ███ ███ ███
                2 | ███ ███ ███ ███ ███
                1 | ███ ███ ███ ███ ███ ███
                  +----+----+----+----+----+
                  65  70   75   80   85   90
                  Score Range
            </pre>

            <p><strong>What this histogram tells us:</strong></p>
            <ul>
                <li>Most scores are in the 85-89 range (5 students)</li>
                <li>Distribution is roughly bell-shaped</li>
                <li>No extreme outliers</li>
                <li>Scores are concentrated in the upper ranges</li>
            </ul>

            <h3>Common Mistake: Choosing the Wrong Graph</h3>

            <p>❌ <strong>Wrong:</strong> Using a line graph for categorical data<br>
            ✅ <strong>Correct:</strong> Use bar charts for categories</p>

            <p>❌ <strong>Wrong:</strong> Using a bar chart for continuous scale data<br>
            ✅ <strong>Correct:</strong> Use histograms for scale data</p>

            <p><strong>Why this matters:</strong> Different graph types are designed for different types of data. Using the wrong type can mislead readers about your data's characteristics.</p>

            <h3>Quick Check</h3>

            <p><strong>Question 1:</strong> You survey 50 students about their favorite subject. Which graph should you use?</p>
            <ul>
                <li>A) Histogram</li>
                <li>B) Bar chart</li>
                <li>C) Line graph</li>
            </ul>

            <p><strong>Answer:</strong> B) Bar chart - because "favorite subject" is categorical data (nominal level)</p>

            <p><strong>Question 2:</strong> You measure the height of 100 people. Which graph should you use?</p>
            <ul>
                <li>A) Histogram</li>
                <li>B) Bar chart</li>
                <li>C) Pie chart</li>
            </ul>

            <p><strong>Answer:</strong> A) Histogram - because height is continuous scale data</p>

            <p><strong>Question 3:</strong> Looking at your histogram, you notice the bars on the left are much taller than those on the right. What does this suggest?</p>
            <ul>
                <li>A) Your data is normally distributed</li>
                <li>B) Your data is right-skewed (positively skewed)</li>
                <li>C) Your data is left-skewed (negatively skewed)</li>
            </ul>

            <p><strong>Answer:</strong> C) Left-skewed - most values are on the higher end, with a tail extending to the lower end</p>

            <hr>
        </div>

        <div id="tab-4" class="tab-panel">
            <h2>Part 6: From Sample to Population</h2>

            <p>So far, we've focused on describing the data we actually collected. But in most research, we want to make conclusions about a larger group than just our participants. This is where the distinction between <strong>samples</strong> and <strong>populations</strong> becomes crucial.</p>

            <h3>Key Definitions</h3>

            <p><strong>Population:</strong> The entire group of individuals, objects, or events that you want to study and make conclusions about.</p>

            <p><strong>Sample:</strong> A subset of the population that you actually study and collect data from.</p>

            <p><strong>Examples:</strong></p>
            <ul>
                <li><strong>Population:</strong> All college students in the United States</li>
                <li><strong>Sample:</strong> 500 college students from your university</li>
            </ul>

            <ul>
                <li><strong>Population:</strong> All smartphones sold last year</li>
                <li><strong>Sample:</strong> 1,000 smartphones tested for battery life</li>
            </ul>

            <ul>
                <li><strong>Population:</strong> All patients with diabetes</li>
                <li><strong>Sample:</strong> 200 patients who received a new medication</li>
            </ul>

            <p><strong>Why use samples?</strong> Because studying entire populations is usually impractical, expensive, or impossible.</p>

            <h3>Parameters vs. Statistics</h3>

            <p><strong>Parameter:</strong> A numerical characteristic of a population (usually unknown)</p>

            <p><strong>Statistic:</strong> A numerical characteristic of a sample (what we actually calculate)</p>

            <p><strong>Symbols:</strong></p>
            <ul>
                <li>Population mean: μ (mu)</li>
                <li>Sample mean: x̄ (x-bar)</li>
                <li>Population standard deviation: σ (sigma)</li>
                <li>Sample standard deviation: s</li>
            </ul>

            <p><strong>Example:</strong></p>
            <ul>
                <li><strong>Parameter:</strong> Average height of all adult women in the US (μ = unknown)</li>
                <li><strong>Statistic:</strong> Average height of 100 adult women in our sample (x̄ = 65.2 inches)</li>
            </ul>

            <p><strong>Key insight:</strong> We use sample statistics to estimate population parameters.</p>

            <h3>The Problem of Bias and the n-1 Correction</h3>

            <p>When we calculate the sample standard deviation, we divide by <strong>n-1</strong> instead of <strong>n</strong>. Why?</p>

            <p><strong>The bias problem:</strong> If we divide by n, our sample standard deviation tends to underestimate the true population standard deviation.</p>

            <p><strong>Why this happens:</strong> In a sample, the values are closer to the sample mean than they would be to the true population mean. This makes our sample look less variable than it really is.</p>

            <p><strong>The solution:</strong> Dividing by n-1 (called "degrees of freedom") corrects for this bias and gives us a better estimate of the population standard deviation.</p>

            <p><strong>Example:</strong><br>
            Population: 1, 2, 3, 4, 5 (μ = 3, σ = √2 ≈ 1.41)<br>
            Sample: 2, 3, 4 (x̄ = 3)</p>

            <p><strong>Wrong way (divide by n):</strong><br>
            s = √[(2-3)² + (3-3)² + (4-3)²] ÷ 3 = √[1+0+1] ÷ 3 = √(2/3) ≈ 0.82</p>

            <p><strong>Right way (divide by n-1):</strong><br>
            s = √[(2-3)² + (3-3)² + (4-3)²] ÷ 2 = √[1+0+1] ÷ 2 = √1 = 1.00</p>

            <p>The n-1 correction gives us a better estimate of the true population standard deviation.</p>

            ### Worked Example: Sample vs. Population Calculation

            **Scenario:** A researcher wants to know the average number of hours college students spend studying per week. She surveys 20 students from her statistics class.

            **Sample data (hours per week):**
            8, 12, 15, 6, 10, 18, 9, 14, 7, 11, 13, 16, 5, 19, 8, 12, 14, 10, 17, 9

            **Step 1: Calculate sample statistics**

            **Sample mean (x̄):**
            Sum = 8+12+15+6+10+18+9+14+7+11+13+16+5+19+8+12+14+10+17+9 = 232
            x̄ = 232 ÷ 20 = 11.6 hours

            **Sample standard deviation (s):**
            Using n-1 correction:

            | Hours | (Hours - x̄) | (Hours - x̄)² |
            |-------|--------------|---------------|
            | 8     | 8-11.6 = -3.6 | (-3.6)² = 12.96 |
            | 12    | 12-11.6 = 0.4 | (0.4)² = 0.16 |
            | 15    | 15-11.6 = 3.4 | (3.4)² = 11.56 |
            | ...   | ...         | ...           |
            | (sum of all squared differences = 284.8) |

            s = √(284.8 ÷ 19) = √14.99 = 3.87 hours

            **Step 2: Interpret in context**

            **Sample findings:**
            - The 20 students in our sample study an average of 11.6 hours per week
            - Study times vary by about 3.9 hours on average from this mean

            **Population inference:**
            - We estimate that all college students study about 11.6 hours per week
            - However, we're not certain—this is just our best estimate based on our sample

            **Step 3: Consider limitations**

            **Potential bias:**
            - These are statistics students (might study more than average)
            - Only from one university (might not represent all colleges)
            - Small sample size (n=20) means less precision

            **Better approach:** Random sampling from multiple universities would give more reliable population estimates.

            ### Why This Matters for Your Assignment

            When you calculate descriptive statistics in your M1 assignment:

            1. **Always use n-1** for sample standard deviation
            2. **Remember you're describing your sample**, not making claims about the entire population
            3. **Be cautious about generalizations** unless you have a representative sample

            ### Quick Check

            **Question 1:** A researcher surveys 100 people about their exercise habits. What is the sample and what is the population?

            **Answer:**
            - Sample: The 100 people surveyed
            - Population: All people (or whatever group the researcher wants to generalize to)

            **Question 2:** The researcher finds that the sample exercises an average of 3.2 hours per week. What type of number is this?

            **Answer:** This is a statistic (sample mean), not a parameter (population mean)

            **Question 3:** Why do we divide by n-1 instead of n when calculating sample standard deviation?

            **Answer:** To correct for bias—samples tend to underestimate population variability, and dividing by n-1 gives a better estimate of the true population standard deviation.

            ---

            ## Part 7: The Normal Distribution and Z-Scores

            Many natural phenomena follow a predictable pattern called the **normal distribution** (also called the bell curve). Understanding this pattern is crucial for statistical inference.

            ### The Normal Distribution (The Bell Curve)

            **Characteristics:**
            - Symmetrical (mirror image on both sides)
            - Bell-shaped
            - Mean, median, and mode are all the same
            - Most values cluster around the center
            - Fewer values as you move away from center

            **Real-world examples:**
            - Heights of adult men
            - IQ scores
            - Test scores (when the test is well-designed)
            - Measurement errors
            - Many biological measurements

            **Key insight:** The normal distribution is so common that many statistical tests assume your data follows this pattern.

            ### The 68-95-99.7 Rule (Empirical Rule)

            For any normal distribution:
            - **68%** of values fall within 1 standard deviation of the mean
            - **95%** of values fall within 2 standard deviations of the mean
            - **99.7%** of values fall within 3 standard deviations of the mean

            **Example:** IQ scores have a mean of 100 and standard deviation of 15
            - 68% of people have IQ between 85 and 115 (100 ± 15)
            - 95% of people have IQ between 70 and 130 (100 ± 30)
            - 99.7% of people have IQ between 55 and 145 (100 ± 45)

            **Visual representation:**
            ```
            Percentage of values
                34%   34%
                   \ /
                    X
                   / \
                13.5% 13.5%
                   |   |
                2.35% 2.35%
                   |   |
                0.15% 0.15%
                -3σ -2σ -1σ μ +1σ +2σ +3σ
            ```

            ### Z-Scores: The Universal Translator

            A **z-score** tells you how many standard deviations a value is from the mean.

            **Formula:** z = (Value - Mean) ÷ Standard Deviation

            **Interpretation:**
            - z = 0: Value equals the mean
            - z = 1: Value is 1 standard deviation above the mean
            - z = -1: Value is 1 standard deviation below the mean
            - z = 2: Value is 2 standard deviations above the mean

            **Why z-scores matter:**
            1. **Standardization:** Convert any normal distribution to the same scale
            2. **Comparison:** Compare values from different distributions
            3. **Probability:** Find the probability of getting a value or range

            ### Worked Examples of Z-Scores

            **Example 1: Test Scores**
            Math test: Mean = 75, Standard deviation = 10
            Your score: 85

            z = (85 - 75) ÷ 10 = 10 ÷ 10 = 1.0

            **Interpretation:** Your score is 1 standard deviation above the mean. You scored better than about 84% of students (50% + 34% = 84%).

            **Example 2: Height**
            Adult male heights: Mean = 70 inches, Standard deviation = 3 inches
            Your height: 76 inches

            z = (76 - 70) ÷ 3 = 6 ÷ 3 = 2.0

            **Interpretation:** You are 2 standard deviations above the mean height. You are taller than about 97.5% of adult men.

            **Example 3: Comparing Different Tests**
            Math test: Score = 80, Mean = 75, SD = 10 → z = 0.5
            English test: Score = 85, Mean = 80, SD = 15 → z = 0.33

            **Interpretation:** You performed better on the math test relative to your classmates, even though your English score was higher in absolute terms.

            ### Using Z-Scores to Find Probabilities

            **Example:** What percentage of people have IQ scores above 115?

            **Step 1:** Calculate z-score
            z = (115 - 100) ÷ 15 = 15 ÷ 15 = 1.0

            **Step 2:** Use the 68-95-99.7 rule
            - 68% of people have IQ between 85 and 115
            - This means 32% have IQ outside this range
            - Since the distribution is symmetrical, 16% have IQ above 115

            **Answer:** About 16% of people have IQ scores above 115.

            **Example:** What percentage of people have IQ scores below 85?

            **Step 1:** Calculate z-score
            z = (85 - 100) ÷ 15 = -15 ÷ 15 = -1.0

            **Step 2:** Use symmetry
            - 16% have IQ above 115 (z = +1)
            - By symmetry, 16% have IQ below 85 (z = -1)

            **Answer:** About 16% of people have IQ scores below 85.

            ### Properties of Z-Scores

            1. **Mean of z-scores = 0**
            2. **Standard deviation of z-scores = 1**
            3. **Shape remains the same** (normal distribution stays normal)
            4. **Easy to interpret** (positive = above average, negative = below average)

            ### Real-World Application

            **College Admissions:** SAT scores are converted to z-scores to compare students from different graduating classes and different high schools.

            **Medical Testing:** Lab results are often reported as z-scores to help doctors identify unusual values (typically z > 2 or z < -2).

            **Quality Control:** Manufacturing processes use z-scores to identify products that are too far from specifications.

            ### Quick Check

            **Question 1:** A student scores 88 on a test where the mean is 80 and standard deviation is 4. What is their z-score?

            **Answer:** z = (88 - 80) ÷ 4 = 8 ÷ 4 = 2.0

            **Question 2:** Using the 68-95-99.7 rule, what percentage of students scored better than this student?

            **Answer:** About 2.5% (since 95% fall within 2 standard deviations, 5% fall outside, and 2.5% are above)

            **Question 3:** If IQ scores are normally distributed with mean 100 and standard deviation 15, what IQ score corresponds to z = -1.5?

            **Answer:** IQ = 100 + (-1.5 × 15) = 100 - 22.5 = 77.5

            ---
        </div>

        <div id="tab-5" class="tab-panel">
            <h2>Part 8: Probability and Inference</h2>

            <p>Probability is the foundation of statistical inference—the process of drawing conclusions about populations based on sample data. Understanding basic probability concepts helps us make sense of statistical tests and their results.</p>

            <h3>What is Probability?</h3>

            <p><strong>Definition:</strong> Probability is the likelihood that a particular event will occur, expressed as a number between 0 and 1.</p>

            <ul>
                <li><strong>0</strong> = Event will never happen (impossible)</li>
                <li><strong>0.5</strong> = Event has equal chance of happening or not (50-50)</li>
                <li><strong>1</strong> = Event will always happen (certain)</li>
            </ul>

            <p><strong>Examples:</strong></p>
            <ul>
                <li>Probability of flipping heads: 0.5 (50%)</li>
                <li>Probability of rolling a 6 on a die: 0.167 (16.7%)</li>
                <li>Probability of rain tomorrow: 0.3 (30%)</li>
            </ul>

            <p><strong>Key insight:</strong> In statistics, we're often interested in the probability of getting certain sample results if our hypothesis about the population is true.</p>

            ### Probability in Normal Distributions

            **The connection:** In a normal distribution, we can calculate the probability of getting any value or range of values.

            **Example:** IQ scores are normally distributed with mean 100 and standard deviation 15.
            - Probability of IQ > 115: About 16%
            - Probability of IQ between 85 and 115: About 68%
            - Probability of IQ < 70: About 2.5%

            **Why this matters:** Statistical tests use probability to determine if our sample results are "surprising" or "expected" if our hypothesis is true.

            ### The Logic of Inferential Statistics (Preview)

            **The basic question:** "Is what I observed in my sample likely to have happened by chance, or does it suggest a real effect in the population?"

            **The process:**
            1. **State a hypothesis** about the population
            2. **Collect sample data**
            3. **Calculate the probability** of getting your sample results if the hypothesis is true
            4. **Make a decision:** If the probability is low, reject the hypothesis

            **Example:** Testing a new teaching method
            - **Hypothesis:** New method = traditional method (no difference)
            - **Sample:** Students using new method score 15 points higher on average
            - **Question:** What's the probability of getting this result by chance?
            - **Decision:** If probability < 5%, conclude new method is better

            ### Concrete Example: Does This Drug Work?

            **Scenario:** A pharmaceutical company tests a new headache medication.

            **Step 1: Set up the hypothesis**
            - **Null hypothesis (H₀):** The drug doesn't work (pain reduction = 0)
            - **Alternative hypothesis (H₁):** The drug does work (pain reduction > 0)

            **Step 2: Collect sample data**
            - Test the drug on 100 people with headaches
            - Measure pain level before and after taking the drug
            - Find average pain reduction = 2.3 points (on a 0-10 scale)

            **Step 3: Calculate probability**
            - **Question:** "What's the probability of getting 2.3 points average reduction if the drug doesn't actually work?"
            - **Answer:** Based on the normal distribution, this probability is 0.02 (2%)

            **Step 4: Make a decision**
            - Since 2% < 5%, we reject the null hypothesis
            - **Conclusion:** The drug appears to work

            **Key insight:** We're not proving the drug works—we're saying the results would be very unlikely if it didn't work.

            ### The p < 0.05 Convention

            **Definition:** p-value is the probability of getting your sample results (or more extreme) if the null hypothesis is true.

            **The 5% rule:** If p < 0.05, we consider the result "statistically significant."

            **What this means:**
            - **p < 0.05:** Less than 5% chance this happened by random luck
            - **p ≥ 0.05:** Could easily have happened by random luck

            **Important:** p < 0.05 doesn't mean:
            - The effect is large or important
            - The result is definitely true
            - You've proven your hypothesis

            **It only means:** The result is unlikely to have occurred by chance alone.

            ### Sampling Error

            **Definition:** The difference between sample statistics and population parameters due to random variation.

            **Example:** Even if a coin is fair, you might get 7 heads out of 10 flips just by chance. This is sampling error.

            **Why sampling error matters:**
            - Every sample will be slightly different
            - We need to account for this when making inferences
            - Statistical tests help us distinguish real effects from sampling error

            ### Building Toward Hypothesis Testing

            **The big picture:** In future modules, you'll learn specific statistical tests (t-tests, ANOVA, correlation) that all follow this same logic:

            1. **State hypotheses** about population parameters
            2. **Calculate a test statistic** from your sample data
            3. **Find the p-value** (probability of getting this result by chance)
            4. **Make a decision** based on the p-value

            **Example preview (t-test):**
            - **Question:** Do men and women differ in height?
            - **Test:** Compare average heights in a sample
            - **Result:** p = 0.03
            - **Decision:** Since p < 0.05, conclude men and women do differ in height

            ### Why This Matters

            **For your assignments:** Understanding probability helps you interpret statistical results correctly.

            **For reading research:** You'll be able to evaluate whether researchers' conclusions are justified by their data.

            **For decision-making:** You'll understand the difference between statistical significance and practical importance.

            ### Quick Check

            **Question 1:** A researcher finds p = 0.08 for their statistical test. What should they conclude?

            **Answer:** They should NOT reject the null hypothesis because p > 0.05. The result could easily have happened by chance.

            **Question 2:** What does p = 0.01 mean?

            **Answer:** There's only a 1% chance of getting this result if the null hypothesis is true. This suggests the null hypothesis is probably false.

            **Question 3:** If you flip a fair coin 10 times and get 9 heads, what's the probability of this happening by chance?

            **Answer:** About 1% (very unlikely). This might make you suspect the coin isn't fair.

            ---

            ## Part 9: Practical Guide: Working with SPSS

            Now let's put theory into practice! SPSS (Statistical Package for the Social Sciences) is a powerful tool for statistical analysis. This section will walk you through the basics you'll need for your M1 assignment.

            ### Setting Up Your Dataset

            **Step 1: Open SPSS**
            - Launch SPSS from your computer or university lab
            - You'll see the Data Editor window with two tabs: "Data View" and "Variable View"

            **Step 2: Define Variables (Variable View)**
            - Click on "Variable View" tab
            - Each row represents one variable
            - Key columns to fill out:
              - **Name:** Variable name (no spaces, start with letter)
              - **Type:** Numeric (for numbers), String (for text)
              - **Label:** Full description of the variable
              - **Values:** Define value labels for categories
              - **Measure:** Scale, Ordinal, or Nominal

            **Example Variable Setup:**
            | Name | Label | Type | Values | Measure |
            |------|-------|------|--------|---------|
            | ID | Student ID | Numeric | | Scale |
            | Gender | Gender | Numeric | 1=Male, 2=Female | Nominal |
            | Hours | Study Hours | Numeric | | Scale |
            | Grade | Course Grade | Numeric | 1=F, 2=D, 3=C, 4=B, 5=A | Ordinal |

            **Step 3: Enter Data (Data View)**
            - Click on "Data View" tab
            - Each row is one participant
            - Each column is one variable
            - Enter your data carefully (double-check for errors)

            **Step 4: Save Your File**
            - File → Save As
            - Choose a location and descriptive filename
            - SPSS files have .sav extension

            ### Creating Frequency Tables

            **For Categorical Variables:**

            **Steps:**
            1. Analyze → Descriptive Statistics → Frequencies
            2. Move your categorical variable(s) to the "Variable(s)" box
            3. Click "Statistics" if you want additional statistics
            4. Click "Charts" if you want bar charts
            5. Click OK

            **Output includes:**
            - Frequency count for each category
            - Valid and missing percentages
            - Cumulative percentages

            **Example Output:**
            ```
            Gender
                        Frequency    Percent    Valid Percent    Cumulative Percent
            Valid   Male        25      50.0           50.0                50.0
                    Female      25      50.0           50.0               100.0
            Total              50     100.0          100.0
            ```

            ### Creating Grouped Frequency Tables

            **For Scale Variables:**

            **Method 1: Using Visual Binning**
            1. Transform → Visual Binning
            2. Select your scale variable
            3. Click "Make Cutpoints" → Equal Width Intervals
            4. Choose number of intervals (e.g., 5)
            5. Click "Make Labels" to create descriptive labels
            6. Click OK to create new grouped variable
            7. Run Frequencies on the new grouped variable

            **Method 2: Manual Grouping**
            1. Transform → Recode into Different Variables
            2. Select your scale variable
            3. Define ranges for each group
            4. Create new variable with group labels
            5. Run Frequencies on the new variable

            ### Creating Graphs

            **Bar Charts (for categorical data):**
            1. Graphs → Chart Builder
            2. Choose "Bar" from gallery
            3. Drag your categorical variable to X-axis
            4. Choose "Count" for Y-axis
            5. Click OK

            **Histograms (for scale data):**
            1. Graphs → Chart Builder
            2. Choose "Histogram" from gallery
            3. Drag your scale variable to X-axis
            4. Click OK

            **Customizing Graphs:**
            - Double-click on graph to open Chart Editor
            - Change colors, titles, axis labels
            - Add gridlines, legends, etc.

            ### Calculating Descriptive Statistics

            **For Scale Variables:**

            **Steps:**
            1. Analyze → Descriptive Statistics → Descriptives
            2. Move your scale variable(s) to the "Variable(s)" box
            3. Click "Options" to choose which statistics to calculate
            4. Recommended statistics: Mean, Std. Deviation, Min, Max
            5. Click OK

            **Output includes:**
            - Sample size (N)
            - Mean
            - Standard deviation
            - Minimum and maximum values
            - Range

            **Example Output:**
            ```
            Study Hours
                        N    Mean    Std. Deviation    Minimum    Maximum
            Valid       50   12.40            3.25        6.00       20.00
            ```

            **For All Variables (including categorical):**
            1. Analyze → Descriptive Statistics → Frequencies
            2. Move all variables to the "Variable(s)" box
            3. Click "Statistics" and select desired statistics
            4. Click OK

            ### Common SPSS Errors and Troubleshooting

            **Error: "Variable names must be unique"**
            - Solution: Check for duplicate variable names in Variable View

            **Error: "String variables cannot be used in arithmetic operations"**
            - Solution: Use Numeric type for variables you want to analyze

            **Error: "No cases in analysis"**
            - Solution: Check for missing data codes; use "Missing" column in Variable View

            **Graphs not displaying properly:**
            - Solution: Check that you have the right variable type (Scale for histograms, Nominal for bar charts)

            **Statistics showing as missing:**
            - Solution: Check for invalid data entry; use "Values" column to define valid codes

            ### Try It Yourself: Practice Exercise

            **Dataset:** Create a dataset with the following variables:
            - Student_ID (Scale): 1, 2, 3, 4, 5
            - Study_Method (Nominal): 1=Reading, 2=Practice Problems, 3=Group Study
            - Hours_Studied (Scale): 5, 8, 12, 6, 10
            - Test_Score (Scale): 78, 85, 92, 67, 89

            **Tasks:**
            1. Set up variables in Variable View
            2. Enter data in Data View
            3. Create frequency table for Study_Method
            4. Create histogram for Test_Score
            5. Calculate descriptive statistics for Hours_Studied and Test_Score
            6. Interpret your results

            **Expected Results:**
            - Study_Method frequencies: Reading (1), Practice Problems (1), Group Study (1), Other (2)
            - Test_Score mean: 82.2, Standard deviation: 9.8
            - Hours_Studied mean: 8.2, Standard deviation: 2.9

            ---

            ## Quick Reference Card

            ### Variable Classification Decision Tree
            1. **Can you do math with it?** No → Go to 2. Yes → Scale
            2. **Does it have order?** No → Nominal. Yes → Ordinal

            ### Measurement Level Quick Guide
            - **Nominal:** Categories only (Gender, Eye Color)
            - **Ordinal:** Ordered categories (Grade, Satisfaction Rating)
            - **Scale:** Numbers with meaning (Age, Height, Score)

            ### Essential Formulas at a Glance
            - **Mean:** Sum ÷ Count
            - **Median:** Middle value (or average of two middle values)
            - **Mode:** Most frequent value
            - **Range:** Highest - Lowest
            - **Standard Deviation:** √(Sum of squared differences ÷ (n-1))
            - **Z-Score:** (Value - Mean) ÷ Standard Deviation

            ### Central Tendency Decision Guide
            - **Normal distribution:** Use mean
            - **Skewed distribution:** Use median
            - **Nominal data:** Use mode

            ### Z-Score Interpretation Guide
            - **z = 0:** At the mean
            - **z = ±1:** 1 standard deviation from mean (68% rule)
            - **z = ±2:** 2 standard deviations from mean (95% rule)
            - **z = ±3:** 3 standard deviations from mean (99.7% rule)

            ### SPSS Variable Setup Checklist
            - [ ] Name: No spaces, starts with letter
            - [ ] Type: Numeric for numbers, String for text
            - [ ] Label: Clear description
            - [ ] Values: Define categories
            - [ ] Measure: Correct level (Scale/Ordinal/Nominal)

            ### Common Mistakes Checklist
            - [ ] Using mean for ordinal data
            - [ ] Forgetting n-1 in standard deviation
            - [ ] Using wrong graph type
            - [ ] Not defining variable labels in SPSS
            - [ ] Confusing sample and population

            ### Graph Selection Quick Guide
            - **Bar Chart:** Categorical data (nominal/ordinal)
            - **Histogram:** Scale data (continuous)
            - **Line Graph:** Time series or continuous relationships

            ### IV vs. DV Identification Trick
            - **IV:** What the researcher manipulates or assumes causes change
            - **DV:** What the researcher measures to see if it changes
            - **Memory:** IV is the "cause," DV is the "effect"

            ### Sample vs. Population Symbols
            - **Population:** μ (mean), σ (standard deviation), N (size)
            - **Sample:** x̄ (mean), s (standard deviation), n (size)

            ### n vs. n-1 Decision
            - **Population standard deviation:** Divide by N
            - **Sample standard deviation:** Divide by n-1 (bias correction)

            ### Module 1 Key Takeaways
            1. **Statistics organizes and interprets data** to move from opinion to evidence
            2. **Variables are the building blocks** of all research
            3. **Measurement level determines** which statistics are appropriate
            4. **Descriptive statistics summarize** what you have; inferential statistics generalize to populations
            5. **Normal distributions and z-scores** are the foundation of statistical inference
            6. **Probability concepts** help us understand statistical significance

            ### Connection to Future Modules
            - **Module 2:** One-sample t-tests (testing if sample mean differs from population mean)
            - **Module 3:** Independent and paired t-tests (comparing two groups)
            - **Module 4:** ANOVA (comparing multiple groups)
            - **Module 5:** Factorial designs (multiple independent variables)
            - **Module 6:** Correlation and regression (relationships between variables)

            Each module builds on these foundations, so master these concepts now!

            ---

            ## Summary and Key Formulas

            ### Core Concepts
            - **Statistics:** Mathematical tools for organizing, summarizing, and interpreting data
            - **Descriptive Statistics:** Summarize data you have collected
            - **Inferential Statistics:** Make conclusions about populations based on samples
            - **Variables:** Characteristics that can take different values
            - **Population:** Entire group you want to study
            - **Sample:** Subset of population you actually study

            ### Measures of Central Tendency
            - **Mean (x̄):** Sum of all values ÷ Number of values
            - **Median:** Middle value when data is ordered
            - **Mode:** Most frequently occurring value

            ### Measures of Variability
            - **Range:** Highest value - Lowest value
            - **Variance (s²):** Sum of squared differences ÷ (n-1)
            - **Standard Deviation (s):** √Variance

            ### Z-Scores
            - **Formula:** z = (Value - Mean) ÷ Standard Deviation
            - **Interpretation:** Number of standard deviations from the mean
            - **68-95-99.7 Rule:** 68% within 1 SD, 95% within 2 SD, 99.7% within 3 SD

            ### Symbols Reference
            - **Population:** μ (mean), σ (standard deviation), N (size)
            - **Sample:** x̄ (mean), s (standard deviation), n (size)
            - **Probability:** p (p-value)

            ### Key Distinctions
            - **Parameter vs. Statistic:** Population vs. sample characteristics
            - **Discrete vs. Continuous:** Counted vs. measured variables
            - **Independent vs. Dependent:** Cause vs. effect variables

            ### Analysis Decision Guide
            1. **Identify your variables** and their measurement levels
            2. **Choose appropriate descriptive statistics** based on measurement level
            3. **Create appropriate visualizations** (bar charts for categories, histograms for scale data)
            4. **Use n-1 correction** when calculating sample standard deviation
            5. **Interpret results** in context of your research question

            ---

            ## Glossary

            **Bias:** Systematic error that affects the accuracy of estimates
            **Central Tendency:** Measures that describe the "typical" value in a dataset
            **Continuous Variable:** Variable that can take any value within a range
            **Degrees of Freedom:** Number of values free to vary (n-1 for sample standard deviation)
            **Descriptive Statistics:** Methods for summarizing and describing data
            **Discrete Variable:** Variable that can only take specific, separate values
            **Frequency Distribution:** Summary showing how often each value occurs
            **Histogram:** Graph showing distribution of continuous data using bars that touch
            **Inferential Statistics:** Methods for drawing conclusions about populations from samples
            **Mean:** Average value (sum divided by count)
            **Median:** Middle value when data is ordered
            **Mode:** Most frequently occurring value
            **Normal Distribution:** Bell-shaped distribution where most values cluster around the mean
            **Parameter:** Numerical characteristic of a population
            **Population:** Entire group of interest in a study
            **Probability:** Likelihood that an event will occur (0 to 1)
            **Range:** Difference between highest and lowest values
            **Sample:** Subset of population actually studied
            **Standard Deviation:** Measure of how spread out values are from the mean
            **Statistic:** Numerical characteristic of a sample
            **Variable:** Characteristic that can take different values
            **Z-Score:** Number of standard deviations a value is from the mean

            ---

            ## Frequently Asked Questions

            **Q: Why do we divide by n-1 instead of n for sample standard deviation?**
            A: This corrects for bias. Samples tend to underestimate population variability because values are closer to the sample mean than the true population mean. Dividing by n-1 gives a better estimate of the population standard deviation.

            **Q: Can I use the mean for ordinal data?**
            A: No. Ordinal data has meaningful order but unequal intervals, so mathematical operations like averaging aren't appropriate. Use the median instead.

            **Q: What's the difference between a parameter and a statistic?**
            A: A parameter is a characteristic of the entire population (usually unknown). A statistic is a characteristic of your sample (what you actually calculate). We use statistics to estimate parameters.

            **Q: When should I use a histogram vs. a bar chart?**
            A: Use histograms for continuous scale data (bars touch). Use bar charts for categorical data (bars don't touch).

            **Q: What does p < 0.05 really mean?**
            A: It means there's less than a 5% chance of getting your sample results if the null hypothesis is true. It doesn't prove your hypothesis is correct or that the effect is large.

            **Q: Can I calculate a z-score for any type of data?**
            A: Z-scores are most meaningful for data that follows a normal distribution. They're less useful for highly skewed or categorical data.

            **Q: How do I know if my data is normally distributed?**
            A: Look at a histogram. Normal data should be roughly bell-shaped and symmetrical. You can also use statistical tests (like Shapiro-Wilk) that you'll learn about in future modules.

            **Q: What's the difference between descriptive and inferential statistics?**
            A: Descriptive statistics summarize the data you have (e.g., "the average age in our sample is 22"). Inferential statistics make conclusions about a larger population (e.g., "we estimate the average age of all college students is 22").

            ---

            ## Connections to Future Modules

            **Module 2: One-Sample Tests**
            - Uses z-scores and normal distributions to test if a sample mean differs from a known population mean
            - Applies probability concepts to hypothesis testing

            **Module 3: Two-Sample Tests**
            - Compares means between two groups using the same statistical reasoning
            - Builds on understanding of sampling error and probability

            **Module 4: Analysis of Variance (ANOVA)**
            - Extends t-test logic to compare multiple groups simultaneously
            - Uses the same probability framework for decision-making

            **Module 5: Factorial Designs**
            - Combines multiple independent variables
            - Requires understanding of variable classification and measurement levels

            **Module 6: Correlation and Regression**
            - Examines relationships between variables
            - Uses similar probability concepts for testing relationships

            Each module builds on the foundations you've learned here. Master these concepts, and you'll have a solid foundation for all future statistical analysis!

            ---

            ## Final Thoughts

            Congratulations! You've completed Module 1 and learned the fundamental concepts that form the foundation of statistical reasoning. You now understand:

            - How statistics helps us move from subjective opinion to objective evidence
            - How to identify and classify variables appropriately
            - How to describe data with numbers and visualizations
            - How samples relate to populations
            - How the normal distribution and z-scores work
            - How probability forms the basis of statistical inference
            - How to use SPSS for basic data analysis

            These concepts might seem abstract now, but they will become your tools for understanding research, evaluating claims, and making data-driven decisions throughout your academic and professional career.

            **Remember:** Statistics is not about memorizing formulas—it's about understanding the logic behind them. When you encounter new statistical concepts in future modules, always ask yourself: "What is this trying to tell me about my data? What does this mean in the context of my research question?"

            As you work through the M1 assignment, focus not just on getting the right answers, but on understanding **why** we do each step. When you calculate a standard deviation, think about what it tells you. When you create a histogram, consider what patterns the shape reveals. When you compare your manual calculations to SPSS output, reflect on the purpose of the n-1 adjustment.

            These fundamental statistical reasoning skills will serve you throughout your academic career and beyond—whether you're reading research papers, evaluating news headlines, or making data-driven decisions in your future career.

            **You've got this!** Statistics builds logically, step by step. Master these foundations, and everything that follows will make sense.

            ---

            _Remember: The goal isn't to memorize formulas—it's to understand the logic behind them. When in doubt, think about what the numbers mean in the context of your research question._
        </div>
    </div>

</div>

<script>
function showTab(tabNumber) {
    // Hide all panels
    const panels = document.querySelectorAll('.tab-panel');
    panels.forEach(panel => panel.classList.remove('active'));
    
    // Remove active from all buttons
    const buttons = document.querySelectorAll('.tab-button');
    buttons.forEach(button => button.classList.remove('active'));
    
    // Show selected panel and activate button
    document.getElementById(`tab-${tabNumber}`).classList.add('active');
    event.target.classList.add('active');
}
</script>
