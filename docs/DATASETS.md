# Datasets

## Overview

The course uses three small, teaching-friendly CSV datasets:

- Titanic for Day 1 data analysis
- Penguins for Day 2 visualization and storytelling
- Gapminder for optional bonus public-data analysis

All datasets are stored locally in `data/`. Notebooks should also include Colab-safe raw URLs so they run without manual file upload.

## Colab Raw URLs

Use these URLs as fallback paths in notebook loading cells:

```python
TITANIC_URL = "https://raw.githubusercontent.com/ValRCS/RTU_Python_Data_Analysis_Visualization_May_2026/main/data/titanic.csv"
PENGUINS_URL = "https://raw.githubusercontent.com/ValRCS/RTU_Python_Data_Analysis_Visualization_May_2026/main/data/penguins.csv"
GAPMINDER_URL = "https://raw.githubusercontent.com/ValRCS/RTU_Python_Data_Analysis_Visualization_May_2026/main/data/gapminder.csv"
```

Preferred loading pattern:

```python
from pathlib import Path

local_path = Path("../data/titanic.csv")
remote_url = TITANIC_URL

if local_path.exists():
    titanic = pd.read_csv(local_path)
else:
    titanic = pd.read_csv(remote_url)

titanic.head()
```

## Day 1: Titanic

Local file: `data/titanic.csv`

Shape: 891 rows, 12 columns

Columns:

- `PassengerId`
- `Survived`
- `Pclass`
- `Name`
- `Sex`
- `Age`
- `SibSp`
- `Parch`
- `Ticket`
- `Fare`
- `Cabin`
- `Embarked`

Teaching strengths:

- familiar introductory dataset
- useful for inspecting rows and columns
- clear categorical variables such as `Sex`, `Pclass`, and `Embarked`
- numeric variables such as `Age` and `Fare`
- missing values suitable for beginner cleaning discussion
- supports grouping and survival-rate summaries

Known missing values:

- `Age`: 177 missing
- `Cabin`: 687 missing
- `Embarked`: 2 missing

Recommended teaching use:

- loading CSV data
- inspecting with `head()`, `shape`, `info()`, and `describe()`
- selecting columns
- filtering and sorting
- counting categories
- identifying missing values
- discussing cleaning decisions
- grouping by `Sex`, `Pclass`, or `Embarked`
- writing short conclusions about survival patterns

Cautions:

- Titanic can lead learners toward machine learning. Keep Day 1 focused on analysis, not prediction.
- Survival patterns can involve sensitive social and historical interpretation. Keep wording careful and evidence-based.
- `Cabin` is mostly missing and should be used mainly to discuss missingness, not as a core analysis column.

## Day 2: Penguins

Local file: `data/penguins.csv`

Shape: 344 rows, 8 columns

Columns:

- `species`
- `island`
- `bill_length_mm`
- `bill_depth_mm`
- `flipper_length_mm`
- `body_mass_g`
- `sex`
- `year`

Teaching strengths:

- compact and readable
- good for charting numeric distributions
- natural group comparisons by `species` and `island`
- useful for scatterplots and color grouping
- supports visual interpretation without advanced statistics

Known missing values:

- 2 missing values in each main body measurement column
- 11 missing values in `sex`

Recommended teaching use:

- reusing inspection patterns from Day 1
- bar charts for categories
- histograms for numeric distributions
- box plots for group comparisons
- scatterplots for relationships
- chart titles, labels, and interpretation
- short visual storytelling mini project

Cautions:

- Avoid turning the notebook into a classification or machine learning lesson.
- Do not overstate causal explanations from scatterplots.
- Explain biological measurements in plain language before charting.

## Bonus: Gapminder

Local file: `data/gapminder.csv`

Shape: 1,704 rows, 6 columns

Columns:

- `country`
- `continent`
- `year`
- `lifeExp`
- `pop`
- `gdpPercap`

Time range: 1952 to 2007 in 5-year steps.

Teaching strengths:

- excellent for line charts
- useful for filtering by country, continent, and year
- supports public-data storytelling
- encourages careful interpretation and caveats

Recommended teaching use:

- line charts of life expectancy over time
- continent summaries
- country comparisons
- scatterplots of `gdpPercap` and `lifeExp`
- discussion of historical data limitations

Cautions:

- This is a historical teaching excerpt ending in 2007.
- It should not be presented as current socioeconomic data.
- Country comparisons require careful wording and context.

## Dataset Selection Rationale

The three datasets support a clear learning progression:

1. Titanic: practical tabular analysis with some messiness.
2. Penguins: readable visualization and group comparison.
3. Gapminder: optional time-series and public-data storytelling.

This avoids repeatedly introducing unfamiliar business contexts while still giving learners varied analytical situations.
