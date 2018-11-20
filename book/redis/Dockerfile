FROM glory/self_docker:14.04
MAINTAINER Glory Xu guangrong_xu@126.com
ENV REFRESHED_AT 2018-11-20
RUN apt-get update
RUN apt-get -y install redis-server redis-tools
EXPOSE 6379
ENTRYPOINT ["/usr/bin/redis-server"]
CMD []
