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

# Analysis of Budget vs. Revenue Trends Across Movie Genres

In our visualization analyzing movies based on budget and revenue, several interesting trends emerged for different genres:

Action Movies (Left Graph)
Action movies demonstrate a clear trend where the highest revenues are achieved when budgets are around $300M USD. This indicates that a substantial investment in production, special effects, and star power significantly contributes to box-office success. Beyond this threshold, there may be diminishing returns, suggesting that a balanced budget is key to maximizing profitability.

Horror Movies (Right Graph)
For horror movies, my personal favorite genre, the data reveals a steady upward trend in revenue as budgets increase. Higher budgets likely enhance production quality, marketing efforts, and distribution reach, leading to a broader audience and higher financial returns. This suggests that investing more in horror films can yield substantial payoffs, as seen with blockbuster hits in the genre.

Supporting Data Highlights
Action Movies: Films with budgets near $300M USD achieve average revenues exceeding $1B USD, significantly outperforming lower-budget counterparts.
Horror Movies: Titles with budgets of $50M+ USD see an average revenue increase of 50% compared to those with smaller budgets, underlining the value of strategic investment in this genre.

Broader Implications
The findings underscore the importance of tailoring budgets to genre-specific characteristics. For action movies, careful budget allocation to maximize impact without overspending is crucial. In contrast, for horror films, increasing budgets generally leads to proportional revenue growth, suggesting untapped potential for high-budget productions in this genre.

<img src="https://github.com/user-attachments/assets/9259d5a8-ea5e-4cba-a466-0bd57e476b9f" alt="Description" width="500" height="500">  <img src="https://github.com/user-attachments/assets/ecd075d1-ae65-4e54-8ed1-46cf50dfc245" alt="Description" width="500" height="500">

# Analysis of Revenue Trands throughout the years

After analyzing Budget vs. Revenue trends across genres, we shifted focus to how revenue evolved over time. The chart below highlights revenue trends for different genres, with a notable drop in 2020 caused by the COVID-19 pandemic.

During this time, global cinema closures and restrictions drastically reduced film revenue. For instance, China’s box office revenue fell from $2.1 billion in early 2019 to just $3.9 million in early 2020, following the closure of 70,000 cinemas in January. Similar trends were seen worldwide: Italy reported a 94% drop in revenue during the first weekend of March 2020, and many other countries—including the US, UK, and Japan—closed cinemas entirely in March and April.

These closures, along with reduced attendance and capacity limitations, had a severe impact on global box office performance. Before 2020, action movies consistently dominated revenue, generating the largest share at the box office.

<img src="https://github.com/user-attachments/assets/70747412-fde5-44a2-a694-64db5b475d3b" alt="Description" width="800" height="500"> <img src="https://github.com/user-attachments/assets/cdb08eb3-5072-4421-8b39-038877a59f7c" alt="Description" width="200" height="500">



3. Trendy v čase![Snímka obrazovky 2025-01-05 o 20 44 55]()


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
