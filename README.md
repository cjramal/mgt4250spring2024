# MGT4250 Spring 2024 Course Project
Authors: CJ Ramalho, cramalho@elon.edu, Mason Esworthy, jesworthy6@elon.edu

## Project Description
Visualization App Link: https://public.tableau.com/views/MGT4250CJRamalhoMasonEsworthy/A-Figure2?:language=en-US&:sid=&:display_count=n&:origin=viz_share_link

This repository is for the class project of MGT 4250 at Elon University

### Questions of Interest
- Question 1: What statistical metrics have the greatest impact on a soccer team's performance (specifically in the Premier League)? 
- Question 2: How can statistics be used to increase soccer team performance?
- Question 3: What indicators are correlated with team success? What indicators lead to over performing or underperforming?
- Question 4: How can analytics be used to adjust tactics to better fit player profiles?

### Importance
- Reason 1: These questions are important because clubs face a plethora of financial and business issues behind the scenes if they are failing to perform in games. It is estimated that clubs take revenue hits of about 85-100 million euros (City AM) if they are relegated (demoted) from the premier league, which is a clear business issue that has real implications on people’s jobs and the business strength of a club. Conversely, teams that perform well or are promoted into the premier league can expect revenue increases of around $210 million on average (Yahoo Sports). Thus, it is obvious that soccer is not just a game - the wellbeing of the organization relies on teams performing well. It is critical from a business standpoint that analytics are employed to address issues and guide a team towards success - first on the pitch, and secondly in the office. 

- Reason 2: Better understanding what metrics are leading to a team preforming / underpreforming will allow managers to fine tune training and acquire players that fit specific profiles to improve overall preformance. Breaking down our dashboard by attacking, passing, and defending is intended to address this.
  
- Reason 3: Elon University could benefit from this type of data visualization because it will allow them to make informed decisions on the types of profiles they want to scout for our University soccer team. Our soccer team is one of the most popular campus involvement activites at the school, and serves as a big draw of the attention of students. A better soccer team means happier students, and happier students means better enrollment.

## Data Description
### Access & Download Data:

**Data Source is included in GitHub repository (premstats.xlsx).**
**Data was extracted using the following means: **

**Source Webpage:** https://fbref.com/en/comps/9/Premier-League-Stats

- On the linked page, click “previous season” under the title banner to access data for the 2022-2023 season, which we deemed more appropriate - the 23/24 season is ongoing.
- We then scraped the data into an excel spreadsheet using a downloaded HTML of the webpage and power query. This means, these tables and the dataset used is not available for direct download on the website. It will be provided with submission of our final project. Essentially, we combined columns from different tables that we thought would be helpful indicators or visualization tools. 


### Data Types & Column Descriptions (All for 22/23 season)
- Team (String): Team Name
- League Position (Integer): Final League Position for 22/23 Season
- Average Age (Integer): Average Age of all players who started at some point in season
- Average Possession (Percentage): Average possession across all games
- Goals (Integer): Total goals
- Goals Against (Integer): Total goals against
- Goals Against per 90 (Float): Goals against per 90 minutes across all games (total goals against divded by total minutes in a season)
- Shots on Target Against (Integer): Total SoTA against
- Non Pentalty Goals (Integer): Total non penalty goals in all games
- Yellow Cards (Integer): total Yellow cards
- Red Cards (Integer): Total Red Cards
- Expected Goals (Float): Total Expected Goals
- Expected Assisted Goals (Float): Total Expected Goals coming directly from an assist
- Progressive Carries (Integer): Total progressive carries (dribbles)
- Progressive Passses (Integer): Total progressive passes (transitions play from neutral to attacking or defending to neutral)
- Goals per 90 (Float): Average goals per 90 minutes
- Assists per 90 (Float): Average assists per 90 minutes
- etc...

Acronyms:
- xG: Expected Goals
- npxG: Non-penalty Expected Goals
- xA: Expected Assists
- xGA: Expected Goals Against
- SoT: Shots on Target

Notes:
- We have also included in our dashboards a premier league table used to filter the visualizations by certain teams.

