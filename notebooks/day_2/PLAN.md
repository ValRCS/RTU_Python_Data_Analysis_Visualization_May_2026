# Day 2 Notebook Plan: Penguins Visualization and Storytelling

Planned notebook path:

```text
notebooks/day_2/02_day2_penguins_visualization_storytelling.ipynb
```

Estimated duration: 3 to 5 academic hours.

This workbook should be shorter and more focused than Day 1 because the optional Gapminder notebook can extend the visualization practice. The core Day 2 outcome is that learners can choose suitable chart types, create readable charts with Matplotlib, Seaborn, and Plotly, and write short visual interpretations.

## Dataset

Use:

```text
data/penguins.csv
```

The Penguins dataset contains 344 observations of penguins from three species: Adelie, Chinstrap, and Gentoo. It includes island, body measurements, sex, and year.

Columns:

- `species`: penguin species
- `island`: island where the penguin was observed
- `bill_length_mm`: bill length in millimeters
- `bill_depth_mm`: bill depth in millimeters
- `flipper_length_mm`: flipper length in millimeters
- `body_mass_g`: body mass in grams
- `sex`: penguin sex
- `year`: observation year

Plain-language measurement explanation:

- Bill length and bill depth describe the size and shape of the penguin's beak.
- Flipper length is the length of the penguin's flipper.
- Body mass is the penguin's weight in grams.
- Species and island are groups that can be compared in charts.

Dataset cautions:

- Some rows contain missing values marked as `NA`.
- Missing values should be handled before charts that use body measurements.
- Charts can show patterns and differences, but they should not be used to claim causality.

## Colab Setup Requirements

The notebook must run top-to-bottom in Google Colab with no manual file upload and no installation cells.

Recommended setup cell:

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
import plotly.express as px
import plotly.io as pio

sns.set_theme(style="whitegrid")
pio.renderers.default = "colab"
```

Recommended data-loading cell:

```python
from pathlib import Path

local_path = Path("../../data/penguins.csv")
remote_url = "https://raw.githubusercontent.com/ValRCS/RTU_Python_Data_Analysis_Visualization_May_2026/main/data/penguins.csv"

if local_path.exists():
    penguins = pd.read_csv(local_path, na_values="NA")
else:
    penguins = pd.read_csv(remote_url, na_values="NA")

penguins.head()
```

Use `penguins` as the DataFrame name throughout the notebook.

The local path goes up two folders because the planned notebook is inside `notebooks/day_2/`.

## Learning Outcomes

By the end of the notebook, learners should be able to:

- explain what the Penguins dataset contains
- inspect a dataset before charting
- choose a chart type based on the question and column types
- create basic Matplotlib charts
- create clearer statistical charts with Seaborn
- create simple interactive charts with Plotly
- improve chart titles, labels, figure size, and legends
- interpret visual patterns in plain language
- create a short visual mini report with 2 to 3 charts

## Workbook Structure

Use 5 compact subchapters. Each subchapter should contain instructor demonstration, guided practice, check-your-understanding questions, an independent mini task, common mistakes, and interpretation.

## Subchapter 1: Meet the Penguins Dataset

Estimated time: 35 to 45 minutes.

Goal: load the dataset, understand rows and columns, and identify chart-ready variables.

Core code examples:

```python
penguins.head()
penguins.shape
penguins.info()
penguins.describe()
penguins.isna().sum()
```

Recommended Markdown:

- Explain that this dataset is useful for visualization because it has both categories and measurements.
- Compare `species` and `island` to Excel category columns.
- Compare `body_mass_g` and `flipper_length_mm` to numeric measurement columns.
- Explain that missing values are common in real data and should be checked before charting.

Visible outputs:

- first rows
- row and column count
- data type summary
- missing value counts

Guided practice:

- Ask learners to inspect `penguins.columns`.
- Ask them to identify two categorical columns and two numeric columns.

Check-your-understanding questions:

- Which columns are categories?
- Which columns are measurements?
- Why should we check missing values before making charts?

Mini task:

- Display the first 10 rows and write one sentence describing what each row represents.

## Subchapter 2: Choosing the Right Chart Type

Estimated time: 35 to 50 minutes.

Goal: give learners a practical chart-choice framework before writing more chart code.

Include a simple chart-choice table:

| Analytical question | Column types | Good chart choices | Penguin example |
| --- | --- | --- | --- |
| How many in each group? | Category | Bar chart | Count penguins by `species` |
| How are values distributed? | One numeric column | Histogram | Distribution of `body_mass_g` |
| How do groups compare? | Category + numeric | Box plot or grouped bar chart | Body mass by `species` |
| Are two measurements related? | Two numeric columns | Scatter plot | Flipper length vs body mass |
| How can we explore interactively? | Any simple comparison | Plotly chart | Interactive scatter by species |

Best-practice tips:

- Start with the question, not the chart.
- Use bar charts for counts and category comparisons.
- Use histograms for numeric distributions.
- Use box plots when comparing spread across groups.
- Use scatter plots for relationships between two numeric measurements.
- Use color for meaningful groups, not decoration.
- Keep titles specific and labels readable.
- Avoid 3D charts and overloaded legends for beginner analysis.
- Do not use pie charts when many categories or precise comparison is needed.

Concrete examples:

```python
species_counts = penguins["species"].value_counts()
species_counts
```

```python
plt.figure(figsize=(7, 4))
species_counts.plot(kind="bar")
plt.title("Penguin Count by Species")
plt.xlabel("Species")
plt.ylabel("Number of penguins")
plt.show()
```

Guided practice:

- Repeat the count pattern for `island`.
- Change the chart title and axis labels.

Check-your-understanding questions:

- Why is a bar chart appropriate for `species`?
- Would a histogram be appropriate for `species`? Why or why not?

Mini task:

- Create a bar chart of penguin counts by island and write one observation.

## Subchapter 3: Matplotlib Foundations

Estimated time: 40 to 55 minutes.

Goal: show Matplotlib as the base plotting library and teach learners the parts of a chart.

Focus on a small number of readable examples:

1. Bar chart for category counts.
2. Histogram for body mass.
3. Scatter plot for flipper length and body mass.

Example 1: Matplotlib bar chart

```python
species_counts = penguins["species"].value_counts()

