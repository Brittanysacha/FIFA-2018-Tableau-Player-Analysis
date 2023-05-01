# Final-Project-Tableau

# Project/Goals
The goal of this project was to analyze the FIFA 2018 player dataset and create a dashboard that uncovers different features within the data. I placed a large focus on gaining insight into the trajectory of football player careers across different divisions and leagues in various areas. In addition, I also explored the relationship between a player's overall rating and their performance in various attributes such as speed, shooting, passing, and dribbling, to identify which attributes have the greatest impact on a player's overall rating.

# Process
### Step 1: Review Dataset:

The FIFA 18 database provided information on football players in the game, including their attributes and preferred positions. The data covered:

-  Player information such as wages, values, names, ages, nationalities, overall and potential ratings, league and country of play, club, and division level. 

- Attributes such as acceleration, agility, ball control, composure, finishing, heading accuracy, passing accuracy, and tackling, among others. 

- Preferred positions categorized as CAM, CB, CDM, CF, CM, LAM, LB, LCB, LCM, LDM, LF, LM, LS, LW, LWB, RAM, RB, RCB, RCM, RDM, RF, RM, RS, RW, RWB, and ST.

### Step 2: Identify which important data type is missing
There are several important data types that could be added to the FIFA 18 dataset to conduct a thorough analysis of the football ecosystem and factors contributing to a team's success and player performance. For instance, country of play, league, and division level information can help identify trends and patterns across similarly ranked leagues. This is important because comparing a lower-spending and less-established league, such as 3.Liga (the third division in Germany), to a more established, higher-spending league, such as the Premier League (the first division in England), would be inappropriate, as the two leagues differ greatly in terms of spending, resources, and overall level of competition.

Moreover, adding revenue and last season finish data could provide insights into the financial performance of teams and the success of players. Although players on the FIFA dataset are listed as individuals, their clubs' revenue and overall season finish could impact their wage and value. Additionally, data on average fan attendance and injury history could help identify the impact of external factors on a player's performance, morale, and career trajectory. Overall, incorporating these missing data types into future FIFA datasets can improve the accuracy and completeness of game analysis.

I chose to add country of play, league, and division level information to my dataset prior to building visualisations as it was readily available on the FIFA 18 website. I felt this would add significantly to what I might be able to uncover across my visualizations and would overall make them easier to understand.

### Step 3. Build at least 5 different visualizations to learn more about the dataset.

##### Player Positions

To get a better understanding of player ratings and the importance of player attributes for different positions, I broke down the 15 player position variables into some four catergories. 

This was done using a IF statement and return "Defender", "Midfielder", "Attacker", or "Goalkeeper" for each player, based on their preferred positions.

    - Defenders: CB, RB, LB, RWB, LWB
    - Midfielders: CM, CAM, LM, RM, CDM
    - Attackers: ST, LW, RW, CF
    - Goalkeeper: GK

Breaking down the 15 independent variables into 4 catergorical variables made them significantly easier to analyse. I then used these catergorical fields to take a look at the amount of different players within each position across all leagues.

![Player Position Breakdown]()

The player breakdown was not surprising. As expected, goalkeepers had the lowest numbers as there is only one goalkeeper on a team of 11 at any given time, and 3-4 are usually listed on a 26-member team sheet at the start of a season. It was also expected to see a higher number of defenders and midfielders compared to strikers. This is because strikers have a more specialized role, with teams relying on a smaller number of them to score goals and create opportunities in the attacking third of the field. On the other hand, defenders and midfielders have a wider range of responsibilities, adapting to various attacking and defending roles based on the opposition and manager's preference.


##### Top and Bottom Wages for Clubs on FIFA
I wanted to examine the football players with the highest and lowest wages across various leagues, in order to gain insight into the range of wealth among clubs in different divisions.

