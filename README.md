# MLB_Pitching_Model
Major League Baseball Daily Fantasy Pitching Model (FanDuel and DraftKings)<br>
Predicts pitching points in daily fantasy baseball<br>

**Final model:**<br>
Gradient Boosting Regressor (scikit-learn)<br>
Mean Absolute Error on test set: 11.957 (FanDuel) and 8.04 (DraftKings)<br>

**Dataset**<br>
1194 observations<br>
29 features<br>

Data scraped from FanGraphs using Beautiful Soup<br>
Imported odds data from sportsbookreviews.com and created csv in Google Sheets to read into Pandas<br>
Engineered three of the four most strongly correlated features to the target variable (average outs recorded per start,<br>
project run differential in game, opponent's projected runs)<br>
Included only features with a Pearson correlation of at least .1 (data wrangling yielded 54 total features)<br>

**Model Evaluation:**<br>
Tried Linear Regression, Lasso Regression, Random Forest, Gradient Boosting Regressor, Ada Boost and XGBoost<br>
Cross-validated using GridSearch CV, tuning n_estimators, max_depth, learning_rate (boosting models) and alpha (Lasso and XGBoost)
