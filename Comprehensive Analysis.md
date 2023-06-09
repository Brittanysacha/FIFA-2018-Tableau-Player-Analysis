# FIFA 2018 Player Data and Career Trajectories

# Project/Goals
The aim of this project was to analyse the FIFA 2018 game dataset and create a dashboard that uncovers different trends and patterns across leagues, countries, and players. I placed a large focus on gaining insight into the trajectory of football player careers across different divisions and leagues. Additionally, I also explored the relationship between a player's overall rating, position, and performance in relation to various attributes such as speed, shooting, passing, and dribbling.

# Process
## Step 1: Review Dataset:

The FIFA 18 database provided information on football players in the game, including their attributes and preferred positions. The data covered:

-  Player information such as wages, values, names, ages, nationalities, overall and potential ratings, league and country of play, club, and division level. 

- Attributes such as acceleration, agility, ball control, composure, finishing, heading accuracy, passing accuracy, and tackling, among others. 

- Preferred positions categorized as CAM, CB, CDM, CF, CM, LAM, LB, LCB, LCM, LDM, LF, LM, LS, LW, LWB, RAM, RB, RCB, RCM, RDM, RF, RM, RS, RW, RWB, and ST.

## Step 2: Identify which important data type is missing
There are several important data types that could be added to the FIFA 18 dataset to conduct a thorough analysis of the footballing ecosystem and factors contributing to a team success and player performance. For instance, country of play, league, and division level information are needed to help identify accurate trends and patterns across leagues and players. This is important because comparing a lower-spending and less-established league, such as 3.Liga (the third division in Germany), to a more established, higher-spending league, such as the Premier League (the first division in England), would be inappropriate, as the two leagues differ greatly in terms of spending, resources, and overall level of competition.

Moreover, adding revenue, net spend in the previous transfer window, and last season finish data could provide insights into the financial performance of teams and the success of players. Although players on the FIFA dataset are listed as individuals, their clubs' revenue and overall season finish could impact their wage and overall value. Additionally, data on average fan attendance and injury history could help identify the impact of external factors on a player's performance, morale, and career trajectory. 

I chose to manually add country of play, league, and division level information to my dataset prior to building visualisations. This information was readily available on the FIFA 18 website, but was not accessible in API or database form. Nonetheless, I felt this information  was necessary to be able to uncover accurate visualizations and would overall make the data easier to understand.

## Step 3. Build at least 5 different visualizations to learn more about the dataset.

### Visualisation One - Player Positions

To gain a better understanding of player ratings and the importance of player attributes for different positions, I broke down the 15 player position variables into some four catergories. 

This was done using a IF statement to return "Defender", "Midfielder", "Attacker", or "Goalkeeper" for each player, based on their preferred positions.

    - Defenders: CB, RB, LB, RWB, LWB
    - Midfielders: CM, CAM, LM, RM, CDM
    - Attackers: ST, LW, RW, CF
    - Goalkeeper: GK

Breaking down the 15 independent variables into 4 catergorical variables made them significantly easier to analyse. I then used these catergorical fields to take a look at the amount of different players within each position across all leagues.

