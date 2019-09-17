FROM centos
MAINTAINER      op@coohua.com
RUN useradd coohua \
;mkdir -p /app/3rd\
;mkdir  -p /app/coohua/apps  \
;mkdir -p /data/coohua/logs/tomcat \
;chown -R coohua:coohua /app/coohua/ /data/coohua \
;ln -sf /usr/share/zoneinfo/Asia/Shanghai  /etc/localtime && /usr/bin/yum -y install net-tools  telnet tcpdump iproute  && /usr/bin/yum clean all && ln -s /app/3rd/mysql/default/bin/mysql /usr/bin/mysql && ln -s /app/3rd/redis/default/bin/redis-cli /usr/bin/redis-cli && echo 'alias log="ll=ls -l"' >> ~/.bashrc
ADD jdk.gz /app/3rd/
COPY mysql /app/3rd/mysql/default/bin/
COPY redis-cli /app/3rd/redis/default/bin/
ENV JAVA_HOME /app/3rd/jdk/default
ENV PATH $PATH:/$JAVA_HOME/bin
ENV LANG en_US.UTF-8
