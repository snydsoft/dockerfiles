#
# certbot
#
# build:
#   docker build --force-rm=true -t draconids/certbot:latest .
#
# bash:
#   docker run -it --rm -v "/tmp/letsencrypt/www:/var/www" draconids/certbot:latest auth --authenticator webroot --webroot-path /var/www --renew-by-default --agree-tos --email draconids@nate.com --server https://acme-v01.api.letsencrypt.org/directory -d dev.pamm.co.kr


FROM quay.io/letsencrypt/letsencrypt:latest

MAINTAINER Choi Iris <draconids@nate.com>
