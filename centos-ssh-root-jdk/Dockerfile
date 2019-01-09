FROM glory/centos-ssh-root
ADD /home/glory/Downloads/jdk-8u191-linux-x64.tar.gz /usr/local/
RUN mv /usr/local/jdk1.8.0_191 /usr/local/jdk1.8
ENV JAVA_HOME /usr/local/jdk1.8
ENV PATH $JAVA_HOME/bin:$PATH