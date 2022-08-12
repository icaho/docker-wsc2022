FROM alpine:3.16

RUN addgroup www
RUN adduser -D -g 'www' nginx

RUN echo http://dl-cdn.alpinelinux.org/alpine/edge/testing >> /etc/apk/repositories
RUN apk update && apk add --no-cache nginx certbot certbot-nginx ddclient openrc

RUN mkdir /www && \
    chown -R nginx:www /var/lib/nginx && \
    chown -R nginx:www /www

COPY site/ /www/site
COPY nginx/tentonpenguin.conf /etc/nginx/http.d/tentonpenguin.conf
COPY ddclient/ddclient.conf /etc/ddclient/ddclient.conf

RUN rc-update add ddclient default

ENTRYPOINT nginx -g 'daemon off;'