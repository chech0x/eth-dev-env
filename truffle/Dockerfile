# docker build -t eth-truffle-dev:0.0.1 .
FROM alpine:3.9.4
LABEL maintainer="Sergio Campos <chech0x@gmail.com>"


RUN apk update --no-cache --purge && apk upgrade --no-cache --purge && apk add -u --no-cache nodejs-current npm git autoconf python build-base curl openssh-client openssl openssl-dev && \
 npm install -g npm@latest && \
 solcLatestVersion=$(curl -sL https://github.com/ethereum/solidity/releases/latest | grep 'solc-static-linux"' | sed -r 's/.*(v\d+.\d+.\d+).*/\1/g') && \
 curl -L -o solc https://github.com/ethereum/solidity/releases/download/$solcLatestVersion/solc-static-linux && \
 chmod +x solc  && \
 mv solc /usr/bin/ && \
 addgroup -S developer && adduser -S developer -G developer

 
 RUN npm install --no-optional -g truffle@latest && \
 npm install -g ganache-cli@latest && \
 npm install -g openzeppelin-solidity@latest
 

USER developer 

RUN mkdir -p /home/developer/workdir && \
 chown developer:developer /home/developer/workdir 

WORKDIR /home/developer/workdir


CMD ["/bin/sh"]
