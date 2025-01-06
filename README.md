# Movie Analysis

Since I am a big fan of movies (especially horror films), I wanted to try data analysis to create a dashboard for the best movies according to genres, revenue, user reactions, ratings, and budget, so I might uncover some hidden gems that I haven't seen yet. I downloaded the data from Kaggle: [Which Movie Should I Watch Today?](https://www.kaggle.com/datasets/hassanelfattmi/which-movie-should-i-watch-today). The dataset consists of four different sheets, each containing 9,718 rows.

# Dataset Overview

Sheet 1:

Columns: id, title, genres, language, user_score, runtime_hour, runtime_min, release_date, vote_count.

Sheet 2:

Columns: id, runtime, budget, revenue, film_id.

Sheet 3:

Columns: id, director, top_billed, budget_usd, revenue_usd.

Sheet 4:

Data Preparation

I used Jupyter Notebook and Python for the analysis. The steps I followed:

# Data Cleaning:

I've merged all sheets into a single dataset, dropped unnecessary columns such as film_id, poster_path, backdrop_path, and top_billed, combined runtime_hour and runtime_min into a single column (total runtime in minutes), removed rows with missing data.

Final Dataset:

After cleaning, 6,128 rows remained. I have converted budget and revenue columns from float to integer data types to allow for better calculations.

Visualization Preparation:

Uploaded the cleaned dataset to Tableau to create interactive dashboards.

After initial data cleaning, I was left with 6,128 rows. I then converted the budget and revenue columns from float to integer data types to allow for averages by genre. After additional cleaning, I uploaded the dataset to Tableau, where I started working on the dashboards.

First, I created a visualization showing all the movies based on the number of vote counts and average user scores throughout the years. Users can filter by genre as desired.

<p align="center">
<img width="1000" alt="Snímka obrazovky 2025-01-03 o 15 57 55" src="https://github.com/user-attachments/assets/9c1beb6b-e5bf-438a-a9af-f79938d65e26" />
</p>
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
<p align="center">
<img src="https://github.com/user-attachments/assets/9259d5a8-ea5e-4cba-a466-0bd57e476b9f" alt="Description" width="400" height="400">  <img src="https://github.com/user-attachments/assets/ecd075d1-ae65-4e54-8ed1-46cf50dfc245" alt="Description" width="400" height="400">
</p>
# Analysis of Revenue Trands throughout the years

After analyzing Budget vs. Revenue trends across genres, we shifted focus to how revenue evolved over time. The chart below highlights revenue trends for different genres, with a notable drop in 2020 caused by the COVID-19 pandemic.

During this time, global cinema closures and restrictions drastically reduced film revenue. For instance, China’s box office revenue fell from $2.1 billion in early 2019 to just $3.9 million in early 2020, following the closure of 70,000 cinemas in January. Similar trends were seen worldwide: Italy reported a 94% drop in revenue during the first weekend of March 2020, and many other countries—including the US, UK, and Japan—closed cinemas entirely in March and April.

These closures, along with reduced attendance and capacity limitations, had a severe impact on global box office performance. Before 2020, action movies consistently dominated revenue, generating the largest share at the box office.
<p align="center">
<img src="https://github.com/user-attachments/assets/70747412-fde5-44a2-a694-64db5b475d3b" alt="Description" width="640" height="350"> <img src="https://github.com/user-attachments/assets/cdb08eb3-5072-4421-8b39-038877a59f7c" alt="Description" width="140" height="350">
</p>

# Analysis of Movie Length and User Score

When evaluating the relationship between movie duration and user scores, key insights can help identify the characteristics of high-scoring films. Based on the data visualization:

Optimal Movie Length for High Scores:
        Movies with durations between 90 and 140 minutes tend to receive the highest user scores.
        Within this range, some films achieve scores above 20, indicating strong audience approval and engagement.

Decreasing Scores Beyond 145 Minutes:
        Films exceeding 145 minutes in runtime generally show a decline in user scores, with scores falling between 6 and 14.
        This trend suggests that longer movies may struggle to maintain viewer interest or satisfaction.

Lowest User Scores for Lengthy Films:
        Movies with durations over 190 minutes exhibit the lowest user scores. These films rarely score above 6, emphasizing the challenges of creating long movies that resonate with audiences.

Key Takeaways for Filmmakers:
        To maximize audience satisfaction, aiming for a runtime between 90 and 140 minutes appears optimal.
        While longer films are sometimes necessary for complex storytelling, filmmakers should carefully consider pacing and narrative engagement to avoid score penalties.

Considerations for Specific Genres:
        Further segmentation by genre may reveal exceptions or additional patterns (e.g., epics or historical dramas might perform differently). Exploring this segmentation could provide tailored insights for specific types of films.

By understanding these patterns, filmmakers and studios can better align their creative and production decisions with audience preferences, optimizing the potential for critical and commercial success.   
<p align="center">
<img src="https://github.com/user-attachments/assets/8c7280a0-32c9-4b02-a98a-7ecac84e3b42" alt="Description" width="600" height="600">
</p>

# Best movie directors

From the visualization, we observe the average user scores for movies directed by various filmmakers. This analysis provides valuable insights for understanding how director performance aligns with user satisfaction, which is crucial for identifying top-performing directors or benchmarks in the film industry. Here's a breakdown of the insights:

