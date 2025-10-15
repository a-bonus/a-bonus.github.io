# Lecture HTML Conversion Guidelines

This document provides standards and guidelines for converting markdown lecture files (M3-M6) to HTML format, ensuring consistency with the established M1 and M2 lecture designs.

## Overview

All lecture HTML files should follow the same structure and styling patterns to maintain visual consistency and user experience across modules. The design is based on the enhanced M1 and M2 lecture templates, which include improved knowledge check functionality, professional glossary formatting, and visual diagram styling.

## Required HTML Structure

### 1. Document Head

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Module X: [Module Title]</title>
    <link rel="stylesheet" href="assets/css/main.css" />
    <style>
      /* Required CSS for Knowledge Checks, Glossary, and Visual Elements */
    </style>
  </head>
</html>
```

### 2. Body Structure

```html
<body>
    <main>
        <h1>Module X: [Module Title]</h1>

        <p><strong>Estimated Study Time:</strong> X-X hours</p>

        <h2>Learning Objectives</h2>
        <p>By the end of this module, you will be able to:</p>
        <ol class="learning-objectives">
            <li>Objective 1</li>
            <li>Objective 2</li>
            <!-- etc. -->
        </ol>

        <hr>

        <div class="lecture-tabs">
            <!-- Tab Navigation and Content -->
        </div>

        <!-- Bottom Navigation -->
        <div class="tab-navigation bottom-nav">
            <!-- Duplicate tab buttons -->
        </div>
    </main>

    <script>
        <!-- JavaScript functions -->
    </script>
</body>
</html>
```

## Required CSS in `<style>` Section

### Include ALL of these styles for consistency:

```css
/* Knowledge Check Styling */
.knowledge-check-item {
  background-color: #f8f9fa;
  border-left: 4px solid #007bff;
  padding: 15px;
  margin: 15px 0;
  border-radius: 4px;
}

.knowledge-check-item.answered {
  border-left-color: #28a745;
  background-color: #f0f8f4;
}

.question-text {
  font-weight: 500;
  margin-bottom: 10px;
}

.question-options {
  margin: 10px 0;
  list-style-position: inside;
}

.answer-reveal {
  background-color: #e7f3ff;
  border: 1px solid #b3d9ff;
  padding: 12px;
  margin-top: 10px;
  border-radius: 4px;
}

.answer-text {
  margin: 0;
  color: #004085;
}

.reveal-answer-btn {
  background-color: #007bff;
  color: white;
  border: none;
  padding: 8px 16px;
  border-radius: 4px;
  cursor: pointer;
  font-size: 14px;
  margin-top: 10px;
  transition: background-color 0.2s;
}

.reveal-answer-btn:hover {
  background-color: #0056b3;
}

.reveal-answer-btn.answered {
  background-color: #28a745;
}

.reveal-answer-btn.answered:hover {
  background-color: #218838;
}

/* Learning Objectives Styling */
.learning-objectives {
  margin: 15px 0;
}

.learning-objectives > li {
  margin-bottom: 8px;
}

/* Glossary Styling */
.glossary-section {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 20px;
  margin: 20px 0;
}

.glossary-item {
  background-color: #f8f9fa;
  border: 1px solid #dee2e6;
  border-radius: 6px;
  padding: 15px;
}

.glossary-item h4 {
  color: #007bff;
  margin-bottom: 8px;
  font-size: 1.1em;
}

.glossary-item p {
  margin: 0;
  color: #495057;
  line-height: 1.5;
}

/* Visual Diagrams Styling */
.visual-diagram {
  background-color: #f8f9fa;
  border: 1px solid #dee2e6;
  border-radius: 8px;
  padding: 20px;
  margin: 20px 0;
}

.visual-diagram h4 {
  color: #495057;
  margin-bottom: 15px;
  border-bottom: 2px solid #007bff;
  padding-bottom: 5px;
}

