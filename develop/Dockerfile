# Tag: bildcode/pyside2:develop

# debian with latest Python release
FROM python:slim-stretch

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
        PySide2 \
        Qt.py \
        xvfbwrapper \
        pytest \
        pytest-cov \
        pytest-xvfb \
        pytest-qt \
        anybadge \
        pylint \
        devpi-client

# setup virtual display
ENV DISPLAY=:99
ENV SCREEN=0
ENV DBUS_SESSION_BUS_ADDRESS=/dev/null

# turn this on for verbose qt feedback
ENV QT_DEBUG_PLUGINS=0

# start the container with a bash shell by default
CMD ["bin/bash"]
