FROM ubuntu:latest
MAINTAINER nlimage@online.net
RUN apt-get update
RUN apt-get -y install apache2
RUN mkdir /var/run/apache2
RUN mkdir /var/lock/apache2 && chgrp www-data /var/lock/apache2 && chmod 770 /var/lock/apache2
ENV APACHE_LOCK_DIR /var/lock/apache2
ENV APACHE_PID_FILE /var/run/apache2.pid
ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data
ENV APACHE_LOG_DIR /var/log/apache2
EXPOSE 80
CMD ["/usr/sbin/apache2", "-DFOREGROUND"]
