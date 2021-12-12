# {{ cookiecutter.project_title }}

{{ cookiecutter.project_short_description }}

----
## Table of contents
- [Project Structure](#structure)
- [Get Started](#getstarted)
- [How to run the project](#run)
- [Pre-commit](#pre-commit)
- [Version Release](#version)

----
## Project Structure <a name="structure"></a>
// TODO

## Get Started <a name="getstarted"></a>

Before you can run this project, you need to have python installed.
You can use [pyenv](https://github.com/pyenv/pyenv) to create a virtual environment.

### Step 1: Set up Python >= 3.7:
Consider installing with [Homebrew](https://docs.brew.sh/):
```bash
brew update
# install pyenv by Homebrew
brew install pyenv
# confirm installation
pyenv --version  # pyenv 1.2.26
# create a python virtual env
pyenv virtualenv 3.8.9 python-starter-3.8.9
# activate the virtual env
pyenv activate python-starter-3.8.9
```

### Step 2: Install dependencies
Automatically create requirements
```bash
python -m pip freeze > requirements.txt
python -m pip install -r requirements.txt
```

To run pre-commit against all files
```bash
pre-commit run --all-files
```

----
## Run the project <a name="run"></a>
// TODO How to run your project

----

## Pre-commit <a name="pre-commit"></a>
This project adopts pre-commit framework to maintain code readability and consistency.
Before you run hooks, you need to have pre-commit package manager installed.

```bash
pip install pre-commit
```

---

## Semantic Version Releases <a name="version"></a>
```bash
pip install python-semantic-release # install the package

semantic-release publish --minor/--patch/--major # bump version
```
