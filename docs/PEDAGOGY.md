# Pedagogy

## Teaching Philosophy

This course teaches reproducible data analysis, not software development.

Learners should leave with the feeling that Python notebooks can help them inspect, clean, summarize, visualize, and explain tabular data. They do not need to feel like programmers.

Prioritize:

- practical usefulness
- visible progress
- short code cells
- repeated patterns
- plain-language explanations
- connections to Excel workflows
- low-stakes practice

Avoid:

- abstract programming theory
- unnecessary jargon
- long unexplained code blocks
- clever syntax
- advanced statistics
- software engineering topics

## Audience

The primary audience is adult professionals with mixed technical backgrounds. Some may use Excel regularly. Some may be anxious about programming.

Assume:

- little or no prior Python experience
- possible Excel experience
- limited confidence with code
- preference for practical examples
- need for instructor pacing and repetition

Do not assume:

- comfort with command lines
- software development experience
- knowledge of statistics beyond basic descriptive ideas
- patience for abstract exercises without workplace relevance

## Excel-to-Python Anchors

Use Excel comparisons to reduce cognitive load.

| Excel concept | Python / Pandas concept |
| --- | --- |
| Worksheet or table | DataFrame |
| Column | Series |
| Filter | Boolean indexing |
| Sort | `sort_values()` |
| Pivot Table | `groupby()` or `pivot_table()` |
| Formula | Python expression |
| Chart | Matplotlib or Seaborn visualization |
| Manual repeated steps | Reproducible notebook workflow |

The message should be:

> Python can automate and document familiar analysis workflows.

Do not frame Excel as obsolete or inferior.

## Cognitive Load

The course is short: 10 academic hours across two days.

Learners should work through two main full-day notebooks:

- Day 1: Titanic data analysis
- Day 2: Penguins visualization and storytelling

Each day workbook has 5 subchapters. Each subchapter should introduce a small number of new ideas and give learners time to practice.

Avoid combining too many new concepts at once. For example, do not introduce filtering, custom functions, complex plotting, and statistical interpretation in the same task.

Better pattern:

1. Introduce one operation.
2. Show one visible output.
3. Interpret that output.
4. Let learners repeat the pattern.
5. Add one small variation.

## Instructor Rhythm

A good academic-hour rhythm is:

| Segment | Approximate time |
| --- | --- |
| Short introduction or recap | 5 minutes |
| Instructor demonstration | 10 to 15 minutes |
| Guided practice | 10 to 15 minutes |
| Check your understanding | 3 to 5 minutes |
| Independent mini task | 5 to 8 minutes |
| Reflection or interpretation | 2 to 4 minutes |

This rhythm should guide the notebooks, but it does not need to be mechanical. Use the flow that best helps learners.

## Instructor Demonstrations

Instructor demonstrations should:

- move slowly
- explain the purpose before the syntax
- show output immediately
- pause after important cells
- occasionally normalize common mistakes
- connect code to analytical reasoning

Beginners often cannot listen, read code, type, and interpret output at the same time. Demonstrations should leave space for thinking.

## Guided Practice

Guided practice should closely follow the demonstrated pattern.

Example:

After demonstrating:

```python
titanic[titanic["Age"] >= 18]
```

guided practice might ask learners to filter:

```python
titanic[titanic["Fare"] > 50]
```

Do not radically change the dataset, syntax, and analytical question all at once.

## Checks for Understanding

Checks should be low-stakes and short.

Good question types:

- Predict the output before running the code.
- Identify which column is being used.
- Explain what the grouped result means.
- Choose which chart type fits a question.
- Describe one pattern in a chart.

Avoid:

- formal exam tone
- memorization-heavy syntax questions
- long debugging tasks
- questions requiring concepts not yet taught

## Independent Mini Tasks

Mini tasks should take about 5 to 8 minutes.

Good mini tasks:

- filter a different subset
- create a count table
- summarize one column by one category
- make one chart
- write one or two observations

Mini tasks should produce visible output. They should reinforce recent concepts rather than introduce major new ones.

## Common Mistakes

Common mistakes sections are pedagogically important. They normalize errors and reduce anxiety.

Useful examples:

- forgetting quotation marks around column names
- misspelling column names
- using `=` instead of `==`
- running cells out of order
- treating missing values as zero
- forgetting parentheses when combining filters
- creating a chart before checking data quality

The tone should be practical:

> This error is common. Here is how to notice and fix it.

## Visualization Pedagogy

Visualization should be taught as communication, not decoration.

Learners should understand:

- when to use a chart type
- why a chart type fits a question
- how to make charts readable
- how to interpret a chart without overclaiming

Core chart types:

- bar chart
- histogram
- box plot
- scatter plot
- line chart for the bonus Gapminder notebook

Every core chart should include a title, axis labels, readable sizing, and interpretation.

## Data Storytelling

Data storytelling means connecting output to meaning.

Encourage learners to write:

- observation: what the table or chart shows
- interpretation: what that might mean
- caution: what the data cannot prove
- possible next question

Weak title:

```text
Body Mass by Species
```

Better title:

```text
Gentoo Penguins Have the Highest Average Body Mass
```

## Emotional Design

The course should build confidence.

Useful signals:

- "This is similar to Excel filtering."
- "This mistake is common."
- "Run the cell and inspect the output."
- "We are documenting the analysis so it can be repeated."

Avoid signals that make the course feel like a programming gatekeeping exercise.

## Scope Control

Do not include these in the core path:

- classes
- decorators
- recursion
- APIs
- SQL
- machine learning
- dashboards
- command-line workflows
- complex environment management
- advanced statistical modeling

Optional bonus tasks may extend the material, but they should never be required for core success.

## Success Criteria

By the end of the two main workbooks, learners should be able to:

1. Run a Colab notebook.
2. Load a CSV dataset.
3. Inspect rows, columns, data types, and missing values.
4. Filter and sort data.
5. Clean basic missing values.
6. Group and summarize data.
7. Create readable charts.
8. Interpret outputs in plain language.
9. Write a short reproducible analysis.

The desired final feeling is:

> I can realistically use Python notebooks for practical data analysis.