![Highest 10 Club Wages](https://github.com/Brittanysacha/Tableau-Project/blob/main/Images/Highest%2010%20Club%20Wages:Week%20Box%20Plot.png)

The first graph displays a box plot of the highest 10 club wages per week across the different football leagues governed by FIFA. From this chart, we can see that the mean weekly wage for these clubs is around €140,000, with a range of €4,000 to €565,000 per week. The box plot shows that the wages of these clubs are relatively tightly clustered, with a small interquartile range (IQR) of around €40,000. However, there are some outliers on the higher end, indicating that a few clubs are paying certain star players (such as Ronaldo, Suarez, and Messi) significantly more than the rest. It should be noted that all of the clubs with the highest wages are from top-flight leagues. In the case of the Premier League, all six of the clubs with the highest wages have never been relegated from the top-flight league.

![Lowest 10 Club Wages](https://github.com/Brittanysacha/Tableau-Project/blob/main/Images/Lowest%2010%20Club%20Wages:Week%20Box%20Plot.png)

On the other hand, the second graph displays a box plot of the lowest 10 club wages per week across the different football leagues governed by FIFA. From this chart, we can see that the mean weekly wage for these clubs is around €1,000, with a range of €1,000 to €2,000 per week. The box plot shows that there is no IQR, indicating that there is no variability among the lowest wages among the lowest-paying clubs. Since there are no outliers on the lower end, this likely suggests that the minimum wage a footballer would receive playing in a lower-level division would be €1,000/week and that all of these clubs are paying similar wages to their players. It should be noted that these low wages are found within all of the smaller or lower-division leagues across Europe.

##### Average Player Value and Wage by Age
The next graph I created aimed to visualize the relationship between age, player value, and wage in football, providing insights into how these variables change over time. The purpose of this graph would be to inform decisions related to player contracts, transfers, and team composition.

![Average Player Value and Wage by Age]()

The graph displays the average player value and wage per age for football (soccer) players. The horizontal axis represents age, ranging from 15 to 40 years old, while the vertical axis represents the average player value and wage in millions of pounds.

Looking at the graph, we can see that both player value and wage increase until the age of 27, where they both reach their peak. After that, both values start to decrease gradually as players get older. This trend is consistent for both values, with the player value starting higher and decreasing faster than the wage as players age.

Additionally, we can see that the gap between player value and wage increases as players get older, indicating that older players tend to be paid more relative to their market value. This could be due to factors such as experience, leadership skills, and a player's ability to perform consistently at a high level. Overall, this graph provides insight into the relationship between age, player value, and wage in football. It suggests that while younger players may have high potential, experienced and older players can bring valuable skills and leadership to a team, which may justify their higher wages.


#####

I next wanted to develop a series of charts that could provide insights into how age can impact a football player's performance (rating) and potential (room for growth). By analysing the distribution of players by age, average player rating by age, and average player potential by age, I hoped to gain a better understanding of the trajectory of a player's career and how age could affects their ability to perform at a high level.

![Distribution of Players by Age, and impact on rating and potential](https://github.com/Brittanysacha/Tableau-Project/blob/main/Images/Player%20Age%20Distribution%2C%20and%20its%20affect%20on%20wage%20and%20rating.png)

The first chart focuses on the distribution of players by age, showing that the majority of players fall between the ages of 22 and 29, with a peak between 20 and 26 years old. This suggests that these are a player's prime years, when they are likely to have the most physicality, freshness, and playing ability.

The second chart shows the average player rating by age. When looking across all divisions, ratings appear to peak at 27 years old and then decrease slightly afterwards. However, when examining the first division teams (which include the biggest and most competitive leagues in Europe), there seems to be very little decline in performance rating in relation to age. This suggests that to continue to compete at a higher level in the first division, players must maintain a higher level of performance despite the impact of aging and the overall wear and tear that football can have on the body. Interestingly, a dip begins to emerge in the average player rating around the age of 33. This could be due to a decline in physical ability or a lack of playing time due to younger teammates being in their prime. However, it can often be a time when a football player begins to consider retirement.

The third chart displays the average player potential by age, with potential peaking at 22 years old and decreasing steadily afterwards. This suggests that younger players have more room to improve and develop their skills, while older players are closer to or have already reached their peak performance level. Notably, this also suggests that if a player's overall rating is not increasing at a consistent rate by the time they are in their early 20s, they will be unlikely to develop further into a top-tier player.

Taken together, these charts suggest that age plays an important role in determining a player's overall performance, rating, and potential in football. While younger players may have a higher potential to grow, there is an element of risk that they may not develop any further or that they may not yet have fully developed enough of their skills and abilities to have an maintain overall impactful performances, leading to lower ratings. On the other hand, older players may have more experience and developed skills, leading to higher ratings, but they also have lower potential to continue growing as their careers may be coming to a close and their overall performance can start to decline. 

These insights are valuable for team managers and talent scouts when making decisions about player recruitment and development. For example, understanding the peak years for players can help teams determine when to invest in younger players with high potential versus older players with more experience and developed skills but lower potential for improvement. Additionally, analyzing the dip in player rating at age of 33 can help teams better understand the potential risks of keeping older players on the team, as they may experience a decline in physical ability and overall performance.

### Step : Detect the most important features ? Why do you think these are important? 




## Results
I chose to complete this assignment based on the FIFA 18 database. I had a few main questions I wanted to answer using my data:

##### Question 1. What is the distribution of players accross different leagues and nationalities?

##### Question 2. How do the skills and attributes of football players vary across different nationalities?

##### Question 3. How does the aggregate player value differ across various football leagues and divisions?

##### Question 4. How do the different attributes contribute to the overall rating of each player?

(Fill in which Option you chose, either 1 or 2. List the dataset you selected for the project if you selected Option 2. Also, discuss the visualizations you created, and why. For Option 2, also identify what your data question was, and how you went through the prompts.)


## Challenges 
(discuss challenges you faced in the project)

## Future Goals
(what would you do if you had more time?)
