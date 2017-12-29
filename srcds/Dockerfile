# Dockerfile for running a SRCDS server using pufferd.
FROM ubuntu:16.04
WORKDIR /server

RUN dpkg --add-architecture i386 && \
    apt-get update && \
    apt-get install -y openssl curl tar git \
      lib32gcc1 lib32tinfo5 lib32z1 lib32stdc++6 \
      libtinfo5:i386 libncurses5:i386 libcurl3-gnutls:i386 && \
    rm -rf /var/lib/apt/lists/*

RUN addgroup --gid 1000 pufferd && \
    adduser --uid 1000 --ingroup pufferd --home /server --shell /bin/bash --disabled-password --gecos "" pufferd

RUN USER=pufferd && \
    GROUP=pufferd && \
    curl -SsL https://github.com/boxboat/fixuid/releases/download/v0.2/fixuid-0.2-linux-amd64.tar.gz | tar -C /usr/local/bin -xzf - && \
    chown root:root /usr/local/bin/fixuid && \
    chmod 4755 /usr/local/bin/fixuid && \
    mkdir -p /etc/fixuid && \
    printf "user: $USER\ngroup: $GROUP\n" > /etc/fixuid/config.yml

USER pufferd:pufferd
ENV HOME /server
ENTRYPOINT ["fixuid"]
