####
# Docker: SRCDS
#
# Builds a docker image for running a SRCDS server using pufferd.
####

FROM        pufferpanel:generic

RUN         apt-get update && apt-get install -y \
              openssl \
              curl \
              git \
              tar \
              python \
              lib32gcc1 \
              lib32tinfo5 \
              lib32z1 \
              lib32stdc++6 \
           && rm -rf /var/lib/apt/lists/*
