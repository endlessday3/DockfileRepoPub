FROM ubuntu:16.04
MAINTAINER endlessday3

RUN cd /etc/apt/ && mv sources.list sources.list_backup

COPY sources.list /etc/apt/sources.list

RUN apt-get update && apt-get install -y \
    software-properties-common \
    python-software-properties

