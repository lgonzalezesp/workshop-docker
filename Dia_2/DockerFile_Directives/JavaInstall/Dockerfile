FROM centos:latest
MAINTAINER lgonzalez@altiuz.com
RUN useradd -ms /bin/bash user
RUN echo "export 192.168.0.0/24" >> /etc/export.list
RUN yum install -y java-1.8.0-openjdk
USER user

RUN cd ~ && echo "export JAVA_HOME=/usr/lib/jvm/java-1.8.0-openjdk-1.8.0.201.b09-2.el7_6.x86_64" >> /home/user/.bashrc

ENV JAVA_BIN /usr/lib/jvm/java-1.8.0-openjdk-1.8.0.201.b09-2.el7_6.x86_64/jre/bin

