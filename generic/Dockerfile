####
# Docker: Generic
#
# Builds a docker image used by pufferd when a specific image is not specified.
####

FROM        ubuntu:16.04

RUN         useradd -m -d /server pufferd

## Add any additional commands here

##

USER        pufferd:pufferd

ENV         DEBIAN_FRONTEND noninteractive
ENV 		HOME  /server

WORKDIR 	/server

CMD         ["/bin/bash"]
