# MLOps-Classification

This is a **uv, cookiecutter and dvc** setUp for an MLOps project.

## UV

```bash
pip install uv
uv init
uv add package
uv remove package
```

## CookieCutter

```bash
(data) MacBook-Air-de-Tomas-3:MLOps loperatomas410$ ccds
project_name (project_name): demomlops
repo_name (demomlops): repomlops
module_name (demomlops): 
author_name (Your name (or your organization/company/team)): TomasLopera
description (A short description of the project.): my first project
python_version_number (3.10): 3.13
Select dataset_storage
    1 - none
    2 - azure
    3 - s3
    4 - gcs
    Choose from [1/2/3/4] (1): 
Select environment_manager
    1 - virtualenv
    2 - conda
    3 - pipenv
    4 - uv
    5 - pixi
    6 - poetry
    7 - none
    Choose from [1/2/3/4/5/6/7] (1): 4
Select dependency_file
    1 - requirements.txt
    2 - pyproject.toml
    3 - environment.yml
    4 - Pipfile
    5 - pixi.toml
    Choose from [1/2/3/4/5] (1): 2
Select pydata_packages
    1 - none
    2 - basic
    Choose from [1/2] (1): 
Select testing_framework
    1 - none
    2 - pytest
    3 - unittest
    Choose from [1/2/3] (1): 2
Select linting_and_formatting
    1 - ruff
    2 - flake8+black+isort
    Choose from [1/2] (1): 
Select open_source_license
    1 - No license file
    2 - MIT
    3 - BSD-3-Clause
    Choose from [1/2/3] (1): 
Select docs
    1 - mkdocs
    2 - none
    Choose from [1/2] (1): 
Select include_code_scaffold
    1 - Yes
    2 - No
    Choose from [1/2] (1): 2
```

## DVC

**S3 Bucket:** `dvc[s3]`

```bash
dvc init
dvc add data
dvc add models
dvc push
```

## Project Organization

```
├── LICENSE            <- Open-source license if one is chosen
├── Makefile           <- Makefile with convenience commands like `make data` or `make train`
├── README.md          <- The top-level README for developers using this project.
├── data
│   ├── external       <- Data from third party sources.
│   ├── interim        <- Intermediate data that has been transformed.
│   ├── processed      <- The final, canonical data sets for modeling.
│   └── raw            <- The original, immutable data dump.
│
├── docs               <- A default mkdocs project; see www.mkdocs.org for details
│
├── models             <- Trained and serialized models, model predictions, or model summaries
│
├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
│                         the creator's initials, and a short `-` delimited description, e.g.
│                         `1.0-jqp-initial-data-exploration`.
│
├── pyproject.toml     <- Project configuration file with package metadata for 
│                         mlops_classification and configuration for tools like black
│
├── references         <- Data dictionaries, manuals, and all other explanatory materials.
│
├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
│   └── figures        <- Generated graphics and figures to be used in reporting
│
├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
│                         generated with `pip freeze > requirements.txt`
│
├── setup.cfg          <- Configuration file for flake8
│
└── mlops_classification   <- Source code for use in this project.
    │
    ├── __init__.py             <- Makes mlops_classification a Python module
    │
    ├── config.py               <- Store useful variables and configuration
    │
    ├── dataset.py              <- Scripts to download or generate data
    │
    ├── features.py             <- Code to create features for modeling
    │
    ├── modeling                
    │   ├── __init__.py 
    │   ├── predict.py          <- Code to run model inference with trained models          
    │   └── train.py            <- Code to train models
    │
    └── plots.py                <- Code to create visualizations
```

--------

