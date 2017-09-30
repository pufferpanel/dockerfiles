####
# Docker: Generic
#
# Builds a docker image used by pufferd when a specific image is not specified.
####

FROM        ubuntu:16.04

ENV         DEBIAN_FRONTEND noninteractive

RUN         useradd -m -d /home/pufferd pufferd

USER        pufferd

CMD         ["/bin/bash"]
