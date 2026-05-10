# Course Structure

## Course Format

This course is a two-day, 10 academic-hour introduction to Python data analysis and visualization.

The course deliverables are full-day Google Colab workbooks:

- `notebooks/01_day1_titanic_data_analysis.ipynb`
- `notebooks/02_day2_penguins_visualization_storytelling.ipynb`
- Optional: `notebooks/03_bonus_gapminder_visual_analysis.ipynb`

Each main workbook contains 5 subchapters. Each subchapter is designed for roughly one academic hour and should include instructor demonstration, guided practice, a short understanding check, a mini task, and interpretation.

## Audience

The primary audience is adult professionals who are new to programming or have limited programming confidence. Many learners may know Excel. The course should use that prior experience as an anchor.

The course is not a software development course. It is a practical course in reproducible data analysis.

## Overall Learning Progression

The course follows a practical analytical workflow:

```text
Open a notebook
Load data
Inspect rows and columns
Clean basic issues
Filter and summarize
Create charts
Interpret findings
Write short conclusions
```

Day 1 emphasizes tabular analysis with Pandas. Day 2 emphasizes visualization, interpretation, and storytelling.

## Day 1 Workbook: Titanic Data Analysis

Dataset: `data/titanic.csv`

Main purpose: help learners become comfortable with notebooks, Pandas, inspection, filtering, missing values, grouping, and short analytical conclusions.

### Day 1 Subchapter 1: Colab, Notebooks, and Loading Data

Learners should be able to:

- run Markdown and code cells
- understand that a notebook is a reproducible analysis document
- import Pandas
- load the Titanic CSV
- view the first rows

Core operations:

```python
import pandas as pd
df = pd.read_csv(...)
df.head()
```

Excel connection: a DataFrame is similar to a worksheet or table.

Visible outputs: first rows, row and column count.

### Day 1 Subchapter 2: Understanding Rows, Columns, and Data Types

Learners should be able to:

- inspect column names
- identify row and column counts
- use `info()` and `describe()`
- distinguish numeric and categorical columns
- notice missing values

Core operations:

```python
df.shape
df.columns
df.info()
df.describe()
df.isna().sum()
```

Excel connection: checking column types and blanks before analysis.

Visible outputs: column list, data type summary, missing value counts.

### Day 1 Subchapter 3: Selecting, Filtering, and Sorting

Learners should be able to:

- select one or more columns
- filter rows using simple conditions
- combine conditions carefully
- sort rows
- count categories

Core operations:

```python
df["Age"]
df[["Name", "Age", "Sex"]]
df[df["Age"] >= 18]
df.sort_values("Fare", ascending=False)
df["Pclass"].value_counts()
```

Excel connection: filtering and sorting table rows.

Visible outputs: filtered tables, sorted tables, category counts.

### Day 1 Subchapter 4: Cleaning Missing and Inconvenient Data

Learners should be able to:

- identify missing values
- decide whether to fill, ignore, or exclude missing values
- create simple cleaned columns when useful
- understand that cleaning choices affect analysis

Core operations:

```python
df.isna().sum()
df["Age"].fillna(df["Age"].median())
df.dropna(subset=["Embarked"])
```

Recommended cleaning focus:

- `Age` has many missing values.
- `Cabin` is mostly missing and should not be overused.
- `Embarked` has a small number of missing values.

Excel connection: replacing blanks, filtering blanks, and documenting decisions.

Visible outputs: before/after missing value summaries.

### Day 1 Subchapter 5: Grouping, Summarizing, and Mini Report

Learners should be able to:

- calculate basic descriptive statistics
- group by category
- compare survival rates by group
- write short analytical conclusions

Core operations:

```python
df["Survived"].mean()
df.groupby("Sex")["Survived"].mean()
df.groupby("Pclass")["Fare"].mean()
pd.pivot_table(...)
```

Excel connection: Pivot Tables and summarized reports.

Visible outputs: grouped summaries and a short final Markdown interpretation.

Expected end-of-day output: a small reproducible Titanic analysis containing code, tables, and 3 to 5 short conclusions.

## Day 2 Workbook: Penguins Visualization and Storytelling

Dataset: `data/penguins.csv`

