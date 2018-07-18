# docker build -t eth-dev-populus:0.0.1 .
#FROM alpine:3.7
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


RUN /usr/bin/python3.6

## RUN cd /root && \
##  apk add --update --no-cache --no-cache openjdk8 python3 python3-dev curl git openssl autoconf automake build-base libffi libffi-dev openssl-dev && \
##  curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py && \
##  python3 get-pip.py && \
##  rm get-pip.py && \
## # pip install "populus>=2.2.0" "web3==v4.0.0-beta.4" && \
## # pip install "web3==v4.0.0-beta.4" && \
##  mkdir -p /root/workdir


WORKDIR /root/workdir


CMD ["/bin/bash"]
