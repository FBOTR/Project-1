# Baseball Regression

This program takes historical data from the last 20 years across the league, with special attention paid to the Yankees, to find the correlation between different statistics and their relation to the win percentage in a given season.

Based on this analysis, we can gain insights into what factors contribute to a team's success and identify the Yankees' strengths that lead to their victories. This data can then be utilized to create a metric and subsequently run through a Monte Carlo simulation to predict the win percentage based on correlated statistics.

**Step 1:** Download `Data_all_teams_Adv+Str.csv` (obtained from Fangraphs.com).

**Step 2:** Open the Streamlined Regression Dynamic Matlab file, input the path for `Data_all_teams_Adv+Str.csv`, and execute the code. This code reveals which baseball statistics are highly correlated with the win percentage for all teams in MLB since 2002. We also conducted a separate analysis specifically for the New York Yankees.

- **Key findings:**
The Yankees heavily rely on offense to win games, in contrast to the rest of the league, which tends to prioritize pitching and defense.

**Step 3:** Download `DataforMonte.csv` (similar data to Step 1 but includes columns for runs scored per game and runs given up per game for Monte Carlo simulation).

**Step 4:** Open the Monte Carlo for Win% Matlab file, input the path for `DataforMonte.csv`, and execute the code. (Input parameters for the Monte Carlo are on line 16). The results display the mean win percentage of the Yankees and the standard deviation.

- **Note:**
We utilize Prof. Kerry Whisnant's Win chance equation (seen in the Beyond_Pythagorean_expectation PDF). In our function, you can input the Yankees' current runs scored, runs given up, total games played, and simulations. The function then employs Prof. Whisnant's win chance equation for both the Yankees and their opponents. The opponent's statistics are obtained from random, normal variables from a distribution described by MLB's mean and standard deviation for those statistics.

- **How is Win% calculated?**
The Monte Carlo method considers the total games played and calculates the remaining games in the season. It then computes the win chance of the Yankees and their opponents. If the Yankees' win chance is greater, it counts as a win for the Yankees. This process iterates through a for loop for the remaining games, simulating the remainder of the season and calculating the final win percentage for that season. An outer loop runs the specified number of simulations to simulate multiple seasons. Finally, the function outputs the mean and standard deviation of the Yankees' win percentage.

**Step 5:** 
These results can be used to make informed predictions about how the Yankees will perform based on their preseason or early-season statistics.

![Screen Recording 2024-03-23 at 10 49 59 PM](https://github.com/FBOTR/Project-1/assets/162471452/f2aada81-c2ed-4b65-8224-72d1fccd4557)
