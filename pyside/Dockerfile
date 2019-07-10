FROM iron/python:2.7

RUN echo "@testing http://nl.alpinelinux.org/alpine/edge/testing" >> /etc/apk/repositories && \
apk update && apk upgrade \
  && apk add --update alpine-sdk nano qt5-qtbase qt5-qttools-dev \
  && rm -rf /var/cache/apk/*

RUN pip3 install PySide2
RUN pip3 install Qt.py
RUN pip3 install pytest
RUN pip3 install pytest-cov
RUN pip3 install anybadge

# ENV PATH /usr/local/lib/python2.7/site-packages/PySide/:$PATH
