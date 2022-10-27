# {{cookiecutter.directory_name}}

{{cookiecutter.directory_name}} is a data science project which explores...

## Requirements

* [Python](https://www.python.org/getit/) development environment
* [Poetry](https://python-poetry.org/docs/): Dependency management
* Add more...

## Installation

1. Clone this repository:
```bash
$ git clone https://github.com/this-repo

```
2. Activate the virtual environment and open a sub-shell within it:
```bash
$ cd {{cookiecutter.directory_name}}

$ poetry shell
```

3. Install the dependencies of this project:
```bash
$ poetry install
```

You are now ready to use this project.

## Usage

You can explore this project in a Jupyter Notebook. There are two ways to do
this:

* If you are already inside a sub-shell of the virtual environment, run the
following command:
```bash
$ jupyter notebook
```
* Alternatively, if you are not in a sub-shell of the virtual environment, you can use the command:
```bash
$ poetry run jupyter notebook
```
This will start a Jupyter server and display this project's Jupyter Notebook in your web browser.
