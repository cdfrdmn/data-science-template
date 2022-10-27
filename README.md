# Data Science Cookie Cutter

**Note**: _This repo was forked from https://github.com/khuyentran1401/data-science-template_

## What is this?
This repository is a template for data science projects.

It allows anybody to quickly and easily create a **reproducible** Python data science
project, already set up with the following tools:

* [Jupyter Notebook](https://docs.jupyter.org/en/latest/): Web application for
creating and sharing computational documents.
* [Ipykernel](https://ipython.readthedocs.io/en/stable/index.html): The Python
execution backend for Jupyter. It is required as the kernel will be used within
a virtual environment.
* [Pandas](https://pandas.pydata.org/docs/): A fast, powerful, flexible and easy to use open source data
analysis and manipulation tool.

## What makes the projects reproducable?

Anyone may simply follow the installation instructions in the project README to reproduce it.

## Requirements
* [Cookiecutter](https://cookiecutter.readthedocs.io/en/stable/): A command-line
utility that creates projects from cookiecutters (project templates).
* [Poetry](https://python-poetry.org/docs/): A tool for dependency management
and packaging in Python - [article](https://towardsdatascience.com/how-to-effortlessly-publish-your-python-package-to-pypi-using-poetry-44b305362f9f).


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

## How To Use This Project

Install Cookiecutter:
```bash
$ pip install cookiecutter
```

Install Poetry:
```bash
$ curl -sSL https://install.python-poetry.org | python3 -
```

Create a new project based on this repo:
```bash
$ cookiecutter https://github.com/cdfrdmn/data-science-template
```
You’ll be prompted to answer certain details about the project:

- Name of the project
- Author of the project
- The Python version constraint for your project - see [Caret requirements](https://python-poetry.org/docs/1.1/dependency-specification/).

**Note**: _By default, Poetry will try to use the Python version used during
Poetry’s installation to create the virtual environment. If this Python
version is not compatible with the Python requirement of the project, see the Poetry documentation's section [Managing Environments](https://python-poetry.org/docs/managing-environments/)._


### Set Up the Environment

Activate the virtual environment, and open a sub-shell within it:
```bash
$ make activate
```
Then run:
```bash
$ make setup
```
This will do the following:

1. Initialise a git repository for your project.
2. Install the tools already specified in the configuration file
`pyproject.toml`.

Congratulations! You have just created a reproducible data science project with
useful tools.

### Install New Packages

If you want, you can install more PyPI packages with:
```bash
$ poetry add <package-name>
```

## How to Share your Project

First, lock the package versions in our project:
```bash
$ poetry lock
```
This will allow others to create exactly the same virtual environment as yours.

In git, stage all changes and commit them.
```bash
$ git add -A
$ git commit
```

Create a git repository using the GitHub UI, and copy its URL.

Add an origin to your local repo so that it's associated with your remote GitHub repo 
```bash
$ git add origin <your-repo-url>
```

Finally, push your local repo to GitHub:
```bash
$ git push --set-upstream origin 
```

Now anybody can reproduce your project by following the installation instructions in its README.
