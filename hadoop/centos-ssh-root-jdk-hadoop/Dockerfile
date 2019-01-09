FROM glory/centos-ssh-root-jdk
ADD hadoop-2.9.2.tar.gz /usr/local
RUN mv /usr/local/hadoop-2.9.2 /usr/local/hadoop
ENV HADOOP_HOME /usr/local/hadoop
ENV PATH $HADOOP_HOME/bin:$PATH