FROM glory/self_docker:14.04
MAINTAINER Glory Xu
ENV REFRESHED_AT 2018-11-18
RUN apt-get update && apt-get -y install ruby ruby-dev build-essential redis-tools

# install ruby 2.2.2
RUN gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3
RUN apt-get -y install curl && \curl -sSL https://get.rvm.io | bash -s stable

#添加rvm可执行路径到环境变量PATH
ENV PATH "$PATH:/usr/local/rvm/bin"

RUN mkdir -p ~/.rvm/user && echo "ruby_url=https://cache.ruby-china.org/pub/ruby" > ~/.rvm/user/db
# 让source能正常执行
RUN rm /bin/sh && ln -s /bin/bash /bin/sh

#使用rvm安装ruby 2.2.2.
RUN source /etc/profile.d/rvm.sh && /usr/local/rvm/bin/rvm reload && /usr/local/rvm/bin/rvm install 2.2.2
#添加ruby可执行路径到环境变量PATH
RUN rm -rf /usr/bin/ruby && ln -s /usr/local/rvm/rubies/ruby-2.2.2/bin/ruby /usr/bin/ruby

ENV PATH="$PATH:/usr/bin"
#gem是ruby软件包管理工具，类似linux的rpm，移除官方地址添加阿里云的地址
RUN gem source -r https://rubygems.org/ && gem source -a http://mirrors.aliyun.com/rubygems/

RUN gem install --no-rdoc --no-ri sinatra json redis

RUN mkdir -p /opt/webapp

EXPOSE 4567

CMD ["/opt/webapp/bin/webapp"]
