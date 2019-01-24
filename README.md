# Predict Stock Movements using news


1. Feature Engineering

Merge Market & News Data
Impute returns data using NOCB https://towardsdatascience.com/how-to-handle-missing-data-8646b18db0d4
Use companies that have data for VolumeCounts7D/NoveltyCount7D.

Find outliers of all variables and treat them. https://www.kaggle.com/artgor/eda-feature-engineering-and-everything

3 Create new features to capture autocorrelation: e.g: https://www.kaggle.com/youhanlee/simple-quant-features-using-python Make these specific to a particular Stock.


Create new Features to account for Time Series auto Correlation between rows.

2. Data reduction & Exploration

Subset of Data for top companies that always appear in news. We considered top 15 companies with news data based on our research.
The reason for doing so was due to the abundant news articles as well as data available for those in particular. The five stocks we used were:
 
Subset of Data from 2013
Use numeric news data (Novelty, Volume counts, Sentececount, Relevance, takeSequence etc.) & returns data columns
Spot outliers and plot correlation

3. Split train and Test

Transform target variable to binary Stock-Movement Up/Down (0/1)
Stock-Movement Up/Down will be the label for training.
TimeSeries Training is different from regular dataset training http://scikit-learn.org/stable/modules/generated/sklearn.model_selection.TimeSeriesSplit.html
4. Compare various Classifiers to find the best one. https://www.kaggle.com/aldemuro/comparing-ml-algorithms-train-accuracy-90 5. Fit Classifier with Train Using Classifiers that work well with Mixed Data.

1. Random Forest
2. BaggingClassifier with DecisionTrees
3. XGBoost
4. Nueral Networks

6. Cross validation to estimate test error for this model.

7. Use GridSearchCV to tune hyper parameters.
Use randomSearchCV instead of GridSearchCv for faster results.

8. Use the best estimator for test prediction and accuracy.