plt.figure(figsize=(7, 4))
plt.bar(species_counts.index, species_counts.values)
plt.title("Adelie Penguins Are the Largest Group in This Dataset")
plt.xlabel("Species")
plt.ylabel("Number of penguins")
plt.show()
```

Example 2: Matplotlib histogram

```python
plt.figure(figsize=(7, 4))
plt.hist(penguins["body_mass_g"].dropna(), bins=20)
plt.title("Body Mass Values Are Spread Across Several Ranges")
plt.xlabel("Body mass (g)")
plt.ylabel("Number of penguins")
plt.show()
```

Example 3: Matplotlib scatter plot

```python
plt.figure(figsize=(7, 5))
plt.scatter(
    penguins["flipper_length_mm"],
    penguins["body_mass_g"],
    alpha=0.7
)
plt.title("Penguins With Longer Flippers Often Have Higher Body Mass")
plt.xlabel("Flipper length (mm)")
plt.ylabel("Body mass (g)")
plt.show()
```

Teaching points:

- `plt.figure(figsize=...)` controls chart size.
- `plt.title()`, `plt.xlabel()`, and `plt.ylabel()` make charts easier to understand.
- `dropna()` avoids plotting missing values.
- Insight-oriented titles are often more useful than generic titles.

Guided practice:

- Change the histogram from `body_mass_g` to `flipper_length_mm`.
- Adjust the number of bins and observe the difference.

Check-your-understanding questions:

- What does each dot represent in the scatter plot?
- What changes when you increase or decrease `bins`?

Mini task:

- Create a Matplotlib histogram of bill length and write one sentence about the shape.

## Subchapter 4: Seaborn for Clearer Statistical Charts

Estimated time: 45 to 60 minutes.

Goal: show that Seaborn makes grouped visualizations easier and often more readable.

Focus examples:

1. Count plot.
2. Histogram with group color.
3. Box plot by species.
4. Scatter plot with species color.

Example 1: Seaborn count plot

```python
plt.figure(figsize=(7, 4))
sns.countplot(data=penguins, x="species")
plt.title("Penguin Count by Species")
plt.xlabel("Species")
plt.ylabel("Number of penguins")
plt.show()
```

Example 2: Seaborn histogram by species

```python
plt.figure(figsize=(8, 5))
sns.histplot(data=penguins, x="body_mass_g", hue="species", bins=20)
plt.title("Body Mass Distribution Differs by Species")
plt.xlabel("Body mass (g)")
plt.ylabel("Number of penguins")
plt.show()
```

Example 3: Seaborn box plot

```python
plt.figure(figsize=(8, 5))
sns.boxplot(data=penguins, x="species", y="body_mass_g")
plt.title("Gentoo Penguins Tend to Have Higher Body Mass")
plt.xlabel("Species")
plt.ylabel("Body mass (g)")
plt.show()
```

Example 4: Seaborn scatter plot

```python
plt.figure(figsize=(8, 5))
sns.scatterplot(
    data=penguins,
    x="flipper_length_mm",
    y="body_mass_g",
    hue="species"
)
plt.title("Flipper Length and Body Mass Show Species Patterns")
plt.xlabel("Flipper length (mm)")
plt.ylabel("Body mass (g)")
plt.show()
```

Teaching points:

- `data=`, `x=`, `y=`, and `hue=` make chart code easier to read.
- Box plots show median, spread, and possible outliers.
- Color should encode a useful variable such as `species`.
- Visual separation between groups is not the same as a formal statistical test.

Guided practice:

- Change the box plot from `body_mass_g` to `bill_length_mm`.
- Change scatter plot color from `species` to `sex` and discuss missing values.

Check-your-understanding questions:

- Which species has the highest typical body mass?
- What does the middle line in a box plot represent?
- Why is Seaborn convenient for group comparisons?

Mini task:

- Create one Seaborn chart comparing `flipper_length_mm` by `species` and write one observation.

## Subchapter 5: Plotly and a Short Visual Story

Estimated time: 45 to 70 minutes.

Goal: introduce Plotly as a Colab-friendly interactive option, then assemble a short visual mini report.

Keep Plotly examples simple and optional-feeling, but runnable. Do not require advanced customization.

Example 1: interactive scatter plot

```python
fig = px.scatter(
    penguins,
    x="flipper_length_mm",
    y="body_mass_g",
    color="species",
    hover_data=["island", "sex", "year"],
    title="Interactive View: Flipper Length and Body Mass by Species",
    labels={
        "flipper_length_mm": "Flipper length (mm)",
        "body_mass_g": "Body mass (g)",
        "species": "Species"
    }
)

