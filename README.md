# Sparkify-Customer-Churn
Used Udemy's Sparkify Dataset to understand customer churn in music apps
Sparkify is a made-up music app. This dataset was solely created for educational purposes<br>
Spark 3.0.0 was used for this project

- We used a subset of te original dataset (~1.5 M rows)
- The data contains event data meaning everytime a customer visited the app , every action between the pages are recorded as a row
- We have data for 2 months (September - October) as a result we had data for only 212 customers 
- We leveraged Spark MLIb for all the analysis
- We used MatPlotLib for ROC curves and seaborn for creating correlation heatmap and other EDA
