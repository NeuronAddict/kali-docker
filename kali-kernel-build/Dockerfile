FROM kalilinux/kali-rolling

ARG TOOLCHAIN_REPO
ARG TOOLCHAIN_BRANCH

ENV ARCH=arm64
ENV SUBARCH=arm64
ENV CROSS_COMPILE=/toolchain64/bin/aarch64-linux-android-

ENV CFLAGS="-Wno-error"
ENV CCFLAGS="-Wno-error"
ENV CXXFLAGS="-Wno-error"

RUN apt-get update && apt-get -y install \
        build-essential \
        clang \
        libelf-dev \
        libssl-dev \
        libncurses5-dev \
        fakeroot \
        git \
        python \
        zip

WORKDIR /src

RUN git clone $TOOLCHAIN_REPO -b $TOOLCHAIN_BRANCH /toolchain64
