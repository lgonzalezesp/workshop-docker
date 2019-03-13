#Dockerfile based on the latest CentOs 7 Image - non-privileged user entry
FROM centos:latest
MAINTAINER lgonzalez@altiuz.com

RUN useradd -ms /bin/bash user
CMD "echo" "This a custom container message for our LinuxAcademy Students"
USER user