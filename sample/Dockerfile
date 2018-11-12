FROM glory/self_docker:latest
MAINTAINER Glory Turnbull "guangrong_xu@126.com"
ENV REFRESHED_AT 2018-11-12
RUN apt-get update
RUN apt-get -y -q install nginx
RUN mkdir -p /var/www/html
ADD nginx/global.conf /etc/nginx/conf.d/
ADD nginx/nginx.conf /etc/nginx/nginx.conf
EXPOSE 80
