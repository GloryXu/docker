# Version: 0.0.1
FROM ubuntu:14.04
MAINTAINER Glory  "glory@example.com"
RUN cp /etc/apt/sources.list /etc/apt/sources.list.bak
RUN rm /etc/apt/sources.list

RUN echo "deb http://mirrors.aliyun.com/ubuntu/ trusty main restricted universe multiverse \ndeb http://mirrors.aliyun.com/ubuntu/ trusty-security main restricted universe multiverse \ndeb http://mirrors.aliyun.com/ubuntu/ trusty-updates main restricted universe multiverse \ndeb http://mirrors.aliyun.com/ubuntu/ trusty-proposed main restricted universe multiverse \ndeb http://mirrors.aliyun.com/ubuntu/ trusty-backports main restricted universe multiverse \ndeb-src http://mirrors.aliyun.com/ubuntu/ trusty main restricted universe multiverse \ndeb-src http://mirrors.aliyun.com/ubuntu/ trusty-security main restricted universe multiverse \ndeb-src http://mirrors.aliyun.com/ubuntu/ trusty-updates main restricted universe multiverse \ndeb-src http://mirrors.aliyun.com/ubuntu/ trusty-proposed main restricted universe multiverse \ndeb-src http://mirrors.aliyun.com/ubuntu/ trusty-backports main restricted universe multiverse \n" >> /etc/apt/sources.list
RUN apt-get update
RUN apt-get install -y net-tools
RUN apt-get install -y iputils-ping
RUN apt-get install -y iproute2
EXPOSE 80
