FROM leo_ubuntu:14.04

MAINTAINER  leo leoiscoding@163.com

RUN mkdir -p /usr/env && \
	apt-get update && \ 
	apt-get install -y make gcc tcl8.6 ruby && \
	rm -rf /var/lib/apt/lists/* && \
	gem sources --add https://gems.ruby-china.org/ --remove https://rubygems.org/ && \
	gem install redis

ADD redis-3.2.8.tar.gz /usr/env

RUN cd /usr/env/redis-3.2.8 && \
	make && make test && \
	apt-get autoremove --purge -y gcc make tcl8.6

ENTRYPOINT /bin/bash /run.sh
