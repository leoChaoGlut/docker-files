FROM index.tenxcloud.com/tenxcloud/ubuntu

MAINTAINER  leo leoiscoding@163.com

COPY sources.list /etc/apt/

RUN apt-get update && \
	apt-get install -y vim tar wget curl rsync bzip2 iptables tcpdump less telnet net-tools lsof expect locales && \ 
	rm -rf /var/lib/apt/lists/* && \
	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8

ENV LANG en_US.utf8

ENTRYPOINT /bin/bash /run.sh
