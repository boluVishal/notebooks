# Titanic Notebooks — SpeedML

A collection of Titanic Kaggle competition notebooks built with the [SpeedML](https://github.com/Speedml/speedml) library, which wraps pandas, numpy, sklearn, xgboost, and matplotlib into a single pipeline-friendly API.

## Notebooks

All notebooks are in the `titanic/` folder:

| Notebook | Description |
|---|---|
| `titanic-solution-using-speedml.ipynb` | Main end-to-end solution using SpeedML |
| `titanic-data-science-solutions-refactor.ipynb` | Refactored version of a popular kernel |
| `titanic-eda-using-speedml.ipynb` | Exploratory data analysis |
| `titanic-feature-correlations-using-speedml.ipynb` | Feature correlation analysis |
| `titanic-solution-using-speedml-api.ipynb` | API-focused walkthrough |
| `titanic-solution-using-speedml-kaggle.ipynb` | Kaggle submission version |
| `titanic-speedml-0.9.2-release-updates-py*.ipynb` | Updates for SpeedML 0.9.2 (Python 2 & 3) |

Submission files with leaderboard scores are in `titanic/output/` — best result: **LB 0.78947**.

## Setup

```bash
pip install speedml
jupyter notebook
```

Data (`train.csv`, `test.csv`) is in `input/titanic/`.

## SpeedML quick start

```python
from speedml import Speedml

sml = Speedml('train.csv', 'test.csv', target='Survived', uid='PassengerId')
sml.plot.correlate()
sml.eda()
sml.feature.impute()
```
