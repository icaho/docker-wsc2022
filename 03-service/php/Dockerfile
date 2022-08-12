FROM alpine:3.16

RUN addgroup web
RUN adduser -D -g 'web' php

RUN apk update && apk add --no-cache php

RUN mkdir /site && \
    chown -R php:web /site

USER php

COPY site/ /site/

ENTRYPOINT ["php", "-S", "0.0.0.0:8000"] 
CMD ["/site/hello.php"]