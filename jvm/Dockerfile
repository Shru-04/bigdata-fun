FROM centos:8
MAINTAINER Karl Stoney <me@karlstoney.com> 

VOLUME /data

ENV JAVA_HOME /usr/lib/jvm/jre-1.8.0-openjdk
ENV JAVA_OPTS "-Xms512m -Xmx2g"
ENV TERM xterm-256color

# Get dependencies
RUN sed -i 's/mirrorlist/#mirrorlist/g' /etc/yum.repos.d/CentOS-Linux-*
RUN sed -i 's|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g' /etc/yum.repos.d/CentOS-Linux-*
RUN yum updateinfo
RUN yum -y -q install curl wget java-1.8.0-openjdk-headless

CMD ["/bin/true"]
