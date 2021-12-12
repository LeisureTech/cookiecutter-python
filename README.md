# Cookiecutter Python 

A cookiecutter template that is aimed for all kinds of python project. It's
straight-forward and easy to use. You can create a brand new python project 
by executing one command.

## Features

- Black Code style formatting
- flake8 Linter.
- Docker-compose for local development.
- Semantic version release.
- CircleCi CI/CD.
- Replay project

----
## Python Project Structure :snake:
It does not necessairly to follow this structure. Feel free to fork this project and create a project of your own accord :sparkling_heart:

    {{ cookiecutter.project_slug }}
    ├── src  # source folder
        ├── main.py  # python script
        ├── Dockerfile
        ├── pytest.ini
        └── requirements.txt
    ├── .template  # cookiecutter replay dir
        ├── cookiecutter-python.json # cookiecutter-replay
        └── cookiecutter-config.yml  # user config
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

## Project Replay :dizzy:
Edit the `cookiecutter-config.yml` file from the `/.template` folder:
```yml
default_context:
    full_name: "Leisure Mojo"
    email: "leisuremojotech@gmail.com"
    github_username: "leisuremojo"
cookiecutters_dir: "~/.cookiecutters/"
replay_dir: "~/cookiecutter_python_example/.template" # set a relative/absolute path
```
Run the following commands:

```bash
cookiecutter --replay --config-file {{cookiecutter.project_slug}}/.template/cookiecutter-config.yml -f gh:LeisureTech/cookiecutter-python
```

> -f = overwrite if exists
