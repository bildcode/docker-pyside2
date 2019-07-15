# Debian, Python 3, Qt5, PySide2 + CI helpers
Built off of the official [`python:3.*-slim-stretch`](https://hub.docker.com/_/python) images, which are based on Debian. 

# What is this repo for?
The intention is to have lightweight containers that work well with CI runners.
We start in a bash shell on purpose, so we can 
conveniently configure our CI setup from here.

# Dockerfiles / Tags
The containers are automatically updated when their base images do.
* **latest** (based on python:slim-stretch)
* **develop** (from my develop branch, experimental)
* **py3.7** (based on python:3.7-slim-stretch)
* **py3.6** (based on python:3.6-slim-stretch)

Link: https://hub.docker.com/r/bildcode/pyside2/tags

# Pre-installed pip packages
* PySide2
* Qt.py
* pytest
* pytest-cov
* pylint
* devpi-client
* anybadge
