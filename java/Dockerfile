############################################################
# Dockerfile to create a Cassandra Node
# Based on Ubuntu image
############################################################

FROM ubuntu
MAINTAINER Ivo Correia

ENV JAVA_HOME /opt/java
ENV TERM linux
ENV PATH=$PATH:/opt/java/bin

# Update repository and install required tools.
RUN sudo apt-get update
RUN sudo apt-get -y install wget vim telnet curl

############################################################
# Install Java.
RUN wget --no-cookies --header "Cookie: oraclelicense=accept-securebackup-cookie" 'http://download.oracle.com/otn-pub/java/jdk/8u74-b02/jdk-8u74-linux-x64.tar.gz'
RUN tar xvf jdk-8u74-linux-x64.tar.gz
RUN mv jdk1.8.0_74 opt/java
RUN rm jdk-8u74-linux-x64.tar.gz

CMD /bin/bash
