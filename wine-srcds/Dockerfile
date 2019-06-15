# Dockerfile for running a SRCDS based Windows server using pufferd and wine.
FROM ubuntu:16.04
RUN useradd -m -d /server pufferd
WORKDIR /server

RUN dpkg --add-architecture i386 && \
    apt-get update && \
    apt-get install -y openssl curl tar git \
      lib32gcc1 lib32tinfo5 lib32z1 lib32stdc++6 \
      libtinfo5:i386 libncurses5:i386 libcurl3-gnutls:i386 && \
    curl -sS 'https://dl.winehq.org/wine-builds/winehq.key' | apt-key add -- && \
    echo 'deb http://dl.winehq.org/wine-builds/ubuntu/ xenial main' > /etc/apt/sources.list.d/wine.list && \
    apt-get update && apt-get install -y --install-recommends  winehq-stable libntlm0 winbind && \
    rm -rf /var/lib/apt/lists/*

USER pufferd:pufferd
ENV HOME /server
ENV WINEPREFIX /server/.wine64
ENV WINEARCH win64
