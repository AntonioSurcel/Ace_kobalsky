The first step of the project involved collecting data from various sources, including the NBA's official statistics database and salary information.
After cleaning and preprocessing the data to handle missing values and ensure consistency, I proceeded to build a predictive model using linear regression.

I want to say a big Thank you to  basketball-reference.com for providing the data.
I use 2 tables of data: 1. https://www.basketball-reference.com/leagues/NBA_2024_per_game.html - 2023-24 NBA Player Stats: Per Game
                        2. https://www.basketball-reference.com/contracts/players.html - 2023-24 NBA Player Contracts

1. The cleaning data:
   First i had to merge the data in one table.
   I did it with Vlookup in excel, but there was a problem. The names of the Balkan players.
   for exemple: Luka Dončić. the letters č, ć and so.
   Execl and R are having problems with reading such letters so i used i realy big function:
   =PROPER(SUBSTITUTE(SUBSTITUTE(SUBSTITUTE(SUBSTITUTE(SUBSTITUTE(SUBSTITUTE(SUBSTITUTE(SUBSTITUTE(SUBSTITUTE(SUBSTITUTE(SUBSTITUTE(CLEAN(A2), " ", CHAR(1)), CHAR(160), CHAR(1)), "č", "c"), "ć", "c"), "ņ", "n"), "š", "s"), "ž", "z"), "ļ", "l"), "ķ", "k"), "ģ", "g"), CHAR(1), " "))
   yes, i said realy big.
   and now my data is ready for R.

2.  I proceeded to build a predictive model using linear regression.
    I added the original code for your use and observation. (also i added the Excels i used).

3. The model performed reasonably well, with a Mean Squared Error of 3.910281e+13. This means, on average, the squared difference between the actual and predicted salaries.
   which is in the same units as my salary data .
   Also the model have R-squared value of 0.757898.
   This means that approximately 75.79% of the variance in salaries is explained by the independent variables in my model.
   This indicates that the model can effectively predict NBA player salaries based on their performance statistics.

4. One of the most interesting findings from this project was the significant impact of certain performance metrics on player salaries.
   For example, points per game (PTS) and assists per game (AST) emerged as strong predictors of salary, highlighting the importance of offensive prowess and playmaking ability in determining player value.

5. I added the plots that i created:
   * Correlation by Salaries
   * Correlation Heatmap
   * Statistiscs vs Salary

  I'm thrilled to share the results of this project and invite you to engage with me by sharing your thoughts and questions.
  If you're interested in delving deeper into the code or exploring the data further, feel free to reach out, and I'll be happy to provide more information
