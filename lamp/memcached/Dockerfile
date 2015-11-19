FROM ubuntu:latest
MAINTAINER nlimage@online.net
RUN apt-get update
RUN apt-get -y install memcached
EXPOSE 11211
CMD ["/usr/bin/memcached", "-u", "memcache"]
