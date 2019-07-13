# Tag: bildcode/pyside2:develop

FROM python:slim-stretch

RUN apt-get update && \
    apt-get autoclean && \
    apt-get install -y --no-install-recommends \
        xvfb \
        qtbase5-dev-tools && \
    apt-get install -y \
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
        anybadge \
        pylint \
        devpi-client

ENV DISPLAY=:99
ENV SCREEN=0
ENV DBUS_SESSION_BUS_ADDRESS=/dev/null
ENV QT_DEBUG_PLUGINS=1
VOLUME /tmp/.X11-unix

CMD ["bin/bash"]
