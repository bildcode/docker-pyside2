FROM python:3.7-slim-stretch

RUN apt-get update && \
    apt-get autoclean && \
    apt-get install -y xvfb qtbase5-dev-tools && \
    rm -rf /var/cache/apk/* && \

    python -m pip install --upgrade pip && \
    pip install --no-cache-dir PySide2 && \
    pip install --no-cache-dir Qt.py && \
    pip install pytest pytest-cov anybadge pylint devpi-client

CMD ["bin/bash"]
