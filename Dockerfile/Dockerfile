# FROM jenkins/jenkins:lts
# # FROM ubuntu:20.04
# # if we want to install via apt
# USER root
# RUN apt-get update && apt-get install -y make && apt-get install -y g++ --fix-missing

# # drop back to the regular jenkins user - good practice

# USER jenkins

# Use official Jenkins LTS image
FROM jenkins/jenkins:lts

USER root

RUN apt-get update && \
    apt-get install -y apt-transport-https ca-certificates && \
    apt-get update && \
    apt-get install -y make g++ --fix-missing && \
    rm -rf /var/lib/apt/lists/*

USER jenkins







