General Overview of Progress
After the completion of our initial project plan, we have made progress in the earlier stages of the data lifecycle process, such as in data acquisition, standardization, and initial integration efforts. For instance, we have explored and collected data from our three datasets and have started preparing them for more advanced integration and analysis. 
	As of right now, our workflow has not yet completed all stages of the data lifecycle mode, but we have built a strong foundation and we are looking forward to continuing on improving our project. 

Task Updates:
Task 1: Evaluate and Become Familiar with the Datasets
Status: Done
The team has all spent their time exploring all 3 datasets. This means the documentation of the datasets in which helped us learn the structure and variables within each dataset. As suspected we found that team name and season will be key identifiers in our analysis. We also reviewed API documentation for NBA and ESPN sources to understand the limitations of the datasource.
Artifacts:
/data/nba_team_statistics_2010_2024.csv
/data/nba_game_outcomes_2010_2024.csv
/data/nba_advanced_metrics_team_2010_2024.csv

Task 2: Collect and Acquire the Data
Status: Done
Python scripts have been developed to collect data from APIs and convert JSONs into structured CSV files. The scripts ensure we can reproduce collecting the data again and again so if the data needs to be updated it can be.
Artifacts:
/data/nba_team_statistics_2010_2024.csv
/data/nba_game_outcomes_2010_2024.csv
/data/nba_advanced_metrics_team_2010_2024.csv

Task 3: Standardize Data Formats and Prepare Data for Integration
Status: In Progress
The team has started standardizing column names, formats, and data types across the 3 datasets. For example:
Converted all team names to a consistent naming convention
Standardized season formats (e.g. 2023-2024)
Made sure numeric fields are properly typed with no mistakes
There is still some work left to do to make sure all data is standardized due to issues combining datasets 
Artifacts:
/data/nba_team_statistics_2010_2024.csv (partially standardized)
/data/nba_game_outcomes_2010_2024.csv (partially standardized)
/data/nba_advanced_metrics_team_2010_2024.csv (partially standardized)

Task 4: Integrate Datasets into a Unified Dataset
Status: In Progress
The team started doing the first merges between the multiple datasets. Our first merges have successfully worked but we have been having some issues with some duplicates and failed merges when we use more columns. We are currently working on fixing the join logistics and making sure the merges are valid.
Task 5: Perform Data Cleaning
Status: Have Not Started
Need to do
Handling missing values
Removing duplicates
Validating merged records
We planned to begin after integration is finalized as we know the current joining logic isn’t working fully and we can’t get the final dataset we are striving for to use for this analysis.
Task 6: Conduct Data Analysis and Create Visualizations
Status: Have Not Started
Need to do
Correlation analysis between stats and win percentage
Regression modeling to identify key predictors
Visualization of relationships (scatter plots, heatmaps)
## Updated Timeline of Tasks

| Task | Status | Timeline |
|------|--------|----------|
| Task 1: Evaluate Datasets | Done | Week 1 |
| Task 2: Data Acquisition | Done | Week 2 |
| Task 3: Data Standardization | In Progress | Weeks 3–4 |
| Task 4: Data Integration | In Progress | Week 5 |
| Task 5: Data Cleaning | Not Started | Week 6 |
| Task 6: Analysis & Visualization | Not Started | Weeks 7–8 |




Individual Team Contributions
Ivan Mei:
Developed data acquisition scripts
Worked on API integration and JSON parsing
Assisted with dataset exploration
James Albarracin:
I mainly led the data standardization efforts, making sure that all the datasets followed consistent naming conventions, formats, and data types to enable successful integration. I also played a major role in merging the datasets, as well as refining the join logic using shared identifiers such as team name and season. Additionally, I actively looked for and debugged any  integration issues that came up, including resolving duplicate records and addressing failed merges, which help ensure the accuracy and reliability of the combined dataset.
Chris Pyter:
I assisted with preprocessing and data validation, as well as helped analyze the dataset structure to gain a better understanding of how to write our code. This entailed generating summary statistics and looking at the column names and data types. The preprocessing involved cleaning, transforming, and organizing data, while the validation involved manually looking at the data to ensure the values were reasonable.

All members contributed through GitHub commits and collaboration.

General Changes to Project Plan
Additionally, based on overall progress and feedback, we made the following adjustments:
1. More Defined Analytical Approach
Our original plan broadly mentioned using “correlation and regression.” Now, after reevaluating, we have refined this to potentially include methods such as:
Multiple linear regression models
Feature importance analysis
Evaluation metrics such as R-squared and RMSE
2. Improved Data Integration Strategy
After initial assessment and deliberations, we added explicit handling for:
Team name inconsistencies (e.g. abbreviations vs full names)
Season alignment across datasets
3. Clearer Success Metrics
We also clarified how we actually define “predictive strength”:
Strength of correlation with win percentage
Model performance metrics (R-squared, prediction error)

Challenges and Solutions
Challenge 1: Inconsistent Team Naming
Different datasets used variations such as abbreviations (e.g., “LAL”) vs full names (e.g., “Los Angeles Lakers”). This would make it difficult to manage and work with the data since we would have to spend extra time figuring out which teams have specific team name variations. Additionally, while not as much of a problem, it could make it slightly difficult to understand which teams are which if we aren’t fully familiar with the abbreviations.
Solution:
	
We created a mapping dictionary to standardize team names across all datasets before merging. This will make managing the data, as well as writing code to analyze the data, a lot easier, as it will save us time and improve the efficiency of our workflows.

Challenge 2: API Data Structure Differences
The APIs returned nested JSON formats that differed significantly across sources. This makes the output inconsistent, meaning we would have to write more scripts and edit our code based on the different formats.
Solution:
	
We implemented parsing functions in Python to flatten JSON responses into structured tables before exporting to CSV, making it easier to draw insights from the data.

Challenge 3: Missing or Incomplete Data
Some seasons or metrics were missing in certain datasets, which would limit the insights we could draw from the data. While we may not use all the metrics, we want to be able to conduct initial analysis and from there, determine the metrics that we believe can give us the most interesting insights. However, this cannot be until null values are dealt with.
Plan:


We will handle missing values by dropping incomplete rows when necessary and considering imputation for minor gaps.

Challenge 4: Dataset Integration Errors
Initial merges resulted in dropped or mismatched records, which would further affect our ability to work with the data in a meaningful way.
Solution:


We are currently working on refining join keys and validating row counts after merges to ensure data integrity.

Challenge 5: API Rate Limits
Repeated API calls risk exceeding usage limits, resulting in delays that could worsen as usage limits are continually encountered.
Solution:


We plan to implement local data storage and caching to minimize repeated API requests and prevent any delays working with the API.


 

