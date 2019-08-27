ARG VERSION=lts
FROM jenkins/jenkins:$VERSION

MAINTAINER rodriggoarantes
LABEL maintainer="rodriggoarantes@gmail.com"

USER root
RUN mkdir /var/log/jenkins
RUN chown -R  jenkins:jenkins /var/log/jenkins
USER jenkins

ENV JAVA_OPTS="-Xmx1024m"
ENV JENKINS_OPTS=" --handlerCountMax=100 --logfile=/var/log/jenkins/jenkins.log"

VOLUME jenkins_home:/var/jenkins_home

EXPOSE 8080
EXPOSE 50000