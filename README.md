# League-of-legend-LOL-analysis-using-Spark

This repository contains code for performing data analysis on League of Legends (LoL) data obtained from the Riot Games API. The analysis is done using Apache Spark (PySpark) and Google Colab.

# Data Collection
The data is accessed through the Riot Games API using the Python Requests library. The following steps are involved in collecting the data:

Region and Leagues:

The data collection focuses on the European region (EUW1). Various leagues, including Challenger, Grandmaster, Master, Diamond, Platinum, Gold, Silver, Bronze, and Iron, are chosen based on the rank distribution.

Summoner Data: The summoner data is prepared by selecting the summoners from the chosen leagues. The summoner data includes information such as summoner names, rankings, and other relevant details.

Match IDs: The global IDs (PUUIDs) of the summoners are queried from the summoners API. These IDs are then used to retrieve match IDs.

Match Data: The match data is obtained using the match IDs. The data includes details about the matches, such as champions, items, and other game-related information.
To efficiently handle the data, additional information from Data Dragon is utilized. Data Dragon helps in mapping champion IDs to champion names, item IDs to item names, and obtaining champion classes.

# Data Analysis
The data analysis focuses on several requirements and provides insights into champion performance, item usage, synergy, and suggestions. The following requirements are addressed:

Champion Win, Pick, and Ban Rates: The pick rate is calculated as the number of times a champion is picked divided by the total number of champions. The win rate is calculated as the number of wins for a champion divided by the number of times the champion is picked. The ban rate is calculated as the number of bans for a champion divided by the total number of games.

Equation: Pick Rate = Number of Champions Picked / Total Number of Champions

Win Rate = Number of Champion Wins / Number of Champions Picked

Ban Rate = Number of Bans / Total Number of Games

Champion Synergy: The synergy between two champions is calculated based on the number of times they appear together in winning teams. The synergy value is calculated by dividing the number of champion pairs in the winning team by the total number of champion pairs.

Equation: Synergy = (Number of Champion Pairs in Winning Team) / (Total Number of Champion Pairs)

Item Win and Pick Rates: The win rate and pick rate for each item are calculated. The win rate is the number of wins when an item is used divided by the total number of times the item is picked. The pick rate is the total number of times the item is picked divided by the total number of items.

Equation: Win Rate = (Total Wins for Item) / (Total Picks for Item)

Pick Rate = (Total Picks for Item) / (Total Number of Items)

Item Synergy: The synergy between items and champions is calculated. For each champion, the total count of items is aggregated, both when the champion wins and overall. The synergy is then calculated by dividing the count of items when the champion wins by the total count for each item.

Equation: Synergy = (Total Items when Champion Wins) / (Total Count for Each Item)

Item Suggestion: Based on the item synergy calculated in the previous task, item suggestions are provided for two champions from different classes. The suggestion is based on the items that have the highest synergy for each champion.

Lane and Champion Synergy: The synergy between lanes and champions is calculated. For each champion, the counts of lanes are aggregated, both when the champion wins and overall.

# Results 

![image](https://github.com/ibrahimabdelaal/League-of-legend-LOL-analysis-using-Spark/assets/49596777/46f4cdcc-7e7e-4a90-82fc-933b9e2997eb)

![image](https://github.com/ibrahimabdelaal/League-of-legend-LOL-analysis-using-Spark/assets/49596777/c8c2e896-892b-46c3-b9f5-4e42ea2d542c)

![image](https://github.com/ibrahimabdelaal/League-of-legend-LOL-analysis-using-Spark/assets/49596777/b9511d64-9904-4f6a-9736-7254bd12aa61)

rest of the results can be found in the business document.





