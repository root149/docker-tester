FROM ubuntu:latest
ENV TZ=Asia/Yekaterinburg
ENV LANG en_US.utf8

RUN apt-get update && \
    apt-get install -y locales && \
    ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone && \
    localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8 && \    
    apt upgrade -y && \
    apt-get install -y telnet curl w3m mtr-tiny mc wget jmeter jmeter-tcp jmeter-http iputils-ping iputils-tracepath traceroute dnsutils  -y && \
    rm -rf /var/lib/apt/lists/*

