# COURSE_STRUCTURE.md

# Course Structure — Python Data Analysis and Visualization

This document describes the overall structure, sequencing, and instructional progression of the Python Data Analysis and Visualization course materials.

The Python-specific portion of the course consists of:

* 10 academic hours
* approximately 40–45 minutes each
* delivered across two consecutive days

The course is intended for:

* adult professionals
* beginner programmers
* participants transitioning from Excel workflows
* learners focused on practical analytical skills

---

# Overall Course Objectives

By the end of the course, participants should be able to:

1. Work in Jupyter Notebook or Google Colab environments.
2. Load and inspect tabular datasets.
3. Perform basic data cleaning and transformation.
4. Calculate descriptive statistics.
5. Filter, sort, group, and summarize data.
6. Create readable visualizations.
7. Interpret analytical results.
8. Produce a small reproducible notebook-based analytical report.

---

# Overall Pedagogical Progression

The course progression intentionally follows a practical analytical workflow:

```text
Environment Setup
    ↓
Loading Data
    ↓
Understanding Data
    ↓
Cleaning Data
    ↓
Transforming Data
    ↓
Summarizing Data
    ↓
Visualizing Data
    ↓
Interpreting Data
    ↓
Communicating Findings
```

This progression mirrors real-world analytical workflows.

---

# Day 1 Overview

Day 1 focuses primarily on:

* Python basics
* Jupyter/Colab workflow
* Pandas fundamentals
* Data cleaning
* Data summarization

The emphasis is:

* comfort with notebooks
* understanding DataFrames
* confidence with basic analytical operations

---

# Day 2 Overview

Day 2 focuses primarily on:

* data visualization
* interpretation
* communication
* data storytelling
* integrating workflows into a mini-project

The emphasis is:

* visual communication
* analytical reasoning
* reproducibility
* practical reporting

---

# Academic Hour Structure

Each academic hour should approximately follow:

| Segment                  | Approximate Time |
| ------------------------ | ---------------- |
| Introduction & recap     | 5 min            |
| Instructor demonstration | 10–15 min        |
| Guided practice          | 10–15 min        |
| Assessment questions     | 3–5 min          |
| Independent mini task    | 5–8 min          |
| Reflection               | 2–4 min          |

This structure should remain consistent across notebooks.

---

# Notebook Sequence

---

# Notebook 01

# Introduction to Jupyter and Python

## Main Goals

Participants should learn:

* how notebooks work
* how to run code cells
* how to edit cells
* how variables work
* how basic Python expressions work

## Topics

* Jupyter Notebook / Google Colab interface
* code cells vs Markdown cells
* running cells
* variables
* strings
* numbers
* simple arithmetic
* printing output

## Typical Outputs

* simple calculations
* variable assignments
* explanatory Markdown text

## Learning Emphasis

Reduce fear of programming and establish confidence early.

---

# Notebook 02

# Loading and Understanding Data

## Main Goals

Participants should understand:

* what a DataFrame is
* how to load CSV/Excel data
* how to inspect datasets

## Topics

* importing Pandas
* read_csv()
* read_excel()
* head()
* info()
* describe()
* rows and columns
* data types

## Typical Outputs

* loaded datasets
* dataset summaries
* identified column types

## Learning Emphasis

Connect DataFrames to Excel tables.

---

# Notebook 03

# Filtering and Sorting Data

## Main Goals

Participants should learn:

* selecting columns
* filtering rows
* combining conditions
* sorting values
* counting categories

## Topics

* boolean indexing
* filtering conditions
* sort_values()
* value_counts()

## Typical Outputs

* filtered tables
* sorted summaries
* category counts

## Learning Emphasis

Relate filtering directly to Excel filtering workflows.

---

# Notebook 04

# Data Cleaning and Missing Values

## Main Goals

Participants should understand:

* real-world data is messy
* missing values require handling
* text inconsistencies matter
* data types matter

## Topics

* isna()
* dropna()
* fillna()
* duplicated()
* string cleanup
* type conversion
* date conversion

## Typical Outputs

