FROM buildpack-deps:xenial

RUN dpkg --add-architecture i386
RUN apt-get update
RUN apt-get upgrade -y

RUN apt-get install -y git cmake pkg-config

# install msa deps
RUN apt-get install -y libcurl4-openssl-dev libssl-dev libgl1-mesa-dev
# install mcpelauncher deps
RUN apt-get install -y libssl-dev:i386 g++-multilib libpng-dev:i386 libx11-dev:i386 libxi-dev:i386 libudev-dev:i386 libevdev-dev:i386 libegl1-mesa-dev:i386
# install mcpelauncher-ui deps
RUN apt-get install -y libuv1-dev libzip-dev libprotobuf-dev protobuf-compiler

# install Qt 5.9
RUN apt-get install -y software-properties-common
RUN add-apt-repository -y ppa:beineri/opt-qt596-xenial
RUN apt-get update
RUN apt-get install -y qt59base qt59declarative qt59quickcontrols qt59quickcontrols2 qt59svg qt59webengine
