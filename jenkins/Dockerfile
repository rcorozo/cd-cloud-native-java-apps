FROM jenkins/jenkins:lts-jdk11
 
USER root
RUN apt-get update \
      && apt-get install -y sudo \
      && rm -rf /var/lib/apt/lists/*
RUN echo "jenkins ALL=NOPASSWD: ALL" >> /etc/sudoers

# Install extra plugins

RUN \
    jenkins-plugin-cli --plugins "docker-workflow:1.26 github-oauth:0.34 git-changelog:3.13 github-checks:1.0.19"

USER jenkins
