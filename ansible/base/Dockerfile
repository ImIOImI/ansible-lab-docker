# BASE image - used as a starting point by MASTER and HOST images

FROM ubuntu:latest

# install required packages
RUN apt-get update && \
    apt-get install software-properties-common -y && \
    add-apt-repository ppa:deadsnakes/ppa -y && \
    apt-get update && \
    apt-get install python3 && \
    apt-get install --no-install-recommends --no-install-suggests -y \
        aptitude iputils-ping net-tools man vim openssh-server && \
    rm -rf /var/lib/apt/lists/*

# ensure that required directories are created
RUN mkdir /var/run/sshd
RUN mkdir /root/.ssh
