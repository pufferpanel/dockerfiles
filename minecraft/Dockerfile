####
# Docker: Minecraft
#
# Builds a docker image for running a Java based Minecraft server using pufferd.
####

FROM        openjdk:8-jdk

ENV         DEBIAN_FRONTEND noninteractive

RUN         useradd -m -d /home/pufferd pufferd

USER        pufferd

CMD         ["/bin/bash"]
