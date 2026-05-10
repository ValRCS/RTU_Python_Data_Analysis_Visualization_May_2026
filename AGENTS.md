# AGENTS.md

# Python Data Analysis and Visualization Course

This repository contains teaching materials for a short intensive course on:

* Python for data analysis
* Pandas
* Data cleaning
* Data visualization with Matplotlib and Seaborn
* Basic data storytelling
* Jupyter Notebook / Google Colab workflows

---

# Audience

Primary audience:

* Adult professionals
* Little or no programming experience
* Possible Excel experience
* Mixed technical backgrounds

The notebooks should assume:

* beginner-level Python knowledge
* possible anxiety about programming
* preference for practical examples over theory

The notebooks should NOT resemble traditional computer science programming exercises.

The notebooks SHOULD resemble:

* guided analytical workflows
* reproducible Excel-like analysis pipelines
* practical business/public-sector data analysis examples

---

# Primary Teaching Philosophy

Participants are NOT becoming software developers.

Participants ARE learning:

* reproducible data analysis
* practical data cleaning
* basic analytical thinking
* visual communication of data
* replacing repetitive Excel workflows

Whenever possible, connect concepts to Excel equivalents.

Examples:

| Excel Concept   | Pandas Equivalent                  |
| --------------- | ---------------------------------- |
| Worksheet/Table | DataFrame                          |
| Column          | Series                             |
| Filter          | Boolean indexing                   |
| Pivot Table     | groupby() / pivot_table()          |
| Formula         | Python expression                  |
| Chart           | Matplotlib / Seaborn visualization |

---

# Technical Environment

Primary target environment:

* Google Colab

Secondary compatible environments:

* Jupyter Notebook
* VS Code Jupyter extension
* JupyterLab

All notebooks must:

* run successfully using "Run All"
* avoid complex setup
* avoid unnecessary package installation
* contain explanatory Markdown between code cells
* contain visible outputs
* support beginner readability

---

# Core Libraries

Primary libraries:

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```

Optional bonus sections may additionally use:

```python
import numpy as np
import plotly.express as px
```

Plotly and NumPy are optional enrichment only and should not be core dependencies.

---

# Repository Structure

Expected repository structure:

```text
/
├── AGENTS.md
├── README.md
├── requirements.txt
├── data/
├── notebooks/
├── images/
├── exports/
└── docs/
    ├── PEDAGOGY.md
    ├── COURSE_STRUCTURE.md
    ├── NOTEBOOK_TEMPLATE.md
    └── DATASETS.md
```

---

# Notebook Naming Convention

```text
01_intro_to_jupyter_and_python.ipynb
02_loading_and_understanding_data.ipynb
03_filtering_and_sorting.ipynb
04_data_cleaning.ipynb
05_statistics_and_grouping.ipynb
06_intro_to_visualization.ipynb
07_matplotlib_basics.ipynb
08_seaborn_visualization.ipynb
09_data_storytelling.ipynb
10_mini_project.ipynb
```

---

# Required Notebook Structure

Every notebook should consistently use the following structure:

```markdown
# Lesson Title

## Learning Outcomes

## Introduction

## Instructor Demonstration

## Guided Practice

## Check Your Understanding

## Independent Mini Task

## Common Mistakes

## Reflection

## Optional Bonus Tasks
```

Consistency is important for beginner adult learners.

---

# Pedagogical Requirements

Every notebook MUST contain:

* explanatory Markdown
* runnable examples
* visible outputs
* assessment questions
* independent mini tasks
* reflection questions
* common mistakes sections

The notebooks should:

* avoid unexplained syntax
* avoid large unexplained code blocks
* avoid excessive abstraction
* prioritize confidence-building
* prioritize practical usefulness

---

# Assessment Design

## Check Your Understanding

These sections should:

* be low-stakes
* focus on conceptual understanding
* include code-reading exercises
* include prediction questions

Avoid:

* formal exams
* memorization-heavy questions
* long coding tasks

Example:

```python
x = 10
y = 5
x + y * 2
```

Question:

"Predict the output before running the code."

---

# Independent Mini Tasks

Mini tasks should:

* be practical
* be short
* reinforce recently demonstrated concepts
* produce visible results
* be achievable within 5–8 minutes

Mini tasks should NOT:

* introduce major new concepts
* require advanced debugging
* overwhelm beginners

---

# Reflection Sections

Reflection questions should encourage:

* conceptual understanding
* workplace application
* comparison with Excel workflows
* self-evaluation

Examples:

* Which concept felt most intuitive today?
* Which concept still feels confusing?
* Where could this workflow help in your work?

---

# Common Mistakes Sections

Every notebook should contain:

```markdown
## Common Mistakes
```

Examples:

* Forgetting quotation marks
* Using = instead of ==
* Misspelling column names
* Running cells out of order
* Forgetting parentheses in filtering conditions

These sections are pedagogically important and help normalize beginner errors.

---

# Dataset Requirements

Datasets should be:

* realistic
* workplace-relevant
* medium-sized
* easy to understand
* somewhat imperfect

Recommended dataset characteristics:

* 200–2000 rows
* 6–12 columns
* at least 2 numeric columns
* at least 2 categorical columns
* at least 1 date column
* several missing values
* minor inconsistencies for cleaning exercises

Preferred dataset themes:

* sales
* surveys
* employees
* public sector data
* libraries
* budgets
* customers
* education
* transport

Avoid:

* highly scientific datasets
* cryptic column names
* excessively large datasets
* advanced statistical datasets

---

# Visualization Philosophy

The visualization section should emphasize:

* readability
* interpretation
* communication
* avoiding misleading charts
* selecting appropriate chart types

Core chart types:

* line chart
* bar chart
* scatter plot
* histogram
* box plot

The notebooks should explain:

* WHEN to use each chart
* WHY to use each chart
* HOW to interpret each chart

All charts should include:

* titles
* axis labels
* legends where appropriate
* readable formatting

---

# Data Storytelling

Participants should learn that:

* charts alone are not analysis
* interpretation matters
* visualizations should communicate insight

Weak title example:

```markdown
Sales by Region
```

Better title example:

```markdown
Riga Region Generated the Highest Total Sales
```

Encourage:

* observation
* interpretation
* explanation
* recommendation

---

# Scope Control

DO NOT include advanced software engineering topics in core materials.

Avoid:

* object-oriented programming
* classes
* decorators
* APIs
* machine learning
* deep statistics
* dashboards
* SQL integration
* complex package management
* virtual environment complexity

The goal is:

A complete beginner should be able to:

1. Load and inspect tabular datasets.
2. Perform basic cleaning and transformation.
3. Compute descriptive statistics.
4. Group and summarize data.
5. Create readable visualizations.
6. Interpret charts and findings.
7. Produce a small reproducible analytical notebook report.

within 10 academic hours.

---

# Final Course Goal

The final mini-project notebook should combine:

* code
* tables
* visualizations
* Markdown explanations
* short analytical conclusions

into a single reproducible workflow suitable for beginner professional learners.
