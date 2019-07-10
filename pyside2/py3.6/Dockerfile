FROM python:3.6-slim-stretch

RUN apt-get update
RUN apt-get autoclean
RUN apt-get install -y xvfb qtbase5-dev-tools \
    && rm -rf /var/cache/apk/*

RUN pip install PySide2
RUN pip install Qt.py \
    && pip install pytest pytest-cov anybadge pylint devpi-client

CMD ["bin/bash"]