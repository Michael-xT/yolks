FROM        ubuntu:latest

EXPOSE      7788/udp
EXPOSE      7788/tcp
LABEL       author="Mike" maintainer="mike"

RUN         apt-get update && apt-get install -y libc-bin libatomic1 wget jq curl 

RUN         useradd -m -d /home/container container

USER        container
ENV         USER=container HOME=/home/container
WORKDIR     /home/container

EXPOSE      7788/udp
EXPOSE      7788/tcp

COPY        ./../entrypoint.sh /entrypoint.sh
CMD         ["/bin/bash", "/entrypoint.sh"]


EXPOSE      7788/udp
EXPOSE      7788/tcp