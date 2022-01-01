FROM        ubuntu:latest

LABEL       author="Mike" maintainer="mike"

RUN         apt update && apt upgrade && apt-get install libc-bin libatomic1 wget jq curl -y 

RUN         useradd -m -d /home/container container

USER        container
ENV         USER=container HOME=/home/container
WORKDIR     /home/container

EXPOSE      7788/udp
EXPOSE      7788/tcp

COPY        ./../entrypoint.sh /entrypoint.sh
CMD         ["/bin/bash", "/entrypoint.sh"]