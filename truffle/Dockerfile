# docker build -t eth-truffle-dev:0.0.1 .
FROM alpine:3.8
LABEL maintainer="Sergio Campos <chech0x@gmail.com>"


RUN apk add -u --no-cache nodejs nodejs-npm git autoconf build-base python curl openssh-client openssl openssl-dev && \
 mpn install -g npm@6 && \
 npm install -g truffle && \
 npm install -g ganache-cli && \
 npm install -g zeppelin-solidity && \
 mkdir -p /root/workdir && \
 curl -L -o solc https://github.com/ethereum/solidity/releases/download/v0.4.24/solc-static-linux && \
 chmod +x solc  && \
 mv solc /usr/bin/




WORKDIR /root/workdir


CMD ["/bin/sh"]
