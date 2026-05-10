# NOTEBOOK_TEMPLATE.md

# Standard Notebook Template

This document defines the standard structure and formatting conventions for all notebooks in this repository.

The purpose of the template is to ensure:

* pedagogical consistency
* beginner readability
* predictable notebook organization
* reduced cognitive load
* reproducible analytical workflows

All notebooks should follow this structure as closely as practical.

---

# General Notebook Principles

Every notebook should:

* run successfully from top to bottom using "Run All"
* contain explanatory Markdown between code cells
* avoid large unexplained code blocks
* prioritize readability over compactness
* contain visible outputs
* reinforce confidence for beginners
* include reflection and interpretation

The notebooks should resemble:

* guided workshops
* practical analytical workbooks
* reproducible tutorials

The notebooks should NOT resemble:

* formal programming textbooks
* computer science theory notes
* algorithm-heavy exercises

---

# Standard Notebook Structure

Each notebook should follow the structure below.

```markdown
# Notebook Title

## Learning Outcomes

## Introduction

## Environment Setup

## Instructor Demonstration

## Guided Practice

## Check Your Understanding

## Independent Mini Task

## Common Mistakes

## Reflection

## Optional Bonus Tasks

## Summary
```

---

# Notebook Header Template

Each notebook should begin with a clear introductory Markdown section.

Example:

```markdown
# Introduction to Filtering and Sorting Data

## Learning Outcomes

By the end of this notebook, you should be able to:

- select columns from a DataFrame
- filter rows using conditions
- sort data
- count category occurrences
- interpret filtered results

## Introduction

In this notebook, we will learn how to filter and sort data using Pandas.

These operations are conceptually similar to filtering and sorting in Excel, but they are reproducible and automated through code.
```

The introduction should:

* explain WHY the topic matters
* connect to practical analytical workflows
* connect to Excel where appropriate

---

# Environment Setup Section

Every notebook should contain a setup section near the beginning.

Example:

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```

If datasets are loaded:

```python
df = pd.read_csv("../data/example_dataset.csv")
```

Setup sections should:

* remain minimal
* avoid unnecessary imports
* avoid complex configuration

---

# Markdown-to-Code Ratio

The notebooks should contain substantial Markdown explanation.

Recommended balance:

* approximately 40–60% Markdown
* approximately 40–60% code

Large uninterrupted blocks of code should generally be avoided.

Code should be separated by explanatory text.

---

# Code Cell Design Principles

Code cells should:

* demonstrate one concept at a time
* remain short where practical
* produce visible outputs
* avoid unnecessary abstraction

Preferred style:

```python
df.head()
```

Preferred over:

```python
print(df.head())
```

unless printing is explicitly being taught.

Avoid:

* deeply nested expressions
* advanced Python syntax
* excessive chaining
* one-line “clever” solutions

---

# Commenting Style

Code comments should explain reasoning rather than restating syntax.

Good example:

```python
# Filter rows where sales exceed 1000 EUR
high_sales = df[df["sales"] > 1000]
```

Weak example:

```python
# Create variable
high_sales = df[df["sales"] > 1000]
```

Comments should:

* clarify intention
* explain analytical purpose
* support beginners

---

# Instructor Demonstration Sections

These sections should:

* introduce one major idea at a time
* include explanatory Markdown
* include visible outputs
* proceed gradually

Example structure:

```markdown
## Instructor Demonstration

Let us first inspect the structure of the dataset.
```

```python
df.head()
```

```markdown
The output shows the first five rows of the dataset.
This helps us understand:
- available columns
- data types
- possible missing values
```

---

# Guided Practice Sections

Guided practice should:

* closely follow demonstrated examples
* slightly modify demonstrated operations
* reinforce procedural confidence

Example:

```markdown
## Guided Practice

Try filtering rows where the salary is greater than 2000.
```

```python
df[df["salary"] > 2000]
```

Guided practice should avoid introducing major new concepts.

---

# Check Your Understanding Sections

Every notebook should contain low-stakes formative assessment.

Purpose:

* verify understanding
* encourage active thinking
* reduce passive observation

Example:

````markdown
## Check Your Understanding

1. What does the following code return?

```python
df[df["age"] > 30]
````

