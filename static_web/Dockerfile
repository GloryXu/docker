# Version: 0.0.1
FROM glory/self_docker:latest
MAINTAINER Glory Turnbull "glory@example.com"
RUN apt-get update
RUN apt-get install -y nginx
RUN echo 'Hi, I am in your container' \
	>/usr/share/nginx/html/index.html
EXPOSE 80
