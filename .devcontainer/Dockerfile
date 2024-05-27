FROM debian:12

WORKDIR /workspace
RUN \
    export DEBIAN_FRONTEND=noninteractive && \
    apt-get update && \ 
    apt-get install -y --no-install-recommends cmake \
    make \
    build-essential \
    libxi-dev \
    libxrandr-dev \
    libxinerama-dev \
    libxcursor-dev \
    libgl1-mesa-dev \
    xorg-dev \
    git \
    ca-certificates && \ 
    git clone --recursive https://github.com/Polytonic/Glitter.git && \
    rm -rf Glitter/.git*