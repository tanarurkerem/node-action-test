FROM jenkins/jenkins:lts-jdk11
USER root
RUN apt-get update
RUN apt-get install -y nodejs npm
COPY config.xml /usr/share/jenkins/ref/jobs/project/config.xml
RUN chown -R jenkins.jenkins /var/jenkins_home
USER jenkins
RUN /usr/local/bin/install-plugins.sh git clover
