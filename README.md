# Cookiecutter Python

A cookiecutter template that is aimed for all kinds of python project. It's
straight-forward and easy to use. You can create a brand new python project 
by executing one command.

In addition, many state-of-art technologies are adopted in this project, including
but not limited to:
- Black Code style formatting
- flake8 Linter.
- Docker-compose for local development.
- Semantic version release.
- Gitlab/CircleCi CI/CD.

----
## Python Project Structure
You can edit it of your own accord :sparkling_heart:

    {{ cookiecutter.project_slug }}
    ├── src  # source folder
        ├── main.py  # python script
        ├── Dockerfile
        ├── pytest.ini
        └── requirements.txt
    ├── .template
        ├── template_tags.json
    ├── .github
        ├── pytest.yml
    ├── .circleci
        ├── config.yml
    ├── docs
        ├── AUTHORS.md  
    ├── .gitignore
    ├── .pre-commit-config.yaml
    ├── CHANGELOG.md
    ├── docker-compose.yml
    ├── LICENSE
    ├── pyproject.toml
    ├── README.md
    ├── setup.cfg
    └── setup.py

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
cd {{cookiecutter.project_slug}}/src
docker build --tag python-project .
docker run python-project
```
