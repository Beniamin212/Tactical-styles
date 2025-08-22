# This project contains Python scripts and Jupyter notebooks for football tactical analysis using StatsBomb open data from the 2015/16 season for top 5 European leagues

It contains 2 files , a jolib model and a folder with scores of metrics for every team for one approach(The 19 playing styles adapted (Best performance)
 
Let's see what these 2 files contain :

### team_tactical_analysis_pca_clustering.ipynb

Compute team-level tactical metrics and analyze playing styles using PCA and clustering. It loads StatsBomb matches for the 2015/16 season and applies the trained VAEP model (only for VAEP metrics and metrics that need VAEP).

Process

- Predict VAEP values for each action using the trained model (only for VAEP metrics , some metrics do not use VAEP scores)

- Compute multiple tactical metrics

- Aggregate metrics per team across matches.

- Apply PCA (Principal Component Analysis) to reduce dimensionality and extract latent tactical styles.

- Cluster teams using different algorithms: KMeans, Agglomerative, GMM, Spectral, Birch.

- Visualize results in 2D/3D tactical style spaces and generate performance tables with color-coded ratings.

This notebook supports four different feature sets, depending on the analysis goal:

1) The 19 playing styles adapted (Best performance)
2) EFA-related indicators
3) VAEP metrics only
4) VAEP + other metrics

### vaep_model_xgboost_5leagues_1516.ipynb

Train a machine learning model (XGBoost) to estimate VAEP values (Valuing Actions by Estimating Probabilities). This model than will be used in the file : team_tactical_analysis_pca_clustering.ipynb for the metrics that require VAEP scores.

Data
StatsBomb open data for the **2015/16 season**:
- Premier League
- La Liga
- Bundesliga
- Serie A
- Ligue 1


## What you need to run these codes :

### Downolad these libraries :

-pip install pandas

-pip install numpy

-pip install socceraction

-pip install scikit-learn

-pip install joblib

-pip install tqdm

-pip install plotly

-pip install matplotlib

-pip install seaborn

-pip install xgboost

### You also need to use StatsBomb data (in my case i downloaded it locally , but you can use API aswell (API not provided in my codes))

Link to StatsBomb data : https://github.com/statsbomb/open-data





