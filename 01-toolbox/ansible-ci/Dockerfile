FROM alpine:3.16

RUN apk add --no-cache mysql-client make python3 python3-dev py3-pip bash gcc musl-dev libffi-dev openssh-client curl
RUN ln -sf python3 /usr/bin/python
RUN ln -sf pip3 /usr/bin/pip
RUN /usr/bin/pip install --no-cache --upgrade pip setuptools
COPY requirements.txt /tmp/requirements.txt
RUN /usr/bin/pip install -Ur /tmp/requirements.txt

WORKDIR /ansible
