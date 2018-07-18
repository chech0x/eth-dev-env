# docker build -t eth-dev-truffle:0.0.1 .
FROM alpine:3.7
LABEL maintainer="Sergio Campos <chech0x@gmail.com>"


RUN apk add --update nodejs nodejs-npm git autoconf build-base python && \
 npm install -g truffle && \
 npm install -g ganache-cli && \
 mkdir -p /root/workdir


WORKDIR /root/workdir


CMD ["/bin/sh"]
