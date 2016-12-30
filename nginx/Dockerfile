#
# nginx
#
# build:
#   docker build --force-rm=true -t draconids/nginx:1.10.2 .
#

FROM draconids/ubuntu:latest

MAINTAINER Choi Iris <draconids@nate.com>

ENV NGINX_VERSION 1.10.2

RUN apt-get -y install build-essential zlib1g-dev libpcre3 libpcre3-dev unzip curl wget

RUN ["/bin/bash", "-c", "bash <(curl -f -L -sS https://ngxpagespeed.com/install) --nginx-version ${NGINX_VERSION}"]

ADD ./nginx.conf /usr/local/nginx/conf/nginx.conf
ADD ./proxy_params /usr/local/nginx/conf/proxy_params

# volume
VOLUME /usr/local/nginx/conf/certs
VOLUME /usr/local/nginx/conf/conf.d
VOLUME /usr/local/nginx/conf/sites
VOLUME /usr/local/nginx/conf/streams

WORKDIR /usr/local/nginx

EXPOSE 80 443

CMD /usr/local/sbin/nginx