Main purpose: help learners create readable visualizations, choose appropriate chart types, compare groups, interpret patterns, and turn charts into short analytical stories.

### Day 2 Subchapter 1: Loading and Re-Inspecting a New Dataset

Learners should be able to:

- load a second dataset independently
- inspect rows, columns, and missing values
- reuse Day 1 inspection patterns
- understand what each measurement means

Core operations:

```python
penguins.head()
penguins.info()
penguins.describe()
penguins.isna().sum()
```

Excel connection: opening a new worksheet and checking fields before charting.

Visible outputs: first rows, data types, missing value counts.

### Day 2 Subchapter 2: Distributions and Category Counts

Learners should be able to:

- count categories
- create bar charts for categories
- create histograms for numeric distributions
- explain what a distribution shows

Core chart types:

- bar chart
- histogram

Recommended variables:

- `species`
- `island`
- `body_mass_g`
- `flipper_length_mm`

Visible outputs: category count table, bar chart, histogram.

### Day 2 Subchapter 3: Comparing Groups

Learners should be able to:

- compare measurements by species
- use grouped summaries
- create box plots
- identify spread, center, and outliers in plain language

Core chart types:

- box plot
- grouped bar chart

Recommended variables:

- `species`
- `body_mass_g`
- `bill_length_mm`
- `flipper_length_mm`

Visible outputs: grouped summary table and comparison charts.

### Day 2 Subchapter 4: Relationships Between Measurements

Learners should be able to:

- create scatterplots
- use color to show groups
- describe relationships without overclaiming causality
- connect chart patterns to interpretation

Core chart type:

- scatter plot

Recommended variables:

- `bill_length_mm`
- `bill_depth_mm`
- `flipper_length_mm`
- `body_mass_g`
- `species`

Visible outputs: scatterplots with readable titles and labels.

### Day 2 Subchapter 5: Visual Storytelling Mini Project

Learners should be able to:

- choose useful charts
- title charts with insights
- write observations and interpretations
- assemble a short reproducible visual report

Expected end-of-day output: a short Penguins visual story with 2 to 3 charts and 3 to 5 written findings.

## Bonus Workbook: Gapminder Visual Analysis

Dataset: `data/gapminder.csv`

This optional workbook is useful for faster groups or for extending Day 2. It should focus on time trends and public-data storytelling.

Suggested subchapters:

1. Load and inspect Gapminder data.
2. Filter by country, continent, and year.
3. Create line charts for life expectancy over time.
4. Compare continents using summaries and charts.
5. Write a short public-data story with caveats.

Recommended chart types:

- line chart
- bar chart
- scatter plot

Important caveat: this is a historical teaching excerpt ending in 2007, not a current source of socioeconomic indicators.

## Standard Subchapter Rhythm

Each subchapter should usually follow this pattern:

1. Short introduction: why this matters.
2. Instructor demonstration: one main idea at a time.
3. Guided practice: learners repeat or slightly modify the pattern.
4. Check your understanding: prediction or interpretation question.
5. Independent mini task: 5 to 8 minutes.
6. Common mistake or troubleshooting note.
7. Short reflection or interpretation.

This rhythm is more important than perfectly equal section lengths.

## Assessment Approach

Assessment should be low-stakes and practical.

Use:

- code-reading questions
- output prediction questions
- short interpretation prompts
- mini tasks that produce visible tables or charts

Avoid:

- formal exams
- syntax memorization
- long coding challenges
- tasks that require concepts not yet demonstrated

## Scope Boundaries

Do not include these in the core notebooks:

- object-oriented programming
- custom classes
- decorators
- APIs
- machine learning
- SQL
- dashboards
- advanced statistics
- complex environment setup

Optional bonus sections may mention extensions, but the core learner path must remain beginner-friendly.

## Success Criteria

By the end of the two main workbooks, learners should be able to:

1. Open and run a Colab notebook.
2. Load a CSV dataset.
3. Inspect rows, columns, data types, and missing values.
4. Filter, sort, and select data.
5. Clean basic missing values.
6. Group and summarize data.
7. Create readable charts.
8. Interpret tables and charts.
9. Write short analytical conclusions.
10. Re-run a notebook as a reproducible analysis.
