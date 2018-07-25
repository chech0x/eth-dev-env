# docker build -t eth-populus-dev:0.0.1 .
FROM centos:7
LABEL maintainer="Sergio Campos <chech0x@gmail.com>"

ENV JAVA_HOME /usr/lib/jvm/java-1.8-openjdk
ENV PATH $PATH:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin


RUN cd /root && \
 yum update -y && \
 yum -y install deltarpm yum-utils  && \
 yum -y groupinstall development && \
 yum -y install https://centos7.iuscommunity.org/ius-release.rpm && \
 yum install -y python36u python36u-libs python36u-devel python36u-pip && \
 yum install -y which git openssl autoconf automake openssl-devel java-1.8.0-openjdk && \
 yum clean all && \
 pip3.6 install --upgrade pip "rlp<=0.6.0,>=0.4.7" && \
 pip3.6 install --no-cache  "populus>=2.2.0" "web3==v4.0.0-beta.4" "web3==v4.0.0-beta.4"

RUN curl -L -o solc https://github.com/ethereum/solidity/releases/download/v0.4.24/solc-static-linux && \
 chmod +x solc && \
 mv solc /usr/bin/


RUN echo "alias virtualp='python3.6 -m venv env && . env/bin/activate'" >> /root/.bashrc && \
 chmod +x /root/.bashrc

ENV LANG en_US.utf8

WORKDIR /root/workdir


CMD ["/bin/bash"]
