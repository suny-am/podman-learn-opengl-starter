FROM mcr.microsoft.com/devcontainers/cpp:1-debian-11

ARG REINSTALL_CMAKE_VERSION_FROM_SOURCE="none"

COPY ./reinstall-cmake.sh /tmp/
COPY ./glad.zip /tmp/

RUN \
    if [ "${REINSTALL_CMAKE_VERSION_FROM_SOURCE}" != "none" ]; then \
        chmod +x /tmp/reinstall-cmake.sh && /tmp/reinstall-cmake.sh ${REINSTALL_CMAKE_VERSION_FROM_SOURCE}; \
    fi && \
    rm -f /tmp/reinstall-cmake.sh && \
    sudo apt-get update && \
    export DEBIAN_FRONTEND=noninteractive && \
    sudo apt-get -y install --no-install-recommends libwayland-dev libxkbcommon-dev xorg-dev && \
    sudo apt-get install -y cmake pkg-config  && \
    sudo apt-get install -y mesa-utils libglu1-mesa-dev freeglut3-dev mesa-common-dev  && \
    sudo apt-get install -y libglew-dev libglfw3-dev libglm-dev  && \
    sudo apt-get install -y libao-dev libmpg123-dev
    
WORKDIR /usr/local/lib/
RUN  \  
    git clone https://github.com/glfw/glfw.git && \
    cd glfw && \
    cmake . && \
    make && \
    sudo make install && \
    unzip /tmp/glad.zip -d /tmp/ && \
    cp -R /tmp/include/* /usr/include/ && \
    mkdir /workspace  && \
    cp -R /tmp/src/* /workspace/*
    rm -rf /tmp/glad.zip /tmp/include