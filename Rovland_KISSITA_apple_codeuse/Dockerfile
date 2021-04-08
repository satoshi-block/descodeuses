FROM jenkins/jenkins:lts
# root user will be used for packages installation to avoid permission denied
USER root
# Packages installation
RUN apt-get update && apt-get install -y ruby make
# drop back to the regular jenkins user
USER jenkins

