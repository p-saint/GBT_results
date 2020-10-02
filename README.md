# Gradient Boosting Algorithms - Hyperparameter Importance Study

This repository aims at centralizing all results data from our hyperparameter importance study as well as providing some simple visualisation tools available in a notebook.

## Objectives

The goal of the study was to acquire a better understanding of the importance of hyperparameters of different gradient boosting implementations (XGboost, LightGBM, scikit-learn, and CatBoost). The experiments consisted in a 1000 points random search performed on different datasets, over a selection of hyperparameters detailed in the section below.


## Algorithm settings

### Library dependencies

    xgboost==1.0.2
    lightgbm==2.3.1
    scikit_learn==0.23.0
    catboost==0.23


### Hyperparameters for XGBoost

|           Parameter name            |           range           |
|-------------------------------------|---------------------------|
|              missing                |          {0, nan}         |
|            tree_method              |{'exact', 'approx', 'hist'}|
|            n_estimators             |         [50, 200]         |
|                eta                  |         [0.1, 1]          |
|             max_depth               |         [6, 20]           |
|             subsample               |         [0.5, 1]          |
|         colsample_bytree            |         [0.4, 1]          |
|         colsample_bylevel           |         [0.4, 1]          |
|          min_child_weight           |         [0.5, 10]         |
|               gamma                 |          [0, 1]           |

### Hyperparameters for LightGBM

|           Parameter name            |           range           |
|-------------------------------------|---------------------------|
|            n_estimators             |         [50, 200]         |
|           learning_rate             |         [0.1, 1]          |
|             max_depth               |          [5, 20]          |
|         min_child_samples           |          [1, 100]         |
|             subsample               |          [0.5, 1]         |
|         colsample_bytree            |          [0.5, 1]         |
|             num_leaves              |         [20, 500]         |
|          min_split_gain             |           [0, 1]          |

### Hyperparameters for HistGradientBoosting

|           Parameter name            |           range           |
|-------------------------------------|---------------------------|
|              max_iter               |         [50, 200]         |
|           learning_rate             |         [0.1, 1]          |
|             max_depth               |          [5, 20]          |
|         min_samples_leaf            |          [1, 100]         |
|             subsample               |          [0.5, 1]         |

### Hyperparameters for CatBoost

|           Parameter name            |           range           |
|-------------------------------------|---------------------------|
|            n_estimators             |         [50, 200]         |
|           learning_rate             |         [0.1, 1]          |
|               depth                 |          [5, 20]          |
|         min_data_in_leaf            |          [1, 100]         |
|          random_strength            |          [1, 20]          |
