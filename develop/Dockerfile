FROM python:slim-stretch

RUN apt-get update && \
    apt-get autoclean && \
    apt-get install -y --no-install-recommends xvfb qtbase5-dev-tools && \
    apt-get install -y x11-xserver-utils && \
    apt-get clean && \
    rm -rf /var/cache/apk/* /var/cache/apt/archives/* /var/lib/apt/lists/* && \

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

ENV DISPLAY=0
ENV SCREEN=0
ENV DISPLAY_MODE=1024x768x16
VOLUME /tmp/.X11-unix

CMD ["bin/bash"]
