# Notebook Template

## Purpose

This document defines the standard structure for the course workbooks.

The course uses full-day notebooks rather than many small lesson notebooks. Each main notebook should be a self-contained Google Colab workbook with 5 subchapters.

Primary notebooks:

- `01_day1_titanic_data_analysis.ipynb`
- `02_day2_penguins_visualization_storytelling.ipynb`
- optional `03_bonus_gapminder_visual_analysis.ipynb`

## Workbook-Level Structure

Each main workbook should follow this high-level structure:

```markdown
# Workbook Title

## Learning Outcomes

## How to Use This Workbook

## Setup

## Subchapter 1: ...

## Subchapter 2: ...

## Subchapter 3: ...

## Subchapter 4: ...

## Subchapter 5: ...

## End-of-Day Mini Report

## Common Mistakes and Troubleshooting

## Reflection

## Optional Bonus Tasks
```

The exact subchapter titles should match the dataset and day goal.

## Required Subchapter Pattern

Each subchapter should normally contain:

```markdown
### Goal

### Instructor Demonstration

### Guided Practice

### Check Your Understanding

### Independent Mini Task

### Interpretation
```

This pattern may be adapted when it improves flow, but every subchapter should include explanation, code, visible output, and learner activity.

## Setup Section

Every workbook must include a simple setup section near the beginning.

Use only the libraries needed for that workbook:

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```

Use stable visual defaults when helpful:

```python
sns.set_theme(style="whitegrid")
```

Avoid unnecessary installation cells. Colab already includes the core libraries used in this course.

## Colab-Safe Data Loading

Notebook data loading must work in Google Colab as-is.

Preferred pattern:

```python
from pathlib import Path

local_path = Path("../data/titanic.csv")
remote_url = "https://raw.githubusercontent.com/ValRCS/RTU_Python_Data_Analysis_Visualization_May_2026/main/data/titanic.csv"

if local_path.exists():
    df = pd.read_csv(local_path)
else:
    df = pd.read_csv(remote_url)

df.head()
```

Use the correct dataset variable names:

- Day 1: `titanic` or `df`
- Day 2: `penguins`
- Bonus: `gapminder`

If the final notebooks are intended to be opened directly from GitHub in Colab, replace the placeholder remote URL with the actual raw CSV URL.

## Markdown Style

Markdown should:

- explain why each step matters
- connect to Excel where useful
- prepare learners for the next code cell
- interpret important outputs
- use plain language

Avoid long theory sections. Short explanations followed by visible output are better for beginners.

Good style:

```markdown
Before creating charts, we need to understand what columns are available.
This is similar to checking the header row and data types in Excel.
```

Weak style:

```markdown
Pandas is a high-performance data manipulation library built on top of optimized array structures.
```

## Code Cell Style

Code cells should:

- be short
- do one main thing at a time
- produce visible output when practical
- avoid clever one-line chains
- use descriptive variable names

Prefer:

```python
adult_passengers = titanic[titanic["Age"] >= 18]
adult_passengers.head()
```

Avoid:

```python
titanic[titanic.Age.ge(18)].sort_values("Fare", ascending=False).head(17).style.background_gradient()
```

## Visible Output Requirement

Most code cells should show something:

- table preview
- summary table
- count result
- chart
- missing value report
- written interpretation after output

Avoid long stretches of hidden processing.

## Chart Standards

All core charts should include:

- clear title
- x-axis label
- y-axis label
- readable figure size
- legend when it helps interpretation

Recommended Matplotlib/Seaborn pattern:

```python
plt.figure(figsize=(8, 5))

sns.barplot(data=summary, x="species", y="body_mass_g")

plt.title("Gentoo Penguins Have the Highest Average Body Mass")
plt.xlabel("Species")
plt.ylabel("Average body mass (g)")
plt.show()
```

Chart titles should increasingly move from descriptive to insight-oriented.

Weak:

```text
Body Mass by Species
```

Better:

```text
Gentoo Penguins Have the Highest Average Body Mass
```

## Check Your Understanding

Each subchapter should include 2 to 4 low-stakes questions.

Use questions such as:

- What do you expect this code to output?
- Which column is being filtered?
- Why is this chart type appropriate?
- What pattern do you notice?
- How would this compare to an Excel workflow?

Avoid formal quiz style and memorization-heavy questions.

## Independent Mini Tasks

Each subchapter should include a mini task that takes about 5 to 8 minutes.

Good mini tasks:

- repeat a demonstrated pattern with a different column
- filter a small subset
- create a simple grouped summary
- make one chart and write one observation

Mini tasks should not introduce major new syntax.

## Common Mistakes

Each workbook must include a common mistakes section. Individual subchapters may also include short mistake notes.

Useful examples:

- misspelling column names
- forgetting quotation marks around column names
- using `=` instead of `==`
- forgetting parentheses when combining filters
- running cells out of order
- interpreting missing values as zero
- creating charts before checking data quality

The tone should normalize beginner mistakes.

## Reflection

Each workbook should end with reflection prompts.

Use questions such as:

- Which operation felt most familiar from Excel?
- Which step still feels confusing?
- What part of this workflow could help in your work?
- What would you want to practice again?
- What did the data suggest, and what can it not prove?

## End-of-Day Mini Report

Each main workbook should end with a small reproducible report.

Day 1 report should include:

- one cleaned or prepared Titanic dataset decision
- two or more summary tables
- optional simple chart
- 3 to 5 short written conclusions

Day 2 report should include:

- 2 to 3 readable Penguins charts
- short interpretation after each chart
- 3 to 5 written findings
- at least one caution about overinterpreting charts

## Optional Bonus Tasks

Bonus tasks should be clearly optional and should not be required for the main learner path.

Good bonus tasks:

- customize chart colors
- save a chart
- create one extra grouped summary
- compare another pair of variables
- try a Gapminder line chart

Avoid bonus tasks that require advanced programming.

## Notebook Length

For each main day workbook, aim for approximately:

- 5 subchapters
- 60 to 120 cells total
- 40 to 60 percent Markdown
- 40 to 60 percent code

The workbook should be long enough to support instructor-led teaching, but not so dense that learners cannot follow while coding along.

## Final Quality Checklist

Before considering a workbook ready:

- It runs top-to-bottom in Google Colab.
- It has no local-only data dependency.
- It uses beginner-readable code.
- It contains visible outputs.
- It includes guided practice and mini tasks.
- It includes checks for understanding.
- It includes common mistakes.
- It includes reflection.
- It ends with a small analytical synthesis.
- Charts have titles and labels.
- The notebook avoids advanced software engineering topics.
