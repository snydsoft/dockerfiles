#
# ubuntu latest upgrade version
#
# build:
#   docker build --force-rm=true -t draconids/ubuntu:14.04.5 .
#
# timezone:
#   RUN echo "Asia/Seoul" > /etc/timezone && dpkg-reconfigure -f noninteractive tzdata

FROM ubuntu:14.04.5

MAINTAINER Choi Iris <draconids@nate.com>

ENV DEBIAN_FRONTEND noninteractive

RUN sed -i -e 's/archive.ubuntu.com/kr.archive.ubuntu.com/g' /etc/apt/sources.list
RUN apt-get update \
    && apt-get -y upgrade \
    && apt-get -y autoremove \
    && apt-get -y clean

RUN locale-gen en_US.UTF-8
ENV LANG en_US.UTF-8
ENV LANGUAGE en_US:en
ENV LC_ALL en_US.UTF-8