2. Why are parentheses needed when combining conditions?

3. Which operation is conceptually similar to Excel filtering?

````

These questions should:

- remain short
- emphasize concepts
- include code-reading
- include prediction exercises

Avoid:

- memorization-heavy questions
- advanced debugging tasks

---

# Independent Mini Task Sections

Every notebook should contain at least one short independent task.

Purpose:

- reinforce confidence
- encourage independent action
- transition beyond imitation

Mini tasks should:

- be achievable within 5–8 minutes
- use previously demonstrated concepts
- produce visible results

Example:

```markdown
## Independent Mini Task

Using the dataset:

- filter rows where sales exceed 1000
- sort results by sales descending
- identify the top 5 entries

Write 2–3 sentences describing your observations.
````

Mini tasks should avoid introducing major new ideas.

---

# Common Mistakes Sections

Every notebook should contain:

```markdown
## Common Mistakes
```

Purpose:

* normalize beginner mistakes
* reduce anxiety
* improve debugging confidence

Example:

```markdown
## Common Mistakes

- Forgetting quotation marks around column names
- Using = instead of ==
- Misspelling column names
- Forgetting parentheses in filtering conditions
- Running notebook cells out of order
```

These sections are pedagogically important.

---

# Reflection Sections

Every notebook should contain reflection questions.

Purpose:

* consolidate learning
* encourage metacognition
* connect concepts to workplace usage

Example:

```markdown
## Reflection

1. Which operation felt most intuitive today?
2. Which concept still feels confusing?
3. How does this compare to Excel workflows?
4. Where could you apply this workflow in your work?
```

Reflection questions should:

* encourage self-assessment
* encourage practical thinking
* reinforce analytical reasoning

---

# Optional Bonus Tasks Sections

Bonus tasks should:

* remain optional
* support faster learners
* avoid penalizing core learners

Example:

```markdown
## Optional Bonus Tasks

- Create an additional visualization.
- Export grouped results to Excel.
- Add a custom chart title and annotations.
- Experiment with additional filtering conditions.
```

Bonus sections should be clearly labeled as optional.

---

# Visualization Notebook Guidelines

Visualization notebooks should:

* explain WHEN to use chart types
* explain WHY to use chart types
* emphasize readability
* emphasize interpretation

All visualizations should include:

* title
* axis labels
* readable formatting

Preferred example:

```python
plt.figure(figsize=(8, 5))

sns.barplot(data=df, x="region", y="sales")

plt.title("Total Sales by Region")
plt.xlabel("Region")
plt.ylabel("Sales")

plt.show()
```

Visualization notebooks should also include interpretation.

Example:

```markdown
The chart shows that Riga has the highest sales values among all regions.
This may suggest higher customer concentration or stronger business activity.
```

---

# Data Storytelling Guidelines

Participants should repeatedly practice:

* observation
* interpretation
* explanation
* recommendation

Weak title:

```markdown
Sales by Region
```

Better title:

```markdown
Riga Region Generated the Highest Total Sales
```

Charts should communicate insight, not merely display numbers.

---

# Output Expectations

Most code cells should generate visible output.

Preferred outputs:

* tables
* summaries
* charts
* counts
* descriptive statistics

Avoid notebooks that contain long stretches of code without output.

---

# Notebook Length Guidelines

Recommended notebook size:

* approximately 30–80 cells
* depending on topic complexity

Avoid:

* extremely short notebooks lacking explanation
* excessively long notebooks causing fatigue

The pacing should support beginner learners.

---

# Scope Control

Avoid including advanced topics in standard notebooks:

* object-oriented programming
* advanced functions
* decorators
* APIs
* machine learning
* advanced statistics
* dashboard frameworks
* complex environment management

The primary objective is:

> practical reproducible data analysis workflows for beginners.

---

# Final Notebook Goal

Every notebook should leave participants feeling:

* capable
* confident
* successful
* practically empowered

The notebooks should consistently reinforce:

> Python can be used as a practical, understandable, reproducible analytical tool.
