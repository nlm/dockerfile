FROM ubuntu:latest
MAINTAINER Nicolas Limage <nlimage@online.net>
RUN apt-get update
RUN apt-get -y install software-properties-common
RUN add-apt-repository ppa:formorer/icinga
RUN apt-get update
RUN apt-get -y install icinga2
RUN mkdir /run/icinga2 && chown nagios:nagios /run/icinga2
CMD ["/usr/sbin/icinga2", "daemon", "-c", "/etc/icinga2/icinga2.conf"]
