FROM        --platform=$TARGETOS/$TARGETARCH python:3.9.9-slim-buster

LABEL       author="Mike" maintainer="mike"

RUN         apt update \
    && apt-get install python3-dev default-libmysqlclient-dev gcc -y \
    && useradd -m -d /home/container container

USER        container
ENV         USER=container HOME=/home/container
WORKDIR     /home/container

COPY        ./../entrypoint.sh /entrypoint.sh
CMD         ["/bin/bash", "/entrypoint.sh"]