## Interpreting Visualizations
### Dashboard 1: Attacking
#### Attacking Dashboard Figure 1.1: Goals Scored vs Expected Goals
<img width="883" alt="Screen Shot 2024-04-24 at 2 06 53 PM" src="https://github.com/cjramal/mgt4250spring2024/assets/152424835/ae4f40f1-7ceb-4f72-bd3b-085f3015a9b3">

#### How does figure 1.1 answer our question?
  Figure 1 is a reflection of goals scored versus expected goals. The rows (teams) are sorted by league position (ascending from bottom to top). The top team in the league is     Manchester City (1st) whilst the bottom team in the league is Southampton (20th).
The figure reflects whether a team outperformed or underperformed their total expected goals for the season. We took their total goals scored across the season and subtracted total expected goals (a metric that uses analytics to predict the outcomes of chances and assign an “xG” value). Using this visualization, we can immediately see that the top two teams in the league both outperformed their xG by over 10 goals - meaning, they scored 10 or more goals than analytics had predicted based on their chance creation. Conversely, we see that Everton underperformed their total expected goals by ~13, meaning they scored 13 goals fewer across the season than expected. This is an extremely important visualization for determining the attacking effectiveness of a team. Overpreforming xG can either mean that the level of goal scoring is not sustainable over the long run - the team is scoring more than they should on average across the season. Or, it can mean that they have a very effective striker or attacker that they cannot lose.
  On the other hand, teams that are underperforming their xG should probably look to acquire a new striker or goal scoring threat. If they are failing to score at the levels they are predicted to based on their chances, that means that they are missing easy shots or that their attackers are not doing their job in front of the net. Thus, we can recommend such teams to invest in attacking coaches or purchase a striker known for being clinical in the box to bridge the gap between expected goals and goals scored. We can analyze a lot from this graph, but more on this in the final project. 

#### Attacking Dashboard Figure 1.2: Average Shot Distance vs Expected Goals
<img width="671" alt="Screen Shot 2024-04-24 at 2 06 37 PM" src="https://github.com/cjramal/mgt4250spring2024/assets/152424835/27444b84-8e76-4567-85e2-9b51192dba53">

#### How does figure 1.2 answer our question?
Figure 2 is a reflection of expected goals versus average shot distance in meters. This is a visualization that might be included in our attacking or chance conversion dashboard. The information for the trend line can also be included in the final project. 
This visualization is helpful for identifying the average shot distance of high scoring teams. We can see that the top performing teams in terms of expected goals, ex Manchester City, Liverpool, Arsenal, etc who all finished in the top 6 of the league, also had a relatively low average shot distance. We can identify a correlation between low average shot distance and expected goals. This tells us that teams should encourage players to not take shots from distance, but rather wait for a better opportunity to score from a closer distance. All too often, lower performing teams waste possession by firing a shot from distance out of frustration of their inability to break a top performing defensive line. However, this graph tells us that shots from longer distances, over time, will lead to lower expected goals.

### Dashboard 2: Passing
#### Passing Dashboard Figure 2.1: Progressive Passes & Expected Assists
<img width="882" alt="Screen Shot 2024-04-24 at 2 06 44 PM" src="https://github.com/cjramal/mgt4250spring2024/assets/152424835/bf54e445-fb53-49ef-8559-cfc4b1b82ea3">

#### How does figure 2.1 answer our question?
Figure 1 is a reflection of expected assists versus progressive passes. The teams are colored by total progressive passes (darker equates to more progressive passes across the season) The rows (teams) are sorted by league position (ascending from bottom to top). The top team in the league is Manchester City (1st) whilst the bottom team in the league is Southampton (20th).
This is an example of a figure that might be included in our “passing/midfield” dashboard to visualize chance creation. For some context, progressive passes are passes into the final third or passes that transition play from defensive or neutral to attacking. Here, we can see that teams with more expected assists also have more progressive passes. This visualization is helpful for explaining the importance of progressive passes: it is crucial that a team invest in players with a high progressive passes per 90, since this directly correlates with chance creation and expected assists. 
	We can also use this visualization to identify outliers - ex, Chelsea. Chelsea were relatively strong with progressive passes, but did not have a lot of expected assists. This indicates that while the team is good at transitioning play into the attack, they struggle with converting attacking opportunities or possession in the final third into actual chances or shots. Chelsea sat at 12th in the table - not ideal for a team of their qualifications. Looking into these strengths and weaknesses would help the club with player selection and coaching styles immensely. 