fig.show()
```

Example 2: interactive box plot

```python
fig = px.box(
    penguins,
    x="species",
    y="body_mass_g",
    color="species",
    title="Interactive Box Plot: Body Mass by Species",
    labels={
        "species": "Species",
        "body_mass_g": "Body mass (g)"
    }
)

fig.show()
```

Example 3: interactive histogram

```python
fig = px.histogram(
    penguins,
    x="flipper_length_mm",
    color="species",
    nbins=20,
    title="Interactive Histogram: Flipper Length by Species",
    labels={
        "flipper_length_mm": "Flipper length (mm)",
        "species": "Species"
    }
)

fig.show()
```

Teaching points:

- Plotly is useful for hovering and exploring details.
- Interactive charts are helpful for exploration, but final reports still need written interpretation.
- Plotly charts should still have clear titles and labels.
- Interactivity should not replace clear analytical thinking.

Guided practice:

- Add `island` to hover information.
- Try coloring by `island` instead of `species`.

Check-your-understanding questions:

- What extra information appears when you hover?
- When might an interactive chart be more useful than a static chart?
- What could become confusing if too many variables are shown at once?

Mini task:

- Create one Plotly chart that helps compare species and write one observation.

## End-of-Day Mini Report

Estimated time: 30 to 45 minutes.

Learners should assemble a short visual story using 2 to 3 charts. The report can be a mix of Seaborn and Plotly, with Matplotlib used for at least one foundational example earlier in the notebook.

Suggested report structure:

1. Short question:
   - Example: "How do penguin body measurements differ by species?"
2. Chart 1:
   - Bar chart or count plot showing species counts.
3. Chart 2:
   - Box plot comparing body mass or flipper length by species.
4. Chart 3:
   - Scatter plot showing the relationship between flipper length and body mass.
5. Written findings:
   - 3 to 5 short bullet points.
6. Caution:
   - One sentence explaining what the charts cannot prove.

Example conclusion prompts:

- Which species appears largest by body mass?
- Which measurement shows the clearest group difference?
- Are there any missing values or sample-size issues to mention?
- What pattern is visible, and what should we avoid overclaiming?

## Common Mistakes to Include

- Choosing a chart before deciding the analytical question.
- Using a histogram for category labels.
- Forgetting `plt.show()` after Matplotlib or Seaborn charts.
- Forgetting `dropna()` when plotting numeric columns with missing values.
- Reading a scatter plot as proof that one variable causes another.
- Adding too many colors, categories, or labels at once.
- Leaving chart titles and axis labels generic.
- Running Plotly code before importing `plotly.express as px`.
- Expecting interactive Plotly charts to appear in exported static formats exactly as they do in Colab.

## Optional Bonus Tasks

Use only if the group is moving quickly:

- Create a faceted Plotly scatter plot with `facet_col="species"`.
- Compare `bill_length_mm` and `bill_depth_mm` by species.
- Save one Matplotlib chart as a PNG using `plt.savefig("penguins_chart.png", dpi=150)`.
- Add a short Markdown caption under each chart.
- Start the Gapminder bonus notebook for time-trend visualization.

## Run All Checklist

Before considering the notebook ready:

- The notebook runs from top to bottom in Google Colab.
- Data loads from local path or raw GitHub URL.
- `NA` values are interpreted as missing values.
- All imports are included near the top.
- No package installation cells are required.
- Every chart has a title and axis labels.
- Plotly examples display with `fig.show()` in Colab.
- Most code cells produce visible output.
- Markdown explains what learners should notice.
- The final mini report contains 2 to 3 charts and 3 to 5 written findings.

## Proposed Cell Flow

Target length: 45 to 70 cells.

Approximate balance:

- 50 percent Markdown
- 50 percent code

Suggested sequence:

1. Title and learning outcomes.
2. How to use this workbook.
3. Setup imports.
4. Load Penguins data.
5. Dataset explanation.
6. Subchapter 1 inspection cells.
7. Subchapter 2 chart-choice guidance and simple bar chart.
8. Subchapter 3 Matplotlib examples.
9. Subchapter 4 Seaborn examples.
10. Subchapter 5 Plotly examples.
11. End-of-day visual mini report.
12. Common mistakes and troubleshooting.
13. Reflection prompts.
14. Optional bonus tasks.
