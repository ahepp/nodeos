FROM debian:bookworm-slim

RUN dpkg-reconfigure debconf -f noninteractive -p critical \
    && echo 'root:root' | chpasswd \
    && groupadd -g 1000 dev \
    && useradd -m -u 1000 -g dev dev

RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        bc \
        build-essential \
        ca-certificates \
        cpio \
        file \
        libncurses-dev \
        python3 \
        rsync \
        unzip \
        wget

USER dev
