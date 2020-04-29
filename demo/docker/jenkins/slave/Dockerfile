FROM centos:7
ENV container docker

RUN yum -y install git; \
yum clean all;

# set environment variables
ENV JAVA_HOME=/var/jenkins_home/tools/hudson.model.JDK/jdk1.8.0_221
ENV JRE_HOME=/$JAVA_HOME/jre
ENV CLASSPATH=.:$JAVA_HOME/jre/lib/rt.jar:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar
ENV PATH=$PATH:$JAVA_HOME/bin:$JRE_HOME/bin

# docker build --rm -t local/centos7-jenkins-slave .
