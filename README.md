# MLB-Predictions

### Do early season performances by pitchers or batters give a better indication of a team's season win-loss percentages?

Data from April 2022 is used to predict season win-loss percentages. Hopefully this exploration will show whether pitchers' or batters' performances can give a better overall picture of the entire season.

Technologies using:
Excel
Jupyter Notebook
Python
Tableau

ETL, data visualization, and supervised machine learning will be used to try to answer the question above.

ETL complete, unless other ML requires more work. Strings turned to floats relating to the situations in a baseball game (example: play result changed from "Out" to -1)

Four linear regression models created. 

Input (X): 'OUTSONPLAY', 'RUNSSCORED', 'Num_Ball/Strike', 'ResultNum'

Target (y): WL Percentage (Win/Loss percentage for pitcher team or batter team)

Models for all pitches and just for pitches that result in plays (out, single, double, etc.)

There is no correlation seen in any of the 4 models with r-squared values of:
Pitcher/all pitches: 0.0002769175762997733
Pitcher/only plays: 0.0007343224227988054
Batter/all pitches: 0.0002116597581568458
Batter/only plays: 0.0015267205914351045

More supervised machine learning will be used to see if the target question can be answered, or if this pitch-by-pitch data can't be used to make predictions for the entire season.
