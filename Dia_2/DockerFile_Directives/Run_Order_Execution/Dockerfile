FROM centos:latest
MAINTAINER lgonzalez@altiuz.com

RUN useradd -ms /bin/bash user
RUN echo "export 192.168.0.0/24" >> /etc/export.list
USER user

