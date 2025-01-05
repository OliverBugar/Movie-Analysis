# Movie Analysis

Since I am a big fan of movies (especially horror films), I wanted to try data analysis to create a dashboard for the best movies according to genres, revenue, user reactions, ratings, and budget, so I might uncover some hidden gems that I haven't seen yet. I downloaded the data from Kaggle: [Which Movie Should I Watch Today?](https://www.kaggle.com/datasets/hassanelfattmi/which-movie-should-i-watch-today). The dataset consists of four different sheets, each containing 9,718 rows.

- The first sheet contains the following columns: id, title, genres, language, user_score, runtime_hour, runtime_min, release_date, vote_count.
- The second sheet contains the following columns: id, runtime, budget, revenue, film_id.
- The third sheet contains the following columns: id, director, top_billed, budget_usd, revenue_usd.
- The fourth sheet contains the following columns: id, poster_path, backdrop_path.

I used Jupyter Notebook and Python for the analysis. First, I joined all the sheets into one dataset. Then, I dropped unnecessary columns like additional film_id, poster_path, backdrop_path, and top_billed (names of actors billed). I merged the runtime_hour and runtime_min columns into one (total minutes) and removed any rows with missing data.

After initial data cleaning, I was left with 6,128 rows. I then converted the budget and revenue columns from float to integer data types to allow for averages by genre. After additional cleaning, I uploaded the dataset to Tableau, where I started working on the dashboards.

First, I created a visualization showing all the movies based on the number of vote counts and average user scores throughout the years. Users can filter by genre as desired.

<img width="896" alt="Snímka obrazovky 2025-01-03 o 15 57 55" src="https://github.com/user-attachments/assets/9c1beb6b-e5bf-438a-a9af-f79938d65e26" />

After creating a visualization showing all the movies based on the number of vote counts, we can not focus on trends of different genres based on budget and revenue. We can see in our analysis, that for example action movies have the highest revenue when their budget is about 300M USD (first photo). As for my favourite genre, we can see, that horror movies have a tendency to have higher revenue, as the budget is getting bigger (second photo). 

<img src="https://github.com/user-attachments/assets/9259d5a8-ea5e-4cba-a466-0bd57e476b9f" alt="Description" width="500" height="300">

![Snímka obrazovky 2025-01-05 o 19 07 32](https://github.com/user-attachments/assets/9259d5a8-ea5e-4cba-a466-0bd57e476b9f).  

![Snímka obrazovky 2025-01-05 o 19 15 06](https://github.com/user-attachments/assets/8e993ab1-b3e9-4fdc-ba86-bfbbf6046599)






Analysing movies by Genre, Revenue etc


1. Vizualizácia žánrov a tržieb

Otázka: Ktoré žánre majú najvyššie tržby?
Postup:
Pretiahni genres do riadkov a revenue do stĺpcov.
Použi Bar Chart na vizualizáciu.
Pridaj filter na language alebo časový filter na release_date.

2. Analýza ROI a rozpočtov

Otázka: Aký je vzťah medzi rozpočtom filmu a návratnosťou investície?
Postup:
Pretiahni budget na X-Axis a ROI na Y-Axis.
Použi Scatter Plot a farebne rozlíš podľa genres.

3. Trendy v čase

Otázka: Ako sa menili tržby v jednotlivých rokoch?
Postup:
Pretiahni release_date (zmeniť na rok) na X-Axis a revenue na Y-Axis.
Použi Line Chart na zobrazenie trendov.
Rozdeľ podľa genres alebo language.

4. Dĺžka filmu a hodnotenie používateľov

Otázka: Má dĺžka filmu vplyv na hodnotenie používateľov?
Postup:
Pretiahni Total Runtime na X-Axis a user_score na Y-Axis.
Použi Scatter Plot.
Pridaj trendovú čiaru (Trend Line) na vizualizáciu vzťahu.

5. Najlepší režiséri

Otázka: Ktorí režiséri majú najvyššie hodnotenia?
Postup:
Pretiahni director do riadkov a priemerné user_score do stĺpcov.
Použi Bar Chart a zoradi podľa priemeru hodnotení.
Pridaj filter na genres alebo release_date.

3. Dashboard v Tableau
Vytvorenie dashboardu:
Kombinuj viacero grafov na jednom plátne (napr. tržby podľa žánrov, dĺžka filmu vs. hodnotenie, trendy v čase).
Pridaj interaktívne filtre, aby používatelia mohli filtrovať podľa jazyka, žánru, alebo rokov.
Použi Actions na prepojenie grafov – napr. kliknutie na žáner aktualizuje všetky grafy.
Príklad:
Ľavá strana: Bar Chart s tržbami podľa žánrov.
Stred: Line Chart s trendmi v čase.
Pravá strana: Scatter Plot s ROI vs. rozpočet.


https://public.tableau.com/app/profile/kimly.scott/viz/Themoviesofthedecade/MoviesoftheDecade
