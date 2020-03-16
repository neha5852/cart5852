#Dockerfile for cart frontend
# DOCKERCOMMAND options
FROM index.docker.io/centos:7
RUN yum -y update
RUN yum -y install http php php-gd php-mysql
ADD code /var/www/html
ENV MY_DB_HOST_WRITE=test MY_DB_HOST_READ=test MY_DB_NAME=test MY_DB_USER=test MY_DB_PASS=test
RUN ln -sf /var/log/httpd/access_log  /dev/stdout
RUN ln -sf /var/log/httpd/error_log /dev/stderr
CMD ["httpd", "-D", "FOREGROUND"]
