# 1. diena: Python, notebook pamati un tabulāru datu analīze

Šī mape satur 1. dienas darba burtnīcas Google Colab un Jupyter Notebook formātā.

Kursa sākumā mērķis ir iegūt pārliecību par darbu ar skaitļošanas piezīmju grāmatām (computational notebooks), Google Colab, Markdown šūnām, Python koda šūnām un Pandas DataFrame tabulām. Pēc tam šīs prasmes tiek izmantotas lielākā datu analīzes uzdevumā ar Titanic datu kopu.

Repozitorijs: [ValRCS/RTU_Python_Data_Analysis_Visualization_May_2026](https://github.com/ValRCS/RTU_Python_Data_Analysis_Visualization_May_2026)

## Ieteicamā darba secība

| Secība | Notebook | Mērķis | Atvērt Colab |
| --- | --- | --- | --- |
| 1 | `01_python_jupyter_notebook_basics_lv.ipynb` | Ievads latviski: notebooks, Colab, Markdown, DataFrame un Python pamati | [![Atvērt Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ValRCS/RTU_Python_Data_Analysis_Visualization_May_2026/blob/main/notebooks/day_1/01_python_jupyter_notebook_basics_lv.ipynb) |
| 2 | `01_day1_titanic_data_analysis.ipynb` | Galvenā 1. dienas datu analīzes darba burtnīca ar Titanic datu kopu | [![Atvērt Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ValRCS/RTU_Python_Data_Analysis_Visualization_May_2026/blob/main/notebooks/day_1/01_day1_titanic_data_analysis.ipynb) |
| Papildu | `01_python_jupyter_notebook_basics.ipynb` | Tā pati ievada burtnīca angļu valodā | [![Atvērt Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ValRCS/RTU_Python_Data_Analysis_Visualization_May_2026/blob/main/notebooks/day_1/01_python_jupyter_notebook_basics.ipynb) |

## 1. dienas galvenie mērķi

Pēc 1. dienas dalībniekiem vajadzētu spēt:

- atvērt un palaist Google Colab notebook
- atšķirt Markdown šūnas un koda šūnas
- saprast, kāpēc notebook ir reproducējamas analīzes dokuments
- ielādēt CSV failu Pandas DataFrame tabulā
- apskatīt rindas, kolonnas, datu tipus un trūkstošās vērtības
- atlasīt kolonnas un filtrēt rindas
- kārtot un skaitīt kategorijas
- veikt vienkāršu datu tīrīšanu
- grupēt datus un veidot kopsavilkumus
- uzrakstīt īsus analītiskus secinājumus

## Ievada notebook saturs

Latviešu ievada notebook `01_python_jupyter_notebook_basics_lv.ipynb` ir paredzēts pirmajām 1 līdz 2 akadēmiskajām stundām.

Tajā ir šādas sadaļas:

1. Kas ir skaitļošanas piezīmju grāmatas (computational notebooks)
2. Jupyter Notebook pamati
3. Google Colab pamati
4. Markdown pieraksts analītiskām piezīmēm
5. Pirmais DataFrame darba process ar `data/pirkumi.csv`
6. Python pamati notebook koda lasīšanai
7. Bonusa stabiņu diagramma (bar chart)

Šajā notebook izmantotā mazā datu kopa ir `data/pirkumi.csv`. Tā palīdz saprast pamatideju bez sarežģīta datu konteksta.

## Galvenā Titanic darba burtnīca

`01_day1_titanic_data_analysis.ipynb` ir galvenā 1. dienas analīzes darba burtnīca.

Tās darba process:

1. Ielādēt Titanic CSV datu kopu
2. Apskatīt pirmās rindas, kolonnu nosaukumus un datu izmēru
3. Pārbaudīt datu tipus un trūkstošās vērtības
4. Atlasīt, filtrēt un kārtot datus
5. Tīrīt vienkāršas datu problēmas
6. Grupēt datus un veidot kopsavilkumus
7. Sagatavot īsu dienas noslēguma mini ziņojumu

Excel salīdzinājumam: DataFrame ir līdzīga darblapai vai tabulai, filtrēšana ir līdzīga Excel filtriem, bet `groupby()` ir līdzīgs Pivot Table idejai.

## Praktiskie uzdevumi

1. Palaist ievada notebook no sākuma līdz beigām.
2. Markdown šūnā uzrakstīt savu pirmo datu jautājumu.
3. Ielādēt `pirkumi.csv` un apskatīt `head()`, `shape`, `info()` un `describe()`.
4. Izveidot jaunu kolonnu `summa`.
5. Saglabāt pārveidoto datu tabulu CSV failā.
6. Izveidot vienkāršu stabiņu diagrammu par tēriņiem pa veikaliem.
7. Galvenajā Titanic notebook atkārtot to pašu analīzes loģiku ar lielāku datu kopu.
8. Dienas beigās uzrakstīt 3 līdz 5 īsus secinājumus par datiem.

## Kā strādāt Google Colab vidē

1. Klikšķiniet uz Colab saites tabulā augstāk.
2. Pagaidiet, kamēr notebook atveras Colab vidē.
3. Izvēlieties **Runtime > Run all**, lai pārbaudītu, ka viss darbojas no sākuma līdz beigām.
4. Nodarbībā labāk palaist šūnas pa vienai un apskatīt katru izvadi.
5. Ja Colab prasa pieslēgties izpildes videi (runtime), apstipriniet to.

Notebook datu ielādes šūnas ir veidotas tā, lai tās darbotos Colab vidē bez manuālas failu augšupielādes.

## Lokāla darbināšana VS Code vidē

Google Colab ir ieteicamā vide. Ja vēlaties strādāt lokāli VS Code vidē, nepieciešams:

- Python
- VS Code
- VS Code Python paplašinājums
- VS Code Jupyter paplašinājums
- lejupielādēts vai noklonēts šis repozitorijs
- instalētas atkarības no `requirements.txt`

Tipiska sagatavošana repozitorija mapē:

```powershell
python -m venv .venv
.\\.venv\\Scripts\\python.exe -m pip install -r requirements.txt
```

Pēc tam atveriet attiecīgo `.ipynb` failu VS Code vidē un izvēlieties `.venv` Python kodolu (kernel).

## Datu kopas

1. dienā tiek izmantotas divas datu kopas:

- `data/pirkumi.csv`: maza mācību datu kopa ievada notebook vajadzībām
- `data/titanic.csv`: galvenā 1. dienas analīzes datu kopa

Abi notebook ir veidoti tā, lai vispirms mēģinātu atrast lokālo failu un pēc tam izmantotu GitHub raw saiti, ja lokālais fails nav pieejams.

## Noslēguma rezultāts

1. dienas beigās dalībniekiem vajadzētu būt nelielam reproducējamam analīzes darbam ar:

- ielādētu tabulāru datu kopu
- pārbaudītām rindām, kolonnām un datu tipiem
- vienkāršiem filtriem un kopsavilkumiem
- vismaz vienu skaidru interpretāciju
- īsu mini ziņojumu ar secinājumiem

Galvenā doma: Python notebook ļauj dokumentēt analīzi tā, lai to varētu atkārtot, pārbaudīt un paskaidrot citiem.