* cleaned datasets
* corrected data types
* normalized text columns

## Learning Emphasis

Show that data cleaning is a major part of analytical work.

---

# Notebook 05

# Statistics and Grouping

## Main Goals

Participants should learn:

* descriptive statistics
* grouped summaries
* pivot-style analysis

## Topics

* mean()
* median()
* sum()
* count()
* groupby()
* agg()
* pivot_table()

## Typical Outputs

* grouped summaries
* aggregated statistics
* pivot-style tables

## Learning Emphasis

Connect grouped analysis to Excel pivot tables.

---

# Notebook 06

# Introduction to Visualization

## Main Goals

Participants should understand:

* why visualization matters
* which chart types fit which analytical tasks

## Topics

* line charts
* bar charts
* scatter plots
* histograms
* box plots
* chart readability
* chart selection

## Typical Outputs

* first simple charts
* comparison of chart types

## Learning Emphasis

Visualization is communication, not decoration.

---

# Notebook 07

# Matplotlib Basics

## Main Goals

Participants should learn:

* creating charts with Matplotlib
* adding titles and labels
* improving readability

## Topics

* plt.plot()
* plt.bar()
* plt.scatter()
* titles
* labels
* legends
* figure size
* grids

## Typical Outputs

* formatted charts
* readable visualizations

## Learning Emphasis

Readable formatting is part of analysis quality.

---

# Notebook 08

# Seaborn Visualization

## Main Goals

Participants should learn:

* statistical visualizations
* easier high-level plotting
* identifying distributions and outliers

## Topics

* sns.barplot()
* sns.histplot()
* sns.boxplot()
* sns.scatterplot()
* hue=
* themes

## Typical Outputs

* cleaner statistical charts
* grouped visualizations

## Learning Emphasis

Visualizations reveal patterns not obvious in tables.

---

# Notebook 09

# Data Storytelling and Interpretation

## Main Goals

Participants should learn:

* charts alone are not analysis
* analytical communication matters
* interpretation is essential

## Topics

* chart interpretation
* identifying patterns
* identifying outliers
* writing analytical conclusions
* communicating insights

## Typical Outputs

* short written interpretations
* annotated charts
* mini analytical narratives

## Learning Emphasis

Analysis requires interpretation and explanation.

---

# Notebook 10

# Mini Project

## Main Goals

Participants should integrate all previous skills into a single workflow.

## Required Workflow

Participants should:

1. Load data.
2. Inspect data.
3. Clean data.
4. Filter and summarize data.
5. Create visualizations.
6. Interpret findings.
7. Produce a small notebook report.

## Expected Deliverable

A reproducible notebook containing:

* code
* tables
* visualizations
* Markdown explanations
* analytical conclusions

## Learning Emphasis

The notebook should resemble a practical analytical report.

---

# Recommended Dataset Strategy

The course should preferably use:

* one main dataset across multiple notebooks

This reduces cognitive overload because participants do not repeatedly learn new domain contexts.

Good dataset characteristics:

* realistic
* medium-sized
* understandable
* slightly imperfect

Recommended themes:

* sales
* surveys
* education
* libraries
* public sector
* transport
* employee records
* budgets

Avoid:

* cryptic datasets
* highly scientific datasets
* advanced statistical datasets

---

# Bonus Sections for Faster Learners

Optional enrichment sections may include:

* pairplot()
* heatmaps
* exporting data
* saving charts
* Plotly examples
* additional pivot tables
* date extraction
* advanced filtering

Bonus sections should always remain optional.

Core learners should never feel punished for not completing bonus material.

---

# Scope Control

The course intentionally excludes:

* advanced Python programming
* object-oriented programming
* machine learning
* dashboard frameworks
* APIs
* SQL
* software engineering architecture
* advanced statistics

The focus is:

> practical analytical workflows for beginners.

---

# Final Desired Outcome

By the end of the course, participants should feel:

> “I can realistically use Python notebooks for practical data analysis tasks.”

The course should maximize:

* confidence
* practical competence
* reproducibility
* analytical thinking

rather than programming sophistication.
