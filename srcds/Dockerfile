####
# Docker: SRCDS
#
# Builds a docker image for running a SRCDS server using pufferd.
####

FROM        ubuntu:16.04

RUN         useradd -m -d /server pufferd

## Add any additional commands here

RUN         dpkg --add-architecture i386 && \
            apt-get update && \
            apt-get install -y \
              openssl \
              curl \
              git \
              tar \
              python \
              lib32gcc1 \
              lib32tinfo5 \
              lib32z1 \
              lib32stdc++6 \
              libcurl3-gnutls:i386 \
           && rm -rf /var/lib/apt/lists/*
##

USER        pufferd:pufferd

ENV         DEBIAN_FRONTEND noninteractive
ENV 		HOME  /server

WORKDIR 	/server

CMD         ["/bin/bash"]