.diagram-caption {
  text-align: center;
  font-size: 0.9em;
  color: #6c757d;
  margin-top: 10px;
  font-style: italic;
}
```

### DO NOT include:

- Custom content box styles (`.highlight-box`, `.solution-box`, etc.)
- Custom table styles
- Custom list styles
- Any module-specific styling beyond the required styles above

## Tab Navigation Pattern

### Top Navigation Structure:

```html
<div class="lecture-tabs">
  <div class="tab-navigation">
    <button class="tab-button active" onclick="showTab(1)">
      <input
        type="checkbox"
        id="progress-1"
        class="tab-checkbox"
        onchange="toggleTabComplete(1)"
      />
      <span class="tab-label">Tab 1 Name</span>
    </button>
    <!-- Repeat for all tabs -->
  </div>

  <div class="tab-content">
    <div id="tab-1" class="tab-panel active">
      <!-- Tab content -->
    </div>
    <!-- Repeat for all tabs -->
  </div>
</div>
```

### Bottom Navigation Structure:

```html
<!-- Single Bottom Navigation -->
<div class="tab-navigation bottom-nav">
  <button class="tab-button" onclick="showTab(1)">
    <input
      type="checkbox"
      id="progress-1-bottom"
      class="tab-checkbox"
      onchange="toggleTabComplete(1)"
    />
    <span class="tab-label">Tab 1 Name</span>
  </button>
  <!-- Repeat for all tabs with -bottom suffix on IDs -->
</div>
```

## Required JavaScript Functions

### 1. Progress Tracking Setup

```javascript
// Progress tracking storage key
const PROGRESS_KEY = "mX-lecture-progress"; // Replace X with module number
```

### 2. Load Progress Function

```javascript
function loadProgress() {
  const savedProgress = localStorage.getItem(PROGRESS_KEY);
  if (savedProgress) {
    const progress = JSON.parse(savedProgress);
    // Update all checkboxes based on saved progress
    for (let i = 1; i <= 5; i++) {
      // Adjust number based on tabs
      const isComplete = progress[i] || false;
      const checkbox = document.getElementById(`progress-${i}`);
      const bottomCheckbox = document.getElementById(`progress-${i}-bottom`);
      if (checkbox) checkbox.checked = isComplete;
      if (bottomCheckbox) bottomCheckbox.checked = isComplete;
      updateTabVisualState(i, isComplete);
    }
  }
}
```

### 3. Save Progress Function

```javascript
function saveProgress(tabNumber, isComplete) {
  const savedProgress = localStorage.getItem(PROGRESS_KEY);
  const progress = savedProgress ? JSON.parse(savedProgress) : {};
  progress[tabNumber] = isComplete;
  localStorage.setItem(PROGRESS_KEY, JSON.stringify(progress));
}
```

### 4. Tab Complete Toggle Function

```javascript
function toggleTabComplete(tabNumber) {
  // Determine which checkbox was clicked (top or bottom)
  const clickedCheckbox = event.target;
  const isComplete = clickedCheckbox.checked;

  // Update both top and bottom checkboxes to stay in sync
  const topCheckbox = document.getElementById(`progress-${tabNumber}`);
  const bottomCheckbox = document.getElementById(
    `progress-${tabNumber}-bottom`
  );
  if (topCheckbox) topCheckbox.checked = isComplete;
  if (bottomCheckbox) bottomCheckbox.checked = isComplete;

  // Update visual state
  updateTabVisualState(tabNumber, isComplete);

  // Save to localStorage
  saveProgress(tabNumber, isComplete);
}
```

### 5. Tab Visual State Function

```javascript
function updateTabVisualState(tabNumber, isComplete) {
  const buttons = document.querySelectorAll(
    `.tab-button:nth-child(${tabNumber})`
  );
  buttons.forEach((button) => {
    if (isComplete) {
      button.classList.add("completed");
    } else {
      button.classList.remove("completed");
    }
  });
}
```

### 6. Show Tab Function

```javascript
function showTab(tabNumber) {
  // Hide all panels
  const panels = document.querySelectorAll(".tab-panel");
  panels.forEach((panel) => panel.classList.remove("active"));

  // Remove active class from all buttons
  const buttons = document.querySelectorAll(".tab-button");
  buttons.forEach((button) => button.classList.remove("active"));

  // Show selected panel and activate button
  document.getElementById(`tab-${tabNumber}`).classList.add("active");
  const activeButton = document.querySelector(
    `.tab-button:nth-child(${tabNumber})`
  );
  if (activeButton) activeButton.classList.add("active");

  // Scroll to tabs
  const tabContainer = document.querySelector(".lecture-tabs");
  if (tabContainer) {
    tabContainer.scrollIntoView({ behavior: "smooth", block: "start" });
  }
}
```

### 7. Knowledge Check Functions

```javascript
// Knowledge check functionality with toggle
function revealAnswer(questionId) {
  const questionItem = document.querySelector(
    `[data-question-id="${questionId}"]`
  );
  const answerDiv = questionItem.querySelector(".answer-reveal");
  const button = questionItem.querySelector(".reveal-answer-btn");

  if (answerDiv && button) {
    if (answerDiv.style.display === "none" || answerDiv.style.display === "") {
      // Show the answer
      answerDiv.style.display = "block";
      button.textContent = "Hide Answer";
      button.classList.add("answered");
      questionItem.classList.add("answered");

      // Save to storage
      markQuestionAsAnswered(questionId, true);
    } else {
      // Hide the answer
      answerDiv.style.display = "none";
      button.textContent = "Show Answer";
      button.classList.remove("answered");
      questionItem.classList.remove("answered");
    }
  }
}

