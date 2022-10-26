# {{cookiecutter.directory_name}}

## Tools used in this project
* [Poetry](https://towardsdatascience.com/how-to-effortlessly-publish-your-python-package-to-pypi-using-poetry-44b305362f9f): Dependency management - [article](https://towardsdatascience.com/how-to-effortlessly-publish-your-python-package-to-pypi-using-poetry-44b305362f9f)

## Project structure
```bash
.
├── .gitignore                      # ignore files that cannot commit to Git
├── Makefile                        # store useful commands to set up the environment
├── notebooks                       # store notebooks
├── pyproject.toml                  # dependencies for poetry
├── README.md                       # describe your project
└── src                             # store source code
    └── __init__.py                 # make src a Python module 
```

## Set up the environment
1. Install [Poetry](https://python-poetry.org/docs/#installation)
2. Set up the environment:
```bash
make activate
make setup
```

## Install new packages
To install new PyPI packages, run:
```bash
poetry add <package-name>
```
