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
    axel \
	bc \
    build-essential \
    clang \
    curl \
    libelf-dev \
    libssl-dev \
    libncurses5-dev \
    fakeroot \
    git \
    python \
    sudo \
    zip

WORKDIR /src

RUN git clone $TOOLCHAIN_REPO --single-branch -b $TOOLCHAIN_BRANCH /toolchain64

CMD ["sh", "-c",  "cd $SRC_SUBDIR && make help && make $MAKE_CONFIG && make menuconfig && make -j4"]