// Knowledge check storage functions
const KC_STORAGE_KEY = "mX-knowledge-checks"; // Replace X with module number

function saveAnsweredQuestion(questionId) {
  const savedProgress = localStorage.getItem(KC_STORAGE_KEY);
  const answeredQuestions = savedProgress ? JSON.parse(savedProgress) : [];

  if (!answeredQuestions.includes(questionId)) {
    answeredQuestions.push(questionId);
    localStorage.setItem(KC_STORAGE_KEY, JSON.stringify(answeredQuestions));
  }
}

function markQuestionAsAnswered(questionId, saveToStorage) {
  const questionItem = document.querySelector(
    `[data-question-id="${questionId}"]`
  );
  if (!questionItem) return;

  // Save to storage if requested
  if (saveToStorage) {
    saveAnsweredQuestion(questionId);
  }
}

function loadKnowledgeCheckProgress() {
  const savedProgress = localStorage.getItem(KC_STORAGE_KEY);
  if (savedProgress) {
    const answeredQuestions = JSON.parse(savedProgress);
    answeredQuestions.forEach((questionId) => {
      markQuestionAsAnswered(questionId, false);
    });
  }
}
```

### 8. Document Ready Function

```javascript
document.addEventListener("DOMContentLoaded", function () {
  loadProgress();
  loadKnowledgeCheckProgress();
});
```

## Content Structure Guidelines

### 1. Image Paths

Use the convention: `assets/mX-assets/image-name.png`

- Replace X with module number
- Use descriptive, kebab-case filenames
- Place images in appropriate module asset folder

### 2. Knowledge Check HTML Pattern

```html
<div class="knowledge-check-item" data-question-id="tabX-q1">
  <p class="question-text"><strong>Question 1:</strong> Question text here?</p>
  <ul class="question-options">
    <li>A) Option A</li>
    <li>B) Option B</li>
    <li>C) Option C</li>
    <li>D) Option D</li>
  </ul>
  <div class="answer-reveal" style="display: none;">
    <div class="answer-content">
      <p class="correct-answer">Correct Answer: B) Option B</p>
      <p class="explanation">
        Explanation of why this answer is correct and why others are incorrect.
      </p>
    </div>
  </div>
  <button class="reveal-answer-btn" onclick="revealAnswer('tabX-q1')">
    Show Answer
  </button>
</div>
```

**Important Notes:**

- Use `data-question-id` instead of `id` for consistency
- Include question number in the ID (e.g., `tab1-q1`, `tab2-q3`)
- Use proper semantic HTML with `<ul>` for options
- Include both correct answer and explanation
- Button text should start as "Show Answer"

### 3. Glossary HTML Pattern

```html
<h2>Glossary</h2>

<div class="glossary-section">
  <div class="glossary-item">
    <h4>Term Name</h4>
    <p>Clear, concise definition of the term</p>
  </div>

  <div class="glossary-item">
    <h4>Another Term</h4>
    <p>Definition for this term</p>
  </div>

  <!-- Continue for all terms -->
