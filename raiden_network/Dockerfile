# docker build -t raiden_network-env:v0.4.0 .

FROM chech0x/eth-populus-dev:latest
LABEL maintainer="Sergio Campos <chech0x@gmail.com>"

ARG RAIDEN_RLEASE_VER="v0.4.0"
ARG RAIDEN_BINARY_NAME="raiden-0.4.0-linux"

RUN cd /root && \
 curl -L -O https://github.com/raiden-network/raiden/releases/download/$RAIDEN_RLEASE_VER/raiden-$RAIDEN_RLEASE_VER-linux.tar.gz && \
 tar -xvzf raiden-$RAIDEN_RLEASE_VER-linux.tar.gz && \
 mv $RAIDEN_BINARY_NAME /usr/bin/raiden && \
 chmod +x /usr/bin/raiden

WORKDIR /root/workdir

CMD ["/bin/bash"]