Top Directors by User Score:
        Martin Scorsese has the highest average user score, exceeding 7.5, making him the most successful director in terms of audience appreciation.
        Directors such as Roman Polanski, Steven Spielberg, and Sam Liu closely follow, with scores above 7.0, indicating consistently well-received work.

Consistency in Scores:
        The directors in this list maintain an average user score of above 6.0, showcasing their ability to deliver movies that resonate well with audiences.
        The scores gradually decrease, with John Carpenter being the lowest among the Top 20, averaging just above 4.0.

Key Insights for Film Production:
        Directors with higher user scores are more likely to create critically acclaimed movies. Collaborating with such directors can lead to better audience reception.
        Martin Scorsese, Roman Polanski, and Steven Spielberg demonstrate the importance of storytelling, direction, and consistency in maintaining audience engagement.

Trends for Movie Development:
        This analysis can guide movie studios in selecting directors for high-budget projects where audience reception is a priority.
        By focusing on directors with scores above 6.0, producers can minimize the risk of underperformance.

<p align="center">
<img src="https://github.com/user-attachments/assets/7c6c1afa-362f-48bc-bafa-0f3eeb30cba0" alt="Description" width="600" height="600">
</p>

# Conclusion

This movie analysis project offered a deep dive into the interplay of factors such as budget, revenue, user scores, runtime, and directors’ influence on the success of films. By leveraging data analysis and visualization tools like Python and Tableau, several valuable insights emerged, shedding light on key trends in the film industry.
Key Takeaways from the Analysis
1. Revenue and Budget Relationship

    Action Movies: These films demonstrate the potential for significant returns on high-budget projects, with a sweet spot for budgets around $300 million yielding revenues exceeding $1 billion. However, diminishing returns beyond this budget point indicate the importance of maintaining a balance between investment and expected returns.
    Horror Movies: While traditionally associated with low budgets, the analysis revealed untapped potential for higher-budget horror films. Investing in budgets above $50 million can yield disproportionately higher returns, making it a promising area for studios to explore.

2. User Preferences and Movie Runtime

    The analysis revealed that audiences tend to favor films with runtimes between 90-140 minutes, as these lengths consistently score higher on user satisfaction metrics. Longer films (over 145 minutes) generally see a decline in scores, likely due to pacing issues or audience fatigue. Filmmakers should consider these preferences during production to maximize viewer engagement and satisfaction.

3. Impact of COVID-19 on Revenue Trends

    The analysis confirmed the devastating impact of the COVID-19 pandemic on global box office revenues, with steep declines observed in 2020. Countries like China, Italy, the US, and the UK faced unprecedented drops, underscoring the vulnerability of the movie industry to global crises. This highlights the need for diversifying revenue streams, such as digital releases and streaming platforms, to mitigate the impact of future disruptions.

4. Director Influence on Movie Success

    Directors like Martin Scorsese, Roman Polanski, Steven Spielberg, and Sam Liu emerged as consistent performers with high average user scores. Collaborating with experienced and acclaimed directors can reduce the risk of underperformance, especially for high-budget productions. Studios should also prioritize creative freedom and innovation in storytelling, as these are often hallmarks of top-rated films.

5. Genre-Specific Trends

    Action and horror movies stood out in the analysis, with action films benefiting from larger budgets and horror films showing potential for growth with mid-to-high-range budgets. Other genres, such as drama and comedy, may require further exploration to identify their unique revenue and audience engagement patterns.

Broader Implications for the Movie Industry
For Studios and Filmmakers:

Data-Driven Decision Making: Leveraging data to predict audience preferences and optimize production budgets can significantly improve financial outcomes.
    Strategic Budget Allocation: Allocating resources according to genre-specific trends can help studios maximize ROI while minimizing risks.
    Adaptation to Changing Market Conditions: The COVID-19 pandemic highlighted the importance of flexibility in distribution strategies, with streaming platforms becoming a vital alternative to traditional box office releases.

For Audiences:

The analysis provides valuable insights into hidden gems and underrated movies that align with user preferences and high scores.
    Understanding trends in runtime, genres, and director influence can help audiences make informed choices when exploring new films.

Future Directions

This project serves as a foundation for deeper exploration of the movie industry. Several areas for future research include:

Regional Analysis: Analyzing trends in specific markets to identify cultural and regional preferences.
    Streaming vs. Box Office Revenue: Comparing the performance of movies released on digital platforms versus traditional theaters.
    Predictive Modeling: Building machine learning models to forecast movie performance based on pre-release data such as cast, director, budget, and genre.
    Audience Segmentation: Studying demographic data to understand how age, gender, and location influence movie preferences.
    Genre Evolution: Investigating how audience tastes in genres have evolved over decades and predicting future trends.

Personal Takeaway

This project has been an enlightening journey into the intricate dynamics of the movie industry. As a passionate movie enthusiast, I now have a deeper appreciation for the factors that contribute to a film's success or failure. The findings not only helped me identify hidden gems to watch but also provided a framework for understanding how the movie industry operates on a global scale.

By bridging data analysis with creative storytelling, this project demonstrates the immense potential of data-driven approaches in shaping the future of entertainment.
