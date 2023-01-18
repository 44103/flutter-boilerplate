FROM ubuntu:20.04

RUN export DEBIAN_FRONTEND="noninteractive" && \
    apt-get update && apt-get -y install --no-install-recommends \
    git \
    zsh \
    vim \
    unzip clang xserver-xorg pkg-config libgtk-3-dev curl cmake ninja-build \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*
RUN git clone https://github.com/flutter/flutter.git && \
    mv flutter /opt/

ENV TZ=Asia/Tokyo
RUN zsh -c "`curl -L raw.github.com/44103/dotfiles/main/install.sh`"