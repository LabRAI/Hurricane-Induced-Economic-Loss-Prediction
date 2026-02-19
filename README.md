# Hurricane-Induced-Economic-Loss-Prediction

This work appears in SpatialConnect‘25: Proceedings of the 1st ACM SIGSPATIAL International Workshop on Spatial Intelligence for Smart and Connected Communities.

## How to Cite

If you find this work useful in your research, please consider citing:

```bibtex
@inproceedings{10.1145/3764924.3770889,
author = {Shen, Bolin and Ozguven, Eren and Zhao, Yue and Wang, Guang and Xie, Yiqun and Dong, Yushun},
title = {Learning from the Storm: A Multivariate Machine Learning Approach to Predicting Hurricane-Induced Economic Losses},
year = {2025},
url = {https://doi.org/10.1145/3764924.3770889},
location = {The Graduate Hotel Minneapolis, Minneapolis, MN, USA},
}
```

## Install Environment

We use [uv](https://github.com/astral-sh/uv) to manage this project.

```shell
uv sync
```

Packages we use
```
hurricane v0.1.0
├── geopandas v1.0.1
├── matplotlib v3.9.4
├── pandas v2.2.3 (*)
├── scikit-learn v1.6.1
├── scipy v1.13.1 (*)
├── shapely v2.0.7 (*)
└── xgboost v2.1.4
```

## Run Experiments

Predict economic loss. 

`model_name`: Name of the model to run (e.g., RF, XGB, NN, GBM, Stacked)
```shell
python main.py --model_name XGB
```

Example:
```text
Evaluating RF with 5-fold cross-validation:
  Fold 1 metrics: R2: 0.7264, MAE: 1.1896, SMAPE: 6.4793, RMSE: 1.6575, RMSLE: 0.0824
  Fold 2 metrics: R2: 0.6310, MAE: 1.4707, SMAPE: 7.9966, RMSE: 1.8900, RMSLE: 0.0957
  Fold 3 metrics: R2: 0.7012, MAE: 1.2913, SMAPE: 7.4189, RMSE: 1.7228, RMSLE: 0.0915
  Fold 4 metrics: R2: 0.6522, MAE: 1.3366, SMAPE: 7.3960, RMSE: 1.8208, RMSLE: 0.0948
  Fold 5 metrics: R2: 0.6633, MAE: 1.4156, SMAPE: 7.8946, RMSE: 1.8395, RMSLE: 0.0930

RF performance (5-fold CV):
R2: 0.675 \pm 0.0
MAE: 1.341 \pm 0.1
SMAPE: 7.437 \pm 0.5
RMSE: 1.786 \pm 0.1
RMSLE: 0.091 \pm 0.0
```


## Visualization

plot importance
```shell
python visualization.py
```

plot heatmap
```shell
python visualization.py
```
