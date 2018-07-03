FROM ubuntu:16.04

MAINTAINER bao.ho hogiabao2601@gmail.com

RUN apt-get update -y && \
    apt-get upgrade -y && \
    apt-get install -y \
    sudo vim gcc wget \
    openssh-client \
    build-essential \
    libreadline-dev \
    zlib1g-dev net-tools \
    iputils-ping \
    xinetd openssl \
    software-properties-common \
    libssl-dev telnet && \
    useradd -m ubuntu && \
    echo "ubuntu:ubuntu" | chpasswd && \
    adduser ubuntu sudo && \
    echo "ubuntu ALL=(ALL) NOPASSWD: ALL" >> /etc/sudoers && \
    echo 'alias ll="ls -lah"' >> /etc/environment

USER ubuntu

WORKDIR /home/ubuntu

CMD /bin/bash