![Player Position Breakdown](https://github.com/Brittanysacha/Tableau-Project/blob/main/Images/Player%20Position%20Breakdown.png)

The player breakdown was not surprising. As expected, goalkeepers had the lowest numbers as there is only one goalkeeper on a team of 11 at any given time, and 3-4 are usually listed on a 26-member team sheet at the start of a season. It was also expected to see a higher number of defenders and midfielders compared to strikers. This is because strikers have a more specialized role, with teams relying on a smaller number of them to score goals and create opportunities in the attacking third of the field. On the other hand, defenders and midfielders have a wider range of responsibilities, adapting to various attacking and defending roles based on the opposition and manager's preference.


### Visualisation 2 - Highest and Lowest Wage Bills for Clubs on FIFA
I next wanted to examine the football clubs with the highest and lowest wages across all of the leagues in FIFA, in order to gain insight into the range of wealth among clubs in different divisions.

![Highest 10 Club Wages](https://github.com/Brittanysacha/Tableau-Project/blob/main/Images/Highest%2010%20Club%20Wages:Week%20Box%20Plot.png)

The first graph displays a box plot of the highest 10 club wages per week. From this chart, we can see that the mean weekly wage for these clubs is around €140,000, with a range of €4,000 to €565,000 per week. The box plot shows that the wages of these clubs are relatively tightly clustered, with a small interquartile range (IQR) of around €40,000. However, there are some outliers on the higher end, indicating that a few clubs are paying certain star players (such as Ronaldo, Suarez, and Messi) significantly more than the rest. It should be noted that all of the clubs with the highest wages are from top-flight leagues. In the case of the Premier League, all six of the clubs with the highest wages have never been relegated from the top-flight league.

![Lowest 10 Club Wages](https://github.com/Brittanysacha/Tableau-Project/blob/main/Images/Lowest%2010%20Club%20Wages:Week%20Box%20Plot.png)

On the other hand, the second graph displays a box plot of the lowest 10 club wages per week across the different football leagues governed by FIFA. From this chart, we can see that the mean weekly wage for these clubs is around €1,000, with a range of €1,000 to €2,000 per week. The box plot shows that there is no IQR, indicating that there is no variability among the lowest wages among the lowest-paying clubs. Since there are no outliers on the lower end, this likely suggests that the minimum wage a footballer would receive playing in a lower-level division would be €1,000/week, and that similar low divison clubs are paying like wages to their players across the board. It should be noted that these low wages are found within all of the smaller or lower-division leagues across Europe.

### Visualisation 3 - Average Player Value and Wage by Age
The next graph I created two scatter plots, which aimed to visualise the relationship between age, player value, league division, and wage in football, providing insights into how these variables change over time as players aged.
The average value in Euros, as well as the average wage in Euros was the variable for clustering, with age and division level as the level of detail. The purpose of this graph would be to inform decisions related to player contracts, transfers, and team composition.

![Average Player Wage by Age](https://github.com/Brittanysacha/Tableau-Project/blob/main/Images/Player%20Wage%20by%20Age.png)

![Average Player Value by Age](https://github.com/Brittanysacha/Tableau-Project/blob/main/Images/Player%20Value%20by%20Age.png)

Looking at the graphs, we can see that both player value and wage increase until the age of 27, where they both reach their peak. After that, both values start to decrease gradually as players get older. This trend is consistent for both values, with the player value starting higher and decreasing faster than the wage as players age.

The gap between player value and wage increases as players get older. This indicates that older players are being paid more relative to their market value. This could be due to factors such as experience, leadership skills, and a player's prior proven ability to perform consistently at a high level. Overall, this graph provides insight into the relationship between age, player value, and wage in football. It suggests that while younger players may have high potential, experienced and older players can bring valuable skills and leadership to a team, which may justify their higher wages.


### Visualisation 4 - Distribution of Players by Age, and impact on rating and potential

I next wanted to develop a series of charts that could demostrate how age might impact a football player's performance (rating) and potential (room for growth). By analysing the distribution of players by age, average player rating by age, and average player potential by age, I hoped to gain a better understanding of the trajectory of a player's career and when age may begin to affect their ability to perform at a high level.

![Distribution of Players by Age, and impact on rating and potential](https://github.com/Brittanysacha/Tableau-Project/blob/main/Images/Player%20Age%20Distribution%2C%20and%20its%20affect%20on%20wage%20and%20rating.png)

The first chart focuses on the distribution of players by age, showing that the majority of players fall between the ages of 22 and 29, with a peak between 20 and 26 years old. This suggests that these are a player's prime years, when they are likely to have the most physicality, freshness, and playing ability.

The second chart shows the average player rating by age. When looking across all divisions, ratings appear to peak at 27 years old and then decrease slightly afterwards. However, when examining the first division teams (which include the biggest and most competitive leagues in Europe), there seems to be very little decline in performance rating in relation to age. This suggests that to continue to compete at a higher level in the first division, players must maintain a higher level of performance despite the impact of aging and the overall wear and tear that football can have on the body. Interestingly, a dip begins to emerge in the average player rating in the top leagues around the age of 33. This could be due to a decline in physical ability or a lack of playing time due to younger teammates being in their prime. However, it can often be a time when a football player begins to consider retirement.

The third chart displays the average player potential by age, with potential peaking at 22 years old and decreasing steadily afterwards. This suggests that although younger players have more room to improve and develop their skills, if a player's overall rating is not increasing at a consistent rate by the time they are in their early 20s, they are unlikely to develop further into a top-tier player. On the other hand, as players get older, their potential becomes lower. This is likely not due to lack of ability but due to potential having less significance as they may be closer to, have reached, or are already past their peak performance level.

Observed together, these charts suggest that age plays an important role in determining a player's overall performance, rating, and potential in football. While younger players may have a higher potential to grow, there is an element of risk that they may not develop any further or that they may not yet have fully developed enough of their skills and abilities to have an maintain overall impactful performances, leading to lower ratings. Conversely, older players may have more experience and developed skills, leading to higher ratings, but they also may be coming to a close and their overall performance can start to decline. 

These insights are valuable for team managers and talent scouts when making decisions about player recruitment and development. For example, understanding the peak years for players can help teams determine when to invest in younger players with high potential versus older players with more experience and developed skills but lower potential for improvement. Additionally, analyzing the dip in player rating at age of 33 can help teams better understand the potential risks of keeping older players on the team, as they may experience a decline in physical ability and overall performance.

### Visualisation 5 - Player Performance by Age

I finally created two visualizations to explore the relationship between player ages, attributes, and ratings for specific positions, with the purpose of identifying potential connections between age and player performance.

![Player Performance by Age - Position](https://github.com/Brittanysacha/Tableau-Project/blob/main/Images/Player%20Performance%20by%20Age%20-%20Position.png)

![Player Performance by Age - Attribute](https://github.com/Brittanysacha/Tableau-Project/blob/main/Images/Player%20Performance%20by%20Age%20-%20Attribute.png)

- Please note that full access to different variables and their resulting correlations can be found [here](https://public.tableau.com/shared/DJJ9WP584?:display_count=n&:origin=viz_share_link) 

From a bird's-eye view, it appears that as players get older, their on-field performance tends to decline. However, goalkeepers seem to be an exception to this trend, as they tend to improve with age and experience. This could be due to the fact that goalkeeper skills such as reflexes or decision-making rely heavily on experience, which comes with age.

To conduct a more in-depth analysis, I focused on the overall rating of players to see if there is a correlation with age. The correlation analysis shows that player attributes are influenced by age, with a non-linear relationship that includes a negative effect of age squared and a positive effect of age. The coefficients indicate that the effect of age on player attributes is positive but decreases with age. The intercept term is not statistically significant, indicating that it does not significantly contribute to the overall model.

These findings suggest that age is an important factor in determining player attributes and overall performance, and that the relationship between age and player attributes is complex and non-linear. However, it's important to note that while the given equation and coefficients provide evidence of a significant relationship between age and player attributes, they don't necessarily imply causality. Other factors such as training, diet, and lifestyle choices may also influence player attributes and overall performance.

Overall this sort of data can be useful for player recruitment and contract negotiations. Teams need to consider age-related performance trends for different positions to build a well-balanced and sustainable roster. For instance, younger players may be more suitable for positions that require physical strength and speed, while older players may be better suited for positions that demand experience and strategic thinking. By analyzing age-related performance trends, teams can also identify potential bargains in the transfer market, as older players who are still performing at a high level may be undervalued due to their age. Investing in younger players with high potential may also prove to be a wise long-term strategy. Overall, teams must consider age as a significant factor when making decisions related to recruitment, contract negotiations, and squad management.

# Results
Based on my findings within the FIFA 18 dataset in my earlier visualisations,  I had a few further questions that I wanted to answer using my data.

## Question 1. What is the distribution of players accross different leagues and nationalities in FIFA 18?

The FIFA 18 dataset contains information on over 17,500 players from various leagues and countries. I wanted to find a way to visualise my data through interactive maps to showcase the distribution of players across different leagues and nationalities.

The league visualisation showcases that the highest concentration of players from the different leagues are in Europe, with countries such as England, Italy, Germany, France, and Spain having between 2-4 divisions represented in the game. Among these leagues, the lower division leagues in Europe appear to have the largest number of players. This could suggest that the top-flight leagues are more competitive. Although there are some larger groups of players across leagues in South America such as Colombia and Brazil, it is noticeable that non-European leagues have less of a presence across the FIFA 18 game. This could be due to the popularity of European League teams, with several teams having a large established overseas presence, as well as a long club history.

Regarding nationality, the map shows that the majority of players in FIFA 18 also originate from European countries such as Spain, Germany, France, and England, followed by South American countries like Brazil and Argentina. Nonetheless, there is a much larger representation of different nationalities with footballers originating from countries whose leagues were not included within the game. When looking further into nationality via different leagues, the visualisation further highlights how players in second division leagues are more likely to originate from that same country. This could be associated with lower skilled players receiving lower wages among lower division leagues, which may make it more difficult to move around freely.


## Question 2. How do the skills and attributes of football players vary across different nationalities?

I wanted to create a second set of map visualisations in order to gain a better understanding of how various attributes of football players, such as dribbling, shooting, passing, and physicality, can vary across nationalities. Since certain regions in Europe and South America have more than one division and, thus, a diverse range of players, I deemed it necessary to not only consider the overall average but also to look at the average of the top 10 players from each region.

Examining specific player attributes from different regions can provide insights into how nationalities approach the game of football. For instance, if a specific nationality has a higher average rating for dribbling, it may imply that this is a focal point in their training and player development. Conversely, if a particular nationality has a higher average rating for physical attributes, it may indicate that physicality is a crucial aspect of their playing style.

The visualisations revealed some interesting findings. For example:

- The South American region showed top players with excellent dribbling, shooting, and physical attributes. Specifically, Argentina had the highest average rating for dribbling among South American countries, while Brazil had players with the highest average rating for shooting.

- Players from African countries had higher average ratings for physicality attributes related to overall endurance such as strength and stamina, as well as physical attributes related to movement and control such as acceleration, sprint speed, and agility.

- Finally, European players had higher average ratings for passing, dribbling, and defending. The data shows that countries such as Spain, Germany, and Italy have high average ratings for passing, while countries such as Belgium, France, and Portugal have high average ratings for dribbling. As for defending, countries such as Italy, England, and Germany tend to have higher average ratings.

Overall, variations in the skills and attributes of football players across different nationalities could be attributed to a combination of cultural and environmental factors, as well as differences in training and development programmes. Nonetheless, it is important to note that these are general trends and that individual players' skills vary greatly across regions. This visualisation could gain better accuracy if the average player attributes were further broken down into separate maps based on division level (1st, 2nd, 3rd, 4th), or team ranking, which is an official feature by FIFA that ranks teams based on their performance in international competitions over the past four years.

## Question 3. How does the aggregate player value differ across various football leagues and divisions?
I next created an interactive series of visualizations to better understand the lack of parity across football leagues and divisions within FIFA. They were broken down into first division teams, second division teams, and then third and fourth division teams. It is important to note that Germany and England were the only countries to have more than two divisions represented in FIFA.

After reviewing the aggregate player values across leagues and divisions, it became apparent that the aggregate player values differed significantly not just across various football leagues and divisions but also within leagues and divisions. The leagues with the highest aggregate player values are the five biggest leagues in Europe:

- English Premier League: approximately €5.9 billion,
- Spanish La Liga: approximately €5.5 billion,
- German Bundesliga: approximately €4.1 billion,
- Italian Serie A: approximately €4 billion,
- French Ligue 1: approximately €3.1 billion.

Looking at the individual clubs within the English Premier League, there is evident disparity across the league. The top six clubs (Manchester United, Manchester City, Liverpool, Arsenal, Chelsea, and Tottenham) account for a significant portion of the league's total player value at a combined value of approximately €3.34 billion, which is 56.4% of the aggregate league value. In contrast, the bottom six clubs (Huddersfield Town, Brighton & Hove Albion, Burnley, Bournemouth, West Bromwich Albion, and Swansea City) have a combined player value of approximately €0.77 billion, which is 13.02% of the aggregate league value. The club with the highest player value in the league is Chelsea at approximately €673 million, while the club with the lowest aggregate league value is Huddersfield Town at approximately €87.6 million. There are even more significant differences in aggregate player value between the top-tier leagues and the lower divisions in similar regions. Taking the English leagues as an example, the English Premier League's total player value is more than ten times the value of the EFL League Two (the fourth tier of English football).

Overall, this once again signifies why different divisions must be taken into account when trying to analyse and find trends and patterns across FIFA blubs and leagues. A further step to gain further insight from this information would be to look at the correlation between league placement and player value or wages. I anticipate that those with higher team values would perform significantly better, although it would also be interesting to observe differences among similarly valued teams.

## Question 4. How do the different attributes contribute to the overall rating of each player?
The final visualisation I wanted to create was a heat map, that could determine the presence of certain attributrs within certain positions. A few examples of some highlights that can be drawnfrom the data are included below:

- Strikers (ST) need attributes such as strength, positioning, finishing, and shot power. This indicates that the traits required from players best suited to be a striker include the ability to score goals, hold up play and be physical with defenders.

- Left wingers (LW) excel in attributes such as sprint speed, dribbling and ball control, which make them highly suitable for playing on the outside of the pitch and controlling the ball. Furthermore, high ratings in finishing, shot power and long shots indicate that they are on average strong scorers. On the downside, LWs typically have lower ratings in defensive attributes such as marking, standing tackle and sliding tackle, which suggests that they may not be suitable for defensive positions.

- Right backs (RB) need to have high stamina, sprint speed and strength to keep up with opponents on the wing. Defensively, they must possess excellent ability to perform standing tackles, interceptions and marking. Attacking-wise, good crossing, short passing and dribbling abilities are crucial for providing crosses and maintaining possession. This sort of player should also have strong vision and composure to make strategic decisions, and quick reactions which are necessary for rapid responses to attacks during a game.

- Goalkeepers (GK) require unique attributes for their position like handling, diving, reflexes, positioning and kicking to stop and distribute the ball. However, they also require vision and composure to make for strategic decisions and remain calm under immense pressure. Physical attributes like strength, jumping, balance and agility are important for reaching, jumping and moving around the goal area.

- Centre backs (CB) must have high levels of composure, aggression and ball control . Composure helps them stay calm under pressure, aggression gives them an edge in winning the ball, and ball control allows for effective distribution from the backline. Other attributes such as dribbling, crossing and curve may be useful for attacking play, while balance, agility and acceleration can help with quick movement and keeping up with opponents.

- Central midfielders (CM) typically have higher stamina, short passing and long passing, as they need to be able to run up and down the middle of the field and distribute the ball effectively to the back line and into the attacking third. Standing tackles, sprint speed and reactions are important defensive attributes for a CM, while shot power and long shots are useful for contributing to the team's attack.

Further examples can be obtained by analyzing the heat map data, which provides valuable insights into the specific areas that current players in certain postions excel at. By identifying these key areas, coaches and trainers can help players improve their skills and work towards mastering the position they wish to play in. 

Moreover, heat map analysis can be a useful tool for scouts and managers when assessing potential new recruits or deciding on player positions within their team. By identifying a player's strengths and weaknesses based on their heat map data, coaches can guide them towards roles that best suit their skill set, or alternatively, help them develop the attributes needed to succeed in a different position. This can lead to a more effective use of resources and better team performance overall.

 Full access to to the charts discussed in the results can be found [here](https://public.tableau.com/shared/DJJ9WP584?:display_count=n&:origin=viz_share_link). 


# Challenges 
I did not have full access to all the data available on the FIFA 18 website in the FIFA 18 dataset. As a result, I manually added team information such as their league, country, and division. If I had relied only on readily available data, my results would have been inaccurate due to the large differences across divisions in terms of spending, resources, player ratings, and overall level of competition.

Furthermore, I encountered a slight issue while trying to format my map within Tableau. To separate the different regions of the UK and be able to look at all the data, I had to use a dual axis map. Without this, the default setting for the United Kingdom was to refer only to English data. This would not only have created inaccuracy and led to missing data, but it could also have potentially offended certain people.

# Future Goals
With more time, there are several things I would have liked to accomplish in this project. Firstly, I would have blended more of my data sources together into a more cohesive dashboard that operates more like an interactive infographic rather than a story with various components. Additionally, I would have liked to set a categorical parameter and calculation for my attributes similarly to how I set one for my positions. This would enable me to run my position categories against attribute categories and determine if there are any correlations between them.

I would have also liked to find information about club revenue from the prior fiscal year, net spend in the previous transfer window, and the previous season's finish to determine the impact of spending and revenue generation on different clubs. Particularly, as revenue, available funds, and previous season finishes are features accessible from FIFA 18.

In terms of future research, conducting a longitudinal study on factors such as spending, resources, player ratings, and FIFA team rankings would be interesting. This type of study would identify any trends or patterns over time and provide a more comprehensive understanding of the relationship between spending and success in football.
