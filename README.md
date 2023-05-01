# Final-Project-Tableau

# Project/Goals
(fill in your description and goals here)

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

##### Average Player Value and Wage by Age
The next graph I created aimed to visualize the relationship between age, player value, and wage in football, providing insights into how these variables change over time. The purpose of this graph would be to inform decisions related to player contracts, transfers, and team composition.

![Average Player Value and Wage by Age]()

The graph displays the average player value and wage per age for football (soccer) players. The horizontal axis represents age, ranging from 15 to 40 years old, while the vertical axis represents the average player value and wage in millions of pounds.

Looking at the graph, we can see that both player value and wage increase until the age of 27, where they both reach their peak. After that, both values start to decrease gradually as players get older. This trend is consistent for both values, with the player value starting higher and decreasing faster than the wage as players age.

Additionally, we can see that the gap between player value and wage increases as players get older, indicating that older players tend to be paid more relative to their market value. This could be due to factors such as experience, leadership skills, and a player's ability to perform consistently at a high level. Overall, this graph provides insight into the relationship between age, player value, and wage in football. It suggests that while younger players may have high potential, experienced and older players can bring valuable skills and leadership to a team, which may justify their higher wages.

##### Top and Bottom 

- Physical Attributes - This group includes Ball Control, Dribbling, Acceleration, Sprint Speed, Agility, and Balance. These attributes determine a player's ability to move with and without the ball, as well as their balance and control while dribbling.

- Shooting Attributes - This group includes Finishing, Shot Power, Long Shots, Volleys, Curve, and Free Kick Accuracy. These attributes determine a player's ability to shoot accurately and with power, as well as their ability to score from long distances and set pieces.

- Passing Attributes - This group includes Long Passing, Short Passing, Vision, Crossing, Penalties, and Composure. These attributes determine a player's ability to pass accurately and with vision, as well as their composure under pressure.

- Physicality Attributes - This group includes Heading Accuracy, Jumping, Strength, Stamina, Aggression, and Interceptions. These attributes determine a player's physical strength, endurance, and ability to win aerial duels and intercept passes.

- Defending Attributes - This group includes Marking, Sliding Tackle, and Standing Tackle. These attributes determine a player's ability to defend and tackle effectively.

- Goalkeeping Attributes - This group includes GK Positioning, GK Reflexes, Special, Reactions, and Positioning. These attributes determine a goalkeeper's ability to position themselves well, make reflex saves, react quickly, and handle special situations such as corners and free kicks.

I also created three map visualisations to gain a more comprehensive understanding of the distribution of where footballers were playing, nationalities, and homegrown players across different leagues in FIFA 18. There maps were based on three different criteria: 

- 1. The breakdown of different football players in the game across different leagues to identify regions with the highest concentration of players and leagues. 

- 2. The nationalities of the players and their representation across FIFA 18. 

- 3. The number of homegrown players within FIFA, which refers to players actively playing in the region where they were born. 

The purpose of this was to see if any patterns or trends emerged in the distribution of football players across FIFA 18. 

I further created a 
### Step : Detect the most important features ? Why do you think these are important? 




## Results
I chose to complete this assignment based on the FIFA 18 database. I had a few main questions I wanted to answer using my data:

1. What is the correlation between player attributes (such as ball control, dribbling, acceleration, sprint speed, etc.) and overall player value for each position?

2. How do player wages in Euros vary across leagues and divisions? 
    - Which clubs pay the highest wages and have the highest player values?
    - Which player positions and statistics are associated with a cost of >= 10% of the team budget?

(Fill in which Option you chose, either 1 or 2. List the dataset you selected for the project if you selected Option 2. Also, discuss the visualizations you created, and why. For Option 2, also identify what your data question was, and how you went through the prompts.)


## Challenges 
(discuss challenges you faced in the project)

## Future Goals
(what would you do if you had more time?)
