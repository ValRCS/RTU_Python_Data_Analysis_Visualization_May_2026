# AGENTS.md

## Mission

Create beginner-friendly Google Colab workbooks for a two-day, 10 academic-hour course on Python data analysis and visualization.

The course is for adult professionals with little or no programming experience. Many learners may have Excel experience. The materials should feel like practical analytical workflows, not computer science exercises.

## Current Deliverables

Build toward these notebooks:

- `notebooks/01_day1_titanic_data_analysis.ipynb`
- `notebooks/02_day2_penguins_visualization_storytelling.ipynb`
- Optional: `notebooks/03_bonus_gapminder_visual_analysis.ipynb`

Each main day notebook must be a self-contained full-day workbook with 5 subchapters. The bonus notebook may be shorter, but should still be runnable and self-contained.

## Datasets

Use the datasets already stored in `data/`:

- `data/titanic.csv` for Day 1
- `data/penguins.csv` for Day 2
- `data/gapminder.csv` for the optional bonus notebook

Notebook data-loading cells must work in Google Colab as-is. Prefer a simple loader that tries the local repository path first and falls back to a raw GitHub URL or another stable public URL documented in the notebook.

## Core Libraries

Use these as the standard course libraries:

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```

Optional enrichment may use:

```python
import numpy as np
import plotly.express as px
```

Do not make optional enrichment a requirement for the main workflow.

## Teaching Style

Prioritize:

- short, readable code cells
- explanatory Markdown between code cells
- visible outputs after most code cells
- Excel comparisons where useful
- practical interpretation of results
- confidence-building for beginners

Avoid:

- object-oriented programming
- decorators
- APIs
- machine learning
- SQL
- complex package management
- advanced statistics
- software engineering topics

Participants are learning reproducible analysis, not software development.

## Required Workbook Pattern

Each main workbook should include:

- clear learning outcomes
- 5 named subchapters
- instructor demonstration
- guided practice
- check-your-understanding questions
- independent mini tasks
- common mistakes
- reflection prompts
- a short end-of-day synthesis or mini report

Each subchapter should normally follow this rhythm:

1. Explain the goal in plain language.
2. Demonstrate the operation.
3. Let learners modify or repeat the pattern.
4. Ask a low-stakes check question.
5. End with a small visible result or interpretation.

## Colab Requirements

All notebooks must:

- run top-to-bottom with "Run all"
- avoid local-only paths
- avoid unnecessary installation cells
- use stable data-loading logic
- contain visible tables, summaries, or charts
- include enough Markdown for learners who revisit the notebook later

## Documentation

Keep this file concise. Put detailed guidance in:

- `docs/PEDAGOGY.md`
- `docs/COURSE_STRUCTURE.md`
- `docs/NOTEBOOK_TEMPLATE.md`
- `docs/DATASETS.md`

If guidance conflicts, follow this priority:

1. `AGENTS.md`
2. `docs/COURSE_STRUCTURE.md`
3. `docs/NOTEBOOK_TEMPLATE.md`
4. `docs/PEDAGOGY.md`
5. dataset-specific notes

## End Goal

By the end of the course, learners should be able to load tabular data, inspect it, clean basic issues, filter and summarize rows, create readable charts, and write short analytical conclusions in a reproducible notebook.
