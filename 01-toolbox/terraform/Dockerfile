ARG ARCH
###############################################################################
# Base image
###############################################################################
FROM ${ARCH}/alpine:3.16

# Install Tools
RUN apk add terraform --repository=https://dl-cdn.alpinelinux.org/alpine/edge/community

RUN apk add --no-cache --update bash jq make git openssh-client aws-cli 

RUN adduser -D -g 'terraform' terraform

WORKDIR /home/terraform

USER terraform:terraform
