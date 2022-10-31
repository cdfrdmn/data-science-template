# Python Data Science Template

**Note**: _This repo was forked from https://github.com/khuyentran1401/data-science-template_

## What is this?
This repository is designed for data scientists who want to create new, 
**reproducable** Python projects with powerful tools out of-the-box, in as 
little as three commands.

Once the user has followed the installation instructions below, they will 
have a new data science project with the following tools already installed:

* [Python](https://docs.python.org/3/): The most popular programming language 
for data science. 

* [Jupyter Notebook](https://docs.jupyter.org/en/latest/): Web application for
creating and sharing computational documents.

* [DVC](https://dvc.org/doc): Helps data science and machine learning teams 
manage large datasets, make projects reproducible, and collaborate better.

* [Pandas](https://pandas.pydata.org/docs/): A fast, powerful, flexible and easy
to use open source data analysis and manipulation tool.

## How is the data science project reproducable?

Every project created with this template:

* is designed for its dependencies to be managed by 
[Poetry](https://python-poetry.org/docs/).
* contains a README, which includes clear installation instructions for
anybody who wants to reproduce it.

## What does the project structure look like? 
```bash
.
├── .gitignore                      # ignore files that cannot commit to Git
├── Makefile                        # store useful commands to set up the environment
├── data                            # store jupyter notebooks
│   ├── processed                   # data after processing
│   └── raw                         # raw data
├── notebooks                       # store jupyter notebooks
├── pyproject.toml                  # dependencies for poetry
├── README.md                       # describe your project
└── src                             # store source code
    └── __init__.py                 # make src a Python module 
```

## Requirements
* [Cookiecutter](https://cookiecutter.readthedocs.io/en/stable/): A command-line
utility that creates projects from cookiecutters (project templates).
* [Poetry](https://python-poetry.org/docs/): A dependency management
and packaging tool for Python - [article](https://towardsdatascience.com/how-to-effortlessly-publish-your-python-package-to-pypi-using-poetry-44b305362f9f).

## How do I create a new project with this template?

Install Cookiecutter:
```bash
$ pip install cookiecutter
```

Install Poetry:
```bash
$ curl -sSL https://install.python-poetry.org | python3 -
```

Create a new project based on this repo using Cookiecutter:
```bash
$ cookiecutter https://github.com/cdfrdmn/data-science-template
```
You’ll be prompted to answer certain details about the project:

- Name of the project.
- Author of the project.
- The Python version constraint for your project (see [dependency specification](https://python-poetry.org/docs/1.1/dependency-specification/)).

_**Note**: By default, Poetry will try to use the Python version used during
Poetry’s installation to create the virtual environment. If this Python
version is not compatible with the Python requirement of the project, see the Poetry documentation's section [Managing Environments](https://python-poetry.org/docs/managing-environments/)._


### Finally, set up the environment

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
data science tools already installed.

### How can I add more packages to this template?

If you want, you can install more PyPI packages to this template with:
```bash
$ poetry add <package-name>
```

This will add your desired packages to the system build requirements file 
`pyproject.toml`.

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
