FROM centos:latest
MAINTAINER lgonzalez@altiuz.com
RUN yum  update -y
RUN yum install -y httpd net-tools

RUN echo "this is a custom index file build during the image creation" > /var/www/html/index.html
ENTRYPOINT apachectl "-DFOREGROUND"