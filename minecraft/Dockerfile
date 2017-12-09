# Dockerfile for running a Java based Minecraft server using pufferd.
FROM debian:9.2
RUN useradd -m -d /server pufferd
WORKDIR /server

# Add any additional commands here
RUN apt-get update && \
    apt-get install -y --no-install-recommends openjdk-8-jre openjdk-8-jdk git && \
    rm -rf /var/lib/apt/lists/*

USER pufferd
