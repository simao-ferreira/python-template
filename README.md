# python-template

Simple project base template for python applications.

- [how-to](#how-to)
  - [environment](#environment)
  - [requirements](#requirements)
  - [run](#run)
  - [tests](#tests)
  - [configuration](#configuration)
  - [problems](#problems)
- [technologies](#technologies)

## how to

### environment

```shell
# Create a new environment
$ python3 -m venv /path/to/new/virtual/environment

# Activate environment
$ source venv/bin/activate

# Install dependencies
$ pip install -r requirements.txt

# Deactivate
$ deactivate
```

### requirements

```shell
# Install pip-tools
$ pip install pip-tools

# Generate requirements.txt
$ pip-compile requirements.in

# Update requirements.txt
$ pip-compile --upgrade

# Update single package
$ pip-compile --upgrade-package <package-name>

# Update single package to a specific version
# e.g. --upgrade-package requests==2.0.0
$ pip-compile --upgrade-package <package-name>==<version>
```

### run

```shell
# Main
$ python main.py

# Scratch files
$ python <module>/<folder>/create_filtered_csv.py <element>

# Module files
$ python -m <module>.<folder>.file
```

### tests

```shell
# Run all tests
$ pytest

# Run class test
$ pytest tests/<test_file_name>.py
```

### configuration

Create a .env file and define `SRC_PATH` with repository path.

```shell
# Arch
SRC_PATH=/home/<...>/core
# OSX
SRC_PATH=/Users/<...>/core
```

### problems

In linux there is an issue installing psycopg2, it looks like it has to be built - through setup.py
Solution was install psycopg2-binary instead.

## technologies
