FROM ubuntu:latest
MAINTAINER Nicolas Limage <nlimage@online.net>
RUN apt-get -q update
RUN apt-get -y install unbound dnsutils
EXPOSE 53/udp 53/tcp 8953/tcp
CMD ["/usr/sbin/unbound", "-d"]
