# Tag: bildcode/pyside2:py3.6

# debian with latest Python 3.6 release
FROM python:3.6-slim-stretch

# install Qt / Pyside2 / CI-helper modules
RUN apt-get update && \
    apt-get autoclean && \
    apt-get install -y --no-install-recommends \
        qtbase5-dev-tools \
        xvfb \
        libegl1-mesa \
        x11-xserver-utils \
        libxkbcommon-x11-0 \
        x11-utils && \
    apt-get clean && \
    rm -rf /var/cache/apk/* && \
    python -m pip install --no-cache-dir --upgrade pip && \
    pip install --no-cache-dir \
        anybadge \
        devpi-client \
        flake8 \
        pylint \
        PySide2 \
        pytest \
        pytest-cov \
        pytest-qt \
        pytest-xvfb \
        Qt.py \
        xvfbwrapper && \
    apt-get purge -y build-essential && \
    apt-get purge -y cmake

# setup virtual display
ENV DISPLAY=:99
ENV SCREEN=0
ENV DBUS_SESSION_BUS_ADDRESS=/dev/null

# turn this on for verbose qt feedback
ENV QT_DEBUG_PLUGINS=0
ENV QT_VERBOSE true
ENV QT_TESTING true

# start the container with a bash shell by default
CMD ["bin/bash"]
