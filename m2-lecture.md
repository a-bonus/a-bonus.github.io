---
layout: lecture
title: "Module 2: Introduction to Hypothesis Testing and the One-Sample t-Test"
---

<h1>Module 2: Introduction to Hypothesis Testing and the One-Sample t-Test</h1>

<div class="study-time">
    <strong>Estimated Study Time:</strong> 2-3 hours
</div>

<h2>Learning Objectives</h2>

<p>By the end of this module, you will be able to:</p>

<ol class="learning-objectives">
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

<p>In Module 1, you learned to <strong>describe</strong> data using means, standard deviations, and graphs. Now we take the crucial next step: using sample data to make <strong>inferences</strong> about populations.</p>

<div class="highlight-box">
    <p><strong>The Central Challenge:</strong> We can't study everyone, so we study a sample. But how do we know if what we observe in our sample reflects a real pattern in the population, or is just random chance?</p>
</div>

<div class="solution-box">
    <p><strong>The Solution:</strong> Hypothesis testing—a systematic method for distinguishing signal from noise.</p>
</div>

<h3>The Courtroom Analogy</h3>

<p>Hypothesis testing works like a legal trial. This analogy is powerful and worth understanding deeply.</p>

<div class="comparison-box">
    <h4>In a Courtroom:</h4>
    <ul>
        <li><strong>Presumption of Innocence:</strong> The defendant is assumed innocent until proven guilty</li>
        <li><strong>Burden of Proof:</strong> The prosecution must provide strong evidence of guilt</li>
        <li><strong>Standard of Proof:</strong> "Beyond a reasonable doubt"</li>
        <li><strong>Decision:</strong> If evidence is overwhelming, we reject innocence and conclude guilt. If evidence is weak, we maintain the presumption of innocence (we don't declare the person "innocent," just "not proven guilty")</li>
    </ul>

    <h4>In Hypothesis Testing:</h4>
    <ul>
        <li><strong>Null Hypothesis (H₀):</strong> We assume "nothing special is happening" (like presuming innocence)</li>
        <li><strong>Burden of Proof:</strong> Our data must provide strong evidence against this assumption</li>
        <li><strong>Standard of Proof:</strong> p < .05 (less than 5% probability the result is due to chance)</li>
        <li><strong>Decision:</strong> If evidence is strong (p < .05), we reject H₀ and conclude there IS an effect. If evidence is weak (p ≥ .05), we maintain H₀ (we don't "prove" H₀, just fail to find evidence against it)</li>
    </ul>

</div>

<div class="key-concept">
    <p><strong>Key Concept:</strong> We never "prove" anything in statistics. We only collect evidence strong enough to reject the null hypothesis, or fail to do so.</p>
</div>

<h3>Why This Backward Logic?</h3>

<div class="question-box">
    <p><strong>Why not just test our research hypothesis directly?</strong></p>
</div>

<p>Because we can never observe all possible outcomes. Consider:</p>

<div class="approach-comparison">
    <div class="approach-direct">
        <h4>Direct Approach (doesn't work):</h4>
        <p>"Does this drug improve memory?"</p>
        <ul>
            <li>To prove this directly, we'd need to test every possible person, under every possible condition, forever</li>
            <li><strong>Impossible!</strong></li>
        </ul>
    </div>

    <div class="approach-indirect">
        <h4>Indirect Approach (hypothesis testing):</h4>
        <p>"Assume the drug does nothing. How likely is it we'd see results this good by chance alone?"</p>
        <ul>
            <li>If the probability is very low (p < .05), the "does nothing" assumption is probably wrong</li>
            <li>We reject that assumption and conclude the drug likely works</li>
        </ul>
    </div>

</div>

<div class="mathematical-analogy">
    <p><strong>Think of it like proof by contradiction in mathematics:</strong> To prove X is true, assume X is false and show that leads to an impossible or highly unlikely situation. Therefore, X must be true.</p>
</div>

<h3>The Hypothesis Testing Process: Overview</h3>

<p>Here's the big picture before we dive into details:</p>

<ol class="process-steps">
    <li>
        <strong>Start with a research question</strong>
        <ul>
            <li>Example: "Does meditation reduce anxiety?"</li>
        </ul>
    </li>
    
    <li>
        <strong>Formulate hypotheses</strong>
        <ul>
            <li>H₀ (Null): Meditation has no effect on anxiety (μ = population mean)</li>
            <li>H₁ (Alternative): Meditation does affect anxiety (μ ≠ population mean)</li>
        </ul>
    </li>
    
    <li>
        <strong>Set decision criteria</strong>
        <ul>
            <li>Alpha level: Usually α = .05</li>
        </ul>
    </li>
    
    <li>
        <strong>Collect data</strong>
        <ul>
            <li>Sample of people who meditate regularly</li>
        </ul>
    </li>
    
    <li>
        <strong>Calculate a test statistic</strong>
        <ul>
            <li>Measures how far your sample result is from what H₀ predicts</li>
        </ul>
    </li>
    
    <li>
        <strong>Determine probability (p-value)</strong>
        <ul>
            <li>If H₀ were true, how likely would we see a result this extreme?</li>
        </ul>
    </li>
    
    <li>
        <strong>Make a decision</strong>
        <ul>
            <li>If p < .05: Reject H₀ (conclude meditation likely works)</li>
            <li>If p ≥ .05: Fail to reject H₀ (insufficient evidence)</li>
        </ul>
    </li>
    
    <li>
        <strong>Interpret in context</strong>
        <ul>
            <li>Translate statistical decision back into meaningful conclusion</li>
        </ul>
    </li>
</ol>

<h3>Real-World Example</h3>

<div class="example-scenario">
    <p><strong>Scenario:</strong> A school psychologist believes a new reading program improves comprehension.</p>
    
    <div class="data-given">
        <h4>What We Know:</h4>
        <ul>
            <li>National average reading score: μ = 100, σ = 15</li>
            <li>Our sample of 25 students using the new program: M = 107</li>
        </ul>
    </div>
    
    <div class="research-question">
        <p><strong>The Question:</strong> Is 107 significantly higher than 100, or could this difference be just random sampling variation?</p>
    </div>
    
    <div class="hypothesis-testing-answer">
        <h4>Hypothesis Testing Answers This:</h4>
        <ol>
            <li>H₀: The program doesn't work (students are just a random sample from the population where μ = 100)</li>
            <li>H₁: The program does work (students come from a different population where μ > 100)</li>
            <li>Calculate: How unlikely is it to get M = 107 from a population where μ = 100?</li>
            <li>Result: If probability is < 5%, we conclude the program likely works</li>
        </ol>
    </div>
    
    <div class="why-matters">
        <p><strong>Why This Matters:</strong> Without hypothesis testing, we couldn't distinguish:</p>
        <ul>
            <li>Real improvements from natural variation</li>
            <li>Effective treatments from placebos</li>
            <li>Meaningful differences from random noise</li>
        </ul>
    </div>
</div>

<h3>Common Misconceptions</h3>

<div class="misconceptions">
    <div class="misconception-item">
        <div class="misconception">
            <span class="incorrect">❌</span> <strong>Misconception:</strong> "If p < .05, we've proven our theory is true"
        </div>
        <div class="reality">
            <span class="correct">✓</span> <strong>Reality:</strong> We've only shown the null hypothesis is unlikely. Our theory is supported, not proven.
        </div>
    </div>
    
    <div class="misconception-item">
        <div class="misconception">
            <span class="incorrect">❌</span> <strong>Misconception:</strong> "If p > .05, we've proven there's no effect"
        </div>
        <div class="reality">
            <span class="correct">✓</span> <strong>Reality:</strong> We failed to find evidence of an effect. Maybe it doesn't exist, or maybe our sample was too small to detect it.
        </div>
    </div>
    
    <div class="misconception-item">
        <div class="misconception">
            <span class="incorrect">❌</span> <strong>Misconception:</strong> "p-value tells us the probability our hypothesis is true"
        </div>
        <div class="reality">
            <span class="correct">✓</span> <strong>Reality:</strong> p-value tells us the probability of getting our data IF the null hypothesis is true.
        </div>
    </div>
</div>

<div class="think-about-it">
    <p><strong>Think About It:</strong> Why is the distinction between "failing to find evidence" and "finding evidence of no effect" important? (Hint: absence of evidence is not evidence of absence!)</p>
</div>

---

<h2>Part 2: Formulating Hypotheses</h2>

<p>Every hypothesis test requires two competing hypotheses: the null (H₀) and the alternative (H₁ or Hₐ).</p>

<h3>The Null Hypothesis (H₀)</h3>

<div class="definition-box">
    <p><strong>Definition:</strong> A statement of "no effect," "no difference," or "no relationship." It represents the status quo or what we'd expect if nothing special is happening.</p>
</div>

<div class="key-characteristics">
    <h4>Key Characteristics:</h4>
    <ul>
        <li>Always includes an equals sign (=, ≤, or ≥)</li>
        <li>Represents the assumption we're trying to disprove</li>
        <li>The hypothesis we "presume true" until proven otherwise</li>
    </ul>
</div>

<div class="examples-section">
    <h4>Examples:</h4>
    <table class="examples-table">
        <thead>
            <tr>
                <th>Research Context</th>
                <th>Null Hypothesis</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>New drug for headaches</td>
                <td>H₀: The drug has no effect on headache duration (μ = 24 hours)</td>
            </tr>
            <tr>
                <td>Mindfulness training for stress</td>
                <td>H₀: Training doesn't reduce stress (μ = 50 on stress scale)</td>
            </tr>
            <tr>
                <td>Teaching method comparison</td>
                <td>H₀: The new method produces the same scores as traditional (μ = 75)</td>
            </tr>
            <tr>
                <td>Gender and salary</td>
                <td>H₀: There is no gender difference in salary (μ_male = μ_female)</td>
            </tr>
        </tbody>
    </table>
</div>

<h3>The Alternative Hypothesis (H₁ or Hₐ)</h3>

<div class="definition-box">
    <p><strong>Definition:</strong> The research hypothesis—what you actually believe or predict. It represents "something special is happening."</p>
</div>

<div class="key-characteristics">
    <h4>Key Characteristics:</h4>
    <ul>
        <li>Never includes an equals sign (uses ≠, <, or >)</li>
        <li>Represents what you're trying to find evidence for</li>
        <li>Can be directional or non-directional</li>
    </ul>
</div>

<div class="examples-section">
    <h4>Examples (matching the null hypotheses above):</h4>
    <table class="examples-table">
        <thead>
            <tr>
                <th>Research Context</th>
                <th>Alternative Hypothesis</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>New drug for headaches</td>
                <td>H₁: The drug reduces headache duration (μ < 24 hours)</td>
            </tr>
            <tr>
                <td>Mindfulness training for stress</td>
                <td>H₁: Training reduces stress (μ < 50 on stress scale)</td>
            </tr>
            <tr>
                <td>Teaching method comparison</td>
                <td>H₁: The new method produces different scores (μ ≠ 75)</td>
            </tr>
            <tr>
                <td>Gender and salary</td>
                <td>H₁: There is a gender difference in salary (μ_male ≠ μ_female)</td>
            </tr>
        </tbody>
    </table>
</div>

<h3>Directional vs. Non-Directional Hypotheses</h3>

<p>This is one of the most important decisions in hypothesis testing.</p>

<h4>Non-Directional (Two-Tailed) Hypotheses</h4>

<div class="hypothesis-type">
    <div class="when-used">
        <p><strong>Used when:</strong> You predict a difference or effect but <strong>not which direction</strong></p>
    </div>
    
    <div class="symbols">
        <p><strong>Symbols:</strong> H₁: μ ≠ [value]</p>
    </div>
    
    <div class="examples">
        <h5>Examples:</h5>
        <ul>
            <li>"Does caffeine affect reaction time?" (could make it faster OR slower)</li>
            <li>"Is the average age of psychology majors different from 20?" (could be higher OR lower)</li>
            <li>"Does music affect study performance?" (could help OR hurt)</li>
        </ul>
    </div>
    
    <div class="explanation">
        <p><strong>Why two-tailed?</strong> You're looking for extreme results in BOTH directions (both tails of the distribution)</p>
    </div>
</div>

<h4>Directional (One-Tailed) Hypotheses</h4>

<div class="hypothesis-type">
    <div class="when-used">
        <p><strong>Used when:</strong> You predict a <strong>specific direction</strong> of difference or effect</p>
    </div>
    
    <div class="symbols">
        <h5>Symbols:</h5>
        <ul>
            <li>H₁: μ > [value] (predicting an increase)</li>
            <li>H₁: μ < [value] (predicting a decrease)</li>
        </ul>
    </div>
    
    <div class="examples">
        <h5>Examples:</h5>
        <ul>
            <li>"Does this anti-anxiety medication reduce anxiety?" (specifically predicts decrease)</li>
            <li>"Are basketball players taller than average?" (specifically predicts increase)</li>
            <li>"Does sleep deprivation impair performance?" (specifically predicts impairment, not improvement)</li>
        </ul>
    </div>
    
    <div class="explanation">
        <p><strong>Why one-tailed?</strong> You're only looking for extreme results in ONE direction (one tail of the distribution)</p>
    </div>
</div>

<h3>How to Choose: Decision Tree</h3>

<div class="decision-question">
    <p><strong>Ask yourself:</strong> Does my research question predict a specific direction?</p>
</div>

<div class="decision-tree">
    <div class="tree-root">
        <p><strong>Research Question</strong></p>
    </div>
    
    <div class="tree-branch">
        <div class="branch-left">
            <p>├─ Predicts specific direction (increase/decrease, higher/lower, more/less)</p>
            <div class="branch-result">
                <p>└─→ <strong>ONE-TAILED TEST</strong></p>
                <ul>
                    <li>H₁: μ > [value] or μ < [value]</li>
                    <li>More statistical power to detect effect in predicted direction</li>
                    <li>But: Can't detect effects in opposite direction</li>
                </ul>
            </div>
        </div>
        
        <div class="branch-right">
            <p>└─ Asks about any difference/change (different from, affects, changes)</p>
            <div class="branch-result">
                <p>└─→ <strong>TWO-TAILED TEST</strong></p>
                <ul>
                    <li>H₁: μ ≠ [value]</li>
                    <li>Can detect effects in either direction</li>
                    <li>More conservative (safer choice when unsure)</li>
                </ul>
            </div>
        </div>
    </div>
</div>

<div class="when-in-doubt">
    <p><strong>When in Doubt:</strong> Use a two-tailed test. It's more conservative and protects against missing unexpected findings.</p>
</div>

<div class="critical-warning">
    <p><strong>⚠️ CRITICAL WARNING:</strong> You MUST decide whether to use a one-tailed or two-tailed test BEFORE collecting or looking at your data. Switching from two-tailed to one-tailed after seeing your results is called <strong>p-hacking</strong> and invalidates your statistical inference. This inflates your Type I error rate and is considered research misconduct.</p>
</div>

<h3>Practice: Writing Hypotheses</h3>

<p>For each research question, write H₀ and H₁, and indicate whether you'd use a one-tailed or two-tailed test.</p>

<div class="practice-scenarios">
    <div class="scenario">
        <h4>Scenario 1:</h4>
        <p>"A researcher wants to know if college students sleep less than the recommended 8 hours per night."</p>
        
        <details>
            <summary>Click to see answer</summary>
            <div class="answer">
                <ul>
                    <li><strong>Type:</strong> One-tailed (predicts "less than")</li>
                    <li><strong>H₀:</strong> μ ≥ 8 hours (students sleep 8 hours or more)</li>
                    <li><strong>H₁:</strong> μ < 8 hours (students sleep less than 8 hours)</li>
                </ul>
            </div>
        </details>
    </div>
    
    <div class="scenario">
        <h4>Scenario 2:</h4>
        <p>"Does listening to classical music while studying affect test scores? The national average is 75."</p>
        
        <details>
            <summary>Click to see answer</summary>
            <div class="answer">
                <ul>
                    <li><strong>Type:</strong> Two-tailed (asks "affect" without direction)</li>
                    <li><strong>H₀:</strong> μ = 75 (music has no effect)</li>
                    <li><strong>H₁:</strong> μ ≠ 75 (music affects scores, either way)</li>
                </ul>
            </div>
        </details>
    </div>
    
    <div class="scenario">
        <h4>Scenario 3:</h4>
        <p>"A therapist predicts that cognitive-behavioral therapy will lower depression scores below the clinical cutoff of 30."</p>
        
        <details>
            <summary>Click to see answer</summary>
            <div class="answer">
                <ul>
                    <li><strong>Type:</strong> One-tailed (predicts "lower")</li>
                    <li><strong>H₀:</strong> μ ≥ 30 (therapy doesn't lower scores below cutoff)</li>
                    <li><strong>H₁:</strong> μ < 30 (therapy lowers scores below cutoff)</li>
                </ul>
            </div>
        </details>
    </div>
    
    <div class="scenario">
        <h4>Scenario 4:</h4>
        <p>"Is the average IQ of chess champions different from the population mean of 100?"</p>
        
        <details>
            <summary>Click to see answer</summary>
            <div class="answer">
                <ul>
                    <li><strong>Type:</strong> Two-tailed (asks "different from")</li>
                    <li><strong>H₀:</strong> μ = 100 (chess champions have average IQ)</li>
                    <li><strong>H₁:</strong> μ ≠ 100 (chess champions differ from average)</li>
                </ul>
            </div>
        </details>
    </div>
</div>

<h3>Common Mistakes in Hypothesis Formulation</h3>

<div class="common-mistakes">
    <div class="mistake-item">
        <div class="mistake-header">
            <span class="incorrect">❌</span> <strong>Mistake 1:</strong> Making H₀ the research hypothesis
        </div>
        <ul>
            <li><span class="wrong">Wrong:</span> H₀: The drug reduces pain</li>
            <li><span class="right">Right:</span> H₁: The drug reduces pain; H₀: The drug has no effect</li>
        </ul>
    </div>
    
    <div class="mistake-item">
        <div class="mistake-header">
            <span class="incorrect">❌</span> <strong>Mistake 2:</strong> Forgetting the equals sign in H₀
        </div>
        <ul>
            <li><span class="wrong">Wrong:</span> H₀: μ > 50</li>
            <li><span class="right">Right:</span> H₀: μ = 50 (or μ ≤ 50 for one-tailed)</li>
        </ul>
    </div>
    
    <div class="mistake-item">
        <div class="mistake-header">
            <span class="incorrect">❌</span> <strong>Mistake 3:</strong> Using wrong direction for one-tailed test
        </div>
        <ul>
            <li>If predicting scores will increase: H₁: μ > [value], not μ < [value]</li>
        </ul>
    </div>
    
    <div class="mistake-item">
        <div class="mistake-header">
            <span class="incorrect">❌</span> <strong>Mistake 4:</strong> Being too specific in the alternative hypothesis
        </div>
        <ul>
            <li><span class="wrong">Wrong:</span> H₁: μ = 105 (this is too specific; we don't know the exact value)</li>
            <li><span class="right">Right:</span> H₁: μ > 100 (we predict it's greater, but not a specific value)</li>
        </ul>
    </div>
</div>

<div class="key-concept">
    <p><strong>Key Concept:</strong> The null hypothesis always represents the "boring" or "no effect" outcome. The alternative represents the "interesting" or "something is happening" outcome.</p>
</div>

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

<p>Once we've formulated hypotheses and collected data, we need a systematic way to decide which hypothesis the evidence supports.</p>

<h3>Understanding p-Values</h3>

<p>The <strong>p-value</strong> is the most important concept in hypothesis testing—and also the most misunderstood.</p>

<div class="definition-box">
    <p><strong>Definition:</strong> The probability of obtaining a result as extreme as (or more extreme than) the one observed, <strong>assuming the null hypothesis is true</strong>.</p>
</div>

<div class="plain-english">
    <p><strong>In Plain English:</strong> If there really is no effect (H₀ is true), how surprising would our result be? How often would random chance alone produce data this extreme?</p>
</div>

<div class="example-box">
    <p><strong>Example:</strong> You test a memory drug and get p = .03</p>
    
    <p><strong>This means:</strong> If the drug actually does nothing (H₀ is true), there's only a 3% chance we'd see improvement this large due to random sampling variation alone.</p>
    
    <p><strong>Interpretation:</strong> That's pretty unlikely! Either:</p>
    <ol>
        <li>We got really lucky with our random sample (3% chance), OR</li>
        <li>The drug actually works (H₀ is probably false)</li>
    </ol>
    <p>We conclude #2 is more plausible.</p>
</div>

<div class="understanding-box">
    <h4>📊 UNDERSTANDING P-VALUES: The Most Misunderstood Concept</h4>
    
    <div class="what-are">
        <h5>What p-values ARE:</h5>
        <ul>
            <li>The probability of getting your data (or more extreme) IF H₀ is true</li>
            <li>A measure of how surprising your results are under the null hypothesis</li>
            <li>Conditional on H₀ being true</li>
        </ul>
    </div>
    
    <div class="what-are-not">
        <h5>What p-values are NOT:</h5>
        <ul>
            <li><span class="incorrect">❌</span> The probability that H₀ is true</li>
            <li><span class="incorrect">❌</span> The probability that your results are due to chance</li>
            <li><span class="incorrect">❌</span> The probability that H₁ is true</li>
            <li><span class="incorrect">❌</span> The probability you made a mistake</li>
        </ul>
    </div>
    
    <div class="key-insight">
        <p><strong>Key Insight:</strong> p-values assume H₀ is true and ask "how weird is our data?" They do NOT tell us the probability that our hypothesis is correct!</p>
    </div>
</div>

<h3>The Alpha Level (α)</h3>

<div class="definition-box">
    <p><strong>Definition:</strong> The threshold for deciding if a p-value is "small enough" to reject H₀. The maximum probability of making a Type I error we're willing to accept.</p>
</div>

<div class="standard-value">
    <p><strong>Standard Value:</strong> α = .05 (5%)</p>
</div>

<div class="decision-rule">
    <h4>The Decision Rule:</h4>
    <ul>
        <li>If p < α (.05): Reject H₀ → Result is <strong>statistically significant</strong></li>
        <li>If p ≥ α (.05): Fail to reject H₀ → Result is <strong>not statistically significant</strong></li>
    </ul>
</div>

<div class="why-alpha">
    <p><strong>Why .05?</strong></p>
    <p>This is somewhat arbitrary! It was popularized by statistician Ronald Fisher in the 1920s.</p>
</div>

<div class="different-alphas">
    <h4>Different fields sometimes use different alphas:</h4>
    <ul>
        <li>Physics: α = .0000003 (very stringent)</li>
        <li>Medicine: α = .05 (standard)</li>
        <li>Exploratory research: Sometimes α = .10 (more lenient)</li>
    </ul>
</div>

<div class="principle">
    <p><strong>The principle:</strong> Lower α = more conservative (harder to reject H₀) = less risk of false positives</p>
</div>

<h3>Worked Example: Making a Decision</h3>

<div class="worked-example">
    <div class="scenario">
        <p><strong>Scenario:</strong> Testing if a new teaching method improves test scores</p>
    </div>
    
    <div class="given-information">
        <h4>Given Information:</h4>
        <ul>
            <li>National average: μ = 70</li>
            <li>Sample of 30 students using new method: M = 75, s = 12</li>
            <li>Statistical test yields: t(29) = 2.36, p = .025</li>
            <li>Alpha level: α = .05</li>
        </ul>
    </div>
    
    <div class="steps">
        <div class="step">
            <h4>Step 1: State hypotheses</h4>
            <ul>
                <li>H₀: μ = 70 (method doesn't work)</li>
                <li>H₁: μ ≠ 70 (method has an effect)</li>
            </ul>
        </div>
        
        <div class="step">
            <h4>Step 2: Compare p-value to alpha</h4>
            <ul>
                <li>p = .025</li>
                <li>α = .05</li>
                <li>Is .025 < .05? <strong>Yes</strong></li>
            </ul>
        </div>
        
        <div class="step">
            <h4>Step 3: Make statistical decision</h4>
            <ul>
                <li>Since p < α, we <strong>reject the null hypothesis</strong></li>
            </ul>
        </div>
        
        <div class="step">
            <h4>Step 4: State conclusion</h4>
            <p>"The new teaching method produced significantly different test scores (M = 75, SD = 12) compared to the national average of 70, t(29) = 2.36, p = .025. Students using the new method scored higher than expected if the method had no effect."</p>
        </div>
    </div>
</div>

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

μ<sub>M</sub> = μ

The average of all possible sample means equals the true population mean.

**2. The standard deviation of the sampling distribution (Standard Error) is smaller than the population SD**

σ<sub>M</sub> = σ / √n

Sample means vary less than individual scores. Larger samples have even less variation.

**3. The shape approaches normal as n increases**

- n ≥ 30: Usually sufficient for good approximation
- n ≥ 100: Very close to perfect normal
- For populations already normal: Works even with small n

### Standard Error: The Variability of Means

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

**Examples:**

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

## Part 7: Effect Size: Measuring Practical Significance

Statistical significance tells you IF there's an effect. Effect size tells you HOW BIG the effect is.

> **Connection to previous concepts:** Remember the distinction between statistical and practical significance from [Part 3](#part-3-the-decision-making-framework)? Effect size is how we measure practical significance. A result can be statistically significant (p < .05) but have a tiny effect size, or have a large effect size but not be statistically significant (underpowered study).

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

d = (M - μ) / s

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
- d = (45 - 50) / 12 = -5 / 12 = -0.42
- **Interpretation:** Small to medium effect (stress is 0.42 SD below population mean)

**Example 2:** Reading program effectiveness

- Population mean: μ = 100
- Sample: M = 112, s = 15
- d = (112 - 100) / 15 = 12 / 15 = 0.80
- **Interpretation:** Large effect (reading scores are 0.80 SD above population mean)

**What This Means in Practice:**

- This is a **substantial improvement** - students improved by 12 points on average
- A Cohen's d of 0.80 is considered educationally significant
- In practical terms: If the program works, it could move an average student from the 50th percentile to approximately the 79th percentile
- **Cost-benefit consideration:** If the program is affordable and scalable, this effect size would strongly support implementation
- **Caution:** Need to verify with randomized controlled trial to rule out selection effects (maybe better students chose the program)

**Example 3:** Memory drug trial

- Population mean: μ = 50
- Sample: M = 52, s = 10
- d = (52 - 50) / 10 = 2 / 10 = 0.20
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

### Complete APA Reporting Guidelines

**Essential Components to Include:**

1. **Descriptive statistics:** M and SD for your sample
2. **Comparison value:** The population mean you're comparing against
3. **Test statistic:** t(df) = value
4. **p-value:** Exact value when possible, or p < .001 for very small values
5. **Effect size:** Cohen's d
6. **Direction and significance:** Clearly state whether the difference was significant and in which direction

**Reporting p-Values:**

| SPSS Output | How to Report               | Why                                    |
| ----------- | --------------------------- | -------------------------------------- |
| p = .000    | **p < .001**                | Never report p = .000; it's rounded    |
| p = .0234   | **p = .023**                | Round to 2-3 decimal places            |
| p = .050    | **p = .050**                | Report exactly (borderline case)       |
| p = .0499   | **p = .050**                | Round to 3 decimals, or report exactly |
| p = .347    | **p = .347** or **p = .35** | Either is acceptable                   |

**Common Reporting Mistakes to Avoid:**

❌ **Wrong:** "The result was p = .000"
✓ **Right:** "The result was p < .001"

❌ **Wrong:** "t = 2.45 with p < .05"
✓ **Right:** "t(23) = 2.45, p = .023" (report exact p when available)

❌ **Wrong:** "The difference was not significant (p = .08)"
✓ **Right:** "The difference was not significant, t(45) = 1.78, p = .08, d = 0.26"

❌ **Wrong:** "Participants scored M = 85"
✓ **Right:** "Participants (M = 85, SD = 12) scored..."

❌ **Wrong:** "Results were significant at the .05 level"
✓ **Right:** "Results were significant, t(30) = 2.34, p = .026"

### APA Format for Different Scenarios

**Scenario 1: Significant Result (Two-Tailed)**
"College students (M = 6.2, SD = 1.3) slept significantly less than the recommended 8 hours, t(149) = -8.52, p < .001, d = 1.38, suggesting substantial sleep deprivation in this population."

**Scenario 2: Non-Significant Result (Two-Tailed)**
"Participants receiving the new study technique (M = 78.5, SD = 11.2) did not differ significantly from the national average of 75, t(32) = 1.79, p = .082, d = 0.31, though the medium effect size suggests the study may have been underpowered."

**Scenario 3: Significant Result (One-Tailed)**
"As predicted, athletes who underwent visualization training (M = 142.3, SD = 18.7) performed significantly better than the population mean of 130, t(27) = 3.48, p = .001 (one-tailed), d = 0.66."

**Scenario 4: Reporting with Context**
"Participants in the mindfulness intervention group (M = 42.1, SD = 9.3) showed significantly lower anxiety scores compared to the clinical cutoff of 50, t(38) = -5.30, p < .001, d = 0.85. This large effect suggests the intervention moved participants from clinically significant anxiety to subclinical levels."

**Best Practices:**

- **Always include SD:** Readers need it to understand variability and calculate effect sizes
- **Report exact p-values:** Don't just say "p < .05" when you have the exact value
- **Include effect size:** Required by most journals and essential for meta-analyses
- **Interpret in context:** Don't just report numbers; explain what they mean
- **Be honest about limitations:** Mention if sample was small, not randomized, etc.

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

## Part 8: Statistical Power

Power is your study's ability to detect a real effect when one exists. Understanding power helps you design better studies and interpret null results.

> **Connection to previous concepts:**
>
> - Power is directly related to **Type II errors** from [Part 4](#part-4-understanding-errors-in-hypothesis-testing): Power = 1 - β
> - Power depends on **effect size** from [Part 7](#part-7-effect-size-measuring-practical-significance): Larger effects are easier to detect
> - Power is why we care about **sample size**: Bigger samples = more power to detect real effects

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

## Part 9: The t-Distribution

We've been using the t-test, but what exactly is this "t-distribution"?

### Why Not Use the Normal Distribution (z)?

**Remember the z-score formula:**

z = (X - μ) / σ

**For testing sample means:**

z = (M - μ) / (σ / √n)

**The problem:** We almost never know σ (population standard deviation)!

**Our solution:** Substitute s (sample standard deviation)

t = (M - μ) / (s / √n)

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

df = n - 1

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
