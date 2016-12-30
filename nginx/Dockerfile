#
# nginx
#
# build:
#   docker build --force-rm=true -t draconids/nginx:latest .
#
# bash:
#   docker run -it --rm draconids/certbot:latest auth --authenticator webroot --webroot-path /var/www --renew-by-default --agree-tos --email draconids@nate.com --server https://acme-v01.api.letsencrypt.org/directory -d dev.pamm.co.kr

FROM draconids/ubuntu:latest

MAINTAINER Choi Iris <draconids@nate.com>

ENV NGINX_VERSION 1.10.2
ENV NGX_PAGESPEED_VERSION 1.11.33.4