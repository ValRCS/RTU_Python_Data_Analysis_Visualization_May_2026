# Python Data Analysis and Visualization Course

Two-day, 10 academic-hour practical course for adult beginners learning data analysis with Python, Pandas, Matplotlib, Seaborn, and Google Colab.

The course is designed for people with little or no programming experience. Excel experience is useful, but not required.

## Start Here

If this is your first visit:

1. Open the Day 1 starter notebook in Google Colab.
2. Sign in with a Google account if Colab asks.
3. During class, run notebook cells one by one and read the output after each step.
4. Use **Runtime > Run all** later when you want to check that the whole notebook still works.

Ja mācības notiek latviski, sāciet ar latviešu 1. dienas ievada notebook.

## What You Need

- A web browser
- A Google account for Google Colab
- No local Python installation
- No previous programming experience
- Willingness to read tables, charts, and short code examples carefully

## What This Course Is About

You will practice a reproducible data analysis workflow:

```text
Open notebook -> Load data -> Inspect table -> Clean simple issues
-> Filter and summarize -> Create charts -> Write conclusions
```

The focus is practical analysis, not software development. The notebooks use short code cells, visible outputs, Excel comparisons, and interpretation prompts.

## Which Notebook Should I Open?

| Situation | Notebook | Open in Colab |
| --- | --- | --- |
| I am starting Day 1 in Latvian | `notebooks/day_1/01_python_jupyter_notebook_basics_lv.ipynb` | [![Open Latvian Starter in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ValRCS/RTU_Python_Data_Analysis_Visualization_May_2026/blob/main/notebooks/day_1/01_python_jupyter_notebook_basics_lv.ipynb) |
| I want the Day 1 starter in English | `notebooks/day_1/01_python_jupyter_notebook_basics.ipynb` | [![Open Starter in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ValRCS/RTU_Python_Data_Analysis_Visualization_May_2026/blob/main/notebooks/day_1/01_python_jupyter_notebook_basics.ipynb) |
| I already know notebook basics | `notebooks/day_1/01_day1_titanic_data_analysis.ipynb` | [![Open Day 1 in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ValRCS/RTU_Python_Data_Analysis_Visualization_May_2026/blob/main/notebooks/day_1/01_day1_titanic_data_analysis.ipynb) |
| I am starting Day 2 | `notebooks/day_2/02_day2_penguins_visualization_storytelling.ipynb` | [![Open Day 2 in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ValRCS/RTU_Python_Data_Analysis_Visualization_May_2026/blob/main/notebooks/day_2/02_day2_penguins_visualization_storytelling.ipynb) |
| I finished early or want extra practice | `notebooks/day_2/03_bonus_gapminder_visual_analysis.ipynb` | [![Open Bonus in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ValRCS/RTU_Python_Data_Analysis_Visualization_May_2026/blob/main/notebooks/day_2/03_bonus_gapminder_visual_analysis.ipynb) |

The Day 1 starter notebooks are shorter onboarding notebooks for the first 1 to 2 academic hours. The main Day 1 and Day 2 workbooks are full-day notebooks with demonstrations, guided practice, check questions, mini tasks, common mistakes, reflection prompts, and a short final synthesis.

## What You Will Learn

By the end of the two main workbooks, you should be able to:

- open and run a Google Colab notebook
- load a CSV file into a Pandas DataFrame
- inspect rows, columns, data types, and missing values
- filter, sort, and summarize tabular data
- clean basic data issues
- create readable charts
- compare groups using tables and visualizations
- write short analytical conclusions
- re-run your analysis as a reproducible notebook

Different groups may move at different speeds. The core path is beginner-friendly, and faster learners can use the extra practice prompts and bonus notebook.

## How To Use Google Colab During Class

1. Click a Colab badge in the table above.
2. Wait for the notebook to open in Google Colab.
3. If Colab asks to connect to a runtime, approve it.
4. In class, run cells one by one so you can see each result.
5. If something looks wrong, re-run the previous few cells before changing the code.
6. Use **Runtime > Run all** when you want to check the whole notebook from start to finish.

The notebook data-loading cells are designed to work in Colab without manual CSV uploads.

## Expected Results

After Day 1, you should have a small reproducible Titanic data analysis with tables, filters, summaries, and 3 to 5 short conclusions.

After Day 2, you should have a short Penguins visual report with 2 to 3 readable charts and written interpretations.

The optional Gapminder workbook gives extra practice with historical public-data trends, chart-choice justification, and visual storytelling.

## Datasets

Datasets are stored in `data/`:

- `titanic.csv` for Day 1 data analysis
- `penguins.csv` for Day 2 visualization and storytelling
- `gapminder.csv` for optional bonus visualization and analysis

Dataset teaching notes and Colab URLs are documented in `docs/DATASETS.md`.

## Instructor And Maintainer Notes

Instructional guidance lives in:

- `AGENTS.md` - concise agent operating brief
- `docs/COURSE_STRUCTURE.md` - two-day workbook structure
- `docs/NOTEBOOK_TEMPLATE.md` - workbook and subchapter template
- `docs/PEDAGOGY.md` - teaching philosophy and adult-learning guidance
- `docs/DATASETS.md` - dataset roles, caveats, and loading URLs

Encoding note: Latvian text in Markdown and notebooks should be saved as UTF-8. If local PowerShell output shows broken Latvian characters, verify the file with explicit UTF-8 decoding before changing the text. GitHub and Colab expect UTF-8.

## Scope

The core course avoids advanced software engineering topics, machine learning, APIs, SQL, and complex environment management. The focus is practical, reproducible analysis for beginner professional learners.
