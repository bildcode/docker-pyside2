FROM iron/python:3.6

RUN echo "@testing http://nl.alpinelinux.org/alpine/edge/testing" >> /etc/apk/repositories
RUN apk update && apk upgrade
RUN apk add --update alpine-sdk nano qt5-qtbase qt5-qttools-dev xvfb py3-qt5 \
    && rm -rf /var/cache/apk/*

RUN pip3 install Qt.py
RUN pip3 install pytest
RUN pip3 install pytest-cov
RUN pip3 install anybadge
