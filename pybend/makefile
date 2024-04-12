include makefile.conda_env
include makefile.help
include makefile.include


# COMMANDS

## Install Python Dependencies by Poetry
dep-install: environment_enabled
	poetry install --with dev


.PHONY: clean
## Delete all compiled Python files
clean: clean-pyc clean-test

## Delete all compiled Python files
clean-pyc:
	find . -name '*.pyc' -exec rm -f {} +
	find . -name '*.pyo' -exec rm -f {} +
	find . -name '*~' -exec rm -f {} +
	find . -name '__pycache__' -exec rm -fr {} +
# find . -type f -name "*.py[co]" -delete
# find . -type d -name "__pycache__" -delete
# rm -f .make.*

## Delete all testing artifacts
clean-test:
	rm -fr .tox/
	rm -f .coverage
	rm -fr htmlcov/

## Delete all stopped docker container
clean-containers:
# ref: https://docs.docker.com/reference/cli/docker/container/rm/#remove-all-stopped-containers
# docker rm $(docker ps --filter status=exited -q)
	docker ps --filter status=exited -q | xargs docker rm

