Overview

The NBA consists of 30 teams, over 400 players, and generating nearly 15 billion dollars in the 2025–2026 season alone. With the fight to win the championship each year to bring in more money for each team, the entire league is very statistically dependent. As the game has continued to grow with modern technology so has the stats. With so many numbers pouring in nightly it can be difficult to see which statistics actually matter and which ones may not contribute as much.
The goal of this project is to analyze which statistics best predict a good season. Our team will be diving into a variety of offensive and defensive stats that we believe are the most important contributions to a team's success in winning games. With that being said we will be using three different datasets which we will integrate together to find the answer to this question. These datasets will be sourced directly from NBA official statistics repositories and APIs that have scraped the NBA databases, meaning the data will come from trustworthy sources within the league.
These datasets contain statistics such as points per game (PPG), field goals made (FGM), and three-point percentage (3P%), along with advanced statistics such as offensive rating (ORtg) and effective field goal percentage (eFG%). To answer our research question we will perform data cleaning and analysis using Python packages like pandas. We will then use feature engineering and visualizations to identify which statistics correlate most with a successful NBA season.

Team
For this project, everyone will contribute equally. We will meet up weekly to work on the project together and ensure that all steps to complete the project are done in a group, and that any issues encountered are resolved with everyone’s help.

Research or Business Questions
	The primary research question for this project is: which team statistics most strongly predict winning seasons in the NBA? Overall, this question focuses on identifying which statistical metrics are most strongly associated with successful team performance. To support this primary research, other related sub-question will also be explored. For instance: which offensive statistics (e.g. points per game, assists, and field goal percentage) are most strongly correlated with team win percentages? Which defensive statistics (e.g. rebounds, assist, and field goal percentage) are most strongly correlated with team win percentages? Do advanced analytics metrics such as offensive rating and defensive rating better explain team success than traditional statistics? Are certain statistical combinations more predictive of winning seasons than any single metric alone? Thus, by answering these questions, this project will aim to understand the statistical factors that contribute to successful NBA teams. 

Datasets
The first dataset we will use are NBA team statistics, which will come from the NBA’s official statistics website. Some of the variables included are:
Team name
Season
Wins 
Losses
Points per game
Assists per game
Rebounds per game
Offensive rating
Defensive rating
While the dataset isn’t readily available on the website, we will utilize API calls to generate a dataset by converting the raw JSON output to a CSV. The reason this dataset is beneficial is because it includes team-level statistics needed to measure winning seasons.
	The second dataset we will use is from ESPN, which will also come from an API. Some of the variables that will be utilized are:
Game date
Home team
Away team
Final score
Winner
Season information
This dataset will allow us to calculate important metrics such as total wins, losses, and win percentages. This gives us the outcome variable for our research question.
The third dataset we will use are advanced basketball metrics from the website Basketball Reference. Some variables it contains are: 
Player Efficiency Rating (PER)
Win Shares
Usage Rate
Offensive Box Plus Minus
Defensive Box Plus Minus
This dataset will be beneficial because we can compute team averages of advanced metrics and analyze whether teams with more efficient players win more games.

Timeline
The project will be completed over an eight-week period and will follow several key stages of the data lifecycle used in data management and analysis projects. These stages include becoming familiar with the datasets, collecting and acquiring the data, preparing and standardizing the datasets, integrating multiple datasets, cleaning and validating the data, and performing data analysis and visualization. The timeline below outlines the main tasks that will be completed during the project and describes when each task will occur. All team members will collaborate on each stage of the project and contribute to the development of everything through the GitHub repository.

Task 1: Evaluate and Become Familiar with the Datasets

Description:
During the first stage of the project, the team will look at the selected datasets and become familiar with the data. This includes looking at the variables included in each dataset, understanding how the data is organized, and identifying which variables can be used to link the datasets together. In addition, the team will review the documentation as 2 of our datasets are APIS. Any issues related to data will be identified during this stage. This will be completed during week 1 of 8 and all team members will work together in-person or over zoom on this. 

Task 2: Collect and Acquire the Data

Description:
After evaluating the datasets, our team will begin writing the code to collect the data from our sources. This involves retrieving data through APIs, downloading datasets from official statistics websites, or extracting data through web scraping. The goal of this task is to ensure that the data can be acquired onto our machines and also be reproduced on other machines.. All datasets will be stored in the project repository. The code used to acquire the datasets will also be saved in the repository so that the data collection process can be reproduced. This will be completed during week 2 of 8 and all team members will work together in-person or over zoom on this. 

Task 3: Standardize Data Formats and Prepare Data for Integration

Description:
Because the datasets come from different sources and use different formats, our team will standardize the datasets to make sure they are compatible. This will involve renaming variables to use consistent naming conventions and ensuring that data types are consistent across datasets. The team will also ensure that key identifiers such as team names and season years are formatted consistently so that the datasets can be integrated successfully. These steps will help prepare the datasets for the integration stage and reduce potential errors when merging the data. This will be completed between weeks 3 or 4 of 8 and all team members will work together in-person or over zoom on this.

Task 4: Integrate Datasets into a Unified Dataset

Description:
Once the datasets have been standardized, the team will integrate them into a dataset that combines the relevant information from each source. This integration will be performed using common attributes such as team names and season identifiers. Python libraries such as pandas will be used to merge the datasets and create a single dataset. The integration process will be implemented through code stored in the repository so that the steps can be repeated. This will be completed during week 5 of 8 and all team members will work together in-person or over zoom on this. 

Task 5: Perform Data Cleaning

Description:
After integrating the datasets, the team will perform data cleaning to address potential data quality issues. This step may involve identifying missing values, removing duplicate entries, correcting inconsistent team names, and converting variables into appropriate data types.

The team will also verify that the integrated dataset accurately represents the information from the original datasets. Any cleaning operations applied to the data will be implemented through scripts to ensure that the process is transparent and reproducible. This will be completed during week 6 of 8 and all team members will work together in-person or over zoom on this. 

Task 6: Conduct Data Analysis and Create Visualizations

Description:
The final stage of the project will involve analyzing the cleaned dataset to determine which team statistics are most strongly associated with winning seasons. The team will use statistical methods such as correlation analysis or regression to examine relationships between team performance metrics and season outcomes.

In addition to statistical analysis, the team will create visualizations that help illustrate patterns in the data. These visualizations may include scatter plots, bar charts, and correlation matrices that show how different team statistics relate to winning percentages. The results of the analysis will help answer the main research question and provide insights into what factors contribute most strongly to successful NBA teams. This will be completed during week 1 of 8 and all team members will work together in-person or over zoom on this. 

Constraints
	Some constraints for our datasets include data consistency, completeness, and API limitations. Since we’re using three datasets, some variables might have slightly different names or abbreviations, including team names. This will require us to standardize the data to ensure that we can grab the necessary information from each dataset. There could also be missing data from certain seasons in one dataset but not the others, meaning we will need to be sure that missing values are removed or imputed. Additionally, there are API rate limitations and restrictions, especially for popular ones like ESPN’s. We will need to be sure we don’t exceed these limits so we aren’t temporarily banned from using the API services.

Gaps
	More research is needed to determine the best analytical method to identify predictors of team success, which will take some trial and error. We will also need to determine which method of integrating the datasets is the most efficient after we gather the data from the APIs.
