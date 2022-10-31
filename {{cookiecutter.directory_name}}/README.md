# {{cookiecutter.directory_name}}

{{cookiecutter.directory_name}} is a data science project which explores...

## Requirements

* [Python](https://www.python.org/getit/) development environment
* [Poetry](https://python-poetry.org/docs/): Dependency management
* Add more if needed...

## Installation Method 1 - Using the Makefile

This method is quicker as it uses `make` commands. 

1. Clone this repository:
```bash
$ git clone https://github.com/<your-repo-name-here>
```
2. In the repository, start a new shell and activate the virtual envoironment:
```bash
$ make activate
```

3. Initialise a git repo and install the project dependencies:
```bash
$ make setup
```
_(**Note**: If you already initialised a git repository - don't worry, 
reinitializing won't do anything.)_

## Installation Method 2 - Using Poetry

If you prefer to know what the `make` commands are doing, follow this method. 

1. Clone this repository:
```bash
$ git clone https://github.com/<your-repo-name-here>
```
2. In the repository, start a new shell and activate the virtual envoironment:
```bash
$ poetry shell
```

3. Initialise a git repository:
```bash
$ git init
```

4. Install the project dependencies:
```bash
$ poetry install
```

You are now ready to use this project!

## Using Poetry
Read the full Poetry docs [here](https://python-poetry.org/docs/).

### Installing more packages

You can add more PyPI packages to this project with:
```bash
$ poetry add <package-name>
```

### Running scripts

To run your script simply use:
```bash
$ poetry run python your_script.py
```

Likewise if you have command line tools such as `pytest` or `black` you can run them using `poetry run pytest`.

## Jupyter Notebook

You can explore this project in a Jupyter Notebook.

From a sub-shell of the virtual environment, run the
following command:
```bash
$ jupyter notebook
```
Alternatively, if you are not in a sub-shell of the virtual environment, you can
use the command:
```bash
$ poetry run jupyter notebook
```
This will start a Jupyter server and open the project's Jupyter Notebook in
your web browser.
