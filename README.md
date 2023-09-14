# Moneyball
## __1.0 Business Problem__
> The data and the description has been adapted from (https://en.wikipedia.org/wiki/Moneyball) and Udemy...
> 
 Following the 2001 MLB season, the Oakland Athletics saw the departure of three key players (Johnny Damon, Jason Isringhausen, and 2000 Al MVP Jason Giambi).  That season they finished second in the American League with a record of 102-60, but lost to the 3 games to 2 against the New York Yankeees in the American League Division Series.  Looking to repeat their success and compete against the New York Yankees, they would need to find a way to replace the key players lost.  Limited to a 44 million dollar salary, how can the Oakland Athletics bring in enough talent to compare to the New York Yankees 125 million dollar payroll?  Using rigorous statistical analysis had demonstrated that on-base percentage and slugging percentage are better indicators of offensive success, and the Athletics became convinced that these qualities were cheaper to obtain on the open market than more historically valued qualities such as speed and contact.  The goal is to find undervalued players that fulfill the new Athletics criteria for offensive success with a 13 million dolllar salary cap.

## 2.0 Business Assumption
The strategy to use ggplot and Rstudio provides the Oakland Athletics with insight into finding undervalued players in the market to replace Jason Giambi, Johnny Damon, and Jason Isringhausen while staying under the 13 million dollar salary cap.

## 3.0 Solution Strategy
My solution to solve this problem will be the development of a data science project. This project will utilize a variety of databases, and analyzed using ggplot and R Studio.

#### Step 01.Data Description: 
In this first section the data will be aggregated and studied.  Data will be used from Sean Lahaman's website, a very useful source for baseball statistics.  The data can be found in tags. Each player is assigned a unique number (playerID).  All of the information relating to that player is tagged with his playerID.  The playerIDs are linked to names and birthdates in the MASTER table.  Along with the master table the database is comprised of the following main tables: batting statistics, pitching, fielding statistics.

#### Step 02. Feature Engineering:
To determmine the value of the player we look at several statistics.  The batting average, on base percentage, and slugging percentage that will be calculated in order to improve the model and exploratory data analysis.  Each will have its own unique column.  Not only do we have to know the best players, but the most undervalued players, meaning we will also need salary information.

#### Step 03. Data Filtering:
Using the summary function we can see that we have statistics about the playerIDs, yearIDs, stints, teamIDs, etc... Its important to note that the statistics date back to 1871, the excess data from needs to be trimmed in order to merge the salary and batting data.  Since we have players playing multiple years, we'll have repetitions of playerIDs for multiple years, meaning we want to merge on both players and years.

#### Step 04. Data Preparation: 
In the fourth section, the data will be prepared to be analyzed against the players being lost.  We'll need to isolate the statistics of the players we want to replace and only concern ourselves with the data from the previous year of player output.  

#### Step 03. Data Analysis:
The fifth step would be the find the replacement players for the three key players lost under three constraints: the total combined salary of the three players can not exceed 15 million dollars, the combined number of At Bats (AB) needs to be equal to or greater than the lost players, their mean on base percentage had to equal to or greater than the mean on base percentage of the lost players.


