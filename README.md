# Cookiecutter Python

Cookiecutter Python is a framework that is aimed for all kinds of python project. It's very straight-forward and easy to use. You can create a brand new project by one command.

In addition, many state-of-art technologies are adpoted including
but not limited to:
- Black Code style formatting
- flake8 Linter.
- Docker-compose for local developement.
- Semantic version release.
- Automatic PyTest in CI/CD.

----
## Get Started :rocket:

### Step 1: Install cookiecutter
Please follow the [documentation](https://cookiecutter.readthedocs.io/en/1.7.2/installation.html) to install the package.

### Step 2: Create your new project
```bash
$cookiecutter https://github.com/LeisureTech/cookiecutter-python
```
Follow the terminal and set up parameters accordingly.

You're all set!

### Step 3: Run your project
```bash
cd {{cookiecutter.project_slug}}/app
docker build --tag python-project .
docker run python-project
```
