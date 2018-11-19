FROM glory/self_docker:14.04
MAINTAINER Glory Xu
ENV REFRESHED_AT 2018-11-18
RUN apt-get update
RUN apt-get -y install ruby ruby-dev build-essential redis-tools

# install ruby 2.2.2
RUN gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3
RUN apt-get -y install curl
RUN \curl -sSL https://get.rvm.io | bash -s stable
#RUN source ~/.bashrc
RUN /bin/bash -c "source ~/.bashrc"
RUN mkdir -p ~/.rvm/user
RUN echo "ruby_url=https://cache.ruby-china.org/pub/ruby" > ~/.rvm/user/db
RUN /bin/bash -c  "source /etc/profile.d/rvm.sh"
RUN /etc/profile.d/rvm.sh install 2.2.2 --disable-binary
RUN /etc/profile.d/rvm.sh use 2.2.2 --default


RUN gem install --no-rdoc --no-ri sinatra json redis


RUN mkdir -p /opt/webapp

EXPOSE 4567

CMD ["/opt/webapp/bin/webapp"]
