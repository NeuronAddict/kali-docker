FROM kalilinux/kali-rolling

ARG TOOLCHAIN_REPO
ARG TOOLCHAIN_BRANCH

ENV ARCH=arm64
ENV SUBARCH=arm64
ENV CROSS_COMPILE=/toolchain64/bin/aarch64-linux-android-

RUN apt-get update && apt-get -y install \
        build-essential \
        libelf-dev \
        libssl-dev \
        libncurses5-dev \
        fakeroot \
        git \
        zip

WORKDIR /src

RUN git clone $TOOLCHAIN_REPO -b $TOOLCHAIN_BRANCH /toolchain64
