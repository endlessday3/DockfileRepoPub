FROM endlessday3/t_ubuntu:16.04
MAINTAINER endlessday3

RUN apt-get update && apt-get install -y \
    build-essential \
    python3.5 \
    python3.5-dev \
    python3-pip \
    python3.5-venv \
    iputils-ping \
    apt-utils \
    openssh-client

COPY pip.conf /root/.pip/pip.conf

RUN python3 -m pip install pip --upgrade \
        && python3 -m pip install wheel \
        && python3 -m pip install setuptools --upgrade

RUN rm -f /usr/bin/python && ln -s /usr/bin/python3 /usr/bin/python