</div>
```

**Important Notes:**

- Use the grid layout for professional appearance
- Keep definitions concise but complete
- Include all key statistical terms from the module
- Maintain alphabetical order when possible

### 4. Visual Diagram HTML Pattern

```html
<div class="visual-diagram">
  <h4>📊 Diagram Title</h4>
  <div class="diagram-content">
    <!-- Your diagram content here -->
    <p>Explanation text for the diagram</p>
  </div>
  <p class="diagram-caption">
    <em>Figure X.Y: Caption describing the diagram</em>
  </p>
</div>
```

**Important Notes:**

- Use emoji icons for visual appeal (📊, 🔄, 📈, etc.)
- Include figure numbering for reference
- Provide clear captions
- Keep content focused and educational

### 5. Tab Content Organization

- Each tab should be a logical unit of content
- Use clear headings (h2, h3) within tabs
- Maintain consistent spacing and structure
- Include knowledge checks at appropriate points
- Add "Quick Check" sections throughout content
- Include visual diagrams where helpful

## Conversion Checklist

### Pre-Conversion:

- [ ] Review markdown file for all content sections
- [ ] Identify logical tab divisions
- [ ] Gather all images and place in appropriate asset folder
- [ ] Plan tab names and structure

### During Conversion:

- [ ] Create proper HTML document structure
- [ ] Add ALL required CSS (knowledge checks, glossary, visual diagrams)
- [ ] Implement tab navigation (top and bottom)
- [ ] Convert markdown content to HTML
- [ ] Add knowledge checks with proper HTML structure and toggle functionality
- [ ] Create professional glossary with grid layout
- [ ] Add visual diagrams where appropriate
- [ ] Update image paths to use asset folders
- [ ] Add all required JavaScript functions (including knowledge check storage)
- [ ] Test tab switching functionality
- [ ] Test progress tracking (localStorage)
- [ ] Test knowledge check show/hide functionality

### Post-Conversion:

- [ ] Verify all tabs display correctly
- [ ] Test knowledge check show/hide toggle functionality
- [ ] Verify progress tracking works for both top and bottom nav
- [ ] Test knowledge check localStorage persistence
- [ ] Verify glossary displays in proper grid format
- [ ] Test visual diagrams display correctly
- [ ] Check responsive design on mobile
- [ ] Validate HTML syntax
- [ ] Test with different browsers
- [ ] Ensure consistent styling with M1/M2
- [ ] Verify learning objectives display without redundant numbering

## File Naming Convention

- Lecture HTML files: `mX-lecture.html`
- Asset folders: `assets/mX-assets/`
- Images: descriptive names in kebab-case

## Enhanced Features (M1/M2 Standard)

### Knowledge Check Improvements:

- **Toggle Functionality**: Show/Hide Answer buttons that work properly
- **Visual Feedback**: Green borders and styling when answered
- **LocalStorage Persistence**: Remembers which questions have been answered
- **Improved UX**: Better button text and state management

### Glossary Enhancements:

- **Professional Grid Layout**: Responsive 2-3 column grid
- **Consistent Styling**: Blue headers, clean backgrounds
- **Better Typography**: Improved readability and spacing

### Visual Diagram Support:

- **Ready-to-Use CSS**: Professional styling for educational diagrams
- **Figure Captions**: Consistent caption formatting
- **Icon Support**: Emoji icons for visual appeal

### Learning Objectives:

- **Clean Numbering**: No redundant circular icons
- **Consistent Spacing**: Proper margins and typography

## Notes

- Keep custom CSS minimal - rely on `main.css` for most styling
- Maintain consistency with established patterns
- Test thoroughly before publishing
- Update this guide if new patterns are established
- **Always include ALL required CSS** for full functionality
- **Test knowledge check toggle functionality** before publishing
- **Ensure glossary uses grid layout** for professional appearance

## Module-Specific Considerations

### M3: Independent and Paired t-Tests

- Focus on comparison between groups
- Include examples of both test types
- Emphasize when to use each test

### M4: ANOVA

- Multiple group comparisons
- Include post-hoc testing concepts
- Effect size calculations

### M5: Mixed Factorial ANOVA

- Complex designs
- Interaction effects
- Multiple factors

### M6: Correlation and Regression

- Relationship analysis
- Prediction concepts
- Multiple regression introduction

Each module should follow these guidelines while adapting content to the specific statistical concepts covered.
