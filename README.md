# Debian, Python 3, Qt5, PySide2 + CI helpers
The intention is to have lightweight containers
to work with CI runners like the ones in GitLab.

We start in a bash shell on purpose, so we can 
conveniently configure our CI setup from here.

# Dockerfiles / Tags
* py3.6  (trusty)
* py3.7  (trusty)
* py3.6-dev (experimental)
* py3.7-dev (experimental)


# Pre-installed pip packages
* PySide2
* Qt.py
* pytest
* pytest-cov
* pylint
* devpi-client
* anybadge
