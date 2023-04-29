# MLB-Predictions

### Do early season performances by pitchers or batters give a better indication of a team's season win-loss percentages?

Data from April 2022 is used to predict season win-loss percentages. Hopefully this exploration will show whether pitchers' or batters' performances can give a better overall picture of the entire season.

Technologies using: Python, Jupyter Notebook, and Excel

ETL and supervised machine learning were used to try to answer the question above.

ETL including strings turned to floats relating to the situations in a baseball game (example: play result changed from "Out" to -1), creating different dataframes for different situations, clearing nulls, etc.
All machine learning models had the same variables.

Input (X): 'OUTSONPLAY', 'RUNSSCORED', 'Num_Ball/Strike', 'ResultNum'

Target (y): WL Percentage (Win/Loss percentage for pitcher team or batter team)

Models for all pitches and just for pitches that result in plays (out, single, double, etc.)

Four linear regression models created. 

There is no correlation seen in any of the 4 models with r-squared values of:

Pitcher/all pitches: 0.0002769175762997733

Pitcher/only plays: 0.0007343224227988054

Batter/all pitches: 0.0002116597581568458

Batter/only plays: 0.0015267205914351045

Decision Tree Regression also shows no correlation. The only data that had an r-squared score other than 0.0 or -0.1 was Batter/only plays which has an r-squared value of -0.01. 

Ensemble Learning (combining Random Forest Regressor, Gradient Boosting Regressor, and Linear Regression) also showed no correlation with the following r-squared values:

Pitcher/all pitches: -0.0004915590802110348

Pitcher/only plays: -0.005896896225054515

Batter/all pitches: -0.00198931491698362

Batter/only plays: -0.008711607780239383

These r-squared values for the different machine learning models show you can not predict win-loss percentages from early season pitch-by-pitch data (at least not when using these inputs: 'OUTSONPLAY', 'RUNSSCORED', 'Num_Ball/Strike', 'ResultNum'), no matter if it's for the pitchers' or batters' teams. Even though this project did not answer my original question, it helped me improve my ETL and supervised machine learning skills.
