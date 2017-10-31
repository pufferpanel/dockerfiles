####
# Docker: Minecraft
#
# Builds a docker image for running a Java based Minecraft server using pufferd.
####

FROM        ubuntu:16.04

RUN         useradd -m -d /server pufferd

## Add any additional commands here
RUN 		apt-get update && apt-get install -y \
              openjdk-8-jre \
			  openjdk-8-jdk \
			&& rm -rf /var/lib/apt/lists/*
##

USER        pufferd

ENV         DEBIAN_FRONTEND noninteractive
ENV 		HOME  /server

WORKDIR 	/server

CMD         ["/bin/bash"]



