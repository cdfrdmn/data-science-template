[![View on Medium](https://img.shields.io/badge/Medium-View%20on%20Medium-blue?logo=medium)](https://towardsdatascience.com/how-to-structure-a-data-science-project-for-readability-and-transparency-360c6716800)

# Data Science Cookie Cutter

**Note**: _This template uses poetry. If you prefer using pip, go to the [pip](https://github.com/khuyentran1401/data-science-template/tree/pip) branch instead._
## What is this?
This repository is a template for a data science project. This is the project structure I frequently use for my data science project. 

## Tools used in this project
* [Poetry](https://towardsdatascience.com/how-to-effortlessly-publish-your-python-package-to-pypi-using-poetry-44b305362f9f): Dependency management - [article](https://towardsdatascience.com/how-to-effortlessly-publish-your-python-package-to-pypi-using-poetry-44b305362f9f)

## Project Structure
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

## How to use this project

Install Cookiecutter:
```bash
pip install cookiecutter
```

Create a project based on the template:
```bash
cookiecutter https://github.com/cdfrdmn/data-science-template
```

Find detailed explanation of this template [here](https://towardsdatascience.com/how-to-structure-a-data-science-project-for-readability-and-transparency-360c6716800).
