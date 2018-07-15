FROM nginx:alpine

RUN apk update
RUN apk add apache2-utils

RUN rm /etc/nginx/conf.d/*
ARG ADMIN_USER
ARG ADMIN_PASSWORD
RUN mkdir /etc/apache2
RUN htpasswd -c -b /etc/apache2/.htpasswd $ADMIN_USER $ADMIN_PASSWORD

COPY proxy.conf /etc/nginx/conf.d