#### Passing Dashboard Figure 2.2: Total Passes Breakdown by Distance
<img width="876" alt="Screen Shot 2024-04-24 at 2 06 19 PM" src="https://github.com/cjramal/mgt4250spring2024/assets/152424835/5163d287-71b4-4997-91d4-0d44cc229a98">

#### How does figure 2.2 answer our question?
Figure 2.2 allows us to visualize how the top teams compare to the lower teams in terms of the total number of passes they completed, as well as the distance of each of these passes. In the graph, we have a stacked bar chart sorted from left to right by table position, featuring total passes broken down by three categories: short passes, medium passes, and long passes. Analyzing this graph will allow managers to have better informed decisions about which pass types are most important, how total passes effects preformance, and what profile of player to purchase if one pass type is lacking (ex, purchase a deep lying playmaker if total pass count is not up to par, or an attacking fullback for more long/medium passes).
Now, to analyze the visualization, we see that having more total passes is correlated with better team success. Manchester City (1st) had the most total passes, while Nottingham Forrest (16th) had the least total passes. It is also interesting to observe outliers - ex, Brentford, who had relatively low total passes but finished 9th. For example, Leicester City (18th) had more total passes than Brentford. However, they had less long passes, which could indicate that Leicester City should invest in a player with a high long pass or progressive pass per 90 statistic. It appears that might be their issue: although they are completeing alot of passes, most are medium to short and thus don't generate much dynamic play. These are the types of conclusions we can draw from such a visualization to continue to inform managers about important in game statistics that lead to success. 

### Dashboard 3: Defending
#### Defending Dashboard Figure 3.1: Goals Against per 90 versus Average Possession
<img width="780" alt="Screen Shot 2024-05-07 at 5 05 58 PM" src="https://github.com/cjramal/mgt4250spring2024/assets/152424835/fd774538-d191-4389-8cbd-416348f6e93a">

#### How does figure 3.1 answer our question?
This figure is a representation of how important possession is in the modern game. There is the timeless saying that if the team doesn't have the ball, they can't score. Maintaining high average possession percentages per game will ensure that a team does not concede. It is crucial that managers look at average possession to identify where problems lie in their starting lineup. This can inform them on purchasing players with higher pass completion or on teams that play a possession based game. 
From the graph, we can see that the teams with the lowest possession per 90 also conceded the most goals. Manchester City (1st), the team with the highest average possession (64.70%), also conceded the least goals per 90 (0.87), reflecting the importance of investing in coaches and players that facilitate a possession based playstyle. Keeping the ball is crucial to denying opponents the opportunity to score.

## Discussion & Summary
### Related Article 
_Article Link: https://analyisport.com/insights/how-is-data-used-in-the-premier-league/_

This article discuesses how AI and Big data is changing how soccer works. There has been more and more debate around using AI in place of managers or assistant managers because of their above-human capacity for analyzing the game. The article discusses how the Premier League has seen a huge rise in the use of data science, making analysis and predictive modeling a must for match analysis. Clubs are using advanced football data API feeds to match talent to top players. Clubs like Liverpool have been known to hire people with PhD's in Research for their data team. Ian Graham, the director of Research at Liverpool, has used statistics continously to help manager Jurgen Klopp with decision making. Liverpool had great success putting this much focus on analytics over the past couple of years, as any Premier League fan will know. 

### Generative AI
_AI Used: ChatGPT_

**Question: What statistical/analytical metrics have the greatest impact on a soccer team's performance (specifically in the Premier League)?**

**AI Answer:**

In soccer, especially in a competitive league like the English Premier League, several statistical metrics are commonly analyzed to gauge and potentially predict a team's performance. Here are some of the key metrics:

1. Goals Scored and Goals Conceded: These are basic but crucial metrics. The difference between them, known as goal differential, is often a clear indicator of a team's performance over the season. Teams with a high goal differential usually finish higher in the standings.
2. Expected Goals (xG): This metric estimates the number of goals a team should have scored based on the quality of the shots they took. It provides insight into both offensive effectiveness and luck.
3. Expected Goals Against (xGA): Similar to xG but for defense, it measures the quality of shots the team allowed. A lower xGA suggests a stronger defense.
4. Possession Percentage: While possession itself is not always directly correlated with winning, it indicates a team's ability to control the game's pace and often correlates with other indicators of dominance in a match.
5. Pass Accuracy: This metric reflects how well a team retains possession and can indicate the quality of a team’s playing style. High pass accuracy in key areas can be crucial, especially in breaking down well-organized defenses.
6. Shots on Target: This is a direct measure of a team's attacking threat. More shots on target typically indicate more scoring opportunities being created.
7. Player-Specific Metrics: Individual performances, such as key passes, dribbles, tackles, and interceptions, can also be critical, especially when evaluating the impact of specific players on a team’s overall performance.

Teams and analysts often use a combination of these metrics, among others, to form comprehensive strategies and evaluate both short-term outcomes and long-term performance trends.

**Question: How can analytics/statistics be used to increase soccer team performance?**

**AI Answer:**

Statistics play a crucial role in modern soccer, helping teams enhance their performance through detailed analysis and strategic implementation. Here’s how statistical analysis can be effectively used to boost a team's performance:

1. Tactical Adjustments: By analyzing match data, coaches can make informed tactical adjustments. For example, a team that struggles to maintain possession might benefit from a change in formation or passing strategy. Conversely, statistics can reveal an opponent's weaknesses, allowing a team to exploit them strategically.
2. Player Performance and Development: Detailed player statistics (like passing accuracy, tackles, xG, and more) allow coaches to identify strengths and weaknesses in individual players. This information can guide personalized training programs, improve player performance, and inform decisions about starting lineups and substitutions.
3. Recruitment: Data analytics are increasingly used in scouting and recruitment. By analyzing performance data across different leagues and competitions, teams can identify and recruit players who match their tactical needs and have the potential to excel within the team's style of play.
4. Injury Prevention and Management: Statistical tools can monitor players’ physical loads and stress levels during games and training. This data helps in managing player fitness and can reduce the risk of injuries by suggesting optimal rest periods and identifying potential overload situations.
5. Set-Piece Optimization: Statistics can identify patterns and success rates related to set-pieces (corners, free kicks, and penalties). Teams can use this information to optimize their set-piece strategies, both defensively and offensively.
6. Game Strategy: By analyzing in-game statistics like possession, shot locations, and player movements, teams can adjust their strategies in real-time. Coaches can make more informed decisions during the game, such as adjusting the team's attacking focus or reinforcing defense.
7. Performance Trends: Longitudinal statistical analysis can reveal performance trends, helping teams understand their progress over time. This can influence broader strategies, such as during the off-season or in preparation for specific competitions.

In essence, integrating statistical analysis in soccer not only enhances a team's performance on the pitch but also supports broader managerial and strategic decisions, ultimately fostering a more scientific approach to the sport.

### Conclusion Discussion

Our visualizations do align very well with the article and the chat gpt responses. They answer our question in a very similar way, reflecting the importance of the same metrics that we found to be helpful in our visualizations. Firstly, ChatGPT solidified that metrics like expected goals, expected goals against, and possession percentage are important for determining premier league success. Our visualizations used all of these metrics and more to draw our conclusions. ChatGPT also reiterated our point about how statistics can inform game strategy, tactical adjustments, and recruitment (the purchasing of players, as we have continously referenced in visualization analysis).

Secondly, the article aligns with our visualizations because it dicusses the growing trend of using analytics in the premier league and how it is helping teams become more successful. It connects to our questions because it further reiterates how important analytics is in the modern game using a real case study, Liverpool, to support our rational for creating the visualizations. Liverpool has invested immensely in hiring competent analytic minds to lead their research team, and it has paid off.


