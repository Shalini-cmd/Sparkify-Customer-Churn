# Sparkify-Customer-Churn
Used Udemy's Sparkify Dataset to understand customer churn in music apps
Sparkify is a made-up music app. This dataset was solely created for educational purposes<br>
Spark 3.0.0 was used for this project

- We used a subset of te original dataset (~1.5 M rows)
- The data contains event data meaning everytime a customer visited the app , every action between the pages are recorded as a row
- We have data for 2 months (September - October) as a result we had data for only 212 customers 
- We leveraged Spark MLIb for all the analysis
- We used MatPlotLib for ROC curves and seaborn for creating correlation heatmap and other EDA

### Problem Statement
It is a known fact that it costs much more to acquire customers than to keep an existing one,
sometimes by up to five times [1]. According to research done by Bain & Company [2],
increasing customer retention rates by 5% increases profits by 25% to 95%. With such figures,
it's paramount for businesses to focus their efforts on satisfying existing customers. The goal of
our project is to help Sparkify, a music streaming service, to identify ways to reduce customer
premium churn where churn refers to paying subscribers who cancel their premium subscription.

### Data: 
For the preliminary analysis to identify we are relying on observational dataset. The data
is extracted from a system that logs all events on the website containing information about
artist,song and session.
- Target variable : Flag if the user churned or not (rows with ‘cancelled confirmation’)
- Explanatory Variables : We have derived user level features from the originals log dataset -
Avg. number of sessions logged daily, Avg. number of sessions logged monthly, Avg. time spent
per session , Avg. no. of songs heard daily.

### Model Implementation
We ran three types of models - Logistic Regression , Gradient Boost , Random Forest.
Through Random Forest, we got an F1 score of 68% ,and AUC of 67% ( 10% improvement
from GBM model). Also, to make sure, we account for class imbalance and superior predictive
power, we end up choosing Random Forest and use metrics like importance of variables to see
feature insights.
