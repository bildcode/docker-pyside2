FROM python:slim-stretch

RUN apt-get update && \
    apt-get autoclean && \
    apt-get install -y --no-install-recommends xvfb qtbase5-dev-tools && \
    rm -rf /var/cache/apk/* && \

    python -m pip install --no-cache-dir --upgrade pip && \
    pip install --no-cache-dir PySide2 && \
    pip install --no-cache-dir Qt.py && \
    pip install --no-cache-dir pytest pytest-cov anybadge pylint devpi-client && \

CMD ["bin/bash"]
