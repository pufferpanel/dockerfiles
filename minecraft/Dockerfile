####
# Docker: Minecraft
#
# Builds a docker image for running a Java based Minecraft server using pufferd.
####

FROM        pufferpanel:generic

RUN 		apt-get update && apt-get install -y \
              openjdk-8-jre \
			  openjdk-8-jdk \
			&& rm -rf /var/lib/apt/lists/*
