FROM alpine:3.16

RUN addgroup www
RUN adduser -D -g 'www' nginx

RUN apk update && apk add nginx

RUN mkdir /www && \
    chown -R nginx:www /var/lib/nginx && \
    chown -R nginx:www /www

COPY site.conf /etc/nginx/http.d/default.conf
COPY site/ /www/site

ENTRYPOINT nginx -g 'daemon off;'