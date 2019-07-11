# Debian, Python 3, Qt5, PySide2 + CI helpers
Built off of the official [`python:3.*-slim-stretch`](https://hub.docker.com/_/python) images, which are based on Debian. 

The intention is to have lightweight containers that work well with CI runners like the ones in GitLab.

We start in a bash shell on purpose, so we can 
conveniently configure our CI setup from here.

# Dockerfiles / Tags
* py3.6
* py3.7


# Pre-installed pip packages
* PySide2
* Qt.py
* pytest
* pytest-cov
* pylint
* devpi-client
* anybadge
