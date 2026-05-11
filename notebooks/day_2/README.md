# 2. diena: datu vizualizācija un analītiska stāstīšana

Šī mape satur 2. dienas Google Colab darba burtnīcas par datu vizualizāciju, diagrammu izvēli un īsu analītisku secinājumu rakstīšanu.

2. dienas mērķis ir pāriet no tabulu pārbaudes un kopsavilkumiem uz skaidrām vizualizācijām. Dalībnieki mācās izvēlēties piemērotu diagrammas tipu, uzlabot virsrakstus un asu nosaukumus, salīdzināt grupas, pamanīt sakarības un nepārspīlēt secinājumus.

Repozitorijs: [ValRCS/RTU_Python_Data_Analysis_Visualization_May_2026](https://github.com/ValRCS/RTU_Python_Data_Analysis_Visualization_May_2026)

## Ieteicamā darba secība

| Secība | Notebook | Mērķis | Atvērt Colab |
| --- | --- | --- | --- |
| 1 | `02_day2_penguins_visualization_storytelling.ipynb` | Galvenā 2. dienas darba burtnīca: Penguins datu vizualizācija, grupu salīdzināšana un vizuāls mini ziņojums | [![Atvērt Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ValRCS/RTU_Python_Data_Analysis_Visualization_May_2026/blob/main/notebooks/day_2/02_day2_penguins_visualization_storytelling.ipynb) |
| Papildu | `03_bonus_gapminder_visual_analysis.ipynb` | Bonusa darba burtnīca: Gapminder vēsturisko publisko datu vizualizācija ar Matplotlib, Seaborn un Plotly | [![Atvērt Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ValRCS/RTU_Python_Data_Analysis_Visualization_May_2026/blob/main/notebooks/day_2/03_bonus_gapminder_visual_analysis.ipynb) |

## 2. dienas galvenie mērķi

Pēc 2. dienas dalībniekiem vajadzētu spēt:

- ielādēt jaunu CSV datu kopu Google Colab vidē
- pārbaudīt rindas, kolonnas, datu tipus un trūkstošās vērtības
- izvēlēties diagrammas tipu pēc analītiskā jautājuma
- veidot stabiņu diagrammas, histogrammas, kastes diagrammas un izkliedes diagrammas
- izmantot Matplotlib pamata diagrammām
- izmantot Seaborn ērtākai grupu salīdzināšanai
- izmantot Plotly interaktīvai izpētei
- rakstīt īsus secinājumus par redzamajiem rakstiem
- noformēt nelielu vizuālu mini ziņojumu ar 2 līdz 3 diagrammām

## Galvenā Penguins darba burtnīca

`02_day2_penguins_visualization_storytelling.ipynb` ir galvenā 2. dienas darba burtnīca.

Tajā izmantota `data/penguins.csv` datu kopa. Katrā rindā ir informācija par vienu novērotu pingvīnu: suga, sala, ķermeņa mērījumi, dzimums un novērošanas gads.

Darba process:

1. Ielādēt Penguins datu kopu
2. Apskatīt pirmās rindas, kolonnas, datu tipus un trūkstošās vērtības
3. Saprast, kā izvēlēties piemērotu diagrammas tipu
4. Veidot Matplotlib pamata diagrammas
5. Veidot Seaborn grupu salīdzinājumus
6. Izmēģināt Plotly interaktīvās diagrammas
7. Sagatavot īsu vizuālu mini ziņojumu

Excel salīdzinājumam: kategoriju skaitīšana ir līdzīga Pivot Table kopsavilkumam, histogramma palīdz saprast skaitlisku vērtību sadalījumu, bet izkliedes diagramma ir līdzīga Excel scatter chart.

## Bonusa Gapminder darba burtnīca

`03_bonus_gapminder_visual_analysis.ipynb` ir papildu darba burtnīca ātrākām grupām vai patstāvīgai praksei pēc 2. dienas.

Tajā izmantota `data/gapminder.csv` datu kopa. Tā ir vēsturiska mācību datu kopa par valstīm, kontinentiem, gadiem, paredzamo dzīves ilgumu, iedzīvotāju skaitu un IKP uz vienu iedzīvotāju.

Bonusa darba burtnīcas fokuss:

- īsa, bet rūpīga Gapminder datu izpēte
- diagrammas izvēles pamatojums
- līniju diagrammas laika tendencēm
- stabiņu diagrammas valstu ranžēšanai
- Seaborn diagrammas kontinentu salīdzināšanai
- Plotly interaktīvas diagrammas un animācija
- īss publisko datu vizuālais stāsts ar piesardzības piezīmēm

Svarīga piezīme: šī Gapminder datu kopa beidzas 2007. gadā. Tā ir piemērota mācībām un vēsturiskai vizualizācijai, bet nav aktuāls sociālekonomisko rādītāju avots.

## Praktiskie uzdevumi

2. dienas laikā dalībnieki pakāpeniski veido:

1. kategoriju skaita tabulas un stabiņu diagrammas
2. histogrammas skaitlisku mainīgo sadalījumam
3. kastes diagrammas grupu salīdzināšanai
4. izkliedes diagrammas sakarību pārbaudei
5. interaktīvas Plotly diagrammas izpētei
6. īsus secinājumus zem diagrammām
7. noslēguma mini ziņojumu ar vairākām diagrammām

Galvenā doma: laba vizualizācija sākas ar jautājumu, nevis ar diagrammas tipu.

## Kā strādāt Google Colab vidē

1. Klikšķiniet uz Colab saites tabulā augstāk.
2. Pagaidiet, kamēr notebook atveras Colab vidē.
3. Izvēlieties **Runtime > Run all**, lai pārbaudītu, ka viss darbojas no sākuma līdz beigām.
4. Nodarbībā labāk palaist šūnas pa vienai un apskatīt katru izvadi.
5. Ja Colab prasa pieslēgties izpildes videi (runtime), apstipriniet to.

Notebook datu ielādes šūnas ir veidotas tā, lai vispirms meklētu lokālo failu un pēc tam izmantotu GitHub raw saiti. Tāpēc Colab vidē nav nepieciešams manuāli augšupielādēt CSV failus.

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
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
```

Pēc tam atveriet attiecīgo `.ipynb` failu VS Code vidē un izvēlieties `.venv` Python kodolu (kernel).

## Datu kopas

2. dienā tiek izmantotas divas datu kopas:

- `data/penguins.csv`: galvenā vizualizācijas un grupu salīdzināšanas datu kopa
- `data/gapminder.csv`: papildu vēsturiska publisko datu kopa laika tendenču un stāstīšanas praksei

Abi notebook ir veidoti tā, lai darbotos Google Colab vidē bez manuālas datu failu augšupielādes.

## Noslēguma rezultāts

2. dienas beigās dalībniekiem vajadzētu būt nelielam reproducējamam vizuālam ziņojumam ar:

- ielādētu un pārbaudītu datu kopu
- vairākām skaidri noformētām diagrammām
- pamatotu diagrammu izvēli
- īsiem secinājumiem zem diagrammām
- vismaz vienu piesardzības piezīmi par datu interpretāciju

Galvenā doma: diagramma nav tikai attēls. Tā ir veids, kā pamatoti atbildēt uz analītisku jautājumu.
